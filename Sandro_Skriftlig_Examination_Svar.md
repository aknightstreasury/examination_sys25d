# Skriftlig Examination - Introduktion till C#

**Kursnamn**: Introduktion till C#  
**Examination av**: Läranderesultat 1, 2 och 3 (Kunskaper)  
**Betyg**: Icke Godkänt (IG) eller Godkänt (G)  
**Tidsåtgång**: Ca 3-4 timmar  
**Inlämning**: Senast söndag den 9 november (23:59)  
**Format**: Kopiera den här filen och skriv svaren här inne.

---

**Sandro Gramner**:

---

## Instruktioner

- Svara på alla frågor med egna ord
- Det är inte tillåtet att använda AI i sina svar.
- Alla inlämningar kontrolleras i ett antiplagiat-verktyg. Fusk kan leda till disciplinära åtgärder och risk för avstängning.
- Förklara tydligt och koncist - inga långa utläggningar krävs
- Ge korta kodexempel endast där det efterfrågas (oftast räcker 1-3 rader)
- Försök att använda korrekt terminologi.
- Det är okej att använda kursmaterial och anteckningar

---

## Del 1: Objektorienterad programmering i C# (Läranderesultat 1)

### Fråga 1 - Grundläggande OOP

**Vad är objektorienterad programmering?** Förklara med egna ord vad OOP innebär och ge minst två fördelar med att använda OOP.

Mitt SVar:
Det står för Objektorienterad programmering. Ett sätt att skriva kod där man använder klasser och objekt för att organisera program. Ett objekt kan innehålla både data och metoder.

Exempel på fördelar med OOP är:
Återanvändning: Man kan återanvända kod genom att skapa flera objekt från samma klass.
Strukturad: Koden blir lättare att organisera, förstå och underhålla.

---

### Fråga 2 - Klasser och Objekt

**.**
a) Förklara skillnaden mellan en klass och ett objekt, använd gärna en analogi från verkligheten för att illustrera din förklaring.
b) Vad innebär det om en klass benämns static? Ex: `public static class File`

Svar A) En klass är som en mall som beskriver vilka egenskaper och metoder något ska ha. Ett objekt är en instans av den klassen.

Om man tar en bil som exempel så beskriver klassen bilen på detta sätt:
till exempel bilens färg, bilens top hastighet och alla specifikationer som följer med bilen.
Ett objekt däremot syftar på en specifik bil, till exempel en röd Volvo.

Svar B) En static klass kan inte instansieras, vilket betyder att man inte kan skapa objekt av den med new. Dess medlemmar används direkt via klassnamnet och måste vara statiska. Statiska klasser passar exempelvis för hjälpfunktioner som inte behöver lagra separat data för varje objekt.

---

### Fråga 3 - Konstruktorer

**Vad är en konstruktor och vad används den till?** Förklara vad som händer när man skapar ett nytt objekt med `new` keyword.

Svar: En konstruktor är en metod som körs när man skapar ett nytt objekt. Den används för att ge objektet ett startläge och tilldela värden.

När man använder nyckelordet new skapar man ett objekt, där minne reserveras för det och dess konstruktor körs.

ett exempel på detta i kod skulle vara:

public class Person
{
    public string Name;
    public Person(string name) { Name = name; }
}

När man skriver Person p = new Person("Anna"); skapas ett objekt och namnet sätts till Anna.

---

### Fråga 4 - Properties och Fields

**Förklara skillnaden mellan ett field och en property i C#.** Ge exempel på när man bör använda respektive.

Svar fråga 4:
"field" är en variabel som lagrar data direkt i en klass. "Property" däremot används för att komma åt eller ändra data på ett kontrollerat sätt.

Exempel på detta skulle va att:

private int age;
public int Age { get; set; }

"Fields" används ofta för intern lagring av data, medan "properties" används när data ska vara tillgänglig för andra delar av programmet.

Properties kan också innehålla logik, till exempel för att kontrollera att ett värde är giltigt innan man sparar det.
---

### Fråga 5 - Inkapsling

**Vad är inkapsling (encapsulation) och varför är det viktigt?** Förklara skillnaden mellan `private` och `public`, och när man bör använda vad.

Inkapsling innebär att man skyddar ett objekts data och kontrollerar hur andra delar av programmet får komma åt den. Det gör koden säkrare och minskar risken för att data ändras på fel sätt.

" private " innebär att man bara kan nå grej direkt från den klass där den är deklarerad. Men om den däremot skulle vara klassad under "public" så innebär de att en sak kan nås från andra delar av programmet, förutsatt att objektet eller klassen är tillgänglig det vill säga.

