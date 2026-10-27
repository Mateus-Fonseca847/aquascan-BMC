# Business Model Canvas · 7. Atividades-Chave

## Introdução

O AquaScan só entrega sua proposta de valor, o aviso confiável do nível do rio em cor, porcentagem e texto, se um conjunto de atividades funcionar de ponta a ponta: da leitura do sensor até o alerta no celular, e da venda ao órgão até a manutenção da estação no rio. Este documento descreve o bloco **Atividades-Chave** do Business Model Canvas: o que o AquaScan precisa fazer, com que frequência e quem executa, para entregar o valor aos clientes.

O texto trata só desse tema. Os recursos que essas atividades usam estão em Recursos-Chave; o que cada atividade exige do cliente e dos parceiros, em Relacionamento com Clientes e Parcerias-Chave; os custos, em Estrutura de Custos.

**Legenda das evidências:** **Verificado** (fonte pública ou repositório do projeto, em Referências) · **Vivência** (observação dos integrantes, moradores de Petrópolis, RJ) · **Hipótese** (a validar, ver seção 7).

---

## 1. Visão geral

| Categoria | Atividade principal | Quem executa |
|---|---|---|
| Plataforma | Desenvolver e evoluir firmware, API e aplicativo | Sócios (software e firmware) |
| Dados | Operar a API, o banco e a infraestrutura; monitorar leituras e estações | Sócios (software) |
| Estação de campo | Montar, instalar, calibrar e manter as estações | Sócios (hardware) e prestadores de campo por demanda |
| Calibração e validação | Definir cota, limiares e revisar alertas com a Defesa Civil | Sócios (hidrologia e institucional), com a Defesa Civil e a universidade |
| Atendimento e capacitação | Plantão em chuva, suporte, treinamento e simulados | Sócios e parceiros |
| Vendas e contratação | Prospectar, demonstrar, pilotar, propor e contratar | Sócios (institucional) |
| Gestão e conformidade | LGPD, Anatel, contabilidade, seguros, segurança da informação | Sócios, contador e advogado |

---

## 2. Perguntas-chave

| Pergunta | Resposta |
|---|---|
| Que atividades a proposta de valor exige? | Medir e calcular o nível com confiabilidade, entregar o alerta no celular, calibrar cada ponto com a Defesa Civil e manter as estações funcionando em ambiente de rio |
| Que atividades os canais exigem? | Publicar e atualizar o aplicativo nas lojas, manter a API no ar nos picos de chuva, instalar a estação e treinar quem usa (Canais, seção 3) |
| Que atividades o relacionamento exige? | Plantão no período chuvoso, relatórios, revisão pós-evento, simulados e manutenção preventiva (Relacionamento com Clientes, seção 3) |
| Que atividades as fontes de renda exigem? | Prospecção, piloto, proposta e contratação; instalação e ativação dos pontos; manutenção e suporte que sustentam a assinatura (Fonte de Renda e Lucro) |

---

## 3. Atividades por categoria

### 3.1 Plataforma: firmware, API e aplicativo

| Atividade | Descrição | Frequência |
|---|---|---|
| Firmware da estação | Medir a distância até a água, filtrar leituras anormais e enviar à API | Evolução contínua; atualização por ponto |
| API e cálculos | Converter distância em nível, porcentagem e estado (estável, atenção, crítico); calcular tendência, estatística, eventos e tempo até o transbordamento; avaliar a qualidade dos dados; registrar alertas (medições detalhadas abaixo) | Contínua |
| Aplicativo | Mapa, estado dos rios, previsão, pontos de apoio, cadastro, notificações e exclusão de conta | Versões periódicas |
| Notificações | Enviar alerta de piora na cidade do usuário, com controle de oscilação para não repetir aviso | Contínua |
| Qualidade e versões | Testes automáticos, controle de versão e integração contínua | A cada alteração |
| Simulador | Simular estações e rio subindo, para testar e demonstrar sem estação física | Sob demanda |

