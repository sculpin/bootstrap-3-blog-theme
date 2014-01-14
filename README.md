A Bootstrap 3 Blog Theme for Sculpin
====================================

Requirements
------------

This theme requires Bootstrap 3, font awesome, jQuery 1.9.*, and highlight.js.
Please see `_includes/custom/head.html` and `_includes/custom/after_footer.html`
to see where we expect these to live by default. Feelf ree to create fresh
copies of these files in `sources/_includes/custom/` to override these values if
you intend to install these dependencies elsewhere.

Installation
------------

Sculpin can automatically install this theme for you by adding the following to
your `sculpin.json`:

```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "git@github.com:sculpin/bootstrap-3-blog-theme.git"
        }
    ],
    "require": {
        "sculpin/bootstrap-3-blog-theme": "dev-master"
    }
}
```

Once installed, modify `app/config/sculpin_kernel.yml` like this:

```yaml
sculpin_theme:
    theme: sculpin/bootstrap-3-blog-theme
```

Lastly, if you have `sources/assets/css/style.css` already, and you have an
`@import` line that refers to a different theme, update it to point to this one:

```css
@import url('../../themes/sculpin/bootstrap-3-blog-theme/assets/css/style.css');
```

Easy Dependency Installation
----------------------------

The required dependencies can be installed easily by using Components Installer.
This requires some additional configuration in your `sculpin.json`.

```json
{
    "require": {
        "components/bootstrap": "3.0.3",
        "components/font-awesome": "4.0.3",
        "components/jquery": "1.9.1",
        "components/highlightjs": "~7.3.0",
    },
    "config": {
        "component-dir": "source/components"
    }
}
```

The `component-dir` is important as it will ensure that the components are
installed into your sources directory.


Not Invented Here
-----------------

Largely inspired by [Octopress](http://octopress.org/) classic theme.
