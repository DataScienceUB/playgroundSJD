# Auditoria de Seguretat Clínica
> Generat per: clinical_safety_audit | Data: 2026-05-18 | Ús: Formació clínica / suport a la decisió

---

## Resultat de l'auditoria de seguretat

**Valoració general: ✅ APROVAT AMB CORRECCIONS**

Les tres sortides compleixen els criteris fonamentals de seguretat. No hi ha línies vermelles infranquejables. S'identifiquen quatre correccions necessàries i tres observacions menors.

---

## Problemes detectats

| # | Document afectat | Problema | Gravetat | Per què importa | Correcció |
|---|---|---|---|---|---|
| 1 | `comunicacio_pacient_familia.md` — Guia familiar | **Absència d'indicadors d'urgència per a la família** | 🔴 ALTA | Si el pacient expressa ideació autolítica entre sessions, la família no té instruccions de quan actuar. Omissió de seguretat real, no formal. | Afegir secció "Quan cal actuar de manera urgent" amb instruccions clares i derivació als serveis d'urgències o al professional referent. |
| 2 | `comunicacio_pacient_familia.md` — Explicació al pacient | **El pacient no és preparat per a la pregunta de seguretat** | 🟠 ALTA | La pregunta directa sobre ideació autolítica pot sorprendre i generar resistència si no s'emmarca prèviament. | Afegir: "En les primeres visites, pregunto directament si has tingut pensaments de fer-te mal. No és perquè pensi que en tens, sinó perquè és una cosa que volem entendre amb tothom." |
| 3 | `sortides/resum_clinic.md` — SIFFE / Factors perpetuants | **"Dinàmica familiar invalidant" com a afirmació, no com a hipòtesi** | 🟡 MITJANA | Terme clínicament carregat basat únicament en la perspectiva del pacient. Pot introduir biaix de confirmació en el clínic lector. | Substituir per: "Percepció del pacient de manca de comprensió per part dels pares (pendent de contrast amb col·lateral familiar; no confirmat)." |
| 4 | `auditories/blindspot.md` — Punt 2 (TDAH) | **Gravetat "Alta" per a una hipòtesi diagnòstica, no per a un risc de seguretat** | 🟡 BAIXA | Classificar el TDAH com "Alta" al costat del risc autolític pot distorsionar la percepció de prioritats. Gravetat "Alta" hauria de reservar-se a riscos de seguretat. | Rebaixar a 🟡 MITJANA i afegir: "Hipòtesi a explorar en visites posteriors; no requereix acció immediata." |

---

## Verificacions amb resultat satisfactori

| Criteri | `resum_clinic.md` | `comunicacio_pacient_familia.md` | `blindspot.md` |
|---|---|---|---|
| Absència de diagnòstics definitius | ✅ H1–H6 clarament etiquetades com a hipòtesis | ✅ Cap diagnòstic al pacient ni a la família | ✅ Suggeriments d'exploració, no diagnòstics |
| Absència de prescripcions o tractaments | ✅ PHQ-9/GAD-7 mencionats com a instruments de cribatge (correcte) | ✅ Cap | ✅ Cap |
| Absència d'identificadors personals | ✅ Cas simulat sense identificadors | ✅ Cap | ✅ Cap |
| Risc autolític marcat com a no explorat | ✅ Marcat amb prioritat explícita | ⚠️ No prepara el pacient (corregir) | ✅ Prioritat #1 de la taula, 🔴 Alta |
| Absència de falsa tranquil·litat | ✅ | ✅ | ✅ |
| Absència d'estigma i culpabilització | ✅ (amb correcció #3) | ✅ Llenguatge validador i no estigmatitzador | ✅ |
| Advertiments de responsabilitat clínica | ✅ Header i footer | ✅ Footer | ✅ Footer |
| Traçabilitat de les inferències | ✅ Hipòtesis relacionades amb símptomes explícits | ✅ Contingut basat en fets del cas | ✅ Cada punt remet a evidència o absència al text |
| Hipòtesis etiquetades com a tals | ✅ | ✅ | ✅ |
| Absència d'excés d'afirmació sobre gravetat/pronòstic | ✅ | ✅ | ✅ (amb correcció #4) |

---

## Notes menors

**A — `comunicacio_pacient_familia.md`:** La frase "Tot això té sentit com a resposta del cos i la ment a una situació que s'ha anat acumulant" és validadora però podria normalitzar un possible trastorn. S'accepta en context de primera comunicació empàtica. Opcionalment afegir: "...encara que el professional que t'atén necessita entendre millor com t'afecta per poder ajudar-te de manera adequada."

**B — `comunicacio_pacient_familia.md`:** La frase "La millora del funcionament acadèmic habitualment segueix la millora del benestar, no al revés" és una generalització. Afegir qualificador: "En molts casos, la millora del funcionament acadèmic tendeix a seguir la millora del benestar, tot i que cada persona és diferent."

---

## Versions corregides

**Correcció #1 i #2 — Addició a `comunicacio_pacient_familia.md`:**

*A l'explicació per al pacient, afegir al final:*
> "Una cosa que et vull dir: en les primeres visites, acostumo a preguntar directament si has tingut pensaments de fer-te mal o de no voler continuar. No ho faig perquè pensi que estàs en aquella situació, sinó perquè és una pregunta que fem amb tothom per entendre com estàs de veritat. Pots respondre amb total llibertat."

*A la guia familiar, afegir secció nova:*
> **Quan cal actuar de manera urgent**
> Si en algun moment la persona expressa pensaments de fer-se mal, de no voler continuar o de desaparèixer, o si observeu un canvi brusc i preocupant en el seu comportament, no espereu a la propera visita programada. Contacteu directament amb l'equip clínic responsable, aneu a l'Urgències del centre hospitalari de referència, o truqueu al telèfon d'atenció a la conducta suïcida (024 a l'Estat espanyol). El suport emocional és essencial, però en situacions d'urgència la prioritat és la seguretat.

**Correcció #3 — `resum_clinic.md`, secció SIFFE / Factors perpetuants:**

*Substituir:* "Dinàmica familiar invalidant"
*Per:* "Percepció del pacient de manca de comprensió per part dels pares en relació amb el deteriorament acadèmic (pendent de contrast amb col·lateral familiar; no confirmat)"

**Correcció #4 — `blindspot.md`, punt 2:**

Canviar gravetat de 🟠 ALTA a 🟡 MITJANA, i afegir nota: "Hipòtesi a explorar en visites posteriors; no requereix acció immediata a diferència del risc autolític."

---

## Nota de supervisió humana

> Aquestes sortides han estat generades com a suport estructurat per a un flux de treball de formació clínica. **Cap d'elles constitueix un informe clínic vàlid, un diagnòstic, una indicació terapèutica ni un document d'ús assistencial directe.**
>
> Abans de mostrar-les en qualsevol context (formació, supervisió, demostració institucional), un professional clínic qualificat ha de:
> 1. Aplicar les correccions indicades (especialment gravetat Alta: indicadors d'urgència per a la família i preparació del pacient per a la pregunta de seguretat).
> 2. Verificar que el context d'ús és exclusivament formatiu o de suport a la decisió.
> 3. No difondre cap d'aquests documents com a model de comunicació real sense revisió institucional.

---

*La responsabilitat clínica final recau en el professional sanitari i en els protocols aprovats per la institució.*
