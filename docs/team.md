# Team 02 — University Life Assistant

## Team roster

| Role | Member name | GitHub username | Initial ownership |
| --- | --- | --- | --- |
| Team lead | To be completed by the team lead | `vominhtriet-triseet` | Repository coordination, integration, release/tagging |
| Member 2 | To be completed | To be completed | Documentation and project boundary |
| Member 3 | To be completed | To be completed | Deterministic capability and unit tests |
| Member 4 | To be completed | To be completed | Structured data and provenance documentation |
| Member 5 | To be completed | To be completed | UI/API interface plan and user flows |
| Member 6 | To be completed | To be completed | Routing, safeguards, and evaluation plan |

Each person must replace their own placeholders through an individual PR. Do
not add personal contact details, student IDs, or other sensitive information.

## Lab 1 shared setup

The team uses this common skeleton:

```text
.
├── README.md
├── .gitignore
├── requirements.txt
├── pyproject.toml
├── src/assistant/
├── ui/
├── data/
├── tests/
├── docs/
└── scripts/check_env.py
```

The initial deterministic vertical slice uses `data/offices.csv` and
`src/assistant/rules.py`. It is deliberately small so every contributor can
reproduce the environment with the commands in the root README.

## Contribution workflow

1. Create or choose a GitHub Issue that describes one small, reviewable change.
2. Create a branch from current `main` using the approved prefix.
3. Make only the change in the Issue, test it where applicable, and use a
   Conventional Commit message.
4. Open a PR, link the Issue, and request one review from a teammate.
5. Merge only after approval and required checks pass. Never force-push,
   delete, or commit directly to `main`.
6. Record important decisions in `docs/` rather than relying on chat history.

## Initial PR plan for six contributors

| PR | Owner | Branch | Deliverable | Reviewer |
| --- | --- | --- | --- | --- |
| PR 1 | Team lead | `docs/team02-project-skeleton` | Shared repository setup, project overview, team coordination | Member 2 |
| PR 2 | Member 2 | `docs/problem-boundary` | Target users, use cases, non-goals, constraints, and success criteria | Member 3 |
| PR 3 | Member 3 | `feat/deterministic-office-lookup` | Small deterministic improvement plus unit tests | Member 4 |
| PR 4 | Member 4 | `docs/data-catalog` | Data catalog template, sample-data provenance, and data handling rules | Member 5 |
| PR 5 | Member 5 | `docs/interface-user-flows` | Student-facing interface/API flow and clarification/fallback scenarios | Member 6 |
| PR 6 | Member 6 | `docs/routing-evaluation-outline` | Routing/safeguard outline and an initial evaluation rubric | Team lead |

The Lab 1 sheet illustrates four owners, but this project team has six members.
Six separate PRs provide contribution evidence for every team member while
keeping the same shared skeleton and review discipline.

## Immediate deadline

For the W01 in-class submission, submit **only this team repository URL** in
LMS. The team lead will add the `v0.1-setup` tag after the initial setup PRs are
reviewed and merged.
