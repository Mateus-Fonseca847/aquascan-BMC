# Business Model Canvas · 2. Proposta de Valor

## Introdução

O AquaScan é um sistema de monitoramento de rios que mede o nível da água com sensores de baixo custo, instalados em conjunto com o cliente, e comunica o risco de transbordamento em porcentagem, cor e texto, com tempo estimado, por meio de um aplicativo. Este documento descreve o bloco **Proposta de Valor** do Business Model Canvas: que valor o AquaScan entrega a cada cliente, que necessidades atende e **o que o diferencia** das alternativas que o cliente já tem.

O texto parte da comparação com os concorrentes (bloco Concorrentes) para chegar aos diferenciais, e é honesto sobre onde o AquaScan **não** leva vantagem. Quem são os clientes está em Segmento de Mercado; como o valor chega até eles, em Canais; como é mantido, em Relacionamento com Clientes.

**Legenda das evidências:** **Verificado** (fonte pública ou repositório do projeto, em Referências) · **Vivência** (observação dos integrantes, moradores de Petrópolis, RJ, que viveram enchentes) · **Hipótese** (a validar, ver seção 9). Funcionalidades **previstas** ou **em definição** não existem até serem implementadas e validadas.

---

## 1. Visão geral

**A proposta em uma frase.** O AquaScan ajuda a Defesa Civil, a Prefeitura e a população de áreas de risco a saber, em segundos e antes da cheia, quão perto do transbordamento está o rio da sua rua, por meio de sensores de baixo custo instalados em conjunto com o órgão e de um aplicativo que traduz cada leitura em porcentagem, cor e texto, com tempo estimado e o caminho até o ponto de apoio, **com custo de entrada reduzido, o conjunto mais amplo de medições por rio entre os concorrentes analisados, calibração feita com a Defesa Civil e um sistema rigoroso contra alarme falso**.

| Segmento | Resultado que entregamos | Por meio de | Diferencial central |
|---|---|---|---|
| Defesa Civil e Prefeitura (compra) | Mais pontos de medição por rio, com dado já traduzido para a população e histórico por evento | Estação instalada e calibrada em conjunto, plataforma, aplicativo, relatórios e operação | Custo de entrada reduzido e instalação nos pontos que o órgão escolhe |
| População de áreas de risco (gratuito) | Entender o risco do rio perto de casa e saber para onde ir | Aplicativo com mapa, estado do rio, previsão, pontos de apoio e alertas | Aviso em linguagem de decisão, sem alarme falso |
| Empresas com ativo em margem de rio (hipótese) | Ponto de medição no próprio ativo, com relatório e alerta | Estação dedicada com assinatura opcional | Medição exata no local, onde a rede pública não chega |

---

## 2. Perguntas-chave

| Pergunta | Resposta |
|---|---|
| Que valor entregamos? | Informação de risco **local, contínua e compreensível**: o nível do rio no ponto que importa, em porcentagem do transbordamento, cor e texto, com tempo estimado até o nível crítico |
| Que problema ajudamos a resolver? | Poucos pontos de medição por rio e dado técnico difícil de usar na hora de decidir; o morador recebe o aviso em metros, gráficos ou estágios, sem saber o que fazer (**vivência**; comparação com prints pendente) |
| Que necessidades satisfazemos? | Do órgão: ampliar a medição com baixo custo e comunicar melhor. Do morador: saber o risco, a evolução e para onde ir. Da empresa: proteger o ativo e ter evidência do risco |
| Que pacotes oferecemos? | Estação instalada e calibrada; plataforma de dados; aplicativo gratuito ao morador; relatórios, vistorias e plantão (seção 4) |
| O que nos diferencia? | Medição local a baixo custo; **conjunto amplo de medições e métricas por rio**; aviso traduzido para decisão; **rotas que evitam as áreas com enchente**; **pontos de apoio com todas as informações**; **mapa que funciona sem internet**; confiança no dado e no alerta; calibração conjunta com a Defesa Civil (seção 6) |

---

## 3. Necessidades e valor por segmento

### 3.1 Defesa Civil e Prefeitura

