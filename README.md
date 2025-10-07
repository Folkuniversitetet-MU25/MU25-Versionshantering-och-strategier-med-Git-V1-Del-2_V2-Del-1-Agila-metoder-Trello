# V1, Del 2 & V2, Del 1 — Agila metoder + Trello ("Brädan")

Fokus: Scrum-grunder, user stories med **INVEST**, **Acceptance Criteria**, enkel **estimering** (Planning Poker), samt **commit/PR-policy** kopplat till Trello-kort.

> **Upplägg**
> - Arbeta i **team** på en gemensam Trello-bräda.
> - Kod/PR kan göras i utbildningens vanliga “lekplats-repo” eller i egna mini-repo – men **PR ska referera Trello-kort**.
> - Övningarna **lämnas inte in i Azomo**.

## Lärandemål (denna modul/vecka)
- Kunna beskriva Scrum (roller, events, artefakter) kortfattat.
- Formulera **user stories** med **acceptance criteria** (AC) enligt **INVEST**.
- Sätta **enkel PR-policy** och göra **grundläggande code review**.
- Använda Trello för planering och uppföljning (board, labels, checklistor).

## Snabblänkar till övningar
- [01 – Bräda & Policies (DoD, PR-policy, WIP)](exercises/01-board-and-policies/README.md)
- [02 – User stories (INVEST) + AC](exercises/02-user-stories-acceptance-criteria/README.md)
- [03 – Estimering (Planning Poker) + Sprint 0](https://github.com/Folkuniversitetet-MU25/MU25-Versionshantering-och-strategier-med-Git-V1-Del-2_V2-Del-1-Agila-metoder-Trello/tree/main/exercises/%2003-estimation-sprint0)
- [04 – PR-flöde (liten drill) + review + länka kort](exercises/04-pr-drill/README.md)
- [05 – Demo & Retrospektiv (simulerad) → förbättringar](exercises/05-demo-retro/README.md)

# Policies & checklistor – Agila metoder + Trello

Denna modul sätter gemensamma arbetssätt: **user stories (INVEST)**, **Acceptance Criteria (AC)**,
**Definition of Ready (DoR)**, **Definition of Done (DoD)**, **WIP-gränser**, samt **commit/PR-policy**
kopplad till Trello-kort.

> **Viktigt:** ÖVNINGAR i denna modul **lämnas inte in** i Azomo. Inlämning sker på grupp- och individ-examinationerna.

---

## PR-policy (kursens enkla standard)

**Syfte:** små, lättgranskade PR:er som är kopplade till planeringen och uppfyller AC.

### Storlek & scope
- Små, fokuserade PR (**≈ ≤ 250 rader diff**; exkl. genererade filer/lockfiles).
- **1 PR = 1 user story/issue/bug** (undvik “blandpåse”).
- Helst **≤ 5 filer** ändrade. Är det större → dela upp, eller motivera tydligt i PR.

### Rubrik & struktur
- **Rubrik:** `type(scope): kort syfte`  
  Ex: `feat(auth): add login form`
- **Tillåtna type:** `feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `ci`
- **Scope** är valfritt (t.ex. `auth`, `ui`, `api`).

### Beskrivning (varför + hur)
- **Varför:** vilket problem/nytta? (knyt till AC)
- **Hur:** huvudgrepp/arkitektur/ev. trade-offs
- **Skärmdump/GIF** om UI ändras

### Koppling till planering
- **Länka Trello-kort** (eller issue) **överst** i PR-beskrivningen
- Lista **Acceptance Criteria** i PR och **bocka av** uppfyllda

### Kvalitet före merge
- Bygg/test **grönt** (om tillämpligt)
- **Minst 1 review** (gärna 2)
- Feedback adresserad (svara “done” eller pusha fix)

### Merge-strategi
- Rekommenderat: **Squash & merge** (ren historik)
- **Force-push aldrig** till delade grenar (ok på *egna* feature-grenar vid behov)

### Branch-namn
- `feat/<kort-namn>`, `fix/<kort-namn>`, `docs/<kort-namn>`  
  Ex: `feat/login-button`, `fix/typo-readme`

---

## Commit-meddelanden (enkelt)
- Kort och i **imperativ**: “add”, “fix”, “update”
- Ex: `feat: add welcome section to README`
- **En commit = en logisk ändring**

---

## Definitioner (AC, DoR, DoD, INVEST, WIP)

### Acceptance Criteria (AC)
Testbar checklista som visar vad som måste vara sant för att storyn ska vara **klar**.
Exempel för *Login*:
- [ ] Inloggning fungerar med giltiga uppgifter  
- [ ] Felmeddelande visas vid fel inlogg  
- [ ] “Logga ut” tar bort session och leder till `/login`

### Definition of Ready (DoR – mini)
En story får planeras när:
- **Titel & syfte** finns (`Som <roll> vill jag <mål> så att <nytta>`)
- **AC** (checkboxlista) finns
- Teamet **förstår** storyn och kan **estimera** den

### Definition of Done (DoD – gäller alla PR)
- Kod kompilerar/kör lokalt utan fel
- Tester (om finns) passerar / manuell test beskriven
- PR **granskad & godkänd** (minst 1 review)
- README/ev. docs uppdaterad
- Trello-kort/issue **länkat** och **stängt** vid merge

### INVEST (för stories)
- **I**ndependent · **N**egotiable · **V**aluable · **E**stimable · **S**mall · **T**estable

- I – Independent (Oberoende): Kan utvecklas testas utan att låsa annan story.
- N – Negotiable (Förhandlingsbar): Inte detaljerad kravspec – går att diskutera.
- V – Valuable (Värdeskapande): Ger faktisk nytta för användaren.
- E – Estimable (Estimerbar): Teamet förstår den så pass att de kan sätta SP (Story Point).
- S – Small (Liten): Ska få plats i en sprint (och gärna i en PR).
- T – Testable (Testbar): Går att verifiera via AC.

### WIP – Work In Progress
- **WIP-gräns i “Doing” = 2** (rekommenderat)
- Syfte: minska multitasking och få saker **klara** innan nytt startas  
  *Tumregel*: WIP ≈ teamstorlek − 1 (justera efter erfarenhet)

---

### Exempel (story + AC)
- Story:
Som inloggad användare vill jag kunna logga ut så att min session avslutas och ingen annan kan använda mitt konto.

- AC:
- [ ] “Logga ut”-knapp visas när jag är inloggad
- [ ] Klick på “Logga ut” rensar session/token
- [ ] Jag skickas till /login efter utlogg
- [ ] Försök att öppna /profil efter utlogg leder till /login

## Tips
- Börja hellre **litet & klart** än stort & halvdant.
- Sätt **WIP-gräns** i “Doing” för att undvika flaskhalsar.
- [Grupparbete: Överenskommelse & Verktyg](https://github.com/lejonmanen/git-instruktion/blob/main/md/group.md
