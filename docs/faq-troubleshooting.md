---
layout: docs
title: Troubleshooting
group: troubleshooting
toc: true
comments: true

previous:
  url: '/docs/analytics'
  title: Analytics

next:
  url: '/docs/other-products'
  title: Other Products

---

Here you can find all the Troubleshooting FAQs.
{:class='title'}

## Settings

**Q**: **I've updated the IDE/plugin to a new version, and now I get an error about the plugin failing to initialize?**

**A**: It could come from multiple issues, but it could simply be a problem with the settings not being compatible to the new version.
In that case, simply make a copy of the settings file, then delete the original file, and restart the IDE.

If the issue is gone, simply go back to the settings and go back to your previous configuration manually.
If the issue persists, please report it in the Issues Section.

**Q**: **I've removed the plugin, and still the background image persists!**

**A**: This is an issue hard to resolve, because the *Custom Wallpaper* function is using the `Set Background image` function from the IDE behind the curtains.
Therefore, removing the plugin might not remove the set image completely.
If that occurs, you can remove the image by opening the Command Panel (<kbd>Cmd-Shift-A/Ctrl-Shift-A</kbd>)
and type `Set Background image` and then manually remove the image, or go into `Settings → Appearance → Background Image`.

**Q**: **What's that analytics option? What data are collected?**

**A**: This is an option to allow sending data to Material Theme servers about users' configuration, usage and trends.
These analytics will allow us to analyze what features are most used or least used,
in order to prioritize development of features, or maybe notify users about specific features, to provide better satisfaction.

These data are completely anonymous, and aren't shared/sold to any third parties.
If you want to stop sending data, simply turn off the option in the `material_theme.xml`.

**Q**: **My settings are lost/jumbled up!**

**A**: As the plugin evolves, sometimes settings are modified or removed, and as a result it can jumble your configuration files.
We're trying our best to limit such issues, but they can happen nonetheless.

If you find yourself being unable to use the plugin or even run the IDE, try to delete your configuration files,
or at least try to delete specific properties until the IDE launches again.

**Q**: **The wizard idea was great! But I've made a mistake, and the wizard won't show up anymore!**

**A**: The wizard will show only once and only when you don't have the `isWizardShown` option set to true in the config file.
But you can reopen it by simply clicking on the action from the Material Theme Toolbar, on the Features menu.

**Q**: **Where have all the icons gone?**

