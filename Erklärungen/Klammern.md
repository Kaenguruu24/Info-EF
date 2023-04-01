## Einleitung
Zuweilen einer der verwirrensten Teile des Programmierens sind die Klammern. Gleich drei verschiedene Typen gibt es:
+ *()* runde Klammern
+ *[]* eckige Klammern
+ *{}* geschweifte Klammern
Um da den Überblick zu behalten, findet ihr hier eine kurze Erklärung.

### () runde Klammern
Runde Klammern benötigt ihr zunächst einmal, wenn ihr Methoden aufruft, egal ob eure eigenen oder bereits "vorinstallierte", oder wenn ihr die Parameter für eine Methode festlegt:
```Java
meineMethode();
meineZweiteMethode("Kekse", 50);

public void meineDritteMethode(String pProdukt, int anzahl, float preis)
{
	// Irrelevant
	blabla();
}
```
Sie werden benötigt, um die Liste der Parameter anzugeben, wobei **()** nichts anderes als "keine Parameter" bedeutet. Außerdem sind sie bei komplexeren mathematischen Operationen hilfreich, um wie in der Mathematik selbst die **Reihenfolge der Operationen** festzulegen. Das könnte zum Beispiel so aussehen:
```Java
int produktAusDerSummeVonAUndBMitDemFaktorC = (a + b) * c;
```
Wie ihr es aus Mathe kennt, würden fehlende Klammern nicht "a plus b und das Ergebnis davon mal c" ergeben, sondern "a plus das Ergebnis von b mal c".
Zuletzt sind sie auch bei Schleifen und Bedingungen von Nöten, um deren "Parameter" darzustellen:
```Java
if (alter >= 18)
{
	// Kram
}

for (int i = 0; i < 10; i++)
{
	// Noch mehr Kram
}
while (timer > 50)
{
	// Noch mehr noch mehr Kram
}
```

### {} geschweifte Klammern
Geschweifte Klammern benötigen wir immer dann, wenn wir einen sog. Code-Block definieren. Als Code-Block bezeichnen wir die Aneinanderreihung beliebig vieler Anweisungen:
```Java
{ // Beginn eines Code-Blocks
	sageHallo();
	frage("Wie heißt du?");
	frage("Wie alt bist du?");
	antworte("Das ist schön.");
} // Ende eines Code-Blocks
```
Auch bei sog. Arrays, also Listen, braucht ihr sie:
```Java
int[12] meineListe = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12};
```

### [] eckige Klammern
Eckige Klammern braucht ihr, wenn ihr mit Listen arbeitet. Das erkennt ihr schon, wenn ihr eine Liste als Variable initialisiert:
```Java
int[] meineListe;
int[5] meineZweiteListe = {1, 2, 3, 4, 5}
```
Oder wenn ihr auf solch eine Liste zugreift:
```Java
// Zeigt den fünften Eintrag in der Konsole an.
print(meineListe[4]);
```
Davon abgesehen braucht ihr sie nur selten.