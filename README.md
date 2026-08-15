# CodePods AI Providers

A collection of declarative manifests describing third-party AI providers that
the [CodePods](https://github.com/lualab-xyz/codepods) application uses to
streamline provider onboarding in its UI.

Each provider lives in its own folder under [`providers/`](providers/) and
contains a `manifest.yml` plus light/dark SVG icons.

## Providers

| Provider | Base URL | Pricing / Free tier |
|----------|----------|---------------------|
| [Ollama](providers/ollama/manifest.yml) | `http://localhost:11434/v1` | Free, local models; cloud flat-rate possible |
| [Hugging Face](providers/hugging-face/manifest.yml) | `https://router.huggingface.co/v1` | Free monthly credits, then pay-per-use |
| [Mistral](providers/mistral/manifest.yml) | `https://api.mistral.ai/v1` | Limited free tier, then pay-per-use |
| [OpenRouter](providers/openrouter/manifest.yml) | `https://openrouter.ai/api/v1` | Free + pay-per-use models |
| [OpenAI](providers/openai/manifest.yml) | `https://api.openai.com/v1` | Pay-per-use |
| [Azure OpenAI](providers/azure/manifest.yml) | `https://<resource>.openai.azure.com/openai/v1` | Initial credits, pay-per-use |
| [Groq](providers/groq/manifest.yml) | `https://api.groq.com/openai/v1` | Free tier + paid plans |

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

1. Create a folder `providers/<slug>/` (lowercase, hyphenated).
2. Add a `manifest.yml` following the schema above.
3. Add `icon` / `icon_dark` SVGs in the same folder and reference their filenames.
4. Keep the description in English and mention the free tier / promo credits
   when one exists.

## License

[MIT](LICENSE)
