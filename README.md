# Marcello Lopes

**Software Engineer.** Over 5 years building web applications — deep in React and TypeScript,
now working across the whole stack: legacy database, Spring Boot service, NestJS BFF, Nuxt host,
React micro-frontend.

What I actually spend my time on: **designing AI agent architectures that survive contact with
production.**

---

### 🤖 Agent architecture, applied

Most "AI in the workflow" stories are about writing code faster. Mine is about designing the
system the agents run inside.

On an enterprise authorization project, I built a set of agents with deliberate boundaries:

- **Architect / executor split.** Whoever designs the authorization primitive is not whoever
  applies it. This is not tidiness — it's what prevents a second source of permission checks
  from appearing in the browser, which is the most expensive failure mode in this class of work.
- **A stop protocol.** When the executor finds a contract different from what it expected, it
  *stops and reports* instead of improvising a fix. An agent that improvises around a missing
  piece will happily build the wrong thing correctly.
- **An evidence protocol.** After applying a change, the agent captures proof with and without
  permission, and a human validates before anything is committed.
- **A versioned source of truth**, replacing an authenticated documentation lookup — with an
  explicit precedence rule, and divergence reported for regeneration rather than patched by hand.
- **Context cost as a design requirement.** The catalog is 5,448 lines; reading it whole would
  cost more than the lookup it replaced. The docs specify reading only the relevant block.

I also deleted a 190-line parser I had written, once the data was versioned — three lines of
`awk` did the same job without a dependency to keep in sync. The note explaining why is in the
repo, so nobody reintroduces it.

**Delivery cadence on that front went from 1 to 8 screens per week.**

<sub>Week 1 was slower because the foundation was being built alongside it — the honest
comparison is week 2 → week 3, same foundation, 3 → 8.</sub>

---

### 🛠️ What I build

| | |
| :--- | :--- |
| **AI tooling** | [Syntra](https://github.com/lopesmarcello/Syntra) · [aidp](https://github.com/lopesmarcello/aidp) |
| **Frontend** | [fs-router-dom](https://github.com/lopesmarcello/fs-router-dom) · [serena-ui](https://github.com/lopesmarcello/serena-ui) |
| **Go & Rust** | [Vitals](https://github.com/lopesmarcello/Vitals) · [Dispatch](https://github.com/lopesmarcello/Dispatch) |

`fs-router-dom` came out of real pain: a file-based router that eliminated 100% of route
conflicts in the inspection system used daily by São Paulo's borough administrations.

---

### 🧰 Stack

| Domain | |
| :--- | :--- |
| **Languages** | TypeScript, JavaScript, Go, Java, Lua |
| **Frontend** | React, Next.js, Micro-frontends (since 2022), Tailwind, Nuxt |
| **Backend** | NestJS, Spring Boot, Go, PostgreSQL, Docker |
| **Practice** | ADRs, OpenAPI contracts, Azure DevOps, testing, agent orchestration |

---

### 📍 Now

Frontend engineer at **NTConsult**, on the **Vivo** account — building the authentication and
authorization layer of a legacy-to-micro-frontend migration, from the database to the browser.

Going deeper on Go, distributed systems, and how to make agents reliable enough that someone
else can trust their output.

📫 [LinkedIn](https://www.linkedin.com/in/lopesmarcello) · marcellolopesdev@gmail.com