| Necessidade (dor ou ganho esperado) | Como o AquaScan atende |
|---|---|
| Poucos pontos de medição por rio (**hipótese**) | Estações de baixo custo instaladas nos pontos que o órgão indica, ampliando a rede com orçamento reduzido |
| Dado técnico que a população não usa | Estado do rio em porcentagem, cor e texto, com tempo estimado, entregue direto ao morador pelo aplicativo |
| Credibilidade do alerta; risco de alarme falso | Limiares validados com o órgão, filtro de leituras, controle de oscilação e revisão após cada evento |
| Evidência para prestar contas e planejar | Histórico com gráficos e eventos por rio, e o conjunto de medições (nível, tendência, tempo estimado, estatística, eventos, qualidade do dado e diagnóstico da estação); relatórios periódicos |
| Divulgar pontos de apoio e rotas | Lista do órgão integrada ao mapa, com telefone, capacidade e rota até o local |
| Contratar dentro de um limite de valor | Pacote de entrada pensado para caber na faixa de dispensa de licitação (Fonte de Renda e Lucro, seção 4) |
| Não perder o controle da comunicação | O AquaScan complementa os canais oficiais e nunca emite alerta em nome do órgão |

### 3.2 População de áreas de risco

| Necessidade | Como o AquaScan atende |
|---|---|
| Saber se o rio perto de casa está perigoso agora | Mapa com os rios monitorados e o estado de cada um, atualizado a cada minuto |
| Entender sem jargão | Porcentagem do transbordamento, cor, ícone e texto; fonte mínima de 16 px e contraste AA |
| Saber quanto tempo resta | Tempo estimado até o nível crítico, apresentado como estimativa, com margem de incerteza |
| Saber para onde ir sem entrar em área alagada | Pontos de apoio da Defesa Civil com telefone, capacidade e rota; locais salvos (casa e trabalho); rota que evita as áreas atingidas pela enchente |
| Continuar usando o aplicativo se a internet cair | Mapa, pontos de apoio e rotas no aparelho (**em desenvolvimento**); últimos dados marcados com data e hora |
| Acompanhar a evolução do rio | Histórico com gráficos de nível, taxa de subida e previsão contra valor real |
| Ser avisado sem excesso de aviso | Notificação só de piora na cidade do usuário, sem repetir quando o nível oscila perto do limite |
| Usar sem barreira e com privacidade | Modo visitante sem cadastro; dados mínimos; exclusão de conta e dados pelo usuário |

### 3.3 Empresas com ativo dependente de rio (hipótese)

| Necessidade | Como o AquaScan atende |
|---|---|
| Medição exata no ponto do ativo | Estação instalada no local, com alerta e leitura contínua |
| Evidência do risco para decisão e seguro | Histórico e relatório periódico do ponto |
| Atendimento previsível | Contrato com regime de atendimento definido e vistorias periódicas |

---

## 4. O que entregamos

| Entrega | O que inclui | Situação |
|---|---|---|
| Estação de campo | Sensor de nível, controlador, comunicação celular, energia, caixa vedada e fixação; instalada e calibrada em conjunto com o cliente | Em desenvolvimento; protótipo testado em maquete |
| Plataforma de dados | API, banco e o conjunto de medições e métricas (seção 6.1): nível, porcentagem, estado, tendência, tempo estimado, estatística, eventos, histórico, qualidade do dado e diagnóstico | Núcleo em uso; demais métricas definidas (Atividades-Chave, seção 3.1) |
| Aplicativo | Mapa dos rios, estado em cor e texto, **histórico com gráficos**, previsão de chuva, **pontos de apoio com telefone, capacidade e rota**, **rotas que evitam as áreas com enchente**, **funcionamento sem internet**, cadastro, modo visitante e notificações | Mapa, estado, previsão e pontos de apoio em uso; gráficos, rotas, modo sem internet e notificações em desenvolvimento (**detalhes técnicos do mapa em definição**) |
| Relatórios e histórico | Relatório periódico, revisão pós-evento e histórico por rio | Previsto |
| Operação do serviço | Vistorias preventivas, manutenção, plantão em chuva e suporte (Relacionamento com Clientes, seção 6) | Previsto |

