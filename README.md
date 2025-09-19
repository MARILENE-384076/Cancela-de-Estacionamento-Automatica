<h1 align = center> Fundamentos de IoT - Cancela de Condomínio Automática </h1>
<h4> Professor: Fred Aguiar </h4>
<h4> Alunos: Danilo Santos, Diulie Mileide, Luna Beatriz, Marilene Araujo, Maycon Siqueira </h4>

<hr>
<h3> Introdução: </h3>

<p align="justify">
	Este é um projeto de automação que simula uma cancela de estacionamento automática. O sistema utiliza um sensor de presença ultrassônico para detectar a aproximação de um objeto (como um carro) e um servo motor para atuar como a cancela, abrindo e fechando a passagem. O projeto foi desenvolvido como parte de uma atividade em grupo para o curso de Técnico em Desenvolvimento de Sistemas , com o objetivo de aplicar conceitos de prototipagem e uso de sensores/atuadores.
</p>

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

<p align="justify"> 
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
</p>

<hr>
<h3> Código Arduino </h3> 

<p align="justify">
	O código abaixo controla a leitura do sensor e a atuação do servo motor. 
</p>

<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/C%C3%B3digo.png" /> </p>

<hr>

<h3> Explicação do Código </h3> 

<p align="justify">
	<h5> Como Funciona </h5>

Detecção de Objeto: O sensor HC-SR04 emite pulsos ultrassônicos e calcula a distância até um objeto com base no tempo que o pulso leva para voltar. A medição é feita constantemente.

<h5> Controle da Cancela: </h5>
Quando um objeto é detectado a uma distância menor que 10 cm, o servo motor move-se para o ângulo de 90°, abrindo a cancela.
Após 5 segundos, o servo retorna à sua posição original, fechando a cancela.
Se nenhum objeto for detectado, a cancela permanece fechada.

<h5> Indicadores Visuais (LEDs): </h5>

- O LED Verde (ledMovimento) acende quando um objeto é detectado. <br>
- E o LED Vermelho (ledSemMovimento) acende quando não há detecção.

<hr>
<h3> Variáveis: </h3>

- ledMovimento: LED que acende quando há movimento <br>
- ledSemMovimento: LED que acende quando não há movimento <br>
- alerta: Buzzer que emite um sinal sonoro quando detecta movimento <br>
- distanciaMax: Inicializa com o valor de 20 cm, esta variavel foi ajustada para determinar o quão perto o objeto precisa estar para ser considerado que existe “detecção de movimento” <br>
</p>

<hr>
<h3> Pinos: </h3>

<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Arduino.png" /> </p>

<hr>
<h3> Montagem do Protótipo: </h3>

<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Montagem%201.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Montagem%202.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Montagem%203.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Montagem%204.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Montagem%205.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Montagem%206.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Montagem%207.jpg" /> </p>

<hr>
<h3> Protótipo Pronto: </h3>

<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Pronto%200.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Pronto%201.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Pronto%202.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Pronto%203.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Pronto%204.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Pronto%205.jpg" /> </p>
<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/Prot%C3%B3tipo.mp4" /> </p>

<hr>
