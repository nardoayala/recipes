# Recipes

Personal recipe collection stored in [Cooklang](https://cooklang.org/) format.

## Structure

```
recipes/
├── pastas/
│   └── pesto.cook
├── postres/
│   ├── marquesa-chocolate.cook
│   └── roles-de-canela.cook
└── config/
    └── aisle.conf       # Supermarket aisle order for shopping lists
```

## Usage

Requires the [CookCLI](https://cooklang.org/cli/help/) tool.

```bash
# View a recipe
cook recipe read pastas/pesto.cook

# Generate a shopping list
cook shopping-list pastas/pesto.cook postres/roles-de-canela.cook

# Start the recipe server
cook server
```

## Format

Recipes are plain `.cook` text files using Cooklang syntax:

- `@ingredient{amount%unit}` — ingredients
- `#tool{}` — cookware
- `~{time%unit}` — timers
- `== Section ==` — recipe sections
- YAML frontmatter for metadata (title, tags, servings, etc.)
