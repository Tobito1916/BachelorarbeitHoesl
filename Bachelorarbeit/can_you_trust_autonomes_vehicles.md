---
type: Bachelor
keywords: Bachelor
---

# Notizen zu: Can you trust autonomes vehicles: Contactless Attacks against Sensors of Self-driving Vehicle

- In dieser Arbeit wollen die Autoren mehrere Angriffe gegen MMW Radare und andere Sensoren fahren, uns interessiert da aber nur das MMW Radar
- Diese Arbeit soll mit empirischen Studien arbeiten, also werden die Angriffe auch wirklich durchgeführt und nicht nur Theoretisch geplant
- Im Background gehen sie erstmal darauf ein, dass in zahlreichen Arbeiten davor gezeigt wurde, dass Man über den CAN-Bus, welcher alle Systeme verbindet, z.b die ECU angreifen kann. Diese Angriffe haben schon gezeigt, welchen zum Teil großen Schaden damit anrichten kann
- Diese Angriffe wurden aber meist durch den OBD-II Port gefahren
- Anderen Studien haben auch schon gezeigt, dass es auch ohne direkten Zugriff auf den CAN-Bus möglich ist angriffe zu fahren und erheblichen Schaden anzurichten. So konnte z.B kontrolle über ganze Teile des Fahrzeuges übernommen werden.
- Die Experimente am Radar werden sowohl in Lab gemacht wie auch an einem Tesla Model S

## Thread Model

- Attacker hat keine Vorwissen über die Senoren
- Mittlere Finazen, ist sowohl in der Lage alleine zu Arbeiten, wie auch mit anderen zusammen zuarbeiten.
- Hat zugang zu den Sensoren oder zu ähnlichen Senoren. 
- Der Angreifer ist bewandert in Hardware Design oder funktioniert off the shelf tech zu seinem zweck um.
- Er greift von außerhalb des Autos an
- der Vicitim Sensor darf nicht beschädigt oder verändert werden
- Die Angriffe werden nicht bei schnell fahrenden Autos funktionieren könne aber in langsameren Szenarien zu Kollisioe oder anderen Fehlfunktionen führen.

## Attack Model

- Unterschied zwischen cyber Angriffen und Senor Angriffen: man nutzt physische Kanäle
- Dabei nutzen Sensor Angriffe die selben Kanäle wie der Opfer
- so können diese Targets gestört oder manipuliert werden.
- Senoren sind eher lower Level Bauteile, normaler Weise wird ihnen vertraut, somit falsche readings könnten ungewollte ergebnisse erzielen
- Nachteile: nahe Angriffsreichweite, zusätzliche Hardware von Nöten, lange exploit Zyklen und viel Wissen von Nöten
- viele Senoren basieren auf anderen physikalischen Regeln, weshalb angriffe nicht einfach übernommen werden können.
- Grundlegende Idee bei den Angriffen: das einbringen von Noise und künstlichen Signalen: Jamming and Spoofing Attacks
- Sensoren sollen gegenüber natürlichem Noise resistent sein, aber die Resistenz gegenüber künstlichem Noise ist noch nicht gegeben
- Wenn künstlich Noise erzeugt wird ändert sich die Signal to Noise Ratio und angriffe könnten erkannt werden.
- Künstliche Signale, können wenn sie richtig bearbeitet werden, nicht von echten Signalen unterschieden werden und werden somit als valide angesehen. Wenn man diese künstlichen Signale kontrollieren kann, könnte man so Manipulationen ausführen

## Die Angriffe auf MMW Radare

- Jamming von dem 76-77 ghz Band hat funktioniert. Einmal nur 76500 gejammed das ander mal um 455 alterniert. 
- Spoofing hat sich als wesentlich schwerer herrausgestellt, da fehlten den Machern aber auch noch eine Hornantenne 
- Kosten sind ein sehr großes Problem das Equipment kostet mehr als der im Test verwendete Tesla Model S