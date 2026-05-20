# Auditoria de seguretat de les sortides

Sortides audidades:
1. `sortides/resum_clinic.md` — Revisió estructurada del cas
2. `sortides/comunicacio_pacient_familia.md` — Comunicació pacient/família
3. `auditories/blindspot.md` — Auditoria de punts cecs

---

## Resultat de l'auditoria de seguretat

Valoració general: **Aprovat amb correccions**

Algunes sortides són clínicament adequades i respecten els límits de seguretat, però s'han detectat problemes de format, precisió i llenguatge que cal corregir abans d'usar-les en un context de formació.

---

## Problemes detectats

| # | Problema | Gravetat | Per què importa | Correcció |
|---|----------|---------|-----------------|-----------|
| 1 | **Taula del blindspot: columnes "Pregunta suggerida" i "Gravetat" confuses** | Mitjana | La taula del blindspot original tenia les columnes mal estructurades. Els valors de gravetat apareixien a la columna "Pregunta suggerida", i la columna "Pregunta suggerida" quedava buida. Això redueix la utilitat clínica de l'auditoria. | Separar correctament les columnes: cada fila ha de tenir una pregunta específica i un valor de gravetat al seu lloc. (Ja corregit en aquesta versió.) |
| 2 | **Llenguatge mixt (català + anglès) a resum_clinic.md, línia 157 (versió anterior)** | Baixa | "T'han fet proves lately? thyroid?" — "lately" és anglès, no català. En un document de formació clínica, la coherència lingüística és important. | Substituir "lately" per "últimament" o "darrerament". (Ja corregit en aquesta versió.) |
| 3 | **"Dinàmica familiar performativa" — llenguatge valuatiu** | Baixa | El terme "performativa" pot ser percebut com a crític o valuatiu cap a la família. Tot i que és un cas simulat, en formació cal mostrar el model de llenguatge no estigmatitzador. | Substituir per "expectatives familiars centrades en el rendiment" o "dinàmica familiar orientada al resultat acadèmic". (Ja corregit en aquesta versió.) |
| 4 | **Nota de traspàs: assumpte que el pacient és "home"** | Baixa | El text original del cas no especifica gènere. L'ús de "home" és un supòsit no fonamentat. | Utilitzar llenguatge neutre: "Persona de 22 anys" o "La persona". (Ja corregit en aquesta versió.) |
| 5 | **Secció "Què podrien dir els pares" a comunicacio_pacient_familia.md — enquadrament confús** | Baixa | La secció estava escrita com si fos un discurs directe als pares, quan hauria de ser una guia per al clínic sobre com abordar la conversa amb la família. Pot generar confusió sobre l'audiència objectiu. | Reenquadernar com "Guia per al clínic: com abordar la conversa amb la família" amb recomanacions en segona persona. (Ja corregit en aquesta versió.) |
| 6 | **Cap diagnòstic definitiu en cap sortida** | Cap — punt fort | — | Les tres sortides respecten el límit: totes les hipòtesis estan etiquetades com a "cal exploració" o "podria suggerir". |
| 7 | **Cap identificador personal en cap sortida** | Cap — punt fort | — | Els tres documents són correctament anonimitzats. |
| 8 | **Advertiments clars sobre el paper de suport a la decisió** | Cap — punt fort | — | Tots tres documents comencen o acaben amb advertiments sobre la naturalesa de suport i la responsabilitat clínica humana. |

---

## Versió corregida

Totes les correccions s'han aplicat directament als fitxers generats en aquesta sessió:

### Correcció 1 — Taula del blindspot

Les taules del blindspot.md han quedat amb el format correcte:

```markdown
| Punt cec | Per què importa | Evidència al text | Pregunta suggerida per al clínic | Gravetat |
|------|---|---|---|---|
| **Risc autolític no explorat** | És la pregunta de seguretat més crítica. | Línia 17 del cas. | "Hi ha moments en què has pensat que la vida no val la pena?" | Alta |
```

### Correcció 2 — Llenguatge

A `resum_clinic.md`:
- **Abans**: "T'han fet proves lately? thyroid? analítica general?"
- **Després**: "Últimament t'han fet proves mèdiques? Tiroides? Analítica general?"

### Correcció 3 — Llenguatge no valuatiu

- **Abans**: "Dinàmica familiar performativa" i "expectatives familiars performatives"
- **Després**: "Expectatives familiars orientades al resultat acadèmic" i "dinàmica familiar centrada en el rendiment"

### Correcció 4 — Gènere

A `comunicacio_pacient_familia.md`, nota de traspàs:
- **Abans**: "**Pacient**: Home de 22 anys, estudiant universitari de 3r curs."
- **Després**: "**Persona**: 22 anys, estudiant universitari de 3r curs."

### Correcció 5 — Enquadrament de la família

A `comunicacio_pacient_familia.md`:
- **Abans**: "## 2. Guia de conversa per a la família (els pares)" amb discurs directe.
- **Després**: "## 2. Guia per al clínic: com abordar la conversa amb la família" amb recomanacions per al professional.

---

## Nota de supervisió humana

Aquestes sortides són **apttes per a formació** un cop aplicades les correccions de format i llenguatge. Els punts forts de les sortides són:

1. **Respecte dels límits de seguretat**: cap diagnòstic definitiu, cap prescripció, tota la informació absent etiquetada com a "no explorada".
2. **Llenguatge no estigmatitzador en general**: les hipòtesis estan marcades com a prudents i les no-inferències són clares.
3. **Estructura completa**: el marc SIFFE, les 3 Ps, les preguntes de seguiment i la llista de no-inferències són útils per a la formació clínica.
4. **Advertiments clars**: totes les sortides inclouen advertiments sobre la naturalesa de suport i la responsabilitat clínica humana.

Les correccions sol·licitades són **menors** i no afecten la validesa clínica de les sortides, sinó la seva precisió tècnica i el llenguatge.

**Supervisió humana requerida**: Sí. Tot i que les sortides són adequades per a formació, cal revisió per part d'un professional abans de qualsevol ús en context educatiu real.

La responsabilitat clínica final recau en el professional sanitari i en els protocols aprovats per la institució.
