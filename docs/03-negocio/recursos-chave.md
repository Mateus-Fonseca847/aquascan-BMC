# Business Model Canvas · Recursos-Chave

## Introdução

O AquaScan é um sistema de monitoramento de rios que mede o nível da água com sensores de baixo custo, instalados em conjunto com o cliente, e comunica o risco de transbordamento em porcentagem, cor e texto, com tempo estimado, por meio de um aplicativo gratuito para a população. Este documento descreve o bloco **Recursos-Chave** do Business Model Canvas: os ativos de que o negócio precisa para entregar a proposta de valor, alcançar os clientes e gerar receita, sejam eles equipamentos, sistemas, pessoas, insumos, dados, autorizações ou dinheiro.

Ao longo do texto são apresentados os recursos por categoria, o que já existe e o que está planejado, uma seção dedicada às **peças do protótipo e seus equivalentes em um rio real**, as dependências e os riscos de indisponibilidade e as hipóteses que ainda precisam ser validadas. As atividades que usam esses recursos ficam no bloco Atividades-Chave; os parceiros que os fornecem, em Parcerias-Chave; os valores, em Estrutura de Custos. **Este bloco distingue o que já existe do que está planejado**: o projeto está em fase de protótipo, e nenhuma estação opera em rio real.

**Legenda das evidências:** **Verificado** (fonte pública ou código nos repositórios) · **Vivência** (observação dos integrantes, moradores de Petrópolis, RJ) · **Pesquisa** (levantamento dos integrantes, fontes a anexar) · **Hipótese** (a validar, ver seção 6).

---

## 1. Visão geral

| Categoria | Recurso | Função |
|---|---|---|
| Físico | Protótipo de bancada (ESP32, sensor ultrassônico de nível, sensor de vazão de cano, display e LEDs) | Demonstrar a cadeia de medição, cálculo e sinalização na maquete |
| Físico | Estação de campo (controlador, sensor de nível de classe de campo, energia, comunicação, caixa e fixação) | Medir o nível de um rio real e enviar o dado à API |
| Físico | Insumos e peças de reposição | Fabricar estações e repor componentes |
| Físico | Bancada de testes e calibração | Montar, testar e calibrar antes de ir a campo |
| Físico | Equipamento e transporte de campo | Instalar e vistoriar as estações |
| Intelectual | Software: firmware, API coletora, banco de dados, aplicativo e painel da Defesa Civil | Coletar os dados dos sensores, calcular as métricas, armazenar o histórico e entregá-los a moradores e à Defesa Civil |
| Intelectual | Funções de cálculo das métricas: nível, tendência, previsão, risco, estatística, qualidade dos dados, eventos, diagnóstico e, quando houver equipamento, vazão e volume | Transformar leituras brutas em informação de decisão (seção 3.2) |
| Intelectual | Calibração por ponto (cota de transbordamento e limiares de risco) | Tornar a porcentagem e o risco válidos em cada rio |
| Intelectual | Base geográfica (mapa dos rios, ruas, estações, pontos de apoio) e locais salvos do usuário | Mostrar todos os rios monitorados, associar cada rua à sua estação e permitir acompanhar casa e trabalho |
| Intelectual | Mapa interativo e roteamento (provedor de mapas, motor de rotas sobre dados do OpenStreetMap e camada de áreas de risco) | Mostrar rotas entre locais e até os pontos de apoio, evitando áreas de risco ligadas aos rios monitorados |
| Intelectual | Histórico de leituras e eventos | Calibrar limiares e comprovar desempenho |
| Intelectual | Marca | Identificar o produto |
| Humano | Competências de software, campo, hidrologia e relacionamento institucional | Construir, instalar, calibrar e sustentar a operação |
| Financeiro | Capital para o primeiro lote, estoque de peças e operação | Sustentar o ciclo até a receita recorrente |
| Acessos | Autorização para instalar, cota de transbordamento por ponto e dados oficiais | Tornar a medição válida e legal |

---

## 2. Perguntas-chave

