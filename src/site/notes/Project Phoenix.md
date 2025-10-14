---
{"dg-publish":true,"permalink":"/project-phoenix/"}
---

## Inleiding: De Volgende Generatie Softwareontwikkeling

Stel je een wereld voorbij GitHub voor. Een wereld waar je niet vastzit aan het ecosysteem van één bedrijf, en waar AI niet zomaar een slimme typ-assistent is, maar een proactief, volwaardig lid van je dev team. Dit document schetst de visie voor een nieuw soort ontwikkelplatform, gebouwd op twee revolutionaire principes: **Federatie** en een **AI-Native architectuur**.

Waarom is dit een goed idee?

1.  **Het doorbreekt de "gouden kooi" van GitHub/GitLab.** In plaats van één gecentraliseerd platform (zelfs als je het zelf host), creëren we een open netwerk van samenwerkende servers (federatie). Dit geeft individuen en bedrijven volledige controle over hun eigen data (data soevereiniteit) zonder het vermogen tot samenwerking te verliezen. Denk aan hoe e-mail werkt: een Gmail-gebruiker kan naadloos communiceren met iemand die zijn eigen server host.
2.  **Het herdefinieert de rol van AI.** In plaats van AI als een add-on (AI-assisted), bouwen we het platform vanaf de grond op rondom AI (AI-native). De kern van het platform is een "App Store voor AI Agents": gespecialiseerde, autonome experts die je kunt installeren in je project. Je wijst geen taken meer toe aan alleen mensen, maar ook aan AI-teamleden die code schrijven, reviews uitvoeren, processen bewaken en je coachen. De rol van de ontwikkelaar verschuift van *schrijver* naar *architect en dirigent* van een gemengd team van mensen en AI.

Dit is geen betere GitHub-kloon; dit is een fundamenteel nieuwe manier van software bouwen.

---

## Hoofdstuk 1: De Kernfilosofie

### GitLab is een Zwitsers Zakmes, Wij bouwen een Formule 1 Pitcrew

*   **GitLab/GitHub:** Een alles-in-één platform met elke denkbare tool. Handig, maar log en niet altijd de beste tool voor elke specifieke taak.
*   **Ons Platform:** Een team van hyper-gespecialiseerde experts (de AI-agents) die perfect samenwerken met maar één doel: jouw code en proces zo snel en efficiënt mogelijk maken.

### Federatie: De Universiteitsbibliotheek Analogie

Federatie lost de spanning op tussen "controle over mijn data" en "samenwerken met anderen".

*   Stel je voor dat jouw bedrijf zijn eigen, private bibliotheek heeft (`git.jouwbedrijf.nl`).
*   Als je wilt samenwerken met een partner, hoef je niet naar hun bibliotheek. Je vraagt vanuit je *eigen* bibliotheek een boek aan.
*   Jouw server (de bibliothecaris) regelt de communicatie op de achtergrond. Het project van de partner verschijnt naadloos in jouw dashboard, terwijl de data veilig bij de partner blijft. Je hebt controle én kunt samenwerken.

---

## Hoofdstuk 2: De Killer Feature: De AI Agent Marketplace

Dit is de "App Store" voor je project, waar je gespecialiseerde AI-experts installeert. Een agent is een pakket met kennis en gereedschappen (in een veilige WASM-module).

### Voorbeelden van Agents:

#### Proces & Management
*   **De Scrum Coach:** Coacht teamleden privé als tickets vertragen en biedt hulp aan.
*   **De Scrum Master Assistent:** Faciliteert stand-ups, werkt statistieken bij en bewaakt het proces.
*   **De Proces Analist:** Observeert de workflow en geeft datagedreven advies ("De review-tijd is met 30% gestegen, de oorzaak ligt hier...").

#### Code & Kwaliteit
*   **De Wachter:** Draait op elke commit, scant op bugs, security en performance. Een onvermoeibare kwaliteitsbewaker.
*   **De Tech Debt Accountant:** Vindt `TODO`s en complexe code, en maakt er automatisch tickets van in de backlog.
*   **De Legacy Modernizer:** Refactort oude code stap-voor-stap naar moderne standaarden.

#### Team & Samenwerking
*   **De Onboarding Buddy:** Geeft nieuwe teamleden een persoonlijke rondleiding door de codebase.
*   **De Kennis Delver:** Ziet wie aan welke code werkt en stelt automatisch de juiste reviewers voor.

#### Infrastructuur & Operations
*   **De Cloud Kosten Optimalisator:** Sluit automatisch test-omgevingen af die niet meer gebruikt worden.
*   **De Incident Assistent:** Start bij een productie-alarm direct een "war room", verzamelt logs en data, en wijst een waarschijnlijke oorzaak aan.

---

## Hoofdstuk 3: De Ideale Technologiestack

*   **Backend: Elixir & Phoenix LiveView**
    *   **Waarom?** Ongeëvenaard in het bouwen van schaalbare, real-time en fouttolerante systemen. Perfect voor de federatieve en live-updating aard van het platform. LiveView zorgt voor extreme productiviteit door frontends te bouwen met pure backend-code.
*   **AI/ML Backend: Python**
    *   **Waarom?** Het ecosysteem (PyTorch, Hugging Face) is onmisbaar voor de AI-functionaliteit. Draait als een aparte service.
*   **Database: PostgreSQL + een Vector Database**
    *   **Waarom?** PostgreSQL voor de relationele data (gebruikers, projecten). Een gespecialiseerde Vector DB voor het "geheugen" van de AI-agents (RAG).
*   **Agent Tools: WebAssembly (WASM)**
    *   **Waarom?** Biedt een veilige, gesandboxte manier om de gereedschappen van derden (uit de marketplace) uit te voeren.

---

## Hoofdstuk 4: Verdienmodel & Licentie

### Verdienmodel (Hybride)
1.  **SaaS (Freemium):** Een gratis basisversie op ons hosted platform.
2.  **Pro (Upsell):** Betaalde toegang tot de beste AI-modellen en geavanceerde agents.
3.  **Enterprise:** Een licentie voor grote bedrijven die zelf willen hosten, met extra features en de "Bring Your Own Key" optie voor LLM's.
4.  **Marketplace Cut:** Een percentage van de verkoop van agents door derden.

### Licentie: Business Source License (BSL)

*   **De "Bakkerij Recept" Analogie:** We publiceren ons recept (broncode) openlijk. Iedereen mag het gebruiken, **behalve** om een directe, concurrerende commerciële hostingdienst te starten.
*   **De Belofte:** Na een periode van 3-4 jaar wordt de licentie automatisch omgezet in een volledig open-source licentie (bv. Apache 2.0).
*   **Waarom?** Het beschermt ons bedrijf in de beginjaren, terwijl het de community vertrouwen en de garantie van uiteindelijke vrijheid geeft.

---

## Conclusie

Dit project gaat niet over het bouwen van een incrementele verbetering. Het gaat over het creëren van een paradigmaverschuiving in hoe we software conceptualiseren, bouwen en beheren, door de kracht van federatie en een diepe, architecturale integratie van AI te omarmen.
