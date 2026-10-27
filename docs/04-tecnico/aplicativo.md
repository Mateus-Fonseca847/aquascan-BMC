# Aplicativo

> Resumo da stack e das telas. O código ficará no repositório [**aquascan-app**](https://github.com/Mateus-Fonseca847/aquascan-app). As justificativas de cada escolha estão na [decisão 001](../decisoes/001-stack-do-aplicativo.md).

## Stack

| Camada | Tecnologia |
|---|---|
| Linguagem | TypeScript |
| Aplicativo | React Native com Expo (Expo Router) |
| Mapa | react-native-maps com estilo personalizado |
| Notificações | Expo Notifications |
| API | Node.js com Fastify e Zod |
| Banco de dados | PostgreSQL com PostGIS, acessado pelo Prisma |
| Ambiente local | Docker Compose |
| Organização | Monorepo com pnpm workspaces |
| Serviços externos | Open-Meteo (tempo), ViaCEP (endereço), OpenStreetMap (ruas) |

## Telas

| Tela | Conteúdo |
|---|---|
| Cadastro e login | Nome, e-mail, número de contato e CEP |
| Mapa (início) | Rios coloridos pelo estado, pesquisa por rua |
| Detalhe do rio | Nível em %, estado, histórico e estimativa |
| Previsão do tempo | Próximos 7 dias com cores de perigo |
| Pontos de apoio | Lista e mapa, capacidade, contato e "Como chegar" |
| Perfil | Dados do usuário e preferências de alerta |

## Estrutura planejada do repositório

```
aquascan-app/
├── apps/
│   ├── mobile/          ← React Native + Expo
│   └── api/             ← Node.js + Fastify + Prisma
├── packages/
│   └── shared/          ← regras de nível e estado usadas pelo app e pela API
├── tools/
│   └── simulador/       ← envia leituras falsas para testar sem a estação física
└── docs/
```

O simulador permite desenvolver e demonstrar o app antes de existir uma estação no rio, seguindo a mesma ideia do potenciômetro no Wokwi.

## Privacidade (LGPD)

O cadastro coleta nome, e-mail, telefone e CEP. Cada dado precisa de uma finalidade clara: o CEP define a região dos alertas, o telefone serve para contato em emergência [PREENCHER: confirmar se será usado]. O app deve pedir consentimento no cadastro e permitir excluir a conta.