| Pergunta | Resposta |
|---|---|
| Quais recursos a proposta de valor exige? | Estação de nível de classe de campo, calibrada em cada ponto; **cota de transbordamento** de cada ponto (sem ela não há porcentagem); cálculo de risco e tempo estimado; API e aplicativo com mapa dos rios monitorados |
| De que precisamos para abastecer os canais? | Hospedagem da API e do banco com HTTPS, contas nas lojas de aplicativos, serviço de notificações push, provedor de mapas (previsto: Google Maps), motor de rotas, a lista de pontos de apoio da Defesa Civil e o painel do órgão. A instalação conjunta exige equipe e equipamento de campo |
| Quais ativos sustentam o relacionamento e a receita? | Estações funcionando e vistoriadas, estoque de peças para manutenção, suporte técnico ao contratante e o histórico de leituras de cada ponto |

---

## 3. Recursos por categoria

### 3.1 Físicos

**Protótipo de bancada (existente).** O repositório do firmware reúne o projeto físico e a simulação. O protótipo usa ESP32 DevKit V1, protoboard de 400 pontos, sensor ultrassônico JSN-SR04M-2 (nível), sensor de vazão YF-S201 (fluxo em cano), display OLED SSD1306, três LEDs (verde, amarelo e vermelho), resistores e jumpers, alimentado por USB (**verificado** na lista de materiais). A compilação foi aprovada (RAM 6,9% e Flash 23,1%) e a simulação no Wokwi foi aprovada, com um HC-SR04 e um botão no lugar dos sensores reais (**verificado** no registro de validação). **Não consta** ensaio físico com medições registradas contra uma referência, nem envio de dados pela rede. A seção 4 compara cada peça com o equivalente em campo.

**Estação de campo (a projetar).** Cada estação reunirá:

| Componente | Observação |
|---|---|
| Controlador | O chip ESP32 pode ser mantido, em placa própria soldada, com proteção contra surtos e reinício automático por falha (**hipótese**, seção 4) |
| Sensor de nível de classe de campo | Tipo ainda **não definido**: ultrassônico impermeável com compensação de temperatura, radar de nível ou sensor de pressão submerso (comparação na seção 4.2) |
| Sensor de temperatura | Necessário se o sensor de nível for ultrassônico sem compensação interna. O firmware atual fixa a velocidade do som em 343 m/s. O próprio repositório registra que a 30 °C o som é 1,9% mais rápido que o assumido, o que equivale a cerca de 5,7 cm a 3 m de distância (**verificado**) |
| Caixa vedada (IP65 ou superior) e fixação | Proteção contra chuva e suporte em ponte ou muro |
| Energia | Painel solar com controlador de carga e bateria, ou rede elétrica. Definição pendente, por ponto |
| Conectividade | Celular (NB-IoT, LTE-M ou 4G), Wi-Fi local, rádio ou satélite. Definição pendente (seção 4.4) |

**O que o protótipo não é.** O YF-S201 mede a água que passa **dentro de um cano**, não a corrente de um rio aberto, e não faz parte da estação de campo. A vazão em rio aberto exige equipamento hidrométrico próprio ou uma curva calibrada por ponto (seção 4.3).

**Insumos e reposição.** Componentes eletrônicos, cabos, caixas, conectores, baterias e peças de fixação. O estoque de reposição evita parada prolongada de uma estação em campo. Fornecedores e preços serão levantados em Estrutura de Custos.

**Bancada de testes e calibração.** Espaço para montar as estações, testar o sensor contra uma régua de referência e calibrar antes da instalação. Hoje não há local definido (**hipótese**).

**Equipamento e transporte de campo.** Trena ou régua de referência, multímetro, ferramentas de fixação, equipamento de proteção individual e deslocamento até os pontos. Como a instalação é conjunta, parte da logística pode ser dividida com o cliente (**hipótese**).

### 3.2 Intelectuais

**Software e fluxo de dados.** Os dados seguem o caminho: sensores, API coletora, funções de cálculo, banco de dados e aplicativo. O firmware do ESP32 mede, filtra e envia; a API (Node.js, Fastify, PostgreSQL com PostGIS) recebe, calcula as métricas e grava o histórico; o aplicativo (React Native com Expo) as apresenta; o painel da Defesa Civil é a visão institucional. Tudo está em repositórios do GitHub. A versão 0.1.0 da API e do aplicativo tem leituras, estações, histórico, rios, alertas, pontos de apoio e previsão de chuva, com simulador de estação e 35 testes automáticos (**verificado**). A estação física ainda não envia dados pela rede (**verificado** no README do firmware), e o painel da Defesa Civil está previsto e não existe na v0.1.0. O código ainda não tem licença definida; se for aberto, o que protege o negócio não é o código, e sim a operação, a calibração, os dados e a relação com o contratante.

