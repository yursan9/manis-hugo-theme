# Manis Hugo Theme

It's a minimalist and responsive theme for Hugo Static Site Generator. It's
name taken from Indonesian Language for *Sweet*.

![Manis' Homepage view](https://raw.githubusercontent.com/yursan9/manis-hugo-theme/master/images/tn.png)

## Features

Like I said, it's really minimal. Its doesn't even have grid or anything nice like that.

- Configurable color!
- Code Highlighting (HighlightJS).
- Responsive.
- Social Icon Links.
- No Grid no worry.
- Disqus Support.
- Translatable.

![Manis' Colorful scheme](https://raw.githubusercontent.com/yursan9/manis-hugo-theme/master/images/blue-red.png)

## Installation

To install Manis, you can clone this repository. The following command will clone Manis in your site's base directory.

```
cd path/to/site/dir
git clone https://github.com/yursan9/manis-hugo-theme themes/manis
```

## Configuration

For configuration example you can look at the `exampleSite/config.toml` (and copy that too!). I put some commentary to, hopefully, guide you at using this theme.

### Disqus Configuration
To add Disqus support, edit your site `config.toml`. Add your discus' shortname to `disqusShortname` and add list of sections that you want to support disqus to `params.disqusSections`:

```toml
disqusShortname = "your-disqus-shortname"

[params]
	disqusSections = ["blog"]
```

### Making Own Navigation Bar

Top navigation bar in Manis is made automatically by making new `section/_index.md`. Example if you want to add/remove navigation items, you can do the following command:

```
hugo new {Section Name}/_index.md
```

And make sure the front matter is formatted like this:

```
+++
title = "Get To Know Me"
menu = "main"
+++
```

`title` will be the string that is shown in navigation bar and the page's title (the title doesn't need to be the same as section's name). `menu = "main"` is the one who make Hugo know how identify it's need to add a new item in navigation bar.

## Other Language

Manis already translated to Bahasa Indonesia. But, if you want to translate this theme to your own language, look for the example in `i18n/en.yaml` and `i18n/in.yaml`.

And then you edit the site's `config.toml` like this.
```
defaultContentLanguage = "en"
[languages.{Your Language Code}]
    lang = "{Your Language Code}"
    languageName = "{Your Language Name. example; Bahasa Indonesia or Japanese}"
    weight = 1
```

## Development

If you found bug, or anything that itch you. Tell me! or maybe make PR.

## License

Manis is licensed under the MIT License. Check the [LICENSE](https://github.com/yursan9/manis-hugo-theme/blob/master/LICENSE.md) file for details.
