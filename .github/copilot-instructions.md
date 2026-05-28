# Copilot Instructions — nora-compliance

> See root `.github/copilot-instructions.md` for global conventions.

Claude Code plugin voor **NORA-compliance checking**. Toetst IT-systemen, architecturen en projecten aan de Nederlandse Overheid Referentie Architectuur (NORA): 10 basisprincipes, 40 afgeleide principes, dochterarchitecturen (GEMMA, PETRA, WILMA, RORA), en 'pas toe of leg uit'-validatie.

## Structure

```
.claude-plugin/plugin.json    # Plugin metadata (name, description, version, keywords)
skills/nora-compliance/
  SKILL.md                    # Skill definition — triggers, model config, scope
```

## Installation

```bash
claude install djimit/nora-compliance
```

## Typical Usage

- **Architectuurreview** — Toets architecturen aan NORA-basisprincipes en afgeleide principes
- **PSA-review** — Review Project Startarchitecturen op NORA-compliance
- **Dochterarchitectuur** — Toets op GEMMA (gemeenten), PETRA (provincies), WILMA (waterschappen), RORA (Rijk)
- **Koppelvlakstandaarden** — Check Digikoppeling, Digimelding, Digilevering, Haal Centraal
- **Interoperabiliteit** — Beoordeel API-standaarden en open koppelvlakken

## Domain Context

- NORA is verplicht voor de gehele Nederlandse overheid (Rijk, provincies, gemeenten, waterschappen, uitvoeringsorganisaties, ZBO's)
- 'Pas toe of leg uit'-principe: elke maatregel moet worden toegepast of afwijking moet worden gemotiveerd
- Bron: [noraonline.nl](https://www.noraonline.nl), [gemmaonline.nl](https://www.gemmaonline.nl)

## License

MIT (see `plugin.json`)
