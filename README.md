# Website perso based on Plainwhite theme

**Source**: [samarsault.com](https://samarsault.com)


## Usage

The "plainwhite" key in \_config.yml is used to customize the theme data.

```yaml
plainwhite:
  name: Adam Denisov
  tagline: Developer. Designer
  date_format: "%b %-d, %Y"

  social_links:
    twitter: samarsault
    github: samarsault
    linkedIn: in/samarsault # format: locale/username
```

**Updating Placeholder Image**

The placeholder portfolio image can be replaced by the desired image by placing it as `assets/portfolio.png` in your jekyll website, or by changing the following line in `_config.yaml`

```yaml
plainwhite:
  portfolio_image:  "assets/portfolio.png" # the path from the base directory of the site to the image to display (no / at the start)
```

To use a different image for dark mode, e.g. with different colors that work better in dark mode, add a `portfolio_image_dark` entry in addition to the `portfolio_image`.

```yaml
plainwhite:
  portfolio_image:      "assets/portfolio.png"
  portfolio_image_dark: "assets/portfolio_dark.png"
```

**Comments (Disqus)**

Comments on posts can be enabled by specifying your disqus_shortname under plainwhite in `_config.yml`. For example,

```yaml
plainwhite:
  disqus_shortname: games
```

**Google Analytics**

It can be enabled by specifying your analytics id under plainwhite in `_config.yml`

```yaml
plainwhite:
  analytics_id: "< YOUR ID >"
```

**Sitemap**

It can be toggled by the following line to under plainwhite in `_config.yml`

```yaml
plainwhite:
  sitemap: true
```

**Excerpts**

Excerpts can be enabled by adding the following line to your `_config.yml`

```yaml
show_excerpts: true
```

**Layouts**

- Home
- Page
- Post

**Navigation**

Navigation can be enabled by adding the following line to your `_config.yml`

```yaml
plainwhite:
  navigation:
    - title: My Work
      url: "/my-work"
    - title: Resume
      url: "/resume"
```

**Mobile**

By default, Plainwhite places the sidebar (logo, name, tagline etc.) above the content on mobile (narrow screens).
To condense it (moving some things to the bottom of the page and making the rest smaller) so it takes up less space, add the following to your `_config.yml`:

```yaml
plainwhite:
  condensed_mobile:
    - home
    - post
    - page
```

This chooses which layouts (types of page) should be condensed on mobile screens. E.g. if you want everything but the landing page to be condensed, remove `home` from the list. This option does not affect rendering on wider screens.

**Dark mode**

Dark mode can be enabled by setting the `dark_mode` flag in your `_config.yml`

The website will check the OS preferred color scheme and set the theme accordingly, the preference will then be saved in a cookie

```yaml
plainwhite:
  dark_mode: true
```


**Multiline tagline**

Tagline can be multiline in this way

```yaml
plainwhite:
  tagline: |
  First Line. 

  Second Line. 

  Third Line.
```

**Search-bar**

Search-bar can be enabled by adding the following line to `config.yml`

```yaml
plainwhite:
  search: true
```

Search is powered by [Simple-Jekyll-Search](https://github.com/christian-fei/Simple-Jekyll-Search) Jekyll plugin. A `search.json` containing post meta and contents will be generated in site root folder. Plugin JavaScript will then match for posts based on user input. More info and `search.json` customization documentation can be found in plugin repository.

**Base URL**

You can specify a custom base URL (eg. example.com/blog/) by adding the following line to `_config.yaml`. Note that there is no trailing slash on the URL.

```yaml
baseurl: "/blog"
```

**Language**

You can set the `lang` attribute of the `<html>` tag on your pages by changing the following line in `_config.yml`:

```yaml
plainwhite:
  html_lang: "en"
```

