# Trainz Config for NotepadPlusPlus
This is a Notepad++ syntax highlighter for Trainz config files, based on a comprehensive list of config.txt tags and constants. As of creating the first version, I've researched an additional 235 items in addition to the index [disclosed on Trainz Wiki](https://online.ts2009.com/mediaWiki/index.php/Index_of_Tags_%26_Containers). Still you may run into unrecognized items. In this case, feel free to either open an issue, or edit the XML file yourself, and submit your changes.

# How to Install and Use
Pretty simple:
1. Grab the latest release from this page. 
   + If you download an XML file, save it to a location you remember.
   + If you download a ZIP file, extract `Trainz Config Syntax.xml` from the archive, and save it to a location you remember.
3. Open Notepad++, and click **Language > User Defined Language > Define your language**.
4. Click **Import**, browse for the file you downloaded or extracted, and proceed.
5. You may need to restart Notepad++ for the changes to take effect.

## My files are not colored! What's wrong?
+ After importing the syntax definition, you may need to restart Notepad++ for the changes to take effect.
+ Click **Language > Trainz Config.txt Files** to turn it on manually.

If it still does not work, open an issue here and we'll see if we can do anything.

## Can I use it for other files?
Yes. 
+ By default it is turned on for _config.txt_ and _\*.config.txt_ files. It means if you have config templates and name them like `my-superb-template.config.txt`, they will automatically be recognized.
+ If you want to turn it on for other filename extensions or patterns, click **Language > User Defined Language > Define your language** and add your extensions in **Ext**. Make sure you use space as the separator.

## Can I use it for other software?
Well, I'm not sure. AFAIK, this special solution for syntax highlighting is specific to Notepad++. However if you use Visual Studio Code or any other editor that supports the [TextMate Grammar](https://manual.macromates.com/en/language_grammars), you should definitely check out [Dangoo's Trainz Config project](https://github.com/Dangoo/trainz_config).

# Assets and Syntax
[Notepad++](https://notepad-plus-plus.org/) uses its own mechanism for syntax highlighting. You can learn more about it by clicking **Language > User Defined Language > Define your language** in Notepad++, and you'll get a link to its help.

## Colors and Categories
The following rules are in place:
+ Level 1 containers are dark red and have a highlight so that you can find them quickly.
+ Level 1 tags (those which only have a single value) have the same color, but no highlight.
+ Level 2+ containers are blue and have a highlight so that you can find them quickly.
+ Level 2+ tags (those which only have a single value) are dark blue, and no highlight.

This lets you easily recognize top-level and lower-level items, as well as if you used a tag at the proper level. If you see a blue tag outside of a container, you probably made a mistake, for example.

Go on:
+ KUIDs have a dark red color to make them outstanding. They are usually important. :)
+ Numbers and vectors (of numbers) are green.
+ Strings are purple.
+ IDs, like mesh names or identifiers you assign to elements in your kuid table appear dark blue, just like level 2+ tags, so your screen won't be as colorful as a rainbow.
+ Obsolete tags show up in gray.

And, you can expand and collapse containers so that you can overview the important parts of your large config files more easily.

# Licensing and other stuff
This project uses the MIT license.

If you think something is missing from this documentation, open an issue and tell me what it is.
