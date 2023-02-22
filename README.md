# Veiculo-BLE
Veículo controlado comandos de celular enviado via BLE (Bluetooth Low Energy), o controlador é compatível com Android/IOS desenvolvido no App Inventor. O veículo é equipado com um esp32 que já vêm com BLE integrado e um driver responsável por acionar os motores DC. 

<div align=center>
<img src=recursos/prototipo.jpg width=40%>

[Video Demonstrativo](https://youtube.com/shorts/sn5v5UQEMDI?feature=share)
</div>

Foram utilizados:
- Chassi em acrílico, 
- 2x Motores DC 6V
- Driver L298
- esp32
- bateria 9V

## Como usar

Dê permissão ao aplicativo para acessar os dispositivos próximos, clique no botão Bluetooth e selecione o dispositivo ao "BLE-Server" aguarde até que o botão mude de cor (Verde - Conectado, Vermelho - Disconectado). Quando o celular estiver conectado, use os botões com as setas ("emojins com dedos indicadores") para controlar a direção do carrinho.

<p align=center>
<span><img src="/recursos/tela3.jpg" width=25%></span>
<span><img src="/recursos/tela2.jpg" width=25%></span>
<span><img src="/recursos/tela1.jpg" width=25%></span>
</p>

Conecte os pinos GPIO 27, 26, 25 e 33, respectivamente, às entradas IN1, IN2, IN3 e IN4 do driver L298. Para alimentar o ESP32 e o driver, utilize uma bateria de 9V. Conecte o polo positivo da bateria ao +Vcc do driver e ao pino 5V (ou Vin) do ESP32. Conecte o polo negativo da bateria aos pinos GND do ESP32 e do driver.

Alguns pontos importante: 
* Mantenha o pino jumper do regular de tensão do driver
* O ESP32 vem com um regulador interno conectado ao pino de 5V, que opera com uma faixa de tensão de 5V a 12V. Se você não tiver certeza se o seu DevKit suporta essa faixa de tensão, é recomendável usar um regulador de tensão externo ou alimentar a placa diretamente com 5V.
