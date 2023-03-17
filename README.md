# BicycleIndicators
Sexy verkeerslichten voor jouw stadsfiets.
werk-in-uitvoering!

Hieronder: voorbeeld!!

<img src="https://github.com/pappavis/FLicht/blob/main/img/fietsKnipperlicht_voorbeeld.jpg?raw=true" width="10%" height="10%" alt="Voorbeeld FLicht">

## Techniek
"FLicht"  Een knipperlicht voor de fiets, bestaande uit 2x losse ESP32s verbonden via Bluetooth - 1x ESP32 aan je stuur met knoppen voor richtingaanwijzer, aan/uit schakelaar. Programmeertaal is <a href="https://micropython.org" target="_blank">MicroPython</a>.

### Low power circuit
<img src="https://github.com/pappavis/FLicht/blob/main/img/ESP32%20lowpower%20Neopixels%20circuit%2020230306%20falstad.com%20circuit.jpg?raw=true" width="60%" height="60%">
Voorbeeld circuit:<br>
- Openen met <a href="http://www.falstad.com/circuit/circuitjs.html">http://www.falstad.com/circuit/circuitjs.html</a><br>
 - Zie <a href="https://github.com/pappavis/FLicht/blob/main/src/circuit-20230316-1343.circuitjs%20ESP32%20lowpower%20Neopixels%20circuit%2020230306.txt">./src/circuit-20230316-1343.circuitjs ESP32 lowpower Neopixels circuit 20230306.txt</a>.<br>

### Hoe het zou moeten werken
1x ESP32 aan je fiets onder de zadel, of rugtas met 2x 8 Neopixels
- Beiden krijgen stroom van een 3,7V LiPo of 18650
- De LiPo is verbonden aan een TP4056 charging module, en ESP32 is direct eraan verbonden in DeepSleep.
- Wanneer IO-pin04 HIGH is, dan moet er stroom staan op de lijn maar, NeoPixel gaat niet aan.
- Wanneer IO-pin05 HIGH gaat bijvb NeoPixel "links"  aan en zelfde voor "rechts".

Moet ook een kastje printen op mijn Ender 3D-printer. Voorlopig prototype ik op een breadboard, maar wil eventueel een ontwerp in KiCAD maken, en door <a href="JLCBCB.com" target="_blank">JLCPCB</a> in China een PCB laten maken (surface mount ICs).

### Vraagstuk
Is mijn circuit "goed", welke mosfet / transistor kan ik beste gebruiken?

# Credits
door: Michiel Erasmus
