---
title: "Customize bootstrap"
---

## Customization
### Table of contents
- [CSS customization](#css-customization)
  - [Example](#example)
  - [This site's bootstrap customizations](#this-sites-bootstrap-customizations)
- [Shortcode Customization](#shortcode-customization)

---

### CSS customization
To customize the bootstrap Sass Variables, create the file `assets/sass/bootstrap.scss`. Here you can add all the
customization features for the bootstrap CSS. The other bootstrap files are available in the `bootstrap/` namespace.\
Your can change the bootstrap variables to customize how bootstrap looks and feels.
For more information about customizing bootstrap, please refer to
[the Bootstrap Documentation](https://getbootstrap.com/docs/5.2/customize/).\
In the `assets/sass/bootstrap.scss` you can also just import the bootstrap components that you use inside of your site
to minify the css bundle. The shortcodes in this theme are all named after the bootstrap components.

#### Example
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

#### This site's bootstrap customizations
```sass
// assets/sass/bootstrap.scss

$code-color: #24292f;
$code-font-size: 85%;

$link-color: #267CB9;
$link-hover-color: #069;

@import "bootstrap/bootstrap";

@import "styles";
// By importing styles here, there is no need import the css manually
// as this file will be imported by the bootstrap partial.
```

```sass
// assets/sass/styles.scss

// ...

.carousel-item {
  img {
    max-height: 90vh;
  }

  .placeholder {
    height: 50vh;
  }

  .carousel-caption {
    h5 {
      color: red;
    }

    p {
      color: greenyellow;
    }
  }
}
```

---

### Shortcode customization
To change a shortcode, just copy the shortcode you want to change from
`themes/hugo-boostrap-shortcodes/layouts/shortcodes/` to `layouts/shortcodes/`.

In the file in `layouts/shortcodes/` you can now modify the shortcode's
behavior. \
Please refer to the
[hugo Documentation {{< icon "box-arrow-up-right" >}}](https://gohugo.io/documentation/)
for further information about how to write shortcodes and how to use
Go Templates in general.

{{< alert "info" "icon" >}}
Please be reminded, that if you do any changes in the shortcodes, you need to
open-sources your changes to that shortcode.
{{< /alert >}}
