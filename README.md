# Metalsmith Data Utility

*First*.. before you say anything, *yes*, I realize the name **metalsmith-data-utility** is anything but descriptive. This is being created to easily accomplish a very specific *[set of tasks](https://github.com/geekwiki/metalsmith-data-util#purpose)*:

1. **Transpile** serialized data files (such as `json`, `xml` and `yaml`) to/from different formats
1. **Move** existing folders/files
1. **Delete** existing folders/files
1. **Rename** existing folders/files
1. **Create** new files with custom serialized data

And there will (more than likely) be other functionality added to later versions. I wanted to be able to add other such functionality without conflicting the name. 

That, and it was simple and available :-)

## Description

A [*Metalsmith*](http://www.metalsmith.io/) plugin used for converting common data serialization formats (json, yaml, xml, etc) as well as moving or renaming said files.


## Purpose 

One of *Metalsmiths* pros is also one of its cons (at least in my book), and thats the significant amount of plugins out there for it. At this time, I found [**483** indexed ](https://www.npmjs.com/search?q=metalsmith), [**877** in Github](https://github.com/search?utf8=%E2%9C%93&q=metalsmith) (Well, now *87***8**), and even [**198** on Metalsmiths homepage](http://www.metalsmith.io/#the-community-plugins). I've always thought *"The more plugins, the better!"*, but thats only provided that the plugins themselves are powerful enough that they aren't *just barely* out of reach of the ability desired or required by developers on other projects, which seems to be the case for a large amount of these plugins.

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

 1. [metalsmith-to-json](https://github.com/hellotoby/metalsmith-to-json)
 1. [metalsmith-writemetadata](https://github.com/Waxolunist/metalsmith-writemetadata)
 1. [metalsmith-renamer](https://github.com/alex-ketch/metalsmith-renamer)
 1. [metalsmith-paths](https://github.com/ahmadnassri/metalsmith-paths)
 1. [metalsmith-packagejson](https://www.npmjs.com/package/metalsmith-packagejson)
 1. [metalsmith-move-up](https://github.com/mcdonnelldean/metalsmith-move-up)
 1. [metalsmith-move-remove](https://github.com/carlnordenfelt/metalsmith-move-remove)
 1. [metalsmith-json-to-files](https://github.com/woodyrew/metalsmith-json-to-files)
 1. [metalsmith-jekyll-dates](https://github.com/fortes/metalsmith-jekyll-dates)
 1. [metalsmith-transform](https://github.com/yeojz/metalsmith-transform)
 1. [metalsmith-elevate](https://github.com/tylersticka/metalsmith-elevate)
 1. [metalsmith-date-in-filename](https://github.com/sanx/metalsmith-date-in-filename)
 1. [metalsmith-concat-convention](https://github.com/RobLoach/metalsmith-concat-convention) *<sub>(Maybe)</sub>*
 1. [metalsmith-copy](https://github.com/mattwidmann/metalsmith-copy)
 1. [metalsmith-filenames](https://github.com/MoOx/metalsmith-filenames)

## Project Stuff

### Details

 * It looks like the native [`RegExp`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp) class supports any of the requirements that may be needed (EG: *lookbehind*/*lookahead*), but I'll do some more digging/testing later to verify it's suitable.
 * Depending on what task the plugin is being used for, or what data format it's transpiling, the exact npm libraries being required may vary. Thus, it may be ideal to define the plugins *not* required for *any* of the tasks as the npm packages `[optionaldependencies](https://docs.npmjs.com/files/package.json#optionaldependencies)` (or any other better-suited method).

#### *Initial* Features

Since this is being created to accomplish some tasks needed by **[geekwiki/blog.git](https://github.com/geekwiki/blog)**, the initial deployment will have a limited amount of features, which will include:

 1. Adding the filename of the source file being processed to the metadata (similar to [*metalsmith-filenames*](https://github.com/MoOx/metalsmith-filenames))
 1. 

#### *Definite* Later Features


#### *Possible* Later Features

 1. Retrieve source data via cURL (Similar: [*metalsmith-remote-json-to-files*](https://github.com/okonet/metalsmith-remote-json-to-files))
 1. In addition to being able to convert data, being able to decode/encode/re-encode files from would be useful (Similar: [*metalsmith-transformer*](https://github.com/HolyMeekrob/metalsmith-transformer))
 1. Convert data to spreadsheets (EG: *csv*, *xls*, *xlsx*, etc). This would obviously require the data to be formatted properly, but may be useful
