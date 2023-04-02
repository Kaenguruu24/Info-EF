### A1
Tim hat eine Klasse "Person", die er für das Erfassen von Daten der Nutzer seiner Android-App verwendet. Er möchte folgende Daten speichern:
+ Name
+ Alter
+ Adresse
+ Ob die Person Haustierbesitzer ist
#### 1.1 (L3)
Füge die Daten nun als Variablen in der unten stehenden Klasse hinzu und initialisiere sie mit einem angemessenen Startwert.
#### 1.2 (L3)
Erweitere zusätzlich den Konstruktor um die Daten beim Erstellen einer neuen Klasse als Konstruktorparameter zu übergeben.

Personen-Klasse:
```Java
public class Person
{
	// Konstruktor
	public Person()
	{
	}
	
	public void sendeNachricht(String Inhalt)
	{
		Message newMessage = new Message(Inhalt);
		newMessage.encrypt("asl3-3fj3-933n-aap3");
		newMessage.send();
	}
}
```

## <span style="color:#5ABA70">Verweise</span>
+ [[Allgemein/Hinweise zu Aufgaben]]
+ [[Erklärungen/Variablen]]
+ [[Erklärungen/Datentypen]]
