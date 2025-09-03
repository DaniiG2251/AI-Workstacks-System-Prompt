
https://github.com/user-attachments/assets/218875b3-041d-4900-ac47-e01658d25519

-------------------------------------------------------------------
**🚀 Setup Instructies**

- Stap 1: System Prompt Installatie
  Ga naar Settings > Claude 4.0 Sonnet
  Plak de volledige system prompt in het System Prompt veld.
  
  Het wordt automatisch opgeslagen
  
⚠️ Let op: Na het instellen van het custom prompt dien je een nieuw gesprek te starten.


- Stap 2: Status Check
  Command: Status - ⚠️ Let op: Shared Data Store UIT staan
  

- Stap 3: Database Initialisatie
  Command: Setup Wise Data - ⚠️ Let op: Shared Data Store AAN staan

-------------------------------------------------------------------
**💻 Functionaliteiten**

📝 Database
 - Genereren van queries op basis van de 1267 tabellen incl. kolommen.
   
🎫 Jira Tickets
Volledige templates voor bug rapportage:

 - Wise versie: 8.0.1 (prod) / 8.0.2-8.0.3 (dev)
 - Reproductie stappen in begrijpelijk Engels
 - Impact assessment (Low/Medium/High)

📋 Release Notes
 - Tabel formatting.
 - Bereik	Omschrijving Aanpassing Versie Jira/ZD.
 - Bug beschrijving en Oplossing.
 - Versie van waar de oplossing in verwerkt zit.

-------------------------------------------------------------------
**📊 Kennis per 24-07-2025**

✅ Database	tabellen: 1267 
 - Laatst toegevoegde tabel: **[ X ]**
  
✅ Termen & Begrippen: 166 
 - Laatst toegevoegde begrip/term: **[ BCB/RCB ]**

✅ Templates
 - Jira
 - Release Notes

✅ Test Servers
 -  OW TEST 01-25

-------------------------------------------------------------------
**🎯 Basis instructie**

De Wise Assistent helpt met:

- Database queries op basis van 1267 database tabellen.
- Jira tickets opstellen voor bugs/issues.
- Release notes genereren.
- Begrippen uitleggen.
- Configuratie ondersteuning voor Wise systemen.

Aan jou de taak om de assistent te voeden met informatie zoals:

 - Wat is het probleem. ( Kopieer de klantvraag incl. maximaal 3 afbeeldingen in de chat )
 - vertel daar onder in het kort hoe heb je getest.
 - Waarmee heb je getest, welke server?, Welke actor? Welke versie?
 - Hoe is het opgelost (t.b.v. release notes.)


-------------------------------------------------------------------

FAQ - Wise Assistant

**Basis Gebruik**

**Q: Hoe start men de Wise Assistant op?**
A: 
1. Zet de **Shared Data Store** aan (schuifje onder tekstbalk)
2. Typ `Setup Wise Data` om de database te initialiseren
3. Wacht tot "✅ SETUP VOLTOOID" verschijnt
4. De assistant heeft nu toegang tot alle 1267 tabellen en 165 begrippen

**Q: Wat gebeurt er als de setup mislukt?**
A: Er verschijnt "❌ SETUP MISLUKT - SHARED DATA STORE VEREIST". Start een nieuw gesprek en probeer opnieuw met de Shared Data Store aan.

**Q: Hoe controleert men de huidige status?**
A: Typ `status` voor een overzicht van geladen tabellen, begrippen en laatste updates.

---

**Database & Queries**

**Q: Welke tabellen kent de assistant?**
A: Alle 1267 tabellen uit Wise 8.0.1, zoals ACTOR, ACTOR_ZOEK, ROL_ABONNEMENT, ACTOR_AUTH_MIDDEL, etc.

**Q: Maakt de assistant alleen queries met bestaande kolommen?**
A: Ja, alleen kolommen die letterlijk gedocumenteerd zijn in de kennisbestanden worden gebruikt. Kolomnamen of structuren worden nooit verzonnen.

**Q: Wat als een tabel niet volledig gedocumenteerd is in de bestanden?**
A: De assistant geeft aan welke tabellen ontbreken en vraagt om deze te delen vanuit het Wise data model. 

**Voorbeeld:** *"Voor een accurate query op tabel FINANCIELE_MUTATIE heb ik de complete tabel structuur nodig. Deel deze tabel uit het online Wise data model."*

**Q: Waarom zijn de queries zo kort?**
A: De assistant maakt bewust korte queries met `*` zodat alle kolommen zichtbaar zijn. 

