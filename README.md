# design-digital-circuit-and-ultrasonic-sensor

what is ultrasonic-sensor

An ultrasonic sensor is an electronic device that measures the distance of a target object by emitting ultrasonic sound waves and converts the reflected sound into an electrical signal. Ultrasonic waves travel faster than the speed of audible sound the sound that humans can hear Ultrasonic sensors have two main components: the transmitter (which emits the sound using piezoelectric crystals) and the receiver which encounters the sound after it has travelled to and from the target

instruction code:

const int trigPin = 9;
const int echoPin = 10;
// defines variables
long duration;
int distance;
void setup() {
  pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output
  pinMode(echoPin, INPUT); // Sets the echoPin as an Input
  Serial.begin(9600); // Starts the serial communication
}
void loop() {
  // Clears the trigPin
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  // Sets the trigPin on HIGH state for 10 micro seconds
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  // Reads the echoPin, returns the sound wave travel time in microseconds
  duration = pulseIn(echoPin, HIGH);
  // Calculating the distance
  distance = duration * 0.034 / 2;
  // Prints the distance on the Serial Monitor
  Serial.print("Distance: ");
  Serial.println(distance);
}


circuit diagrams:

![image](https://github.com/xsaad7/design-digital-circuit-and-ultrasonic-sensor/assets/139689886/470dfd7d-21d0-4cd3-a41c-ab804143b204)

what is digital circuit:

A digital circuit is designed by using a number of logic gates on a single integrated circuit – IC. The input to any digital circuit is in the binary form “0’s” and “1’s”. The output obtained on processing raw digital data is of a precise value. These circuits can be represented in 2 ways either in a combinational way or a sequential way


Advantages:

1- High reliability
2- A high rate of transmission
3- Highly secure

Disadvantages

1-Consumes more energy than analog circuits
3-Heat dissipation is more
4-High cost

circuit diagram:

![image](https://github.com/xsaad7/design-digital-circuit-and-ultrasonic-sensor/assets/139689886/d131f689-211e-458d-929c-76dc963356e3)


