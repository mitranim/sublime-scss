## Overview

CSS and SCSS syntaxes for Sublime Text. Complete redesign.

Goals:

* Simplicity.
* Graceful degradation.
* Usable symbol indexing and `goto_definition`.
* Compatibility with CSS extensions.
* Generalize special cases to open-ended principles.
* Design for open sets, not closed sets.
* Different scopes for declarations and references.
* Minimize maintenance.
* Minimize false positives.
* Minimize false negatives.
* False positives over false negatives.
* Reality over specs.

Non-goals:

* Validation of CSS properties. Use LSP/linter.
* Predefined autocompletion of CSS properties and values. Use LSP/linter, create your own AC file, or rely on ST's automatic AC.
* Ruby-like Sass syntax.
* "Smart" "helpful" typing aids.
* 100% spec conformance.

## Why

Compared to ST's built-in CSS package and existing Sass/SCSS packages, the design of these syntaxes is very different, and serves a different audience.  CSS is _**huge**_, keeps growing, and has various preprocessors and extensions.

Other packages are designed around _closed sets_ of whitelisted properties, tags, operators. They require constant updates, and produce large amounts of false negatives, such as for "unknown" properties. They're also not very compatible with CSS extensions.

This package is designed around general principles, and covers _open sets_ of possibilities, without relying on whitelists. It does not require updates for new CSS properties, property value keywords, or HTML tags. It requires updates only for completely new CSS syntax.

## Usage

Requires manual install. Example for MacOS:

```sh
git clone https://github.com/mitranim/sublime-scss.git
cd sublime-scss
ln -sf "$(pwd)" "$HOME/Library/Application Support/Sublime Text/Packages/"
```

To find the packages directory on your system, use Sublime Text menu → Preferences → Browse Packages.

**Disable other CSS and Sass/SCSS packages to avoid collisions.**

## Known Limitations

Not intentional, and may be addressed in the future.

* Scopes are simplified and slightly unconventional. Color scheme support may be limited.
* No hotkeys.
* No indent rules.
* No syntax tests.
* In local index (^R or ⌘R), symbols are "bare": `class` not `.class`.

## License

https://unlicense.org

## Misc

I'm receptive to suggestions. If this package _almost_ satisfies you but needs changes, open an issue or chat me up. Contacts: https://mitranim.com/#contacts
