# Edge-Computing---CP2---README

# Checkpoint 2

**Nome: Anna Heloisa, Danilo Urze, Lucas Sobral, Murilo Alves, Pedro Henrique Oliveira** 

**Turma: 1ESPX**

**Ano: 2023**

## Objetivo
Projetar um sistema Arduino para a Adega e garantir a qualidade do vinho. Ele será responsável por, coletar informações de luminosidade, temperatura e umidade, e expressar para os funcionários essas medidas, caso estejam fora do ideal.

## Descrição do desafio

## Desenvolvimento do projeto
Após pesquisas e consultas em antigos projetos para a mesma vinheria. A montagem se baseia em sensores, sendo DHT11 para a umidade, LDR para luminosidade e TMP36 para temperatura. Ao adicionarmos as unidades de medida ideais para cada um dos sensores, forcando em manter o padrão recomendado para armazenamento de vinhos, foi possível projetar a parte de alertas do sistema, que se baseia em LEDs verde, amarelo e vermelho, um buzzer que aciona uma buzina para chamar a atenção dos funcionários, e um LCD, responsável por expressar quais medidas estão em seu nível ideal, e quais fora de seus padrões.

## Como executar o projeto
Iniciamos projetando o hardware do sistema, conectando do arduino para as placas de ensaio os cabos de alimentação, sendo esses o cabo de 5V, que se conecta no lado positivo, e o GND, o fio terra, que se conecta do lado negativo. Após isso, em uma placa de ensaio pequena, conectamos os LEDs (1-vermelho, 1-amarelo e 1-verde), cada LED possui um resistor de 220Ω e um cabo que se liga a uma entrada. Após a placa de LEDs ser concluida, adicionamos uma placa de ensaio maior, a qual terá seus cabos de alimentação e fio terra compartilhados com a outra placa, dessa forma, podemos conectar os sensores, começando pelo TMP36 (temperatura), que possui 3 entradas:
 - Esqueda → alimentação 5V;
 - Direita → GND;
 - Central → uma das portas análogas;
 
O sensor de luminosidade LDR possui apenas 2 entradas:
 - Esquerda → alimentação 5V;
 - Direita → um resistor de 10 kΩ, que liga ao GND, e um cabo até outra porta análoga;
 
O sensor de umidade potenciômetro também possui 3 entradas:
 - Esquerda → GND;
 - Direita → alimentação 5V;
 - Central → outra porta análoga;
 
Finalizando os sensores, podemos adicionar o buzzer:
 - Esquerda → GND;
 - Direita → uma das portas padrões;
 
 Para fizalizar, o LCD, que necessita outro potenciômetro para seu funcionamento:
 
 Potenciômetro:
 - Entrada esquerda → Alimentação 5V;
 - Entrada central → Entrada "V0" LCD;
 - Entrada direita → GND;
 
 LCD:
 - Entrada "GND" → GND;
 - Entrada "VCC" → Alimentação 5V;
 - Entrada "V0" → Entrada central do Potenciômetro;
 - Entrada "RS" → Porta padrão;
 - Entrada "RW" → GND;
 - Entrada "E" → Porta padrão;
 - Entrada "DB4" → Porta padrão;
 - Entrada "DB5" → Porta padrão;
 - Entrada "DB6" → Porta padrão;
 - Entrada "DB7" → Porta padrão;
 - Entrada "LED" → Alimentação 5V, com resistor de 220Ω;
 - Entrada "LED" → GND;
 
 Após a finalização do hardware, escrevemos o código em liguagem C++ que funcionava a base de IFs, para o acionamento das LEDs, buzzer, teste dos níveis de medida e escritas no LCD.
 
 OBS: Para funcionamento do LCD, é necessario adicionarmos a biblioteca LiquidCrystal.h, essa permite o uso de comandos como led.begin(),led.print(), led.setCursor(), entre outros.

## Pré-requisitos
   - 1 Arduino Uno;
   - 1 Placa de ensaio pequena;
   - 1 Placa de ensaio;
   - 4 Resistores 220 ohm;
   - 1 Resistor 10 Kohm;
   - Led vermelho;
   - Led amarelo;
   - Led verde;
   - 1 Buzzer;
   - 1 Sensor LDR;
   - 1 Sensor TMP36;
   - 2 Potenciômetros;
   - 1 LCD;
   - Jumper cables.

## Video Explicativo
   - https://drive.google.com/file/d/1Nrjb1TQQlC53qLwR3Mbx9-K86HNMi1Sd/view?usp=sharing
   
## Projeto no Tinkercad
   - https://www.tinkercad.com/things/h0JlAGi9phX-edge-computing-cp2/editel?sharecode=3tSuf4tAIvBjvFOCKOfIhCWa1yIDzIUsrhb1YiZwMBo
