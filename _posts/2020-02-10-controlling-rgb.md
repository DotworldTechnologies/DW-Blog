---
layout: post
title:  "Controlling RGB strips with Arduino"
author: lalith
image: assets/images/controlling-rgb/violet.jpg
description: "RGB strips can be controlled using own RGB program using arduino"
featured: true
hidden: false
comments: false
---

The RGB (Red Green Blue) LED can be controlled using Arduino programming also we can bring the varies colours in a single strip.

Today, I want to show you how you too can control that powerful little LED in your own and make your place as smarter.

Incandescent light bulbs are slowly becoming a thing of the past with LEDs kicking in, especially RGB LEDs. So, why not learn how to control your RGB LEDs the way you want?

Our RGB and multi-colour LED strip light allows customers to have full control over the colour of their lighting. With three or more LEDs on each node, users can seamlessly blend colours to achieve the perfect hue. ... Use your imagination and choose your desired colour to set the mood


#### List of things you’ll need

    - Arduino uno board
    - 5v LED strip
    - USB cable (or something else to power your Arduino)
    - 330ohm resistor


#### What is a light strip?

An LED strip light (also known as an LED tape or ribbon light) is a flexible circuit board populated by surface mounted light-emitting diodes (SMD LEDs) and other components that usually comes with an adhesive backing.

#### What is RGB colour value?

A colour’s RGB value indicates its red, green, and blue intensity. Each intensity value is on a scale of 0 to 255, or in hexadecimal from 00 to FF. RGB values are used in HTML, XHTML, CSS, and other web standards

In this tutorial we’ll be setting our RGB LED to any colour. 

#### Let’s go!

Make the connections as shown below.

![Arduino Connection](//blog.dotworld.in/assets/images/controlling-rgb/circuit.png)

Once you completed the final circuit please download (fast led) library file in Arduino then go with program listed below:

Procedure for downloading FastLED.h library file:

Open Arduino Software --> Tools --> Manage libraries --> seach for ***FastLED.h*** --> install

![Download library](//blog.dotworld.in/assets/images/controlling-rgb/download.png)

```c
#include "FastLED.h"
#define NUM_LEDS 60
#define DATA_PIN 6
CRGB leds[NUM_LEDS];
void setup() {
  FastLED.addLeds<WS2812B, DATA_PIN, RGB>(leds, NUM_LEDS);
}
void loop() {
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(0, 255, 0);
    FastLED.show();
    delay(5);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(255, 0, 0);
    FastLED.show();
    delay(5);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(0, 0, 255);
    FastLED.show();
    delay(5);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(51, 0, 102);
    FastLED.show();
    delay(5);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(245, 30, 30);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(55, 255, 0);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(0, 102, 51);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(250, 0, 190);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(55, 255, 10);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(0, 243, 122);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(255, 0, 255);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(122, 106, 0);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(135, 255, 12);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(255, 255, 255);
    FastLED.show();
    delay(15);
    leds[i] = CRGB(0, 0, 0);
    FastLED.show();
  }
}
```


When the circuit get completed compile and run the program in a circuit 

#### Colour codes for controlling RGB LED to various colours


|  Colourname |  (R, G, B) |  Hex | 
|---|---|---|
| Black		 | (0,0,0)			 | #000000 |
| White		 | (255,255,255)	 | #FFFFFF |
| Red		 | (255,0,0)		 | #FF0000 |
| Lime		 | (0,255,0)		 | #00FF00 |
| Blue		 | (0,0,255)		 | #0000FF |
| Yellow	 | (255,255,0)		 | #FFFF00 |
| Cyan		 | (0,255,255)		 | #00FFFF |
| Magenta	 | (255,0,255)		 | #FF00FF |
| Silver	 | (192,192,192)	 | #C0C0C0 |
| Grey		 | (128,128,128)	 | #808080 |
| Maroon	 | (128,0,0)		 | #800000 |
| Olive		 | 128,128,0)		 | #808000 |
| Green		 | (0,128,0)		 | #008000 |
| Purple	 | (128,0,128)		 | #800080 |
| Teal		 | (0,128,128)		 | #008080 |
| Navy		 | (0,0,128)		 | #000080 |
{:.mbtablestyle}

These are some of the colour code for controlling RGB led to bring various colour, you can use these values and change the colour code as your convenience. 