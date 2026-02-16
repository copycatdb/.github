# 🐱 CopyCat

**SQL Server deserves a proper open-source ecosystem. We're building it.**

PostgreSQL has PostgREST (26K stars), pgBouncer, psql, asyncpg, pgx, and hundreds of community tools. SQL Server has… corporate drivers and SSMS. We're fixing that.

Everything is MIT licensed. Everything is cat-themed. We regret nothing.

---

## 🐾 The Ecosystem

### Core

| Project | What it does |
|---------|-------------|
| **[tabby](https://github.com/copycatdb/tabby)** | 🐱 Pure Rust TDS 7.4+ protocol library — the heart of CopyCat. Home of the RowWriter trait for zero-copy row serialization |
| **[claw](https://github.com/copycatdb/claw)** | 🐾 Idiomatic Rust client for SQL Server — like tokio-postgres but sharper. `connect()`, typed queries, Arrow support |

### Drivers

| Project | Language | What it does |
|---------|----------|-------------|
| **[hiss](https://github.com/copycatdb/hiss)** | Python | 🐍 Async Python driver for SQL Server — like asyncpg, but angrier |
| **[whiskers](https://github.com/copycatdb/whiskers)** | Python | 🐈 PEP 249 DB-API 2.0 driver — synchronous, drop-in replacement |
| **[furball](https://github.com/copycatdb/furball)** | C (ODBC) | 🐱 ODBC driver for SQL Server — works with pyodbc, R, Excel, everything |
| **[kibble](https://github.com/copycatdb/kibble)** | Node.js | 🍚 Node.js driver — napi-rs + tabby, faster than tedious |
| **[catnip](https://github.com/copycatdb/catnip)** | Go | 🌿 Go `database/sql` driver — pgx walked so catnip could run |
| **[hairball](https://github.com/copycatdb/hairball)** | Java | ☕ JDBC driver — we're sorry, Java made us do this |
| **[nuzzle](https://github.com/copycatdb/nuzzle)** | .NET | 💜 ADO.NET driver — Dapper and EF Core compatible |
| **[pounce](https://github.com/copycatdb/pounce)** | Arrow | 🐾 ADBC Arrow driver — zero-copy columnar access for analytics |

### Tools

| Project | What it does |
|---------|-------------|
| **[lazypaw](https://github.com/copycatdb/lazypaw)** | 😴 Instant REST API for SQL Server — PostgREST equivalent with realtime, SDK, codegen, and auth |
| **[meow](https://github.com/copycatdb/meow)** | 📟 Terminal client for SQL Server — psql, but with attitude |
| **[prowl](https://github.com/copycatdb/prowl)** | 🐱 MCP server — let AI agents query your database |
| **[catnap](https://github.com/copycatdb/catnap)** | 💤 Connection pooler — PgBouncer but it lands on its feet |

---

## 🧵 How it fits together

```
Your App / AI Agent / Dashboard
    │
    ├── lazypaw (REST API)      ── uses claw ──┐
    ├── prowl (MCP for AI)      ── uses claw ──┤
    ├── hiss (Python async)     ── uses tabby ─┤
    ├── whiskers (Python sync)  ── uses tabby ─┤
    ├── kibble (Node.js)        ── uses tabby ─┤
    ├── catnip (Go)             ── uses tabby ─┤
    ├── hairball (Java)         ── uses tabby ─┤
    ├── nuzzle (.NET)           ── uses tabby ─┤
    ├── pounce (Arrow/ADBC)     ── uses tabby ─┤
    └── furball (ODBC)          ── uses tabby ─┘
                                       │
                                     tabby
                                  (TDS protocol)
                                       │
                                  SQL Server
```

Every driver speaks TDS natively through **tabby** — no ODBC, no FreeTDS, no Microsoft driver required. One protocol library, every language.

---

## 🧶 Philosophy

**Independent.** CopyCat is not owned by, affiliated with, or endorsed by any corporation. It's a community project built by people who love databases and think SQL Server deserves better open-source tooling.

**Ideas flow freely.** We learn from Postgres tooling, from Microsoft's official drivers, from everywhere good ideas live. Open source means open in every direction.

**Community-owned.** Read our [Governance doc](../GOVERNANCE.md). We welcome contributions and sponsorship. We will never be acquired.

---

## 🐈 Get Involved

- 🐛 Found a bug? Open an issue in the relevant repo
- 💡 Have an idea? Start a discussion
- 🔧 Want to contribute? Check our [Contributing Guide](../CONTRIBUTING.md)
- 📜 Read our [Code of Conduct](../CODE_OF_CONDUCT.md)

---

*Built with 😺 by the CopyCat community*
