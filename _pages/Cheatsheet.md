<!--
NOTE: Requires Markdown Extra. See http://michelf.ca/projects/php-markdown/extra/
 -->
<link href="style.css" type="text/css" rel="stylesheet"/>

<table width="100%">
<tr>
<td class="title" width="70%">ProLogis Coding Guidelines C# Cheat Sheet</td>
<td rowspan="2" style="text-align:right">![logo](assets/images/logo.png)</td>
</tr>
</table>

<table width="100%">
<tr>
<td class="column" markdown="1">
<div markdown="1" class="sidebar">
**Grundlegende Prinzipien**

* The Principle of Least Surprise
* Keep It Simple Stupid
* You Ain't Gonna Need It
* Don't Repeat Yourself
* OOP: Encapsulation, abstraction, inheritance, polymorphism

</div>

**Basismuster**

* Alle Datenbankzugriffe werden über das Repository Basismuster durchgeführt ({{ site.default_rule_prefix }}9000)
* Für die Erzeugung von variablen aber gleichartigen Objekten, denen eine abstrakte Basisklasse zugrunde liegt wird das Factory Pattern verwendet. ({{ site.default_rule_prefix }}9001)
* Um den Datenzugriff klar zu strukturieren setzen wir auf das CQRS pattern. ({{ site.default_rule_prefix }}9002)

<br/>

**Namensmuster**

* tbd. ({{ site.default_rule_prefix }}9100)

<br/>

**Namensgebung**

* Sprache von Bezeichnern ist US Englisch  ({{ site.default_rule_prefix }}1000)
* Domänenbegriffe auf Deutsch ({{ site.default_rule_prefix }}1001)
* Keine Sonderzeichen verwenden ({{ site.default_rule_prefix }}1002)
* Keine Nummern in Zeichnern  ({{ site.default_rule_prefix }}1003)
* Keine Typinformationen in Bezeichnern ({{ site.default_rule_prefix }}1004)
* Keine untergeordneten Wiederholungen ({{ site.default_rule_prefix }}1005)
* Korrekte Groß- und Kleinschreibung ({{ site.default_rule_prefix }}1006)
* Keine Abkürzungen verwenden ({{ site.default_rule_prefix }}1007)
* Typen mit Nomen, Nominalen Phrasen oder Adjektiven bennenen ({{ site.default_rule_prefix }}1008)
* Namen einer Klasse oder Enumeration nicht in den Membern wiederholen ({{ site.default_rule_prefix }}1009)
* Namenskonventionen des Frameworks adaptieren ({{ site.default_rule_prefix }}1010)
* Benennung von Properties ({{ site.default_rule_prefix }}1011)
* Benennung von Methoden ({{ site.default_rule_prefix }}1012)
* Bennung von Events mit Verben oder verbialen Phrasen ({{ site.default_rule_prefix }}1013)
* Verlaufs- und Vergangenheitsformen für Pre- und Postevents ({{ site.default_rule_prefix }}1014)
* Eventhandler immer mit Prefix "On" ({{ site.default_rule_prefix }}1015)
* Underscore für irrelevante lambda parameter verwenden ({{ site.default_rule_prefix }}1016)
* Asynchrone Methoden werden mit dem Suffix "Async" bennant ({{ site.default_rule_prefix }}1017)
</td>
<td class="column">

**Komponenten Design**

* Namensgebung Komponenten  ({{ site.default_rule_prefix }}2000)
* Namensgebung Namespaces ({{ site.default_rule_prefix }}2001)
* Zu jeder Implementierung genau ein Kontrakt ({{ site.default_rule_prefix }}2002)
* Zu jedem Kontrakt mind. eine Implementierung ({{ site.default_rule_prefix }}2003)
* Eine Basisausnahme pro Kontrakt ({{ site.default_rule_prefix }}2004)
* Datenklassen im Kontrakt ({{ site.default_rule_prefix }}2005)
* Callback im Kontrakt ({{ site.default_rule_prefix }}2006)
* Kontrakt besitzt nur Schnittstellen im Root  ({{ site.default_rule_prefix }}2007)
* Schnittstellen eines Kontraktes immer im Root ({{ site.default_rule_prefix }}2008)
* Keine Implementierungsabhängigkeiten ({{ site.default_rule_prefix }}2009)

<br/>

**Klassen Design**

