# Clinical AI Skills Demo Pack

Skills per fer una demostració segura amb metges d'un hospital, especialment en salut mental.

Basat en: Lempp T, de Lange D, Radeloff D, Bachmann C. **The clinical examination of children, adolescents and their families**. In: Rey JM, editor. IACAPAP e-Textbook of Child and Adolescent Mental Health. Geneva: International Association for Child and Adolescent Psychiatry and Allied Professions; 2012.

## Instal·lació local a Claude Code

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

Si no vols autoritzar cada acció, pot executar abans:

```text
--dangerously-skip-permissions
```

## Principi de seguretat

Aquest pack és només per a formació amb casos ficticis o dades sintètiques. No s'ha d'usar amb dades identificables de pacients ni per prendre decisions clíniques autònomes.
