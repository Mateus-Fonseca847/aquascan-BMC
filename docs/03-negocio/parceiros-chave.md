# Business Model Canvas · 8. Parcerias-Chave

## Introdução

O AquaScan depende de terceiros para três coisas: **ter autorização e dado para operar** (poder público), **ter peças e serviços para funcionar** (fornecedores) e **ter conhecimento técnico e financiamento para crescer** (pesquisa e fomento). Este documento descreve um dos blocos do Business Model Canvas, as **Parcerias-Chave**: quem são os parceiros e fornecedores, o que cada um entrega e o que o AquaScan precisa para tê-los.

O texto trata só desse tema. As atividades e os recursos que dependem dos parceiros estão nos blocos Atividades-Chave e Recursos-Chave, e os custos de cada fornecimento, em Estrutura de Custos.

**Legenda das evidências:** **Verificado** (fonte pública ou repositório do projeto, em Referências) · **Vivência** (observação dos integrantes, moradores de Petrópolis, RJ) · **Hipótese** (a validar, ver seção 8). Nenhuma das parcerias abaixo está formalizada: todas são **parcerias a construir**, salvo indicação em contrário.

---

## 1. Visão geral

| Categoria | Parceiros | O que entregam | Criticidade |
|---|---|---|---|
| Poder público | Defesa Civil, Prefeitura de Petrópolis (Meio Ambiente, compras) | Pontos de instalação, autorização, cotas de transbordamento, lista de pontos de apoio, contratação | **Crítica** |
| Fornecedores de campo | Lojas e distribuidores de eletrônicos, importador de sensores, fornecedores de energia solar | Estações: sensor, controlador, bateria, painel, caixa e cabos | **Crítica** |
| Conectividade | Operadora móvel (chip de dados para IoT) | Envio das leituras do campo para a API | **Crítica** |
| Plataforma e dados | Hospedagem, lojas de aplicativos, serviço de notificações, fontes de clima e de mapas | Operar a API, o banco e o aplicativo; entregar o alerta ao celular | **Crítica** |
| Pesquisa e conhecimento técnico | Universidades e centros de pesquisa, com destaque ao LNCC, em Petrópolis | Validação hidrológica e técnica, calibração, apoio de estudantes | Alta |
| Dados públicos de rios e clima | ANA, INEA, Serviço Geológico do Brasil, Cemaden, INMET | Séries históricas, cotas e referências de campo | Alta |
| Serviços profissionais | Contabilidade, advocacia, corretora de seguros, prestadores de campo por demanda | Funcionamento legal e operacional da empresa | Alta |
| Comunidade | Associações de moradores, escolas, Comitê de Bacia | Validação dos pontos críticos e adesão da população | Média |
| Financiamento e ecossistema | SEBRAE e Supernova, FAPERJ, FINEP, aceleradoras | Capital, mentoria e acesso a clientes | Média |

---

## 2. Perguntas-chave

| Pergunta | Resposta |
|---|---|
| Quem são os parceiros-chave? | Defesa Civil e Prefeitura, que dão acesso, dado e contrato; fornecedores de sensor e de comunicação; universidades para validação |
| Quem são os fornecedores-chave? | Distribuidores de eletrônicos e importador de sensores, operadora móvel, provedor de hospedagem, lojas de aplicativos e serviço de notificações |
| Que recursos recebemos deles? | Autorização de instalação, cota de transbordamento, pontos de apoio, peças, chips de dados, hospedagem, dados meteorológicos e conhecimento técnico |
| Que atividades eles executam? | A Defesa Civil valida limiares e atualiza pontos de apoio; fornecedores abastecem as estações; a operadora transporta os dados; universidades validam os modelos |
| Que parceria não pode falhar? | Defesa Civil e Prefeitura. Sem autorização, cota e contrato, não há estação instalada nem receita (Recursos-Chave, seção 5) |

---

## 3. Poder público

**Defesa Civil e Prefeitura de Petrópolis** são cliente e parceiro ao mesmo tempo. Como parceiros entregam:
- **Pontos de instalação e autorização** para fixar a estação em ponte, muro ou margem;
- **Cota de transbordamento** e referências de campo de cada ponto, sem as quais o sistema não calcula a porcentagem;
- **Lista de pontos de apoio** (nome, localização, telefone e capacidade máxima), atualizada periodicamente;
- **Validação dos limiares** de atenção e crítico e participação na revisão após cada evento;
- **Divulgação do aplicativo** à população, nos canais do órgão (Relacionamento com Clientes, seção 3);
- **Integração ao plano de contingência municipal**, como sirenes e equipes de campo.

**Como formalizar:** termo de cooperação para o piloto, antes de qualquer contrato de compra; no contrato, cláusulas de acesso aos pontos, de atualização dos pontos de apoio e de divulgação do aplicativo (Estrutura de Custos, seção 3.5).

