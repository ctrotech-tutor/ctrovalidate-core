# ctrovalidate-core

**Zero-dependency, platform-agnostic validation engine for JavaScript and TypeScript.**

[![npm version](https://img.shields.io/npm/v/ctrovalidate-core.svg)](https://www.npmjs.com/package/ctrovalidate-core)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

The headless validation engine at the heart of the Ctrovalidate ecosystem. Provides pure validation logic with zero runtime dependencies — runs in Node.js, browsers, edge functions, and any JavaScript environment.

---

## Installation

```bash
npm install ctrovalidate-core
```

---

## Quick Start

```typescript
import { validate } from 'ctrovalidate-core';

const results = validate(
  { email: 'user@example.com', age: 25 },
  { email: 'required|email', age: 'required|min:18' }
);
// { email: { isValid: true, error: null, rule: null }, age: { ... } }
```

---

## API Overview

| Function | Description |
|----------|-------------|
| `validateValue(value, rules, options?)` | Validate a single value synchronously |
| `validate(data, schema, options?)` | Validate an entire data object synchronously |
| `validateValueAsync(value, rules, options?)` | Validate a single value asynchronously |
| `validateAsync(data, schema, options?)` | Validate an entire data object asynchronously |

**Full documentation:** [ctrovalidate-core API Reference](https://ctrovalidate.vercel.app/api/core) · [Guide](https://ctrovalidate.vercel.app/guide/core)

---

## Features

- **22 built-in rules**: `required`, `email`, `min`, `max`, `minLength`, `maxLength`, `alpha`, `alphaNum`, `alphaDash`, `alphaSpaces`, `numeric`, `integer`, `decimal`, `url`, `ipAddress`, `json`, `phone`, `creditCard`, `strongPassword`, `exactLength`, `between`, `sameAs`
- **4 validation functions**: Sync and async, single value and full object
- **Schema formats**: String (`"required|email"`), array, or hybrid
- **Rule aliases**: Recursive macro expansion with cycle protection
- **i18n**: Built-in `Translator` with locale switching and parameter interpolation
- **Async support**: `AbortSignal` integration for race-condition-free remote validation
- **Zero dependencies**: ~5KB minified

---

## Documentation

- [Full API Reference](https://ctrovalidate.vercel.app/api/core)
- [Core Concepts Guide](https://ctrovalidate.vercel.app/guide/core)
- [Rules Catalog](https://ctrovalidate.vercel.app/guide/rules)
- [Schema System](https://ctrovalidate.vercel.app/guide/schemas)
- [Custom Rules](https://ctrovalidate.vercel.app/advanced/custom-rules)
- [Async Validation](https://ctrovalidate.vercel.app/advanced/async)
- [i18n & Localization](https://ctrovalidate.vercel.app/advanced/i18n)

---

## License

MIT © [Ctrotech](https://github.com/ctrotech-tutor)
