GS-EDGE
Rodrigo Mori RM:555384
Gaabriel Barros RM:555410
link do tinkercard: https://www.tinkercad.com/things/h2a39NRv7Dr-gs-edge?sharecode=01QEn8Xa92ZKJdjzMPpKDA0BCmMqbuKxfa0_hDiAFzs

Neste projeto, nosso objetivo é criar um sistema simples, mas eficaz, para monitorar a qualidade da água, utilizando um Arduino Uno e sensores de temperatura e potenciômetro.

Para este projeto, utilizamos os seguintes componentes: um Arduino Uno, um potenciômetro para simular o sensor de pH, e LEDs para indicações visuais.
Conexões do Potenciômetro:

O potenciômetro tem três pinos. Conectamos o pino central ao pino analógico A1 do Arduino, um dos pinos laterais ao GND e o outro ao 5V do Arduino. Essa configuração permite que o potenciômetro simule os valores analógicos de um sensor de pH real.

Adicionamos LEDs para indicar visualmente diferentes níveis de pH. Conectamos os anodos dos LEDs aos pinos digitais 8, 9 e 10 do Arduino, e os catodos a resistores, que por sua vez estão conectados ao GND. Esses LEDs vão nos ajudar a visualizar quando o pH está em diferentes intervalos.

O código começa definindo os pinos de conexão e inicializando a comunicação serial. No loop principal, lemos o valor analógico do potenciômetro, que simula o pH, e convertemos essa leitura para um valor de pH."
Conversão do Valor do Potenciômetro:

A leitura do potenciômetro é convertida utilizando a fórmula ph = phValue * (5.0 / 1024.0) * 3.5, onde phValue é o valor lido do pino analógico. Este valor é então exibido no monitor serial."
Controle dos LEDs:

Utilizamos condicionais para acender diferentes LEDs com base no valor do pH. Por exemplo, se o pH for menor que 4.0, acendemos o primeiro LED. Se estiver entre 4.0 e 7.0, acendemos o segundo LED, e se for maior que 7.0, acendemos o terceiro LED."