**Outras fontes públicas (acesso e termos a confirmar):**
- **ANA, INEA e Serviço Geológico do Brasil:** séries históricas de nível e de chuva, e mapeamento de áreas de risco para calibrar os limiares;
- **Cemaden e INMET:** dados de chuva e alertas, para contexto e para evitar duplicidade de aviso. A relação com o Cemaden pode ser de **complementaridade**, já que a rede dele mede chuva e o AquaScan mede o nível do rio (hipótese).

---

## 4. Pesquisa e conhecimento técnico

**Universidades e centros de pesquisa** entram como parceiros para validação, não para desenvolvimento do produto:
- **LNCC**, com sede em Petrópolis (**verificado**), é o parceiro mais próximo para modelagem computacional. Instituições de ensino da cidade e de universidades federais do estado, como UFRJ e UFF, são candidatas para hidrologia, hidráulica e estágio (**hipótese**; contato ainda não feito).
- **O que se busca:** validação hidrológica das cotas e dos limiares, revisão dos cálculos de nível, vazão e tendência, apoio de estudantes na instalação e na calibração, e acesso a laboratório para testes de bancada.
- **Limite honesto:** a série de dados do AquaScan ainda é curta. O relatório técnico do projeto não recomenda modelos estatísticos complexos nessa fase (Recursos-Chave, seção 4). Por isso a parceria acadêmica começa em **validação e calibração**, e não em aprendizado de máquina.

**Formalização:** acordo de cooperação técnica com cláusulas de propriedade intelectual, de uso dos dados e de crédito, definidas por advogado antes de qualquer compartilhamento.

---

## 5. Fornecedores

A cadeia depende de poucos fornecedores, e três deles têm risco de indisponibilidade ou de preço: sensor, módulo celular e operadora.

| Fornecimento | Fornecedores candidatos | Observação |
|---|---|---|
| Controlador e eletrônica geral | Curto Circuito, Usinainfo | Preço e disponibilidade verificados em lojas de varejo (Estrutura de Custos, seção 3.1) |
| Sensor de nível de campo | MaxBotix e Vega (referências de classe), importador ou distribuidor nacional a definir | **Fornecedor ainda não definido**; sensor de campo com importação é o maior item de custo da estação |
| Energia | Fornecedores de painel solar, controlador e bateria selada | Preço verificado para controlador e bateria; painel a cotar |
| Conectividade | Operadora móvel com plano de dados para IoT | Oferta da Vivo levantada; outras operadoras a cotar |
| Hospedagem da API e do banco | Provedor de nuvem ou de servidor virtual | Provedor ainda não escolhido; estimativa feita com base em um provedor de referência |
| Lojas de aplicativos | Apple e Google | Conta de desenvolvedor; aprovação das versões |
| Notificações push | Expo e, por trás dele, Apple e Google | A mensagem não leva dado pessoal (Relacionamento com Clientes, seção 4) |
| Dados de clima | Open-Meteo | O plano gratuito é só para uso não comercial; uso comercial exige plano pago |
| Dados e mapa do aplicativo | OpenStreetMap e provedor de mapa, **em definição** | Atribuição e licença ODbL a respeitar |

**Princípio de escolha:** dois fornecedores qualificados para cada item crítico (sensor, módulo celular, bateria), para não depender de um só. Os preços de cada fornecedor estão em Estrutura de Custos.

**Serviços profissionais (parceiros operacionais):**
- **Contador:** regime tributário, notas e obrigações;
- **Advogado:** contrato-modelo, limite de responsabilidade por falha de alerta, LGPD e propriedade intelectual;
- **Corretora de seguros:** seguro de responsabilidade civil e de equipamentos e, no cenário de contrato maior, seguro-garantia;
- **Prestadores de campo por demanda:** instalação e vistorias, com dois prestadores cadastrados para o caso de indisponibilidade na cheia (Estrutura de Custos, seção 3.2);
- **Gráfica:** cartazes, folhetos e placas com QR code.

---

## 6. Comunidade e organizações locais

- **Associações de moradores e escolas:** validam os pontos críticos de risco, participam dos simulados e levam o aplicativo à população (Relacionamento com Clientes, seção 3).
- **Comitê de Bacia (Comitê Piabanha):** reúne poder público, usuários da água e sociedade civil na bacia que inclui Petrópolis (**verificado** em notícia local). Serve como fórum de apresentação e de validação dos pontos de monitoramento (**hipótese**).

---

## 7. Financiamento e ecossistema

