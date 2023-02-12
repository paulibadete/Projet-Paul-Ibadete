#Code des capteurs

#define FORCE_SENSOR_PIN2 A2 // the FSR and 10K pulldown are connected to A2
#define FORCE_SENSOR_PIN3 A3 // the FSR and 10K pulldown are connected to A3 //probleme de capteur
#define FORCE_SENSOR_PIN4 A4 // the FSR and 10K pulldown are connected to A4 //probleme de capteur
#define FORCE_SENSOR_PIN5 A5 // the FSR and 10K pulldown are connected to A5
int cp;
int test;


void setup() {
  Serial.begin(9600);
  int cp=0;
}

void loop() {
  int analogReading = analogRead(FORCE_SENSOR_PIN5);

  Serial.print("Force sensor reading = ");
  Serial.print(analogReading); // print the raw analog reading

  if (analogReading < 10)       // from 0 to 9
    Serial.println(" -> no pressure");
  else if (analogReading < 200) // from 10 to 199
    Serial.println(" -> light touch");
  else if (analogReading < 500) // from 200 to 499
    Serial.println(" -> light squeeze");
  else if (analogReading < 800) // from 500 to 799
    Serial.println(" -> medium squeeze");
  else // from 800 to 1023
    Serial.println(" -> big squeeze");
  
  if (analogReading >0) { 
    cp++; // initialiser le compteur du chrono à 0
    Serial.println(cp);
    }
  if (analogReading=0){
    cp=0;
  }
  delay(1000);
}


  
  
  
  
  
