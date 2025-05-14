# Highlight
```
The red-colored text in your Slack message isn’t standard Markdown behavior; it’s Slack’s syntax highlighting for inline code when it guesses the content looks like code (e.g., variable names in all caps).

Unfortunately, in pure Markdown, there is no native way to color text red — especially inside inline code blocks (i.e., using backticks). Markdown just supports:

*italic* or _italic_

**bold** or __bold__

`inline code` (grey background, monospaced)

Code blocks with syntax highlighting via triple backticks (```)

In Slack specifically:
Slack adds color (like red) only in message UI for:

Strings that look like constants or environment variables (ALL_CAPS with underscores)

Inside code formatting (backticks)
```
So:

## slack
* `RESCALE_FACTOR_JSON` → Slack will render as grey background + red font
* `foo` or `myVariable` → grey background only
* This red styling is not Markdown, it's Slack’s internal styling.

## Summary:
* If you're writing Markdown for GitHub, Confluence, etc.: no red text inside inline code is possible
* If you're in Slack: using backticks around ALL_CAPS_VARIABLES usually triggers red text
* For true text coloring, you'd need HTML or a platform that supports extended Markdown (like some Notion/Obsidian plug-ins)
