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
- [03 – Estimering (Planning Poker) + Sprint 0](exercises/03-estimation-sprint0/README.md)
- [04 – PR-flöde (liten drill) + review + länka kort](exercises/04-pr-drill/README.md)
- [05 – Demo & Retrospektiv (simulerad) → förbättringar](exercises/05-demo-retro/README.md)

## Standards & Policys (kopiera till Trello som checklistor)

### PR-policy (kursens enkla standard)
- Små, fokuserade PR (≈ **≤ 250 rader diff**).
- Rubrik: `type(scope): kort syfte` (ex. `feat(auth): add login form`).
- Beskrivning: **varför** + **hur** + ev. **skärmdump**.
- **Länka Trello-kort** (eller issue) i PR-texten.
- **Minst 1 review** krävs innan merge.
- Mergestrategi: `Squash & merge` är OK.

### Definition of Done (DoD)
- Kod kompilerar/kör lokalt.
- PR granskad & godkänd.
- README/ev. ändrade instruktioner uppdaterade.
- Trello-kort länkat i PR och **stängt** vid merge.

### Definition of Ready (DoR) — mini
- Story har **titel** och **kort syfte** (som <roll> vill jag… så att…).
- **Acceptance Criteria** (checkboxlista) finns.
- Story är **förstådd av teamet** och går att estimera.

### INVEST (för stories)
- **I**ndependent · **N**egotiable · **V**aluable · **E**stimable · **S**mall · **T**estable

## Tips
- Börja hellre **litet & klart** än stort & halvdant.
- Sätt **WIP-gräns** i “Doing” för att undvika flaskhalsar.
- [Grupparbete: Överenskommelse & Verktyg]([exercises/01-board-and-policies/README.md](https://github.com/lejonmanen/git-instruktion/blob/main/md/group.md))
