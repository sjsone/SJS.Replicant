# SJS.Replicant

## Quick Start

Create or Update your `CLAUDE.md` file with:

```markdown
## Neos Documentation

General Neos Documentation for Coding Agents: @Packages/Documentation/SJS.Replicant/Documentation/AGENTS.md
```

> [!IMPORTANT]
> Symlinks are not followed!
> If your package is in `DistributionPackages` do not use `@Packages/...` but `@DistributionPackages/...`

Run `/context` in claude-code to check if everything looks good:

```bash
Memory files · /memory
     └ ~/.claude/CLAUDE.md: 131 tokens
     └ CLAUDE.md: 43 tokens
     └ Packages/Documentation/SJS.Replicant/Documentation/AGENTS.md: 34 tokens
     └ Packages/Documentation/SJS.Replicant/Documentation/NeosOverview.md: 79 tokens
     └ Packages/Documentation/SJS.Replicant/Documentation/IdealProjectStructure.md: 273 tokens
     └ Packages/Documentation/SJS.Replicant/Documentation/CodingGuidelines.md: 364 tokens
     └ Packages/Documentation/SJS.Replicant/Documentation/NeosContentRepository.md: 88 tokens
```

Then test it with:
> Does my package in DistributionPackages/Vendor.Site adhere to the ideal package layout?
or:
> Check if all the annotations are good
