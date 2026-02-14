# CopyCat 🐱

**Everything Postgres has, but for SQL Server.**
*Because imitation is the sincerest form of flattery.*

---

We looked at the PostgreSQL ecosystem — the beautiful drivers, the elegant tools, the developer experience that makes you *actually enjoy* talking to a database — and thought:

> "Why can't SQL Server have nice things?"

So we copied them. All of them. Like a cat knocking things off the Postgres table and dragging them to SQL Server's doorstep.

## The Family

At the center of everything is **tabby** 🐱 — a pure Rust implementation of the TDS 7.4+ protocol. No ODBC. No FreeTDS. No crying. Just a cat that speaks fluent SQL Server.

Every other project is a lightweight shim on top of tabby, because why rewrite protocol logic when you have a perfectly good cat doing all the work?

```
                         ┌─────────────────────┐
                         │   lazypaw (REST) 😴  │
                         │   meow (CLI) 📟      │
                         │   catnap (pooler) 💤 │
                         └────────┬────────────┘
                                  │
  ┌──────────┬───────────┬────────┴───┬──────────┬──────────┐
  │  hiss 🐍 │whiskers 🐈│ pounce 🐾  │ yarn 🧶  │scratch 🪵│
  │ (async   │ (DB-API   │ (ADBC      │ (Node)   │ (Rust)   │
  │  Python) │  Python)  │  Arrow)    │          │          │
  ├──────────┼───────────┼────────────┼──────────┼──────────┤
  │catnip 🌿 │ purr 💜   │hairball ☕  │furball 🤮│          │
  │ (Go)     │ (.NET)    │ (JDBC)     │ (ODBC)   │          │
  └────┬─────┴─────┬─────┴──────┬─────┴────┬─────┴──────────┘
       │           │            │          │
       └───────────┴─────┬──────┴──────────┘
                         │
                 ┌───────▼────────┐
                 │   tabby 🐱     │
                 │   Pure Rust    │
                 │   TDS 7.4+    │
                 │   The real MVP │
                 └───────┬────────┘
                         │
                 ┌───────▼────────┐
                 │  SQL Server    │
                 │  (the dog)     │
                 └────────────────┘
```

## The Projects

| Repo | Copies | What |
|------|--------|------|
| [**tabby**](https://github.com/copycatdb/tabby) 🐱 | libpq | Pure Rust TDS 7.4+ protocol library. The one cat to rule them all. |
| [**pounce**](https://github.com/copycatdb/pounce) 🐾 | adbc_driver_postgresql | Arrow-native ADBC driver. Zero-copy. Zero shame. |
| [**hiss**](https://github.com/copycatdb/hiss) 🐍 | asyncpg | Async Python driver. Like asyncpg, but angrier. |
| [**whiskers**](https://github.com/copycatdb/whiskers) 🐈 | psycopg2 | Python DB-API 2.0 driver. Standards-compliant, boring-reliable. |
| [**scratch**](https://github.com/copycatdb/scratch) 🪵 | tokio-postgres | Idiomatic Rust API. Like tokio-postgres but it leaves marks. |
| [**furball**](https://github.com/copycatdb/furball) 🤮 | psqlODBC | ODBC driver. Nobody asked for this but here we are. |
| [**yarn**](https://github.com/copycatdb/yarn) 🧶 | node-postgres | Node.js driver. Because cats love yarn and so does npm. |
| [**catnip**](https://github.com/copycatdb/catnip) 🌿 | pgx | Go driver. pgx walked so catnip could run. |
| [**hairball**](https://github.com/copycatdb/hairball) ☕ | pgjdbc | JDBC driver. We're sorry. Java made us do this. |
| [**purr**](https://github.com/copycatdb/purr) 💜 | Npgsql | .NET ADO.NET driver. Npgsql with a SQL Server accent. |
| [**lazypaw**](https://github.com/copycatdb/lazypaw) 😴 | PostgREST | Instant REST API from your DB. Minimal effort. Maximum nap. |
| [**catnap**](https://github.com/copycatdb/catnap) 💤 | PgBouncer | Connection pooler. PgBouncer but it lands on its feet. |
| [**meow**](https://github.com/copycatdb/meow) 📟 | psql | CLI tool. psql, but with attitude. |

## Why?

SQL Server has been around for 30+ years. Its official drivers are incredible — they support customers running apps from every era, with backward compatibility that borders on heroic. That dedication is admirable.

But what if you could start fresh? No legacy protocol versions. No ODBC layer. No 20 years of backward-compatible baggage. Just modern protocols, modern languages, and a cat.

That's CopyCat. We looked at what Postgres developers get — asyncpg, PostgREST, pgx, connection pooling, lightweight drivers — and thought: SQL Server deserves the same. One cat at a time.

## Credits & Inspiration

This project stands on the shoulders of giants (and some very patient database developers):

- **[tiberius](https://github.com/prisma/tiberius)** — The Rust TDS driver that proved you don't need ODBC. Tabby's spiritual ancestor.
- **[asyncpg](https://github.com/MagicStack/asyncpg)** — Showed the world what a fast database driver looks like.
- **[PostgREST](https://github.com/PostgREST/postgrest)** — "What if the database just... was the API?"
- **[PgBouncer](https://github.com/pgbouncer/pgbouncer)** — Connection pooling done right.
- **[libpq](https://www.postgresql.org/docs/current/libpq.html)** — 32K lines of battle-tested C that inspired tabby's architecture.
- **[Microsoft.Data.SqlClient](https://github.com/dotnet/SqlClient)** — Decades of backward compatibility. We salute you.
- **[mssql-jdbc](https://github.com/microsoft/mssql-jdbc)** — The Java driver that's seen things.
- **[pyodbc](https://github.com/mkleehammer/pyodbc)** — For every developer who typed `pip install pyodbc` and went to make coffee while ODBC headers compiled.
- **[FreeTDS](https://www.freetds.org/)** — The OG open-source TDS implementation. Been fighting the good fight since 1998.

## Philosophy

1. **tabby does the work** — Every driver is a thin, language-idiomatic wrapper around tabby. Protocol logic lives in one place.
2. **Standards first** — DB-API 2.0, ADBC, JDBC, ADO.NET. If there's a standard, we follow it.
3. **No ODBC tax** — No ODBC Driver Manager, no unixODBC, no 50MB binary blobs. Pure protocol, pure speed.
4. **Copy shamelessly, credit generously** — Every project documents exactly what it's copying and why.

---

*"SQL Server's official drivers are awesome — battle-tested, rock-solid, and fiercely dedicated to supporting customers who've been running the same app since 2003. We respect that deeply. CopyCat is just a cat that wanted to see what happens when you start fresh with zero backward-compatibility baggage."*

*One purr at a time.* 🐱
