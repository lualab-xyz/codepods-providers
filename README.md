# CodePods AI Providers

A collection of declarative manifests describing third-party AI providers that
the [CodePods](https://github.com/lualab-xyz/codepods) application uses to
streamline provider onboarding in its UI.

Each provider lives in its own folder at the repository root (e.g. `ollama/`,
`openai/`) and contains a `manifest.yml` plus light/dark SVG icons.

## Manifest schema

```yaml
display_name: "OpenAI"          # Human-readable name shown in the UI
description: |                  # Multiline English text; notes free tier / pricing
  ...
icon: "openai-light.svg"        # Light-theme icon filename (in the provider folder)
icon_dark: "openai-dark.svg"    # Dark-theme icon filename
base_url: "https://api.openai.com/v1"   # Default API base URL
doc_url: "https://platform.openai.com/api-keys"  # How to get an API key
```

## Adding a provider

1. Create a folder `<slug>/` at the repository root (lowercase, hyphenated).
2. Add a `manifest.yml` following the schema above.
3. Add `icon` / `icon_dark` SVGs in the same folder and reference their filenames.
4. Keep the description in English and mention the free tier / promo credits
   when one exists.

## License

[MIT](LICENSE)
