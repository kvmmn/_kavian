# Kavian — civic memory that watches power without taking it

Page size: **A4 Portrait 210×297 mm**. Chat SVG is a layout contract, not print-accurate.

---

## E0

**E0 · Environment**  
**Goal:** One system that watches power and must not become power.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  PW["Political power"] -->|"acts & promises"| KV["Kavian civic memory"]
  MX["Media & experts"] -->|"claims & sources"| KV
  EL["Founding elite circle"] -.->|"seed docket once"| KV
  ST["Kawe & GitHub stewards"] -->|"runtime & code"| KV
  KV -->|"unfinished snapshots"| PB["Public & civic users"]
  PB -->|"contest & dissent"| KV
  KV -.->|"must not rule"| STT["State, courts, parties"]
```

| Node | Purpose | In | Action | Out | Owner | Success / failure |
|---|---|---|---|---|---|---|
| Political power | Environment to watch | — | Exercises office | Acts, promises | Those in office | — |
| Media & experts | Source environment | Events | Publish claims | Citations | Outsiders | Not treated as canon |
| Founding elites | Seed once | Prior discussion | Propose first subjects | Founding docket | Named circle | Failure: set agenda forever |
| Kawe & stewards | Bootstrap & keep lights | Intent, PRs | Configure, then code only | Running agents | Kawe + GitHub | Failure: bury dissent |
| **Kavian** | Watch without office | Acts, claims, contests | Remember & ask | Snapshots, no verdict | Process, not a bench | Failure: judge or capture |
| Public & civic users | Consume & contest | Snapshots | Use, challenge, dissent | Contests | Anyone | Failure: only elites speak |
| State / courts / parties | Must stay outside | — | Their own power | — | Themselves | Kavian has **no standing** |

**Register:** Confirmed — not a government, not a judge. Dashed — elite seed ends; no standing toward the state.

**Footer:** Solid = primary · dashed = optional/forbidden-as-power · **A4 P · E0/9** · stack: humans + agents, not an office

---

## P1

**P1 · Backbone**  
**Goal:** Highest units of a counter-institution that publishes memory, never verdicts.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  ST["Kawe & GitHub"] -->|"bootstrap & patches"| A["A · Stewardship"]
  PW["Political power"] -->|"public acts"| B["B · Charter & docket"]
  A -->|"agents live"| C["C · Watch & memory"]
  B -->|"scope & seed"| C
  C -->|"citation graph"| D["D · Admission & dossiers"]
  D -->|"dossiers + dissent"| E["E · Public return"]
  E -->|"snapshots"| PB["Public & civic users"]
  PB -->|"challenges"| E
  E -->|"contests & clocks"| C
  E --> OC["Outcome · memory, no verdict"]
```

| Unit | Purpose | In | Out | Owner |
|---|---|---|---|---|
| **A Stewardship** | Start agents; then hands off agenda | Config, PRs | Runtime; freeze signal | Kawe + GitHub |
| **B Charter & docket** | Bound what may be watched | Elite seed once; charter | Frozen seed + scope | Charter; seats after live |
| **C Watch & memory** | Continuous remember | Acts, claims, contests | Citation graph | Agents as clerks |
| **D Admission & dossiers** | Stamp status; keep asking | Graph, board, dissent | Living dossiers | Rotating adversarial board |
| **E Public return** | Publish without standing | Dossiers + dissent | Snapshots; loops | Public + board cadence |

**Lineage:** A→P2-A · B→P2-B · C→P2-C · D→P2-D · E→P2-E · all P2→P3

**Register:** Outcome is unfinished public memory. Feedback is contests + clocks into C, not a score.

**Footer:** Confirmed ranks · default grain on C/D · **A4 P · P1/9** · 4-word payloads

---

## P2-A

