# Business Model Canvas · Fonte de Renda e Lucro

## Introdução

O AquaScan é um sistema de monitoramento de rios que mede o nível da água com sensores de baixo custo, instalados em conjunto com o cliente, e comunica o risco de transbordamento em porcentagem, cor e texto, com tempo estimado, por meio de um aplicativo gratuito para a população. Este documento descreve o bloco **Fonte de Renda e Lucro** do Business Model Canvas: quem paga, pelo quê, de que forma e com que previsibilidade o dinheiro entra, e como a receita se relaciona com o lucro.

Ao longo do texto são apresentadas as fontes de renda por segmento, a lógica de preço e de contratação pública, a relação entre receita e lucro e as hipóteses que ainda precisam ser validadas. Os custos detalhados ficam no bloco Estrutura de Custos; os segmentos de clientes, no bloco Segmento de Mercado. **Ainda não há preços definidos nem disposição de pagar validada**; os valores citados são referências de mercado ou limites legais, não o preço do AquaScan.

**Legenda das evidências:** **Verificado** (fonte pública em Referências) · **Vivência** (observação dos integrantes, moradores de Petrópolis, RJ) · **Pesquisa** (levantamento dos integrantes, fontes a anexar) · **Hipótese** (a validar, ver seção 6).

---

## 1. Visão geral

| Fonte | Quem paga | O que paga | Forma | Papel |
|---|---|---|---|---|
| Implantação do conjunto de estações | Defesa Civil e Prefeitura | Sensores, instalação conjunta e calibração | Pagamento único | Principal |
| Assinatura anual de plataforma e suporte | Defesa Civil e Prefeitura | Painel, aplicativo com mapa e pontos de apoio, API, manutenção e suporte | Recorrente | Principal |
| Estação dedicada para empresas | Empresas com ativo ou operação dependente de rio | Estação instalada, com assinatura opcional | Pagamento único mais assinatura | Secundária |
| Fomento e financiadores de impacto | Fundos, programas e empresas com ações sociais | Sensores para comunidades sem orçamento próprio | Pontual | Complementar |

**Quem não paga:** o morador e quem circula perto de rios usam o aplicativo gratuitamente. A venda de dados e a venda a seguradoras estão fora do foco, por falta de evidência de demanda, e a ANA já oferece dados de rios gratuitamente (**verificado**).

---

## 2. Perguntas-chave

| Pergunta | Resposta |
|---|---|
| Por qual valor os clientes estão dispostos a pagar? | Pela ampliação dos pontos de medição e pelo dado traduzido em risco, em porcentagem, cor e texto, com tempo estimado até o nível crítico. Disposição de pagar e valor **não validados** (**hipótese**) |
| Como pagam atualmente? | O poder público contrata soluções de monitoramento, como o E-Noé em Rio do Sul e Rio Branco, o radar de Joinville e o sistema de Olinda (**verificado**). Preços reais são pouco divulgados |
| Como prefeririam pagar? | Município: contrato direto de valor reduzido, com implantação e serviço no mesmo instrumento. Empresa: compra da estação com assinatura opcional (**hipótese**) |
| Quanto cada fonte contribui para a receita? | Sem dados. A expectativa é que o setor público seja a maior fonte e o setor privado a complementar; percentuais só serão estimados depois das entrevistas (**hipótese**) |

---

## 3. Fontes de renda

### 3.1 Implantação do conjunto de estações (setor público)

- **O que é vendido:** conjunto de estações de monitoramento, instalação em conjunto nos pontos que o órgão indica, calibração e configuração da plataforma para o município.
- **Quem paga:** Defesa Civil ou Prefeitura.
- **Forma:** pagamento único por contrato.
- **Ponto de atenção:** o preço precisa incluir a mão de obra e o deslocamento da equipe em campo, porque a instalação é conjunta (bloco Segmento de Mercado).

### 3.2 Assinatura anual de plataforma e suporte (setor público)

