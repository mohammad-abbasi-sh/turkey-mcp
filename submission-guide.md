# Turkey MCP — submission guide

How to suggest a new MCP server for the Turkey MCP catalog
(https://mohammad-abbasi-sh.github.io/turkey-mcp/). This catalog is a
static, community-built reference: every server runs locally on the
user's own computer with `uvx`, is read-only by default, and is free —
no accounts, no hosted execution, no payments.

## What belongs here

- A **Turkish web service** with public data people actually ask an AI
  assistant about: shopping, travel, finance, news, jobs, food, sports,
  real estate, public services.
- A **working MCP server** (stdio transport) that reads that service's
  public data. One server = one service.
- **Real tests**: every tool must have been run against the live service
  at least once. No guessed endpoints, no invented responses.
- **Open source** code (the catalog links every server's repository).

## What does not belong here

- Servers for non-Turkish services (the Germany catalog covers German
  services; other countries are out of scope for this repo).
- Servers that need a paid API key to do anything useful, or that only
  work behind a login wall for their core tools.
- Servers that buy, book, pay or change anything in an account without
  an explicit local-session design (user's own cookie, confirm-before-
  mutate, never automatic payment). Write tools are the exception, not
  the rule, and are reviewed case by case.
- Scrapers that hammer a site: every server must be polite (small
  request counts, no aggressive polling) and must use the site's own
  public endpoints.

## How to submit

1. Open the **Submit** page on the site (`#/submit`) and fill in the
   form, or open an issue directly at
   https://github.com/mohammad-abbasi-sh/turkey-mcp/issues/new
   with the title `New server: <service-name>`.
2. Include:
   - **Service**: name + URL of the Turkish service.
   - **Why**: what would people ask their assistant about this service?
   - **Tools**: the tool list (name + one-line description each).
   - **Repository**: link to the server's code (or say you are offering
     the idea only — ideas are welcome, but code moves faster).
   - **Install**: the `uvx` package name (PyPI) if published.
   - **Sample questions**: 2–3 questions a user would ask after
     installing.
3. A maintainer reviews the submission. Accepted servers are added to
   the catalog with a detail page, a search entry and a `.mcp.json`
   profile entry.

## Field limits (what the form enforces)

| Field | Limit |
|---|---|
| Server id | lowercase letters, digits, hyphens; ends with `-mcp` |
| Summary | 160 characters max, one line |
| Tools | name + one-line description each; keep tool names short |
| Sample questions | 2–3, plain language |

## Standards a server must meet

- **Transport**: stdio, runnable as `uvx <package>`. No hosted URL
  required to use it.
- **No secrets in the repo**: no API keys, no session cookies, no
  credentials of any kind.
- **Honest errors**: if the service is down or changes, the tool
  returns a clear error — never a fabricated answer.
- **License**: PolyForm Noncommercial 1.0.0 (same as the catalog), or
  another open license stated in the repository.
- **Language**: tool names and summaries in English; the catalog adds
  Turkish and Persian descriptions.

## Review checklist (for maintainers)

- [ ] Service is Turkish and public.
- [ ] Every tool was run live at least once (evidence in the repo or
      the issue).
- [ ] No secrets, no credentials, no paid key required.
- [ ] Read-only, or write tools follow the local-session rules.
- [ ] README documents install + each tool + limits.
- [ ] Added to `servers.json`, the platform page, `.mcp.json`,
      `llms.txt`, `catalog.json` and `search.json` (the factory
      scripts regenerate the derived files).

## Questions?

Open an issue — or use the feedback form in the site footer.
