---
name: clinical_demo_orchestrator
description: Utilitza quan vulguis fer una demostració completa de formació per a clínics hospitalaris, mostrant com les habilitats d'IA poden revisar un cas de salut mental simulat, generar sortides per a audiències diverses, detectar punts cecs i auditar la seguretat.
version: 0.1.0
---

# Orquestrador de Demo Clínica

## Propòsit
Executar una demostració completa i segura per a clínics, usant únicament casos de salut mental simulats o anonimitzats.

## Seqüència de la demo

### Pas 0 — Verificació de seguretat
Abans de fer res, verifica que el cas està anonimitzat, no hi ha identificadors personals. Si l'entrada inclou noms, identificadors, telèfons, adreces, dates de naixement exactes o altres identificadors, para i demana l'anonimització.

La sortida és només per a formació o suport al clínic.

### Pas 1 — Revisió estructurada del cas
Invoca el flux de treball clinical_case_review:
- Fets
- Hipòtesis prudents
- Informació absent
- Mapa de risc/protecció
- Preguntes de seguiment
- Llista de no-inferències

Desa a:
`sortides/resum_clinic.md`

### Pas 2 — Transformació de la comunicació
Invoca el flux de treball patient_family_communication:
- Explicació per al pacient
- Guia de conversa per a la família
- Nota de traspàs breu per al clínic

Desa a:
`sortides/comunicacio_pacient_familia.md`

### Pas 3 — Auditoria de punts cecs
Invoca el flux de treball clinical_blindspot_audit:
- Informació absent
- Supòsits ocults
- Tancament prematur
- Infradetecció/sobredetecció de risc
- Estigma
- Factors protectors

Desa a:
`auditories/blindspot.md`

### Pas 4 — Auditoria de seguretat
Invoca el flux de treball clinical_safety_audit sobre totes les sortides generades.
Produeix:
- Aprovat / Aprovat amb correccions / No s'ha d'usar
- Problemes detectats
- Versió corregida
- Nota de supervisió humana

Desa a:
`auditories/seguretat.md`

### Pas 5 — Debriefing per a clínics
Conclou amb un debriefing docent concís:
- En què ha ajudat la IA
- Què no podia saber
- On el judici humà ha estat essencial
- Com es podria governar institucionalment el flux de treball

Desa a:
`auditories/debriefing.md`

## Guió de demo per al presentador
Utilitza aquest enquadrament verbal:

> "Això no és un sistema diagnòstic. És un flux de treball estructurat de lectura, resum, comunicació i auditoria. El valor clau no és l'automatització del judici, sinó fer visibles els supòsits, les omissions i les incerteses."

## Missatge final obligatori
Conclou sempre amb:

> La responsabilitat clínica final recau en el professional sanitari i en els protocols aprovats per la institució.
