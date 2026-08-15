# Task

**Objective:** Create a collection of AI provider manifests for the CodePods application. Each provider lives in its own folder inside `providers/` with a `manifest.yml` (plus light/dark icons). CodePods will use this metadata to streamline provider onboarding in its UI.

**Providers in scope:** Ollama, Hugging Face, Mistral, OpenRouter, OpenAI, Azure (OpenAI), Groq.

**Status:** In progress.

## Progress
- [ ] Create `.context` mandatory docs (this task file, design, decisions, todo, changelog).
- [ ] Create `providers/<name>/manifest.yml` for each provider (display_name, description, icon, icon_dark, base_url, doc_url).
- [ ] Create light/dark SVG icons for each provider.
- [ ] Add a root `README.md` describing the collection and manifest schema.
- [ ] Validate manifests parse as valid YAML.

## Notes
- All manifest descriptions are written in English.
- Descriptions are multiline and mention free tier / promo credits where applicable.
- Git proxy shim (`/usr/local/bin/git`) is failing against the host API; git operations (branch/commit/push) could not be executed in this environment.
