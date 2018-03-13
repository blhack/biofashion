###Colors
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

###Multicolor Blink
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
