# A Tree of AI Model Names

An interactive tree of every major AI model name, version, and naming crime committed by the industry.

Published at [sajarin.com/blog/modeltree](https://sajarin.com/blog/modeltree/).

## Contributing

Edit `models.yaml` and open a PR. That's the only file you need to touch.

Each company is a top-level entry:

```yaml
- name: Company Name
  company: companyid          # used for CSS color class (co-companyid)
  tagline: "short description"
  children:
    - name: Model Name
      date: "Month Year"      # always quoted
      url: https://example.com # announcement or blog post link
      tip: "<strong>Bold text.</strong> Tooltip shown on hover."  # always quoted, supports HTML
      note: "red annotation"
      note_dim: "gray annotation"
      dead: true              # strikethrough for discontinued models
      section: true           # uppercase label for grouping
      children:               # nested models
        - name: Sub-model
```

### Rules

- `date` values must be quoted (`"Jun 2024"`, not `Jun 2024`)
- `tip` values must be quoted (they contain HTML)
- Use `dead: true` for discontinued/unreleased models
- Use `section: true` for category headers (e.g., "GPT Series", "The -stral Universe")
- Every name listed must be real

## Files

| File | Purpose |
|------|---------|
| `models.yaml` | All model data — the only file contributors edit |
| `model-tree.js` | Web component that renders the tree |

## License

[MIT](LICENSE). The model names belong to their respective companies, who should probably hire a naming consultant.
