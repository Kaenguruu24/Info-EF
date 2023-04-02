## Einleitung
while- und for-Schleifen sind ebenfalls ein essentieller Teil des Programmierens. Sie nehmen die Rolle des dynamischen Skalierens einer oder mehrerer Anweisungen ein und stellen somit eine verständlichere und kompaktere Alternative zu diesem Chaos dar:
```Java
// Sehr schlecht, nie machen!
fahre();
fahre();
fahre();
fahre();
fahre();
fahre();
fahre();

// Sehr gut, oft machen!
for (int i = 0; i < 7; i++)
{
	fahre();
}
```

### While-Schleifen
Eine While-Schleife (eng. while loop) ist eine Schleife, die einen Code-Block solange ausführt, wie die angegebene Bedingung wahr ist. Sie besteht aus dem Schleifenkopf mit dem Keyword **while** und der Bedingung und dem Code-Block darunter. Hier ein Beispiel:
```Java
while (lampeAn == true) // alternativer Ausdruck: while(lampeAn)
{
	// Tue Dinge
}

do
{
	// Tue Dinge
} while (lampeAn == true)
```
Die While-Schleife bietet eine gute Möglichkeit, Code über einen unbestimmten Zeitraum auszuführen, solange die angegebene Bedingung erfüllt ist. Wie im Beispiel zu sehen, gibt es zwei verschiedene Formen: **while** und **do-while**. Der Unterschied zwischen den beiden ist relativ simpel: Bei while-Schleifen wird zuerst die Bedingung überprüft und dann, wenn diese erfüllt ist, der Code-Block ausgeführt. Do-While-Schleifen kehren die Reihenfolge um. Erst wird der Code-Block ausgeführt und dann die Bedingung überprüft. Wenn diese erfüllt ist, springen wir wieder zum **do**-Teil der Schleife.

Um, ähnlich if und else, das "Übersetzer-Prinzip" anzuwenden, überlegen wir uns nun einen Satz, der "Solange" als "Keyword" für "while" benutzt. Ein Beispiel:
**Solange die Variable lampeAn wahr ist, sende einen Lichtstrahl aus**
+ 1. Übersetzen (ins Englische)
	-> While the variable "lampeAn" is true, cast light.
+ 2. Kürzen von sprachspezifischen Eigenheiten
	-> while lampeAn true, light.
+ 3. Übertragung in Java-Syntax (oder andere Sprachen)
```Java
while (lampeAn == true)
{
	light();
}
```
Hier ist gut zu erkennen, wie der Originalsatz im Endergebnis eingebettet ist. Da Boolean-Expressions (d.h. Bedingungen, die aus einem oder mehreren Booleans bestehen) in Java kein '== true' oder '== false' benötigen, kann man auch ``while (lampeAn)`` bzw. ``while (!lampeAn)`` verwenden.

### For-Schleifen (auch Zählschleifen)
Wie ihr alternativer Name bereits suggeriert, eignen sich for-Schleifen dafür, eine Reihe von Operationen begrenzt oft auszuführen. Das könnte zum Beispiel das fahren von fünf Feldern sein o.ä. Ihr Syntax ist allerdings etwas komplizierter, da wir eine Zählvariable, die Bedingung und die Zähloperation im Schleifen-Kopf festlegen müssen. Das sieht dann zum Beispiel so aus:
```Java
for (int i = 0; i < 10; i++)
{
	fahre();
}
```
Hier initialisieren wir die Zählvariable **i** mit dem Wert **0** (*int i = 0*), setzen als Bedingung, dass der Wert von **i** kleiner als **10** ist (*i < 10*) und addieren nach Durchlaufen des Code-Blocks immer **1** zu der Zähvariable (*i++* auch *i += 1*). Alternativ kann für **10** auch eine bereits initialisierte Variable verwendet werden. Diese könnte dann zum Beispiel als Methodenparameter beim Aufruf der Methode mitgegeben werden. Hier ein Beispiel:
```Java
public void fahreNFelder(int anzahlFelder)
{
	for (int i = 0; i < anzahlFelder; i++)
	{
		fahre();
	}
}
```
Das Aufrufen dieser Methode mit dem Parameter 5 (``fahreNFelder(5);``) würde das Objekt fünf "Felder fahren" lassen.

Auch hier wollen wir das "Übersetzer-Prinzip" anwenden. Unser Beispielsatz:
**Für die Variable i, wenn sie kleiner als 15 ist, addiere 1 und fahre jedes mal**
+ 1. Übersetzen (ins Englische)
	-> For the variable i, if it is smaller than 15, add 1 and move every time.
+ 2. Kürzen von sprachspezifischen Eigenheiten
	-> for i, i smaller 15, add 1, move
+ 3. Übertragung in Java-Syntax (oder andere Sprachen)
```Java
for (int i = 0; i < 15; i++)
{
	fahre();
}
```
Da for-Schleifen etwas abstrakter sind, bedarf es hier einer etwas ausführlicheren Erklärung.
Unsere Zählvariable **int i = 0** finden wir in unserem Satz als "Für die Variable i" wieder. Da wir beim Zählen von Natur aus immer bei **0** anfangen, machen wir das auch hier beim Computer. Dann kommt unsere Bedingung, also **i < 15**. Das bedeutet nichts anderes als "i ist kleiner als 15", was wir in unserem Satz als "wenn sie kleiner als 15 ist" wiederfinden. **i++** ist die Kurzschreibweise für **i = i + 1**, also einer einfachen Addition. Das ist unsere "Zähloperation". Schließlich ist der Code, den wir ausführen wollen (also zu "fahren", wohin auch immer), im Code-Block als Methodenaufruf wiederzufinden.

## <span style="color:#5ABA70">Verweise</span>
+ [[Erklärungen/Klammern]]
+ [[Erklärungen/Variablen]]
+ [[Erklärungen/Datentypen]]
+ [[Erklärungen/If und Else]]
+ [[Aufgaben/While und For]]