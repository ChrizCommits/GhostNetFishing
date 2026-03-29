# 🌊 ghostnetfishing

Webprojekt im Modul Programmierung von industriellen Informationssystemen (Java EE).
Im Rahmen des ersten Sprints entstand eine Webanwendung zur Meldung, Verwaltung und Visualisierung von Geisternetzen inkl. Kartenansicht und Statusverwaltung.

## 🏠 Home
<img src="https://github.com/user-attachments/assets/7a406ba3-62dd-4313-9637-dc322a73ef8d" width="65%" alt="Home">

---

## 📊 Übersicht und Kartenansicht
Visualisierung aller gemeldeten Geisternetze weltweit nach Status (z. B. geborgen / offen), inkl. Kartenansicht.

<img src="https://github.com/user-attachments/assets/8087556e-f1fb-4ef6-b7ff-187b9fe14709" width="65%" alt="Overview">

---

## 📝 Meldung & Bergung

<p>
  <img src="https://github.com/user-attachments/assets/e0c271f5-7b0d-4f23-8c15-6c566eef01de" width="42%" alt="Report Form">
  <img src="https://github.com/user-attachments/assets/e8311878-0dc0-4ce5-8cf6-b96c074c9795" width="42%" alt="Recovered Form">
</p>

## ⚙️ Installation & Setup

### 📋 Voraussetzungen
- **[JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)** oder höher
- **Maven** – in Eclipse bereits integriert, in VS Code z. B. über das Plugin *Maven for Java*  
- **MySQL** – z. B. über [XAMPP](https://www.apachefriends.org/de/index.html) oder lokal installiert  
- **IDE** – Eclipse, VS Code, IntelliJ IDEA …

---

### 🧩 Einrichtungsschritte

#### 1️⃣ Repository in IDE klonen
```git clone https://github.com/chriz/ghostnetfishing.git```

#### 2️⃣ XAMPP starten
Im XAMPP-Control-Panel **Apache** und **MySQL** starten.

#### 3️⃣ Datenbank erstellen und Dump importieren
1. Im Browser http://localhost/phpmyadmin/ öffnen:
2. Neue Datenbank erstellen
  SQL Befehle:
  ```
  CREATE DATABASE ghostnetfishing;
  USE ghostnetfishing;
  ```
3. Anschließend die Datei `db/ghostnetfishing.sql` aus dem Repository über phpMyAdmin importieren.

#### 4️⃣ Anwendung in IDE starten
Eclipse: Run As → Spring Boot App
VS Code: `GhostNetFishingApplication.java` ausführen

#### 5️⃣ Anwendung im Browser öffnen
http://localhost:8090/

---

## 💡 Hinweise

Falls Port 8090 oder 3306 belegt ist, kann in `resources/application.properties` ein anderer Port gewählt werden:
```
pring.datasource.url=jdbc:mariadb://localhost:3306/ghostnetfishing
server.port=8090
```

Die Ports sollten mit der `my.ini` (MySQL-Konfiguration) übereinstimmen:
```
[client]
port=3306

[mysqld]
port=3306 
```

Falls eine andere Version als Jdk 17 gewählt wurde, bitte in `pom.xml` anpassen:
```
<java.version>*VERSIONSNUMMER*</java.version>
```



