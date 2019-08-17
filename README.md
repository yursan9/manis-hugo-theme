# Manis Hugo Theme

It's a minimalist and responsive theme for Hugo Static Site Generator. It's
name taken from Indonesian Language for *Sweet*.

> Note: Manis going to follow [SEMVER](https://semver.org/) scheme from now. It's mean you can clone this repository from master without breaking.

![Manis' Mockup Device](https://raw.githubusercontent.com/yursan9/manis-hugo-theme/master/images/mockup.jpg)

## Features

Like I said, it's really minimal. Its doesn't even have grid or anything nice like that.

-   Configurable color!
-   Code Highlighting (HighlightJS).
-   Print.css (for single post only)
-   Responsive.
-   Social Icon Links.
-   No Grid no worry.
-   Disqus Support.
-   Translatable.

![Manis' Homepage view](https://raw.githubusercontent.com/yursan9/manis-hugo-theme/master/images/blue-red.png)

## Get Started

If this is your first time using Hugo, and you want to use this theme. Follow the instruction below:

```
mkdir name_of_web
cd name_of_web
git clone https://github.com/yursan9/manis-hugo-theme themes/manis
cp themes/manis/exampleSite/config.toml config.toml
hugo new blog/hello.md
```

Edit the `config.toml` according to your preference. Then edit `content/blog/hello.md` to
start writing your first post. (Look at the `exampleSite/content` for example.)

### Theme Only

To only install Manis, you can clone this repository. The following command will clone Manis in your site's base directory.

```
cd path/to/site/dir
git clone https://github.com/yursan9/manis-hugo-theme themes/manis
```

Ensure you have `blog` and `work` sections to make this theme works.

```
content/
├── blog
│   └── _index.md
└── work
    └── _index.md
```

## Configuration

For configuration example you can look at the `exampleSite/config.toml` (and copy that too!). I put some commentary to, hopefully, guide you at using this theme.

### Change Latest Section

You can edit which sections show up as latest posts and latest works by editing `mainSections` and `workSections`. `workSections` is optional.

```toml
# Configure which sections for Latest Posts
mainSections = ["blog", "post"]
# Configure which sections for Latest Works
workSections = ["work"]
```

### Disqus Configuration
To add Disqus support, edit your site `config.toml`. Add your discus' shortname to `disqusShortname` and add list of sections that you want to support disqus to `params.disqusSections`:

```toml
disqusShortname = "your-disqus-shortname"

[params]
  disqusSections = ["blog"]
```

### Making Own Navigation Bar

Top navigation bar in Manis is made by configuring the navigation bar in `config.toml` with the following code:

```
[menu]
    [[menu.main]]
        name = "Blog"
        url = "/post/"

    [[menu.main]]
        name = "About"
        url = "/about"

```

### Other Language

Manis already translated to Bahasa Indonesia. But, if you want to translate this theme to your own language, look for the example in `i18n/en.yaml` and `i18n/in.yaml`.

And then you edit the site's `config.toml` like this.

```toml
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
