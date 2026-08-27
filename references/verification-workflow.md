# Verification Workflow

## Task Card

Before editing, record objective, authorized scope, directly related files, risks, verification level, and completion conditions. Group related adjustments before implementation to avoid repeated scans and full-suite runs.

## Verification Levels

### L1: Low Risk

For prose, documentation, or narrow presentation changes: inspect the diff, run the relevant documentation validator, and inspect only affected visuals when appearance changed.

### L2: Module Risk

For one feature, parser, lifecycle, or behavior: run focused tests and add type or build checks when crossing a compile or bundle boundary.

### L3: Stage or Commit Boundary

For a completed feature stage, repository guard change, dependency change, or final commit: run the full test suite, lint, build, security or protected-code guards, documentation checks, and targeted desktop/mobile UI review when applicable.

## Automated Documentation Checks

A validator accepts explicit paths and optional configuration. Check frontmatter; one H1 and no heading jumps; configured numbered sections; unique identifiers and exact index/detail agreement; prefix, type, and label consistency; type-specific required fields; end time and evidence for completed records; release copy for candidates; and document update time.

The validator reads only specified files, emits actionable diagnostics, and never modifies documentation.

## Repository Integration

Compose documentation validation with existing pre-commit guards. Do not replace protected-code, secret, private-research, or build-leak checks. Inspect staged paths before committing so fixtures, generated outputs, and private materials remain excluded.