**Tecnologia (verificado no repositório):** TypeScript em todo o software; aplicativo em React Native com Expo; API em Node.js com Fastify; banco PostgreSQL com PostGIS e Prisma; testes com Vitest e integração contínua no GitHub Actions. O firmware das estações está em repositório próprio.

**Medições e métricas que a plataforma produz.** A única grandeza medida em campo é a distância até a água; tudo o mais é calculado pela API a partir dela, dos dados externos e do cadastro de cada ponto.

| Grupo | O que é medido ou calculado | Origem | Situação |
|---|---|---|---|
| Medição em campo | Distância do sensor até a superfície da água, a cada intervalo, com filtro de leituras impossíveis e saltos bruscos | Sensor e firmware | Em uso |
| Nível | Nível atual em centímetros (altura de instalação menos a distância); porcentagem da cota de transbordamento; metros restantes até transbordar | API, com a cota de cada ponto | Porcentagem em uso; demais definidos |
| Estado de risco | Estado em cor, ícone e texto (estável, atenção e crítico no aplicativo); índice de 0 a 100 | API | Estado em uso; índice definido |
| Tendência e previsão | Taxas de subida e descida em janelas de 5, 10, 30 e 60 minutos; aceleração da subida; tempo estimado até o nível crítico e até o transbordamento | API | Tempo estimado em uso; demais definidos |
| Estatística | Máximo, mínimo, média, mediana, desvio padrão, amplitude e percentis do período | API | Definida |
| Eventos | Início da subida, pico, recessão, fim, duração e nível máximo de cada evento de cheia | API | Definida |
| Histórico | Série de leituras de cada estação; gráficos de nível, taxa de subida e previsão contra valor real | API e aplicativo | Lista das últimas 24 horas em uso; gráficos pendentes |
| Qualidade dos dados | Leituras impossíveis, saltos bruscos, sensor sem resposta e dados ausentes; estação sem leitura recente aparece como "Sem dados" | Firmware e API | Parcialmente em uso |
| Diagnóstico da estação | Sensor funcionando, possível falha ou obstrução, perda de comunicação | Firmware e API | Definido |
| Vazão e volume | Vazão instantânea, média e máxima, volume acumulado e relação entre nível e vazão | Sensor de fluxo (tubulação) e API | Armazenada; exibição pendente. Em rio aberto exige equipamento próprio |
| Clima | Previsão de chuva dos próximos 7 dias, com classificação de perigo por cor | Fonte externa de previsão, via API | Em uso (limites provisórios) |
| Pontos de apoio e rotas | Pontos de apoio com telefone, capacidade e rota até o local; rotas entre locais que evitam áreas de risco | Lista da Defesa Civil e aplicativo; **funcionamento em definição** | Lista e contato em uso |

A cota de transbordamento e os limiares de cada ponto são definidos com a Defesa Civil (seção 3.4); sem eles a porcentagem não tem valor.

### 3.2 Dados e infraestrutura

| Atividade | Descrição | Frequência |
|---|---|---|
| Operar a API e o banco | Hospedagem com HTTPS, backups e capacidade para os picos de acesso durante tempestades | Contínua |
| Monitorar as estações | Acompanhar leituras recebidas, estações sem dados, bateria e falhas de sensor, para agir antes do cliente perceber | Contínua, reforçada em chuva |
| Integrar dados externos | Previsão de chuva e dados públicos de rios e clima, com cache | Contínua |
| Segurança da informação | Controle de acesso, tokens por estação, senhas com hash, logs sem dado pessoal | Contínua |
| Histórico e relatórios | Guardar o histórico de leituras e gerar os relatórios para os órgãos | Mensal e após eventos |

### 3.3 Estação de campo: produção, instalação e manutenção

