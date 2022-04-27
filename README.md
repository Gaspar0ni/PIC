# PIC

# INTRODUÇÃO, PIC16F84A

microprocessador X microcontrolador

microcontrolador: funciona por si só

Software: Isis e microC

pino 16 e 15:  destinados ao cristal de oscilação externo

pino 4: master clear ou seja reset do dispositivo

barra em cima do pino a: significa que ele é ativo em nível lógico baixo

port a e port b: b tem 8 bits, ou seja 8 pinos que podem ser programados

se apontarmos 0 para para o pino 4, estamos enviando um reset para ele






anodo e catodo

### OBS

1.1 – Ânodo: É o polo negativo, sofre oxidação porque perde elétrons e é o agente redutor. 
1.2 - Cátodo: É o polo positivo, sofre redução por ganhar elétrons e é o agente oxidante.





Software: microC for pic






Firmware: 


# Aula 2 - Fusíveis de consig dos processadores, data sheet, sofware de simulação

Proteus: Proteus Design Suite é um software para criação de projetos eletrônicos, composto por uma suíte de ferramentas, [wiki](https://pt.wikipedia.org/wiki/Proteus_(programa_de_computador)).

5bits no porte a, e 8 bits no porte b.





não permite desabilitar o pino de reset (MCLR master clear)

precisa estar em nível lógico alto, ou então conectado a um botão para um pulso em nível baixo(a barra nele significa que ele é ativo em nível baixo), para reiniciar o processador.



Ao apertar o botão ele recomeça do zero(reset)

O botão não apaga o que foi feito no processador, apenas restarta ele





# Aula 3 - GRAVANDO O PRIMEIRO PIC, 12F675

Apenas 8 pinos, mas possui conversores ad

[Data sheet](http://ww1.microchip.com/downloads/en/devicedoc/30430c.pdf)

Ele possui apensa 8 pinos

Cristal oscilador

Registradores do controlador na linha abaixo

```
ANSEL = 0;
CMCON = 7;

TRISIO0_bit = 0;        TRISIO1_bit = 0;

GPIO = 0;     // começa em nível baixo

while(1){

  GPIO.F0 = 1;    //nível alto
  GPIO.F1 = 0;    //nível baixo
  delay_ms(100);  
  GPIO.F0 = 0;    
  GPIO.F1 = 1;   
  delay_ms(100);
}
```

OBS: para ligar os leds ele adicionou resistores







Osciloscópio

formas de onda

Os canais estão em saída diferente, pois quando um está em HIGH, o outro está em LOW.

horizontal-> tempo          vertical-> tensão

Os leds demandão de corrente para ligar.

rize time = tempo que a aonda demora par ir de 10% para 100%.

efeito spike =

picos de tensão = várias vezes a onda em HIGH

--------------------------------------------------------------------------

# ENTRADAS DIGITAIS Aula 4

com entrada digitais podemos implementar sensores.

pic 12F675

resistor de 220 ohms e um led que vai para o terra. Implementar um botão na entrada que aciona o circuito de 5 volts em nível alto

pino para alimentação(incompleto)

entensder "tree state"  da próxima aula (não sei se é esse nome tree state)







pull up e pull down






