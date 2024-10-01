# Kompetenz
Applikationen und Schnittstellen objektorientiert modellieren, implementieren, testen und dokumentieren

>TL;DR wir können objektorientiert Programmieren, inklusive dem Dokumentieren und Testen

# Ziele

## 1. Anwendungsprobleme für objektorientierte Programme analysieren
_also was die für dumme Sprache verwenden in den Modulen, fühlen sich einfach schlau ig_

## 1.1 Objektorientierter Ansatz

Kennen der Grundkonzepte des objektorientierten Programmierens 
- Kapselung: das Verbergen von Daten/ Infos von aussen. Direkter Zugriff auf interne Datenstruktur wird unterbunden
- Vererbung: halt die Vererbung 
- Polymorphie: Bezeichnet dass abhängig seiner Verwendung Objekte unterschiedlichen Datentyps annimmt

## 1.2 Klassenfindung

Wir müssen Vorgehensweisen zur Klassenfindung kennen, und diese anwenden können. Dazu gehört zum Beispiel Spezialisierung und Generalisierung.
Generalisierungen drücken eine Weitergabe (Vererbung) von Merkmalen und Fähigkeiten aus, welche in einer Objektgruppe als kleinstes Gemeinsames betrachtet werden.
Kurze Erläuterung
	Wir nehmen die Gruppe Handwerker, welche viele Unterschiede hat, je nach Beruf. Dennoch haben viele Handwerker vieles gemeinsam. 
	In einem ersten Schritt der Generalisierung isoliert man alle Gemeinsamkeiten einer grossen Objektgruppe. Alle so definierten Merkmale und Fähigkeiten werden von einer Mutterklasse (Mensch) zusammengefasst.
	Von einer Klasse Mensch lassen sich Tochterklassen ableiten (Maler, Tischler etc) welche spezielle Fähigkeiten und Merkmale haben. Dies ist dann die Spezialisierung
![[Pasted image 20240708074838.png]]
(Beispiel Konto | Sparkonto..)

### 1.3 Abstraktionskonzepte

Abstraktionskonzepte sind Prinzipien und Techniken, welche helfen, komplexe Systeme in einfachere Einheiten zu zerlegen

> Klassen und Objekte [[M320 Objektorientiertes Programmieren#3.1 Klassen und Objekte |hier]]
> Datenabstraktion: Verbergen der internen Representation von Daten
> Kapselung: Daten einer Klasse sind private und können nur über öffentliche Methoden erreicht werden
> Vererbung: Klassen können Eigenschaften und Methoden einer anderen Klasse übernehmen 


## 2. modellieren und dokumentieren

Modellieren umfasst die Darstellung anhand eines Modells wie z.B. einer CRC-Card, ein brainstorming tool
Man zeigt auf, welche Klasse welche Verantwortungen hat und welche Kollaboratoren sie hat

dokumentieren heisst dokumentieren

## 3. objektorientiertes Design implementieren

### 3.1 Klassen und Objekte
Klasse ist die Vorlage welche zum Erstellen von Objekten verwendet wird. Objekt ist eine Instanz der Klasse
Klasse ist logische Einheit, Objekt physische

### 3.2 objektorientierte Sprache und deren Elemente kennen
aka wir können objektorientiert programmieren

### 3.2 dynamische Bindung
dynamische Bindung ist die Bindung während der Runtime

### 3.3 inversion of Control
aka Dependency Injection..
Ein Objekt welches ein anderes Objekt braucht, davon abhängig ist

## 4. Überprüfung
Wir können Projekte Testen (Testfälle erstellen)
Wir kennen automatisches Unit testing