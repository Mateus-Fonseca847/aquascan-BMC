# Business Model Canvas · 1. Segmento de Mercado

## Introdução

O AquaScan é um sistema de monitoramento de rios que mede o nível da água com sensores de baixo custo e comunica o risco de transbordamento em porcentagem, cor e texto, com tempo estimado, por meio de um aplicativo. Este documento descreve o primeiro bloco do Business Model Canvas, o **Segmento de Mercado**: para quem o AquaScan cria valor.

Ao longo do texto são apresentados quem compra a solução (Defesas Civis, Prefeituras e empresas que dependem de rios), quem a utiliza no dia a dia (moradores, pessoas com rotina perto de rios e equipes de Defesa Civil), o perfil de cada grupo (agrupamento, localização, necessidades e comportamentos), os segmentos fora do foco, a abrangência geográfica e as hipóteses que ainda precisam ser validadas. Os demais blocos do canvas devem ser coerentes com o que está descrito aqui.

**Legenda das evidências:** **Verificado** (fonte pública em Referências) · **Vivência** (observação dos integrantes, moradores de Petrópolis, RJ, que vivenciaram enchentes) · **Pesquisa** (levantamento dos integrantes, fontes a anexar) · **Hipótese** (a validar, ver seção 7).

---

## 1. Visão geral

| Papel | Segmento | Paga? |
|---|---|---|
| Comprador principal | Defesa Civil municipal e Prefeitura | Sim |
| Comprador secundário | Empresas com ativo ou operação dependente de rio | Sim (hipótese) |
| Comprador terciário | Turismo de natureza em rio | Sim (hipótese) |
| Usuário final | Moradores de áreas próximas a rios | Não |
| Usuário final | Pessoas com rotina perto de rios (trabalho, escola, serviços) | Não |
| Usuário institucional | Equipe da Defesa Civil, pelo painel | Parte do contrato |

O usuário final não paga: informação de segurança em enchentes deve ser gratuita.

---

## 2. Perguntas-chave

| Pergunta | Resposta |
|---|---|
| Para quem criamos valor? | Para o poder público, que precisa ampliar o monitoramento de rios a baixo custo, e para quem vive ou circula perto de rios e precisa entender o risco |
| Quem sente a dor mais importante? | O morador de área de risco, que pode perder a casa e a vida (**vivência**) |
| Quem se beneficia mais? | Moradores e frequentadores, com aviso claro e antecipado; o município, com mais pontos de monitoramento |
| Quem compra? | Defesa Civil ou Prefeitura; onde não há compra pública, empresas |
| Quem usa? | Moradores e frequentadores pelo aplicativo; Defesa Civil pelo painel |
| Quem valoriza o diferencial e paga? | O poder público e empresas (**hipótese**). Diferencial: custo de entrada reduzido e risco em porcentagem, cor e texto, com tempo estimado para transbordar |

---

## 3. Compradores

### 3.1 Principal: Defesa Civil municipal e Prefeitura

- **Perfil:** município com rios urbanos e histórico de enchentes. Ponto de partida: Petrópolis (RJ).
- **Como adquire:** contrata o AquaScan; a instalação é conjunta (o órgão indica os pontos, a equipe do AquaScan instala e calibra); os sensores enviam dados a uma API que calcula as métricas e as grava em banco; a população acessa pelo aplicativo e a Defesa Civil, pelo painel. O órgão também fornece o relatório de pontos de apoio, que o AquaScan integra ao mapa.
- **Dor (hipótese):** poucos pontos de medição por rio e dificuldade de transformar dado técnico em informação que o morador use para decidir.
- **Recursos:** existe verba pública para prevenção e resposta a desastres (**vivência**); programas e valores serão levantados junto ao órgão (**hipótese**).
- **Preço de entrada:** contratações de menor valor podem ser feitas por dispensa de licitação. Em 2026 o limite é de **R$ 65.492,11** para compras e outros serviços e de **R$ 130.984,20** para obras e serviços de engenharia (Decreto 12.807/2025, **verificado** em fonte secundária; decreto federal, aplicação ao município a confirmar). A solução de entrada deve caber nessa faixa, sem excluir contratos maiores nem contratações emergenciais. O prazo médio de contratação não foi levantado.
- **Evidência de adoção (verificado):** Rio do Sul (SC) usa o E-Noé, da USP; Olinda (PE) tem o Ih, Alagou, com 10 postes de sensores; em Joinville (SC), uma universidade instalou um radar de nível com apoio da Defesa Civil.
- **Mercado (verificado):** 2.095 municípios na lista federal de prioridade; o Cemaden cobre 1.295 com pluviômetros. A lista inclui deslizamentos, e só parte dos municípios tem rios onde um sensor de nível se aplica.

