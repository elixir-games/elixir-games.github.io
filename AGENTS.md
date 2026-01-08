AGENTS.md

Build / Lint / Test
- Build: this is a static site; open `index.html` in a browser or serve with `python -m http.server`.
- Lint: no project linter configured. Use `htmlhint` or `prettier --check` if you add a config.
- Test: no test framework present. To run a single test (after adding tests), prefer a targeted command like `pytest tests/test_file.py::test_name` or `mix test test/some_test.exs:12` depending on language.

Code Style Guidelines
- Formatting: use Prettier or language-native formatter (e.g., `mix format` for Elixir) before commits.
- Imports / requires: keep imports explicit and minimal; group third-party then local.
- Types: prefer explicit types/specs where supported (e.g., `@spec` in Elixir).
- Naming: use snake_case for files and functions, PascalCase for modules/components.
- Error handling: return tagged tuples `{:ok, val} | {:error, reason}` in Elixir; avoid raising unless unrecoverable.
- Tests: write focused, deterministic unit tests; mock external network calls.
- Commits: keep atomic and focused; include motivation in commit messages.

Agent rules
- Respect existing project structure and do not create unrelated files.
- If adding linters or tests, include minimal config and document commands here.

Notes
- No Cursor or Copilot rule files detected.
- If you need specific tooling (Elixir, Node), add a `mix.exs` or `package.json` and update this file.
