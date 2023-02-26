#Code des capteurs

// Déclaration des broches des capteurs de pression<br>
const int sensor1Pin = A0;<br>
const int sensor2Pin = A1;<br>
const int sensor3Pin = A2;<br>
const int sensor4Pin = A3;<br>
const int sensor5Pin = A4;<br>
const int sensor6Pin = A5;<br>
<br>
// Seuil de pression à partir duquel on considère que le capteur est activé<br>
const int VALEUR_SEUIL = 200;<br>
<br>
// Stockage des valeurs maximales pour chaque capteur pendant la foulée<br>
int pressionMax1;<br>
int pressionMax2;<br>
int pressionMax3;<br>
int pressionMax4;<br>
int pressionMax5;<br>
int pressionMax6;<br>
<br>
int moycapteur1;<br>
int moycapteur2;<br>
int moycapteur3;<br>
int moycapteur4;<br>
int moycapteur5;<br>
int moycapteur6;<br>

int totalcapteur1;<br>
int totalcapteur2;<br>
int totalcapteur3;<br>
int totalcapteur4;<br>
int totalcapteur5;<br>
int totalcapteur6;<br>
<br>
int nbrfoulée=0;<br>
<br>
void setup() {<br>
  // Configuration des broches des capteurs de pression en entrée<br>
  pinMode(sensor1Pin, INPUT);<br>
  pinMode(sensor2Pin, INPUT);<br>
  pinMode(sensor3Pin, INPUT);<br>
  pinMode(sensor4Pin, INPUT);<br>
  pinMode(sensor5Pin, INPUT);<br>
  pinMode(sensor6Pin, INPUT);<br>
  Serial.begin(9600);<br>
}<br>
<br>
void loop() {<br>
  // Attente que le pied soit en contact avec le sol<br>
  while (analogRead(sensor1Pin) < VALEUR_SEUIL &&<br>
         analogRead(sensor2Pin) < VALEUR_SEUIL &&<br>
         analogRead(sensor3Pin) < VALEUR_SEUIL &&<br>
         analogRead(sensor4Pin) < VALEUR_SEUIL &&<br>
         analogRead(sensor5Pin) < VALEUR_SEUIL &&<br>
         analogRead(sensor6Pin) < VALEUR_SEUIL) {<br>
    // Attendre
  }

  // Initialisation des valeurs maximales à 0
  pressionMax1 = 0;<br>
  pressionMax2 = 0;<br>
  pressionMax3 = 0;<br>
  pressionMax4 = 0;<br>
  pressionMax5 = 0;<br>
  pressionMax6 = 0;<br>

  debut_contact = millis();<br>

  // Enregistrement des valeurs de chaque capteur pendant la foulée<br>
  while (analogRead(sensor1Pin) >= VALEUR_SEUIL ||<br>
         analogRead(sensor2Pin) >= VALEUR_SEUIL ||<br>
         analogRead(sensor3Pin) >= VALEUR_SEUIL ||<br>
         analogRead(sensor4Pin) >= VALEUR_SEUIL ||<br>
         analogRead(sensor5Pin) >= VALEUR_SEUIL ||<br>
         analogRead(sensor6Pin) >= VALEUR_SEUIL) {<br>
    pressionMax1 = max(pressionMax1, analogRead(sensor1Pin));<br>
    pressionMax2 = max(pressionMax2, analogRead(sensor2Pin));<br>
    pressionMax3 = max(pressionMax3, analogRead(sensor3Pin));<br>
    pressionMax4 = max(pressionMax4, analogRead(sensor4Pin));<br>
    pressionMax5 =max(pressionMax5, analogRead(sensor5Pin));<br>
    }<br>
<br>
    unsigned long fin_contact = millis();<br>
    unsigned long duree_contact = fin_contact - debut_contact;<br>
      
   nbrfoulée+=1;<br>
   totalcapteur1+=pressionMax1;<br>
   totalcapteur2+=pressionMax2;<br>
      totalcapteur3+=pressionMax3;<br>
      totalcapteur4+=pressionMax4;<br>
      totalcapteur5+=pressionMax5;<br>
      totalcapteur6+=pressionMax6;<br>

   moycapteur1=totalcapteur1/nbrfoulée;<br>
      moycapteur2=totalcapteur2/nbrfoulée;<br>
      moycapteur3=totalcapteur3/nbrfoulée;<br>
      moycapteur4=totalcapteur4/nbrfoulée;<br>
      moycapteur5=totalcapteur5/nbrfoulée;<br>
      moycapteur6=totalcapteur6/nbrfoulée;<br>
<br>
      Serial.print(moycapteur1);<br>
      Serial.print(",");<br><br>
      Serial.print(moycapteur2);<br><br>
      Serial.print(",");<br><br>
      Serial.print(moycapteur3);<br>
      Serial.print(",");<br>
      Serial.print(moycapteur4);<br>
      Serial.print(",");<br>
      Serial.print(moycapteur5);<br>
      Serial.print(",");<br>
      Serial.print(moycapteur6);<br>
      Serial.println("");<br>
      
      

   // Réinitialisation des valeurs maximales de pression<br>
      pressionMax1 = 0;<br>
      pressionMax2 = 0;<br>
      pressionMax3 = 0;<br>
      pressionMax4 = 0;<br>
      pressionMax5 = 0;<br>
      pressionMax6 = 0;<br>
    }

   delay(1);
  }<br>
}