**P2-A · Stewardship**  
**Goal:** Founder power ends at go-live. Technology may continue; the docket may not.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  KW["Kawe · configure once"]
  GH["GitHub contributors"]
  subgraph A["Focus: A — Stewardship"]
    A1["A1 · Start agent runtime"]
    A2["A2 · Cut steward agenda"]
    A3["A3 · Maintain code only"]
    A4["A4 · Refuse bury/smooth"]
    A5["A5 · Health & uptime"]
    A1 --> A2
    A2 --> A3
    A2 --> A4
    A3 --> A5
  end
  KW -->|"bootstrap config"| A1
  GH -->|"patches"| A3
  A2 -->|"hands-off signal"| B["B · Charter & docket"]
  A3 -->|"running agents"| C["C · Watch & memory"]
  A4 -.->|"cannot touch"| D["D · Admission"]
```

| ID | Purpose | In | Action | Out | Owner | Success / failure |
|---|---|---|---|---|---|---|
| A1 | Bring agents up | Config | Launch watchers | Runtime | Kawe | Up vs never live |
| A2 | End founder agenda | Go-live | Revoke docket rights | Hands-off | Bylaw | Failure: silent override |
| A3 | Keep machine honest | PRs | Patch, deploy | Same contracts | GitHub | Failure: logic that buries |
| A4 | Protect dissent | Pressure | Refuse | No-op | Stewards | Success = cannot comply |
| A5 | Stay alive | Runtime | Monitor | Alerts | Stewards | Failure: quiet death |

**Register:** Confirmed — stewards are code-only after live. Default — same-cycle code mergers cannot sit on the board.

**Footer:** Focus A · parent outs to B/C · dashed = forbidden reach · **A4 P · P2-A/9**

---

## P2-B

**P2-B · Charter & founding docket**  
**Goal:** Elites may seed once. After live, attention is public + seats, inside a written scope.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  EL["Founding elite circle"]
  A2["A · hands-off signal"]
  subgraph B["Focus: B — Charter & docket"]
    B1["B1 · Receive seed subjects"]
    B2["B2 · Publish freeze"]
    B3["B3 · Charter scope"]
    B4["B4 · After-live intake"]
    B5["B5 · Reject favorites"]
    B1 --> B2
    B3 --> B4
    B2 --> B4
    B5 -.-> B4
  end
  EL -->|"seed once"| B1
  A2 --> B2
  B3 -->|"promises money harm"| C["C · Watch & memory"]
  B4 -->|"new subjects"| C
  SE["Seats + public"] -->|"attention claims"| B4
```

| ID | Purpose | In | Action | Out | Owner | Success / failure |
|---|---|---|---|---|---|---|
| B1 | Take first list | Elite ideas | Record as seed | Draft docket | Elites, once | Failure: secret list |
| B2 | Freeze in public | Seed + go-live | Publish, lock stewards | Frozen seed | Process | Failure: quiet adds |
| B3 | Bound the watch | Values | Hold scope | Scope contract | Charter | Failure: favorite topics |
| B4 | Open attention | Contests, seats | Admit subjects in scope | New dockets | Board + public | Failure: steward queue |
| B5 | Block cliques | Steward/elite asks | Refuse | — | Bylaw | Success = no |

**Charter scope (default):** public promises, decisions, money, outcomes, harm.  
**Not in scope:** what should happen next; ranking actors; scoring “truth.”

**Register:** Confirmed — 1 then 3 from Q6. Open — how freeze is published.

**Footer:** Focus B · **A4 P · P2-B/9** · dashed B5 = control

---

## P2-C

**P2-C · Watch & citation memory**  
**Goal:** Agents clerk a graph. Nothing is true because it was repeated.

**Grain (default):** docket = one promise or decision · children = claims, evidence items, outcome observations.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  IN["B · scope & subjects"]
  WX["Power, media, experts"]
  LP["E · contests & clocks"]
  subgraph C["Focus: C — Watch & memory"]
    C1["C1 · Continuous watchers"]
    C2["C2 · Bind to grain"]
    C3["C3 · Citation graph"]
    C4["C4 · Camp layers"]
    C5["C5 · Collision flags"]
    C1 --> C2 --> C3
    C3 -.-> C4
    C3 --> C5
    C4 -.-> C5
  end
  IN --> C1
  WX -->|"raw claims"| C1
  LP -->|"re-ask payload"| C1
  C5 -->|"graph + flags"| D["D · Admission"]
