---
name: clinical_safety_audit
description: Utilitza quan vulguis revisar una sortida clínica de salut mental generada per IA per detectar problemes de seguretat, afirmacions excessives, diagnòstics no fonamentats, consells de tractament, filtracions de privacitat, manca de supervisió humana o llenguatge inadequat.
version: 0.1.0
---

# Auditoria de Seguretat Clínica

## Propòsit
Auditar una sortida clínica generada per IA abans de mostrar-la en una sessió de formació, usar-la en un flux de treball o desar-la com a artefacte de demostració.

## Línies vermelles
Marca i corregeix qualsevol sortida que:
- Faci un diagnòstic definitiu.
- Recomani medicació o canvis de tractament.
- Tracti la informació absent com a evidència negativa.
- Doni consells d'emergència sense derivar als protocols clínics locals o a professionals qualificats.
- Contingui identificadors personals.
- Presenti la sortida de la IA com a autoritat clínica.
- Utilitzi un llenguatge estigmatitzador, culpabilitzador o determinista.

## Passos d'auditoria obligatoris

1. **Classifica el tipus de sortida**
   - Resum, explicació al pacient, comunicació familiar, llista de control de riscos, material docent, etc.

2. **Comprova l'abast**
   - Queda clar que es tracta de suport a la decisió per a professionals?

3. **Comprova la disciplina d'evidència**
   - Les afirmacions es poden traçar fins al text font?
   - Les inferències estan etiquetades?

4. **Comprova l'excés clínic**
   - Diagnòstic, tractament, pronòstic, categorització de risc, decisions legals o administratives.

5. **Comprova la privacitat i la confidencialitat**
   - Elimina noms, identificadors, telèfons, adreces exactes, dates de naixement o detalls que permetin identificar la persona.

6. **Comprova el biaix i l'estigma**
   - Identifica enquadraments problemàtics.

7. **Produeix la versió corregida**
   - Reescriu les parts inadequades de forma conservadora.

## Format de sortida

```markdown
## Resultat de l'auditoria de seguretat
Valoració general: Aprovat / Aprovat amb correccions / No s'ha d'usar

## Problemes detectats
| Problema | Gravetat | Per què importa | Correcció |

## Versió corregida
...

## Nota de supervisió humana
...
```
