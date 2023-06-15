## Einleitung
Wir haben bereits besprochen, dass Informatiker ihre Daten in Variablen speichern. Die Form, die ihr im Unterricht bis jetzt kennengelernt habt, hat allerdings einen entscheidenden Nachteil: Wenn ihr viele Daten speichern wollt, die alle gleich verwendet werden (z.B. die Adressen eurer Freunde), dann ist es ab einem gewissen Zeitpunkt sehr unpraktisch, wenn man für jede einzelne Adresse eine neue Variable erstellen müsstet. Denn dann wäre auch die Verwendung deutlich komplizierter. Dafür verwenden wir deshalb Arrays, zu Deutsch auch "Listen" genannt.

### Ein Problem
Angenommen, ihr wollt die Adressen eurer Freunde speichern. Das könntet ihr z.B. so:
```Java
private String AdresseKevin = "Sabbelstraße 42";
private String AdresseTim = "Mariannengraben 12";
private String AdresseOtto = "Auf der Wiese 3";
private String AdresseAnna = "Unter der Brücke 66";
```
Doch wenn ihr nun die Adresse eines neuen Freundes hinzufügen wollt, müsst ihr eine neue Variable erstellen:
```Java
private String AdresseNeuerFreund = "Neue Adresse";
```
Das wird auf Dauer anstrengend. Und jetzt stellt euch vor, ihr würdet eine Methode schreiben wollen, die alle Adressen ausdruckt:
```Java
public void alleAdressenDrucken()
{
	System.out.println(AdresseKevin);
	System.out.println(AdresseTim);
	System.out.println(AdresseOtto);
	System.out.println(AdresseAnna);
}
```
Jedes Mal, wenn ihr einen neuen Freund hinzufügt, müsstet ihr diese Methode ändern. Das mag auf diesem Maßstab zwar mehr oder weniger irrelevant sein, aber jetzt stellt euch so etwas mit einer Freundesliste in einem Videospiel vor, beispielsweise Call of Duty. Dann müssten die Entwickler für jede Person, sobald diese einen Freund hinzufügt oder entfernt, den Code ändern und dann an **alle** Spieler ein Spielupdate schicken, damit es keine Probleme gibt. Das wäre absolut unmöglich.
### Die Lösung
Um dieses Problem zu beheben, haben sich Programmierer Arrays ausgedacht. Diese sind im Prinzip nichts anderes als Listen, in denen wir nur Einträge eines bestimmten Typs speichern:
```Java
private String[] alleAdressen;
```
Diese Liste können wir dann beim Programmstart initialisieren:
```Java
public void starteProgramm()
{
	alleAdressen = new String[4];
	alleAdressen[0] = "Sabbelstraße 42";
	alleAdressen[1] = "Mariannengraben 12";
	...

}
```
Dadurch sieht unsere Methode dann so aus:
```Java
public void alleAdressenDrucken()
{
	for (int i = 0; i < alleAdressen.length; i++)
	{
		System.out.println(alleAdressen[i]);
	}

}
```

### Stück für Stück erklärt
Das war jetzt viel neuer Syntax auf einmal, deshalb werden wir das ganze jetzt Stück für Stück durchgehen, angefangen bei der Deklaration. Arrays haben, da sie in gewisser Weise auch eine Art Datentyp sind, ersteinmal relativ viel mit den euch bereits bekannten Datentypen gemeinsam. Bei ihrer Deklaration bestimmen wir die Sichtbarkeit (private, public, protected), die Art der Einträge und den Namen. 

### Listen erstellen
```Java
Sichtbarkeit Datentyp[] Bezeichner;
```

```**Vordefinierte Länge**
```Java
Sichtbarkeit Datentyp[Länge] Bezeichner;
```

Im nächsten Schritt *könnt* ihr das Array initialisieren, wobei es hier zwei Möglichkeiten gibt:
**Direkte Wertzuweisung**
```Java
private int[] myIntArray = {1, 2, 3, 4, 5};
```
**Datentyp-Initialisierung**
```Java
private int[] myIntArray = new int[5];
```
Hier wird die Länge des Arrays durch die **5** in den eckigen Klammern definiert. Bei der direkten Wertzuweisung wird ein Array erschaffen, das die in den geschweiften Klammern angegebenen Werte hat.  Bei der Datentyp-Initialisierung wird das Array mit der **null-Value** des entsprechenden Datentyps gefüllt:
| Index | Direkt | Datentyp |
| ------ |  ----- | ----------- |
| 0 | 1 | 0 |
| 1 | 2 | 0 |
| 2 | 3 | 0 |
| 3 | 4 | 0 |
| 4 | 5 | 0 |

### Zugriff
Hier wird es nun etwas knifflig. Weil Programmierer beim **Zählen immer mit 0** anfangen, ist der Index des ersten Eintrags also 0. Wenn wir also den Eintrag, den wir direkt mit 4 initialisiert haben, auslesen wollen, müssen wir auf den Index 3 zurückgreifen. Der Syntax ist recht einfach:
```Java
eineVariable = Bezeichner[Index];
Bezeichner[Index] = eineVariable;
```
In der ersten Zeile speichern wir den Wert des Arrays an der Stelle *Index* in *eineVariable*. Die Zweite Zeiile funktioniert genau umgekehrt; wir speichern den Wert von *eineVariable* im Array *Bezeichner* an der Stelle *Index*.

### Durch ein Array gehen
Die häufigste Verwendungsart von Arrays hat meist zur Folge, dass man zu irgendeinem Zeitpunkt einfach durch alle Einträge durch geht und dann irgendetwas mit ihnen macht. Um dies so unkompliziert wie möglich zu machen, benutzen wir for-(Zähl-) Schleifen. Dabei gibt es dann diesen "Standard-Syntax":
```Java
for (int i = 0; i < myArray.length; i++)
{
	myArray[i] = i;
}
```
Hier gibt es nun folgendes zu beachten:
+ **Array.length** gibt die Länge des Arrays zurück. In anderen Programmiersprachen ist es mal eine Funktion, also **Array.length**, oder auch **len(Array)**.
+ Da die Länge "normal" gezählt ist, müssen wir als Zählbedingung **i < length** verwenden, da wir somit nur bis zum **Index (length - 1)** gehen. Wenn ihr an dieser Stelle **<=** verwendet, wird das Programm mit dem Fehler *Index out of Bounds* crashen. Mehr dazu siehe [[Häufige Fehlermeldungen]]
+ Wir verwenden ``myArray[i]``, um den Eintrag mit dem Index **i** zu verändern.