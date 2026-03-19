# Bootstrap IA — Spec Driven Development for AI-Powered Project Generation

A comprehensive ruleset and workflow system that transforms Cursor into a **Spec Driven Development (SDD)** engine. Specifications are the single source of truth — they drive architecture, implementation, tests, and documentation.

## What is Bootstrap IA?

Bootstrap IA combines three layers of intelligence with a spec-first methodology:

1. **Core SDD Rules** — A structured methodology where specifications drive everything: planning, architecture, implementation, testing, and documentation.
2. **Global Quality Rules** — Universal coding standards that apply to every project regardless of tech stack.
3. **Technology-Specific Rules** — Best practices for 18+ programming languages and frameworks.

When you drop these rules into a project, Cursor becomes a senior engineer that:
- Writes formal specifications before any code (OpenAPI, JSON Schema, Gherkin).
- Designs architecture driven by contracts, not assumptions.
- Generates conformance tests from specs before implementation.
- Implements features that conform to specifications.
- Validates quality through spec conformance gates at every step.
- Evolves specs first when requirements change, then propagates to code.

## What is Spec Driven Development?

SDD is a methodology where **specifications are the single source of truth**:

```
Discovery → Specification → Contract Design → Scaffolding → Spec-First Implementation → Conformance Gates → Iteration
```

| Principle | Description |
|-----------|-------------|
| **Spec First** | Write formal specs (OpenAPI, JSON Schema, Gherkin) before any code |
| **Contract-Driven** | API, data, and UI contracts are defined and validated before implementation |
| **Conformance Testing** | Tests are generated from specs — implementation must conform to contracts |
| **Living Documentation** | Specs ARE the documentation — auto-generated, never stale |
| **Spec Evolution** | When requirements change, update the spec first, then propagate to code |

## Compatibility

| Tool | File | Format |
|------|------|--------|
| **Cursor** | `.cursor/rules/*.mdc` | MDC with YAML frontmatter |
| **Claude Code** | `CLAUDE.md` | Markdown (project root) |
| **OpenCode / Agents** | `AGENTS.md` | Markdown (project root) |

## Rules Overview

### Core Rules (SDD Workflow & Project Generation)

These rules define HOW the AI approaches spec-driven project creation.

| Rule | Description |
|------|-------------|
| `core-workflow` | Master SDD workflow: discovery → specification → contract design → scaffold → implement → conform → iterate |
| `core-planning` | Spec-driven planning: requirements as specifications, contracts as acceptance criteria |
| `core-specification` | **NEW** — Spec authoring: how to write, structure, and manage specifications |
| `core-architecture` | Contract-first architecture: design driven by specifications and contracts |
| `core-scaffolding` | Spec-driven scaffolding: project structure with specs directory and conformance tooling |
| `core-implementation` | Spec-first implementation: code derived from specifications, conformance over creativity |
| `core-quality-gates` | Conformance gates: spec-driven validation checkpoints at every phase |
| `core-iteration` | Spec-driven iteration: specs evolve first, code follows |
| `core-agent-orchestration` | SDD agent patterns: spec-first prompting, contract-then-code workflow |
| `core-devops` | CI/CD pipelines with spec validation, deployment strategies, monitoring |
| `core-tech-stack` | Technology selection framework, stack recommendations by project type |
| `core-ux-design` | UX/UI design principles, forms, loading states, accessibility, responsive design |

### Global Rules (Always Apply)

Universal coding standards for every project.

| Rule | Description |
|------|-------------|
| `global-clean-code` | Naming, functions, readability, simplicity |
| `global-error-handling` | Fail fast, meaningful errors, logging |
| `global-security` | Input validation, secrets, auth, common vulnerabilities |
| `global-testing` | Spec conformance testing, test pyramid, contract validation |
| `global-git-conventions` | Commits, branches, PR workflow |
| `global-documentation` | Living documentation: specs as source of truth, auto-generated docs |
| `global-performance` | Bottlenecks, caching, async, payloads |
| `global-solid-principles` | SOLID, DRY, KISS, YAGNI |
| `global-project-structure` | File organization, module boundaries |
| `global-code-review` | Review checklist and feedback guidelines |

### Technology-Specific Rules

Activated automatically when working with matching file types.

