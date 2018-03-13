https://adafruit.github.io/arduino-board-index/package_adafruit_index.json 

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

# 5 pixels

```
#include <Adafruit_NeoPixel.h>

Adafruit_NeoPixel strip = Adafruit_NeoPixel(10, 12, NEO_GRB + NEO_KHZ800);

void setup() {
  pinMode(10, INPUT_PULLUP);
  pinMode(9, INPUT_PULLUP);
  strip.begin();
  strip.show();
}

void blackOut() {
  for (int i=0; i<10; i++) {
    strip.setPixelColor(i, 0, 0, 0);
  }
}

void loop() {
  blackOut();
  strip.setPixelColor(0, 255, 0, 0);
  strip.show();
  delay(500);

  blackOut();
  strip.setPixelColor(1, 255, 0, 0);
  strip.show();
  delay(500);

  blackOut();
  strip.setPixelColor(2, 255, 0, 0);
  strip.show();
  delay(500);

  blackOut();
  strip.setPixelColor(3, 255, 0, 0);
  strip.show();
  delay(500);

  blackOut();
  strip.setPixelColor(4, 255, 0, 0);
  strip.show();
  delay(500);

}
```

# 5 pixels speedup

```
#include <Adafruit_NeoPixel.h>

Adafruit_NeoPixel strip = Adafruit_NeoPixel(10, 12, NEO_GRB + NEO_KHZ800);

int speed = 100;

void setup() {
  pinMode(10, INPUT_PULLUP);
  pinMode(9, INPUT_PULLUP);
  strip.begin();
  strip.show();
}

void blackOut() {
  for (int i=0; i<10; i++) {
    strip.setPixelColor(i, 0, 0, 0);
  }
}

void loop() {
  blackOut();
  strip.setPixelColor(0, 255, 0, 0);
  strip.show();
  delay(speed);

  blackOut();
  strip.setPixelColor(1, 255, 0, 0);
  strip.show();
  delay(speed);

  blackOut();
  strip.setPixelColor(2, 255, 0, 0);
  strip.show();
  delay(speed);

  blackOut();
  strip.setPixelColor(3, 255, 0, 0);
  strip.show();
  delay(speed);

  blackOut();
  strip.setPixelColor(4, 255, 0, 0);
  strip.show();
  delay(speed);

}
```
