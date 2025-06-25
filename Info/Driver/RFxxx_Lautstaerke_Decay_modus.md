Der "Decay Modus" bei Schrittmotortreibern, auch als **Strom-Abkling-Modus** (current decay) bezeichnet, ist ein entscheidender Parameter für die Regelung des Stroms in den Wicklungen eines Schrittmotors. Er bestimmt, wie schnell der Strom in einer Spule abgebaut wird, wenn sie abgeschaltet wird. Die richtige Einstellung des Decay Modus ist entscheidend für die Leistung des Motors, insbesondere bei höheren Geschwindigkeiten, und beeinflusst das Drehmoment, die Geräuschentwicklung und die Erwärmung.

### **Grundlagen des Stromabbaus**

Ein Schrittmotortreiber steuert den Strom durch die Motorwicklungen mithilfe von pulsweitenmodulierten (PWM) Signalen. Wenn der Zielstrom in einer Wicklung erreicht ist, schaltet der Treiber den Strom ab. Die Art und Weise, wie dieser Strom abgebaut wird, wird durch den Decay Modus bestimmt. Es gibt hauptsächlich drei Modi:

* **Slow Decay (langsamer Abbau):** Beim Slow Decay wird der Strom langsam abgebaut, indem die Spule kurzgeschlossen wird und der Strom durch die Freilaufdioden der H-Brücke des Treibers zirkuliert. Dies führt zu einer geringen Stromwelligkeit (ripple), was einen ruhigeren und leiseren Motorlauf zur Folge hat. Allerdings kann es bei hohen Drehzahlen dazu führen, dass der Strom nicht schnell genug dem Sollwert folgen kann, was zu einem Verlust an Drehmoment führt.
* **Fast Decay (schneller Abbau):** Im Fast Decay Modus wird die Polarität der an der Wicklung anliegenden Spannung umgekehrt. Dies führt zu einem sehr schnellen Abbau des Stroms. Der Vorteil ist eine bessere Stromregelung bei hohen Geschwindigkeiten, was ein höheres Drehmoment ermöglicht. Der Nachteil ist eine höhere Stromwelligkeit, die zu mehr Vibrationen, Geräuschen und einer stärkeren Erwärmung des Motors führen kann.
* **Mixed Decay (gemischter Abbau):** Dieser Modus kombiniert die Vorteile von Slow und Fast Decay. Typischerweise beginnt der Abbauzyklus mit einem schnellen Abbau (Fast Decay) für eine definierte Zeit und geht dann in einen langsamen Abbau (Slow Decay) über. Moderne Treiber können diesen Übergang auch intelligent steuern, je nachdem, wie schnell der Strom abgebaut werden muss. Dies ermöglicht eine gute Leistung über einen weiten Drehzahlbereich – ein ruhiger Lauf bei niedrigen Geschwindigkeiten und ein hohes Drehmoment bei hohen Geschwindigkeiten.

---

### **Auswirkungen der verschiedenen Modi**

| Eigenschaft | Slow Decay | Fast Decay | Mixed Decay |
| :--- | :--- | :--- | :--- |
| **Laufruhe/Geräusch** | Sehr ruhig | Lauter, mehr Vibrationen | Guter Kompromiss |
| **Drehmoment bei niedriger Drehzahl** | Gut | Gut | Gut |
| **Drehmoment bei hoher Drehzahl** | Geringer | Höher | Gut |
| **Stromwelligkeit (Ripple)** | Gering | Hoch | Moderat |
| **Mot erwärmung** | Geringer | Höher | Moderat |

---

### **Einstellung des Decay Modus**

Bei vielen modernen Schrittmotortreibern, wie beispielsweise denen von Trinamic (TMC-Serie), ist der Decay Modus intelligent und passt sich automatisch an die Betriebsbedingungen an (z.B. durch Technologien wie StealthChop™ und SpreadCycle™). Bei einfacheren Treibern (z.B. A4988 oder DRV8825) kann der Modus oft nicht direkt eingestellt werden, sondern arbeitet in einem festen oder automatisch gemischten Modus. Bei einigen Treibern lässt sich das Verhalten über externe Widerstände oder Potentiometer beeinflussen.

**Zusammenfassend lässt sich sagen**, dass die Wahl des richtigen Decay Modus ein Kompromiss zwischen Laufruhe und Drehmoment bei hohen Drehzahlen ist. Für die meisten Anwendungen, insbesondere im 3D-Druck oder bei CNC-Fräsen, bieten Treiber mit einem intelligenten oder gemischten Decay Modus die beste Gesamtleistung.

Author: DennisNochmal aus dem rf1000.de Forum
Quelle: https://www.rf1000.de/viewtopic.php?f=7&t=3459
