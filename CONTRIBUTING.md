# Contributing to Awesome Multi-Agent Orchestrators

Awesome Multi-Agent Orchestrators is intentionally narrow. The goal is not to list every AI tool. The goal is to document open or publicly documented products that are clearly about orchestrating multiple agents, parallel coding-agent work, agent workflows, shared knowledge, or agent-centered operating systems.

## Good contributions

- Add a new directory entry that fits the current scope.
- Fix broken or outdated links.
- Tighten summaries or directory notes to be more factual.
- Update metadata, assets, or SEO details when the site content changes.
- Improve the editorial framing without turning the site into a generic marketing page.

## Scope

Projects are usually a good fit when they have a clear orchestration angle, such as:

- multi-agent coordination
- parallel coding-agent execution
- workflow or job orchestration
- agent workspaces with memory, tools, and execution
- company or team operating systems built around agents
- open-source or publicly documented systems adjacent to the orchestration layer
- closed products that are important enough to shape the category, listed separately as not open but important

Projects are usually not a good fit when they are primarily:

- generic chat apps
- thin wrappers around a single model
- unrelated AI tooling without a meaningful orchestration layer
- impossible to verify from public sources

## Requirements for new submissions

Every new project submission must meet both requirements at review time:

- **At least 10 GitHub stars:** The project's public GitHub repository must have at least 10 stars. For closed-source products, an official public project, SDK, or integration repository may satisfy this requirement; disclosure of the product's source code is not required, and the separate closed-product category remains available.
- **A dedicated project website on its own/custom domain:** The website must be functioning and provide public information about the project. A GitHub-only presence, such as a repository, README, or `github.io` site without a custom domain, does not qualify. A custom domain must serve a project website, rather than simply redirect to a GitHub repository.

Include both the qualifying public GitHub repository and the project website in the README entry and pull request so maintainers can verify them. Starring this directory is separate from the project's minimum star requirement.

These requirements apply to new submissions. Existing listings will not be removed retroactively because of these requirements.

## How to add or update an entry

Listing contributions only need to update [`README.md`](./README.md).

1. Before submitting a pull request, please star this repository.
2. Add or update a bullet in the appropriate README category. You may also feature a new project in Latest Additions.
3. Include the project name, official links (both the qualifying website and GitHub repository for new submissions), and a short, factual description of its orchestration angle. State the license or source-availability status accurately.
4. In the pull request, explain why the project belongs and link the public sources used to verify the description.

External contributors do not need to edit `src/data/orchestrators.ts`, supply website metadata or assets, install dependencies, run website tests, or preview the site locally for a listing submission. Maintainers handle website data, presentation, and validation separately.

## Website maintenance

Maintainers keep the website directory in `src/data/orchestrators.ts` in sync with accepted README listings. Website changes should preserve existing entries and validate the rendered order, count, and relevant pages with the repository tests and build.

For website development, a local preview is available with `npm install` followed by `npm run dev`. This is optional for README listing contributions.

## Copy and sourcing rules

- Prefer official website, docs, and GitHub links.
- Keep summaries to one short paragraph.
- Keep the directory note to one sentence.
- For website maintenance, prefer local fallback marks or local assets over hotlinking third-party icons into the page shell.
- Do not add unverifiable claims, funding claims, or feature claims that are not obvious from public materials.

## Pull requests

Include a short note on what changed and why it belongs in the directory. If you are adding a new project, include the public source you used to verify the entry.
