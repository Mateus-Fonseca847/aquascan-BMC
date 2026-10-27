# Resultados de validação

Registro consolidado dos testes de **todas as frentes** do projeto. Cada frente técnica mantém seu registro detalhado no próprio repositório; aqui fica o resumo para a banca.

## Resumo

| Frente | Teste | Data | Resultado |
|---|---|---|---|
| Firmware | Compilação com PlatformIO | 30/09/2026 | Aprovado |
| Firmware | Simulação no Wokwi: OLED, LED e pulsos | 30/09/2026 | Aprovado |
| Firmware | Cálculo de vazão em toda a faixa do potenciômetro | | Pendente |
| Firmware | Calibração do sensor físico | | Pendente |
| Sensor de nível | Leitura em bancada | | Pendente |
| App | Fluxo completo com o simulador | | Pendente |
| Usuários | Entrevistas com moradores | | Pendente |

## Firmware

Detalhes completos em [docs/validacao.md do firmware](https://github.com/CaiqueRV/Monitoramento-Fluxo-de--gua-ESP32/blob/main/docs/validacao.md).

**Compilação (30/09/2026):** aprovada em 15,86 s. O firmware usa 6,9% da RAM e 24,1% da Flash, deixando espaço para o sensor de nível e o Wi-Fi.

**Simulação (30/09/2026):** aprovada. Os valores exibidos conferem com o cálculo esperado:

| Pulsos em 1 s | Vazão esperada (f ÷ 7,5) | Vazão exibida |
|---|---|---|
| 55 | 7,33 L/min | 7,33 L/min |
| 73 | 9,73 L/min | 9,73 L/min |

Dois problemas foram encontrados e corrigidos durante o teste: a quebra de linha do Monitor Serial e fios do circuito passando sobre o display.

## Sensor de nível

[PREENCHER] Sugestão de teste em bancada: fixar o sensor acima de um balde, medir a distância com régua em 5 alturas de água diferentes e comparar com a leitura do sensor. Registrar o erro de cada medida.

## Aplicativo

[PREENCHER]

