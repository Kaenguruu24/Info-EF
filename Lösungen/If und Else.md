### A1
#### 1.1 (L1)) <span style="color:#ffaaaa">LÖSUNG</span>
Das if-Statement überprüft, ob die in den runden Klammern angegebene Bedingung wahr ist. Dann führt sie den Code im Code-Block aus. Die Bedingungen ähneln mathematischen Gleichungen bzw. Gleichsetzungen.
#### 1.2 (L1)) <span style="color:#ffaaaa">LÖSUNG</span>
Fügt man das Keyword **else** am Ende des Code-Blocks eines if-Statements an, wird der Code-Block des **else**-Keywords ausgeführt, sofern die Bedingung im **if**-Statement nicht erfüllt wurde.

### A2
#### 2.1 (L2) <span style="color:#aaaaff">Mögliche Lösung</span>
Wenn die Variable "müdigkeit" größer oder gleich 80 ist, gehe schlafen.
#### 2.2 (L3)) <span style="color:#ffaaaa">LÖSUNG</span>
Das **if**-Statement überprüft hier, ob das angegebene Alter höher als 14 ist, und gibt dann einen Energydrink aus.
#### 2.3 (L3)) <span style="color:#ffaaaa">LÖSUNG</span>
**Wenn die Variable "motorAn" wahr ist, schalte das Navi an**
+ 1. Übersetzen (ins Englische)
	-> If the variable "motorAn" is true, start the navigation system
+ 2. Kürzen von sprachspezifischen Eigenheiten
	-> If "motorAn" true, start navi
+ 3. Übertragung in Java-Syntax (oder andere Sprachen)
```Java
// (motorAn == true) gleichbedeutend mit (motorAn)
if (motorAn)
{
	starteNavi();
}
```

*Hinweis: Die konkrete Implementierung von Methoden ist nicht erforderlich, es geht ausschließlich um den Syntax eines If-Statements. Es dürfen nicht-definierte Funktionen aufgerufen werden.*

### A3
#### 3.1 (L2/L3)) <span style="color:#ffaaaa">LÖSUNG</span>
+ IF: Wenn der Tankfüllstand höher als 50 ist, wird der Motor gestartet.
+ ELSE IF: Wenn der Tankfüllstand niedriger als 50 ist, aber höher als 0, wird der Motor gestartet und eine Warnung angezeigt, dass der Tankfüllstand niedriger als 50% ist.
+ ELSE: Wenn der Tankfüllstand gleich 0 ist, wird mit einem Fehler angezeigt, dass der Tank leer ist.

#### 3.2 (L3)) <span style="color:#ffaaaa">LÖSUNG</span>
Implementiere eine Methode, die das folgende Bedingungskonstrukt umsetzt:
**Wenn die Variable "akkuStand" größer oder gleich 50 ist, setze die Helligkeit auf 100%, sonst, wenn die Variable "akkuStand" größer oder gleich 20 ist, setze die Helligkeit auf 50%, sonst setze die Helligkeit auf 5%**
```Java
// Methodenparameter freiwillig, gibt trotzdem einen Pluspunkt
public void reguliereHelligkeit(int akkuStand)
{
	if (akkuStand >= 50)
	{
		setzeHelligkeit(100);
		// Alternativlösung
		helligkeit = 100;
	} else if (akkuStand >= 20)
	{
		setzeHelligkeit(50);
		// Alternativlösung
		helligkeit = 50;
	} else
	{
		setzeHelligkeit(5);
		// Alternativlösung
		helligkeit = 5;
	}
}
```

## <span style="color:#5ABA70">Verweise</span>
+ [[Erklärungen/If und Else]]
+ [[Erklärungen/Datentypen]]
+ [[Erklärungen/Klammern]]
+ [[Erklärungen/Variablen]]