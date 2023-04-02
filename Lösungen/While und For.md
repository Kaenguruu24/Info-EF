### A1
#### 1.1 (L1) <span style="color:#ffaaaa">LÖSUNG</span>
Die **do-while**-Schleife ist eine sog. nachprüfende Schleife, d.h. es wird zuerst der Code-Block ausgeführt, bevor die Bedingung überprüft wird. **do-while**-Schleifen werden also **immer** mindestens ein mal ausgeführt.
#### 1.2 (L2) <span style="color:#ffaaaa">LÖSUNG</span>
Hier eignet sich eine **while**-Schleife besser, da sie für einen unbestimmten Zeitraum laufen kann.
#### 1.3 (L1) <span style="color:#ffaaaa">LÖSUNG</span>
Die **for**-Schleife eignet sich hier, da wir eine limitierte, aber trotzdem dynamische Anzahl an Ausführungen haben.
#### 1.4 (L3) <span style="color:#ffaaaa">LÖSUNG</span>
Implementiere die Methode in der folgenden Klasse:
```Java
public class Backofen
{
	private boolean istOffen = false;

	public Backofen()
	{
	}

	// Methode für 1.4:
	public void oeffneNMal(int anahlOeffnungen)
	{
		for (int i = 0; i < anzahlOeffnungen; i++)
		{
			oeffnen();
			warte(5); // wartet 5 Sekunden. Nicht zwingend notwendig für die Aufgabe!
			schliessen();
		}
	}

	public void oeffnen()
	{
		istOffen = true;
		oeffneTuer();
	}
	public void schliessen()
	{
		istOffen = false;
		schliesseTuer();
	}
}
```

## <span style="color:#5ABA70">Verweise</span>
+ [[Erklärungen/While und For]]
+ [[Erklärungen/Datentypen]]
+ [[Erklärungen/Klammern]]
+ [[Erklärungen/Variablen]]