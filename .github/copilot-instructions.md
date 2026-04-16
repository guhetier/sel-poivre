
# Recipe Conventions

This repository is a Jekyll-based static site for cooking recipes.

- Concise, specific, to-the-point cooking recipes are the main and only goal. No vague instructions or filler descriptions.
- All recipes are in English, even if the recipe title is in French or French is used for technical terms.
- Metric units are used, except for small approximate measures. Temperatures are in Celsius, with Fahrenheit in parentheses.

## File Naming

All recipes live in `_posts/` as Markdown files.

```
YYYY-MM-DD-recipe-slug.md
```

- Date is the publish date.
- Slug is lowercase, hyphen-separated, in English even if the recipe title is French.

## Front Matter

```yaml
---
title: "Recipe Name"
categories:
  - Category Name
tags:                         # Optional; omit if no tags
  - Tag Name
sidebar:
  - title: Ingredients        # Use "Ingredients (Np)" when the recipe targets N servings
    text: |
      - Ingredient, quantity
---
```

## Ingredient List (sidebar `text` block)

- Named ingredients: `Ingredient Name, quantity+unit` — e.g., `Flour, 250g`, `Heavy cream, 20cL`, `Eggs, 3`
- Capitalize the ingredient name; lowercase units (SI notation, `cL`, `mL`, `g`)
- Use metric units (`g`, `mL`, `cL`...), except for small approximate measures where `tsp`, `tbsp` or `a pinch` are preferable
- Approximate amounts: prefix with `~`

## Recipe body

```markdown
One-line description of the dish. No heading above it.

# Instructions

- Do this step.
- Do that step.
```

- Keep the description to one short sentence; state what the dish is or what makes it notable.

## Instructions Section

- Use `# Instructions` as the section heading.
- Write steps as a bullet list (`-`), not a numbered list.
- Use the imperative form: "Cut", "Mix", "Add", "Deglaze".
- Be concise, omit filler, use specific technical terms rather than vague descriptions.
- For complex recipes with distinct components, add `## Sub-section` headings inside `# Instructions`.

**Formatting rules inside steps:**

| Element | Format | Example |
|---------|--------|---------|
| Temperature | Bold Celsius + Fahrenheit in parentheses | `**180°C** (356°F)` |
| Duration | Bold | `**45 minutes**`, `**5 min**` |
| Inline quantity | Bold | `**30g**` of butter |

## Cross-Recipe Links

Link to other recipes using the `post_url` Liquid tag:

```markdown
[Recipe Name]({{ "" | relative_url }}{% post_url YYYY-MM-DD-slug %})
```

## Notes Section (optional)

Use a `# Notes` section at the end for substitutions, variations, or tips:

```markdown
# Notes

- The X can be replaced with Y.
```
