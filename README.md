# Placeholder for a Metalsmith plugin

## Description

A [*Metalsmith*](http://www.metalsmith.io/) plugin used for converting common data serialization formats (json, yaml, xml, etc) as well as moving or renaming said files.


## Purpose 

One of *Metalsmiths* pros is also one of its cons (at least in my book), and thats the significant amount of plugins out there for it. At this time, I found [**483** indexed ](https://www.npmjs.com/search?q=metalsmith), [**877** in Github](https://github.com/search?utf8=%E2%9C%93&q=metalsmith) (Well, now **87_8_**), and even [**198** on Metalsmiths homepage](http://www.metalsmith.io/#the-community-plugins). I've always thought *"The more plugins, the better!"*, but thats only provided that the plugins themselves are powerful enough that they aren't *just barely* out of reach of the ability desired or required by developers on other projects, which seems to be the case for a large amount of these plugins.

For example, one plugin that could:

 1. **Convert** various file formats
 2. Manage file/folder names/locations by:
  * **Moving** files/folders
  * **Delete** files/folders (probably by setting the `destination` to something *falsey*)
  * **Rename** files/folders 
  * **Create** files/folders, either empty or maybe redirect output to them or something fancy
 
 3. Allow the `source` and `destination` values to be specified either...
  * **Statically** - With simple string values to represent absolute or relative file/folder paths; or... 
  * **Dynamically** - Such as using *variables*, *wildcards*, *regex* patterns, or even the result of executing some provided JS (either a function in the *build.js* script or potentially the result of `eval`'d JS code in the `metalsmith.json` file)

  Would easily be able to replace up to _**14** existing plugins_ (which are listed on the metalsmith homepage, meaning they're basically suggested by the Metalsmith developers), all of which are listed below:

### Succeedable Metalsmith Plugins

[metalsmith-to-json](https://github.com/hellotoby/metalsmith-to-json)
[metalsmith-writemetadata](https://github.com/Waxolunist/metalsmith-writemetadata)
[metalsmith-renamer](https://github.com/alex-ketch/metalsmith-renamer)
[metalsmith-paths](https://github.com/ahmadnassri/metalsmith-paths)
[metalsmith-packagejson](https://www.npmjs.com/package/metalsmith-packagejson)
[metalsmith-move-up](https://github.com/mcdonnelldean/metalsmith-move-up)
[metalsmith-move-remove](https://github.com/carlnordenfelt/metalsmith-move-remove)
[metalsmith-json-to-files](https://github.com/woodyrew/metalsmith-json-to-files)
[metalsmith-jekyll-dates](https://github.com/fortes/metalsmith-jekyll-dates)
[metalsmith-transform](https://github.com/yeojz/metalsmith-transform)
[metalsmith-elevate](https://github.com/tylersticka/metalsmith-elevate)
[metalsmith-date-in-filename](https://github.com/sanx/metalsmith-date-in-filename)
[metalsmith-concat-convention](https://github.com/RobLoach/metalsmith-concat-convention) **(Maybe)**
[metalsmith-copy](https://github.com/mattwidmann/metalsmith-copy)


## P.S.

I'm not developing this plugin in an attempt to boot anyone off of any imaginary *Metalsmith plugin throne*, 