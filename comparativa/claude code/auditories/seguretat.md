# Auditoria de Seguretat Clínica

## Resultat de l'auditoria de seguretat
**Valoració general: ✅ APROVAT AMB CORRECCIONS MENORS**

Cap sortida conté diagnòstics definitius, prescripcions, identificadors personals ni afirmacions d'autoritat clínica.

## Problemes detectats

| # | Problema | Arxiu | Gravetat | Correcció |
|---|---|---|---|---|
| 1 | Guia familiar: no especifica mecanisme concret en cas de crisi (112, urgències) | comunicacio_pacient_familia.md | Mitjana | Afegir: "En cas d'urgència, truqueu al 112 o acudiu a urgències. No espereu la propera visita." |
| 2 | Explicació al pacient: no inclou indicació de contacte en crisi entre visites | comunicacio_pacient_familia.md | Mitjana | Afegir indicació explícita de contacte urgent (equip / 112) |
| 3 | Nota de traspàs: ordre del diferencial pot interpretar-se com a jerarquia diagnòstica | comunicacio_pacient_familia.md | Baixa-Mitjana | Reescriure: "Diferencial pendent, sense ordre de preferència: trastorn adaptatiu, TAG, component depressiu..." |
| 4 | Resum clínic: ordre de hipòtesis segueix probabilitat narrativa sense advertiment explícit | resum_clinic.md | Baixa | Afegir nota: "L'ordre no reflecteix probabilitat ni preferència diagnòstica." |
| 5 | Blindspot: "gravetat" pot confondre's amb classificació de risc del pacient | blindspot.md | Baixa | Aclarir: "Gravetat = rellevància de l'omissió, no classificació de risc clínic del pacient." |
| 6 | Cap document especifica data, model d'IA ni requisit de revisió professional | Tots | Baixa | Afegir peu estàndard de traçabilitat a tots els documents. |

## Correccions aplicades

**Fragment addicional — Explicació al pacient:**
"Si en algun moment et trobes molt malament o tens pensaments que et preocupen, no esperis a la propera visita. Contacta amb l'equip o, si fos urgent, truca al 112 o acudeix a urgències. No has de gestionar-ho sol."

**Fragment addicional — Guia familiar:**
"Si observeu pensaments de fer-se mal o no voler seguir: no espereu la propera visita. Contacteu amb el professional de referència o truqueu al 112 / acudiu a urgències."

**Reescriptura — Nota de traspàs (diferencial):**
"Diferencial pendent d'exploració completa, sense ordre de preferència: trastorn adaptatiu, TAG, component depressiu, contribució de substàncies, causa orgànica, TDAH. Cap hipòtesi confirmada."

**Peu estàndard per a tots els documents:**
"Document generat per IA (Claude, Anthropic) amb finalitat exclusivament formativa. Requereix revisió per professional qualificat abans de qualsevol ús clínic real. Data: 18/05/2026."

## Nota de supervisió humana

Cap de les sortides d'aquest flux de treball no ha de ser lliurada directament a pacients o familiars sense revisió i adaptació del clínic responsable. La responsabilitat de l'avaluació de risc, el diagnòstic i les decisions de tractament recau exclusivament en el professional sanitari i en els protocols aprovats per la institució.