- **O que é vendido:** acesso ao painel da Defesa Civil, ao aplicativo e à API, integração e atualização da lista de pontos de apoio fornecida pelo órgão (telefone, capacidade máxima e rota até o local), manutenção preventiva e corretiva das estações, diagnóstico de falhas dos sensores e suporte.
- **Quem paga:** o mesmo órgão contratante.
- **Forma:** contrato anual (**hipótese**).
- **Pontos de apoio:** a lista vem do relatório do próprio órgão e só tem valor se for mantida atualizada; combinar a atualização em contrato. O custo recorrente do provedor de mapas entra em Estrutura de Custos.
- **Por que importa:** é a fonte recorrente. Sem ela, a receita fica concentrada na venda inicial, e o custo de manter plataforma e estações recai sobre o AquaScan.
- **Atenção:** a manutenção e o suporte são o que sustenta a receita mesmo que o código do projeto seja público. O valor do serviço está na instalação, na calibração, na operação e na garantia, e não apenas no software.

### 3.3 Estação dedicada para empresas (setor privado, hipótese e pesquisa)

- **O que é vendido:** estação instalada em ponto de interesse da empresa (agronegócio, pequenas geradoras de energia, saneamento de municípios pequenos, comércio e condomínios em margem de rio), com assinatura opcional para histórico, relatórios e alertas.
- **Quando acontece:** sobretudo em cidades sem Defesa Civil estruturada ou sem verba para comprar, onde nenhum órgão público disponibiliza o aviso a todos. Onde o município já contratou, a demanda privada tende a se restringir a quem precisa de um ponto exato no seu ativo (**hipótese**).
- **Forma:** pagamento único pelo equipamento instalado mais assinatura opcional.
- **Limite:** a medição de vazão em rio aberto exige equipamento hidrométrico próprio, de custo maior; o protótipo mede fluxo em tubulação. A oferta de "relatório de vazão" só deve ser vendida onde o equipamento permitir.

### 3.4 Fomento e financiadores de impacto (complementar, hipótese)

- **O que é:** recursos de fundos, programas de responsabilidade social de empresas e editais destinados a custear sensores em comunidades sem orçamento próprio.
- **Por que entra:** contorna a dependência do orçamento municipal e atende a lógica de impacto do canvas. É receita pontual, não recorrente.
- **Situação:** nenhum financiador identificado até agora.

---

## 4. Preço e contratação pública

**Limites de dispensa de licitação em 2026 (verificado, fonte secundária).** Compras e outros serviços: **R$ 65.492,11**. Obras e serviços de engenharia: **R$ 130.984,20** (art. 75, I e II, Lei 14.133/2021, conforme o Decreto 12.807/2025). O decreto é federal; a aplicação ao município e o enquadramento do objeto (compra de equipamento, serviço ou engenharia) precisam ser confirmados com o setor de compras.

**Três cuidados**
1. **Somatório no exercício.** A lei manda considerar o total gasto pela unidade gestora no exercício, em despesas do mesmo objeto ou ramo (art. 75, §1º, a confirmar). Dividir o conjunto em contratos menores para caber no limite é fracionamento e não é permitido. O pacote de entrada deve caber **inteiro** no limite: estações, instalação e o primeiro ano de serviço.
2. **Recorrência.** A assinatura dos anos seguintes é nova contratação e também deve caber no limite; do contrário, exige outro rito de contratação (**hipótese**).
3. **Exceções.** Contratações acima da faixa continuam possíveis, inclusive em situação de emergência, conforme a regra aplicável a cada caso. O prazo de contratação não foi levantado.

**Referências de preço do mercado (verificado)**

| Solução | Preço |
|---|---|
| E-Noé (USP) | Cerca de R$ 15 mil por conjunto |
| Radar de nível, Joinville | Cerca de R$ 138 mil |