**Voorbeelden:**
```sql
SELECT * FROM ACTOR WHERE actor_id = 92550;
SELECT * FROM ROL_ABONNEMENT WHERE status = '5';
```

---

**Workstacks Beperkingen**

**Q: Heeft de assistant toegang tot het internet?**
A: **NEE** - Workstacks heeft momenteel geen internettoegang. Alle informatie moet via de Shared Data Store worden gedeeld.

**Q: Hoe krijgt men de meest accurate informatie?**
A: Deel zoveel mogelijk relevante bestanden en tabel structuren in de Shared Data Store. De assistant werkt alleen met de beschikbare documenten.

**Q: Wat als specifieke Wise documentatie ontbreekt?**
A: De assistant geeft aan welke documenten/tabellen nodig zijn en vraagt om deze te delen vanuit:
- Het online Wise data model
- Interne Wise documentatie
- Specifieke tabel definities

**Voorbeeld:** *"Voor tabel UITLENING_HISTORIE ontbreekt de structuur. Deel deze tabel uit het Wise data model voor accurate queries."*

---

**Templates**

**Q: Welke templates kan de assistant maken?**
A: 
- **Jira tickets** (in begrijpelijk Engels)
- **Release notes** (Nederlandse tabel format)
- **Status updates** van de kennisbank

**Q: Waarom stelt de assistant soms extra vragen voor Jira templates?**
A: Alleen bekende informatie wordt ingevuld. Voor ontbrekende details (server, versie, credentials) worden eerst vragen gesteld in een apart bericht.

**Jira template voorbeeld:**
```
Current Wise version: 8.0.1
When did the problem start? When trying to use online registration
Description: Users cannot complete registration process
Replication environment: OW TEST 01
```

---

**Shared Data Store & Performance**

**Q: Waarom wordt de Shared Data Store vol?**
A: Alle geüploade documenten worden opgeslagen. Dit kan de performance beïnvloeden - hoe meer data, hoe langzamer de responses.

**Q: Kunnen oude bestanden verwijderd worden?**
A: Nee, dat is momenteel niet mogelijk. Dit is doorgemeld aan de Workstacks developers.

**Q: Hoe verwijst men naar specifieke Wise documenten?**
A: Gebruik concrete namen in vragen:

**Voorbeelden:**
- *"Welke kolommen heeft ACTOR? Kijk in **WiseDataBrain** voor de tabel structuur"*
- *"Wat betekent IBL? Check de **Begrippenlijst** voor terminologie"*
- *"Hoe werkt de database? Zie **Data model** voor de structuur"*

---

**Specifieke Wise Kennis**

**Q: Welke versie van Wise gebruikt de assistant?**
A: Wise 8.0.1 (laatste stabiele versie). 8.0.2 en 8.0.3 zijn in development.

**Q: Welke sectoren kent de assistant?**
A: Primair: Openbare bibliotheken (BIEB). Ook: schoolWise, educatWise, mediatheekWise, ticketWise.

**Q: Welke servers zijn beschikbaar voor testen?**
A: OW TEST 01-25 met verschillende organisaties (CultuurConnect, Probiblio, BiSC, Rotterdam, etc.)

**Q: Kan de assistant vragen buiten Wise beantwoorden?**
A: **NEE** - Door de beperkte internettoegang kan alleen informatie uit de Shared Data Store worden gebruikt.

---

**Problemen Oplossen**

**Q: Waarom geeft de assistant verkeerde database info?**
A: De assistant werkt alleen met gedocumenteerde informatie uit WiseDataBrain, Setup, Data model, etc. Bij ontbrekende informatie wordt gevraagd om aanvullende documenten.

**Q: Hoe voorkomt men irrelevante antwoorden?**
A: Wees specifiek in vragen en deel relevante documenten:

**Goed:** *"Maak een query voor ACTOR_ZOEK tabel om actoren te zoeken op naam"*
**Slecht:** *"Zoek een actor"*

**Q: De assistant geeft te veel uitleg, hoe wordt dit korter?**
A: Standaard worden korte antwoorden gegeven. 

**Voorbeeld:** *"Geef alleen de query, geen uitleg"* of *"Kort antwoord graag"*

**Q: Wat als een antwoord onvolledig lijkt?**
A: Deel meer specifieke documenten of tabel structuren. De assistant kan alleen werken met beschikbare informatie in de Shared Data Store.