```

| ID | Purpose | In | Action | Out | Owner | Success / failure |
|---|---|---|---|---|---|---|
| C1 | Not forget | Acts, claims, revisits | Fetch, attach time | Raw bundle | Agents | Failure: idle watch |
| C2 | Keep grain | Bundle | File under docket | Claims/items | Agents | Failure: slurred blobs |
| C3 | No canon | Items | Link who-said-what | Graph | Agents | Failure: merge to “fact” |
| C4 | Plural memory | Camps | Parallel admitted-sets | Layers | Camps | Optional at v0 |
| C5 | Show clash | Graph, layers | Flag collision | Flags | Agents | Failure: hide clash |

**Register:** Confirmed — citation graph under the board. Default — official gazette is a source node, not truth. Open — store/runtime.

**Footer:** Focus C · camp dashed · **A4 P · P2-C/9**

---

## P2-D

**P2-D · Admission & living dossiers**  
**Goal:** The board is clerical. The four questions stay open. Missing dissent is the alarm.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  CG["C · graph + flags"]
  subgraph D["Focus: D — Admission & dossiers"]
    D1["D1 · Adversarial seats"]
    D2["D2 · Stamp evidence status"]
    D3["D3 · Four questions"]
    D4["D4 · Never close docket"]
    D5["D5 · Require dissent"]
    D6["D6 · Forbid kept/broken"]
    D1 --> D2 --> D3
    D3 --> D4
    D1 --> D5
    D6 -.-> D3
  end
  CG --> D2
  D5 -->|"dossiers + dissent"| E["E · Public return"]
  D2 -->|"status on items"| CG
```

| ID | Purpose | In | Action | Out | Owner | Success / failure |
|---|---|---|---|---|---|---|
| D1 | Prevent one church | Cohort rules | Seat opposition | Seated board | Bylaw | Failure: tame opposition |
| D2 | Clerical power only | Graph | Stamp A/C/U | Status | Board | Failure: moral stamp |
| D3 | Civic product | Status + graph | Ask four questions | Living dossier | Agents + board | Failure: answer instead |
| D4 | Long horizon | Time | Refuse close | Still open | Process | Failure: settled case |
| D5 | Capture alarm | Draft snapshot | Block if no dissent | Dissent record | Board | Failure: unanimous quiet |
| D6 | Stay off the bench | Urge to verdict | Refuse | — | Charter | Success = no verdict |

**Four questions (confirmed):** What was promised? What happened? Who benefited? What evidence?

**Status vocabulary (confirmed):** admitted / contested / unverified — reopenable by later board, dissent, or new primary source.

**Register:** Default v0 board = named plural cohort; not sitting officials, sponsors, or same-cycle merge authors.

**Footer:** Focus D · **A4 P · P2-D/9** · dashed = forbidden verdict

---

## P2-E

**P2-E · Public return**  
**Goal:** Others may use the evidence. Kavian has no standing. Reality can force another look.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  DS["D · dossiers + dissent"]
  subgraph E["Focus: E — Public return"]
    E1["E1 · Snapshot cadence"]
    E2["E2 · Publish with dissent"]
    E3["E3 · Contest intake"]
    E4["E4 · Clocks 1 / 4 / 10y"]
    E5["E5 · No standing"]
    E6["E6 · Affected-first?"]
    E1 --> E2
    E3 --> E4
    E5 -.-> E2
    E6 -.-> E3
  end
  DS --> E1
  PB["Public & civic users"] -->|"challenges"| E3
  E2 -->|"snapshots"| PB
  E3 -->|"contests"| C["C · Watch & memory"]
  E4 -->|"re-ask"| C