Man använder oftast private för intern data, och public för metoder och properties som andra delar av programmet behöver använda.
---

### Fråga 6 - Metoder

**Förklara följande:**

a) Vad är skillnaden mellan en metod som returnerar något (t.ex. `int`) och en `void` metod?  
b) Vad innebär det att en metod är `static`?

Svar fråga A)
En metod som returnerar ett värde skickar tillbaka ett resultat med hjälp av "return.
En void-metod däremot utför en uppgift utan att returnera några värden till dig.

Exempelpå detta skulle vara att:

int Add(int a, int b) => a + b;
void SayHello() => Console.WriteLine("Hej!");

Den första metoden returnerar summan, medan den andra skriver ut ett hälsningsmeddelande.

Svar till B)
Om en metod är klassad som "static" så tillhör den klassen i stället för ett specifikt objekt. Den kan anropas direkt via klassnamnet utan att man behöver skapa ett objekt.

Exempel: Math.Max(5, 10) returnerar det större av de två talen.
---

## Del 2: Applikationstyper (Läranderesultat 2)

### Fråga 7 - Applikationstyper i .NET

**C# och .NET kan användas för att bygga olika typer av applikationer.**

a) Nämn minst tre olika typer av applikationer man kan bygga med C# och .NET (t.ex. console)  
b) Beskriv kort vad dessa applikationstyper har för syfte.

Tre exempel skulle nog vara:

Konsolapplikationer.
Webbapplikationer.
Desktopapplikationer.

Om jag ska beskriva dess syften skulle jag säga att Konsolapplikationer: Körs i en terminal och används exempelvis för enklare program eller verktyg och eventuellt inom automatisering.
Webbapplikationer: Körs på en webbserver och används för webbplatser och på olika webbtjänster.

Desktopapplikationer: kan man Installera på sin dator och används för program med grafiska gränssnitt, exempelvis ett program för att hantera olika dokument.

---

### Fråga 8 - Konsolapplikationer

**Vi har fokuserat på konsolapplikationer (Console Application) i kursen.**

a) Vad är en konsolapplikation?  
b) Ge ett exempel på när en konsolapplikation kan vara lämplig att använda.

En konsolapplikation är ett program som körs i en terminal eller kommandotolk. Användaren kan vanligtvis skriva in information och läsa resultat som visas som text.

Om jag ger ett exempel på när en konsolapplikation är lämplig skulle jag säga t.ex att en konsolapplikation passar exempelvis för ett program som räknar ut medelvärdet av en mängd tal. Det kan också passa för mindre verktyg som automatiserar uppgifter eller bearbetar filer.
---

## Del 3: Datatyper i C# (Läranderesultat 3)

### Fråga 9 - Primitiva Datatyper

**Beskriv följande datatyper och när man använder dem:**

a) `int`  
b) `double`  
c) `string`  
d) `bool`

Förklara också skillnaden mellan `int` och `double`.

a) int
int använder man för att lagra heltal utan decimaler, exempelvis ålder, antal produkter eller antalet poäng, etc.

b) double
double används dock för att lagra tal med decimaler, exempelvis temperaturer, avstånd eller resultat från olika beräkningar.

c) string
En string används för att lagra text, exempelvis namn, adresser eller meddelanden.

d) bool

bool används för att lagra ett logiskt värde som: true eller false. 
Det används exempelvis i villkor för att kontrollera om något stämmer elle rinte

Å skillnaden mellan int och double är exempelvis att int lagrar heltal, medan double kan lagra tal med decimaler. int kan lagra siffran 5, medan double kan lagra 5,5.
---

### Fråga 10 - Stark typning

**C# är ett starkt typat språk, medan JavaScript är löst typat.**

a) Vad innebär det att ett språk är starkt typat?  
b) Ge ett exempel på en fördel med stark typning som du märkt av i C#.

Ett starkt typat språk har tydliga regler för vilka datatyper som man kan använda tillsammans.
Kodar man i C# måste man exempelvis ta hänsyn till om en variabel innehåller ett heltal, text eller ett "logiskt" värde.

exempel på en fördel med stark typning som jag märkte av när jag kodat i C# är att kompilatorn kan upptäcka många typfel innan programmet körs ^^. Och om jag exempelvis försöker skriva text direkt till en int-variabel får jag ett kompileringsfel. Det hjälper mig att hitta och rätta fel tidigare under arbetets gång.
---

### Fråga 11 - Arrays och Listor

**Förklara skillnaden mellan en array och en `List<T>` i C#.**