### 3.2 Secundário: empresas com ativo ou operação dependente de rio (hipótese e pesquisa)

**Quando esse segmento entra.** Em cidades pequenas, sem Defesa Civil estruturada ou sem verba para comprar, não há poder público que adquira o produto e o disponibilize de graça. Quem depende do rio compra por conta própria. Onde a Defesa Civil já contratou, o aviso geral da cidade chega a todos, e a demanda privada tende a se restringir a quem precisa de um ponto exato no seu ativo (**hipótese**).

**Quem são (pesquisa dos integrantes).**

| Grupo | Dependência do rio |
|---|---|
| Energia | Hidrelétricas e geradoras; usinas solares instaladas perto de rios |
| Agronegócio | Lavouras e criações em área próxima a rios, irrigação, piscicultura |
| Saneamento | Captação e estações de tratamento em margem de rio |
| Comércio e imóveis | Lojas, restaurantes, concessionárias, empresas imobiliárias e condomínios em margem de rio |

**Por que é secundário.** Amplia a base de clientes além do setor público e permite entrar em municípios sem comprador público. A dor é financeira e direta: perda de estoque, equipamento, colheita ou operação.

**Prioridade de entrada (hipótese).** Agronegócio e comércio/condomínios primeiro: decisão do proprietário, ticket menor e necessidade de um ponto específico. Energia e saneamento de grande porte tendem a já ter telemetria profissional e exigir equipamento certificado; o encaixe é maior em pequenos operadores (pequenas centrais, usinas solares menores, saneamento de municípios pequenos). A validar.

**A validar.** Disposição de pagar, valor aceitável e autorizações para instalar sensor em ponte, muro ou margem (município e órgão ambiental).

### 3.3 Terciário: turismo de natureza em rio (hipótese)

Pousadas, cachoeiras, parques e operadores de aventura. A dor é a segurança do visitante diante de cheias repentinas. Compradores dispersos e de menor poder de compra.

---

## 4. Usuários

| | Moradores de áreas próximas a rios | Pessoas com rotina perto de rios | Equipe da Defesa Civil |
|---|---|---|---|
| **Agrupamento** | Por bairro e rua ao longo do mesmo rio | Por local de trabalho, estudo ou serviços | Por órgão municipal |
| **Localização** | Áreas de risco e margens; em Petrópolis há rios em praticamente toda a cidade (**vivência**) | Áreas centrais e comerciais cortadas por rios (**vivência**) | Sede do órgão |
| **Necessidade** | Saber a tempo se o rio sobe e quanto tempo resta para agir; proteger a casa e saber para onde ir se precisar sair (**vivência**) | Decidir quando sair e por onde voltar quando chove, longe de casa (**vivência**) | Acompanhar estações e apoiar decisão de alerta (**hipótese**) |
| **Comportamento** | Observam chuva e rio e seguem avisos oficiais; usam smartphone (**hipótese**) | Consultam o celular ao longo do dia; precisam de informação curta, em cor e texto (**hipótese**) | Já usam SMS e sirenes (**verificado**); o AquaScan se soma a esses canais |

**Como usam o aplicativo.** Salvam local de moradia e de trabalho, acompanham o rio de cada local e consultam todos os rios monitorados da cidade em um mapa, com nível, porcentagem do transbordamento, risco (baixo, moderado, alto) em cor e texto e tempo estimado para transbordar. Rio sem estação aparece como "sem monitoramento", nunca como seguro. Quando há contrato com a Defesa Civil, o mapa mostra também os **pontos de apoio** do órgão: ao tocar em um ponto, o usuário vê o telefone e a capacidade máxima de pessoas e pode traçar a rota até ele. Está prevista ainda a **rota** entre dois locais (por exemplo, da rua em que a pessoa está até casa ou trabalho) que evite áreas de risco associadas ao estado dos rios monitorados. A rota é indicativa: o sensor mede um ponto do rio, não a rua, e a informação não substitui a orientação da Defesa Civil.

