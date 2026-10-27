# Business Model Canvas · Estrutura de Custos

## Introdução

O AquaScan é um sistema de monitoramento de rios que mede o nível da água com sensores de baixo custo, instalados em conjunto com o cliente, e comunica o risco de transbordamento em porcentagem, cor e texto, com tempo estimado, por meio de um aplicativo gratuito para a população. Este documento descreve o bloco **Estrutura de Custos** do Business Model Canvas: quais são os custos mais importantes para manter o negócio funcionando, quanto custa uma estação instalada em campo, quanto custa manter a plataforma e se o modelo fecha dentro e acima do limite de contratação direta do poder público.

Ao longo do texto são apresentados o custo estimado de uma estação de campo, os custos de instalação e operação, de plataforma, de pessoas, de marketing, de administração e de conformidade, dois cenários de contratação (dentro e acima do limite de dispensa de licitação), com seus limites e margens, e as hipóteses que ainda precisam ser validadas. Os recursos que geram esses custos estão no bloco Recursos-Chave; os preços e a lógica de receita, no bloco Fonte de Renda e Lucro; os fornecedores, em Parcerias-Chave.

**Escopo:** este bloco trata somente do custo do **sistema em funcionamento**, isto é, de estações instaladas em rios reais e da plataforma que as sustenta. O custo da maquete usada no Supernova não entra aqui. Os valores da estação de campo e da operação são um **cenário de trabalho**, montado com preços verificados onde existem e com premissas explícitas onde não existem; onde não foi possível obter cotação, o valor está marcado como **premissa** e a lista dos itens pendentes está na seção 3.1 (hipótese C1).

**Legenda das evidências:** **Verificado** (fonte pública em Referências, consultada em 16/10/2026) · **Vivência** (observação dos integrantes, moradores de Petrópolis, RJ) · **Pesquisa** (levantamento dos integrantes, fontes a anexar) · **Premissa** (valor de trabalho assumido sem cotação, a substituir) · **Hipótese** (a validar, ver seção 9).

