# Telo for Claude

![Telo](assets/icon.png)

Explore your Apple Health history with telo. This plugin brings two guided workflows to Claude: a weekly review of sleep, activity and workouts, and longer-term comparisons across months or years. Both explain missing records and compare your own history without turning gaps into zeros.

## Get started

Install the plugin, open its Connectors tab, and connect Telo. Sign in with your telo account. First sync Apple Health from the telo iPhone app so that records are available. If you already use the Telo connector, this plugin references the same server URL.

For a private installation, upload the plugin ZIP from Customize → Plugins → Add → Upload plugin. In Claude Code, the skills can also be invoked as `/telo:weekly-health-review` and `/telo:long-term-trends`.

## Try these prompts

- “Give me my weekly health review, including missing data and comparison with the previous seven days.”
- “How have my available health metrics changed over the last year?”
- “What health data has reached telo, and how recent is it?”

The first two prompts use the bundled skills. Data availability can also be inspected directly through the connector. Answers follow the language of your request.

## What the plugin does

The plugin contains Markdown instructions and one remote MCP connector at https://telo.health/mcp. It queries the health records synced to your connected telo account, including daily metrics, sleep and workout sessions, personal baselines and data availability. Relevant results are returned to Claude to answer your request. The telo service records access metadata in your account history. The plugin adds no executable scripts, hooks, local services or additional external data destinations.

Queries do not modify health records. Data availability depends on the records accessible to the iPhone app and the uploads received by telo. The plugin cannot verify HealthKit read permissions or that a history import has finished. It does not diagnose conditions or recommend treatment.

## Skills

- **Weekly health review:** compares the last seven complete local days with the preceding seven days, reports coverage, and uses available personal baselines.
- **Long-term trends:** compares weekly or monthly aggregates with explicit dates, units and observed days; handles gaps and truncated responses.

[Website](https://telo.health) · [Privacy](https://telo.health/privacy) · [Terms](https://telo.health/terms) · [Support](mailto:contact@telo.health)

The MIT license covers this plugin's instructions and configuration. The telo service remains subject to its own terms. Telo names and branding are not granted as trademarks by the plugin license.
