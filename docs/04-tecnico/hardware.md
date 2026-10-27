# Hardware e firmware

> Resumo para a banca e para quem não é da área técnica. A documentação completa, o código e a simulação estão no [repositório do firmware](https://github.com/CaiqueRV/Monitoramento-Fluxo-de--gua-ESP32).

## O que já funciona

O protótipo atual mede **quanta água passa por um cano**:

```
Água → Sensor YF-S201 → Pulsos elétricos → ESP32 → Vazão no display OLED + LED de alerta
```

A água gira uma pequena hélice dentro do sensor, e cada volta gera pulsos elétricos. O ESP32 conta os pulsos por segundo e converte em vazão: `vazão (L/min) = frequência (Hz) ÷ 7,5`. Se a vazão passar de 5 L/min, um LED acende.

Como o simulador Wokwi não tem o sensor YF-S201, o próprio ESP32 gera os pulsos, controlados por um potenciômetro que funciona como uma "torneira virtual". O programa não percebe a diferença entre os pulsos simulados e os reais.

| Componente | Função |
|---|---|
| ESP32 DevKit | Conta os pulsos, calcula e controla tudo |
| YF-S201 | Transforma o fluxo de água em pulsos |
| OLED SSD1306 | Mostra pulsos, frequência e vazão |
| LED + resistor 220 Ω | Alerta visual |

Resultados dos testes: [validação](../05-validacao/resultados.md).

## O que falta para monitorar um rio

O YF-S201 mede a água que passa **por dentro dele**, não a altura de um rio. Para o aplicativo mostrar o nível em %, a estação precisa de um **sensor de nível** ([decisão 002](../decisoes/002-sensor-de-nivel.md)).

## Roadmap do firmware

| Versão | Entrega | Situação |
|---|---|---|
| v0.1.0 | Medição de vazão, OLED, LED e simulação | Em validação |
| v0.2.0 | Modo de calibração | A fazer |
| v0.3.0 | Volume acumulado | A fazer |
| v0.4.0 | Sensor de nível | A fazer (prioridade) |
| v0.5.0 | Estimativa de tempo até o transbordamento | A fazer |
| v0.6.0 | Envio de dados via Wi-Fi para a API | A fazer (prioridade) |
| v1.0.0 | Montagem física completa | A fazer |

Para o app funcionar com dados reais, as versões **v0.4.0** e **v0.6.0** são o caminho crítico.
