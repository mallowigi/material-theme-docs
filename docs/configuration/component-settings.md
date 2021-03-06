---
layout: docs
title: Component Settings
description: Further customize the IDE components
group: configuration
comments: true
toc: true

previous:
  url: '/docs/configuration/project-view-settings'
  title: Project View Settings
next:
  url: '/docs/configuration/features-settings'
  title: Features Settings
---

This page controls the components used throughout the IDE, like buttons, scrollbars, etc.
{:class='title'}

{% include carbonads.html %}

### Uppercase buttons

This setting sets the text of the buttons to be uppercase, just like the Material Design buttons. This is optimal for a
full-fledged Material Design Experience.

{% include figure.html content="/screens/uppercaseButtons.png" caption="Uppercase Buttons" %}

### Outline buttons

This feature is only available for premium users.
{:class='card-panel warn'}

Starting from version 6.2 this new setting replaces buttons with **outlined buttons**.

{% include figure.html content="/screens/outlinedButtons.png" caption="Outlined Buttons" %}

-----
### Transparent Scrollbars and Accent Scrollbars

This feature is available in the free plan.
{:class='card-panel warn'}

These options control the appearance of the scrollbars. Note: This feature works completely on Windows and Linux, but on
Mac it is only working for non-native scrollbars (i.e. scrollbars that appear only while scrolling).

*Transparent scrollbars* will add more transparency to the scrollbars and set it as the same color as the current
theme's background color. This is adding _50% opacity_ and there is no way to change it.

*Accent scrollbars* will replace the scrollbar color with the _current accent color_.

{% include figure.html content="/screens/scrollbars.png" caption="Accent Scrollbars" %}

#### Editor Scrollbars

This feature is available in the free plan.
{:class='card-panel warn'}

Since 2019.1 the scrollbars enter into two categories:
* _UI Scrollbars_: These are the scrollbars found throughout the UI (lists, trees and so on)
* _Editor Scrollbars_: These are the scrollbars inside editors

Thanks/Because of this separation, the aforementioned settings is now controlling only the _UI Scrollbars_. Instead, the
_Editor Scrollbars_ are managed via a [**Color Scheme Setting Page**](/docs/configuration/scrollbars.md#important-information).

---
### Tabs Shadow

This feature is only available for premium users.
{:class='card-panel warn'}

This option enables/disables the shadow under the tabs.

{% include figure.html content="/screens/tabShadow.png" caption="Tabs Shadow" %}

---

### Inverted Selection Color

This feature is available in the free plan.
{:class='card-panel warn'}

This setting allows you to choose between two styles for the **selected option** in the *Autocomplete Panel*:

{% include figure.html content="/screens/normalSelection.png" caption="Normal selection" %}

{% include figure.html content="/screens/invertedSelection.png" caption="Inverted selection" %}

