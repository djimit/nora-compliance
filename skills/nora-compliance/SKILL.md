---
name: nora-compliance
description: >-
  Toetst IT-systemen, architecturen en projecten aan de Nederlandse Overheid
  Referentie Architectuur (NORA). Bevat de 10 NORA-basisprincipes, 40 afgeleide
  principes, dochterarchitecturen per bestuurslaag, koppelvlakstandaarden en
  het 'pas toe of leg uit'-mechanisme. Gebruikt bij architectuurreviews,
  projectstartarchitecturen (PSA), en leveranciersselecties.
  Gebruik deze skill wanneer de gebruiker vraagt over 'NORA', 'Nederlandse Overheid
  Referentie Architectuur', 'overheidsarchitectuur', 'referentiearchitectuur',
  'interoperabiliteit overheid', 'architectuurprincipes overheid', 'pas toe of leg uit',
  'GEMMA', 'PETRA', 'WILMA', 'RORA', 'architectuurcheck', 'project startarchitectuur',
  'PSA', 'GDI', 'Generieke Digitale Infrastructuur', 'Digikoppeling', 'Digimelding',
  'Digilevering', 'Haal Centraal', 'overheid API', 'overheidsdienst', 'basisregistratie',
  of wanneer de gebruiker een architectuur wil laten toetsen aan NORA-normen.
model: sonnet
allowed-tools:
  - WebFetch(*)
---

# NORA Compliance Checker

