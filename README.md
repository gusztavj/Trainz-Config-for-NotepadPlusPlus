# Syntax highlight and autocomplete support in Notepad++ for Trainz Config files
This is a Notepad++ syntax highlighter for Trainz config files, based on a comprehensive list of config.txt tags and constants. As of creating the first version, I've researched an additional 235 items in addition to the index [disclosed on Trainz Wiki](https://online.ts2009.com/mediaWiki/index.php/Index_of_Tags_%26_Containers). Still you may run into unrecognized items. In this case, feel free to either open an issue, or edit the XML file yourself, and submit your changes.


## Features
### Syntax highlighting 
Colors the contents of Trainz `config.txt` [according to their purposes or meaning](#colors-and-categories).

![Syntax Highlighting](https://user-images.githubusercontent.com/12009110/120111811-ac3cd600-c173-11eb-996b-6960e20609c4.png)

### Autocomplete
Notepad++ will display a pop-up list of keywords matching the characters you typed. This makes it easier for you to find keywords you don't remember exactly.

![Autocomplete](https://user-images.githubusercontent.com/12009110/120111824-b3fc7a80-c173-11eb-86f8-033dc91679a0.png)

### Explanation and parameter info
Once you typed or selected a supported keyword, type a bracket to display a so-called calltip, which will show a short summary of the keyword, the type of data to supply and, in some cases, will show a link to the Trainz Wiki for more information.

![Calltip](https://user-images.githubusercontent.com/12009110/120111819-b068f380-c173-11eb-9033-7c3ab82e6466.png)

Be aware of the [multipart-keyword issue](https://github.com/gusztavj/Trainz-Config-for-NotepadPlusPlus/issues/1), for which you won't currently receive calltips for keywords containing one or more dashes (such as `category-keyword`), or wrong calltip is displayed.

### Template support
The syntax highlighter recognizes not only `config.txt` files, but files with `.trainz-acs` extension, too to let you create `config.txt` templates under different names. Since Notepad++ only considers the last extension part of files with multipart extensions, it cannot employ the highlighter for files with a name pattern of `something.config.txt`. To circumvent this, I added this extension, and you only need to add this extension to your config.txt templates.

# How to Install and Use
Pretty simple:
1. Grab the latest release from this page. 
   + If you download an XML file, save it to a location you remember.
   + If you download a ZIP file, extract `Trainz Config Syntax.xml` from the archive, and save it to a location you remember.
1. Copy `Trainz Config Syntax.xml` to `%APPDATA%\Notepad++\userDefineLangs\`
1. Copy `Trainz Config Files.xml` to `<Notepad++ Installation Folder>\autoCompletion\`. That is, if Notepad++ is installed to `c:\Program Files (x86)\Notepad++`, copy the file to `c:\Program Files (x86)\Notepad++\autoCompletion`.
1. Restart Notepad++ for the changes to take effect.

If you don't want Notepad++ to offer keywords, delete `Trainz Config Files.xml` and restart Nodepad++.

Installation is successful if you open a `config.txt` file or a file with `.trainz-acs` extension, and the text is colored. If it is not, first check if you can see `Trainz Config Files` in the `Language` menu. If you can, you are okay. If you cannot, open an issue.


## My files are not colored! What's wrong?
After installation, you may need to restart Notepad++ for the changes to take effect. If it still does not work, open an issue here and we'll see if we can do anything.

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
+ Level 1 containers are dark red and have a highlight so that you can find them quickly. You can expand/collapse these containers.
+ Level 1 tags (those which only have a single value) have the same color, but no highlight.
+ Level 2+ containers are blue and have a highlight so that you can find them quickly. You can expand/collapse these containers.
+ Level 2+ tags (those which only have a single value) are dark blue, and no highlight.

This lets you easily recognize top-level and lower-level items, as well as if you used a tag at the proper level. If you see a blue tag outside of a container, you probably made a mistake, for example.

Furthermore:
+ KUIDs have a dark purple color to make them outstanding. They are usually important. :)
+ Numbers and vectors (of numbers) are green.
+ Strings are purple.
+ Obsolete tags show up in gray.

And, you can expand and collapse containers so that you can overview the important parts of your large config files more easily.

# Licensing and other stuff
This project uses the MIT license.

If you think something is missing from this documentation, open an issue and tell me what it is.
