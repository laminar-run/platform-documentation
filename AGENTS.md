# Documentation project instructions

## About this project

- This is the public documentation site for **Minicor** (minicor.com), built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## What Minicor is

Minicor is an automation platform for legacy systems that have low or no API coverage (EHR, ERP, DMS, PMS, AMS, and similar). A **job** is an endpoint that represents an automation. You teach it with real sample API calls, the builder makes every sample pass, and then you call it like any other API. Automations run on Windows desktops through the Minicor Desktop Service, and every run is recorded.

## Terminology

Use these words. The left column is the only acceptable term in prose.

| Use | Never use |
| --- | --- |
| job | route, middleware route |
| sample, sample API call | test case |
| scenario | test suite, test group |
| teach, teaching | train, configure |
| the builder | build agent, teach loop |
| go live, Live, Learning | publish, deploy (for jobs) |
| stability, stability score | health score |
| desktop | VM (except infrastructure contexts where "Windows VM" is fine) |
| configuration | config store, environment variables |
| co-pilot | copilot, assistant |
| replay | video recording (as a noun for the artifact) |
| jobs engine | middleware, middleware-service (allowed only on the network boundary page, where it names the deployed service) |

Other rules:

- The product is **Minicor**, always capitalized, at **minicor.com**. The legal entity is Laminar Run, Inc.
- The desktop agent is the **Minicor Desktop Service**.
- Never say "computer use agents".
- Never cite accuracy percentages, click rates, or performance claims that are not in the product.
- Workflows are mentioned only as "the automation steps underneath a job". Do not document workflow publishing, Dev Mode mechanics, or routers.
- Self-healing means accumulation: enough scenarios and the job stops breaking. An agent in teach mode handles new failures and the fix becomes another scenario. Do not describe runtime improvisation as self-healing.

## Style preferences

- Write like the existing platform docs: plain declarative paragraphs, a table or list where it earns its place, a short blockquote for the one thing worth calling out. Explain the product to another developer like a human being.
- Use active voice and second person ("you")
- Keep sentences concise. One idea per sentence.
- Use sentence case for headings
- **No em dashes. No emojis.** Use commas, periods, or parentheses instead.
- No hedging ("might", "can help"), no marketing filler ("seamlessly", "leverage", "empower")
- Bold for UI elements: Click **Go live**
- Code formatting for file names, commands, paths, endpoints, and code references
- All code blocks have language tags
- Internal links are root-relative without file extensions: `/teaching/stability`

## Content boundaries

- Never name customers. Deployment stories are anonymized ("a healthcare customer", "your cloud project").
- SOC 2 Type II and HIPAA compliance are stated on the index page.
- No internal service names in prose (middleware-service, bedrock, lamcron). The architecture story is: your API call, the jobs engine, the Minicor platform, the Minicor Desktop Service on a desktop.