| Parceiro | Papel | Situação |
|---|---|---|
| SEBRAE e Supernova | Programa e evento em que o AquaScan se apresenta; mentoria e contato com clientes e investidores | Em andamento (competição em 20/10/2026) |
| FAPERJ (estadual) e FINEP (federal) | Fomento à inovação por editais | Programas e editais abertos a **levantar**; a elegibilidade de cada edital precisa ser conferida |
| Aceleradoras e fundos | Capital, mentoria e rede de clientes | **Hipótese**, para a fase de expansão |

Contratos de solução inovadora com o poder público (Marco Legal das Startups) são tratados como forma de contratação, não como parceria (Estrutura de Custos, seção 5).

---

## 8. Dependências, riscos e hipóteses

| Risco | Efeito | Mitigação |
|---|---|---|
| Defesa Civil ou Prefeitura não entrega cota, autorização ou lista de pontos de apoio | Estação não instalada ou aviso sem porcentagem | Termo de cooperação no piloto; pontos indicados pelo órgão; cláusulas contratuais |
| Dependência de um único fornecedor de sensor ou de módulo celular | Parada de produção e variação de preço e de câmbio | Dois fornecedores qualificados por item crítico; estoque de reposição |
| Mudança de termos de dados ou de plano de terceiros (clima, mapa, notificações) | Custo novo ou perda de função | Cache; aplicativo continua exibindo o nível medido sem a previsão; contrato de uso comercial onde exigido |
| Cobertura da operadora insuficiente em um ponto | Estação sem envio de dados | Teste de cobertura antes da instalação; segunda operadora |
| Propriedade intelectual e uso de dados em parcerias acadêmicas | Disputa sobre o que é de quem | Acordo de cooperação revisado por advogado |
| Parceria institucional depende de uma pessoa | Perda de apoio com a troca de gestão | Relação em mais de um nível do órgão |

**Hipóteses a validar** (código PC, de Parcerias)

| Código | Hipótese | Como testar | Critério |
|---|---|---|---|
| PC1 | A Defesa Civil assina termo de cooperação para o piloto e fornece cotas e pontos de apoio | Reunião com o órgão e minuta do termo | Termo assinado ou aceite formal, com lista de entregas |
| PC2 | Pelo menos uma universidade ou centro de pesquisa da região aceita validar os limiares e a calibração | Contato com o LNCC e com cursos de engenharia e geociências da região | Um responsável técnico identificado e escopo combinado |
| PC3 | Existem pelo menos dois fornecedores para o sensor de campo e para o módulo celular, com prazo e preço conhecidos | Cotação com dois fornecedores por item | Duas cotações com data e prazo de entrega |
| PC4 | A operadora tem cobertura IoT nos pontos candidatos e oferece plano adequado | Teste de campo e proposta comercial | Ao menos 95% dos envios entregues no teste (Estrutura de Custos, C4) |
| PC5 | O uso comercial do Open-Meteo tem custo e condições definidos | Pedido de proposta ao fornecedor | Condições por escrito (Estrutura de Custos, C5) |
| PC6 | ANA, INEA e Serviço Geológico do Brasil liberam séries e mapeamentos para uso no projeto | Solicitação formal de dados e consulta aos termos | Dados obtidos ou termos de uso confirmados |
| PC7 | Há edital aberto da FAPERJ ou da FINEP compatível com o AquaScan | Levantamento dos editais vigentes | Ao menos um edital elegível identificado |
| PC8 | Dois prestadores de campo aceitam atender por demanda, inclusive em chuva forte | Cotação e conversa com dois prestadores | Dois prestadores cadastrados com preço e disponibilidade (Estrutura de Custos, C17) |

---

## Referências

- Repositório aquascan-bmc, arquivo `parceiros-chave.md` (versão anterior, consultada em 16/10/2026).
- Blocos do BMC do AquaScan: Recursos-Chave (seções 3.5, 4 e 5), Estrutura de Custos (seções 3.1 a 3.3 e 5; hipóteses C4, C5 e C17), Relacionamento com Clientes (seções 3 e 4), Concorrentes (Cemaden e INMET).
- [LNCC: folder institucional 2026 (sede em Petrópolis)](https://www.gov.br/lncc/pt-br/centrais-de-conteudo/divulgacao-cientifica/folder-institucional-2026-pt.pdf)
- [Correio da Manhã: Comitê Piabanha e o licenciamento em Petrópolis (jul/2026)](https://www.correiodamanha.com.br/serrano/2026/07/299293-comite-piabanha-volta-a-pedir-suspensao-do-licenciamento-de-grandes-empreendimentos.html)
- [Comitê Piabanha](https://www.comitepiabanha.org.br/)
- [Open-Meteo: preços e termos](https://open-meteo.com/en/pricing)
- Fornecedores consultados para preços: ver Referências do bloco Estrutura de Custos.
