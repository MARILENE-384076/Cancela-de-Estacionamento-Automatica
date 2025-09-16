<h1 align = center> Fundamentos de IoT - Cancela de Estacionamento Automática </h1>
<h4> Professor: Fred Aguiar </h4>
<h4> Alunos: Danilo, Diulie, Luna Beatriz, Marilene Araujo, Maycon Siqueira </h4>

<hr>
<h3> Introdução: </h3>

<p align="justify">
  Este é um projeto de automação que simula uma cancela de estacionamento automática. O sistema utiliza um sensor de presença ultrassônico para detectar a aproximação de um objeto (como um carro) e um servo motor para atuar como a cancela, abrindo e fechando a passagem. O projeto foi desenvolvido como parte de uma atividade em grupo para o curso de Técnico em Desenvolvimento de Sistemas , com o objetivo de aplicar conceitos de prototipagem e uso de sensores/atuadores.
  
<hr>
<h3> Componentes Necessários: </h3>

- Arduino Uno: A plataforma de microcontrolador que executa a lógica do projeto.
- Sensor de Distância Ultrassônico HC-SR04: Atua como o sensor de presença para detectar a proximidade.
- Servo Motor SG90: Atua como a cancela, controlando o movimento de abertura e fechamento.
- Protoboard: Para montar o circuito sem a necessidade de solda.
- Jumpers: Fios de conexão.
- Cabo USB: Para carregar o código no Arduino.
  
<hr>
<h3> Montagem do Circuito </h3> 

O circuito foi montado conforme o esquema abaixo. As conexões foram diretas e simples.

- Sensor Ultrassônico (HC-SR04):

   - VCC -> Pino 5V do Arduino

   - GND -> Pino GND do Arduino

   - Trig -> Pino digital D9 do Arduino

   - Echo -> Pino digital D10 do Arduino

- Servo Motor (SG90):

   - VCC (Vermelho) -> Pino 5V do Arduino

   - GND (Marrom/Preto) -> Pino GND do Arduino

   - Sinal (Laranja/Amarelo) -> Pino digital D3 do Arduino (pino PWM)
