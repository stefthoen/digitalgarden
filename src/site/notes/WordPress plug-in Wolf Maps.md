---
{"dg-publish":true,"permalink":"/word-press-plug-in-wolf-maps/"}
---

Tags: #develop
# Elementen
- Invoerveld token
- Import/Sync button: Download locaties van alle kaarten
- Optioneel: 
	- Toon documentatie voor developer met namen van velden die gebruikt kunnen worden om custom fields op te halen en te tonen.
	- Toon shortcodes die gebruikt kunnen worden om metadata te tonen.
# Metadata
Metadata die op het Custom Post Type moet worden opgeslagen:
- name 
- subtitle 
- description
- postalcode 
- city
- address
- email
- website
- image
- video
- category
- tags
# API 
- Voeg `X-API-KEY` header toe
- Base URL is api.wolfmaps.nl
- image is een cloudinary ID, die haal je op als volgt
https://res.cloudinary.com/studio-wolf/images/g_auto,c_fill,h_405,w_720,f_auto,q_auto/{IMAGE_ID}/{EIGEN_SLUG}. `{EIGEN_SLUG}` is een zelfverzonnen bestandsnaam die het bestand krijgt.
## Calls:
* `/maps`: Haal alle maps voor een team op
- `/maps/{mapId}/features`: Haal alle locaties van een kaart op
- `/maps/{mapId}/categories`: Haal alle categorieen voor een kaart op
- `/maps/{mapId}/tags`: Haal alle tags voor een kaart op
- `/batch/<map_pk>`: Haal *alles* voor een kaart op
# Oplossing
- Bij het drukken van de {Import} knop, download hij alle locaties. Ik heb tevens een lijst met locale locaties (Custom Post Type).
- Ik loop door de locaties heen. 
	- Als een locatie ID lokaal nog niet bestaat, maak ik een nieuwe Location CPT custom post type (CPT) aan. 
	 - Voor elke locatie weet ik wanneer hij voor het laatst is geupdate (updatedAt). Als de locatie lokaal ouder is dan die in de API, dan overschrijf ik alle metadata.
