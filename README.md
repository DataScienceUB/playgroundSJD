# Clinical AI Skills Demo Pack

Skills per fer una demostració segura amb professionals de salut mental.


## Baixar el codi

Des d'un navegador, eentra al repositori https://github.com/DataScienceUB/playgroundSJD/ i prem:
1. botó verd Code
2. opció Download ZIP

Descomprimeix:
```bash
unzip repo.zip
```

## Instal·lació local a Claude Code

Des del directori de treball:

```bash
mkdir -p ~/.claude/skills
cp -R clinical_case_review ~/.claude/skills/
cp -R clinical_blindspot_audit ~/.claude/skills/
cp -R clinical_safety_audit ~/.claude/skills/
cp -R patient_family_communication ~/.claude/skills/
cp -R clinical_demo_orchestrator ~/.claude/skills/
```

Després, obre Claude Code dins d'una carpeta de demo amb un cas simulat i demana, per exemple:

```text
Fes servir l'skill clinical_demo_orchestrator per fer una revisió del cas que pots trobar al fitxer 'cas_simulat.md'.
```

## Principi de seguretat

Aquest pack és només per a formació amb casos ficticis o dades sintètiques. No s'ha d'usar amb dades identificables de pacients ni per prendre decisions clíniques autònomes.
