const int buzzer = 3; 
const int sensor = 4;

int state; // 0 close - 1 open switch

void setup()
{
    pinMode(sensor, INPUT_PULLUP);
    pinMode(buzzer, OUTPUT);
}

void loop()
{
  state = digitalRead(sensor);
    
  if (state == HIGH) {
    tone(buzzer, 1000);  
    delay(300);          
    noTone(buzzer);      
    delay(200);          
  }
  else {
    noTone(buzzer);      
  }
}
