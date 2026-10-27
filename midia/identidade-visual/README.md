# Identidade visual

Definida no mapa mental: **azul e branco**, **acessível**, **interface amigável** e a **capivara como mascote**. As decisões abaixo estão materializadas no protótipo de telas em `identidade-visual-acquascan.pdf`, que é a referência visual do projeto.

## Nome da marca

> **[DECIDIR — registrar como ADR]** O protótipo escreve **AquaScan**, sem o "c". Os repositórios e a documentação escrevem **AcquaScan**. Refazer logo e telas custa mais do que renomear repositórios e documentos, mas a escolha é da equipe. Decidir antes de produzir banner e pitch, e aplicar em todos os materiais de uma vez.

## Tagline

**Mais informação. Mais tranquilidade.**

Usada na tela de abertura. Serve também para banner e pitch.

## Paleta

> As cores abaixo são a proposta original. Conferir contra o arquivo de origem do protótipo e corrigir os valores se divergirem.

| Uso | Cor | Hex | Contraste com branco |
|---|---|---|---|
| Azul principal | Botões, títulos, cabeçalho | `#0B5FA5` | 6,6 : 1 |
| Azul escuro | Textos e ícones | `#083D6B` | 11,1 : 1 |
| Azul claro | Fundos de cartões | `#E8F2FB` | Fundo (texto em azul escuro: 9,8 : 1) |
| Branco | Fundo principal | `#FFFFFF` | — |

### Estados da estação

São a única exceção à paleta azul e branca, porque precisam comunicar risco de imediato.

| Estado | Hex | Contraste com branco | Ícone | Quando aparece |
|---|---|---|---|---|
| Estável | `#1E7B34` | 5,3 : 1 | ✓ | Nível abaixo do limiar de atenção |
| Atenção | `#9A5B00` | 5,4 : 1 | ! | Nível em elevação, acima do limiar de atenção |
| Crítico | `#B3261E` | 6,5 : 1 | ▲ | Risco de transbordamento |
| Sem dados | [PREENCHER — cinza neutro, conferir contraste] | [PREENCHER] | — | Estação sem comunicação |

**"Sem dados" não é um estado cosmético.** Quando a estação para de enviar leitura, o app mostra a última comunicação e deixa explícito que não é possível estimar o trecho. Nunca exibir "Estável" na ausência de dado: silêncio de sensor não é sinal de segurança.

Todas as combinações definidas passam no nível AA das diretrizes WCAG (mínimo de 4,5 : 1 para texto).

## Tipografia

[PREENCHER: fonte escolhida no protótipo, com os pesos usados. Preferir uma fonte do Google Fonts, por disponibilidade no React Native e boa leitura em tela pequena.]

## Mascote: capivara

A capivara vive na beira de rios e lagos, o que conecta o mascote ao tema e traz um tom amigável. [PREENCHER: nome do mascote]

**Onde aparece:**

- tela de boas-vindas e fluxo de criação de conta;
- estados vazios e de permissão negada (localização e notificações desativadas);
- telas de previsão do tempo, com uma variação por condição — chuvoso, instável, ensolarado, nublado e tempestuoso;
- materiais do evento.

**Onde não aparece:** em alerta crítico, em tela de risco de transbordamento e em rota de evacuação. Numa emergência a mensagem é direta e séria, sem ilustração.

## Tom de voz

O protótipo estabelece um padrão consistente que vale registrar, porque pitch, banner e textos futuros precisam soar igual.

- **Segunda pessoa, acolhedor:** "Que bom ter você aqui", "Boas-vindas", "Vamos ajudar você".
- **Erro sem culpa:** o app explica o que aconteceu e oferece a próxima ação. "Não foi possível conectar. O mapa e as rotas salvos continuam disponíveis sem internet."
- **Em alerta, direto e acionável:** estado, número, prazo estimado e o que fazer. "Rio Quitandinha em 86%. Pode transbordar em 30 min no ritmo atual. Procure um local seguro agora."
- **Sem alarmismo fora de alerta.** Nada de linguagem de emergência em tela comum.

## Padrões de interface

### Navegação

Quatro abas fixas: **Mapa · Apoio · Tempo · Conta**.

### Aviso de responsabilidade

Padrão obrigatório em toda tela que exiba estimativa, rota ou alerta. O app **não substitui** o alerta oficial da Defesa Civil, e isso aparece escrito, não subentendido:

- em previsão: "Estimativa demonstrativa. Consulte os comunicados oficiais da Defesa Civil."
- em rota: "Rota ilustrativa. Não atravesse vias alagadas; confirme o apoio com a Defesa Civil."
- em lista de alertas: "Estes alertas não substituem a Defesa Civil."

O contato **199 — Defesa Civil** aparece em todo ponto de apoio e em toda tela de risco.

### Modo offline

Decisão estruturante do produto: numa enchente a rede cai, e é exatamente quando o app precisa funcionar. O protótipo trata isso como primeira classe, não como erro.

- Indicador permanente com o horário do último dado: "Sem internet — dados de 18:02".
- Download prévio de mapa, rotas e contatos, com tamanho declarado por item e opção de baixar só no Wi-Fi.
- Rota salva navegável sem rede, incluindo recálculo quando o usuário sai do caminho.
- Perda de GPS tratada com fallback: direção em linha reta até o apoio.

### Funciona sem conta

Mapa, previsão e pontos de apoio funcionam sem cadastro. A conta serve para alertas e preferências, e o convite para criá-la nunca bloqueia o acesso à informação de risco.

## Acessibilidade

- **Nunca usar só a cor** para indicar o estado. Pessoas com daltonismo podem não distinguir verde de vermelho. Sempre cor, ícone e texto juntos: `▲ Crítico · 87%`.
- Textos com no mínimo 16 px no app e suporte ao aumento de fonte do celular.
- Botões com área de toque de pelo menos 44 × 44 px.
- Imagens e ícones com descrição para leitores de tela.
- Mensagens de erro de formulário descrevem o problema e a correção, não apenas marcam o campo em vermelho.

## Privacidade na interface

A tela de privacidade declara a base legal e os dados coletados: nome, e-mail e cidade, usados para enviar alertas. O usuário pode baixar os próprios dados e excluir a conta, com confirmação por senha. Manter alinhado com `docs/privacidade.md`.

## Arquivos

| Arquivo | Situação |
|---|---|
| `identidade-visual-acquascan.pdf` | Protótipo de telas — referência visual atual |
| Arquivo de origem do protótipo (Figma ou equivalente) | [PREENCHER: link] |
| `logo.svg` | [PREENCHER] |
| `logo.png` (fundo transparente) | [PREENCHER] |
| `mascote-capivara.svg` | [PREENCHER] |
| `tipografia.md` | [PREENCHER] |

Exportar logo e mascote como arquivos próprios é pré-requisito para o banner do evento — recortar do PDF perde qualidade na impressão.