**Métricas calculadas.** As funções da API produzem o conjunto de métricas abaixo, definido a partir do relatório técnico do sensor e do desenho do aplicativo.

| Grupo | Métricas | Origem |
|---|---|---|
| Nível | Nível atual em cm e em porcentagem da cota de transbordamento; metros restantes até transbordar; máximo, mínimo, média, mediana e variação | Sensor de nível e API |
| Tendência | Taxas de subida e descida (5, 10, 30 e 60 minutos); aceleração da subida | API |
| Previsão | Tempo estimado até o nível crítico; nível previsto em um intervalo | API |
| Risco | Estado em cor e texto (baixo, moderado, alto); índice de 0 a 100 | API |
| Estatística | Média, mediana, mínimo, máximo, desvio padrão, amplitude e percentis | API |
| Qualidade dos dados | Leituras impossíveis, saltos bruscos, sensor sem resposta, dados ausentes | Firmware e API |
| Eventos | Início da subida, pico, recessão, fim, duração e nível máximo de cada evento | API |
| Diagnóstico | Sensor funcionando, possível falha ou obstrução, perda de comunicação | Firmware e API |
| Relações e gráficos | Nível × tempo, taxa de subida × tempo, previsão × valor real | API e aplicativo |
| Vazão e volume | Vazão instantânea, média e máxima; volume acumulado; relação nível × vazão | YF-S201 (cano) |
| Clima | Previsão e classificação de chuva | Open-Meteo, via API |
| Usuário | Locais salvos (casa e trabalho); pontos de apoio com telefone, capacidade máxima e rota até o local; rota entre locais que evita áreas de risco ligadas aos rios | Aplicativo, lista de pontos de apoio da Defesa Civil e motor de rotas |

O aplicativo mostra o mapa com todos os rios monitorados e, em cada rio, o nível, a porcentagem do transbordamento, o risco em cor e texto, os metros restantes e o tempo estimado, com gráficos e histórico de eventos ao abrir o rio.

**Cota de transbordamento e calibração por ponto.** É o dado que transforma a distância medida pelo sensor em porcentagem, e é o que torna o aviso válido em cada rio. O modelo já existe no cadastro de cada estação da API (**verificado** no código) e funciona em três passos:

1. O sensor mede a **distância** até a superfície da água.
2. **Nível** = altura de instalação − distância (altura da água acima do fundo do rio).
3. **Porcentagem** = nível ÷ nível de transbordamento. Acima de 100%, o rio já transbordou.

| Parâmetro | O que é | Como obter | Onde fica |
|---|---|---|---|
| Altura de instalação | Distância entre o sensor e o fundo do rio, em cm | Na instalação, com o rio baixo: medir com régua graduada a profundidade da água no ponto (h0) e ler a distância do sensor no mesmo instante (d0). Altura = d0 + h0. Onde não for seguro entrar na água, usar levantamento topográfico da seção | Cadastro da estação |
| Nível de transbordamento | Altura da água, a partir do fundo, em que o rio sai da calha e passa a atingir ruas ou imóveis no trecho da estação | Em ordem de preferência: (1) marcas de cheia e relatos da Defesa Civil sobre o nível em que a rua alagou; (2) cota oficial, quando existir, convertida para o zero local; (3) medição da margem: nível de transbordamento = altura de instalação − distância vertical do sensor ao ponto mais baixo da margem | Cadastro da estação |
| Limites de atenção e crítico | Porcentagens que mudam o estado (estável, atenção, crítico). O padrão atual é 50% e 80% | Definir com a Defesa Civil a partir de eventos passados | Cadastro, por estação |

Regras de implementação:

