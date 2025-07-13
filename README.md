# VSRegexX

**Turn your VSCode-style regex find & replace patterns into ready-to-run `perl` commands.**

VSRegexX helps you bridge the gap between GUI regex workflows and CLI automation. No more guessing how to convert `$1` or escaping slashes? This tool handles it for you.

---

## Features

-  Convert VSCode search/replace regex to:
  - `perl -pe` command-line one-liners
-  Automatically escapes slashes and special characters
- Converts `$1`, `$2`, ... to appropriate syntax
-  Simple, fast, browser-based utility (no backend)

---

## Live Demo

[Try VSRegexX Online](https://a1245967.github.io/VSRegexX/)

---

## Example

### Input

- Search pattern: `(\d+)\s+items?`
- Replace pattern: `Found $1 item(s)`

### Output

```bash
# Perl
perl -pe 's/(\d+)\s+items?/Found $1 item(s)/g'
```