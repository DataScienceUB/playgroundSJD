
# playgroundSJD

Entorn d’experimentació per al desenvolupament i validació de fluxos de treball basats en intel·ligència artificial aplicats al suport al raonament clínic en salut mental.

Aquest repositori permet explorar arquitectures basades en *skills*, agents i workflows estructurats per donar suport a professionals clínics en processos com el *screening*, l’avaluació estructurada de casos, l’anàlisi diferencial i la generació d’informes clínics preliminars.

## Objectiu

L’objectiu del projecte és construir un espai segur d’experimentació per prototipar assistents d’IA capaços de:

- identificar informació clínica rellevant en una primera entrevista
- detectar informació absent o insuficient
- estructurar hipòtesis diagnòstiques preliminars
- identificar factors de risc i factors protectors
- generar preguntes de seguiment clínicament útils
- donar suport a la documentació estructurada de casos

Aquest projecte està orientat a **experimentació i recerca**, no a ús assistencial directe.

Basat en: *Lempp T, de Lange D, Radeloff D, Bachmann C. **The clinical examination of children, adolescents and their families**. In: Rey JM, editor. IACAPAP e-Textbook of Child and Adolescent Mental Health. Geneva: International Association for Child and Adolescent Psychiatry and Allied Professions; 2012.*

## Cas d’ús

Exemple de situació:

Un professional de salut mental atén un pacient jove amb simptomatologia inespecífica:

- insomni
- angoixa persistent
- dificultats de concentració
- deteriorament funcional acadèmic
- aïllament social progressiu
- consum ocasional de substàncies

L’assistent pot ajudar a:

1. estructurar la informació disponible
2. detectar absències crítiques en l’avaluació
3. suggerir exploració complementària
4. identificar possibles riscos
5. generar una síntesi clínica estructurada

---

## Limitacions

Aquest sistema:
- no substitueix criteri clínic professional
- no proporciona diagnòstic automàtic
- no és un dispositiu mèdic
- no ha de ser utilitzat per decisions assistencials autònomes
Totes les sortides han de ser revisades per professionals qualificats.

---


## Instal·lació manual d'aquest repositori i connexió a claude code

1. Baixar aquest repositori (en format .zip) a l'ordinador personal
2. Des del terminal navegar fins el directori que es crea al descomprimir el .zip ('/playgroundSJD-main')
3. Executar des del terminal:

```bash
mkdir -p ~/.claude/skills
cp -R clinical_case_review ~/.claude/skills/
cp -R clinical_blindspot_audit ~/.claude/skills/
cp -R clinical_safety_audit ~/.claude/skills/
cp -R patient_family_communication ~/.claude/skills/
cp -R clinical_demo_orchestrator ~/.claude/skills/
```

## Instal·lació automàtica dels skills i connexió a claude/ollama

1. Des del terminal navega fins el directori on tens el cas
2. Per connectar-ho a claude, executar des del terminal:

```bash
claude code
```
3. Per connectar-ho a ollama, executar des del terminal:

```text
# necessita 24GB de memòria
ollama launch claude --model qwen3.6
```
o en el cas d'un Mac amb prou memòria pots executar aquest model especialitzat en agents:

```text
# necessita 38GB de memòria
ollama launch claude --model qwen3.6:35b-a3b-coding-mxfp8 
```

3. Un cop dins de l'assistent executa aquestes dues instruccions per activar els skills:

```text
/plugin marketplace add DataScienceUB/datascienceub-skills
/plugin install playgroundSJD@datascienceub-skills
```

## Execució dels skills amb claude code des del terminal (requereix anonimització del cas): 

Des de claude code, entra aquest prompt:
 
```text
Fes servir l'skill clinical_demo_orchestrator per fer una revisió del cas que pots trobar al fitxer 'cas_simulat.md'.
```

## Execució dels skills amb ollama des del terminal (no requereix anonimització del cas):

Des d'ollama, entra aquest prompt:
 
```text
Fes servir l'skill clinical_demo_orchestrator per fer una revisió del cas que pots trobar al fitxer 'cas_simulat.md'.
```

## Principi de seguretat

Aquest pack és només per a formació amb casos anònims o dades sintètiques. No és aconsellable usar-lo amb dades identificables de pacients ni per prendre decisions clíniques autònomes sense una auditoria prèvia del projecte.

## Contacte

Data Science & AI Group  
Universitat de Barcelona
