# Documentação

**Aqui se encontram todos os passos da ponderada:**

## Fotos

<div align="center">
<img src="/assets/fotoSemafaro-1.jpg" width="60%">
<br>
<br>
</div>

<div align="center">
<img src="/assets/fotoSemafaro-2.jpg" width="60%">
</div>
<br> <br>

## Vídeo

https://youtube.com/shorts/-9cZF4fGurg?feature=share


## Relato e Especificações

A montagem do protótipo foi feita seguindo a lógica ensinada em sala, de como se liga um componente e como podemos fazê-lo funcionar mandando energia para seu pino positivo assim que necessário. Também, é utilizada a lógica de adicionar uma resistência na passagem da corrente elétrica para que o Diodo Emissor de Luz (LED) não queime, e seu funcionamento é programado no IDE do Arduíno utilizando a biblioteca ESP32 para adaptar para o funcionamento desse microprocessador.


## Código

Código utilizado juntamente com a biblioteca "ESP32 Dev Module":
```
/ Definição de pins
const int LED_VERDE = 3;
const int LED_AMARELO = 6;
const int LED_VERMELHO = 9;
//Variáveis para controle de tempo
void setup() {
// Liga os LED umas apenas uma vez, fazendo o código funcionar corretamente:
  pinMode(LED_VERDE, OUTPUT);
  pinMode(LED_AMARELO, OUTPUT);
  pinMode(LED_VERMELHO, OUTPUT);
}
void loop() {
  // LEDs ligando na ordem correta dita pelo comando;
    //Pin verde
    digitalWrite(LED_VERDE, HIGH);
    delay(2000);
    digitalWrite(LED_VERDE, LOW);
    
    //Pin amarelo
    digitalWrite(LED_AMARELO, HIGH);
    delay(2000);
    digitalWrite(LED_AMARELO, LOW);

    //Pin vermelho
    digitalWrite(LED_VERMELHO, HIGH);
    delay(6000);
    
    //Pin amarelo
    digitalWrite(LED_AMARELO, HIGH);
    delay(2000);
    digitalWrite(LED_AMARELO, LOW);
}
``` 

## Tabela de Avaliação entre Pares

### Avaliador 1: Igor Sguissardi

Avalei o Trabalho da minha colega de sala Ana Beggiato, ela fez uma trabalho completinho, com todas as exigências do exercício, código totalmente condizente com o pedido, o semáfaro completamente funcional, cores dos fios se diferenciando seguindo a lógica convencional e ela ainda foi além, pois adicionou um buzzer ao seu semáfaro que fazia barulho quando a luz ficava vermelha.

|Critério|	Contempla (Pontos)|	Contempla Parcialmente (Pontos)	|Não Contempla (Pontos)	|Observações do Avaliador|
|-|-|-|-|-|
|Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores	|Até 3	|Até 1,5	|0 | contempla |	
|Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo	|Até 3	|Até 1,5	|0 | contempla |	
|Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) |	Até 3|	Até 1,5 |	0 | contempla |	
|Ir além: Implementou um componente de extra, fez com millis() ao invés do delay() e/ou usou ponteiros no código |	Até 1 |	Até 0,5 |	0 | contempla |	
| | | | |Pontuação Total = **10 pontos**|
<br> 

### Avaliador 2: Ana Beggiato

A Ana avaliou meu trabalho e viu que tudo também estava correto (todas os critérios que descrevi acima), no entanto, eu não adicionei algum elemento que fosse além do pedido.

|Critério|	Contempla (Pontos)|	Contempla Parcialmente (Pontos)	|Não Contempla (Pontos)	|Observações do Avaliador|
|-|-|-|-|-|
|Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores	|Até 3	|Até 1,5	|0 | contempla |	
|Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo	|Até 3	|Até 1,5	|0 | contempla |	
|Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) |	Até 3|	Até 1,5 |	0 | contempla |	
|Ir além: Implementou um componente de extra, fez com millis() ao invés do delay() e/ou usou ponteiros no código |	Até 1 |	Até 0,5 |	0 | não contempla |	
| | | | |Pontuação Total = **9 pontos**|