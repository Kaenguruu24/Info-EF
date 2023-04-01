## Einleitung
Bis zu einem gewissen Punkt geht es auch ohne, aber irgendwann sind sie unausweichlich: Bedingungen. Ohne if könntet würdet ihr schon nach kürzester Zeit scheitern, weil euch keine kaum andere Möglichkeiten bleiben, den Wert einer Variable o.ä. zu überprüfen.

## Wenn-Dann-Sonst
Das ist die (deutsche) Kurzzusammenfassung von if und else. Dabei stellt **if** den *Wenn-Dann*-Teil dar und **else** entspricht dem *sonst*. Ein guter Weg, um Bedinungen zu verstehen, ist es, mit einem Satz zu beginnen, und ihn dann systematisch immer weiter zu kürzen. Unser Beispiel:

### IF (isoliert)
**Wenn die Variable alter größer oder gleich 18 ist, erstelle einen Ausweis**
Jetzt befolgen wir mehrere Schritte, um den Satz zu einer Bedingung umzuwandeln.
+ 1. Übersetzen (ins Englische)
	-> If the variable "alter" is bigger or equal to 18, create a new identification card
+ 2. Kürzen von sprachspezifischen Eigenheiten
	-> If "alter" bigger or equal 18, new identification card
+ 3. Übertragung in Java-Syntax (oder andere Sprachen)
	```Java
	if (alter >= 18)
	{
		Ausweis meinAusweis = new Ausweis(name, alter, adress);
	}
	```
Hier benutzen wir das Keyword **if**, um dem Computer zu signalisieren, dass in den folgenden **runden** Klammern eine Bedingung folgt. Die besteht aus drei Teilen:
+ Variable *(alter)*
+ Operator *('>=' / größer oder gleich)*
+ Wert *(18)*
Danach folgen die *{}* Geschweiften Klammern und zwischen den beiden der Code, der ausgeführt werden soll, wenn die Bedingung wahr ist.

### IF / ELSE (kombiniert)
Jetzt kommt noch etwas dazu: Die **else**-Anweisung. Die Schritte bleiben die selben:
**Wenn die Variable alter größer oder gleich 18 ist, erstelle einen Ausweis, sonst sage "Du bist zu jung!"**
+ 1. Übersetzen (ins Englische)
	-> If the variable "alter" is bigger or equal to 18, create a new identification card or else say "Du bist zu jung!"
+ 2. Kürzen von sprachspezifischen Eigenheiten
	-> If "alter" bigger or equal 18, new identification card, else say "Du bist zu jung!"
+ 3. Übertragung in Java-Syntax (oder andere Sprachen)
	```Java
	if (alter >= 18)
	{
		Ausweis meinAusweis = new Ausweis(name, alter, adress);
	} else
	{
		System.out.println("Du bist zu jung!");
	}
	```
Auch hier starten wir mit if, fügen allerdings auch das Keyword **else** hinzu. Dort benötigen wir keine *()* runden Klammern, da wir keine Bedingung angeben müssen.

### IF / ELSE IF / ELSE (kombiniert)
Als letztes wollen wir uns noch die sog. **else if**-Anweisung anschauen. Sie bedeutet soviel wie "wenn a, dann b, sonst wenn c, dann d, sonst e". Wir erweitern wieder unser Beispiel:
**Wenn die Variable alter größer oder gleich 18 ist, erstelle einen Ausweis, sonst, wenn die Variable alter größer als 14 ist, sage "Du darfst bald einen Ausweis haben!", sonst sage "Du bist zu jung!"**
+ 1. Übersetzen (ins Englische)
	-> If the variable "alter" is bigger or equal to 18, create a new identification card or else if the variable "alter" is bigger than 14, say "Du darfst bald einen Ausweis haben!" or else say "Du bist zu jung!"
+ 2. Kürzen von sprachspezifischen Eigenheiten
	-> If "alter" bigger or equal 18, new identification card, else if "alter" bigger 14 say "Du darfst bald einen Ausweis haben!", else say "Du bist zu jung!"
+ 3. Übertragung in Java-Syntax (oder andere Sprachen)
	```Java
	if (alter >= 18)
	{
		Ausweis meinAusweis = new Ausweis(name, alter, adress);
	} else if (alter > 14)
	{
		System.out.println("Du darfst bald einen Ausweis haben!");
	} else
	{
		System.out.println("Du bist zu jung!");
	}
```
Wie in den vorherigen Beispielen haben wir eine **if** und **else** Anweisung, diesmal allerdings auch **else if**. Diese braucht genauso wie die **if**-Anweisung eine Bedingung in *()* runden Klammern.

## <span style="color:#5ABA70">Verweise</span>
+ [[Erklärungen/Klammern]]
+ [[Erklärungen/Variablen]]
+ [[Aufgaben/If und Else]]