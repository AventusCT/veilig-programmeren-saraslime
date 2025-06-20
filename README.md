[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/aznyoZ53)
﻿# TechShop Security Lab - Onveilige Webshop

## 🎯 Doel
In deze opdracht analyseer je een **expres onveilig gebouwde** PHP-webshop. Je leert beveiligingsproblemen herkennen, begrijpen waarom ze gevaarlijk zijn en hoe je ze kunt voorkomen.

⚠️ **WAARSCHUWING:** Deze webshop bevat opzettelijke beveiligingslekken voor educatieve doeleinden. Gebruik deze code NOOIT in een productieomgeving!

## 📋 Benodigdheden
- XAMPP of WAMP (lokaal webserverpakket)
- Een browser (Chrome/Firefox aanbevolen)
- Een teksteditor (VS Code aanbevolen)
- phpMyAdmin (meegeleverd in XAMPP/WAMP)

## 🚀 Installatie Instructies

### Stap 1: Download de Webshop
```bash
# Clone via Git
git clone [repository-url]

# OF download als ZIP via GitHub
```

### Stap 2: Installeer XAMPP/WAMP
1. Download XAMPP: https://www.apachefriends.org/
2. Installeer XAMPP
3. Start Apache en MySQL via XAMPP Control Panel

### Stap 3: Plaats de Webshop
1. Kopieer de webshop folder naar:
   - XAMPP: `C:\xampp\htdocs\webshop\`
   - WAMP: `C:\wamp64\www\webshop\`

### Stap 4: Database Setup
1. Open phpMyAdmin: http://localhost/phpmyadmin
2. Klik op "New" / "Nieuw"
3. Database naam: `webshop`
4. Klik "Create"
5. Klik op "Import" / "Importeren"
6. Kies bestand: `db.sql`
7. Klik "Go" / "Start"

### Stap 5: Configuratie
1. Open `config.php` in je editor
2. Controleer deze instellingen:
```php
$host = "localhost";
$user = "root";
$password = "";  // Leeg voor XAMPP, "root" voor WAMP
$dbname = "webshop";
```

### Stap 6: Test de Installatie
1. Open: http://localhost/webshop/
2. Je zou de TechShop homepage moeten zien
3. Test accounts:
   - `admin` / `admin123`
   - `john` / `password`
   - `jane` / `123456`

## 🔍 Quick Start voor Security Testing

### Handige URLs
- Homepage: http://localhost/webshop/
- Login: http://localhost/webshop/login.php
- Admin Panel: http://localhost/webshop/admin.php
- Products: http://localhost/webshop/products.php
- Register: http://localhost/webshop/register.php

### Debug Mode
Voor SQL injection debugging:
```
http://localhost/webshop/login.php?debug=1
```

## ⚡ Tips voor de Opdracht
1. **Gebruik Incognito Mode** voor XSS tests (voorkomt browser caching)
2. **Developer Tools (F12)** helpen bij het debuggen
3. **Maak screenshots** van elke succesvolle exploit
4. Test systematisch - volg de opdracht stap voor stap
5. Documenteer alles wat je vindt

## 🛠️ Troubleshooting

### Apache start niet
- Check of Skype/Teams port 80 niet gebruiken
- Verander Apache port in XAMPP naar 8080

### Database connection failed
- Controleer of MySQL draait in XAMPP
- Verify database naam is exact `webshop`
- Check username/password in config.php

### Pagina's laden niet
- URL moet zijn: http://localhost/webshop/ (niet vergeten: `/webshop/`)
- Check of alle bestanden in de juiste folder staan

### XSS werkt niet
- Test in incognito/private browsing mode
- Probeer verschillende payloads
- Check browser console voor errors

## 📝 Opdracht Overzicht
Je gaat 6 verschillende security kwetsbaarheden onderzoeken:
1. SQL Injection
2. Cross-Site Scripting (XSS)
3. Insecure Direct Object References (IDOR)
4. Sensitive Data Exposure
5. Broken Access Control
6. Input Validation Failures

Voor elk onderdeel moet je:
- De kwetsbaarheid demonstreren
- De OWASP categorie identificeren
- Een oplossing voorstellen

## ⚠️ Ethische Hacking Disclaimer
Deze vaardigheden zijn bedoeld voor:
- Het beveiligen van je eigen applicaties
- Security audits met toestemming
- Bug bounty programma's

**NOOIT** gebruiken voor:
- Hacken zonder toestemming
- Schade aanrichten aan systemen
- Illegale activiteiten

---
*Veel succes met de opdracht! Remember: with great power comes great responsibility 🕷️*