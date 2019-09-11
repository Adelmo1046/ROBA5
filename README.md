roba5

//declaração de variáveis
char inChar= 0;
int piscar=0;

void setup() {                
  // initialize the digital pin as an output.
  // Pin 13 has an LED connected on most Arduino boards:
  pinMode(13, OUTPUT); 

  // open the serial port:
  Serial.begin(9600);


 
}


void loop() {

  if (Serial.available() > 0) {
    inChar= Serial.read();

    if (inChar =='1'){
      Serial.print("acender o led ");
      digitalWrite(13, HIGH);   // LIGA O LED
      piscar=0;
    ;n
    if (inChar =='0'){
      Serial.print("apagar o led ");
      digitalWrite(13, LOW);   // DESLIGA O LED
    } ;
    if (inChar =='3'){
      piscar =1;
       }
    }

if (piscar == 1) {
 Serial.print("led pisca");
      digitalWrite(13, HIGH); // LIGA LED
      delay(1000); // 1 SEGUNDO              
      digitalWrite(13, LOW); // DESLIGA LED
      delay(1000); // 1 SEGUNDO
}

},
