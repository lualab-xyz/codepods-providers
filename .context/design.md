# Design

## AI Provider Collection (CodePods)

A repository of declarative manifests that describe third-party AI providers so the CodePods application can onboard them in its UI.

## Layout

```
providers/
  <provider-id>/
    manifest.yml       # provider metadata (see schema below)
    <provider>-light.svg
    <provider>-dark.svg
```

## Manifest schema

| Field        | Type   | Purpose |
|--------------|--------|---------|
| `display_name` | string | Human-readable provider name shown in the UI. |
| `description`  | string | Multiline English description; notes free tier / promo credits / pricing model. |
| `icon`         | string | Light-theme icon filename. |
| `icon_dark`    | string | Dark-theme icon filename. |
| `base_url`     | string | Default API base URL used to reach the provider. |
| `doc_url`      | string | Link to instructions for obtaining an API key. |

## Conventions
- Provider folder id is a lowercase, hyphenated slug (`openai`, `hugging-face`, ...).
- Descriptions are written in English and are the single source of truth for pricing/free-tier notes.
- Icons are minimal SVG placeholders (rounded square + provider wordmark) that resolve to the referenced filenames.