a) När bör man använda en array?  
b) När bör man använda en `List<T>`?  
c) Skriv ett kort kodexempel (1-3 rader) som visar hur man lägger till ett element i en `List<int>`.

Skilllnaden mellan demm är: en array har t.ex en fast storlek som bestäms när man skapar den. En List<T> kan däremot växa eller minska när man lägger till eller tar bort element i koden.

a)
ett bra exempel där jag tycker det passar att använde en array är när man vet hur många element som behövs, och att man vet att storleken inte behöver ändras nå på dem.

b)
En List<T> passar dock in när antalet element kan ändras under tiden ett program körs, exempelvis när man samlar in en användarens uppgifter.

c)
Såhär kan man använda sig utav List<int> funktionen:
List<int> numbers = new List<int>();
numbers.Add(10);

Koden skapar en lista med heltal och talet 10 läggs till.
---

### Fråga 12 - Dictionary

**Vad är en `Dictionary<TKey, TValue>` och när är den användbar?**

Förklara med egna ord och ge två exempel på scenarion där Dictionary är ett bra val (inget kodexempel krävs).

De är en samling som lagrar värden kopplade till olika unika nycklar. Man använder nyckeln för att snabbt hitta det värde som hörs till den.

exempel på när "dictionary" är användbart:

1) vid användaruppgifter: Man kan koppla ett användarnamn till information om användaren.

2) Produktpriser: Man kan koppla ett produktnamn eller produkt-ID till en produkts pris.

En Dictionary passar särskilt bra när man vill hitta ett värde utifrån en bestämd nyckel i stället för att söka igenom alla andra element.
---

### Fråga 13 - LINQ

**Vad är LINQ och vad används det till?**

Ge exempel på minst två LINQ-metoder du använt (t.ex. `Where`, `Select`, `OrderBy`, `Count`, etc.) och förklara kort vad de gör.

Det står för Language Integrated Query (LINQ) och de är en funktion man har i C# som gör det enklare att söka, filtrera, sortera och bearbeta data från exempelvis listor och arrayer.

Två exempel på LINQ-metoder är:

Where -> Filtrerar en samling så att endast element som uppfyller ett villkor blir kvar.
OrderBy -> Sorterar elementen efter ett angivet värde, vanligtvis i stigande ordning.

Exempel på detta:

List<int> numbers = new List<int> { 5, 2, 8, 1 };
var result = numbers.Where(n => n > 3).OrderBy(n => n);

Ovan filtreras listan så att endast tal större än 3 behålls. Därefter sorteras resultaten i stigande ordning, vilket ger 5, 8.
---

## Inlämning och Bedömning

### Format

- Ladda upp den här md filen med dina svar på It's learning senast den 9 november 2025. För de
  som hellre vill länka till sin Git får ni också göra det.

- Skriv ditt **namn** i dokumentet

### Bedömning

#### Godkänt (G)

För att få **Godkänt** krävs att du:

- Besvarar **alla 13 frågor**
- Visar förståelse för grundläggande koncept
- Ger tydliga förklaringar med egna ord
- Använder korrekt terminologi
- Ger kodexempel där det efterfrågas (behöver inte vara perfekt, men ska visa förståelse)

#### Icke Godkänt (IG)

Du får **Icke Godkänt** om:

- Flera frågor är obesvarade eller mycket ofullständiga
- Svaren visar grundläggande missförstånd av koncept
- Svaren är uppenbart kopierade från AI eller andra källor utan egen förståelse
- Svaren är så kortfattade att de inte visar förståelse

**Vid gränsfall**: Om du är nära G men några svar är otillräckliga kan du få möjlighet att komplettera specifika frågor.

---

## Tips för att lyckas

- Börja med frågorna du känner dig säkrast på
- Svara koncist - kvalitet över kvantitet
- Läs igenom dina svar innan inlämning
- Börja i tid - du har två veckor på dig
- Fråga på lektioner om något är oklart

**Kom ihåg**: Det viktiga är att du visar att du **förstår** koncepten, inte hur mycket du skriver. Tydliga, korta förklaringar är ofta bättre än långa utsvävningar.

---

## Hjälp och resurser

### Tillåtet

- Använda kursmaterial och dina egna anteckningar
- Titta på kod du själv skrivit under kursen
- Använda C# dokumentation (docs.microsoft.com)
- Fråga läraren om du inte förstår vad en fråga betyder
- Man får också använda AI för egen inlärning

### Inte tillåtet

- Kopiera svar från ChatGPT eller andra AI-verktyg
- Kopiera svar från klasskamrater eller internet
- Låta någon annan skriva dina svar

---

**Lycka till! 🚀**