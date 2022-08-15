---
title: "Home"
---

# hugo-bootstrap-shortcodes

This hugo theme makes it really easy to use any bootstrap components!

- [Installation](#installation)
- [Usage](#usage)
- [Overview of the shortcodes]({{< relref "shortcodes/_index.md" >}})

---

## Installation
If you use git to index your site, add this repository as a submodule to your
themes folder:

```bash
git submodule add https://github.com/MaFeLP/hugo-bootstrap-shortcodes themes/hugo-bootstrap-shortcodes
git submodule foreach git submodule init
git submodule update --recursive
```

Otherwise just clone the files:

```bash
git clone https://github.com/MaFeLP/hugo-bootstrap-shortcodes --depth=1 --recursive themes/hugo-bootstrap-shortcodes
```

After any one of the last commands, you need to mount the static files of this
theme and enable it in your `config.toml`:

```toml
theme = ["hugo-bootstrap-shortcodes"]

[module]
[[module.mounts]]
source = 'assets'
target = 'assets'
[[module.mounts]]
source = 'assets/sass'
target = 'assets/sass'
[[module.mounts]]
source = 'assets/fonts'
target = 'assets/fonts'
```

if you use YAML, include the following into your `config.yml`:

```yaml
theme:
  - 'hugo-bootstrap-shortcodes'

module:
  mounts:
    - source: 'assets'
      target: 'assets'
    - source: 'assets/sass'
      target: 'assets/sass'
    - source: 'assets/fonts'
      target: 'assets/fonts'
```

---

## Usage
To be able to use any of the bootstrap components, you need to insert the
partial `bootstrap` into the head of your site:

```markdown
...
<head>
...
    {{- partial "bootstrap" }}
...
</head>
...
```

See `exampleSite/layouts/_default/single.html` for a real world example.

You can then use any of the [shortcodes](./shortcodes/) in any
of your markdown files!