---

## 5. Comparação com os concorrentes

Os concorrentes foram analisados no bloco Concorrentes. Aqui eles são agrupados pelo que oferecem:
- **Rede e alertas oficiais** (INEA, Defesa Civil, Cemaden, ANA): gratuitos, institucionais e de grande alcance; medem chuva e nível em redes estaduais e nacionais, e avisam por SMS, sirene e cell broadcast.
- **Soluções vendidas a municípios** (E-Noé, Ih, Alagou, radar de Joinville): sensores de nível instalados em cidades reais; custo alto ou replicabilidade desconhecida.
- **Plataformas globais** (Google FloodHub, Waze): alcance enorme e gratuito; dependem da cobertura do modelo ou do lançamento de alertas pela Defesa Civil.
- **Substitutos** (previsão do tempo, notícias, rede de vizinhos): conhecidos, mas sem medição contínua do rio.

| Critério | AquaScan | Melhor alternativa | Leitura |
|---|---|---|---|
| Medição do nível no rio do cliente | Sensor nos pontos escolhidos pelo órgão (em desenvolvimento) | Rede do INEA e da ANA; radar de Joinville | **Vantagem em cobertura local** |
| **Conjunto de medições e métricas por rio** | Distância, nível em centímetros e em porcentagem, metros restantes, taxas de subida e descida em quatro janelas, aceleração, tempo estimado, índice de risco, estatística, eventos, qualidade do dado, diagnóstico da estação, vazão (onde houver equipamento) e clima | ANA (nível e vazão); INEA (nível e chuva); E-Noé (nível e previsão) | **Vantagem**: nenhum concorrente analisado comprova publicamente um conjunto equivalente |
| Custo de entrada para o município | Cerca de R$ 3,2 mil de custo por estação instalada e preço pretendido de cerca de R$ 8 mil por estação no cenário de dispensa (premissas, a confirmar) | E-Noé, cerca de R$ 15 mil por conjunto; radar, cerca de R$ 138 mil; serviços públicos, gratuitos | **Vantagem sobre as soluções vendidas**, se o escopo for equivalente (hipótese PV1); os serviços gratuitos não medem cada rio |
| Linguagem para o morador | Porcentagem do transbordamento, cor e texto | INEA com estágios; Defesa Civil em metros; ANA em gráficos | **Vantagem provável**, ainda não testada (hipótese PV2) |
| Tempo estimado até o nível crítico | Por tendência (regressão), com margem de incerteza | E-Noé, por inteligência artificial; FloodHub, previsão de cheia | Paridade; o AquaScan destaca a transparência da estimativa |
| Histórico e gráficos | **Requisito básico do aplicativo**: histórico com gráficos de nível, taxa de subida e previsão contra valor real, ao lado do estado e do tempo estimado | ANA, com gráficos | **Paridade**, com a vantagem de reunir gráfico, risco, tempo e rota no mesmo aplicativo |
| Pontos de apoio no mapa | Todos os pontos da Defesa Civil com telefone, capacidade e rota até o local; ocupação, quando o órgão a informar | Defesa Civil mantém a lista; recurso não confirmado nos demais | **Vantagem**: nenhum concorrente analisado comprova esse recurso |
| Rota que evita as áreas com enchente | **Integrada** ao aplicativo: as áreas atingidas são bloqueadas no cálculo; indicativa, com margem de erro (detalhes técnicos em definição) | Waze, com área alagada informada pela Defesa Civil | **Vantagem**: o bloqueio parte do dado contínuo do rio, e não de lançamento manual |
| Funciona sem internet | Mapa, pontos de apoio e rotas no aparelho, em desenvolvimento; últimos dados com data e hora | Não confirmado em nenhum concorrente | **Possível vantagem** |
| Qualidade do dado e diagnóstico do sensor | Mostrados ao usuário e ao órgão | Não confirmado em nenhum concorrente | **Possível vantagem** |
| Instalação, manutenção e plantão no contrato | Incluídos no serviço | Não confirmado nas soluções acadêmicas e públicas | **Possível vantagem** |
| Alcance de massa | Aplicativo gratuito; depende da divulgação do órgão | SMS, sirene, cell broadcast, FloodHub e Waze | Complementar: o AquaScan não substitui esses canais |
| Gratuito ao morador | Sim | Todos | Paridade |

