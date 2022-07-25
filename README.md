# Hugo Bootstrap Shortcodes
A simple hugo theme that allows for easy usage of some bootstrap components via templating.

- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Documentation](#documentation)

## Installation
Add this repository as a submodule to your themes folder:

```bash
git submodule add https://github.com/MaFeLP/hugo-bootstrap-shortcodes themes/hugo-bootstrap-shortcodes
git submodule update --recursive
```

Add the following to your `config.toml`.

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

## Usage
To import the stylesheets, javascript and fonts (used for the bootstrap icons), just include the partial
`bootstrap.html` into your header:

```html
<head>
...
  {{- partial "bootstrap.html" }}
...
</head>
```

For the usage of the individual components, please refer to [the Documentation](#documentation).

## Customization
To customize the bootstrap Sass Variables, create the file `assets/sass/bootstrap.scss`. Here you can add all the
customization features for bootstrap. The other bootstrap files are available in the `bootstrap/` namespace.\
For more information about customizing, please refer to
[the Bootstrap Documentation](https://getbootstrap.com/docs/5.2/customize/).\
In the `assets/sass/bootstrap.scss` you can also just import the bootstrap components that you use inside of your site
to minify the css bundle. The shortcodes in this theme are all named after the bootstrap components.

### Example
```sass
// Change the background color

// Import bootstrap functions for manipulations
@import "bootstrap/functions";

// Customize bootstrap
$body-bg: #000;
$body-color: #FFF;

// Import the rest of bootstrap
@import "bootstrap/bootstrap";
```

## Documentation
Documentation is built with GitHub Actions and available under <https://mafelp.github.io/hugo-bootstrap-shortcodes>.
The source code for this documentation is available inside of the `exampleSite` folder and uses this theme as well.

---

This theme is based on [Bootstrap](https://github.com/twbs) and their icons.

This theme is licensed under the [GNU Lesser General Public License version 3.0
or later](./LICENSE). The terms and conditions of the GNU General Public
License version 3.0 or later, which are incorporated by the GNU Lesser General
Public License version 3.0 can be found at [`LICENSE.GPLv3`](./LICENSE.GPLv3).