Toets IT-systemen, architecturen en projecten aan de Nederlandse Overheid Referentie Architectuur (NORA). NORA is verplicht voor de gehele Nederlandse overheid (Rijk, provincies, gemeenten, waterschappen, uitvoeringsorganisaties, ZBO's) op basis van het 'pas toe of leg uit'-principe.

Bron: [NORA Online](https://www.noraonline.nl) | [GEMMA Online](https://www.gemmaonline.nl) | [Digikoppeling](https://www.logius.nl/diensten/digikoppeling)

## NORA Vijflaagsmodel

```
1. POLITIEK-BESTUURLIJK — Beleid, wet- en regelgeving
    ├── Wet digitale overheid, AVG, Archiefwet
    └── Besluiten en kaders van bestuur
2. ORGANISATIE — Inrichting, processen, governance
    ├── Bedrijfsfuncties en -processen
    └── Rollen, verantwoordelijkheden en governance
3. INFORMATIEVOORZIENING — Informatie, gegevens
    ├── Informatiemodellen, gegevenswoordenboeken
    └── Informatiebeveiliging en privacy
4. APPLICATIE — Applicatiefuncties en -services
    ├── Applicaties en API's
    └── Berichtuitwisseling en koppelvlakken
5. TECHNISCHE INFRASTRUCTUUR — Netwerk, hardware, cloud
    ├── Netwerken, datacenters, cloud
    └── Middleware, operating systems
```

Bij architectuurreviews: loop alle vijf lagen af. Problemen ontstaan vaak op laagovergangen.

## 10 NORA-Basisprincipes

| # | Principe | Kernvraag | Afgeleide principes |
|---|----------|-----------|-------------------|
| **BP01** | Afnemers krijgen de dienstverlening waar ze recht op hebben | Is de dienst toegankelijk en rechtmatig? | AP01–AP06 (dienstverlening, rechtmatigheid, vindbaarheid, toegankelijkheid, begrijpelijkheid, transparantie) |
| **BP02** | Afnemers ervaren uniformiteit in dienstverlening | Is de dienst consistent met andere overheidsdiensten? | AP07–AP10 (uniforme benadering, gemak, eenduidige informatie, uniforme interactie) |
| **BP03** | Overheidsorganisaties bieden hun diensten digitaal en fysiek aan | Is er een volwaardig digitaal kanaal? | AP11–AP14 (digitale diensten, fysieke diensten, kanaaldiversiteit, gebruiker centraal) |
| **BP04** | Afnemers hebben inzage in eigen gegevens en kunnen deze corrigeren | Kunnen burgers hun data inzien? | AP15–AP18 (inzage, correctie, vergetelheid, dataportabiliteit) |
| **BP05** | Afnemers en overheidsorganisaties vertrouwen op de vertrouwelijkheid, integriteit, beschikbaarheid en controleerbaarheid van gegevens | Is de beveiliging op orde? | AP19–AP24 (vertrouwelijkheid, integriteit, beschikbaarheid, controleerbaarheid, authenticiteit, onweerlegbaarheid) |
| **BP06** | Afnemers worden zo min mogelijk belast met het aanleveren van informatie | Wordt data hergebruikt (eenmalige uitvraag)? | AP25–AP28 (eenmalige uitvraag, hergebruik, gegevens bij de bron, minimalisatie) |
| **BP07** | Overheidsorganisaties gebruiken open standaarden en open source | Worden Forum Standaardisatie-standaarden toegepast? | AP29–AP32 (open standaarden, open source, leveranciersonafhankelijkheid, herbruikbaarheid) |
| **BP08** | Overheidsorganisaties zijn transparant over hun dienstverlening | Is de werking en het presteren openbaar? | AP33–AP36 (prestatietransparantie, procesinrichting, verantwoording, algoritme transparantie) |
| **BP09** | Overheidsorganisaties zijn wendbaar en kunnen snel inspelen op veranderingen | Is het systeem aanpasbaar? | AP37–AP38 (wendbaarheid, schaalbaarheid) |
| **BP10** | Overheidsorganisaties gebruiken de Generieke Digitale Infrastructuur (GDI) | Wordt de GDI benut? | AP39–AP40 (GDI-gebruik, aansluiten bij GDI) |

## NORA Dochterarchitecturen (per bestuurslaag)

| Architectuur | Bestuurslaag | Domein | Beheerder | Kernfocus |
|-------------|-------------|--------|-----------|-----------|
| **NORA** | Alle overheden | Overkoepelend kader | ICTU / Logius | 10 basisprincipes, interoperabiliteit |
| **GEMMA** | Gemeenten | Gemeentelijke IT | VNG Realisatie | Zaakgericht werken, Common Ground, API-strategie |
| **PETRA** | Provincies | Provinciale IT | IPO | Provinciale processen, omgevingsvisies |
| **WILMA** | Waterschappen | Waterschaps-IT | Het Waterschapshuis | Waterbeheer, dijken, zuivering |
| **RORA** | Rijksoverheid | Rijks-IT | BZK/CIO-Rijk | Vervangt EAR sinds 2024; rijksbrede kaders |
| **MARIJ** | Rechtspraak | Rechtspraak-IT | IVO-Rechtspraak | Zaaksbehandeling rechtspraak, digitale toegang |

## Project Startarchitectuur (PSA) Checklist

Een PSA geeft op hoofdlijnen aan hoe een project invulling geeft aan de architectuur. Eis: elk overheids-IT-project moet een PSA hebben.

- [ ] **Scope**: Welke NORA-lagen en -principes zijn relevant?
- [ ] **Principes**: Welke basisprincipes en afgeleide principes zijn van toepassing?
- [ ] **Knelpunten**: Welke NORA-eisen conflicteren met projectdoelen?
- [ ] **Afwijkingen**: Welke 'leg uit'-punten zijn er? (pas toe of leg uit)
- [ ] **GDI**: Welke GDI-componenten worden gebruikt? (Digikoppeling, Digimelding, etc.)
- [ ] **Standaarden**: Welke Forum Standaardisatie-standaarden worden toegepast?
- [ ] **Beveiliging**: Hoe worden BP05 (BIV) aspecten ingevuld?
- [ ] **Privacy**: Hoe wordt omgegaan met BP04 (inzage/correctie)?
- [ ] **Dochterarchitectuur**: Is GEMMA/PETRA/WILMA/RORA correct toegepast?
- [ ] **Relaties**: Afhankelijkheden met andere systemen en GDI-componenten

## Generieke Digitale Infrastructuur (GDI) Componenten

NORA BP10 vereist gebruik van de GDI. Dit zijn de kerncomponenten:

| Component | Functie | Beheerder | NL-Voorziening |
|-----------|---------|-----------|----------------|
| **DigiD** | Authenticatie burgers | Logius | Verplicht voor burger-toegang tot overheidsdiensten met substantiële betrouwbaarheid |
| **eHerkenning** | Authenticatie bedrijven | Logius | Verplicht voor bedrijven-toegang |
| **Machtigen** | Machtigingsregister | Logius | Vertegenwoordiging regelen |
| **Berichtenbox** | Digitale post | MijnOverheid | Berichten van overheid aan burgers |
| **Digikoppeling** | Servicebus voor GDI | Logius | Gestandaardiseerde berichtuitwisseling (WUS, ebMS2, REST-API, Grote Berichten) |
| **Digilevering** | Event-gedreven data-levering | Logius | Wijzigingen in basisregistraties propageren |
| **Digimelding** | Terugmelding fouten | Logius | Burger/ambtenaar kan fouten in registraties melden |
| **Haal Centraal** | API's voor basisregistraties | VNG/Kadaster | Gemeentelijke API's voor BRP, BRK, BAG, etc. |
| **MijnOverheid** | Burgerportaal | Logius | Inzage in eigen gegevens (BP04) |
| **DigiToegankelijk** | Toegankelijkheid | Logius | EN 301 549 / WCAG 2.1 — verplicht voor alle overheidssites |
| **PKIOverheid** | Certificaten | Logius | Nederlands vertrouwensmodel, OV-certificaten voor publiek toegankelijke diensten (BIO2 5.14.02) |

Check: voor elk GDI-component — maakt het project er gebruik van of is er een gemotiveerde afwijking?

## 'Pas toe of leg uit' Mechanisme

Het 'comply or explain'-principe (NORA, Forum Standaardisatie):

1. **Pas toe** = standaard gebruiken zoals bedoeld
2. **Leg uit** = gemotiveerde afwijking documenteren:
   - Welke maatregelen zijn genomen om alsnog aan het doel te voldoen?
   - Waarom is de standaard niet toepasbaar?
   - Hoe wordt het achterliggende principe wel geborgd?
   - Wanneer wordt heroverwogen?

Een 'leg uit' is geldig, mits:
- Gedocumenteerd in PSA of projectdocumentatie
- Goedgekeurd door de architectuurboard
- Periodiek geherevalueerd
- Functioneel gelijkwaardig alternatief geboden

## Architectuurprincipes Validatie

Voor elke architectuurbeslissing, toets:

```
1. Welk NORA-basisprincipe raakt deze beslissing?
2. Welke afgeleide principes zijn van toepassing?
3. Voldoet de beslissing aan het principe?
   ├── Ja → documenteren in PSA
   └── Nee → Is er een "leg uit"?
       ├── Ja → Is de uitleg valide?
       │   ├── Ja → documenteren, goedkeuren door board
       │   └── Nee → HEROVERWEGEN
       └── Nee → HEROVERWEGEN
4. Heeft de beslissing impact op andere lagen? (5-lagencheck)
5. Is de beslissing compliant met de relevante dochterarchitectuur?
```

## Leveranciersselectie NORA-toets

Bij aanbestedingen en vendor-selectie:

- [ ] **Open standaarden**: Ondersteunt de oplossing Forum Standaardisatie-standaarden?
- [ ] **GDI-integratie**: Kan de oplossing koppelen met Digikoppeling, Haal Centraal, DigiD/eHerkenning?
- [ ] **Open source**: Is er een open-source alternatief overwogen? (BP07)
- [ ] **Vendor lock-in**: Welke exit-strategie is er? (BP07 — leveranciersonafhankelijkheid)
- [ ] **Data bij de bron**: Blijft data bij de bron of kopieert de oplossing data?
- [ ] **Toegankelijkheid**: Voldoet de oplossing aan DigiToegankelijk (WCAG 2.1)?
- [ ] **Architectuurfit**: Past de oplossing in het NORA-vijflagenmodel?

## Meer informatie

- [NORA Online](https://www.noraonline.nl) — volledige wiki met principes, kaders, en praktijkvoorbeelden
- [GEMMA Online](https://www.gemmaonline.nl) — gemeentelijke referentiearchitectuur
- [Forum Standaardisatie](https://www.forumstandaardisatie.nl/open-standaarden) — verplichte standaarden
- [GDI Overzicht](https://www.digitaleoverheid.nl/overzicht-van-alle-onderwerpen/generieke-digitale-infrastructuur-gdi/)
- [Digikoppeling](https://www.logius.nl/diensten/digikoppeling)
- [Common Ground](https://commonground.nl/) — gemeentelijke informatiekundige visie
