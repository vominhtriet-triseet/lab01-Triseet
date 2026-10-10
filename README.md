# University Life Assistant — Team 02

A student-facing **Smart Virtual Assistant** for CSC10014. The project will
combine course, campus, regulation, and schedule information so students can
find reliable university-life information in one place.

> **Lab 1 scope:** this repository establishes the shared, reproducible project
> skeleton. It currently includes a small deterministic, rule-based office
> lookup as a smoke-testable vertical slice. The full assistant will be built
> incrementally in later weeks.

## Project direction

The future University Life Assistant will support four core ideas:

- **Search:** retrieve relevant information from approved, documented sources.
- **Structured data:** use validated records such as office locations, hours,
  course data, and schedules.
- **Planning:** break multi-step student requests into clear actions.
- **Routing:** send each request to the suitable capability, ask for
  clarification when needed, and provide a safe fallback otherwise.

### Current deterministic capability

The starter implementation intentionally has no LLM or external API. It
answers greetings and matches a requested office against the structured sample
file `data/offices.csv`. This provides a deterministic capability that can be
run and tested by every team member before later AI-enabled features are added.

## Repository rules

- Start changes from a GitHub Issue and work on a branch such as `feat/...`,
  `fix/...`, `docs/...`, `test/...`, or `chore/...`.
- Do **not** push directly to `main`; open a pull request (PR) and request a
  review from another team member.
- Use Conventional Commits, for example `docs(team): add initial team roles`.
- Never commit `.env`, secrets, tokens, real student/personal data, raw chat
  logs, or files under `data/raw/`.
- Do not add dependencies without first discussing and recording the decision
  with the team.

## Team

See [`docs/team.md`](docs/team.md) for the six team roles and the initial
contribution plan. Member names and GitHub usernames will be added by each
member in their own onboarding PR.

## Setup

Requirements: Python 3.10+ and Git.

Clone the repository and enter it:

```bash
git clone https://github.com/vominhtriet-triseet/lab01-Triseet.git
cd lab01-Triseet
```

Create and activate a virtual environment.

Git Bash on Windows:

```bash
python -m venv .venv
source .venv/Scripts/activate
```

PowerShell on Windows:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the project and its test dependency:

```bash
python -m pip install -r requirements.txt
python -m pip install -e .
```

## Run

With the virtual environment active:

```bash
python -m assistant "where is the library?"
```

Expected output:

```text
Library: room B.201, open Mon-Sat 07:00-20:00.
```

For interactive mode, run `python -m assistant` and type questions. Enter
`quit` or `exit` to stop.

## Test

```bash
python -m pytest -q
```

Expected result: `5 passed`.

To check the complete developer setup:

```bash
python scripts/check_env.py
```

Every check should show `[ OK ]`.

## Project structure

- `src/assistant/`: application code and response rules.
- `tests/`: automated tests.
- `data/`: small sample data used by the assistant.
- `scripts/check_env.py`: environment verification script.
- `docs/`: project documentation, team roles, and contribution records.
- `ui/`: future end-to-end user-interface plan.
- `requirements.txt`: pinned direct dependencies.
- `pyproject.toml`: package and test configuration.

## Troubleshooting

- `No module named assistant`: activate `.venv` and run `python -m pip install -e .`.
- `pytest` is not found: activate `.venv` and run `python -m pip install -r requirements.txt`.
- PowerShell blocks activation: run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` once, then activate again.
- The app does not know an office: check that its name exists in `data/offices.csv`.
