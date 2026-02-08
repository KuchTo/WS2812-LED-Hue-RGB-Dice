# Funktionsbeschreibung

Dieses Dokument beschreibt die wichtigsten Funktionen und Bedienelemente des WS2812 Würfels.

## Taster (PIN 2)

- **Kurz drücken (< 2s)**:
  - Beendet Demo-Modus (falls aktiv)
  - Startet einen normalen Würfelwurf
- **Lang drücken (≥ 2s)**:
  - Reaktiviert den Demo-Modus

## Piezo-Lautsprecher (PIN 9)

- Wird bei jedem Würfelwurf kurz angesteuert (2200 Hz, 15 ms)
- Danach auf `LOW` gezogen und Pin als `INPUT` gesetzt → kein Rauschen durch LED-PWM

## Demo-Modus

- Würfelt automatisch im Zyklus:
  1. Würfelroll-Animation
  2. Würfelanzeige 7 Sekunden
  3. Fade-Out Animation
  4. Pause 9 Sekunden
- Wiederholt sich endlos, bis Taster kurz gedrückt wird oder Demo durch langen Druck reaktiviert wird.

## Normalmodus

- Würfel startet nur bei Tastendruck
- Roll-Animation ähnlich wie Demo
- Piezo-Klick bei jedem Wurf
- Nach Fertigstellen der Anzeige bleibt der Würfel im Idle-Zustand, bis erneut gedrückt wird.
