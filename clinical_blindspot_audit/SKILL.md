---
name: clinical_blindspot_audit
description: Utilitza quan vulguis auditar un resum clínic, una revisió de cas de salut mental o una nota clínica generada per IA per detectar omissions, supòsits ocults, tancaments prematurs, estigma, ancoratge i preguntes contextuals que falten.
version: 0.2.0
---

# Auditoria de Punts Cecs Clínics

## Propòsit
Identificar allò que un clínic o un resum generat per IA pot estar passant per alt. Aquesta habilitat s'inspira en la revisió de "punts cecs": cerca omissions, supòsits ocults, conclusions prematures i oportunitats desaprofitades.

Quan el cas impliqui un infant o adolescent, s'apliquen dimensions addicionals derivades dels criteris de l'avaluació clínica infanto-juvenil (IACAPAP A.5).

## Entrades
- Text original del cas.
- Resum generat per IA o esborrany de nota.
- Qualsevol criteri clínic local o política de seguretat.

## Dimensions de l'auditoria

### Dimensions generals

1. **Informació absent**
   - Quina informació clínicament rellevant manca?
   - L'absència queda marcada clarament com "no explorada" en lloc de tractar-se com a negativa?

2. **Tancament prematur**
   - El text salta massa ràpidament a una sola explicació?
   - S'ignoren alternatives diagnòstiques o de comorbiditat?

3. **Supòsits ocults**
   - S'estan fent supòsits socioeconòmics, familiars, de gènere, culturals, migratoris o educatius?

4. **Infradetecció de risc**
   - Estan insuficientment explorats la seguretat, l'autolesió, la violència, el consum de substàncies, la protecció o el deteriorament funcional?

5. **Sobredetecció de risc**
   - La sortida exagera el risc més enllà de l'evidència?

6. **Estigma i enquadrament**
   - El llenguatge moralitza, culpabilitza, patologitza o medicalitza en excés la persona?

7. **Factors protectors i fortaleses**
   - Es noten les fortaleses, les relacions, la motivació, les rutines i la conducta de cerca d'ajuda?

8. **Preguntes de seguiment accionables**
   - Genera preguntes que un clínic podria fer a continuació.

### Dimensions específiques per a casos infanto-juvenils
*(aplica sempre que el pacient sigui un infant o adolescent)*

9. **Avaluació aïllada del nen**
   - S'ha avaluat el nen sense considerar el context familiar, escolar i comunitari?
   - El nen mai s'ha d'interpretar en aïllament: els símptomes poden reflectir un trastorn subjacent, una incompatibilitat amb l'entorn, o un problema dins l'ambient.

10. **Font i motiu real de la derivació**
    - S'ha identificat qui ha iniciat la consulta i per quina raó? (¿De quién es el problema? ¿Por qué ahora?)
    - Les expectatives dels diferents actors (pares, escola, pediatre, el propi nen) estan explorades o s'assumeix que coincideixen?

11. **Perspectiva múltiple d'informants**
    - S'ha considerat la informació de pares, educadors, pediatre i altres cuidadors?
    - El desacord entre informants s'ha tractat com a dada clínica, no com a problema a resoldre?
    - Nota: els nens són millors informants dels símptomes internalitzants; els pares, dels externalitzants.

12. **Context de desenvolupament ignorat**
    - Els símptomes s'interpreten sense tenir en compte l'edat i l'etapa del desenvolupament?
    - Existeixen discontinuïtats o retards en les fites evolutives que no s'han considerat?
    - La presentació dels símptomes és diferent en nens petits vs. adolescents (p.ex., depressió, TEPT)?

13. **Marc SIFFE incomplet**
    - **S** — Freqüència, intensitat, durada i evolució dels símptomes principals: explorats?
    - **I** — Impacte en família, escola, iguals i desenvolupament: explorat?
    - **F** — Factors de risc (les 3 Ps): predisposants, precipitants i perpetuants identificats?
    - **F** — Fortaleses del nen, la família i l'entorn: identificades?
    - **E** — Explicacions i tractaments previs: recollits?

14. **Les 3 Ps de factors de risc no aplicades**
    - S'han confós factors de risc sense distingir si predisposen, precipiten o perpetuen?
    - Els factors perpetuants (dinàmica familiar inadequada, manca d'intervenció, accés limitat a serveis) sovint s'ignoren però són els més modificables.

15. **Psicopatologia parental no considerada**
    - La percepció dels pares sobre el nen pot estar esbiaixada per la seva pròpia salut mental (p.ex., una mare deprimida pot valorar més negativament la conducta del fill)?
    - S'ha notat o descartat aquesta possibilitat?

16. **Context escolar absent**
    - Manquen informes escolars o la perspectiva del centre educatiu?
    - Un declivi acadèmic abrupte o gradual, grans diferències entre assignatures, o comentaris sobre problemes socials/emocionals són senyals que cal recollir rutinàriament.

17. **Comorbiditats i diagnòstic diferencial no explorats**
    - La comorbiditat és extremadament freqüent en salut mental infanto-juvenil: s'ha considerat?
    - Símptomes com irritabilitat poden correspondre a depressió, trastorn bipolar, TDAH, ansietat: s'han considerat alternatives?

## Format de sortida
Utilitza una taula amb les columnes:
- Punt cec
- Per què importa
- Evidència al text
- Pregunta suggerida per al clínic
- Gravetat: Baixa / Mitjana / Alta

Afegeix-hi un breu apartat de "consells de revisió".

## Limitacions
- No generis un diagnòstic.
- No suggereixis decisions de tractament.
- No afirmis que el risc és present quan només és no avaluat.
