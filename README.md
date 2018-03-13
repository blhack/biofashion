### Colors
```
#include <Adafruit_NeoPixel.h>

Adafruit_NeoPixel strip = Adafruit_NeoPixel(1, 8, NEO_GRB + NEO_KHZ800);

void setup() {
  strip.begin();
  strip.show();
}

void loop() {
  strip.setPixelColor(0, 255, 255, 255);
  strip.show();
}
```

### Blink

```
#include <Adafruit_NeoPixel.h>

Adafruit_NeoPixel strip = Adafruit_NeoPixel(1, 8, NEO_GRB + NEO_KHZ800);

void setup() {
  strip.begin();
  strip.show();
}

void loop() {
  strip.setPixelColor(0, 255, 255, 255);
  strip.show();
  delay(1000);
  strip.setPixelColor(0, 0, 0, 0);
  strip.show();
  delay(1000);
}
```

### Multicolor Blink
```
#include <Adafruit_NeoPixel.h>

Adafruit_NeoPixel strip = Adafruit_NeoPixel(1, 8, NEO_GRB + NEO_KHZ800);

void setup() {
  strip.begin();
  strip.show();
}

void loop() {
  strip.setPixelColor(0, 255, 255, 255);
  strip.show();
  delay(1000);
  strip.setPixelColor(0, 255, 0, 255);
  strip.show();
  delay(1000);
}
```

### Switch
```
#include <Adafruit_NeoPixel.h>

Adafruit_NeoPixel strip = Adafruit_NeoPixel(1, 8, NEO_GRB + NEO_KHZ800);

void setup() {
  pinMode(10, INPUT_PULLUP);
  strip.begin();
  strip.show();
}

void loop() {
  if (digitalRead(10) ==  LOW) {
    strip.setPixelColor(0, 255, 0, 0);
    strip.show();
  } else {
    strip.setPixelColor(0, 0, 0, 0);
    strip.show();
  }
}
```

### Multicolor Switch

```
#include <Adafruit_NeoPixel.h>

Adafruit_NeoPixel strip = Adafruit_NeoPixel(1, 8, NEO_GRB + NEO_KHZ800);

void setup() {
  pinMode(10, INPUT_PULLUP);
  pinMode(9, INPUT_PULLUP);
  strip.begin();
  strip.show();
}

void loop() {
  if (digitalRead(10) ==  LOW) {
    strip.setPixelColor(0, 255, 0, 0);
    strip.show();
  }
  else if (digitalRead(9) ==  LOW) {
    strip.setPixelColor(0, 0, 255, 0);
    strip.show();
  } 
  else {
    strip.setPixelColor(0, 0, 0, 0);
    strip.show();
  }
}
```
