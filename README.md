# hello-world

int zader = 0;

int rast = 0;

void setup()

{

pinMode (11, INPUT);

pinMode (12, OUTPUT);

pinMode (8, OUTPUT);

pinMode (10, OUTPUT);

pinMode (9, INPUT);

}

void loop()

{

digitalWrite(12, LOW);

delayMicroseconds(10);

digitalWrite(12, HIGH);

delayMicroseconds(10);

digitalWrite(12, LOW);

zader = pulseIn(11, HIGH);

rast = (zader/2)/29.1;

digitalWrite(8, HIGH);

if (rast<100)

{

analogWrite(10, 200);

digitalWrite(8, LOW);

delay(3000);

analogWrite(10, 100);

digitalWrite(8, LOW);

delay(3000);

analogWrite(10, 0);

digitalWrite(8, HIGH);

delay(500);

}

}