```

| ID | Purpose | In | Action | Out | Owner | Success / failure |
|---|---|---|---|---|---|---|
| E1 | Cadence not agenda | Dossiers | Cycle publish | Draft | Board rhythm | Failure: newsroom capture |
| E2 | Public instrument | Draft + dissent | Release | Snapshot | Board | Failure: missing dissent |
| E3 | Anyone may force look | Challenge | Triage to classify | Contest payload | Public + agents | Failure: elite-only queue |
| E4 | Stop freeze | Time | Re-ask four questions | Revisit | Agents + board | Silence = failure |
| E5 | No office | Urge to sue/rule | Refuse standing | — | Charter | Success = unused as court |
| E6 | Harm standing | Affected person | ? reopen | ? | Open | Not designed |

**Register:** Confirmed — seats, then public contest, then clocks. Open — affected-first (E6). Default — harm uses E3.

**Footer:** Focus E · `?` = open · **A4 P · P2-E/9**

---

## R1

**R1 · Why this shape**  
**Title:** A civic memory that refuses the bench

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  R1["Watch power, hold no office"] --> R2["Refuse judge and state"]
  R2 --> R3["Founder is first capture"]
  R3 --> R4["Hands off docket after live"]
  R4 --> R5["Elites seed once, then stop"]
  R5 --> R6["Charter bounds favorites"]
  R6 --> R7["Graph is not a canon"]
  R7 --> R8["Board stamps status only"]
  R8 --> R9["Four questions stay open"]
  R9 --> R10["Missing dissent is alarm"]
  R10 --> R11["Public can force a look"]
  R11 --> R12["Time revisits 1/4/10y"]
  R12 --> X["Memory without verdict"]
```

**Boundary reasons (not a private chain of thought):**

- **Counter-institution before legal person** — cadence, seats, and bylaws can exist while GitHub + agents run; a nonprofit board is a later capture surface, so it is last.
- **Witness as floor** — ranking, truth scores, and “what should happen” would make Kavian a rival authority.
- **Living dossiers, not kept/broken** — a closure stamp is the thing worth capturing; unfinished questions stay humane and non-ideological.
- **Admission ≠ truth** — rotating adversarial seats classify evidence; the citation graph underneath keeps repetition from becoming reality.
- **Hands-off after bootstrap** — Kawe must be unable to add, bury, or smooth dissent once agents run; otherwise stewardship is the ideology.
- **Return order** — missing dissent first (capture inside), public contest second (capture of agenda), clocks third (capture by freeze).

**Confidence:** Architecture is ready to implement as process + agents. Jurisdiction, first cohort names, and store are still open.

**Footer:** R1 justification · 2-col stack · **A4 P · R1/9**

---

## P3

**P3 · One-page blueprint**  
**Goal:** Dependencies only. Confirmed / default / open on this sheet.

```mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 28, "rankSpacing": 32, "padding": 8}, "themeVariables": {"fontSize": "14px"}}}%%
flowchart TB
  A["A · Stewardship"] -->|"agents live"| C["C · Watch & memory"]
  A -->|"hands-off"| B["B · Charter & docket"]
  B -->|"scope & seed"| C
  C -->|"graph + flags"| D["D · Admission & dossiers"]
  D -->|"status"| C
  D -->|"dossiers + dissent"| E["E · Public return"]
  E -->|"snapshots"| PB["Public users"]
  PB -->|"challenges"| E
  E -->|"contests & clocks"| C
  E6["E6 affected-first?"] -.-> E
  LF["Legal person?"] -.-> A
  ST["Store & surface?"] -.-> C
```

**Lineage check:** P2-A..E expand A..E with no new powers. No kept/broken. No steward docket. No standing.

### Confirmed
- Name: Kavian (کاویان). Watch power; do not take it. Not a government or judge.
- Ranked boundary: counter-institution practice → public instrument → plural ledger → witness floor.
- After bootstrap: stewards = code only; founding docket then hands off; charter-scope second fence.
- Board: rotating, adversarial; status only; required dissent on snapshots.
- Product: living dossiers (four questions); citation graph; public contests; 1/4/10y revisits.

### Design defaults
- Grain: docket per promise/decision; claims, evidence, outcome observations.
- v0 board: named plural cohort; not officials, sponsors, or same-cycle mergable authors.
- Camp layers optional at v0. Affected-first off; harm via public contest.
- Legal person late. GitHub + running agents + bylaws enough to start.
- Success: reopenable dossiers; dissent never missing; steward hands off the docket.

### Open
- First jurisdiction and language of watch.
- Named first adversarial cohort; public freeze of the elite seed.
- Memory store, runtime, public read surface, cost/scale/compliance.
- Affected-first standing (E6). Legal person (dashed). Camp visibility on day one.

**Footer:** Solid = primary · dashed/`?` = open · **A4 P · P3/9** · print frame for geometry
