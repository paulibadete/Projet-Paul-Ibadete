#Code des capteurs

#define FORCE_SENSOR_PIN0 A0 // the FSR and 10K pulldown are connected to A0<br>
#define FORCE_SENSOR_PIN1 A1 // the FSR and 10K pulldown are connected to A1<br>
#define FORCE_SENSOR_PIN2 A2 // the FSR and 10K pulldown are connected to A2<br>
#define FORCE_SENSOR_PIN3 A3 // the FSR and 10K pulldown are connected to A3<br>
#define FORCE_SENSOR_PIN4 A4 // the FSR and 10K pulldown are connected to A4<br>
#define FORCE_SENSOR_PIN5 A5 // the FSR and 10K pulldown are connected to A0<br>

int  tableau[6];<br>
int cp;<br>
unsigned long millis();<br>
unsigned long currentTime=0;<br>
unsigned long previousTime=0;<br>
int moycapteur1;<br>
int moycapteur2;<br>
int moycapteur3;<br>
int moycapteur4;<br>
int moycapteur5;<br>
int moycapteur6;<br>
int nombrefois;<br>

int totcapteur1;<br>
int totcapteur2;<br>
int totcapteur3;<br>
int totcapteur4;<br>
int totcapteur5;<br>
int totcapteur6;<br>


void setup() {<br>
  Serial.begin(9600);<br>
}<br>

void loop() {/*pour afficher les vaeurs (pas neccessaire)*/<br>
  
Serial.print(millis());<br>
Serial.print("  ");<br>
Serial.print(analogRead(FORCE_SENSOR_PIN1));/*1capteur1*/<br>
Serial.print("  ");<br>
Serial.print(analogRead(FORCE_SENSOR_PIN0));/*0capteur2*/<br>
Serial.print("  ");<br>
Serial.print(analogRead(FORCE_SENSOR_PIN2));/*2capteur3*/<br>
Serial.print("  ");<br>
Serial.print(analogRead(FORCE_SENSOR_PIN3));/*3capteur4*/<br>
Serial.print("  ");<br>
Serial.print(analogRead(FORCE_SENSOR_PIN5));/*5capteur5*/<br>
Serial.print("  ");<br>
Serial.print(analogRead(FORCE_SENSOR_PIN4));/*4capteur6*/<br>
Serial.println("  ");<br>  

  tableau[0]=analogRead(FORCE_SENSOR_PIN0);<br>
  tableau[1]=analogRead(FORCE_SENSOR_PIN1);<br>
  tableau[2]=analogRead(FORCE_SENSOR_PIN2);<br>
  tableau[3]=analogRead(FORCE_SENSOR_PIN3);<br>
  tableau[4]=analogRead(FORCE_SENSOR_PIN4);<br>
  tableau[5]=analogRead(FORCE_SENSOR_PIN5);<br>
  
  int maximum;<br>
  for (int i=0;i<6;i++){<br>
    maximum=max(tableau[i],tableau[i+1]);<br>
  }<br>

if(maximum>0){<br>
  currentTime=millis();<br>
  nombrefois+=1;<br>
  if ((currentTime-previousTime)>438){ /*2749-2311*/<br>
    previousTime=currentTime;<br>
    totcapteur1+=analogRead(FORCE_SENSOR_PIN1);<br>
    Serial.print(analogRead(FORCE_SENSOR_PIN1));<br>
}<br>
  if ((currentTime-previousTime)>583){ /*2894-2311*/<br>
    previousTime=currentTime;<br>
    totcapteur2+=analogRead(FORCE_SENSOR_PIN0);<br>
    Serial.print(analogRead(FORCE_SENSOR_PIN0));<br>
}<br>
  if ((currentTime-previousTime)>971){ /*3282-2311*/<br>
    previousTime=currentTime;<br>
    totcapteur3+=analogRead(FORCE_SENSOR_PIN2);<br>
    Serial.print(analogRead(FORCE_SENSOR_PIN2));<br>
}<br>
  if ((currentTime-previousTime)>1046){ /*3357-2311*/<br>
    previousTime=currentTime;<br>
    totcapteur4+=analogRead(FORCE_SENSOR_PIN3);<br>
    Serial.print(analogRead(FORCE_SENSOR_PIN3));<br>
}<br>
  if ((currentTime-previousTime)>1314){ /*3625-2311*/<br>
    previousTime=currentTime;<br>
    totcapteur5+=analogRead(FORCE_SENSOR_PIN5);<br>
    Serial.print(analogRead(FORCE_SENSOR_PIN5));<br>
}<br>
  if ((currentTime-previousTime)>1415){ /*3726-2311*/<br>
    previousTime=currentTime;<br>
    totcapteur6+=analogRead(FORCE_SENSOR_PIN4);<br>
    Serial.print(analogRead(FORCE_SENSOR_PIN4));<br>
}<br>
moycapteur1=(totcapteur1/nombrefois);<br>
moycapteur2=(totcapteur2/nombrefois);<br>
moycapteur3=(totcapteur3/nombrefois);<br>
moycapteur4=(totcapteur4/nombrefois);<br>
moycapteur5=(totcapteur5/nombrefois);<br>
moycapteur6=(totcapteur6/nombrefois);<br>
delay(1); <br>               
}<br>
}<br>