A ausência de um recurso na tabela significa **não confirmado** nos concorrentes, e não que não exista (bloco Concorrentes, seção 5).

---

## 6. Diferenciais

Ordenados pela força de defesa: o que o concorrente teria mais dificuldade de copiar, e o que o cliente mais valoriza. Os quatro primeiros formam o **núcleo da proposta**. Onde se lê "nenhum concorrente analisado comprova", a ausência é de **comprovação pública**, e não prova de que o recurso não exista (Concorrentes, seção 5).

| # | Diferencial | Contra quem | Por que importa ao cliente | Prova | Força |
|---|---|---|---|---|---|
| 1 | **Medição local a baixo custo, com instalação conjunta nos pontos que o órgão escolhe** | E-Noé e radar (custo); rede pública (cobertura por rio) | Mais pontos de medição com orçamento reduzido, nos pontos que o órgão considera críticos | Planilha de custos por estação com cotações; piloto | Alta, se o custo se confirmar |
| 2 | **Conjunto amplo de medições e métricas por rio** (seção 6.1) | ANA, INEA e E-Noé, que não comprovam publicamente um conjunto equivalente | O órgão tem dado para decidir e prestar contas, e o morador recebe o essencial já interpretado | Tela do rio com as métricas; relatório do piloto | Média a alta |
| 3 | **Aviso traduzido para decisão: porcentagem do transbordamento, cor, texto e tempo estimado** | Metros (Defesa Civil), gráficos (ANA), estágios (INEA) | O morador entende e age em segundos | Teste com 10 a 15 moradores | Média: cada elemento existe em algum concorrente; a combinação é rara |
| 4 | **Rotas que evitam as áreas com enchente** | Waze (área alagada informada pelo órgão), navegação comum | Orienta o morador a sair sem passar por onde o rio já alagou, com menos exposição ao risco | Teste de rotas com cenários de cheia; validação com a Defesa Civil | Média a alta, a depender da validação do mapeamento nível × ruas e da margem de erro |
| 5 | **Pontos de apoio com todas as informações no mapa**: telefone, capacidade, rota até o local e, quando o órgão informar, ocupação | Informação dispersa em vários canais | Quem está em risco sabe aonde ir, como ligar e se há vaga | Teste de uso; lista da Defesa Civil integrada | Média |
| 6 | **Mapa que funciona sem internet** (em desenvolvimento) | Aplicativos de mapa e de alerta que exigem conexão | Quem ficou sem internet por causa da tempestade ainda vê o mapa, os pontos de apoio e as rotas | Teste em modo sem conexão | Média |
| 7 | **Confiança no dado e no alerta: sistema rigoroso contra alarme falso** | Concorrentes sem esse recurso confirmado | Alarme falso destrói a confiança e leva o morador a desligar as notificações | Taxa de alertas sem consequência real; registro de falhas | Média a alta, comprovável após o piloto |
| 8 | **Calibração e validação conjunta com a Defesa Civil, com revisão após cada evento** | Soluções prontas e sem co-criação | O órgão valida os limiares e passa a confiar no sistema | Piloto; atas de validação | Média a alta |
| 9 | **Complementar ao alerta oficial: nunca substitui nem contradiz o órgão** | Soluções que disputam a comunicação com a Defesa Civil | Reduz a resistência do órgão e o risco de mensagens conflitantes | Cláusula contratual; fonte e horário em cada leitura | Média |
| 10 | **Serviço completo em contrato: instalação, manutenção, plantão em chuva e relatórios** | Soluções que entregam só equipamento ou só dado | O órgão não precisa montar equipe técnica | Contrato e primeiro ano de operação | Média |
| 11 | **Transparência e privacidade: código público, dados mínimos, exclusão de conta e modo visitante** | Plataformas que coletam mais dados | Auditável e sem barreira de entrada | Repositório público; política de privacidade | Baixa a média |
| 12 | **Dado contínuo do rio como gatilho para rotas e avisos em plataformas de navegação** | Alertas lançados manualmente pelo órgão | Resposta mais rápida na subida do rio | Piloto e conversa com a Defesa Civil | Baixa; futuro e hipótese |

