<!--
Instructions for AI coding agents working on this repository.
Keep this file short (20-50 lines) and focused on repository-specific conventions,
important files, and workflows so an assistant can be productive quickly.
-->

# Copilot instructions — data-clean-up-pandas-for-beginners-project

Quick context:
- This repository is a learning/exercise project that centers around `project.ipynb` (a Jupyter notebook)
  that walks students through small Python exercises and a Pandas-based real estate data cleaning
  lab using the CSV at `assets/real_estate.csv`.

What you should know up front:
- Primary artifact: `project.ipynb`. Changes should preserve cell structure and keep markdown hints intact.
- Dependencies are listed in `requirements.txt` (pandas, numpy, matplotlib, scikit-learn, etc.).
- No application server or build system — the workflow is notebook-driven.

Common tasks and how to do them:
- Run the notebook interactively in VS Code / Codespaces or locally after installing requirements:
  - pip install -r requirements.txt
  - Open `project.ipynb` and run cells sequentially. Avoid modifying exercise prompts unless fixing clear errors.
- Inspect dataset: use `pd.read_csv('assets/real_estate.csv', sep=';')` (note the semicolon separator used in the notebook).
- When editing code cells, keep examples small and deterministic. Use the dataset in `assets/` for any data-driven examples.

Repository-specific conventions and patterns:
- Do not refactor notebook cell ids or remove explanatory markdown — students rely on them.
- Prefer small, self-contained code snippets for exercises (no heavy refactors across many cells).
- Language: Notebook cells use English and Spanish in markdown; preserve existing wording and formatting.

Important files to reference:
- `project.ipynb` — the full set of exercises and the primary workspace.
- `assets/real_estate.csv` — dataset used for Pandas exercises (read with sep=';').
- `requirements.txt` — pinning baseline libraries used by exercises.

Examples (use these exact patterns when editing or creating cells):
- Read data: `ds = pd.read_csv('assets/real_estate.csv', sep=';')`
- Display head: `ds.head()` (prefer `.head()` not printing entire DF in exercises).
- Filter by population: `ds[ds['level5'] == 'Arroyomolinos (Madrid)']`

Quality guidance:
- Keep changes minimal and pedagogical — this is an educational repo.
- Do not add external network calls or scrape sites. Work only with provided `assets/` files.
- If adding tests or scripts, keep them lightweight and document how to run them in the README.

If you need clarification from the repo owner:
- Ask about desired changes to exercise text vs. solution code. Avoid inserting final answers into student-facing prompts unless requested.

End of instructions.
