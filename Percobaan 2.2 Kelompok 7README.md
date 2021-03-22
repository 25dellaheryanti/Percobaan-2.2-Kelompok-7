byte pin_7segment[20][7]= {
  //anggota kelompok Della Heryanti
  {1,1,0,1,1,0,1}, //=2
  {1,1,0,1,1,0,1}, //=2
  {1,1,0,1,1,0,1}, //=2
  {1,1,1,1,1,1,0}, //=0
  {1,1,1,1,1,1,0}, //=0
  {0,1,1,0,0,0,0}, //=1

  //anggota kelompok Sandra Shadiqah
  {0,1,1,0,0,0,0}, //=1
  {1,0,1,1,1,1,1}, //=6
  {0,1,1,0,0,0,0}, //=1
  {1,1,1,1,1,1,0}, //=0
  {1,1,0,1,1,0,1}, //=2
  {1,1,1,1,1,1,0}, //=0
  {1,1,1,1,1,1,0}, //=0
  {1,1,1,1,1,1,0}, //=0

  //anggota kelompok Nurul Fatimah Kaltsum
  {0,1,1,0,0,1,1}, //=4
  {1,1,1,1,0,0,1}, //=3
  {1,1,0,1,1,0,1}, //=2
  {1,1,1,1,1,1,0}, //=0
  {1,1,1,1,1,1,0}, //=0
  {0,1,1,0,0,0,0}}; //=1
  
void setup() {
  pinMode(2, OUTPUT), pinMode(3, OUTPUT), pinMode(4, OUTPUT);
  pinMode(5, OUTPUT), pinMode(6, OUTPUT), pinMode(7, OUTPUT);
  pinMode(8, OUTPUT), pinMode(9, OUTPUT), digitalWrite(9,LOW);

}

void loop() {
  for(byte angka = 0; angka<20; ++angka) {
    delay(500);
    tampilkan(angka);
  } 
 }
 
 void tampilkan(byte baris) {
  byte pin = 2;
  for(byte kolom = 0;kolom <7; ++kolom) {
    digitalWrite(pin, pin_7segment[baris][kolom]);
    ++pin;
  }
 }
