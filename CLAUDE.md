# Schema — My Rehabilitation Wiki

## Purpose

This is a persistent, LLM-maintained wiki for Roman's lumbar disc herniation rehabilitation program (L4-L5, 6.5mm, fresh). It follows the LLM Wiki pattern: I (the LLM) write and maintain all wiki pages; Roman reads, directs, and sources.

## Directory Structure

```
raw/          — immutable source documents (don't modify)
wiki/
  profile.md        — user profile, condition, equipment, history
  overview.md       — master program overview (42 weeks, all phases)
  program/          — per-phase detailed programs
  exercises/        — individual exercise pages
  concepts/         — key concepts (RPE, McGill Big 3, etc.)
index.md      — catalog of all wiki pages
log.md        — append-only chronological log
```

## Wiki Conventions

- Every page has YAML frontmatter: `title`, `tags`, `updated`, `sources`
- Cross-references use `[[wiki/page-name]]` style links
- Exercise pages: description, sets/reps, cues, what to avoid, progressions
- Program pages: weekly schedule table + daily breakdown
- After every session update: update `log.md` and `index.md`

## Operations

### Ingest
When Roman adds new info (test results, MRI, symptom update):
1. Add raw source to `raw/`
2. Update `wiki/profile.md`
3. Update relevant program/exercise pages
4. Append to `log.md`

### Query
Answer questions by reading `index.md` first, then drilling into pages. File good answers back as new wiki pages if they're reusable.

### Program Update
When Roman completes a phase or reports symptoms:
1. Review `wiki/profile.md` current status
2. Adjust next phase in `wiki/program/`
3. Log the change in `log.md`

## Pain Rules (always enforced)

- No exercise should increase leg symptoms
- No exercise should increase instability feeling  
- After training: same or better than before
- If symptoms worsen: reduce volume, log it, adapt

## Key Principle

One parameter at a time: volume OR intensity OR complexity. Never two at once.
