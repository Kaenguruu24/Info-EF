### A1
#### 1.1 (L1)
Worin besteht der Unterschied zwischen einer **while**-Schleife und einer **do-while**-Schleife?
#### 1.2 (L2)
Du möchtest einen Timer solange erhöhen, wie ein Knopf gedrückt ist. Solltest du eine while-Schleife oder eine for-Schleife benutzen? Begründe.
#### 1.3 (L1)
Dein automatischer Ofen soll, abhängig vom Gericht, unterschiedlich oft auf- und wieder zugehen, um den Wasserdampf rauszulassen. Begründe, warum du hier eine for-Schleife anstatt einer while-Schleife verwenden solltest.
#### 1.4 (L3)
Implementiere die Methode in der folgenden Klasse:
```Java
public class Backofen
{
	private boolean istOffen = false;

	public Backofen()
	{
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