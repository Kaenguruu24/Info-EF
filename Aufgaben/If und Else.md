### A1
#### 1.1 (L1)
Welche Aufgabe erfüllt das if-Statement?
#### 1.2 (L1)
Was bedeutet das Keyword **else**?

### A2
#### 2.1 (L2)
Formuliere einen Satz, der eine Bedingung enthält, die aus einer Variable und einem Wert besteht.
#### 2.2 (L3)
Erläutere, welche Aufgabe das if-Statement hier erfüllt und wann die angegebene Bedingung erfüllt ist.
```Java
if (alter > 14)
{
	gibEnergydrink();
}
```
#### 2.3 (L3)
Implementiere die folgende Bedingung als Java-Code:
**Wenn die Variable "motorAn" wahr ist, schalte das Navi an**

*Hinweis: Die konkrete Implementierung von Methoden ist nicht erforderlich, es geht ausschließlich um den Syntax eines If-Statements. Es dürfen nicht-definierte Funktionen aufgerufen werden.*

### A3
#### 3.1 (L2/L3)
Schreibe aus dem folgenden Java-Code alle if-/else if-/else-Bedingungen heraus. Notiere ihre Funktion und wann sie "auslösen".
```Java
public void starteFahrzeug()
{
	if (tankFüllStand > 50)
	{
		starteMotor();
	} else if (tankFüllStand > 0)
	{
		starteMotor();
		zeigeWarnung("Tankfüllstand unter 50%!");
	} else
	{
		zeigeFehler("Tank leer!");
	}
}
```
#### 3.2 (L3)
Implementiere eine Methode, die das folgende Bedingungskonstrukt umsetzt:
**Wenn die Variable "akkuStand" größer oder gleich 50 ist, setze die Helligkeit auf 100%, sonst, wenn die Variable "akkuStand" größer oder gleich 20 ist, setze die Helligkeit auf 50%, sonst setze die Helligkeit auf 5%**

## <span style="color:#5ABA70">Verweise</span>
+ [[Erklärungen/If und Else]]
+ [[Erklärungen/Datentypen]]
+ [[Erklärungen/Klammern]]
+ [[Erklärungen/Variablen]]