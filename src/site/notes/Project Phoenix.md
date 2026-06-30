---
{"dg-publish":true,"permalink":"/project-phoenix/"}
---

# Project Phoenix

## Inleiding

GitHub heeft net aangekondigd dat ze 12-18 maanden geen nieuwe features gaan bouwen. Ze zijn volledig gefocust op hun migratie naar Azure omdat hun infrastructuur het niet meer aankan. GitLab is ondertussen een log alles-in-één platform geworden dat probeert elk probleem op te lossen maar er geen echt goed oplost.

Dit is ons moment.

**Het probleem:** Ontwikkelplatforms zijn gecentraliseerde monopolies waar je vendor lock-in hebt, geen controle over je data, en waar AI slechts een add-on is - een slim autocomplete-feature in plaats van een fundamenteel onderdeel van hoe je software bouwt.

**De oplossing:** Een platform gebouwd op twee principes:

1. **Federatie** - Net zoals e-mail werkt: je kan je eigen server draaien (`git.jouwbedrijf.nl`) maar nog steeds naadloos samenwerken met projecten op andere servers. Volledige controle over je data, zonder het verlies van samenwerking. Geen vendor lock-in.

2. **AI-Native** - In plaats van AI achteraf toevoegen, bouwen we het platform eromheen. Een "App Store voor AI Agents": gespecialiseerde experts die je installeert in je project. Een agent die automatisch tech debt tracked, een die code reviews doet, een die je coacht wanneer tickets vastlopen. AI is niet een feature, maar een teamlid.

**Waarom dit werkt:** GitHub en GitLab plakken AI bovenop een bestaande architectuur. Wij bouwen vanaf nul met AI als kernprincipe. Zij blijven gecentraliseerde platforms. Wij geven je vrijheid via federatie. Het verschil tussen een elektrische motor in een oude auto proppen versus een Tesla ontwerpen.

---

## Hoofdstuk 1: Waarom Nu?

### De GitHub Situatie

In oktober 2025 kondigde GitHub aan dat ze feature development pauzeren voor 12-18 maanden om te migreren naar Azure. Intern noemt CTO Vladimir Fedorov dit "existentieel" - hun datacenters kunnen de groei van AI-workloads niet meer aan. CEO Thomas Dohmke vertrok in augustus 2024, en GitHub is nu volledig opgeslokt door Microsoft.

Dit toont aan: gecentraliseerde platforms kunnen niet schalen voor de AI-era zonder nog afhankelijker te worden van één grote cloud provider. En hun klanten betalen door, zonder nieuwe features te krijgen.

*Bron: [The New Stack](https://thenewstack.io/github-will-prioritize-migrating-to-azure-over-feature-development/)*

### Onze Aanpak: Twee Kernprincipes

**1. Federatie = Vrijheid zonder isolatie**

Net zoals e-mail: jij draait `git.jouwbedrijf.nl`, ik draai `git.mijnbedrijf.nl`, maar we kunnen naadloos samenwerken. Jouw data blijft bij jou, maar je bent niet geïsoleerd. Geen vendor lock-in, geen gedwongen migraties, geen "we pauzeren features voor een jaar".

**2. AI-Native = Agents als teamleden**

Niet "AI-autocomplete als feature", maar een platform ontworpen rond AI vanaf dag één. Gespecialiseerde agents die je installeert: één tracked tech debt, één doet security scans, één coacht teamleden bij vertraagde tickets. Ze draaien autonoom, hebben context van je hele project, en zijn uitwisselbaar via een marketplace.

GitHub plakt Copilot op een 15 jaar oud platform. Wij bouwen het platform rond de agents heen.

---

## Hoofdstuk 2: De Killer Feature: De AI Agent Marketplace

Dit is de "App Store" voor je project, waar je gespecialiseerde AI-experts installeert. Een agent is een pakket met kennis en gereedschappen (in een veilige WASM-module).

### Voorbeelden van Agents

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