**Escala de referência (verificado):** em Petrópolis, 72.070 moradores viviam em áreas de risco em 2010 (24,4% de 295.917). O número inclui deslizamento; é um teto, não o público-alvo.

**Limite:** quem não tem smartphone ou internet depende dos canais oficiais.

---

## 5. Fora do foco

| Segmento | Motivo |
|---|---|
| Seguradoras e venda de dados | Sem evidência de demanda; a ANA já oferece dados de rios gratuitamente |
| Órgãos estaduais e federais | Compras de maior volume; relevantes apenas em fase de escala |

---

## 6. Abrangência geográfica

Petrópolis (RJ) → região serrana fluminense → demais municípios brasileiros com rios urbanos → cidades costeiras, com adaptação do produto a maré e ressaca → países andinos com rios de montanha, como Peru e Colômbia. As duas últimas etapas são visão de longo prazo, não escopo inicial.

---

## 7. Hipóteses a validar

| # | Hipótese | Como testar | Critério |
|---|---|---|---|
| H1 | A Defesa Civil de Petrópolis tem interesse e orçamento para o produto | Entrevista com o órgão | Custo atual por estação, quem decide, prazo de contratação |
| H2 | O conjunto de sensores cabe na dispensa de licitação | Consulta ao setor de compras | Resposta formal sobre enquadramento |
| H3 | O morador entende porcentagem com cor melhor que metros | 10 a 15 moradores comparam duas telas | Taxa de acerto na decisão |
| H4 | Empresas de agronegócio, comércio e pequenas geradoras pagariam por sensor próprio | Três a cinco conversas | Ao menos uma disposição de pagar, com valor |
| H5 | Grandes geradoras e operadoras de saneamento aceitam sensor de baixo custo | Conversa com um operador | Requisitos técnicos e de certificação |
| H6 | A Defesa Civil fornece e mantém atualizada a lista de pontos de apoio (localização, telefone e capacidade máxima) em formato aproveitável | Solicitar o relatório atual e combinar a frequência de atualização | Lista recebida e responsável pela atualização definido |

---

## Referências

- [Revista Pesquisa FAPESP: E-Noé, 2023](https://revistapesquisa.fapesp.br/dispositivo-emite-em-tempo-real-alertas-contra-enchentes/)
- [Portal de Prefeitura: Olinda lança sistema de alerta contra enchente](https://portaldeprefeitura.com.br/regiao-metropolitana/olinda/prefeitura-de-olinda-lanca-sistema-de-alerta-contra-enchente/599671/)
- [NSC Total: radar de nível em Joinville](https://www.nsctotal.com.br/?p=2560512)
- [Casa Civil: Nota Técnica 1/2025](https://www.gov.br/casacivil/pt-br/assuntos/cadastro-de-municipios-suscetiveis-a-eventos-de-enxurradas-e-inundacoes/sei_6390694_nota_tecnica_1_2025.pdf)
- [Jornal de Brasília: Cemaden, 1.295 municípios, maio de 2026](https://jornaldebrasilia.com.br/noticias/brasil/cemaden-expande-rede-de-monitoramento-para-1-295-municipios/)
- [IBGE: população em áreas de risco, Censo 2010](https://agenciadenoticias.ibge.gov.br/agencia-sala-de-imprensa/21565-em-2010-brasil-tinha-8-3-milhoes-de-pessoas-morando-em-areas-com-risco-de-desastres-naturais.html)
- [Effecti: limites de dispensa de licitação em 2026 (Decreto 12.807/2025)](https://effecti.com.br/decreto-12807-de-2025/)
- [O Imparcial: ANA lança aplicativo gratuito com dados de rios, 2019](https://oimparcial.com.br/cidades/2019/04/ana-lanca-aplicativo-gratuito-com-dados-de-rios-e-chuvas-em-todo-o-brasil/)
