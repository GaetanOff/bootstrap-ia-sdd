# Bootstrap IA — SDD 🚀

🛠️ **A Spec Driven Development ruleset that transforms Cursor into a specification-first project generation engine. Specs are the single source of truth.**

## 📌 Features

✅ **Spec Driven Development methodology** (specifications drive planning, architecture, implementation, testing, documentation)  
✅ **Formal specs before any code** (OpenAPI, JSON Schema, Gherkin)  
✅ **Contract-first architecture** (design driven by specs, not assumptions)  
✅ **Conformance tests from specs** (generated before implementation)  
✅ **Spec conformance gates** at every step  
✅ **Spec-first iteration** (specs evolve first, then code follows)  
✅ **18+ language/framework support** (TypeScript, React, Next.js, Python, Rust, Go, C#, Java, and more)  

## 🔌 Compatibility

| Tool | File | Format |
|------|------|--------|
| **Cursor** | `.cursor/rules/*.mdc` | MDC with YAML frontmatter |
| **Claude Code** | `CLAUDE.md` | Markdown (project root) |
| **OpenCode / Agents** | `AGENTS.md` | Markdown (project root) |

## 📦 Installation

### 1️⃣ Clone the project

```bash
git clone https://github.com/GaetanOff/bootstrap-ia-sdd.git
cd bootstrap-ia-sdd
```

### 2️⃣ Copy to your project — Full Bootstrap

```bash
# Copy all rules to your project
cp -r bootstrap-IA/.cursor/ /path/to/your-project/.cursor/

# Copy agent entrypoints
cp bootstrap-IA/AGENTS.md /path/to/your-project/
cp bootstrap-IA/CLAUDE.md /path/to/your-project/
```

### 3️⃣ Cherry-Picking Rules

Copy only the rules you need:

```bash
# Core SDD workflow rules only
cp bootstrap-IA/.cursor/rules/core-*.mdc /path/to/your-project/.cursor/rules/

# Global quality rules only
cp bootstrap-IA/.cursor/rules/global-*.mdc /path/to/your-project/.cursor/rules/

# Specific tech rules (pick what you need)
cp bootstrap-IA/.cursor/rules/specific-typescript.mdc /path/to/your-project/.cursor/rules/
cp bootstrap-IA/.cursor/rules/specific-react.mdc /path/to/your-project/.cursor/rules/
```

## ⚙️ Configuration

Each `.mdc` rule file has YAML frontmatter you can modify:

```yaml
---
description: What this rule does
globs: "**/*.ts"       # File pattern (specific rules only)
alwaysApply: false     # Set to true to always apply
---
```

### Adjusting the Workflow

- **Lighter SDD**: Remove `core-devops.mdc` and `core-quality-gates.mdc` for smaller projects.
- **Backend only**: Remove `core-ux-design.mdc` and frontend-specific rules.
- **Different stack**: Edit `core-tech-stack.mdc` with your preferred technologies.
- **Minimal specs**: Use only OpenAPI + JSON Schema, skip Gherkin behavior specs.

## 📜 What is Spec Driven Development?

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

## 📜 Rules Overview

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

## 🚀 Usage

### 1️⃣ Using with Cursor

1. Copy the rules into your project's `.cursor/rules/` directory.
2. Open the project in Cursor.
3. Start a conversation — the AI will automatically follow the SDD workflow.
4. For new projects, begin with: *"I want to build [description]. Let's start with discovery and specification."*

### 2️⃣ Using with Claude Code

Place `CLAUDE.md` at your project root. Claude Code reads it automatically.

### 3️⃣ Using with OpenCode / Other Agents

Place `AGENTS.md` at your project root.

## 💡 SDD Workflow Example

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

## 📂 Project structure

```
bootstrap-IA/
├── README.md                    # 📖 Documentation
├── AGENTS.md                    # 🤖 Entrypoint for OpenCode / agents
├── CLAUDE.md                    # 🧠 Entrypoint for Claude Code
├── .gitignore
└── .cursor/
    └── rules/
        ├── core-workflow.mdc            # 🔄 Master SDD workflow
        ├── core-planning.mdc            # 📋 Spec-driven planning
        ├── core-specification.mdc       # 📝 Spec authoring (NEW)
        ├── core-architecture.mdc        # 🏗️ Contract-first architecture
        ├── core-scaffolding.mdc         # 🏭 Spec-driven scaffolding
        ├── core-implementation.mdc      # ⚡ Spec-first implementation
        ├── core-quality-gates.mdc       # ✅ Conformance gates
        ├── core-iteration.mdc           # 🔁 Spec-driven iteration
        ├── core-agent-orchestration.mdc # 🤖 SDD agent patterns
        ├── core-devops.mdc              # 🚀 CI/CD & infrastructure
        ├── core-tech-stack.mdc          # 🛠️ Technology selection
        ├── core-ux-design.mdc           # 🎨 UX/UI design
        ├── global-*.mdc                 # 🌍 10 global quality rules
        └── specific-*.mdc              # 🔧 18 tech-specific rules
```

## 📝 License

All the code is licensed under GPL v3.
Feel free to modify and improve it! 😃

## 🙌 Contributing

1. Fork the repository.
2. Create a feature branch: `feat/add-xyz-rule`.
3. Add or modify rules following the existing format.
4. Submit a PR with a description of the changes.

💡 Ideas, suggestions, or bugs?
Open an issue or submit a pull request!

## 📬 Contact

📧 contact@gaetandev.fr
🌍 [Website](https://gaetandev.fr)
💬 Discord: GaetanDev

## 🎉 Thank you for using Bootstrap IA — SDD!

If you have any questions or suggestions, let me know! 🚀😃