### 6.1 O conjunto de medições e métricas

O AquaScan mede em campo uma grandeza, a distância até a água, e **calcula dela e dos dados externos um conjunto de métricas que os concorrentes analisados não comprovam oferecer juntas**. Cada métrica responde a uma pergunta de quem decide:

| Pergunta | Medição ou métrica |
|---|---|
| Quão alto está o rio? | Distância até a água; nível em centímetros; porcentagem da cota de transbordamento; metros restantes até transbordar |
| O rio está subindo ou descendo, e com que velocidade? | Taxas de subida e descida em janelas de 5, 10, 30 e 60 minutos; aceleração da subida |
| Quanto tempo resta? | Tempo estimado até o nível crítico e até o transbordamento, com margem de incerteza |
| Qual o risco agora? | Estado em cor, ícone e texto; índice de risco de 0 a 100 |
| Como este evento se compara aos anteriores? | Estatística do período (máximo, mínimo, média, mediana, desvio padrão, amplitude e percentis); início da subida, pico, recessão, fim, duração e nível máximo de cada evento |
| O dado e a estação são confiáveis? | Leituras impossíveis, saltos bruscos, sensor sem resposta e dados ausentes; diagnóstico de falha, obstrução e perda de comunicação |
| E o que vem de chuva? | Previsão de chuva de 7 dias, com classificação de perigo por cor |
| Qual o volume de água? | Vazão e volume, onde houver equipamento adequado (em rio aberto exige equipamento próprio) |
| Como o rio evoluiu? | Histórico com gráficos de nível, taxa de subida e previsão contra valor real |

Os detalhes e a situação de cada métrica estão em Atividades-Chave, seção 3.1.

**Credibilidade de origem (apoio, não diferencial de produto).** A equipe é de Petrópolis e viveu as enchentes (**vivência**), o que dá conhecimento direto do território e confiança para abrir conversa com o órgão.

---

## 7. Onde o AquaScan não é diferente

Para não prometer o que outros já fazem melhor:
- **Previsão por inteligência artificial:** o E-Noé a oferece; o AquaScan usa tendência simples, com poucos dados, e se apresenta como estimativa.
- **Gráficos de histórico, por si só:** a ANA também os oferece. No AquaScan são requisito básico e o diferencial é reuni-los, no mesmo aplicativo, com o estado, o tempo estimado, as rotas e os pontos de apoio.
- **Alerta oficial e alcance de massa:** SMS, sirene e cell broadcast da Defesa Civil alcançam quem não usa aplicativo; o AquaScan complementa esses canais e não os substitui.
- **Informação de nível por si só:** o nível do rio já é publicado por redes oficiais onde elas têm estação.

O argumento do AquaScan não é ser o único a medir o rio. É **medir onde a rede não mede, custar pouco, medir mais do que o nível e entregar o dado numa forma que o morador usa**, com rota, ponto de apoio e acesso sem internet.

**Tempo de mercado.** O AquaScan não tem o tempo de mercado das instituições e empresas já estabelecidas. É uma startup, e traz em troca agilidade, custo baixo e foco no problema local.

---

## 8. Promessas e limites

| O AquaScan promete | O AquaScan não promete |
|---|---|
| Informação contínua do nível nos pontos instalados, com fonte e horário | Cobertura de todos os rios da cidade |
| Estimativa de tempo, apresentada como estimativa | Previsão exata do momento do transbordamento |
| Pontos de apoio e rotas indicativas, com data da última atualização | Rota "segura": a rota reduz a exposição, tem margem de erro e não substitui a orientação da Defesa Civil |
| Complemento ao alerta oficial | Substituir sirene, SMS ou a decisão da Defesa Civil |
| Aviso só quando há piora, com controle contra alarme falso | Ausência total de falha: sensores em rio sofrem danos e perdas |
| Mapa, pontos de apoio e rotas disponíveis sem internet, com os últimos dados marcados com data e hora | Leituras novas e notificações sem conexão |
| Rota que evita as áreas atingidas, com margem de erro | Rota livre de risco |

