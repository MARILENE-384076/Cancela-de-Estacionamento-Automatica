<h1 align = center> Fundamentos de IoT - Cancela de Estacionamento Automática </h1>
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

<hr>
<h3> Código Arduino </h3> 

<p align="justify">
 O código abaixo controla a leitura do sensor e a atuação do servo motor. 

<hr>
<h3> Como Funciona </h3> 

<p align="justify">
O código no loop() constantemente mede a distância de objetos na frente do sensor ultrassônico. Se um objeto é detectado a menos de 10 cm, o servo motor gira para o ângulo de 90°, simulando a abertura da cancela. Após um tempo de 5 segundos, a cancela se fecha. Se não houver nenhum objeto próximo, a cancela permanece fechada.
</p>

<p align="center"> <img src="https://github.com/MARILENE-384076/Cancela-de-Estacionamento-Automatica/blob/main/Imagens%20Projeto/C%C3%B3digo.png" /> </p>

<hr>
<h3> Explicação do código </h3> 

<p align="justify">  
	1.	Sensor de distância: O sensor HC-SR04 envia um pulso ultrassônico e mede o tempo que ele demora para voltar. Esse tempo é usado para calcular a distância até o objeto. </h>
	2.	Servo motor: O servo começa na posição de 90 graus. Quando detecta um objeto dentro da distância configurada (distanciaMax), ele move para 180 graus. Quando não detecta mais, volta para 90 graus.</h>
	3.	LEDs: Um LED (ledMovimento) acende quando há movimento, e outro (ledSemMovimento) acende quando não há movimento.</h>

Ajustes:

	•	distanciaMax: Ajuste o valor para determinar o quão perto o objeto precisa estar para ser considerado “detecção de movimento”.
	•	Pinos: Verifique se os pinos usados no código correspondem à sua montagem (pinos do sensor, servo, e LEDs).



 <hr>
<h3> Melhorias </h3> 

<p align="justify">  
Adicionar Feedback Visual: Incluir LEDs (vermelho e verde) para indicar o estado da cancela (aberta ou fechada).
Sistema de Detecção mais Robusto: Usar um segundo sensor ou um sensor de barreira para fechar a cancela somente depois que o veículo tiver passado completamente.
Controle de Tempo Dinâmico: Em vez de um delay fixo, usar a detecção do sensor para fechar a cancela quando o objeto se afastar.



