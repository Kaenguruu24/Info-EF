## Einleitung
Klassen und Objekte sind ein wichtiger Teil von den sogenannten objektorientierten Programmiersprachen wie Java. Wie ihr Name schon sagt, basieren sie auf **Objekten**.
Die sogennanten **Klassen** dienen mehr oder weniger als Verhaltensanleitung für
diese Objekte. Die sind dann **Instanzen** dieser Klasse.

## Zwei Vergleiche
Um das Konzept von Klassen und Objekten zu verstehen, hilft es, diese Beziehung auf etwas weniger abstraktes zu projizieren. Im Folgenden betrachten wir nun zwei Beispiele, an denen der Unterschied zwischen Klassen und Objekten eindeutig wird. 
### 1. Tierarten
Stellt euch vor, ihr seid in der Grundschule und müsst in "Sachkundeunterricht", oder wie auch immer das damals hieß, ein Plakat zu Wölfen erstellen. Jetzt stellt sich für euch die Frage, was ihr auf dem Plakat an Informationen darstellen wollt. Vielleicht die Lebenserwartung, Rudelverhalten, Beute, etc. Das würde dann vielleicht etwa so aussehen:

+ Alter: Männchen bis 15 Jahre, Weibchen bis 13
+ Gewicht: Männchen etwa 20kg, Weibchen bis zu 30kg
+ Beute: Rehe, Vögel

Dieses Plakat stellt in unserer Analogie eine Klasse dar, denn es beschreibt **generelle Eigenschaften und Verhaltensweisen** von Wölfen. Jetzt nehmen wir an, ihr habt einen Wolf mit in den Unterricht genommen. Der ist 8 Jahre alt, hat von euch zum Frühstück eine Elster bekommen, weil er keine Rege mag und wiegt 18kg. Ganz unabhängig davon, dass es eine sehr schlechte Idee ist, einen Wolf mit in den Unterricht zu nehmen, sollte euch auffallen, dass es sich hierbei um ein Tier von der Tierart Wolf handelt, das aber konkrete "Werte" bzw. Eigenschaften hat (Alter, Gewicht, etc.). Und genau diesen Individualismus kennzeichnet **Objekte**. In einem Wolfsrudel gibt es mehrere Objekte (die einzelnen Wölfe) mit jeweils verschiedenen Eigenschaften (oder Attributen im Programmier-Kontext) - aber es sind alles Wölfe. Im Grunde verhalten sie sich also ähnlich wenn nicht sogar gleich.

### 2. Gesellschaft
Dieser Vergleich ist etwas ungewöhnlich, aber funktioniert trotzdem recht gut. Wir Menschen leben in einer Gesellschaft, die gewisse Verhaltensweisen für jeden Menschen definiert. So muss sich (eigentlich) jeder an die Verkehrsordnung halten und wer etwas im Geschäft kauft, muss dafür auch bezahlen. Jetzt ist es aber so, dass wenn ihr in der Stadt unterwegs seid, ganz viele unterschiedliche Menschen seht. Sie unterscheiden sich in ihrem Aussehen, Charackter, wie sie sich gegenüber dir Verhalten, etc. Jede Person einer Gesellschaft ist eine Instanz der von der Gesellschaft als "Standard-Mensch" definierten Klasse.

## Implementation
Im letzten Schritt wollen wir nun zumindest so tun, als würden wir für eine Staubsauger-Roboterfirma die Roboter programmieren. Dafür müssen wir nun zuerst eine Klasse schreiben, die das Verhalten eines solchen Roboters definiert:

```Java
public class Roboter
{
	// Ein paar Variablen, die in diesem Kontext unwichtig sind
	public int botID = 0;
	public boolean isActive = false;
	public String name = "";

	// Der Konstruktor. Wenn wir ein neues "Roboterobjekt" erschaffen wollen, benutzen wir 'roboter = new Roboter(1234, "Timmy")'
	public Roboter(int ID, String botName)
	{
		botID = ID;
		name = botName;
	}

	// Diese Funktion säubert das Zimmer. Die genaue Funktionsweise ist irrelevant
	public void zimmerSaugen()
	{
		aktiviereMotor();
		fahreZimmerAb();
		fahreZuLadestation();
		deaktiviereMotor();
	}
}
```
Diese Klasse hat ein paar Variablen, den Konstruktor und eine Funktion zum Staubsaugen des Zimmers. Wenn wir jetzt einen Server hätten, mit dem alle Staubsaugerroboter kommunizieren, würden wir dort ganz oft solche Dinge finden:
```Java
Roboter neuerRoboter = new Roboter(5, "as3rfkdf2");
```
Hier erstellen wir ein neues Objekt und speichern die Referenz in der Variable "neuerRoboter". Dieses Objekt hat auch die Funktion "zimmerSaugen". Aber die ID ist hier die 5 und der Roboter heißt "as3rfkdf2" - nicht sehr leserlich, aber einzigartig. 

## <span style="color:#5ABA70">Verweise</span>
+ [[Erklärungen/Datentypen]]
+ [[Aufgaben/Klassen und Objekte]]