**A**:
Since 5.0.0, the icons related settings have been moved to the [Atom Material Icons plugin](https://plugins.jetbrains.com/plugin/10044-atom-material-icons),
another plugin developed by the Material Theme team.
This is in order to encourage developers to develop _Icon Themes_, as the plugin is now free of icons.

**Q**: **I've downloaded a theme from the Plugins Page, and now I'm seeing texts that aren't themed, or checkboxes that are wrongly colored, etc…**

**A**: This is because these are native themes, and such themes use the Theme API provided by JetBrains rather than the API used by the Material Themes.
Even though the plugin tries to convert it to its own format, it won't be as good as the originals.
Still, it should be as similar as possible, so there shouldn't be any critical issues.
In that case, please report to the repository's issues.

**Q**: **I've bought a license, but I am still identified as a Free User!**

**A**: That means that you haven't activated your license yet. At the moment, the only way to do it's to run the action to open the _Registration Modal_.

{% include figure.html content="/screens/activateLicense.png" caption="Activate License" %}

{% include figure.html content="/screens/license.png" caption="License" %}

**Important note**: Android Studio users, in order to activate the plugin (or any paid plugin),
you need to install a plugin first:<https://plugins.jetbrains.com/plugin/13407-jetbrains-marketplace-licensing-support>.

-----

## Tab settings

**Q**: Why limit the thickness or the tab height? I want to have 10 in thickness and 100 in tabs!!!

**A**: Because allowing values past these limits would make the UI ugly or worse, crash it.
If you have a good reason to want it anyway, you can open an issue on GitHub with why you would want that.
At most, you can still fork the plugin and tweak it to whatever you want.

**Q**: The uppercase tabs feature is so useless! Editor Tabs !== Material Design Tabs!

**A**: While I might agree with this statement, Personally, I think that this is a cool feature, and it doesn't bother me.
It isn't allowed by default, so new users won't be startled by it, and if you don't like it, you can simply turn it off.

----

## Panel settings

- Because the IDE is developed with compact table cells in mind, using "padded table cells" may result of displaying artifacts in some components.
  One example is the [*Python DataView*](https://github.com/ChrisRM/material-theme-jetbrains/issues/485).
  If you are using such features a lot, just enable the "Compact Table Cells" option to solve that problem.

----

## Component settings

- Scrollbar settings don't work well with HiDPI yet. For a better experience, please disable these options if you are in such environments.
- The scrollbar settings and color only affect the **UI Scrollbars**, as opposed to the **Editor Scrollbars**.
  Editor scrollbar's colors are managed by the color scheme, in the *Color Scheme → General → Vertical Scrollbars* section.

----

## Icons settings

- The Monochrome icons feature messes up some parts of the IDE, such as the SVG Image Viewer. If you need to use it, please disable the option temporarily.

----

## Project view settings

- Tree views' settings work in all tree views, even views such as "Project Structure" or "Remote Host"

----

## Custom themes

***Q**: Can I use more than one custom theme?

**A**: No, you can't.
But if you're confident with your theme, you can decide to publish your theme with the aforementioned properties,
so that it would be caught by the plugin, or save the XML file so that you can export it and use it wherever you want.

**Q**: Where are stored my custom theme colors?

**A**: You can find your custom colors inside the config directory, just like the Material settings.

**Q**: Why do I get a popup asking me for "resetting the theme colors" at start?

**A**: This popup is used to reset the custom theme colors to their default ones and is popping up when switching from
a dark theme to a light theme and vice-versa.
But sometimes, like when you install the plugin or reset your settings,
since it doesn't know what theme you came from, it will ask even though you didn't ask for it.
Simply press OK, and it won't bother you anymore.

**Q**: I changed the colors, but it doesn't look as good as the default themes.

**A**: Creating a theme isn't an easy task, and the Material ones are the result of a long-thought process about
which colors are best suited for a UI.
However, you can check out other famous Sublime/Atom/Visual Studio themes as an inspiration and start from it.

**Q**: OK I have an idea of a theme, but there aren't enough options in the settings for me to make it.

**A**: It's true that those settings are for color palettes of a few colors only, and regroup components of the
same purpose under the same color group.
But if you'd like to have a different color for checkboxes and radio buttons, or between lists and tables,
or set the tree color different as the main background color, etc. — for this the best option would be to
fork the project and create a brand-new theme.

**Q**: I set the color scheme via the Editor > Color Scheme options, but it resets every time I restart the IDE!

**A**: If you're using a _Custom Theme_, that might be due to the [Color Scheme option](/docs/configuration/custom-themes#color-scheme).
Make sure to specify the color scheme you want to use to this screen as well.

----

## Excluded file colors

**Q**: Is there a way to change the text color?

**A**: Another setting controls the color of the text. See [File Status Colors](/docs/configuration/file-status-colors) for more info.

----

## File status colors

Because this feature modifies the original `VCS File Colors` feature, please bear in mind the following issues:

- When switching to another scheme that doesn't define file status colors, some defaults will be applied, which aren't the defaults provided by
  Darcula/IntelliJ,
  and therefore look bad.
- Uninstalling/Disabling the plugin won't revert these settings, so you will still keep the last file colors even after restarting.

Thankfully there is an easy fix for that: in the `VCS File Colors` there is a button _Reset Default_ that will
revert the value back to the Darcula/IntelliJ default.
**Please note, however, that as soon as you change a color scheme, the values will change back again.**

-----

## Scrollbars

**Q**: **I've set the `Accent Scrollbars` setting off, but my scrollbar is still blue/orange/whatever!**

**A**: The `Accent Scrollbars` and `Transparent Scrollbars` feature control the appearance of the IDE Scrollbars, not the editor scrollbars.
For the editor scrollbars, the only way to do so is to use the _Scrollbars_' Color Scheme Panel.

**Q**: **I've uninstalled the theme, but the scrollbar colors persist!**

**A**: Since these colors are part of the color scheme, removing the plugin wouldn't revert them back, just like with
the [File Status Colors](/docs/configuration/file-status-colors).
The only way to do so would be to restore the color scheme.


----

## License activation

**Q**: I've bought a license, but I am still identified as a Free User!

**A**: That means that you haven't activated your license yet. At the moment, the only way to do it would be to run the action to open the _Registration Modal_.

{% include figure.html content="/screens/activateLicense.png" caption="Activate License" %}

{% include figure.html content="/screens/license.png" caption="License" %}

**Important note**: Android Studio users, in order to activate the plugin (or any paid plugin), you need to install a plugin
first: <https://plugins.jetbrains.com/plugin/13407-jetbrains-marketplace-licensing-support>.
