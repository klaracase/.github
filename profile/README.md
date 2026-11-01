# Klaracase: API, SDKs and MCP server for German court decisions and statutes

Klaracase is a search and research service for German case law and statutes. The decisions and norms are linked by a resolved citation graph. You can reach it through a REST API, through an MCP server for AI assistants, and through official SDKs. It can also check the citations in a text against the corpus.

## SDKs

All five SDKs are 0.x. They wrap the REST API.

| Language | Install | Repository |
|---|---|---|
| Node.js and TypeScript | `npm install @klaracase/sdk` | [klaracase-node](https://github.com/klaracase/klaracase-node) |
| Python | `pip install klaracase` | [klaracase-python](https://github.com/klaracase/klaracase-python) |
| PHP | `composer require klaracase/klaracase` | [klaracase-php](https://github.com/klaracase/klaracase-php) |
| Go | `go get github.com/klaracase/klaracase-go` | [klaracase-go](https://github.com/klaracase/klaracase-go) |
| Rust | `cargo add klaracase` | [klaracase-rust](https://github.com/klaracase/klaracase-rust) |

Create an API token at https://klaracase.de/settings/api-tokens.

## MCP server

The server URL is `https://klaracase.de/mcp` (streamable HTTP). There are two ways to connect:

- OAuth 2.1, for Claude on the web and in Claude Desktop, and for ChatGPT. You sign in once in the client.
- A bearer token, for clients that can send headers. The same token works on the REST API and on the MCP server.

## Agent skills

The [skills](https://github.com/klaracase/skills) repository holds Agent Skills and a Claude Code plugin. In Claude Code:

```bash
claude plugin marketplace add klaracase/skills
claude plugin install klaracase@klaracase
```

## Documentation

- API reference: https://klaracase.de/docs/api
- MCP tools: https://klaracase.de/docs/mcp

## Scope and limits

Klaracase covers German law only. It is a research tool. It gives no legal advice and does not replace a lawyer's review. A `not_found` verdict means the citation was not found in the corpus; it is not a claim that the citation is fabricated.

Klaracase is not affiliated with any court or with the federal government.

---

## Auf Deutsch

Klaracase ist ein Recherchedienst für deutsche Rechtsprechung und Gesetze. Über eine REST-API, einen MCP-Server und offizielle SDKs für Node.js, Python, PHP, Go und Rust fragen Sie Entscheidungen und Normen ab und prüfen die Fundstellen in einem Text gegen den Bestand.

Klaracase deckt nur deutsches Recht ab. Es ist ein Recherchewerkzeug. Es gibt keine Rechtsberatung und ersetzt keine anwaltliche Prüfung. Das Ergebnis `not_found` heißt: Die Fundstelle wurde im Bestand nicht gefunden. Es sagt nicht, dass sie erfunden ist.

Klaracase ist mit keinem Gericht und nicht mit der Bundesregierung verbunden.

Dokumentation: https://klaracase.de/docs
