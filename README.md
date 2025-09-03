
https://github.com/user-attachments/assets/218875b3-041d-4900-ac47-e01658d25519


**🚀 Initialisatie**
-------------------------------------------------------------------

Stap 1: System Prompt Installatie
1. Ga naar Settings > Claude 4.0 Sonnet
2. Plak de system prompt in het System Prompt veld
3. Start een nieuw gesprek

Stap 2: Database Initialisatie
1. Zet Shared Data Store AAN (schuifje onder tekstbalk)
2. Type: Setup Wise Data
3. Wacht op: ✅ SETUP VOLTOOID

Stap 3: Status Verificatie
Type: status

💻 **Basis Functionaliteiten**
-------------------------------------------------------------------

📝 Database Queries
- **1267 tabellen** - Volledige Wise 8.0.1 database
- **Veilige queries** - Alleen SELECT * statements
- **Gevalideerde kolommen** - Enkel gedocumenteerde database structuur

🎫 Jira Ticket Templates
- **Engels format** voor internationale stappen
- **Complete bug rapportage** structuur
- **Impact assessment** (Low/Medium/High)
- **Automatische versie detectie** (8.0.1 prod / 8.0.2-8.0.3 dev)

📋 Release Notes Generator
| Bereik | Omschrijving | Aanpassing | Versie | Jira/ZD |
|--------|--------------|------------|--------|---------|
| Client | Bug fix | Query optimalisatie | 8.0.1 | WISENL-1234 / ZD 1234 |

**🎯 Ondersteunde Wise Componenten**
-------------------------------------------------------------------

Database Tabellen (1267)
- ACTOR - Hoofdtabel actoren
- ACTOR_ZOEK - Performance zoektabel
- ACTOR_AUTH_MIDDEL - Authenticatie methoden
- ROL_ABONNEMENT - Abonnementen beheer
- [En 1263 andere tabellen...]

Sectoren & Systemen
- **Primair:** Openbare bibliotheken (BIEB)
- **Extended:** schoolWise, educatWise, mediatheekWise, ticketWise
- **Landen:** Nederland, België (Vlaanderen)
- **Netwerken:** NBC+, NBD Biblion, Wise Community

Test Servers (25)
OW TEST 01-25 | CultuurConnect, Probiblio, BiSC, Rotterdam, OBGZ, etc.
Versies: 8.0.0, 8.0.1, 8.0.2, 8.0.3 (development)

**⚠️ Kritieke Beperkingen**
-------------------------------------------------------------------

🚫 Geen Internet Toegang
- **Workstacks beperking** - Alle kennis gaat via Shared Data Store.
- **Performance impact** - Volle datastore = langzamere responses & geen accurate antwoorden

📊 Vereiste Documenten
WiseDataBrain - Database structuur
Begrippenlijst - 165 terminologieën  
Data model - Database relaties
Setup/Wise Data Setup - Implementatie
BigParts - Wise onderdelen

🔍 Ontbrekende Tabel Structuren
Voor [TABELNAAM] ontbreekt volledige structuur.
Deel deze tabel uit het online Wise data model.
Workstacks heeft geen internettoegang.

📚 Huidige Kennisbank Status

Database Tabellen: 1267/1267 
Begrippen & Termen: 165 
Templates: Jira, Release Notes 
Test Servers: OW TEST 01-25 

**🎯 Best Practices**
-------------------------------------------------------------------

Effectief:
- "Maak query voor ACTOR_ZOEK om actoren te zoeken op naam"
- "Kijk in WiseDataBrain voor FINANCIELE_MUTATIE structuur"  
- "Genereer Jira ticket voor login probleem op OW TEST 01"

Vermijd
- "Zoek een actor" (te vaag)
- Queries zonder tabel specificatie
- Vragen zonder context over Wise versie/server

📋 Optimale Workflow
1. Upload relevante documenten naar Shared Data Store
2. Beschrijf probleem + context (server, versie, actor_id)
3. Voeg screenshots toe (max 3)
4. Geef testresultaten door
5. Vraag specifieke output (query/jira/release notes)

**🔧 Troubleshooting**
-------------------------------------------------------------------

Setup Problemen
❌ SETUP MISLUKT - SHARED DATA STORE VEREIST
→ Oplossing: Nieuw gesprek + Shared Data Store aan

Performance Issues  
Langzame responses? 
→ Shared Data Store vol met irrelevante bestanden
→ Momenteel geen cleanup optie beschikbaar

Onvolledige Antwoorden
→ Upload specifieke tabel structuren
→ Verwijs naar concrete document namen
→ Geef meer context over Wise versie/omgeving

**📖 FAQ - Veelgestelde Vragen**
-------------------------------------------------------------------

**Basis Gebruik**

**Q: Hoe start men de Wise Assistant op?**

A: 
1. Zet de **Shared Data Store** aan (schuifje onder tekstbalk)
2. Typ Setup Wise Data om de database te initialiseren
3. Wacht tot "✅ SETUP VOLTOOID" verschijnt

**Q: Wat gebeurt er als de setup mislukt?**

A: Er verschijnt "❌ SETUP MISLUKT - SHARED DATA STORE VEREIST". Start een nieuw gesprek en probeer opnieuw met de Shared Data Store aan.

**Q: Hoe controleert men de huidige status?**

A: Typ status voor een overzicht van geladen tabellen, begrippen en laatste updates.

**Database & Queries**

**Q: Welke tabellen kent de assistant?**

A: Alle 1267 tabellen uit Wise 8.0.1, zoals ACTOR, ACTOR_ZOEK, ROL_ABONNEMENT, ACTOR_AUTH_MIDDEL, etc.

**Q: Wat als een tabel niet volledig gedocumenteerd is?**

A: De assistant geeft aan welke tabellen ontbreken en vraagt om deze te delen vanuit het Wise data model.

**Q: Waarom zijn de queries zo kort?**

A: De assistant maakt bewust korte queries met * zodat alle kolommen zichtbaar zijn.

**Workstacks Beperkingen**

**Q: Heeft de assistant toegang tot het internet?**

A: **NEE** - Workstacks heeft momenteel geen internettoegang. Alle informatie moet via de Shared Data Store worden gedeeld.

**Q: Hoe krijgt men de meest accurate informatie?**

A: Deel zoveel mogelijk relevante bestanden en tabel structuren in de Shared Data Store.

**Q: Wat als specifieke Wise documentatie ontbreekt?**

A: De assistant geeft aan welke documenten/tabellen nodig zijn en vraagt om deze te delen uit het online Wise data model.

**Templates & Output**

**Q: Welke templates kan de assistant maken?**

A: Jira tickets (Engels), Release notes (Nederlandse tabel), Status updates van de kennisbank

**Q: Waarom stelt de assistant soms extra vragen voor Jira templates?**

A: Alleen bekende informatie wordt ingevuld. Voor ontbrekende details worden eerst vragen gesteld.

---

🔗 Snelle Commands

| Command | Functie |
|---------|---------|
| status | Kennisbank overzicht |
| Setup Wise Data | Database initialisatie |
| Document naam | Specifieke focus (bijv. "WiseDataBrain") |

---

**⚡ Laatste Update:** 03-09-2025  
**🎯 Versie:** Wise 8.0.1 (Stabiel) | 8.0.2-8.0.3 (Development)  
**🔧 Platform:** AI Workstacks met Shared Data Store ondersteuning
