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

<br/>

**Namensmuster**

* Alle Businesslogik zu einer Datenklasse wird in Klassen mit dem Suffix “Controller” implementiert. ({{ site.default_rule_prefix }}9100)
* Alle Vergleiche werden in Klassen mit dem Suffix “Comparer” benannt. Die Klassen müssen IComparer implementieren. ({{ site.default_rule_prefix }}9101)
* Alle Validierung von Datenklassen werden in Klassen mit dem Suffix “Validator” implementiert. ({{ site.default_rule_prefix }}9102)

<br/>

**Namensgebung**

* Sprache von Bezeichnern ist US Englisch  ({{ site.default_rule_prefix }}1000)
* Domänenbegriffe auf Deutsch ({{ site.default_rule_prefix }}1001)
* Keine Sonderzeichen verwenden ({{ site.default_rule_prefix }}1002)
* Keine Nummern in Zeichnern  ({{ site.default_rule_prefix }}1003)
* Keine Typinformationen in Bezeichnern ({{ site.default_rule_prefix }}1004)
* Keine untergeordneten Wiederholungen ({{ site.default_rule_prefix }}1005)
* Benennung von Klassen (Großbuchstabe) ({{ site.default_rule_prefix }}1006)
* Benennung von Interfaces (I + Großbuchstabe) ({{ site.default_rule_prefix }}1007)
* Benennung von Enums (Großbuchstabe) ({{ site.default_rule_prefix }}1008)
* Benennung von Delegates (Großbuchstabe + Suffix Handler) ({{ site.default_rule_prefix }}1009)
</td>
<td class="column">

**Member Design**

* Benennung von Enumerationswerten (Großbuchstabe) ({{ site.default_rule_prefix }}2000)
* Benennung von Events (Großbuchstabe) ({{ site.default_rule_prefix }}2001)
* Benennung von Feldern (_ + Kleinbuchstabe) ({{ site.default_rule_prefix }}2002)
* Benennung von Methoden (Großbuchstabe) ({{ site.default_rule_prefix }}2003)
* Benennung von Eigenschaften (Großbuchstabe) ({{ site.default_rule_prefix }}2004)
* Methoden mit maximal 20 LOC ({{ site.default_rule_prefix }}2005)
* Methoden mit maximaler Komplexität von 7 ({{ site.default_rule_prefix }}2006)
* Methoden mit maximal 5 Parametern ({{ site.default_rule_prefix }}2007)
* Methoden mit maximal 5 Überladungen ({{ site.default_rule_prefix }}2008)
* Konstruktoren mit maximal 5 Parametern ({{ site.default_rule_prefix }}2009)
* Keine statischen Member ({{ site.default_rule_prefix }}2010)
* Keine öffentlichen Felder  ({{ site.default_rule_prefix }}2011)
* Keine obsoleten Objekte verwenden ({{ site.default_rule_prefix }}2012)

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

</td>
<td class="column">

**Komponenten Design**

* Namensgebung Komponenten  ({{ site.default_rule_prefix }}4000)
* Namensgebung Namespaces ({{ site.default_rule_prefix }}4001)
* Zu jeder Implementierung genau ein Kontrakt ({{ site.default_rule_prefix }}4002)
* Zu jedem Kontrakt mind. eine Implementierung ({{ site.default_rule_prefix }}4003)
* Eine Basisausnahme pro Kontrakt ({{ site.default_rule_prefix }}4004)
* Datenklassen im Kontrakt ({{ site.default_rule_prefix }}4005)
* Callback im Kontrakt ({{ site.default_rule_prefix }}4006)
* Kontrakt besitzt nur Schnittstellen im Root  ({{ site.default_rule_prefix }}4007)
* Schnittstellen eines Kontraktes immer im Root ({{ site.default_rule_prefix }}4008)
* Keine Implementierungsabhängigkeiten ({{ site.default_rule_prefix }}4009)

<br/>

**Layout Guidelines**

* Kommentare (nicht mehr als 10%)  ({{ site.default_rule_prefix }}5000)
</td>
<tr>

<table width="100%" class="footer">
<tr>
<td>
  ProLogis
  %commitdate%
</td>
<td style="text-align:right">
  [www.prologis.de](http://www.prologis.de)
</td>
</tr>
</table>
