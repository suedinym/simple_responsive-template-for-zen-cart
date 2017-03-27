#  Zen Cart Your Package Name
Version:       1.0,0
Designed For:  Zen Cart v1.5.5e
Created on 03/20/2017 by Susan Jensen

Released under the General Public License <http://www.gnu.org/licenses/gpl.txt> 
// Skeleton framework V2.0.4 is Copyright 2014, Dave Gamache
// Free to use under the MIT license.
// http://www.opensource.org/licenses/mit-license.php
// For details on how Skeleton works, visit www.getskeleton.com

## FEATURES

- Easy Installation
- Mostly vanilla CSS
- No changes to core files. It lives entirely within the override system.
- No changes to your template. The installation procedure creates a new template which you can turn on or off.
- Easily customizable, with 'try-it' files so you can see what the effect of changes before applying them to your site
- Small footprint: only uses about 265 kb additional disk space when uploaded.
- Cross browser compatible with Firefox, Chrome, Opera, and Android, and should work on other browsers, as there are no CSS transitions or annimations, but may have large degradation prior to IE9.

This module is a basic add-on for Zen Cart 1.5.5e, and has only been tested with that version. It was developed using a local copy and a virtual host with PHP 7.0.15 (for Ubuntu Linux). It was not tested on earlier versions, but should work on other Zen cart & PHP versions as well.

This add-on was created in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

### WHAT DOES THIS ADD-ON DO?

This add-on template allows people who are still using the basic Classic template, and have modified little beyond the images and CSS to make their site responsive.

### WHAT'S IN THE DOWNLOAD?

```
├── README.md
├── license.txt
├── readme-HTML
│   ├── index.html
│   └── try_it
│       ├── images
│       |── tryit.html
│       └── tryit-css
│           ├── style-a-skeleton.css
│           ├── stylesheet.css
│           └── stylesheet_mq.css
└── simple_responsive
    └── includes
        ├── extra_datafiles
        │   └── simple_responsive_column_widths.php
        └── templates
            └── simple_responsive
               ├── common
               │   └── tpl_main_page.php
               ├── css
               │   ├── style-a-skeleton.css
               │   └── stylesheet_mq.css
               └── template_info.php
```

- This text-only README.md (markdown) file.
- A detailed readme HTML file with links to additional information, including videos.
- An HTML 'try it' package (with links, etc, disabled) so you can see approximately how this add-on should work on your site before installing it.
- The actual add-on files!

##  TRY-IT DEMO 

The 'try it' demo is a basic html page (with links, etc, disabled) which you can open in your browser and can check out approximately how this add-on should work on your site before installing it. 

You can also modify the following files with your favorite code editor:
- tryit.html
- stylesheet_mq.css

### try-it.html

Open this file in your browser, then resize it by grabbing the side of the browser window with your cursor, and change the width, making it as thin as the browser will let you. You should see a lot of changes happen when it's almost as thin as it will get. This approximates what the site would look like on a mobile device. 

If you open tryit.html in your editor, leaving word wrap off, you will see some very long blocks of code along with this code:

```
<!-- BEGINNING OF LEFT COLUMN -->
<div class="columnLeft three columns "> 

<!-- BEGINNING OF CENTER COLUMN -->
<div class="six columns">

<!-- BEGINNING OF RIGHT COLUMN	 -->
<div class="columnRight three columns">

```

You can change the width of all three columns. 

Basically the total width all of the columns should add up to twelve columns. For instance - if you set the center column at six columns, each side can be three columns wide. 

Or, if you have your store set up with only one side column, and the center column is eight columns, the remaining side should be four columns. (Note: one column is not plural, and widths can also be set at one-third and two-thirds columns.)

If there is only a center column, it should be set at twelve columns.

You can find more information about the Skeleton grid at: <http://getskeleton.com/#grid>

### stylesheet_mq.css
This stylesheet rearranges and resizes parts of the the logo and header sections. It also makes the left and right columns disappear in the mobile layout. The Skeleton framework slides the columns on top of each other, starting with the left column, so it's best to hide the left column for mobile layouts. 

If you wish to show the right column, delete .columnRight and the comma before it.

- The best way to make modifications to your template, etc, is to try it in a local host before uploading it to your live online site, but that is beyond the scope of this tutorial. For information on how to set up a local copy:<https://www.zen-cart.com/wiki/index.php/Making_a_Local_Copy> 

## INSTALLATION 

All files are arranged in the correct Zen Cart version structure.

```
└── includes
    ├── extra_datafiles
    │   └── simple_responsive_column_widths.php
    └── templates
        └── simple_responsive
            ├── common
            │   └── tpl_main_page.php
            ├── css
            │   ├── style-a-skeleton.css
            │   └── stylesheet_mq.css
            └── template_info.php

```

### BACKUP YOUR SITE!

-----BACK-UP YOUR FILES AND DATABASE BEFORE INSTALLING------
Always backup your shop and database before making changes.

Not only is it a really good idea to make a backup, you will also be copying some of your files to the add-folders.

### EXTRACT ZIPS

