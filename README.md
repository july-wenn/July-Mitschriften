# July Mitschriften

Das ist die README.md - Datei. MD sthet für Markdown. Markdown ist eine heutzutage weit verbreitets Auszeichnungssprache (_Markup Language_, [Wikipedia](https://de.wikipedia.org/wiki/Auszeichnungssprache)).

Weitere bekannte Auszeichnungssprachen sind:

- Hypertext Markup Language (HTML)

- Extensible Markup Language (XML)

- Yet Another Markup Language (YAML)

<<<<<<< HEAD

# Installation node.JS

Javascript läuft unter normalen Umständen in einer Browser-Sandbox (nur im Browser). Seit ca. 2010 gibt es Laufzeitumgebung (_Runtime Environment_) für JS, damit man auch serverseitig JS programmieren und ausführen kann: [Node.js](https://nodejs.org/en).

## Installation von pnpm

Der standardmäßige _Package Manager_ für Node.js ist npm (_Node Package Manager_). Eine etwas modernere und inzwischen beliebtere alternative ist [Pnpm](pnpm.io)

## Installation von strapi

Installation mit dem Skript `pnpm create strapi` Daraufhin führt das CLI durch die Installation. Falls bei der Installation sogennante build scripts nicht eingeführt werden können. schlägt die CLI die Fehlerbehandlung selbständig vor.

1. Wechseln in das Installationsverzeichnis (z.B. mit `cd strapi-project`)
2. Führe den Befehl `pnpm install` aus, um die fehlenden Pakete zu installieren und die uild-Skripte auszuführen. Dieser scheitert in der Regel - die Build Skripte müssen mit pnpm approve-builds manuell freigegebn werden.

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent view.
Dort können alle ANpassungen des "_COding Harness_" vorgenimmen werden. Wir können uns _Harness_ mit verschiedenen Methoden anpassen:

-**MCP-Server:**
MCP steht für _Model Context Protokoll_. Es ist ein Standard, der von Anthropic entwickelt wurde. Mit Hilfe von MCP können Chatbots / LLMs (_Large Language model_) auf zusätzliche Tools zugreifen, die sie zu Experten in einem bestimmten Themenbereich machen. In unserem Fall ist das der _VibeCoding Harness_.

# 4BHK

## komponente

`wiederverwendbare UI-Bausteine`, die in einer Anwendung verwendet werden können. Komponenten können aus HTML, CSS und JavaScript bestehen und können in verschiedenen Teilen der Anwendung wiederverwendet werden.

## props

props sind `Eigenschaften`, die an eine Komponente übergeben werden können. Sie ermöglichen es, dass eine Komponente flexibel und wiederverwendbar ist. Props können in einer Komponente als Parameter verwendet werden und können auch Standardwerte haben.

## each block

anstatt für einer Liste jedes einzelne Element zu rendern, kann man mit `each block` die Liste in einem Block rendern. Das spart Rechenleistung und ist performanter.

```html
<div>
  {#each colors as color}
  <button
    style="background: red"
    aria-label="red"
    aria-current="{selected"
    =""
    =""
    ="red"
    }
    onclick="{()"
    =""
  >
    selected = 'red'} >
  </button>
  {/each}
</div>
```

## anonyme Funktionen

die keine Namen haben. Sie werden oft als Argumente an andere Funktionen übergeben oder als Rückgabewerte von Funktionen verwendet. Anonyme Funktionen können mit der `function`-Syntax oder mit der Pfeilfunktion (`=>`) definiert werden.

## aria

`accessibility rich internet applications`. Das ist eine Spezifikation, die beschreibt, wie Webinhalte und Webanwendungen für Menschen mit Behinderungen zugänglich gemacht werden können.

## Keyed each block

keyed each block ist eine Erweiterung des each blocks. Es ermöglicht es, dass die Elemente in der Liste anhand eines Schlüssels identifiziert werden können. Das ist wichtig, wenn die Liste dynamisch ist und sich die Elemente ändern können.

```html
{#each things as thing (thing.id)}
<Thing name="{thing.name}" />
{/each}
```

## queue

List von Elementen, die nach dem First-In-First-Out-Prinzip (FIFO) organisiert sind. Das bedeutet, dass das zuerst hinzugefügte Element als erstes entfernt wird. Eine Queue kann mit den Methoden `enqueue` und `dequeue` manipuliert werden.

## Events

#### - DOM events:

Bei DOM events handelt es sich um Ereignisse, die im Browser ausgelöst werden. Beispiele für DOM events sind `click`, `mouseover`, `keydown`, `submit` usw. DOM events können mit der Methode `addEventListener` an ein Element gebunden werden. Kann position der `Maus verfolgen`, wenn sie sich über einem Element bewegt. Das ist nützlich, um interaktive Anwendungen zu erstellen.

```html
<div onpointermove="{onpointermove}" role="presentation">
  The pointer is at {Math.round(m.x)} x {Math.round(m.y)}
</div>
```

#### - Inline handlers:

Inline handlers sind Ereignis-Handler, die direkt in einem HTML-Element definiert werden z. B `onclick={() => count++}`

```html
<button on:click="{handleClick}">Click me</button>
```

#### -Component events:

component events sind Ereignisse, die von einer Komponente ausgelöst werden. Sie können mit der Methode `dispatch` an eine Komponente gebunden werden. Component events können auch an eine übergeordnete Komponente weitergeleitet werden.

### package.json

Die Datei `package.json` ist eine JSON-Datei, die Metadaten über ein Node.js-Projekt enthält. Sie enthält Informationen wie den Namen des Projekts, die Version, die Abhängigkeiten, die Skripte und andere Konfigurationsoptionen. Die Datei wird von npm und pnpm verwendet, um das Projekt zu verwalten.

# Historische Entwicklung von WebDev

Webdevelopment hat im Laufe der letzten rund 35 Jahre einige Evolutionsstufen durchlaufen:

**1. Statische Webseiten** (HTML, CSS, ggr. JavaScript) - initiale Phase des Webdevelopments, bei der Inhalte fest im HTML-Code verankert sind. Dominant in der 1990er Jahren.

**2. Dynamische Webseiten** (mit serverseitiger Programmiersprache die auf Datenbanken zugreift - PHP, Python, NodeJS - und Datenanbindung. Dominant in den 2000er Jahren.)

**3. _Single-Page Applications_ (SPA)** - mit JavaScript-Frameworks erstellt "Wepapps", die ähnliche Funktionen wie klassische Desptop-Anwenundngen bzw. Handy-apps bieten. Dominant in der 2010er Jahren. Um Handy-Apps möglichst nahe zu kommen, werden oft _Progressive Web Apps_ (PWA) erntwickelt. Damit können Webapps offline funktionieren, Push-Benachrichtigungen senden und auf bestimmte natibe Funktionen des Geräts zugreifen. Es gibt drei vorraussetzungen die eine Webapp erfüllen muss, um als PWA zu gelten:

**1.** Sie muss über HTTPS ausgeliefert werden.

**2.** Sie muss ein Web-App-Manifest manifst.json haben.

**3.** Die WEbapp muss über https erreichbar sein und einen Service Worker haben, der die App offline verfügbar macht.

- Pushbenachrichtigungen
- Mikrofon
- Kamera
- GPS
- Bluetooth
- Gyroskop

#

- **Frontend- Frameworks**: werden folgende Architekturprinzipien an, um eine möglichst gute _User Experience_ zu gewährleisten. Beispiele sind: React, Vue, Angular, Svelte

- **Komponenten** sind die wiederverwendbaren "Lego" Bausteine einer Webapp. Sie können aus HTML, CSS und JavaScript bestehen und können in verschiedenen Teilen der Anwendung wiederverwendet werden.

-**deklarative Programmierung:** - der Javaskript und Template (HTML) - code beschreiben, wie die Benutzerpberfläche ausssehen soll (die Umsetzung), dabei kommt die Reactivity ins spiel: Wenn sich der Zustand der Anwendung ändert, aktualisiert das Framework automatisch die Benutzeroberfläche, ohne dass der Entwickler sich um die Details kümmern muss. Wenn ödie Aktualisierung in die andere Richtung funktioniert, (d.h. wenn sich die Benutzeroberfläche ändert, weil der Benutzer mit ihr interagiert, und der Zustand (_state_) der Anwendung entsprechend aktualisiert wird), spricht man von bidirektionaler Datenbindung. (_two-waydata binding_)

Logikelemente (Schleifen zur Darstellung von Listen und Bedingungen für das konsitinale Ein und Ausblenden von UI - Elementen) werdenin den Templates (HTML) der Komponente definiert. Die Templates werden vom Framework in die eigentliche Benutzeroberfläche übersetzt.

Komponenten können auch andere Komponenten enthalten, wodurch eine hierarchische Struktur entsteht. Die Kommunikation zwischen Komponenten erfolgt über `_props_` (Eigenschaften) und `_events_` (Ereignisse). Props sind Daten, die von einer übergeordneten Komponente an eine untergeordnete Komponente weitergegeben werden. Events sind Ereignisse, die von einer untergeordneten Komponente an eine übergeordnete Komponente gesendet werden.

## VibeCoding / AgenticEngineering mit VS-Code und GitHub Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View. Dort können alle Anpassungen des "_Coding Harness_" vorgenommen werden. Wir können unseren _Harness_ mit verschiedenen Methoden anpassen:

-**MCP-Server**:
MCP steht für _Model COntext Protocol_. Es ist ein Standard, der von Anthropic entwickelt wurde. Mit Hilfe von MCP können Chatbots/LLMs auf zustzliche Tools zugreifenm, die sie zu Experten in einem bestimmten Bereich machen.

# stack

### \* Datenstrukture (lifo)

### \* server / software stack

### \* bereiche im RAM (Speicher) einer anwendung

List von Elementen, die nach dem Last-In-First-Out-Prinzip (LIFO) organisiert sind. Das bedeutet, dass das zuletzt hinzugefügte Element als erstes entfernt wird. Ein Stack kann mit den Methoden `push` und `pop` manipuliert werden.

## server stack

server stack ist eine Sammlung von Softwaretechnologien, die zusammenarbeiten, um eine Webanwendung zu erstellen. Ein typischer Server Stack besteht aus einem Betriebssystem, einem Webserver, einer Datenbank und einer serverseitigen Programmiersprache. Beispiele für Server Stacks sind LAMP (Linux, Apache, MySQL, PHP), MEAN (MongoDB, Express.js, AngularJS, Node.js) und MERN (MongoDB, Express.js, React.js, Node.js).

## rest api

rest api ist ein Architekturstil für die Entwicklung von Webservices. REST steht für _Representational State Transfer_. RESTful Webservices verwenden HTTP-Methoden (GET, POST, PUT, DELETE) und URIs, um Ressourcen zu identifizieren und auf sie zuzugreifen. RESTful Webservices sind stateless, das bedeutet, dass jeder Request alle Informationen enthalten muss, die der Server benötigt, um ihn zu verarbeiten. RESTful Webservices sind skalierbar und können leicht in verschiedene Anwendungen integriert werden.

## server / software stack:

ist eine Sammlung von Softwaretechnologien, die zusammenarbeiten, um eine Webanwendung zu erstellen. Ein typischer Server Stack besteht aus einem Betriebssystem, einem Webserver, einer Datenbank und einer serverseitigen Programmiersprache. Beispiele für Server Stacks sind LAMP (Linux, Apache, MySQL, PHP), MEAN (MongoDB, Express.js, AngularJS, Node.js) und MERN (MongoDB, Express.js, React.js, Node.js).