* Extensionklasse mit Suffix Extensions ({{ site.default_rule_prefix }}3000)
* Basisklassen mit Suffix Base ({{ site.default_rule_prefix }}3001)
* Attributklassen mit Suffix Attribute ({{ site.default_rule_prefix }}3002)
* Exceptionklassen mit Suffix Exception ({{ site.default_rule_prefix }}3003)
* Keine Klasse mit mehr als 10 Methoden ({{ site.default_rule_prefix }}3004)
* Keine Klasse mit mehr als 220 LOC ({{ site.default_rule_prefix }}3005)
* Keine Klasse mit mehr als 15 Feldern ({{ site.default_rule_prefix }}3006)
* Verhältnis öffentlichen zu privaten Methoden nicht mehr als 2:1 ({{ site.default_rule_prefix }}3007)
* Keine Bidirektionalen Abhängigkeiten ({{ site.default_rule_prefix }}3008)
* Keine statischen Klassen ({{ site.default_rule_prefix }}3009)
* Keine nested Klassen ({{ site.default_rule_prefix }}3010)
* Sichtbarkeit von Klassen einschränken ({{ site.default_rule_prefix }}3011)
* Eine Klasse oder Interface darf nur eine Aufgabe erfüllen ({{ site.default_rule_prefix }}3012)
* Konstruktoren müssen sinnvolle Objekte zurückliefern ({{ site.default_rule_prefix }}3013)
* Interfaces müssen klein und fokussiert sein ({{ site.default_rule_prefix }}3014)
* Objekte sollten keine anderen abhängigen Objekte anbieten ({{ site.default_rule_prefix }}3015)
* Klassen müssen die Konsistenz des eigenen internen Status sicherstellen n ({{ site.default_rule_prefix }}3016)

</td>
<td class="column">

**Member Design**

* Properties müssen in beliebiger Reihenfolge belegt werden können ({{ site.default_rule_prefix }}4000)
* Methoden anstatt Properties verwenden ({{ site.default_rule_prefix }}4001)
* Keine Properties die sich gegenseitig ausschließen ({{ site.default_rule_prefix }}4002)
* Property / Methode darf nur eine Aufgabe erfüllen ({{ site.default_rule_prefix }}4003)
* Methoden mit maximal 20 LOC ({{ site.default_rule_prefix }}4004)
* Methoden mit maximaler Komplexität von 7 ({{ site.default_rule_prefix }}4005)
* Methoden mit maximal 5 Parametern ({{ site.default_rule_prefix }}4006)
* Methoden mit maximal 5 Überladungen ({{ site.default_rule_prefix }}4007)
* Konstruktoren mit maximal 5 Parametern ({{ site.default_rule_prefix }}4008)
* Keine statischen Member ({{ site.default_rule_prefix }}4009)
* Keine öffentlichen Felder  ({{ site.default_rule_prefix }}4010)
* Keine obsoleten Objekte verwenden ({{ site.default_rule_prefix }}4011)
* Immer ein IEnumberable oder ICollection anstatt einer Konkreten Auflistung zurückliefern ({{ site.default_rule_prefix }}4012)
* Properties, Argumente, und Rückgaben von String, Collections oder Tasks dürfen niemals null sein ({{ site.default_rule_prefix }}4013)
* Parameter werden so spezifisch wie möglich definiert ({{ site.default_rule_prefix }}4014)
* Domänen-spezifische Wertetypen sollten primitiven Typen vorgezogen werden ({{ site.default_rule_prefix }}4015)

<br/>

**Layout Guidelines**

* Einhaltung eines einheitlichen Layouts ({{ site.default_rule_prefix }}5000)
* Namespaces nach der Firma sortieren und gruppieren ({{ site.default_rule_prefix }}5001)
* Jede Kontrollstruktur wird mit Klammern versehen ({{ site.default_rule_prefix }}5002)
* Member in einer vorgegeben Reihenfolge implementieren ({{ site.default_rule_prefix }}5003)
* region Keyword nicht verwenden ({{ site.default_rule_prefix }}5004)
* Expression-bodies Members sinnvoll verwenden ({{ site.default_rule_prefix }}5005)

<br/>

**Framework Guidelines**

* C# Typaliasse verwendet anstatt den Typen aus dem System Namespace ({{ site.default_rule_prefix }}6000)
* Sprachsyntax anstatt expliziter Aufrufe der darunterliegenden Implementierungen verwenden ({{ site.default_rule_prefix }}6001)
* Builden mit dem höchsten Warnungslevel ({{ site.default_rule_prefix }}6002)
* LINQ Query Syntax für einfache Abfragen vermeiden ({{ site.default_rule_prefix }}6003)
* Lambda Ausdrücke anstelle von anonymen Methoden verwenden ({{ site.default_rule_prefix }}6004)

<br/>

**Framework Guidelines**

* Alle Kommentare und Dokumentationen werden in US Englisch geschrieben ({{ site.default_rule_prefix }}7000)
* Alle public, protected und internal Typen und Member werden dokumentiert ({{ site.default_rule_prefix }}7001)
* Inline Kommentare vermeiden ({{ site.default_rule_prefix }}7002)
* Kommentare nur für komplexe Logiken und Entscheidungen verwenden ({{ site.default_rule_prefix }}7003)
* Keine TODO-Kommentare ({{ site.default_rule_prefix }}7004)
</td>
<tr>

<table width="100%" class="footer">
<tr>
<td>
  ProLogis Automatisierung und Identifikation GmbH
  %commitdate%
</td>
<td style="text-align:right">
  [www.prologis.de](http://www.prologis.de)
</td>
</tr>
</table>