- **A estação envia só a distância; a API calcula.** O firmware do protótipo calcula a porcentagem sozinho (30 cm = 0%, 20 cm = 100%, com limites de 33% e 66%), e a API usa outro modelo (zero no fundo do rio, 50% e 80%). Concentrar o cálculo na API elimina a divergência e permite recalibrar sem regravar o dispositivo.
- **Guardar a distância bruta e o histórico de calibrações.** A distância bruta de cada leitura já é guardada. O cadastro, porém, mantém só os valores atuais: se a cota for corrigida, as leituras antigas ficam sem a referência da época. A mudança mínima é uma tabela de calibrações por estação, com data, método e responsável.
- **Validar cada leitura.** Distância menor que a zona cega do sensor ou maior que a altura de instalação é leitura inválida e não vira porcentagem.
- **Posicionar o sensor acima do nível máximo esperado.** A distância no nível de transbordamento (altura de instalação − nível de transbordamento) deve superar a zona cega do sensor (25 cm no SR04M-2, segundo o fornecedor), com folga, e o sensor deve ficar fora d'água em cheias acima da cota, conforme as marcas históricas.
- **Falta de dado nunca é "estável".** Estação sem leitura recente aparece como "sem dados", porque em uma cheia forte a própria estação pode ser atingida.
- **A porcentagem vale para o trecho da estação.** A cota é local: duas estações do mesmo rio não são comparáveis, e o ponto de transbordamento real pode estar em outro trecho (estreitamento, ponte).
- **Reconferir a calibração periodicamente** (periodicidade a definir) e após cheias grandes, porque o fundo do rio muda com assoreamento e obras.

**Mapa de nível (nível × áreas atingidas).** Cada estação precisa saber **quais ruas** são atingidas quando o rio chega a cada faixa de nível. Isso alimenta a camada de áreas de risco do mapa, a rota que evita essas áreas e o aviso de ponto de apoio em área atingida. Implementação em cinco passos:

1. **Faixas por estação.** Usar as que já existem: atenção, crítico e transbordamento (100%), e uma faixa acima de 100% se houver dados.
2. **Áreas por faixa.** Desenhar as áreas das ruas que a Defesa Civil e os moradores sabem que alagam quando o rio chega àquele nível. Fontes: histórico e marcas de cheia, manchas de inundação do Serviço Geológico do Brasil e topografia.
3. **Banco de dados.** Tabela de áreas de risco com estação, faixa e geometria (PostGIS). Como o Prisma não trata geometria, a tabela e as consultas usam SQL direto, como o projeto já faz com as consultas por distância.
4. **Tempo real.** A faixa ativa é a maior atingida pela porcentagem atual da estação. O aplicativo destaca as áreas dessa faixa, o motor de rotas as exclui do cálculo e os pontos de apoio dentro delas recebem aviso.
5. **Piloto.** Uma bacia, três faixas, validadas com a Defesa Civil (hipótese RC9).

Este mapa substitui a associação "estação mais próxima do rio", que fica como solução provisória. Ele cobre o alagamento causado pelo **rio**; alagamento por chuva na própria rua não é visto por sensor de rio.

**Base geográfica.** Mapa dos rios e das estações, ruas importadas do OpenStreetMap para o PostGIS e associadas provisoriamente à estação mais próxima do rio, mais o cadastro de pontos de apoio, que já tem nome, endereço, capacidade, contato e coordenadas, mas ainda não registra a data e a fonte da última atualização (**verificado** no código; a pesquisa por rua responde "não implementado" na v0.1.0 e os dados de apoio atuais são fictícios). A associação por proximidade pode errar em encostas e cruzamentos e deve ser validada. Os dados do OpenStreetMap exigem atribuição conforme a licença ODbL.

**Mapa interativo, pontos de apoio e rotas.** O aplicativo tem um mapa exclusivo da cidade. Com contrato da Defesa Civil, o mapa mostra os **pontos de apoio** do órgão: ao tocar em um ponto, o usuário vê o telefone e a capacidade máxima de pessoas e pode traçar a rota até ele. O AquaScan integra ao banco o relatório de pontos de apoio fornecido pelo órgão (a API já tem o cadastro, hoje com dados fictícios). A capacidade informada é a **máxima**, não a vaga disponível, e a lista só vale se o órgão a mantiver atualizada.

Para a **rota que evita áreas de risco**, há três pontos de atenção:

