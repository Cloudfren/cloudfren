# Domain Docs

How engineering agents should consume this repository's domain documentation.

## Before exploring, read these

- **`CONTEXT.md`** at the repository root, if it exists.
- **`docs/adr/`**: read decisions that touch the area being changed.

If these files do not exist, proceed without flagging their absence. Create or update them when domain terms or architectural decisions are resolved, rather than preemptively inventing project commitments.

## Layout: single-context

This repository uses one shared product and domain context:

```text
/
├── CONTEXT.md
└── docs/
    └── adr/
```

## Use the domain vocabulary

Use terms as defined in `CONTEXT.md` when referring to domain concepts in issues, proposals, hypotheses, and tests. If a needed concept is not defined, identify it as a gap instead of silently creating competing terminology.

## Flag decision conflicts

If proposed work conflicts with an existing ADR, call out the conflict explicitly rather than silently overriding the recorded decision.
