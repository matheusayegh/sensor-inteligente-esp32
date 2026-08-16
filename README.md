[README_ESP32.md](https://github.com/user-attachments/files/31110347/README_ESP32.md)
# 🚦 Semáforo Inteligente para Segurança de Pedestres

Sistema ciberfísico simulado com ESP32, desenvolvido em C/C++ (Arduino Framework), que monitora a presença de pedestres em uma calçada/faixa e a distância de veículos se aproximando, sinalizando o nível de risco através de LEDs (semáforo) e buzzer.

> Projeto acadêmico da disciplina de Fundamentos de Sistemas Ciberfísicos.
> Desenvolvido em equipe por: Ali Amer, Arthur Brambilla, Matheus Sayegh e João Thiago.

## Como funciona

1. Um **sensor PIR** detecta a presença de um pedestre na calçada/faixa.
2. Um **sensor ultrassônico (HC-SR04)** mede a distância de um veículo se aproximando.
3. O sistema cruza as duas leituras e decide o nível de risco:

| Situação | Distância do veículo | Indicação |
|---|---|---|
| 🟢 Seguro | Longe (acima do limiar de atenção) | LED verde |
| 🟡 Atenção | Aproximando-se (< 100 cm) | LED amarelo |
| 🔴 Perigo | Muito próximo (< 30 cm) | LED vermelho + buzzer intermitente |
| ⚪ Repouso | Nenhum pedestre presente | LED verde, sem alerta |

## Componentes utilizados (simulação)

- ESP32 DevKit C V4
- Sensor ultrassônico HC-SR04
- Sensor de movimento PIR
- Buzzer
- 3 LEDs (vermelho, amarelo, verde) + resistores

## Tecnologias

- C/C++ (Arduino Framework)
- Simulação via [Wokwi](https://wokwi.com)

## Como executar

1. Acesse o [simulador do projeto no Wokwi](https://wokwi.com/projects/466946399625834497) **ou** importe os arquivos `sketch.ino` e `diagram.json` em um novo projeto ESP32 no Wokwi.
2. Clique em "Start Simulation".
3. Acione o sensor PIR (clique nele na simulação) e ajuste a distância do HC-SR04 para ver os diferentes estados do semáforo.

## Status

Protótipo funcional em ambiente de simulação (Wokwi) — ainda não implementado em hardware físico.

## Possíveis melhorias futuras

- Implementação física com os componentes reais
- Conectividade (Wi-Fi/MQTT) para enviar alertas a um painel remoto
- Registro de dados de passagem/eventos de risco

## Autores

Ali Amer · Arthur Brambilla · Matheus Sayegh · João Thiago
