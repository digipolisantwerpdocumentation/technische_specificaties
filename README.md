# Technische Specificaties

*Deze bijlage geeft een overzicht van de technische specificaties en reikt tools aan om het product snel en kwalitatief te realiseren. In de titels wordt aangegeven welk onderdeel verplicht (**V**) of optioneel (**O**) is.*


Bij hyperlinks wordt aangegeven of de info:
1. publiek beschikbaar is: [**publiek**]
2. beschikbaar is via een actief medewerkersaccount: [**MW**]
3. beschikbaar is op het intranet via VPN: [**VPN**]

[Voor info types 2 en 3 kan u terecht bij de contactpersoon van Digipolis (zie offertevraag)]

[1. Architectuur](#1-architectuur)

[2. Technologieën](#2-technologieën)

[3. Ontwikkeltools](#3-ontwikkeltools)

[4. Testing](#4-testing)

[5. Architectuur](#5-technische-documentatie-v)

***


## 1. Architectuur

### 1.1. Algemeen
We verwachten dat de ontwikkelingen rekening houden met het maximaal gebruik van bestaande herbruikbare componenten zoals onze ACPaaS engines en ACPaaS front-end libraries waaronder de stijlbibliotheken.

Nieuwe componenten en services dienen zo generiek mogelijk te worden ontwikkeld volgens **Microservice Architectuur** zodat ze herbruikbaar en vervangbaar zijn.

Een algemene presentatie met deze architectuurprincipes: https://acpaas.digipolis.be/nl/docs/acpaas-principes-microservice-architectuur-sa2020 [**publiek**].

### 1.2. ACPaaS (V)
Een overzicht van alle ACPaaS engines en detailinfo is hier terug te vinden: https://acpaas.digipolis.be/nl/products [**publiek**].

Het gebruik van de **API/SDK engine** is verplicht. Meer informatie vind je hier: https://acpaas.digipolis.be/nl/docs/gebruik-van-api-engine [**publiek**].

Voor gebruikerstoegang en voor het ophalen en opslaan van gebruikersattributen dient het **A-profiel (burgers) en M-profiel (medewerkers)** te worden hergebruikt. Meer informatie vind je hier: https://acpaas.digipolis.be/nl/docs/identiteit-authenticatie-en-autorisatie [**publiek**].

### 1.3. Microservice Architectuur (**V**)

#### 1.3.1. Algemeen
Nieuwe functionaliteit wordt steeds gebouwd conform de microservice architectuur principes. Bestaande functionaliteit dient bij aanpassingen of refactor in lijn gebracht te worden met deze principes.
Meer informatie vind je op https://acpaas.digipolis.be/nl/docs/acpaas-principes-microservice-architectuur-sa2020 [**publiek**].

#### 1.3.2. Versioning (V)
Zie https://acpaas.digipolis.be/nl/docs/api-requirements [**publiek**].

#### 1.3.3. API Requirements (V)
Zie https://acpaas.digipolis.be/nl/docs/api-requirements [**publiek**].

#### 1.3.4. API monitoring (V)
Status call te voorzien voor elke API, zodat deze kan opgenomen worden in de status monitor (https://status-o.antwerpen.be/ [**VPN**]).

Meer info hoe deze te implementeren vind je hier: https://github.com/digipolisantwerpdocumentation/status-monitoring [**publiek**]

#### 1.3.5. Logging (**V**)
Logging is verplicht te voorzien voor alle cron jobs en voor privacy gevoelige info.
Hiervoor dient de ACPaaS logging engine gebruikt te worden:

https://acpaas.digipolis.be/nl/product/logging-engine [**publiek**].

Voor het raadplegen van de logging is altijd VPN vereist.


## 2. Technologieën

### 2.1. Algemeen: DAAS
Zie https://acpaas.digipolis.be/nl/docs/digipolis-antwerp-application-stack-daas [**publiek**].

### 2.2. Frontend (V)

#### 2.2.1. Digitale huisstijl (V)
Het design dient conform de huisstijlrichtlijnen van de stad Antwerpen te worden uitgevoerd. Bekijk alle documentatie op https://acpaas.digipolis.be/nl/docs/digitale-huisstijl [**publiek**].

#### 2.2.2. Technologieën (V)
Een overzicht van alle mogelijke technologieën kan je vinden op https://acpaas.digipolis.be/nl/docs/front-end-technologieen [**publiek**].

#### 2.2.3. Toegankelijkheid en WCAG (V)
In overeenstemming met de [Europese richtlijn omtrent toegankelijkheid](https://eur-lex.europa.eu/legal-content/NL/TXT/HTML/?uri=CELEX:32016L2102&from=EN) dienen alle apps en websites toegankelijk gemaakt te worden volgens WCAG 2.1 niveau AA. Meer info op https://acpaas.digipolis.be/nl/docs/toegankelijkheid-websites-en-mobieleapps-einclusie-en-wcag [**publiek**].


### 2.3. Backend (V)
Alle documentatie over de verschillende technologieën en database mogelijkheden is te vinden op https://acpaas.digipolis.be/nl/docs/backend-technologieen [**publiek**].


## 3. Ontwikkeltools
### 3.1. Application Lifecycle Management

#### 3.1.1 Jira (V)
Nieuwe functionaliteiten worden in de vorm van epics en stories ingebracht in Jira. Hier gebeurt ook de bugtracking en projectopvolging. Gebruik van de Jira Workflow binnen Digipolis is verplicht.

#### 3.1.2 BitBucket (V)
Zowel de front- als backend code van iedere applicatie zit in een eigen Git Repository die beheerd wordt binnen BitBucket. Codewijzigingen worden via pull requests gereviseerd door 2 ontwikkelaars. Er worden zowel voor front- als backend 3 ontwikkelaars doorgegeven die als approver kunnen geselecteerd worden.

Er moet dagelijks gecommit worden, vermijden om branches langer dan een paar dagen open te laten staan.

#### 3.1.3 Bamboo (V)
Meer info over de opzet: https://bitbucket.antwerpen.be/projects/PLAT/repos/documentation/browse/Bamboo.md [**MW**]

### 3.2. Vagrant (**O**)
voor lokale development: https://bitbucket.antwerpen.be/projects/ASTAD/repos/vagrant_chef_ruby/browse [**MW**]

### 3.3. Docker (**O**)
Beschikbaar voor local development. Er is een traject bezig om Docker op te nemen in de Application Lifecycle Management tools.

### 3.4. App Config (**O**)
Optioneel voor nieuwe apps: https://appconfig.antwerpen.be/ [**VPN**]


## 4. Testing
Zie https://acpaas.digipolis.be/nl/docs/testing [**publiek**].


## 5. Technische documentatie (V)
API / applicatie documentatie beschikbaar stellen in **readme.md**, **swagger.json**, **changelog.md** formaat, verwijzing naar kibana monitor opnemen.