| Rule | Globs | Description |
|------|-------|-------------|
| `specific-typescript` | `**/*.ts, **/*.tsx` | Strict types, patterns, nullability |
| `specific-react` | `**/*.tsx, **/*.jsx` | Components, hooks, state, performance |
| `specific-nextjs` | `**/*.tsx, **/*.ts` | App Router, server components, data fetching |
| `specific-python` | `**/*.py` | PEP 8, type hints, pytest, project structure |
| `specific-nodejs` | `**/*.js, **/*.ts` | Async, error middleware, API design, logging |
| `specific-css-tailwind` | `**/*.css, **/*.scss, **/*.tsx` | Utilities, responsive, accessibility |
| `specific-sql-database` | `**/*.sql, **/*.prisma` | Schema, queries, migrations, ORM |
| `specific-docker` | `Dockerfile, docker-compose*` | Multi-stage, security, compose |
| `specific-rust` | `**/*.rs` | Ownership, error handling, idiomatic patterns |
| `specific-go` | `**/*.go` | Error handling, concurrency, project layout |
| `specific-vue` | `**/*.vue, **/*.ts` | Composition API, Pinia, performance |
| `specific-csharp` | `**/*.cs` | .NET patterns, async, LINQ, nullable, DI |
| `specific-java` | `**/*.java` | Modern Java 17+, Spring, Optional, streams |
| `specific-dart` | `**/*.dart` | Dart 3 / Flutter, null safety, state management |
| `specific-c` | `**/*.c, **/*.h` | Memory safety, defensive programming, portability |
| `specific-cpp` | `**/*.cpp, **/*.hpp, **/*.cc` | RAII, smart pointers, modern C++17/20/23 |
| `specific-api-rest` | `**/api/**, **/routes/**` | URL design, HTTP methods, response format |
| `specific-markdown` | `**/*.md` | Markdown layout, headings, links |

## Usage

### Quick Start — Full Bootstrap

Copy the entire ruleset into your project:

```bash
git clone https://github.com/YOUR_USERNAME/bootstrap-IA.git

cp -r bootstrap-IA/.cursor/ /path/to/your-project/.cursor/

cp bootstrap-IA/AGENTS.md /path/to/your-project/
cp bootstrap-IA/CLAUDE.md /path/to/your-project/
```

### Cherry-Picking Rules

Copy only the rules you need:

```bash
cp bootstrap-IA/.cursor/rules/core-*.mdc /path/to/your-project/.cursor/rules/

cp bootstrap-IA/.cursor/rules/global-*.mdc /path/to/your-project/.cursor/rules/

cp bootstrap-IA/.cursor/rules/specific-typescript.mdc /path/to/your-project/.cursor/rules/
cp bootstrap-IA/.cursor/rules/specific-react.mdc /path/to/your-project/.cursor/rules/
```

### Using with Cursor

1. Copy the rules into your project's `.cursor/rules/` directory.
2. Open the project in Cursor.
3. Start a conversation — the AI will automatically follow the SDD workflow.
4. For new projects, begin with: *"I want to build [description]. Let's start with discovery and specification."*

### Using with Claude Code

Place `CLAUDE.md` at your project root. Claude Code reads it automatically.

### Using with OpenCode / Other Agents

Place `AGENTS.md` at your project root.

## SDD Workflow Example

Here's how Bootstrap IA transforms a typical conversation:

**Without Bootstrap IA (SDD):**
> "Build me a todo app" → AI immediately dumps 500 lines of code in one go.

**With Bootstrap IA (SDD):**
> "Build me a todo app" → AI follows the SDD workflow:
> 1. **Discovery**: Asks about features, users, constraints.
> 2. **Specification**: Writes OpenAPI spec, JSON Schemas, behavior specs (Given-When-Then).
> 3. **Contract Design**: Designs architecture driven by the specs.
> 4. **Scaffolding**: Creates project structure with `specs/` directory and conformance tooling.
> 5. **Spec-First Implementation**: Generates conformance tests from specs, then implements to pass them.
> 6. **Conformance Gates**: Validates all contracts hold, all scenarios pass.
> 7. **Iteration**: Evolves specs first when requirements change, then updates code.

## Customization

Each `.mdc` rule file has YAML frontmatter you can modify:

```yaml
---
description: What this rule does
globs: "**/*.ts"
alwaysApply: false
---
```

### Adjusting the Workflow

- **Lighter SDD**: Remove `core-devops.mdc` and `core-quality-gates.mdc` for smaller projects.
- **Backend only**: Remove `core-ux-design.mdc` and frontend-specific rules.
- **Different stack**: Edit `core-tech-stack.mdc` with your preferred technologies.
- **Minimal specs**: Use only OpenAPI + JSON Schema, skip Gherkin behavior specs.

## File Structure

```
bootstrap-IA/
├── README.md
├── AGENTS.md
├── CLAUDE.md
├── .gitignore
└── .cursor/
    └── rules/
        ├── core-workflow.mdc            # Master SDD workflow
        ├── core-planning.mdc            # Spec-driven planning
        ├── core-specification.mdc       # Spec authoring (NEW)
        ├── core-architecture.mdc        # Contract-first architecture
        ├── core-scaffolding.mdc         # Spec-driven scaffolding
        ├── core-implementation.mdc      # Spec-first implementation
        ├── core-quality-gates.mdc       # Conformance gates
        ├── core-iteration.mdc           # Spec-driven iteration
        ├── core-agent-orchestration.mdc # SDD agent patterns
        ├── core-devops.mdc              # CI/CD & infrastructure
        ├── core-tech-stack.mdc          # Technology selection
        ├── core-ux-design.mdc           # UX/UI design
        ├── global-*.mdc                 # 10 global quality rules
        └── specific-*.mdc              # 18 tech-specific rules
```

## Contributing

1. Fork the repository.
2. Create a feature branch: `feat/add-xyz-rule`.
3. Add or modify rules following the existing format.
4. Submit a PR with a description of the changes.