Unzip/extract the zip file to a convenient folder on your computer.

You should now have two zip files:

1. Your site backup
2. The add-on download

After this step, you should see both the zip file and the extracted folders in your directory.

```
├── backup.zip
├── extracted backup folder
├── add-on.zip
└── extracted add-on folder
```

### PREPARE ADD-ON FILES

This tutorial assumes that you are still using the basic Classic template, and have only modified the images and CSS.

Instead of copying the files from the add-on into YOUR_TEMPLATE, you will be making a new template (simple_responsive), by adding YOUR_TEMPLATE's customized files to the add-on files folders.

By doing it this way, instead of having to 'uninstall' the add-on if you're not fond of the result, all you have to do is return to YOUR_TEMPLATE using the admin tools.

Copy your CSS files and images from the backup, either from the Classic Template, or your Custom template into the corresponding folders in the add-on.

└── includes
    ├── extra_datafiles
    │   └── simple_responsive_column_widths.php
    └── templates
       └── simple_responsive
            ├── common
            │   └── tpl_main_page.php
            ├── css
            │   ├── YOUR_TEMPLATE.css
            │   ├── style-a-skeleton.css
            │   └── stylesheet_mq.css
            ├── images
            │   ├── YOUR_TEMPLATE_logo.jpg
            │   └── YOUR_TEMPLATE_header_bg.jpg
            └── template_info.php

(If you have gone further and placed Custom template files in other locations, you know where they are, and should know how to add them to this template.)

### CUSTOMIZE

Most modifications should ONLY be made in:
simple_responsive_column_widths.php

Open simple_responsive_column_widths.php with your favorite code editor. There are three lines of code: 

- `DEFINE('COLUMN_WIDTH_CENTER', 'six columns');`
- `DEFINE('COLUMN_WIDTH_LEFT', 'three columns');`
- `DEFINE('COLUMN_WIDTH_RIGHT', 'three columns');`

If you modified the column widths in the 'tryit' example, this is the file you use to make the same changes for your actual site.

If you have used media queries before, and understand how they work, you may also want to modify:
- stylesheet_mq.css

OR
If you mofified it in the 'try-it' folder, you can copy and paste the stylesheet_mq.css to your simple_responsive template folder.
(Otherwise, don't modify it!)

- You can rename the simple_responsive template folder at this point if you like.

DON'T CHANGE: 

- style-a-skeleton.css 
- template_info.php
- tpl_main_page.php*

### CODING

*If you have made changes to tpl_main_page.php in YOUR_TEMPLATE, you should compare your tpl_main_page.php with the one in simple_responsive using a tool like Diffuse Merge Tool http://diffuse.sourceforge.net/ 

*If you have added additonal pages that rely on tpl_main_page.php, you should also compare those with Diffuse, and modify them as necessary


### UPLOAD

Upload the files to your Zen Cart shop directory,  via FTP or cPanel, maintaining their file structure.

```
└── simple_responsive
    └── includes
       ├── extra_datafiles
       │   └── simple_responsive_column_widths.php
       └── templates
        └── simple_responsive
                ├── common
                │   └── tpl_main_page.php
                ├── css
                │   ├── style-a-skeleton.css
                │   └── stylesheet_mq.css
                ├── images
                │   └── scr_template_default.jpg
                └── template_info.php
```

NOTE! You should already be loading jquery.min.js as it is included in the html header file, so even if it in any part of this (or any other) add-on, DO NOT add it again!

##  BUGS 

There are currently no known bugs/ these known bugs.

### Contributing 
If you see a bug and know how to fix it, please make a pull request at


## SUPPORT 
Please direct support questions:
- On the zen-cart add-on thread at: <http://getskeleton.com>
- Or at github: <http://getskeleton.com>

### UNINSTALL
This add-on lives entirely in the override system, so there is no need to remove it. Simply switch back to your custom template using the admin panel.

But if you wish to uninstall completely, remove all simple_responsive files and restore your backup files.
Remove all files in the plugin package.

Restore your backup for includes/templates/YOUR_TEMPLATE/common/tpl_main_page.php.

Restore your includes/templaes/YOUR_TEMPLATE/css/index_home.css file.

### HISTORY
Modified(00/07/2017): http://www.suedinym.com
-  00/00/17  - Initial Release


## CREDITS 

### The Actual Add-on

Full credit for the 'bones' of the responsive grid goes to [Dave Gamache](https://twitter.com/dhg), who created Skeleton for a better web. All Sue Jensen did was extract those 'bones', figure out a way to add them to Zen Cart's Classic template, and tweak a few Zen Cart bits and pieces with media queries.

### The Add-on HTML Tutorial
 
The code sections of the HTML tutorial were converted at http://www.freebits.co.uk/convert-html-code-to-text.html.

Tree diagrams were extracted from directories using Tree for Linux. HTML representations were styled using the [tree structure tutorial] at (https://two-wrongs.com/draw-a-tree-structure-with-only-css).

If you find this mod useful, please consider making a donation to the Zen Cart project - http://www.zen-cart.com/content.php?6-donate



