# WS2812 LED Würfel mit Demo- und Normalmodus

Dieses Projekt steuert einen 8x8 WS2812 LED-Würfel mit einem Taster und optional einem Piezo-Lautsprecher.  
Der Würfel zeigt Würfelzahlen an, hat einen Demo-Modus mit automatischen Würfen und ermöglicht manuelle Würfe per Taster.

## Features

- **Demo-Modus**: Würfelt automatisch und zeigt animierte Würfelzahlen.
- **Normalmodus**: Manuelles Würfeln per Taster.
- **Taster-Kurz-/Langdruck**:
  - Kurz: normaler Wurf, Demo endet endgültig.
  - Lang (>2s): Demo wird wieder aktiviert.
- **Piezo-Klick**: Ton bei jedem Würfelwurf.
- **Non-blocking State-Machine**: LEDs, Würfelanimationen und Taster-Abfrage laufen parallel.

## Hardware

- 8x8 WS2812 LED-Matrix
- Arduino Uno (oder kompatibel)
- Taster an `PIN 2`
- Piezo-Lautsprecher an `PIN 9` (optional)
- Widerstände und Verkabelung nach WS2812-Vorgaben
- Arduino `INPUT_PULLUP` für den Taster

## Software / Bibliotheken

- [FastLED](https://github.com/FastLED/FastLED)
- Arduino IDE 1.8+ oder PlatformIO

## Installation

1. Repository klonen oder ZIP herunterladen.
2. FastLED Bibliothek in der Arduino IDE installieren.
3. Pins ggf. an die eigene Hardware anpassen.
4. Hochladen auf Arduino.