- **O sensor mede um ponto do rio, não a rua.** Dizer que uma rua está sujeita a alagamento quando o rio passa de certo nível exige um mapeamento entre nível e áreas atingidas (por exemplo, manchas de inundação do Serviço Geológico do Brasil ou o histórico da Defesa Civil). Esse mapeamento não existe hoje no projeto e está descrito no "mapa de nível", na seção 3.2. Alagamentos causados só pela chuva na rua, sem transbordamento do rio, não são vistos por sensores de rio.
- **O Google não oferece evitar uma área personalizada.** A Routes API permite evitar pedágios, rodovias, balsas e áreas internas, mas não um polígono definido pelo usuário (documentação do Google, consultada em 14/10/2026). Evitar ruas específicas exige um motor de rotas próprio sobre os dados do OpenStreetMap já presentes no banco, com as ruas de risco removidas do cálculo. Motores de código aberto como Valhalla e GraphHopper oferecem exclusão de áreas (**confiança média**, a confirmar na documentação). Os termos da Google Maps Platform limitam o uso combinado de seu conteúdo com outros dados e mapas; conferir antes de implementar.
- **A rota deve ser apresentada como indicativa**, com aviso de que não substitui a orientação da Defesa Civil. Chamá-la de "segura" não é sustentável com dados de pontos isolados.

**Histórico próprio de leituras e eventos.** Cresce com a operação. Serve para calibrar limiares e demonstrar desempenho. Uma série curta não sustenta modelos estatísticos mais complexos (relatório do sensor).

**Marca AquaScan.** Não consta registro no INPI (**hipótese** de registro). A grafia "AquaScan" e "AQUASCAN" aparece nos materiais e deve ser padronizada antes de qualquer registro.

### 3.3 Humanos

| Competência | Para quê |
|---|---|
| Engenharia de software e firmware | Manter ESP32, API e aplicativo |
| Eletrônica e montagem | Projetar a placa de campo e fabricar as estações |
| Hidrologia e calibração | Definir cota de transbordamento, limiares e leitura crítica dos dados |
| Técnico de campo | Instalar, vistoriar e fazer manutenção, com habilitação para trabalho em altura quando a fixação exigir (NR-35, enquadramento a confirmar) |
| Relacionamento institucional e contratação | Reunir-se com a Defesa Civil e a Prefeitura, preparar propostas e acompanhar contratos |

Os integrantes são moradores de Petrópolis e viveram as enchentes (**vivência**), o que dá conhecimento direto do problema e acesso ao território. O produto usa regras de cálculo determinísticas, sem inteligência artificial, portanto **não exige cientista de dados** nesta fase.

### 3.4 Financeiros