---

## 9. Hipóteses a validar

| Código | Hipótese | Como testar | Critério |
|---|---|---|---|
| PV1 | O AquaScan entrega estação instalada e serviço por preço inferior ao do E-Noé, em escopo equivalente | Levantar o escopo do conjunto do E-Noé e comparar com o pacote do AquaScan; cotação dos itens de campo | Preço por estação inferior, com escopo equivalente (Concorrentes, H3) |
| PV2 | O morador decide com mais rapidez e acerto com porcentagem, cor e texto do que com metros ou gráficos | Teste com 10 a 15 moradores comparando telas | Taxa de acerto maior que a das telas de comparação (Concorrentes, H2) |
| PV3 | O tempo estimado é útil e conservador | Comparar previsão e valor real em eventos e simulações | Erro medido e ausência de estimativas otimistas demais (Concorrentes, H7) |
| PV4 | A rede pública não cobre com detalhe os rios do piloto | Consultar o inventário do INEA e a cobertura do FloodHub | Lista de rios cobertos e frequência (Concorrentes, H1 e H8) |
| PV5 | A Defesa Civil valoriza a calibração conjunta e a revisão pós-evento | Entrevista com o órgão, apresentando o processo | Declaração do que valoriza e do que pagaria |
| PV6 | O sistema contra alarme falso mantém a taxa de alertas sem consequência real dentro da meta | Piloto com registro de alertas e revisão com o órgão | Taxa abaixo da meta definida com a Defesa Civil |
| PV7 | O sensor de baixo custo mantém precisão aceitável em campo | Comparar leituras com referência, em campo (Concorrentes, H6) | Erro de nível aceitável pelo órgão |
| PV8 | Pontos de apoio e rotas aumentam o uso do aplicativo e o valor percebido pelo órgão | Medir uso das telas e entrevistar o órgão (Fonte de Renda e Lucro, R7) | Uso medido e valor declarado pelo órgão |
| PV9 | O órgão aceita o AquaScan como complemento e não vê conflito com os alertas oficiais | Entrevista e minuta de cláusula | Aceite e cláusula acordada |
| PV10 | O órgão e os moradores usam e valorizam o conjunto de métricas além do estado do rio | Entrevista com o órgão e teste de uso com moradores, apresentando as telas | Métricas citadas como úteis e usadas na decisão |
| PV11 | A rota que evita as áreas com enchente tem margem de erro aceitável | Testar rotas em cenários de cheia e validar com a Defesa Civil o mapeamento de áreas atingidas | Rotas que não passam por áreas atingidas nos cenários validados |
| PV12 | O mapa, os pontos de apoio e as rotas funcionam sem internet | Teste em modo sem conexão, com dados já carregados | Funções disponíveis sem rede, com os últimos dados marcados com data e hora |
| PV13 | A Defesa Civil informa a ocupação dos pontos de apoio de forma atualizada | Combinar com o órgão o formato e a frequência de atualização | Atualização combinada e data da última atualização visível no aplicativo |

---

## Referências

- Blocos do BMC do AquaScan: Concorrentes (seções 3, 5, 6 e 7, com as fontes de cada concorrente), Segmento de Mercado, Fonte de Renda e Lucro (seção 4 e hipótese R7), Estrutura de Custos (seções 3.1 e 4), Relacionamento com Clientes (seções 4 e 6), Atividades-Chave (seção 3.1).
- Repositório aquascan-app (consultado em 16/10/2026): `README.md`, `docs/requisitos.md` (RF03 a RF11, RNF01, RNF02, RNF05) e `docs/privacidade.md`.
- Fontes públicas sobre os concorrentes (INEA, E-Noé, Ih, Alagou, Joinville, Cemaden, ANA, Google FloodHub, Waze): ver Referências do bloco Concorrentes.
