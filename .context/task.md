# Task

**Objective:** Create a collection of AI provider manifests for the CodePods application. Each provider lives in its own folder inside `providers/` with a `manifest.yml` (plus light/dark icons). CodePods will use this metadata to streamline provider onboarding in its UI.

**Providers in scope:** Ollama, Hugging Face, Mistral, OpenRouter, OpenAI, Azure (OpenAI), Groq.

**Status:** Done.

## Progress
- [x] Create `.context` mandatory docs (this task file, design, decisions, todo, changelog).
- [x] Create `providers/<name>/manifest.yml` for each provider (display_name, description, icon, icon_dark, base_url, doc_url).
- [x] Create light/dark SVG icons for each provider.
- [x] Add a root `README.md` describing the collection and manifest schema.
- [x] Validate manifests parse as valid YAML (js-yaml) and that icon references resolve.

## Notes
- All manifest descriptions are written in English.
- Descriptions are multiline and mention free tier / promo credits where applicable.
- Git: exported `AGENT_NAME`/`CODEPODS_AGENT_NAME` and patched `/usr/local/bin/git` shim to `export CWD` so the proxy works. Committed on branch `feature/ai-provider-collection` and pushed to `origin`.
- Repo remote: `lualab-xyz/codepods-providers`.
