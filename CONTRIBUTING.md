# Bijdragen aan cvskills

Deze map (`cvskills/`) wordt gevoed vanuit meerdere projectrepositories. Elk project waar Ali Sultan aan werkt kan skills en diensten toevoegen of bijwerken.

## Doel

`cvskills/` is een gedeeld geheugen van skills en diensten, opgebouwd vanuit echte projectervaring. Geen zelfpromotie-bla, maar concrete observaties vanuit lopend werk.

---

## Bestandsstructuur

```
cvskills/
  skills.md          — Technische vaardigheden (gegroepeerd per domein)
  diensten.md        — Wat AI Sultan kan leveren (diensten voor klanten)
  CONTRIBUTING.md    — Dit bestand
```

---

## Hoe bijdragen vanuit een ander project

### Stap 1 — Clone of subtree

**Optie A: Aparte clone**
```bash
git clone git@github.com:aisultan/cvskills.git
# of als subtree in jouw project:
git subtree add --prefix cvskills git@github.com:aisultan/cvskills.git main --squash
```

**Optie B: Subtree pull (update vanuit bestaand project)**
```bash
git subtree pull --prefix cvskills git@github.com:aisultan/cvskills.git main --squash
```

### Stap 2 — Bestand aanpassen

Voeg een frontmatter-blok toe bovenaan de bijdrage zodat duidelijk is waar de info vandaan komt:

```markdown
---
source: naam-van-het-project
updated: YYYY-MM-DD
category: skills | diensten
---
```

### Stap 3 — Terugpushen

```bash
git subtree push --prefix cvskills git@github.com:aisultan/cvskills.git main
```

---

## Schema voor `skills.md`

```markdown
## [Domein]
- **[Technologie / Tool]** — [Concrete toepassing in dit project]
- **[Technologie / Tool]** — [Concrete toepassing in dit project]
```

Regels:
- Schrijf in het Nederlands (of Engels als het project in het Engels is)
- Beschrijf concreet wat je hebt gedaan, niet wat je "kunt"
- Geen buzzwords zonder onderbouwing
- Voeg toe aan bestaande categorie als die er al is, maak geen duplicaten

---

## Schema voor `diensten.md`

```markdown
## [Dienst nummer]. [Dienst naam]
[Korte omschrijving — max 2 zinnen]

- [Bullet: wat inbegrepen is]
- [Bullet: wat inbegrepen is]

**Geschikt voor:** [doelgroep]
```

Regels:
- Alleen diensten toevoegen die je aantoonbaar hebt geleverd (dus vanuit een echt project)
- Verwijs in het frontmatter naar het bronproject
- Prijs nooit noemen in dit bestand

---

## Hoe Claude dit bestand gebruikt

Als je Claude Code vraagt skills of diensten bij te werken, geef het dan dit commando:

```
Lees cvskills/CONTRIBUTING.md en voeg op basis van dit project toe wat ontbreekt in skills.md en diensten.md. Gebruik het schema en de frontmatter-conventie.
```

Claude leest de bestaande bestanden, vergelijkt met het huidige project, en vult aan zonder duplicaten.