**Quantas estações cabem na dispensa (aritmética ilustrativa, não é preço do AquaScan).** Se o preço total por estação instalada fosse de R$ 5 mil, cabem 13 estações no limite de R$ 65.492,11; a R$ 10 mil, cabem 6; a R$ 15 mil, cabem 4. O custo real da estação e o preço serão definidos pelo bloco Estrutura de Custos.

**Base do preço (hipótese).** O valor entregue é a ampliação de cobertura e a antecipação do aviso. O preço deve ficar abaixo das alternativas conhecidas e acima do custo total de implantação e operação. O custo de instalação em campo e o de manutenção das estações entram no cálculo.

---

## 5. Receita e lucro

**Receita** é tudo o que entra com as fontes acima; **lucro** é o que sobra depois de custos de fabricação, instalação, operação e impostos. Vender muito não significa lucrar: no AquaScan, o custo de estar em campo (instalação, manutenção, deslocamento) pode consumir a margem de contratos de valor baixo.

- **Margem por estação:** só pode ser estimada depois que o bloco Estrutura de Custos fechar o custo por estação instalada.
- **Meta de margem bruta (hipótese):** a definição fica pendente. O critério de "superior a 50%" não tem benchmark; deve ser tratado como meta de partida até haver custos e preços.
- **Receita recorrente:** o objetivo é que a assinatura cubra a operação e a manutenção contínuas, para que a venda inicial não seja a única fonte de caixa.
- **Pró-labore:** o salário dos sócios não se confunde com o lucro da empresa. Fica fora do cálculo deste bloco.

---

## 6. Hipóteses a validar

| # | Hipótese | Como testar | Critério |
|---|---|---|---|
| R1 | O pacote de entrada (estações, instalação e primeiro ano) cabe no limite de dispensa do município | Consulta ao setor de compras de Petrópolis | Resposta formal sobre limite e enquadramento |
| R2 | A margem bruta por estação sustenta a operação, incluindo a instalação em campo | Planilha de custos com cotações | Margem positiva por estação instalada |
| R3 | Prefeituras aceitam pagar assinatura anual de manutenção além da implantação | Entrevista com a Defesa Civil e a Prefeitura | Ao menos um órgão declara disposição e faixa de valor |
| R4 | Empresas pagariam por estação própria | 3 a 5 conversas com empresas em margem de rio | Ao menos uma disposição de pagar, com valor |
| R5 | A assinatura dos anos seguintes cabe na dispensa ou tem rito de contratação viável | Consulta ao setor de compras | Resposta formal |
| R6 | Há financiadores de impacto dispostos a custear sensores | Mapeamento de programas e editais | Ao menos um programa elegível identificado |
| R7 | A Defesa Civil valoriza o mapa com pontos de apoio e rotas a ponto de justificar a assinatura anual | Entrevista com o órgão, mostrando o mapa | Declaração do que o órgão pagaria e por quê |

---

## Referências

- [Effecti: limites de dispensa de licitação em 2026 (Decreto 12.807/2025)](https://effecti.com.br/decreto-12807-de-2025/)
- [Lei nº 14.133/2021 (Nova Lei de Licitações), art. 75](https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2021/lei/l14133.htm)
- [Revista Pesquisa FAPESP: E-Noé, 2023](https://revistapesquisa.fapesp.br/dispositivo-emite-em-tempo-real-alertas-contra-enchentes/)
- [NSC Total: radar de nível em Joinville](https://www.nsctotal.com.br/?p=2560512)
- [Portal de Prefeitura: Olinda lança sistema de alerta contra enchente](https://portaldeprefeitura.com.br/regiao-metropolitana/olinda/prefeitura-de-olinda-lanca-sistema-de-alerta-contra-enchente/599671/)
- [O Imparcial: ANA lança aplicativo gratuito com dados de rios, 2019](https://oimparcial.com.br/cidades/2019/04/ana-lanca-aplicativo-gratuito-com-dados-de-rios-e-chuvas-em-todo-o-brasil/)
