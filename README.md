// Diode Signal Detector on ESP32

const int signalPin = 25; // Pin connected after the diode

void setup() {
  Serial.begin(115200);        // Start serial communication at 115200 baud
  pinMode(signalPin, INPUT);   // Set the signal pin as input
}

void loop() {
  int signalState = digitalRead(signalPin);  // Read the signal state

  if (signalState == HIGH) {
    Serial.println("High voltage detected!");
  } else {
    Serial.println("No high voltage detected (safe).");
  }

  delay(500);  // Wait for 500 milliseconds
}
