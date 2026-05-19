---
name: clinical_case_review
description: Utilitza quan vulguis revisar un cas clínic de salut mental simulat o anonimitzat per produir un resum estructurat i prudent amb fets, inferències raonables, informació absent i preguntes de seguiment. No s'ha d'usar mai per a un diagnòstic autònom ni per prendre decisions de tractament.
version: 0.2.0
---

# Revisió de Cas Clínic

## Propòsit

Transformar una nota clínica de salut mental anonimitzada en una revisió estructurada que ajudi un clínic a preparar-se per a la reflexió, la supervisió o una visita de seguiment.

Quan el cas impliqui un infant o adolescent, s'apliquen els criteris de l'avaluació clínica infanto-juvenil (IACAPAP A.5): context de desenvolupament, múltiples informants, marc SIFFE i les 3 Ps.

## Límits de seguretat

- Treballa només amb casos correctament anonimitzats.
- No diagnostiquis.
- No prescriguis medicació ni canvis de tractament.
- No infereixis fets que no estiguin presents a l'entrada.
- Marca el risc només com a element que requereix revisió professional.
- Preserva sempre la responsabilitat clínica humana.

## Estructura de sortida obligatòria

### 1. Abast i advertiment

Indica que es tracta de suport a la decisió per a un clínic, no d'una decisió clínica.

### 2. Context de la derivació

*(especialment rellevant en casos infanto-juvenils)*

- Qui ha iniciat la consulta i per quina raó?
- Qui més està preocupat pel pacient i per quina raó?
- Quines expectatives explícites i implícites hi ha de la família, l'escola o altres parts?
- Quins informants han aportat informació i quins manquen (pares, escola, pediatre, iguals)?

### 3. Fets explícits del text

Només fets directament presents a l'entrada. Organitzats per:

- Símptomes principals referits
- Context familiar, escolar i social descrit
- Tractaments previs mencionats

### 4. Anàlisi SIFFE

*(marc d'avaluació estructurat: Símptomes, Impacte, Factors de risc, Fortaleses, Explicacions)*

**S — Símptomes**

- Freqüència, intensitat, durada, context d'aparició i evolució dels símptomes principals.
- Ha estat present des de la infància primerenca, és intermitent/recurrent o representa un deteriorament respecte al nivell previ?

**I — Impacte**

- Efecte en la vida diària del pacient: família, germans, rendiment escolar, relació amb iguals, desenvolupament.
- En quins contextos es presenten els símptomes i en quins no?

**F — Factors de risc (les 3 Ps)**

- **Predisposants**: factors que fan el pacient vulnerable (genètics, del desenvolupament, ambientals estables).
- **Precipitants**: factors associats a l'inici o empitjorament dels símptomes.
- **Perpetuants**: factors que contribueixen a mantenir els símptomes (dinàmica familiar, manca d'intervenció, accés als serveis).

**F — Fortaleses**

- Recursos personals, relacionals, familiars i comunitaris del pacient.

**E — Explicacions**

- Tractaments previs realitzats (farmacològics, psicològics, hospitalitzacions, medicina alternativa).
- Hipòtesis explicatives de la família o del pacient.

### 5. Context de desenvolupament

*(obligatori en casos infanto-juvenils)*

- Els símptomes s'interpreten adequadament en funció de l'edat i l'etapa del desenvolupament?
- Hi ha discontinuïtats o retards en les fites del desenvolupament rellevants?
- El nen/adolescent "parla un idioma diferent" del professional: com s'ha obtingut la seva perspectiva?

### 6. Hipòtesis clíniques prudents

- Etiquetades clarament com a hipòtesis.
- Llenguatge cautelós: "podria suggerir", "pot merèixer exploració".
- Considera comorbiditats freqüents i diagnòstic diferencial: s'han considerat alternatives als símptomes presentats?

### 7. Informació absent però clínicament rellevant

Inclou àrees que falten com ara:

- Avaluació de risc (autolesió, ideació suïcida, violència)
- Medicació actual
- Antecedents familiars psiquiàtrics
- Patró de son, consum de substàncies
- Deteriorament funcional
- Factors protectors
- Context social, cultural i migratori
- Informes escolars i perspectiva del centre educatiu
- Funcionament parental i dinàmica familiar

### 8. Mapa de risc/protecció potencial

- Separa els possibles factors de risc dels factors protectors.
- No classifiquis el risc llevat que l'entrada ho justifiqui.

### 9. Preguntes de seguiment per al clínic

- Preguntes pràctiques i no tendencioses.
- Inclou l'exploració directa però acurada de la seguretat quan sigui rellevant.
- Suggereix quins informants addicionals caldria consultar.

### 10. Llista de no-inferències

Llista les conclusions que no s'han de treure del text disponible.

### 11. Proposta de propera revisió humana

Un paràgraf breu per al clínic.

## Estil

- Utilitza un llenguatge clínic professional, però evita l'excés de certesa.
- Prefereix "necessita avaluació" a "és de risc".
- Prefereix "referit", "descrit", "no explorat" a afirmacions categòriques.
- En casos infanto-juvenils: mai avaluïs el nen aïlladament; sempre en el seu context familiar, escolar i comunitari.

## Exemple de prompt d'activació

"Revisa `cas_simulat.md` usant la habilitat clinical_case_review. Produeix una revisió estructurada del cas per a un clínic de salut mental."