- **Capital para o primeiro lote e para o piloto.** Compra de componentes de campo, estações de teste, deslocamento e ferramentas. O valor depende do custo por estação de campo, ainda sem cotações (bloco Estrutura de Custos). O plano financeiro inicial do projeto foi feito para um modelo de produto anterior e não é usado como referência aqui.
- **Capital de giro.** Cobre os custos entre a instalação e o recebimento do contratante. O prazo de pagamento do poder público **não foi levantado** (**hipótese** de que seja necessário reservar caixa).
- **Reserva de reposição.** Fundo para peças, baterias e substituição de estações danificadas por cheia, descarga elétrica, furto ou vandalismo.
- **Custos recorrentes de plataforma.** Hospedagem da API e do banco, conta de desenvolvedor nas lojas (Apple Developer Program: US$ 99 por ano; Google Play: US$ 25, pagamento único, conforme o [Canaltech](https://canaltech.com.br/apps/como-publicar-um-app-na-play-store-e-app-store-entenda-o-processo-das-lojas/)), plano de dados das estações e provedor de mapas e de rotas. Valores em Estrutura de Custos.

### 3.5 Acessos e autorizações

| Recurso | Fornecedor provável | Por que é crítico |
|---|---|---|
| Autorização para fixar a estação em ponte, muro ou margem | Prefeitura, órgão ambiental ou proprietário do local | Sem ela a estação não pode ser instalada. A instalação conjunta, com pontos indicados pelo cliente, reduz o risco (**hipótese**) |
| Cota de transbordamento e referências de campo | Defesa Civil, órgãos estaduais ou levantamento próprio | Sem ela não há porcentagem |
| Dados meteorológicos e hidrológicos | Open-Meteo (já usado na previsão), ANA e INEA (acesso e termos a confirmar) | Contexto de chuva e séries históricas para calibração |
| Energia e rede no ponto | Cliente, proprietário do local ou operadora móvel | A estação precisa de alimentação contínua e de canal de envio |
| Lista de pontos de apoio (nome, localização, telefone e capacidade máxima) | Defesa Civil | Alimenta o mapa; precisa de atualização periódica pelo órgão |
| Mapeamento entre nível do rio e áreas atingidas | Serviço Geológico do Brasil, Defesa Civil ou levantamento próprio | Permite dizer quais ruas ficam sob risco; sem ele não há rota que evite áreas de risco |

---

## 4. Peças do protótipo e equivalentes em um rio real

O protótipo prova a **ideia** em uma maquete: um sensor mede a distância até a água, o controlador converte em nível e sinaliza o estado. A estrutura de uma estação real é a mesma (sensor, controlador, comunicação, banco de dados e alerta). O que muda são as **peças**: as do protótipo foram escolhidas por custo e facilidade de bancada e não resistem a um rio. Base: relatório técnico do sensor (seções 8 a 10), documentação do firmware e fontes públicas.

### 4.1 Peça por peça

| Peça do protótipo | Função | Por que não serve no rio | No mundo real |
|---|---|---|---|
| Maquete | Ambiente controlado | A água é calma e limpa; o rio varia em metros e carrega lixo e galhos | Rio natural, com ponto de medição e cota de referência |
| ESP32 DevKit e protoboard | Processamento e ligações | Placa de bancada: contatos soltos, sem proteção contra umidade e raios | Controlador de campo, ou o mesmo chip em placa soldada e protegida (**hipótese**) |
| Sensor ultrassônico JSN-SR04M-2 | Mede a distância até a água | Faixa curta, só a sonda é à prova d'água e a medida se distorce com calor, espuma e chuva (seção 4.2) | Radar, ultrassom de campo ou sensor de pressão |
| Sensor de vazão YF-S201 | Mede o fluxo dentro de um cano | Não mede a correnteza de um rio aberto (seção 4.3) | Equipamento hidrométrico ou curva calibrada por ponto |
| Display OLED e LEDs | Mostram o estado | Ninguém lê um display sob uma ponte | Aplicativo, painel e alertas remotos |
| Alimentação USB | Energia | Exige tomada | Painel solar, controlador de carga e bateria (seção 4.4) |
| Monitor serial | Saída dos dados | Nenhum dado sai do aparelho | Rede celular, rádio ou satélite (seção 4.4) |
| Tendência linear do nível | Estima o tempo até transbordar | Não é um modelo hidrológico, e o índice de risco de 0 a 100 é uma métrica do projeto, não uma classificação oficial | Mantida como **estimativa**; chuva e estações a montante entram como evolução |

### 4.2 Sensor de nível: a peça mais crítica

Três problemas do módulo atual:

- **Zona cega.** O sensor não mede o que está muito perto dele. O fornecedor do SR04M-2 informa 25 cm; o firmware usa 20 a 30 cm como faixa da maquete, ou seja, na borda ou dentro dessa zona. O datasheet do JSN-SR04T informa 20 cm. As variantes diferem, e é preciso conferir o datasheet do módulo comprado.
- **Resolução da maquete.** Com faixa de 10 cm, cada 1 cm vale 10% de nível. Em um rio, a faixa é de metros e o mesmo erro pesa bem menos, o que só um ensaio em ponto real confirma.
- **Ambiente.** O calor muda a velocidade do som e distorce a medida (1,9% a 30 °C, segundo o repositório). Espuma, chuva forte e detritos geram leituras falsas, e o módulo não declara grau de proteção IP.

Opções para campo:

| Opção | Vantagem | Limitação | Referência |
|---|---|---|---|
| Ultrassônico de campo, com compensação de temperatura | Barato; instalado de uma ponte, sem entrar na água | Ainda sujeito a espuma, chuva e feixe largo | Preço a cotar |
| Radar de nível | Muito preciso e pouco afetado pelo calor. O VEGAPULS WL 61 informa até 15 m, ±2 mm e IP68 | Mais caro (preço **não levantado**); saída industrial | Folha do fabricante |
| Sensor de pressão submerso | Não depende de feixe nem de chuva; usado pelo E-Noé, cujo sistema completo custa cerca de R$ 15 mil | Fica na água e sofre com sedimento e cheia; exige cuidado de calibração (**confiança média**) | Revista Pesquisa FAPESP |

O custo do protótipo não é referência da estação de campo: as peças de campo são mais caras e precisam ser cotadas em Estrutura de Custos.

### 4.3 Vazão

O YF-S201 mede a água que passa dentro de um cano e não serve para rio aberto. Em um rio, as alternativas são:

- **Curva-chave (nível × vazão):** estima a vazão pelo nível, mas só vale depois de medições locais, e cada ponto tem a sua.
- **Radar de velocidade superficial:** em testes do USGS (rios dos Estados Unidos), ficou em torno de 5% de diferença da vazão de referência depois do ajuste. A velocidade média foi cerca de 0,85 da velocidade da superfície, valor que precisa ser confirmado em cada local.
- **ADCP (perfilador acústico):** indicado pelo relatório para rio aberto, de custo bem maior.

**Decisão:** o alerta do AquaScan se baseia no **nível** em relação à cota de transbordamento. A vazão em rio aberto fica fora da oferta inicial.

### 4.4 Energia e comunicação

- **Energia:** painel solar, controlador de carga e bateria. A cheia ocorre com céu fechado, então a bateria deve durar vários dias sem sol. Medir em intervalos, com leitura mais frequente quando o rio sobe, economiza energia (**hipótese**).
- **Comunicação:** a estação envia poucos dados por vez, o que combina com redes celulares de internet das coisas (NB-IoT, 4G). A TIM anunciou NB-IoT em mais de 3 mil municípios (matéria de 2021). A cobertura em Petrópolis, em vales e encostas, **não foi verificada** (hipótese RC3).

---

## 5. Dependências e riscos

| Recurso | Origem | Risco de indisponibilidade | Mitigação |
|---|---|---|---|
| ESP32 e sensor de nível | Compra de varejo ou importação | Médio: prazo, preço e câmbio | Estoque de reposição; sensor alternativo qualificado |
| Estação em ambiente de rio | Fabricação própria | Alto: umidade, detritos, vandalismo, descarga elétrica | Caixa IP65 ou superior, placa soldada com proteção contra surtos, fixação protegida, diagnóstico de falha do sensor e visitas periódicas |
| Autorização de instalação | Prefeitura, órgão ambiental | Alto: burocracia ou negativa | Pontos indicados pelo cliente; termo de cooperação prévio |
| Cota de transbordamento | Defesa Civil ou levantamento | Alto: sem ela o produto não entrega porcentagem | Levantar no piloto junto com o cliente |
| Energia e conectividade no ponto | Cliente, operadora | Médio a alto, variando por ponto | Painel solar com bateria dimensionada para dias nublados; módulo celular onde não houver Wi-Fi |
| Hospedagem da API e do banco | Provedor de nuvem (ainda não escolhido) | Baixo | Backups automáticos e HTTPS |
| Dados externos (Open-Meteo, OpenStreetMap, ANA/INEA) | Terceiros | Médio: mudança de termos ou indisponibilidade | Cache (a API já usa cache de 30 minutos na previsão); o aplicativo continua exibindo o nível medido sem a previsão |
| Competências de hidrologia e campo | Parceria ou contratação | Médio: sem responsável hoje | Apoio de universidade e da Defesa Civil; manuais de instalação e calibração |
| Aprovação nas lojas de aplicativos | Apple e Google | Baixo a médio | Submissão antecipada; notificações push exigem versão de produção |
| Provedor de mapas (Google Maps Platform) | Terceiro, cobrança por uso | Médio: custo variável e mudança de termos | Limites de uso, cache e alternativa com mapa de código aberto |
| Lista de pontos de apoio | Defesa Civil | Médio a alto: dado desatualizado leva o usuário a um local fechado ou lotado | Data da última atualização visível no aplicativo; rotina de atualização combinada em contrato |
| Mapeamento entre nível e áreas atingidas | Serviço Geológico do Brasil, Defesa Civil | Alto: sem ele a rota não pode evitar áreas de risco | Lançar a rota em fase posterior; no início, mostrar o estado dos rios próximos ao trajeto |

---

## 6. Hipóteses a validar

| # | Hipótese | Como testar | Critério |
|---|---|---|---|
| RC1 | O sensor de nível de campo, com compensação de temperatura, mantém a precisão sob chuva e umidade, fora da zona cega | Ensaio em bancada e em ponto real, contra régua de referência, por 30 dias em Petrópolis | Erro absoluto de até ±2 cm e sem perda de sinal. O critério anterior, de variação inferior a 3%, não tinha base de cálculo definida |
| RC2 | O custo da estação de campo instalada, com mão de obra, permite que o pacote de entrada caiba na dispensa de licitação | Cotações de peças de campo em duas lojas com data e planilha de custos | Pacote inteiro (estações, instalação e primeiro ano) abaixo do limite, conforme o bloco Fonte de Renda e Lucro |
| RC3 | Há energia e canal de envio nos pontos que o cliente indicar | Visita aos pontos candidatos com teste de sinal celular e Wi-Fi | Solução de energia e conectividade definida para todos os pontos do piloto |
| RC4 | A cota de transbordamento de cada ponto pode ser obtida com a Defesa Civil ou levantada em campo | Reunião com a Defesa Civil sobre marcas de cheia e medição no piloto, pelo procedimento da seção 3.2 | Altura de instalação e nível de transbordamento definidos e registrados para todos os pontos do piloto, com a leitura conferida contra régua |
| RC5 | A base do OpenStreetMap, no PostGIS, cobre as ruas de risco e a associação rua-estação está correta | Amostra de 20 ruas históricas do Centro e dos distritos, conferida com moradores e Defesa Civil | Mais de 95% das vias presentes e associação correta nos casos conferidos |
| RC6 | A prefeitura ou o órgão competente autoriza a fixação das estações em prazo viável | Consulta formal sobre ponte e margem | Resposta formal sobre procedimento e prazo |
| RC7 | A equipe consegue cobrir hidrologia e trabalho de campo por parceria | Contato com universidade e Defesa Civil | Ao menos um apoio técnico identificado |
| RC8 | Pelo menos um dos tipos de sensor de nível de campo da seção 4.2 (ultrassônico de campo, radar ou sensor de pressão) atende à precisão exigida e ao custo do pacote | Cotar os tipos e instalar os que couberem no orçamento no mesmo ponto do piloto, lado a lado, comparando cada um com uma régua de referência por 30 dias | Pelo menos um tipo com erro absoluto de até ±2 cm, sem perda de leitura em chuva forte, e com custo (sensor e instalação) dentro do pacote definido em RC2 |
| RC9 | É possível associar o nível de cada rio monitorado às ruas sujeitas a alagamento | Obter as manchas de inundação do Serviço Geológico do Brasil e o histórico da Defesa Civil; cruzar com a cota de cada ponto | Mapa por faixa de nível para ao menos uma bacia do piloto, conferido com eventos passados |
| RC10 | A Defesa Civil entrega e mantém a lista de pontos de apoio em formato aproveitável | Solicitar o relatório atual e combinar a frequência de atualização | Lista com nome, localização, telefone e capacidade máxima, e responsável pela atualização definido |

---

## Referências

- [Repositório do firmware: Monitoramento de Fluxo de Água ESP32](https://github.com/CaiqueRV/Monitoramento-Fluxo-de-Agua-ESP32) (lista de materiais, análise de cálculos, registro de validação e README)
- [Repositório do aplicativo e da API: aquascan-app](https://github.com/Mateus-Fonseca847/aquascan-app)
- Relatório técnico do sensor de monitoramento hidrológico (arquivo do projeto), seções 8 a 10
- [Datasheet do JSN-SR04T 2.0](https://www.mikrocontroller.net/attachment/541933/JSN-SR04T-2.0.pdf)
- [Makers Electronics: SR04M-2, especificações do fornecedor](https://makerselectronics.com/product/sr04m-2-waterproof-ultrasonic-distan/)
- [VEGAPULS WL 61: folha de dados do fabricante](https://agriculture.yodify.com/Documentation/Document/YBKYq/38064-EN-VEGAPULS-WL-61-420mA-HART-two-wire.pdf)
- [Revista Pesquisa FAPESP: E-Noé, 2023](https://revistapesquisa.fapesp.br/dispositivo-emite-em-tempo-real-alertas-contra-enchentes/)
- [Google Routes API: recursos de rota que podem ser evitados](https://developers.google.cn/maps/documentation/routes/route-modifiers?hl=pt-br)
- [USGS: uso de radares para medir a vazão de rios sem contato](https://pubs.usgs.gov/publication/70028331)
- [Tecnoblog: TIM e a rede NB-IoT](https://tecnoblog.net/noticias/tim-expande-rede-nb-iot-internet-das-coisas/)
- [Canaltech: custos para publicar aplicativos nas lojas](https://canaltech.com.br/apps/como-publicar-um-app-na-play-store-e-app-store-entenda-o-processo-das-lojas/)
- [OpenStreetMap: licença e atribuição](https://www.openstreetmap.org/copyright)
