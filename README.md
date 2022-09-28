# TINKERCAD
Atividade no tinkercad sobre blinking led
//Curso: Bacharelado em Engenharia de Controle e Automação
//Disciplina: Sistemas Embacardos I
//Data: 26/09/2022
//Autor:Brenda Mayra
//Objetivo: blinking led

//LED_BUILTIN referente ao pino 13, ou coloca isso ou 13

#define LED 12//uso da diretiva define
//ou
/*int LED=12;*/
int statusLED = HIGH;
void blink (const int led, const int status);

void setup()//executa uma vez
{    
  pinMode(LED, OUTPUT);//define a configuração do pino
                               // input ou output
}

void loop()//varias vezes
{
  blink(LED, statusLED); //meu parametro
  
  
  if(statusLED == HIGH)
  {
    statusLED = LOW;
  }
  else
  {
    statusLED = HIGH;
  }
}
void blink(const int led, const int status)
{
  digitalWrite(led, status);
  delay(1000); // Wait for 1000 millisecond(s)
  
}
  
  
  
