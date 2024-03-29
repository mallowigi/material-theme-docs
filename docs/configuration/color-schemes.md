---
layout: docs
title: Color Schemes
description: Installation and Configuration
group: configuration
comments: true
toc: true

previous:
  url: '/docs/configuration/settings'
  title: Settings
next:
  url: '/docs/configuration/main-settings'
  title: Main Settings
---

The plugin comes prebundled with a bunch of color schemes adapted for the Material Themes, resulting in a flat,
borderless and slick experience.
{:class='title'}

{% include carbonads.html %}

## Installation

There are multiple ways to change the color scheme:
- Through the settings, in `Editor → Color Schemes`
- Through the `Quick Switch`, with the first option `Color Scheme`.

{% include figure.html content="/screens/quickswitch.png" caption="Quick Switch" %}

In this list you'll find all your installed color schemes alongside those provided by JetBrains. The color schemes provided by the plugin are:

<ul>
{% for theme in site.data.themes.material %}
    <li>Material {{ theme.name }}</li>
{% endfor %}

{% for theme in site.data.themes.material2 %}
    <li>Material {{ theme.name }}</li>
{% endfor %}

{% for theme in site.data.themes.other %}
    <li>{{ theme.name }}</li>
{% endfor %}

{% for theme in site.data.themes.other2 %}
    <li>{{ theme.name }}</li>
{% endfor %}
</ul>

## Customization

Though the color schemes have been made for an optimal day-to-day usage, if there are colors you don't like,
you can create your own configuration and select which colors or fonts are best suited for you.

To do so, open the `Colors and Fonts` editor at `Settings → Editor → Color Scheme`,
then click on the small icon next to the scheme selector and select `Duplicate`.
This will create a copy of the color scheme that you can customize at your own will.

{% include figure.html content="/screens/colorschemes.png" caption="Color Scheme Editor" %}


You can also directly modify the original color schemes, and it will create a copy in the colors' folder with the name `_@user_<schemeName>.icls`.
The color scheme will then appear in *accent color* in the list.

However, if you enabled the
[Automatically reset color schemes](/docs/configuration/other-tweaks-settings#automatically-reset-color-schemes) option (which is recommended),
your changes will not be persisted, so _duplicate_ is a better option.

To revert the copies to their original state, in the previous menu select `Restore Defaults`.
Or, you can run the [Reset Color Scheme](/docs/configuration/quick-actions-panel#material-theme-features) action from the [Quick Actions Panel](/docs/configuration/quick-actions-panel).

Be careful, though, as that means that __all the changes you've made will be lost__.
Therefore, it is preferable that you make a copy (of the copy) using the `Duplicate` function, this way you can always go back to your changes one by one.

----------
## Supported languages

|              |             |             |
|:-------------|:------------|:------------|
| Java         | Properties  | Erlang      |
| Gradle       | Yaml        | Elm         |
| Groovy       | JSON        | Matlab      |
| Scala        | Ruby        | Haskell     |
| Kotlin       | Python      | Elixir      |
| CSS          | PHP         | Hibernate   |
| Sass         | Twig        | SQL         |
| LESS         | Blade       | Markdown    |
| Stylus       | C           | Bash        |
| HTML         | C++         | HOCON       |
| Haml         | C#          | Apache      |
| XML          | ASP         | Gitignore   |
| Jade/Pug     | Objective C | Lua         |
| JavaScript   | Swift       | Perl        |
| TypeScript   | Go          | Slim        |
| CoffeeScript | ERB         | Velocity    |
| Ini          | EJS         | Rust        |
| Regex        | Rdoc        | HTTP Client |

----------
## Color Palette

These are relevant only for _Material Themes_ (hover to see the hex value):

<span style="float:none">Dark variant</span>
<span style="float:right">Light variant</span>

{% for color in site.data.colors %}
{% include color.html color=color %}
{% endfor %}