**Câmbio usado nas conversões:** US$ 1 = R$ 4,9851 e € 1 = R$ 5,5840 (fechamento de 09/10/2026, [O Povo](https://www.opovo.com.br/noticias/economia/2026/10/09/fechamento-do-mercado-financeiro.html)). Valores em dólar variam com o câmbio.

---

## 1. Visão geral

| Categoria | O que inclui | Natureza | Situação do valor |
|---|---|---|---|
| Estação de campo | Sensor de nível, controlador, módulo celular, energia, caixa e fixação | Único, por estação | Parcialmente **verificado**; o resto é **premissa** |
| Instalação e calibração | Deslocamento, mão de obra, levantamento da cota de transbordamento | Único, por estação | **Premissa** |
| Operação das estações | Dados móveis, vistorias, reposição de peças | Recorrente, por estação | Dados móveis **verificado**; o resto é **premissa** |
| Plataforma | Hospedagem, banco, clima, mapas e rotas, lojas de aplicativos | Recorrente, quase fixo | Parcialmente **verificado** |
| Pessoas | 6 sócios e até 2 técnicos (instalação e manutenção) | Recorrente | Três estruturas na seção 3.4 |
| Marketing e exposição da marca | Tráfego pago, orgânico, mídia física e online, eventos, registro da marca | Misto, quase todo fixo | **Premissa**, exceto o registro da marca (**verificado**) |
| Administração, seguros, jurídico e conformidade | Contabilidade, seguros, jurídico e LGPD, segurança da informação, ferramentas e EPI, homologação | Misto | Contabilidade **verificada**; o resto é **premissa** |

---

## 2. Perguntas-chave

| Pergunta | Resposta |
|---|---|
| Quais são os custos mais importantes? | No cenário de trabalho, três itens somam 60% do custo instalado de uma estação: o **sensor de nível de campo (com importação)**, o **módulo celular** e a **instalação**. O controlador ESP32, a peça mais citada nos materiais, pesa cerca de 2% (seção 3.1). No negócio como um todo, os custos fixos pesam mais que os variáveis: **estrutura administrativa, marketing próprio (R$ 8,5 mil no primeiro ano, já sem tráfego pago e exposição da marca, a cargo dos órgãos) e equipe** (seção 7) |
| Quais recursos-chave são mais caros? | Sensor de nível de campo, comunicação celular, a equipe de campo e o marketing. O ESP32 é irrelevante no custo de campo |
| Quais atividades-chave são mais caras? | Instalação conjunta, calibração e manutenção em campo, porque envolvem deslocamento e mão de obra por estação. O bloco Atividades-Chave será conferido quando for fechado |
| O modelo é viável com os recursos, ações e alianças de hoje? | **Ainda não é possível afirmar.** No cenário de trabalho, um pacote de 8 estações dentro do limite de dispensa de licitação deixa margem de cerca de 43% sobre o custo variável, mas o contrato não cobre os custos fixos de um ano (cerca de R$ 33 mil sem pessoas); acima do limite (30 estações, por licitação), a margem vai de cerca de 11% a 62%, conforme o preço obtido na disputa. O resultado depende de números ainda sem cotação: a importação do sensor de campo, o painel solar, a perda anual de estações e, sobretudo, o marketing e a estrutura de equipe (seções 3.4, 3.5 e 7) |

---

## 3. Custos por categoria

### 3.1 Estação de campo (cenário de trabalho)

O cenário usa um sensor ultrassônico de campo da classe do MaxBotix MB7389 (IP67). **Não é decisão de sensor**: a escolha entre ultrassônico de campo, radar e sensor de pressão é a hipótese RC8 do bloco Recursos-Chave e muda este custo.

| Item | Cotação ou referência | Valor no cenário (R$) | Base |
|---|---|---|---|
| Sensor de nível de campo (classe MB7389, IP67) | US$ 109,95 no site do fabricante, ao câmbio de 09/10/2026 | 548 | **Verificado** |
| Importação, frete e impostos do sensor | Sem cotação | 274 | **Premissa** (50% do preço de tabela) |
| Controlador ESP32 | R$ 56,81 (Usinainfo) a R$ 62,00 (Curto Circuito) | 62 | **Verificado**, usa o maior valor |
| Módulo celular SIM7080G (Cat-M e NB-IoT, com antena) | R$ 440,00 (Curto Circuito, em estoque) | 440 | **Verificado**; é módulo de prototipagem, a versão industrial pode custar diferente |
| Painel solar de cerca de 10 W | Modelos de 10 W listados na NeoSolar (Resun, Sinosola, Ztroon), sem preço obtido | 130 | **Premissa** |
| Bateria selada de chumbo, 12 V, 9 Ah (Moura VRLA) | Kit com 5 unidades a R$ 745,02 no Pix (Minha Casa Solar); R$ 149,00 por unidade, por divisão | 149 | **Verificado** (item indisponível na data) |
| Controlador de carga solar PWM 10 A (Sun21 CCS-P1024) | R$ 117,20 no boleto (Minha Casa Solar); a página também exibe R$ 109,00 | 117 | **Verificado** |
| Caixa de passagem de sobrepor, 150 x 150 x 100 mm, com tampa parafusada | R$ 43,91 (SINAPI, 07/2026, média nacional); o grau de proteção IP65 não consta e deve ser confirmado | 44 | **Verificado** |
| Prensa-cabos PG7 IP67 (3 unidades: sensor, painel e antena) | R$ 2,43 cada no Pix (Usinainfo) | 7 | **Verificado** |
| Suporte de fixação, placa de circuito, antena, cabos e conectores | Sem cotação | 350 | **Premissa** |
| **Subtotal de peças** | | **2.122** | |
| Contingência de 20% (perdas, retrabalho, peças de reposição iniciais) | | 424 | **Premissa** |
| Instalação e calibração: mão de obra (1 eletrotécnico a R$ 40,70 por hora e 1 ajudante a R$ 25,07 por hora, 8 horas) | SINAPI, 07/2026, média nacional (não há valor específico do RJ) | 526 | **Verificado** |
| Deslocamento e EPI da equipe | Sem cotação | 100 | **Premissa** |
| **Total instalado por estação** | | **3.172** | |

**Peso de cada item no total instalado:** sensor com importação 26%, instalação 20%, módulo celular 14%, contingência 13%, energia (painel, bateria e controlador) 12%, caixa, prensa-cabos, suporte e placa 13%, ESP32 2%.

**O que ainda é premissa:** importação do sensor, painel solar, suporte e placa, contingência, deslocamento e EPI. Os demais itens têm preço de loja ou de tabela oficial. O painel de 10 W é a cotação mais fácil de obter e deve ser a primeira a ser substituída (hipótese C1).

**Referências de sensor de nível de outras classes (apenas o sensor, não a estação):**

| Classe | Referência | Preço |
|---|---|---|
| Ultrassônico de campo, IP67 | MaxBotix MB7389 | US$ 109,95 (**verificado**) |
| Radar profissional | Vega PS6X, substituto do PS61 (até 35 m, IP66/IP67, saída 4 a 20 mA com HART), na RS | £ 2.447,00 sem IVA (**verificado**); cerca de R$ 15 mil a R$ 20 mil em conversão aproximada, sem importação (confiança baixa) |
| Radar compacto de 80 GHz | Linha de baixo custo citada em publicações do setor | Sem cotação obtida |

**Comunicação.**
- **Módulos:** o SIM7080G aceita Cat-M e NB-IoT e exige chip IoT específico, não funciona com chip comum (**verificado** na página da loja). O A7670SA (R$ 375,00, esgotado em 16/10/2026) é LTE Cat 1 com fallback 2G.
- **Chip de dados:** o plano M2M da Vivo custa R$ 6,90 por mês (20 MB), R$ 9,90 (50 MB) ou R$ 11,90 (100 MB) por linha (**verificado**). A página não informa preço nem inclusão de NB-IoT; confirmar com a operadora. Chips IoT passaram a pagar apenas ISS, sem ICMS, desde a reclassificação da Anatel (2021, [Tecnoblog](https://tecnoblog.net/379991/anatel-reduz-impostos-de-chips-para-internet-das-coisas/)).
- **Consumo:** uma leitura por minuto, enviada por HTTPS com nova conexão a cada envio, pode consumir dezenas a centenas de MB por mês, porque o estabelecimento da conexão segura é muito maior que a leitura (ordem de grandeza, **confiança média**). Enviar em lote, aumentar o intervalo em nível baixo ou manter a conexão aberta reduz o plano necessário (hipótese C3).
- **Cobertura:** Petrópolis é região serrana, com vales e encostas. A cobertura de NB-IoT e LTE-M nos pontos de instalação **não foi verificada** (hipótese C4).

### 3.2 Instalação e operação em campo

| Item | Frequência | Valor no cenário (R$) | Base |
|---|---|---|---|
| Plano de dados | Por mês | 11,90 (R$ 143 por ano) | **Verificado** (Vivo M2M, 100 MB) |
| Vistorias preventivas e corretivas | 2 visitas por ano; cada uma com 1 eletrotécnico e 1 ajudante por 4 horas (R$ 263, SINAPI) mais R$ 40 de deslocamento | 606 por ano | Mão de obra **verificada**; deslocamento **premissa** |
| Reserva de reposição (cheia, descarga elétrica, furto, vandalismo) | 10% das peças e da contingência, por ano | 255 por ano | **Premissa** |
| **Operação por estação, por ano** | | **1.004** | |

**Técnico por demanda.** No início, o campo é feito por prestador contratado a cada serviço (instalação e duas vistorias por ano), sem vínculo fixo. Os valores acima usam o custo horário do SINAPI, que é **piso**: o preço de mercado de um prestador tende a ser maior por causa de encargos, ferramentas, deslocamento até o ponto e valor mínimo por chamado. Se o prestador for autônomo, o contratante pessoa jurídica ainda recolhe contribuição patronal de 20% sobre o pagamento (a confirmar com o contador); prestador com CNPJ evita essa incidência. Três pontos de atenção:
- **Disponibilidade na cheia.** Manutenção corretiva em dia de chuva forte é justamente quando o prestador é mais difícil de achar. Convém ter dois prestadores cadastrados e um sócio treinado para o atendimento de emergência.
- **Capacitação mínima.** O prestador deve receber procedimento escrito de instalação e calibração, para o resultado não depender de quem vai ao ponto.
- **Escala.** Com 8 estações são cerca de 16 visitas por ano, e a demanda por prestador é baixa e irregular; o valor mínimo por chamado pesa mais no cenário A do que no B (sensibilidade na seção 4).

O **primeiro ano** de uma estação custa, portanto, cerca de **R$ 4.176** (R$ 3.172 instalada mais R$ 1.004 de operação), sem rateio da plataforma. Dos anos seguintes em diante, o custo da estação cai para cerca de R$ 1.004 por ano, e é isso que a assinatura precisa cobrir.

Uma estação em ponte, muro ou margem de rio é, por definição, exposta à própria cheia que mede. A taxa real de perda é desconhecida e o valor de 10% é só um ponto de partida (hipótese C7).

### 3.3 Plataforma (software e dados)

| Item | Valor | Situação | Observação |
|---|---|---|---|
| Hospedagem da API e do banco (PostgreSQL com PostGIS) | R$ 150 por mês | **Premissa** | Servidores virtuais pequenos custam poucos euros por mês (o plano CX22 da Hetzner, hoje descontinuado, listava € 3,79; [vpsbenchmarks](https://vpsbenchmarks.com/hosters/hetzner/plans/cx22)). Para produção com backup e monitoramento, o valor deve ser dimensionado |
| Previsão de chuva (Open-Meteo) | US$ 29 por mês (R$ 145) | **Verificado** em publicação do fornecedor de 2023; confirmar valor atual | **O uso gratuito é só para fins não comerciais** (página de preços, 16/10/2026). O AquaScan, vendido a órgãos públicos, é uso comercial. O plano comercial Standard inclui 1 milhão de chamadas por mês. É um custo que não estava previsto e precisa de confirmação com o fornecedor ou de troca de fonte (hipótese C5) |
| Contas de desenvolvedor | Apple: US$ 99 por ano (R$ 494); Google Play: US$ 25, pagamento único (R$ 125) | **Verificado** ([Canaltech](https://canaltech.com.br/apps/como-publicar-um-app-na-play-store-e-app-store-entenda-o-processo-das-lojas/)) | Diluídos em 12 meses: cerca de R$ 52 por mês |
| Geração do aplicativo (EAS Build, da Expo) | Plano gratuito, com builds de baixa prioridade; Starter a US$ 19 por mês | **Verificado** ([Expo](https://docs.expo.dev/billing/plans/)) | Necessário só se o prazo de build exigir prioridade |
| Notificações push | Não verificado | A confirmar | Verificar limites e custos do serviço usado |
| Dados do OpenStreetMap | Gratuitos | **Verificado** (licença ODbL) | Exigem atribuição |
| Domínio, e-mail institucional, monitoramento | Não levantado | A levantar | |
| Mapa e rotas no aplicativo | Sem cobrança por uso identificada | **Verificado** no código | Ver abaixo |

**Mapa e rotas: como o aplicativo funciona hoje e o que isso custa.** Verificado no repositório aquascan-app em 16/10/2026:
- **Mapa:** exibido com `react-native-maps` (tela `apps/mobile/app/(tabs)/mapa.tsx`). No Expo Go funciona sem configuração; em build próprio ou na versão final para Android exige uma chave do Google Maps, configurada em `app.json` (`docs/solucao-de-problemas.md`). Em iOS a biblioteca usa por padrão o mapa da Apple (**confiança média**, conhecimento da biblioteca; confirmar na configuração do projeto).
- **Rotas:** calculadas **a pé, no próprio celular e sem internet**, por um algoritmo A* escrito no projeto (`packages/roteamento`) sobre um grafo de ruas do OpenStreetMap, com desvio de rios em estado crítico (`packages/desvio`). A decisão é de 16/10/2026 (`docs/decisoes.md`) e descartou serviços externos de rotas porque exigem internet, enviam a localização a terceiros e têm limites de uso e custo.
- **Grafo:** arquivo de 1,9 MB (344 KB compactado), gerado com `tools/grafo` a partir do OpenStreetMap e distribuído com o aplicativo.

| Elemento | Custo | Situação |
|---|---|---|
| Cálculo de rotas | Nenhum por rota; roda no aparelho | **Verificado** no desenho do código |
| SDK de mapa nativo no Android (chave do Google) | A tabela global de preços da Google lista o SDK de mapa como sem custo; a chave exige conta de faturamento | **Verificado** na tabela; confirmar os termos (hipótese C6) |
| Mapa no iOS | Nenhum custo identificado | A confirmar (hipótese C6) |
| Dados de ruas e rios do OpenStreetMap | Gratuitos, com atribuição e obrigações da licença ODbL | **Verificado** (`docs/creditos-dados.md`) |
| Atualização do grafo | Tempo de engenharia e hospedagem de um arquivo pequeno. A Overpass API pública não deve ser usada para consultas repetidas; usar extração local (por exemplo, da Geofabrik) | O repositório orienta; custo a levantar |

**Consequência:** o custo de mapas e rotas **não cresce com o número de usuários**, ao contrário de um serviço externo cobrado por requisição. Os custos que restam são horas de engenharia para manter o grafo e a chave do mapa, e as obrigações da licença do OpenStreetMap.

**Plataforma no cenário de trabalho:** hospedagem R$ 150 + clima R$ 145 + lojas R$ 52 = **R$ 346 por mês, cerca de R$ 4.153 por ano**, sem custo por uso de mapas e rotas.

### 3.4 Pessoas

A estrutura inicial é de **6 pessoas, os criadores do projeto, e no máximo 2 técnicos** para instalação e manutenção. A remuneração ainda não foi definida; o documento mostra três estruturas de custo, chamadas E0, E1 e E2 para não se confundirem com os cenários A e B de contratação.

| Estrutura | Quem | Custo fixo anual (R$) | Observação |
|---|---|---|---|
| E0 | 6 sócios sem pró-labore; mão de obra de campo por demanda (prestadores, paga por hora e já incluída nos custos por estação) | 0 | Fase de competição e de piloto |
| E1 | 6 sócios com pró-labore de um salário mínimo (R$ 1.621 em 2026, **verificado**); mão de obra de campo por demanda | 116.712 | Sem encargos; o regime tributário define os encargos (a confirmar com o contador) |
| E2 | 6 sócios a R$ 3.500 por mês (média do plano financeiro anterior, **premissa**) e 2 técnicos fixos a R$ 3.500 por mês com encargos (**premissa**) | 336.000 (252.000 dos sócios e 84.000 dos técnicos) | Os técnicos fixos substituem a mão de obra por demanda dos custos por estação |

**Os dois técnicos só se justificam em rede grande.** Cada estação exige, no primeiro ano, cerca de 32 horas-pessoa em campo (16 de instalação e 16 de duas vistorias) e, nos anos seguintes, 16. A rede do cenário A (8 estações) usa cerca de 256 horas por ano, e a do cenário B (30 estações), cerca de 960; dois técnicos em tempo integral oferecem cerca de 4.000 horas (premissa de 2.000 horas por pessoa). No **cenário A** (e em todo o início da operação) a hipótese de trabalho é **técnico por demanda**: o AquaScan chama um prestador para instalar e para cada vistoria e paga só pelo serviço (seção 3.2). A mão de obra por demanda custa cerca de R$ 1.052 por estação no primeiro ano (SINAPI): R$ 8,4 mil no cenário A e R$ 31,6 mil no B, contra R$ 84 mil por ano dos dois técnicos fixos. O ponto de cruzamento é de cerca de **80 estações** (R$ 84.000 ÷ R$ 1.052).

- **Recomendação (hipótese, confiança média):** manter o limite de 2 técnicos, mas contratá-los só quando a rede se aproximar de 80 estações; antes disso, usar prestadores por demanda, com os sócios treinados para as tarefas que não exigem habilitação. O custo real de um técnico contratado (salário e encargos) não foi levantado e pode mudar o cruzamento (hipótese C17).
- **Segurança em campo.** Fixar estação em ponte ou muro pode exigir habilitação para trabalho em altura (NR-35, enquadramento a confirmar).
- **Plantão em período de chuva.** Alerta fora do ar na cheia é a falha mais grave do produto. A escala de plantão dos sócios nos meses críticos não tem custo em caixa, mas tem custo em tempo e deve ser prevista.
- O pró-labore dos sócios não se confunde com o lucro (bloco Fonte de Renda e Lucro, seção 5).

### 3.5 Marketing e exposição da marca

O AquaScan fala com dois públicos. A **população** precisa instalar o aplicativo, porque é essa adesão que dá valor ao contratante; como o aplicativo é gratuito, essa divulgação é custo de entregar o serviço, não de vender. Os **órgãos públicos e as empresas** compram, e o objetivo com eles é credibilidade e relacionamento.

**Decisão do grupo para a fase inicial:** o **tráfego pago** e a **exposição da marca** ficam a cargo da **Defesa Civil e da Prefeitura**, pelos canais deles, até a estabilização financeira do AquaScan. O orçamento próprio de marketing fica restrito ao que o grupo produz e controla (conteúdo orgânico, material de apoio, site institucional e registro da marca).

| Canal | Quem paga e executa na fase inicial | O que inclui | Valor do AquaScan no primeiro ano (R$) | Base |
|---|---|---|---|---|
| Tráfego pago | **Defesa Civil e Prefeitura** (canais próprios, carro de som, rádio, escolas) | Divulgação do aplicativo à população nos meses de chuva | 0 | Decisão do grupo; depende de compromisso do órgão (hipótese C15) |
| Exposição da marca e eventos | **Defesa Civil e Prefeitura** | Crédito "tecnologia AquaScan" no aplicativo, nas placas das estações e nas divulgações do órgão (seção abaixo sobre limite legal) | 0 | Decisão do grupo; participação na Supernova tratada fora desta estrutura |
| Assessoria de imprensa | Pauta produzida pelo órgão e pela equipe | Releases e matérias locais | 0 | **Premissa** (tempo da equipe) |
| Orgânico | AquaScan | Conteúdo educativo em redes e vídeos curtos com o mascote; ferramentas de edição e agendamento | 3.000 | **Premissa**; a produção é feita pela equipe |
| Mídia física | AquaScan cria o material; o órgão distribui | Cartazes e folhetos para escolas, associações de moradores e pontos de apoio (2.500); placa com QR code do aplicativo em cada estação (R$ 40 por estação, incluída no custo por contrato) | 2.500 mais 40 por estação | **Premissa** |
| Mídia online e institucional | AquaScan | Site institucional com domínio e hospedagem (600 por ano); material institucional e relatório técnico diagramado (1.500, único) | 2.100 | **Premissa** |
| Registro da marca | AquaScan | Pedido no INPI para 2 classes (software e serviços), R$ 440 por classe com o desconto de 50% para microempresa (R$ 880 por classe sem desconto); o primeiro decênio não tem custo adicional | 880 | **Verificado** (tabela do INPI de dezembro de 2025); classes a confirmar |
| **Total do primeiro ano** | | | **8.480** | |

Nos anos seguintes saem os itens únicos (material institucional e registro da marca), e o total cai para **R$ 6.100 por ano**. Para comparação, o orçamento completo, com o AquaScan pagando tráfego pago (R$ 7.500), eventos (R$ 6.000) e banner de estande (R$ 1.200), seria de R$ 23.180 no primeiro ano; esses **R$ 14.700 ficam como verba de reativação**, a ser liberada quando a marca se estabilizar.

**Quando a marca assume o marketing.** Proposta de gatilho (hipótese, a validar pelo grupo): a contribuição dos contratos cobrir os custos fixos anuais da estrutura vigente (seção 7) por dois semestres seguidos, ou a assinatura do primeiro contrato do cenário B. Até lá, o AquaScan não paga mídia.

**Limite legal da exposição da marca pelo órgão público (confiança média; confirmar com advogado).** A publicidade de órgãos públicos deve ter caráter educativo, informativo ou de orientação social, sem promoção de marca ou de pessoas (Constituição, art. 37, § 1º). A Prefeitura e a Defesa Civil podem divulgar o **serviço** e informar que é prestado com tecnologia do AquaScan, mas não podem fazer propaganda comercial da empresa. Por isso a exposição da marca por esse caminho é **informativa e de menor alcance** do que a propaganda própria. Há também limites a publicidade institucional em período eleitoral (Lei 9.504/1997, art. 73), a conferir para o calendário de Petrópolis.

**Consequências dessa decisão:**
1. **O custo de marketing cai 63%, mas o risco migra para a dependência.** O alcance do aplicativo passa a depender de agenda, verba e vontade de um terceiro, sem garantia de intensidade. A adesão da população é o que dá valor ao contrato; sem ela, a renovação fica em risco.
2. **O crédito da marca precisa estar no contrato.** Cláusula de crédito "tecnologia AquaScan" no aplicativo, nas placas e em toda divulgação do serviço, e de uso do nome como referência (case) pelo AquaScan.
3. **O contrato deve prever a divulgação do aplicativo como obrigação do contratante** (canais, frequência e período de chuva), e não só como intenção.
4. **A dependência vale só para Petrópolis.** Em novo município ou cliente privado, a divulgação precisa ser negociada de novo.

### 3.6 Administração, seguros, jurídico e conformidade

Além do marketing, há custos que não aparecem no produto mas são necessários para operar e vender ao setor público.

| Item | Por que existe | Valor (R$) | Situação |
|---|---|---|---|
| Contabilidade | Emissão de nota, impostos, registro de pró-labore ou folha | 5.400 por ano (R$ 450 por mês) | **Verificado**: planos de R$ 259 (Basic) a R$ 450 por mês (Unique, com IRPF dos sócios), faixa de R$ 250 a R$ 950 no artigo da Agilize (2026). Adotado o plano Unique por haver 6 sócios |
| Impostos sobre a receita | ISS e tributos federais | Fora das margens deste documento | A definir com o contador |
| Seguros | Responsabilidade civil por falha de alerta e perda ou dano dos equipamentos | 3.600 por ano | **Premissa**, sem cotação (**confiança baixa**) |
| Jurídico | Contrato-modelo com limite de responsabilidade, termos de uso, política de privacidade e LGPD | 4.000, único | **Premissa** |
| Segurança da informação | O aplicativo guarda nome, e-mail, CEP, localização aproximada, senha em hash e token de notificação (**verificado** no modelo de dados), e a API recebe dados de campo. Inclui teste de invasão, revisão da autenticação e monitoramento de disponibilidade | 3.000 por ano | **Premissa** |
| Ferramentas, EPI e bancada | Kit de trabalho em altura, escada, multímetro, régua graduada, nível, bancada de teste de peças | 4.000, único | **Premissa** |
| Homologação de produto com transmissor de rádio | O produto final com rádio celular e Wi-Fi pode exigir homologação na Anatel, mesmo com módulos certificados | Sem valor | A confirmar (hipótese C9) |
| Proposta e documentação para contratação pública | Certidões, proposta técnica e acompanhamento | Incluído nos R$ 3.000 do cenário B | **Premissa** |

**Itens considerados de maior importância e que não estavam no orçamento:** seguros, segurança da informação, jurídico e plantão. Os dois primeiros protegem o negócio da falha mais cara, um alerta que não sai na cheia ou um vazamento de dados de moradores; o jurídico limita a responsabilidade no contrato; o plantão só tem custo em tempo. Um canal de aviso redundante (por exemplo, SMS para a Defesa Civil, além da notificação do aplicativo) deve ser avaliado, com custo a levantar.

---

## 4. Cenário A: dentro do limite de dispensa de licitação

O limite de dispensa para compras e serviços em 2026 é de **R$ 65.492,11** (verificado, fonte secundária; bloco Fonte de Renda e Lucro, seção 4). O pacote de entrada (estações, instalação e primeiro ano de serviço) precisa caber inteiro nesse valor, sem fracionamento. O limite fixa o preço total do pacote; o que ele deixa livre é o número de estações.

**Resultado no cenário de trabalho** (custo por estação no primeiro ano de R$ 4.176, mais R$ 4.153 de plataforma, preço do pacote igual ao limite, antes de impostos e dos custos fixos da seção 7):

| Estações no pacote | Preço médio por estação (R$) | Custo no primeiro ano (R$) | Margem (R$) | Margem |
|---|---|---|---|---|
| 5 | 13.098 | 25.031 | 40.461 | 61,8% |
| 8 | 8.187 | 37.558 | 27.934 | 42,7% |
| 10 | 6.549 | 45.909 | 19.583 | 29,9% |
| 13 | 5.038 | 58.436 | 7.056 | 10,8% |

**Teto de custo por estação** (instalada e operada no primeiro ano) para atingir cada margem, já descontada a plataforma:

| Estações | Margem 0% | Margem 30% | Margem 50% |
|---|---|---|---|
| 5 | 12.268 | 8.338 | 5.719 |
| 8 | 7.667 | 5.211 | 3.574 |
| 10 | 6.134 | 4.169 | 2.859 |
| 13 | 4.718 | 3.207 | 2.199 |

**Sensibilidade (pacote de 8 estações):** se as peças e a contingência custarem metade do cenário, a margem sobe para 60%; no valor do cenário, 43%; 50% acima, cerca de 26%; o dobro, 8%.

**Técnico por demanda: sensibilidade do valor pago ao prestador (pacote de 8 estações).** A mão de obra de campo do primeiro ano é de R$ 8.416 (8 × R$ 1.052, a preço de SINAPI). Se o preço de mercado for maior:

| Acréscimo sobre o SINAPI | Mão de obra de campo (R$) | Margem (R$) | Margem |
|---|---|---|---|
| 0% (cenário de trabalho) | 8.416 | 27.934 | 42,7% |
| 30% | 10.941 | 25.409 | 38,8% |
| 60% | 13.466 | 22.884 | 34,9% |
| 100% | 16.832 | 19.518 | 29,8% |

O acréscimo tira de 4 a 13 pontos percentuais da margem, mas não inverte o resultado: o prestador por demanda é a opção correta para o cenário A, pois o custo é variável e só existe se há contrato. A cotação real de dois prestadores (hipótese C17) fecha esse número.

**O que isso mostra:**
1. **Caber no limite é possível, mas a escala é pequena.** Com custo de cerca de R$ 4,2 mil por estação, o pacote comporta de 5 a 10 estações com margem positiva. Acima disso a margem some.
2. **A meta de "margem superior a 50%" do bloco Fonte de Renda e Lucro (sem benchmark) só é atingida, neste cenário, com 5 estações.** Com 8 estações o teto para 50% é R$ 3.574 por estação, abaixo dos R$ 4.176 do cenário. A meta deve ser tratada como ponto de partida, não como premissa.
3. **Os anos seguintes custam muito menos que o primeiro:** o custo de operar 8 estações é cerca de R$ 8,0 mil por ano mais o rateio da plataforma. A assinatura anual tem espaço, e também precisa caber no limite de dispensa (hipótese R5 do bloco Fonte de Renda e Lucro).
4. **Os resultados são mais sensíveis a três números ainda sem cotação:** a importação do sensor, a perda anual de estações e o tipo de sensor escolhido (hipótese RC8).

---

## 5. Cenário B: acima do limite de dispensa

Um contrato acima de R$ 65.492,11 não é impossível; ele exige processo licitatório. Os caminhos conhecidos:

| Caminho | Regra | Situação |
|---|---|---|
| Pregão | Modalidade obrigatória para bens e serviços comuns, com julgamento por menor preço ou maior desconto (Lei 14.133/2021, art. 6º, XLI, e art. 29) | **Verificado** |
| Contrato Público de Solução Inovadora (Marco Legal das Startups, Lei Complementar 182/2021) | Valor máximo de R$ 1,6 milhão pago à startup; vigência de 12 meses, prorrogável por mais 12 | **Verificado** em artigo de escritório de advocacia; o enquadramento do AquaScan como startup e como solução inovadora, e o contrato de fornecimento posterior, precisam ser confirmados |

**O que muda em relação ao cenário A:**
- **Garantia contratual** de até 5% do valor do contrato, e de até 10% em contratos de grande vulto (art. 96 da Lei 14.133/2021, **verificado** em fonte secundária). O custo do seguro-garantia varia com o contrato e com a análise de crédito da empresa; o valor não foi levantado.
- **Disputa por preço.** No pregão por menor preço, o preço final é definido na disputa, não pelo teto. Existe um preço mínimo abaixo do qual o contrato não vale a pena (tabelas abaixo).
- **Proposta e habilitação** mais custosas, e prazo maior até a assinatura.
- **Capital de giro maior**, porque as estações são compradas e instaladas antes do pagamento.

**Premissas do cenário B** (marcadas como **premissa**, a substituir): rede de **30 estações**, que cobre os principais rios (a quantidade real depende do município); mesmo custo por estação do cenário A (R$ 4.176 no primeiro ano); mesma plataforma (R$ 4.153 por ano); seguro-garantia de **1% do valor do contrato** (prêmio não verificado); proposta e habilitação de **R$ 3.000**. Antes de impostos e de pessoas.

**Margem por preço por estação (30 estações):**

| Preço por estação (R$) | Valor do contrato (R$) | Custo no primeiro ano (R$) | Margem (R$) | Margem |
|---|---|---|---|---|
| 5.000 | 150.000 | 133.921 | 16.079 | 10,7% |
| 6.549 | 196.470 | 134.385 | 62.085 | 31,6% |
| 8.187 | 245.610 | 134.877 | 110.733 | 45,1% |
| 10.000 | 300.000 | 135.421 | 164.579 | 54,9% |
| 12.000 | 360.000 | 136.021 | 223.979 | 62,2% |

**Margem por tamanho da rede:**

| Estações | Margem a R$ 8.187 por estação | Margem a R$ 10.000 por estação |
|---|---|---|
| 20 | 43,6% | 53,7% |
| 30 | 45,1% | 54,9% |
| 50 | 46,2% | 55,8% |

**Preço mínimo por estação (30 estações) para atingir cada margem:** R$ 4.459 para margem 0%; R$ 6.397 para 30%; R$ 9.008 para 50%.

**Escala:** se a compra em volume reduzir em 10% o custo das peças, da contingência e da reposição, a margem de 30 estações a R$ 8.187 sobe de 45,1% para 48,5%. É uma sensibilidade, não uma cotação.

**Caixa necessário antes do primeiro pagamento:** cerca de R$ 95 mil em peças e instalação de 30 estações, mais cerca de R$ 12 mil de garantia de 5% (a R$ 8.187 por estação), contra R$ 25 mil no cenário A (8 estações).

---

## 6. Comparação entre os cenários

| Aspecto | Cenário A: dispensa | Cenário B: licitação |
|---|---|---|
| Limite de valor | R$ 65.492,11 por exercício e objeto; fracionamento vedado | Sem teto no pregão; até R$ 1,6 milhão no contrato de solução inovadora |
| Estações no exemplo | 8 | 30 |
| Valor do contrato | R$ 65.492 | R$ 150 mil a R$ 360 mil, conforme o preço |
| Preço por estação | R$ 8.187, fixado pelo teto | Definido na disputa; abaixo de R$ 6.397 a margem fica inferior a 30% |
| Custo no primeiro ano | R$ 37.558 | R$ 134.877 (a R$ 8.187 por estação) |
| Margem | 42,7% (R$ 27.934) | 45,1% (R$ 110.733) a R$ 8.187; 31,6% a R$ 6.549; 54,9% a R$ 10.000 |
| Contribuição por contrato, antes dos custos fixos | R$ 32,1 mil | R$ 114,9 mil |
| Caixa antes de receber | R$ 25 mil | R$ 95 mil mais garantia de cerca de R$ 12 mil |
| Resultado do primeiro ano com 1 contrato, após custos fixos sem pessoas (E0) | Cerca de zero (prejuízo de R$ 0,9 mil) | Lucro de cerca de R$ 81,1 mil |
| Exigências | Proposta e contratação direta | Edital, habilitação, garantia contratual de até 5% |
| Risco principal | Escala pequena: a margem some acima de 10 estações | Disputa por preço, capital de giro e prazo do processo |

**Leitura.**
1. **A margem percentual é parecida (43% e 45% ao mesmo preço por estação); o que muda é o valor absoluto, o risco e o capital.** O cenário B gera quatro vezes mais margem por contrato e exige quase quatro vezes mais caixa.
2. **A dispensa limita o tamanho, não o preço:** o piloto cabe em até cerca de 13 estações, e com margem aceitável em cerca de 8.
3. **No cenário B, o preço é o que decide.** Com disputa por menor preço, a margem fica entre 11% e 62% conforme o lance; abaixo de R$ 6,4 mil por estação ela cai de 30%.
4. **Caminho recomendado (hipótese, confiança média):** começar pelo cenário A, que prova a solução com baixo capital, e propor o cenário B (ou o contrato de solução inovadora) com os dados do piloto, depois de o município ter visto o resultado. Este ponto depende de o município querer ampliar a rede (hipótese C12).

---

## 7. Estrutura de custos do negócio e ponto de equilíbrio

**Classificação.**

| Tipo | Custos |
|---|---|
| Variáveis, por estação | Peças, contingência, instalação (no primeiro ano); plano de dados, vistorias e reposição (todo ano); placa com QR code |
| Variáveis, por contrato | Seguro-garantia e proposta (cenário B) |
| Fixos, sem pessoas | Plataforma, marketing próprio (sem tráfego pago e eventos na fase inicial), contabilidade, seguros, segurança da informação, jurídico, ferramentas |
| Fixos, pessoas | Pró-labore dos sócios e técnicos fixos, conforme a estrutura E0, E1 ou E2 (seção 3.4) |

**Custos fixos sem pessoas.**

| Item | Primeiro ano (R$) | Anos seguintes (R$) |
|---|---|---|
| Plataforma | 4.153 | 4.153 |
| Marketing próprio (sem tráfego pago e exposição da marca, a cargo do órgão) | 8.480 | 6.100 |
| Contabilidade | 5.400 | 5.400 |
| Seguros | 3.600 | 3.600 |
| Segurança da informação | 3.000 | 3.000 |
| Jurídico | 4.000 | 0 |
| Ferramentas, EPI e bancada | 4.000 | 0 |
| **Total sem pessoas** | **32.633** | **22.253** |

**Contribuição por contrato** (receita menos custos variáveis, antes dos custos fixos): cenário A, cerca de **R$ 31,8 mil** (R$ 65.492 menos o custo de 8 estações no primeiro ano e as placas); cenário B, a R$ 8.187 por estação e 30 estações, cerca de **R$ 113,7 mil** (R$ 245.610 menos o custo das estações, o seguro-garantia, a proposta e as placas). Na estrutura E2, os técnicos fixos substituem a mão de obra por demanda, e a contribuição sobe para R$ 40,2 mil (A) e R$ 145,3 mil (B).

**Contratos por ano necessários para cobrir os custos fixos:**

| Estrutura | Custo fixo total, primeiro ano (R$) | Contratos A no primeiro ano | Contratos B no primeiro ano | Custo fixo total, anos seguintes (R$) | Contratos A depois | Contratos B depois |
|---|---|---|---|---|---|---|
| E0: sócios sem pró-labore | 32.633 | 1,0 | 0,3 | 22.253 | 0,7 | 0,2 |
| E1: sócios com um salário mínimo | 149.345 | 4,7 | 1,3 | 138.965 | 4,4 | 1,2 |
| E2: sócios a R$ 3.500 e 2 técnicos fixos | 368.633 | 9,2 | 2,5 | 358.253 | 8,9 | 2,5 |

**Resultado do primeiro ano com um único contrato, na estrutura E0:** cenário A, **resultado próximo de zero (prejuízo de cerca de R$ 0,9 mil)**; cenário B, **lucro de cerca de R$ 81,1 mil**. Com o marketing pago pelos órgãos, um contrato do cenário A cobre os custos fixos sem pessoas; com o orçamento completo de marketing (R$ 23.180) o prejuízo seria de R$ 15,6 mil.

**Leitura crítica.**
1. **Com o marketing a cargo dos órgãos, os custos fixos sem pessoas (R$ 32,6 mil) ficam do tamanho da contribuição de um contrato do cenário A (R$ 31,8 mil).** Em E0, um contrato por ano empata no primeiro ano e sobra no seguinte; qualquer remuneração dos sócios já exige vários contratos.
2. **A economia de marketing é real, mas é transferência de dependência, não eliminação de risco.** O ponto de equilíbrio só vale se o órgão cumprir a divulgação; se o aplicativo não for instalado pela população, o contrato não é renovado (seção 3.5). Quando a verba de reativação de R$ 14.700 for liberada, o equilíbrio em E0 volta a cerca de 1,5 contrato A por ano.
3. **A estrutura E2 só se sustenta com contratos do tipo B ou com vários municípios:** exige cerca de 9 contratos A ou 3 contratos B por ano.
4. **Caminho coerente com os números:** operar em E0 durante a competição e o piloto, passar a E1 quando houver contrato recorrente e só contratar técnicos fixos quando a rede se aproximar de 80 estações (seção 3.4).

---

## 8. Dependências e riscos

| Risco | Impacto | Mitigação |
|---|---|---|
| Câmbio e importação do sensor | Sensor importado em dólar; o custo varia com o câmbio e com os impostos de importação | Cotar fornecedores nacionais e importadores; manter margem para variação |
| Disponibilidade de peças | Várias peças estavam esgotadas em 16/10/2026 | Comprar reposição junto com o primeiro lote; mais de um fornecedor por peça |
| Uso comercial do Open-Meteo | Custo não previsto ou necessidade de trocar de fonte | Confirmar o valor com o fornecedor (hipótese C5) |
| Chave e termos do mapa no Android | O SDK de mapa nativo exige chave do Google; mudança de termos pode gerar cobrança | Confirmar os termos antes da publicação; registrar a chave e as restrições de uso (hipótese C6) |
| Obrigações da licença do OpenStreetMap | O grafo de ruas é uma base derivada; se distribuído, pode precisar continuar aberto sob a ODbL | Manter atribuição e confirmar as obrigações com quem entende de licenças |
| Perda de estações | Cheias, descarga elétrica e furto aumentam a reposição | Reserva de reposição; fixação em locais protegidos; seguro a cotar |
| Cobertura de rede | Falha de comunicação em vales e encostas | Teste de campo antes de fixar o ponto (hipótese C4) |
| Prazo de pagamento do poder público | Exige capital de giro entre a instalação e o recebimento | Levantar o prazo real com o setor de compras (hipótese C11) |
| Disputa por menor preço (cenário B) | Preço abaixo do mínimo leva a margem a menos de 30% ou a prejuízo | Definir o preço mínimo antes do lance; não participar abaixo dele (hipótese C12) |
| Garantia contratual e capital (cenário B) | Garantia de até 5% e compra antecipada de 30 estações | Cotar o seguro-garantia e dimensionar o caixa (hipótese C13) |
| Equipe contratada antes da receita | Compromete o caixa e o ponto de equilíbrio | Estruturas E0 e E1 da seção 3.4; técnicos fixos só perto de 80 estações |
| Divulgação do aplicativo depende do órgão público | Baixa adesão da população reduz o valor do contrato e a renovação; limite legal à promoção de marca | Cláusula contratual de divulgação e de crédito à marca; verba de reativação de R$ 14.700; medir instalações (C14 e C15) |
| Prestador de campo indisponível na cheia | Estação sem manutenção quando mais precisa | Dois prestadores cadastrados, procedimento escrito e sócio treinado (C17) |
| Alerta fora do ar na cheia | Falha mais grave do produto; risco jurídico e de imagem | Plantão em período de chuva, monitoramento, seguro e canal redundante (C10 e C16) |

---

## 9. Hipóteses a validar

| # | Hipótese | Como testar | Critério |
|---|---|---|---|
| C1 | O custo real de uma estação de campo cabe no teto da seção 4 | Cotar os itens marcados como premissa na seção 3.1 (painel, importação do sensor, suporte e placa, deslocamento) em pelo menos duas lojas ou fornecedores, com data, e confirmar o IP65 da caixa | Custo instalado mais operação do primeiro ano igual ou inferior a R$ 5.211 (pacote de 8 estações, margem de 30%) |
| C2 | A instalação conjunta leva um dia com duas pessoas e custa até R$ 626 | Instalar o ponto do piloto registrando tempo e despesas | Custo e tempo dentro do valor |
| C3 | O consumo de dados de uma estação cabe em um plano de 50 a 100 MB por mês | Medir bytes por envio em bancada por 7 dias, com o intervalo de leitura definido | Consumo mensal projetado igual ou inferior a 50 MB |
| C4 | Há cobertura de NB-IoT ou LTE-M nos pontos de instalação de Petrópolis | Teste de campo do módulo com chip IoT nos pontos candidatos | Pelo menos 95% dos envios entregues em 7 dias |
| C5 | O uso comercial do Open-Meteo tem custo conhecido ou há alternativa permitida | Escrever ao fornecedor pedindo o preço do plano comercial e as condições do plano gratuito | Valor mensal confirmado por escrito, ou fonte alternativa definida |
| C6 | O mapa e o roteamento do aplicativo não geram cobrança por uso | Ler os termos do SDK de mapa do Google para Android e do mapa do iOS; medir o tamanho do grafo da cidade e a frequência de atualização | Nenhuma cobrança por uso confirmada nos termos e grafo distribuível sem custo relevante |
| C7 | A perda anual de estações é igual ou inferior a 10% | Piloto de 90 dias, mais histórico da Defesa Civil sobre danos a equipamentos em rios | Taxa observada e reserva ajustada |
| C8 | A estrutura de equipe permite ponto de equilíbrio com poucos contratos | Definir os custos fixos mensais reais e calcular os contratos necessários | Na estrutura definida (E0 ou E1), ponto de equilíbrio igual ou inferior a 2 contratos do cenário A por ano, ou a 1 do cenário B |
| C9 | A homologação do produto final na Anatel tem custo e prazo conhecidos | Consultar a Anatel ou um organismo de certificação | Lista de exigências, custo e prazo |
| C10 | O contrato limita a responsabilidade por falha de alerta e há seguro viável | Revisão do contrato-modelo por advogado e cotação de seguro | Cláusula revisada e cotação obtida |
| C11 | O prazo de pagamento do município é compatível com o caixa | Consulta ao setor de financeiro e compras de Petrópolis | Prazo informado e capital de giro dimensionado |
| C12 | O município quer ampliar a rede acima do limite de dispensa, e o objeto pode ser licitado por pregão ou contratado como solução inovadora | Conversa com a Defesa Civil e o setor de compras, com os resultados do piloto | Interesse declarado, modalidade indicada e faixa de orçamento; preço mínimo por estação definido |
| C13 | O seguro-garantia e a garantia de até 5% cabem no caixa | Cotar o seguro-garantia com corretoras para um contrato de R$ 250 mil | Prêmio igual ou inferior a 1% do valor do contrato (premissa do cenário B) |
| C14 | Quando o AquaScan voltar a pagar tráfego, o custo por instalação do aplicativo fica entre R$ 3 e R$ 15 em Petrópolis (dimensiona a verba de reativação) | Campanha de teste de R$ 500 por 2 semanas, geolocalizada, em Android e iOS | Custo por instalação medido e igual ou inferior a R$ 15 |
| C15 | Prefeitura e Defesa Civil assumem tráfego pago e exposição da marca na fase inicial, dentro do limite legal da publicidade pública | Conversa com o órgão; minuta de cláusula de divulgação e crédito; consulta a advogado sobre o art. 37, § 1º da Constituição | Compromisso por escrito de ao menos dois canais e do crédito "tecnologia AquaScan" |
| C16 | Seguros e canal redundante de aviso cabem no orçamento | Cotar seguro de responsabilidade civil e de equipamentos em duas corretoras; levantar o custo de SMS para a Defesa Civil | Cotações obtidas; seguros iguais ou inferiores a R$ 3.600 por ano |
| C17 | O prestador por demanda custa até 30% acima do SINAPI e há disponibilidade na cheia; o técnico contratado só compensa perto de 80 estações | Cotar com dois prestadores (preço por instalação e por vistoria, valor mínimo por chamado, atendimento de emergência) e levantar o custo de um técnico com encargos | Preços reais conhecidos e ponto de cruzamento recalculado |

---

## Referências

**Estação de campo e comunicação (consultadas em 16/10/2026)**
- [Usinainfo: ESP32 NodeMCU 30 pinos CP2102](https://www.usinainfo.com.br/esp32/esp32-nodemcu-iot-com-wifi-e-bluetooth-30-pinos-com-cp2102-5147.html)
- [Curto Circuito: placa DOIT ESP32 (ESP32-WROOM-32D)](https://curtocircuito.com.br/placa-doit-esp32-esp32-wroom-32d-wifi-bluetooth.html)
- [Curto Circuito: módulo SIM7080G](https://curtocircuito.com.br/modulo-sim7080g-4g-lte-gps-antena-fcp-gps.html)
- [Curto Circuito: módulo A7670SA](https://curtocircuito.com.br/modulo-a7670sa-4g-lte-antena-fcp.html)
- [MaxBotix: MB7389](https://maxbotix.com/products/mb7389)
- [Minha Casa Solar: controlador de carga PWM 10 A Sun21](https://www.minhacasasolar.com.br/controladores-de-carga)
- [Minha Casa Solar: kit de 5 baterias Moura VRLA 12 V 9 Ah](https://www.minhacasasolar.com.br/kit-5-baterias-estacionaria-vrla-9ah-12v-moura-nobreak-12mva9-83241)
- [Usinainfo: prensa-cabo PG7 IP67](https://www.usinainfo.com.br/conectores-e-adaptadores/prensa-cabo-pg7-ip67-14-para-condutor-de-35-a-65mm-5043.html)
- [NeoSolar: kit solar de 10 Wp (painel e controlador)](https://www.neosolar.com.br/loja/kit-energia-solar-fotovoltaica-10wp.html)
- [Orçamentor/SINAPI 07/2026: eletrotécnico (horista)](https://orcamentor.com/insumo/2438/)
- [Orçamentor/SINAPI 07/2026: ajudante de eletricista (horista)](https://orcamentor.com/insumo/247/)
- [Orçamentor/SINAPI 07/2026: caixa de passagem de sobrepor](https://orcamentor.com/insumo/43097/)
- [RS: Vega série 61 (PS61) e substituto PS6X](https://uk.rs-online.com/web/p/level-sensors/9010299)
- [Vivo: ofertas M2M](https://vivo.com.br/para-empresas/produtos-e-servicos/servicos-essenciais/movel/m2m-e-kite-platform/ofertas)
- [Tecnoblog: Anatel reduz impostos de chips para Internet das Coisas](https://tecnoblog.net/379991/anatel-reduz-impostos-de-chips-para-internet-das-coisas/)

**Plataforma, mapa e rotas**
- Repositório aquascan-app (consultado em 16/10/2026): README, `docs/decisoes.md` (roteamento offline), `docs/creditos-dados.md` (OpenStreetMap e ODbL), `docs/solucao-de-problemas.md` (chave do Google Maps no Android), `packages/roteamento` e `packages/desvio`
- [Google Maps Platform: visão geral de cobrança](https://developers.google.com/maps/billing/overview/)
- [Google Maps Platform: tabela global de preços](https://developers.google.com/maps/billing-and-pricing/pricing)
- [Open-Meteo: preços e termos](https://open-meteo.com/en/pricing)
- [Open-Meteo: assinaturas para uso comercial (2023)](https://openmeteo.substack.com/p/api-subscriptions-for-commercial)
- [Expo: planos e cobrança](https://docs.expo.dev/billing/plans/)
- [vpsbenchmarks: Hetzner CX22](https://vpsbenchmarks.com/hosters/hetzner/plans/cx22)
- [Canaltech: custos para publicar aplicativos nas lojas](https://canaltech.com.br/apps/como-publicar-um-app-na-play-store-e-app-store-entenda-o-processo-das-lojas/)

**Contratação, câmbio e financiamento**
- [Effecti: limites de dispensa de licitação em 2026 (Decreto 12.807/2025)](https://effecti.com.br/decreto-12807-de-2025/)
- [Lei nº 14.133/2021, arts. 6º, 29 e 75](https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2021/lei/l14133.htm)
- [Effecti: seguro-garantia em licitações públicas (art. 96)](https://effecti.com.br/sem-categoria/seguro-garantia-licitacoes-publicas/)
- [Demarest: Marco Legal das Startups sancionado (CPSI)](https://www.demarest.com.br/marco-legal-das-startups-e-sancionado/)
- [O Povo: fechamento do mercado financeiro, 09/10/2026](https://www.opovo.com.br/noticias/economia/2026/10/09/fechamento-do-mercado-financeiro.html)

**Marketing, pessoas e administração (consultadas em 16/10/2026)**
- [INPI: tabela de retribuições, marcas (dez/2025)](https://www.gov.br/inpi/pt-br/servicos/custos-e-pagamento/NovaTabeladeRetribuiesINPI_MARCAS_Final_20_dez_25.pdf)
- [Agilize: custo de contabilidade para empresas](https://agilize.com.br/artigos/?p=881)
- [Bahia Notícias: salário mínimo de 2026 fixado em R$ 1.621](https://www.bahianoticias.com.br/noticia/311858-salario-minimo-para-2026-e-fixado-em-r-1621-com-reajuste-de-679)
- [Trafius: quanto custa anunciar no Facebook e Instagram](https://trafius.com.br/blog/quanto-custa-anunciar-facebook-instagram)
