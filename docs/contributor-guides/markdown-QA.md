# Markdown Quality Assurance Guide

To ensure high-quality markdown files in this repository, contributors must use **Vale** for spell and grammar checking and **markdownlint-cli** for markdown formatting before committing changes.

## Running Vale for Spell and Grammar Checking

Vale checks markdown files for spelling, grammar, and style issues. To run Vale, use:

```sh
vale .
```

If Vale reports issues, follow its suggestions to improve readability, grammar, and style.

### Vale Configuration

Vale uses a `.vale.ini` file in the root directory with:
- **Style Guide**: Google Developer Documentation Style Guide
- **Supplementary Style**: write-good
- **Markdown Support**: MDX

## Running markdownlint for Markdown Formatting

markdownlint-cli ensures markdown files follow best practices. To check markdown formatting, run:

```sh
markdownlint .
```

### markdownlint Configuration

This repository uses a `.markdownlint.json` file with:

```json
{
    "MD013": false
}
```

This disables the line-length restriction.

## Running Both Commands Together

To check both spelling/grammar and markdown formatting in one step, run:

```sh
vale . && markdownlint .
```

## Best Practices

Before committing any markdown files, always run both checks:

1. **Check for spelling, grammar, and style issues:**
   ```sh
   vale .
   ```

2. **Check for markdown formatting issues:**
   ```sh
   markdownlint .
   ```

Fix any reported issues to maintain consistency and readability in the documentation.
