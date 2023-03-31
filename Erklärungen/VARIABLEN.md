## Einleitung
Was sind "Variablen", was sind "Attribute" oder "Eigenschaften"? Bei den vielen verschiedenen Worten, handelt es sich im Grunde genommen um das selbe, mit ein paar kleinen Unterschieden. Dazu aber erst später etwas mehr. Variablen (so nennen wir sie ab jetzt), sind kleine Speichereinheiten, die einen ganz bestimmten Wert speichern. Sei es dein Alter, dein Name, ob du einen Führerschein haben darfst, etc.

## Eine Box im Lager
Stellen wir uns nun vor, wir wären ein Unternehmen, das sich darauf spezialisiert hat, solche Variablen zu speichern. Wichtig sind für uns:
+ Die Namen der Variablen
+ Die Art des gespeicherten Werts (Datentyp, dazu später mehr)
+ Den aktuellen Wert, den die Variable tatsächlich hat
+ Die "Zugriffsberechtigungen" von außerhalb
Dafür haben wir uns nun kleine Boxen angeschafft. Diese beschriften wir nach dem Muster **Datentyp** + **Name** und in diese Boxen legen wir jetzt einen Zettel, auf dem der aktuelle Wert der Variable steht. Wir schauen uns jetzt verschiedene Prozesse an, bei denen wir diese Boxen benötigen.
### 1. Erstellen einer neuen Box
Es gibt verschiedene Möglichkeiten das Erstellen einer neuen Box anzugehen. Wir machen es auf die einfache Weise: Von Rechts nach Links. Dafür entscheiden wir uns zuerst, ob nur wir, oder alle anderen auch auf diese Variable zugreifen und diese verändern dürfen.
Je nachdem setzen wir den ersten Teil auf **public** (= öffentlich) oder **private** (= privat). Dann müssen wir entscheiden, wie bzw. was wir überhaupt speichern. Das entscheidet über den Datentypen (String, int, float, boolean, etc.). Als nächstes sollten wir darüber nachdenken, wie die Variable heißt. Es lohnt sich immer, einen gut verständlichen Namen zu verwenden, selbst wenn er dann etwas länger ist. In der Informatik verwenden wir im Gegensatz zur Mathematik nur ungern Namen wie **x** oder **a**. Zuletzt legen wir fest, wie die Box bei der Erstellung befüllt werden soll. Wenn wir diesen Schritt nicht machen, wird die Box automatisch mit der sogenannten **Null-Value** des jeweiligen Datentyps befüllt.
```Java
// Ziel: Variable für das Alter einer Person
private int alter = 0;
```
Mit **private** geben wir an, dass nur wir selbst diese Variable verändern dürfen. **int** bezeichnet den Datentyp *Ganzzahl*, also Zahlen wie 0, 1, etc. (auch negative Zahlen!). **alter** ist der Variablenname - Der erste Buchstabe ist **immer** klein, dannach wird der Anfangsbuchstabe jedes neuen Wortes groß geschieben (z.B. ***d**as**I**st**E**ine**V**ariable*). Der Standardwert eines Integers ist 0, aber um die Lesbarkeit zu verbessern, **initialisieren** wir die Variable an dieser Stelle mit dem Wert 0. Wir haben jetzt also eine Box mit der Aufschrift **int alter**, in der ein Zettel mit der Zahl **0** liegt, und mit einem Codeschloss verschlossen ist, dessen Schlüssel nur wir haben.