| Atividade | Descrição | Frequência |
|---|---|---|
| Compra e estoque | Comprar os componentes (sensor, controlador, comunicação, energia, caixa) e manter estoque de reposição | Por lote |
| Montagem e teste de bancada | Montar a estação, testar sob umidade e variação térmica e calibrar o sensor | Por estação |
| Instalação conjunta | O órgão indica o ponto; a equipe fixa a estação em ponte, muro ou margem, liga a energia e a comunicação e confere o envio | Por estação |
| Vistorias preventivas | Duas por ano por estação: limpar o sensor, verificar bateria e fixação, conferir a leitura | Semestral, antes do período chuvoso |
| Manutenção corretiva | Reparar ou substituir estação danificada por cheia, descarga elétrica ou vandalismo | Sob demanda; prioridade em chuva |
| Reposição | Substituir peças e estações perdidas | Sob demanda |

Montagem e calibração ficam com os sócios; instalação e vistorias podem ser feitas por prestadores de campo por demanda, com procedimento escrito e capacitação mínima (Estrutura de Custos, seção 3.2). Fixação em ponte ou muro pode exigir habilitação para trabalho em altura (NR-35, enquadramento a confirmar).

### 3.4 Calibração e validação com a Defesa Civil

| Atividade | Descrição | Frequência |
|---|---|---|
| Cota de transbordamento por ponto | Levantar com o órgão a cota e as referências de campo, base da porcentagem | Por ponto, na instalação |
| Limiares de atenção e crítico | Definir e validar, ponto a ponto, com a Defesa Civil | Por ponto; revisão após eventos |
| Pontos de apoio | Integrar a lista fornecida pelo órgão (nome, local, telefone, capacidade) e manter a data de atualização visível | Conforme atualização do órgão |
| Revisão pós-evento | Comparar o aviso com o que ocorreu e ajustar os limiares | Após cada evento relevante |
| Validação técnica | Revisão dos cálculos e da calibração por universidade ou centro de pesquisa | Por ciclo |
| Base geográfica e rotas | Dados de ruas, áreas de risco e roteamento do aplicativo; **funcionamento em definição** | A definir |

### 3.5 Atendimento, capacitação e educação

| Atividade | Descrição | Frequência |
|---|---|---|
| Plantão e suporte | Atendimento em regime de plantão nos períodos de chuva e alertas críticos, com horário comercial nos demais; migração para suporte 24 horas com o crescimento (Relacionamento com Clientes, seção 6) | Contínua, reforçada em chuva |
| Capacitação do órgão | Treinar a equipe da Defesa Civil no uso do aplicativo e dos relatórios | Na implantação e a cada renovação |
| Capacitação de prestadores | Procedimento de instalação, calibração e segurança para os prestadores de campo | Antes do primeiro serviço e a cada revisão do procedimento |
| Simulados e educação | Ações com escolas e associações de moradores, em conjunto com a Defesa Civil, e conteúdo educativo nas redes | Antes do período chuvoso |
| Canal de retorno | Receber e tratar relatos dos moradores: ponto de apoio desatualizado, estação sem dados, alerta sem sentido | Contínua |

### 3.6 Vendas, contratação e parcerias

| Atividade | Descrição | Frequência |
|---|---|---|
| Prospecção e demonstração | Contato com órgãos e, depois, com empresas; demonstração do sistema (Canais, seções 3 e 5) | Contínua |
| Piloto | Estações em pontos do órgão, sob termo de cooperação, com relatório de resultado | Por cliente |
| Proposta e contratação | Proposta formal; contratação por dispensa dentro do limite ou licitação acima dele | Por contrato |
| Parcerias | Manter a relação com Defesa Civil, universidade, fornecedores e operadora (Parcerias-Chave) | Contínua |
| Renovação | Relatório anual e conversa de renovação antes do vencimento | Anual |

### 3.7 Gestão e conformidade

| Atividade | Descrição | Frequência |
|---|---|---|
| Privacidade (LGPD) | Consentimento, coleta mínima, exclusão de dados, termos de uso e política de privacidade | Contínua |
| Homologação | Anatel, para o módulo de comunicação do produto final (enquadramento a confirmar) | Antes da produção em escala |
| Administração | Contabilidade, seguros, contratos e controle financeiro | Mensal e anual |

---

## 4. Ritmo operacional

As atividades se concentram em torno do período de chuva:

