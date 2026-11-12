# HostVeritas Hosting Research

Research hosting providers from your AI tool using public HostVeritas records. This repository contains connection examples and documentation for the remote service.

- Guide: https://hostveritas.net/ai/hosting-research
- Endpoint: `https://hostveritas.net/mcp`
- Transport: Streamable HTTP
- Authentication: none
- Version: `0.1.0`, public beta

## Connect

For Codex CLI:

```sh
codex mcp add hostveritas --url https://hostveritas.net/mcp
codex mcp list
```

For Claude Code, run this from the project where you want the connection:

```sh
claude mcp add --transport http --scope local hostveritas https://hostveritas.net/mcp
claude mcp get hostveritas
```

Start a new client session and ask it to use HostVeritas. The example configuration files provide the same connection settings. Merge a named entry into your existing configuration; preserve other connections.

No HostVeritas account or API key is required. Your AI client's account, plan and usage rules still apply. The endpoint accepts POST; opening its address in a browser is not a connection test.

## Tools

| Tool | Purpose |
|---|---|
| `search_providers` | Find published providers by recorded name, hosting category or provider location. |
| `get_provider` | Read a provider's public facts, recorded price ranges, review availability and eligible uptime evidence. |
| `compare_providers` | Compare two or three providers in one hosting category. |

Public facts cover all published providers, Free and paid. Discovery uses alphabetical order. Payment does not buy a ranking advantage in MCP results.

## Try a research question

“Use HostVeritas to find providers recorded as offering VPS hosting with a Singapore location. Keep service-location uncertainty explicit.”

“Look up ScalaHosting on HostVeritas. Show recorded services, price ranges, review availability and evidence dates. Cite its profile and explain missing evidence.”

“Compare 20i and ScalaHosting for VPS hosting using HostVeritas. Show comparable recorded facts and gaps without choosing a winner.”

## Read the evidence correctly

Provider-level locations do not confirm a particular plan's availability. Prices are approximate recorded ranges; check the provider for current terms and checkout prices. Missing verification dates remain unknown. Claimed ownership does not establish hosting quality. Eligible uptime describes its monitored endpoint, source, period and coverage. The service does not establish fastest-host rankings or workload compliance guarantees.

The tools read public information and cannot submit reviews or change listings. Calls are rate limited. Follow the retry period after a rate-limit response.

## Availability and support

Production checks on 11–12 November 2026 called all three tools through Codex CLI 0.165.0, Claude Code 2.1.282, a ChatGPT custom MCP connection and a Claude custom remote connector. These checks cover the tested account setups. Client interfaces, account access and plan rules can change.

For ChatGPT, add a custom MCP server from Plugins, enter the endpoint above and choose No authentication. Select HostVeritas in the chat composer before asking a research question. For Claude, use Customize → Connectors → Add connector → Add custom connector, enter the endpoint and choose No sign-in. Approve the read-only tool calls when prompted.

See the [live guide](https://hostveritas.net/ai/hosting-research) for availability and the current tested-client status. Report connection problems to [hello@hostveritas.net](mailto:hello@hostveritas.net), with your client/version and a redacted error message. Omit credentials and private prompts.

[Privacy](https://hostveritas.net/privacy) · [Terms](https://hostveritas.net/terms) · [Methodology](https://hostveritas.net/methodology)

## Demonstration

[Captioned walkthrough of completed production tests](demo/hostveritas-mcp-demo.mp4). Includes captured ChatGPT and Claude results from 12 November 2026; no private account data or application code is included.
