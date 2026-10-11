<!-- THUBAN:PROTOCOL v2 -->

# Nodes, growth, and startup

Read the sections needed for the current structure change. Existing v1 contracts use [Compatibility](COMPATIBILITY.md).

## Node format

Use the project's language. A node needs Scope and only the remaining sections that affect future work.

```markdown
<!-- THUBAN:NODE v2 -->
# Thuban — <area>

## Scope
- Owns: <project or local responsibility>
- Excludes: <adjacent areas that would otherwise be confused>
- Parent: <direct parent THUBAN.md; omit at root>

## Contract
- <project-specific invariant, evidence owner, or decision boundary>

## State
- <useful verified local fact or explicitly chosen transition>

## Routes
| Read when | Path | Contribution |
|---|---|---|
| <recognizable task> | `<concrete file>` | <responsibility and evidence role> |
```

Keep node rules specific to the project. Ordinary source documents retain their names and formats. State belongs at the narrowest owner; the root carries cross-scope consequences. Date a fact only when its time sensitivity matters.

## Topology and growth

One root governs the adopted scope. Each child has one direct parent, and that parent routes to the child under an observable task condition. Cross-branch task routes are allowed; ownership remains a tree.

Create a child when independent ongoing work, distinct local decisions/context, and the cost of recovering that context justify a gateway. Clear evidence can justify one on first adoption. A small tool may need only its root. Several responsibilities may share a node when they share the same context and decisions.

When scope grows, consider splitting. When responsibilities converge or a node becomes an unnecessary forwarding layer, merge its useful contract/routes into the remaining owner and retire the old node. Update parents, consumers, and any local bootstrap together. Preserve a recovery copy; keep a redirect only for a known consumer that cannot be updated.

Record external or generated areas at their nearest owned boundary. Their directory size does not create governance ownership.

## Routes and the human map

A route says when to read, which concrete file to open, and what it contributes. Prefer the nearest useful gateway; let it select task-local artifacts. Combine related conditions for the same target. For a large file, identify the relevant heading or search term rather than creating an index solely for its length.

Use existing README/architecture/index files to show the overall structure and important-file responsibilities. A small project's table may suffice; a multi-area project can benefit from a diagram. The human map explains the project; nodes route tasks. Keep them consistent when the structure changes without copying full contracts or status into both.

Respect the effective AGENTS instructions already loaded. Route downstream toward evidence, not back into a startup loop.

## Startup

Inspect the effective instruction chain and nested scopes. In a project-owned AGENTS.md, maintain one matched bootstrap block; preserve unrelated content and authority. If none exists, an authorized adoption may create a minimal local AGENTS.md. Select a placement that governs the intended scope without modifying broader ancestors.

```markdown
<!-- THUBAN:BOOTSTRAP v2 -->
For project work, read `THUBAN.md` and follow the routes needed for the task. After authorized changes, apply its Maintenance contract. “右枢” or an explicit full-governance request invokes $thuban for the current scope; review/discussion requests keep their stated scope.
<!-- /THUBAN:BOOTSTRAP -->
```

Resolve effective competing startup/maintenance rules as part of authorized adoption; adding another block above a conflict does not resolve it. Preserve substantive project constraints and useful documents. Unknown, duplicate, or unbalanced markers need explicit interpretation before replacement. If startup cannot be made effective within the owned scope, report passive adoption and how to invoke it.

## Maintenance contract

Newly adopted v2 roots include this rule, translated to project language and constrained by local ownership where needed. Children inherit it.

```markdown
## Maintenance
After authorized work, update verified facts, instructions, routes, and the human-facing map affected by that work. Within that affected scope, use $thuban when node growth, merging, retirement, or document/directory reorganization is justified; continue under the existing task authorization for recoverable local changes. Preserve project constraints, user-owned goals/priorities, and protected records. Ask about a material expansion or unresolved authority. “右枢” requests a complete governance pass for the current project; routine tasks maintain their actual impact. With no changed truth, leave files unchanged.
```

Maintenance is performed by the working agent when tasks occur. A separate automation requires its own setup; these files do not run a watcher.