| Momento | Atividades |
|---|---|
| Antes da chuva | Vistoria de todas as estações; teste de notificações; atualização dos pontos de apoio; simulados e educação |
| Durante a chuva | Plantão; monitoramento das estações e da API; atendimento ao órgão; manutenção corretiva de emergência |
| Depois de cada evento | Revisão com a Defesa Civil; ajuste de limiares; reparo e reposição; relatório ao órgão |
| Ao longo do ano | Desenvolvimento, vendas, parcerias, relatórios mensais e conformidade |

---

## 5. Fora do foco

| Atividade | Motivo |
|---|---|
| Fabricar sensores ou chips próprios | O modelo usa componentes comerciais de prateleira; o valor está na integração, na calibração e no serviço |
| Operar sirenes, resgate e salvamento | Competência legal da Defesa Civil e dos bombeiros; o AquaScan atua no monitoramento e na comunicação antecipada |
| Gerar previsão meteorológica própria | O aplicativo usa fonte externa de previsão; o produto mede o nível do rio, que a previsão não substitui |
| Modelos de inteligência artificial nesta fase | O cálculo é determinístico, com regressão para a tendência; a série de dados ainda é curta para modelos complexos |

---

## 6. Dependências e riscos

| Risco | Efeito | Mitigação |
|---|---|---|
| Atividades concentradas em poucas pessoas | Sobrecarga e falha de atendimento em chuva | Procedimentos escritos, prestadores por demanda, escala de plantão |
| Estação danificada na cheia | Ponto sem leitura quando mais se precisa | Vistoria antes da chuva, estoque de reposição, monitoramento de estação sem dados |
| API indisponível em pico de acesso | Alerta não chega | Capacidade dimensionada, cache, monitoramento e teste de carga |
| Cota ou limiar mal calibrados | Alerta falso ou atrasado | Validação com a Defesa Civil e revisão pós-evento |
| Dependência da Defesa Civil para cota e pontos de apoio | Estação sem porcentagem ou rota errada | Termo de cooperação e rotina de atualização combinada (Parcerias-Chave, seção 3) |

---

## 7. Hipóteses a validar

| Código | Hipótese | Como testar | Critério |
|---|---|---|---|
| AT1 | O sensor de campo mantém estabilidade de leitura sob chuva prolongada | Piloto em um ponto crítico, comparado a referência de medição | Erro aceitável frente à referência da Defesa Civil ou do órgão hidrológico |
| AT2 | A API e o aplicativo suportam picos de acesso simultâneo em tempestade | Teste de carga na API e no aplicativo | Tempo de resposta inferior a 2 segundos sob a carga prevista (meta proposta) |
| AT3 | As duas vistorias anuais mantêm a taxa de falhas dentro do projetado | Acompanhar falhas e perdas de estação no piloto | Taxa observada compatível com a reserva de reposição (Estrutura de Custos, C7) |
| AT4 | Prestadores de campo instalam e fazem vistoria com qualidade a partir do procedimento escrito | Instalação-teste com dois prestadores e checklist | Instalação correta, sem retrabalho |
| AT5 | O plantão em período chuvoso cobre os alertas críticos e os chamados | Escala simulada e registro de tempo de resposta no piloto | Resposta dentro do prazo definido (Relacionamento com Clientes, seção 3) |
| AT6 | A Defesa Civil valida cota e limiares em tempo compatível com a instalação | Acompanhar o prazo de validação no piloto | Limiares validados por ponto antes de entrar em operação |

---

## Referências

- Repositório aquascan-bmc, arquivo `atividades-chave.md` (versão anterior, consultada em 16/10/2026).
- Repositório aquascan-app (consultado em 16/10/2026): `README.md` (stack e fluxo de dados), `docs/requisitos.md`, `docs/privacidade.md`.
- Blocos do BMC do AquaScan: Recursos-Chave (seções 3 a 5), Relacionamento com Clientes (seções 3, 4 e 6), Canais (seções 3 e 5), Parcerias-Chave (seções 3 a 5), Estrutura de Custos (seções 3.2 e 3.4; hipótese C7).
