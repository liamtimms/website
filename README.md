# Liam's Personal Website

The site is generated by using a simple `bash` script (`sssb`). The contents of the site are mine but you can modifiy this for your own use by writing your own content in the "site" directory and "index.md." The style should be modified using "default.css." The following explains the use of the script in more detail:

## Simple Static Site Builder

The `sssb` bash script is an Simple Static Site Builder that converts Markdown pages to HTML, minifies the HTML, and copies over other non-markdown files to a destination directory. It uses Pandoc to convert the Markdown pages and sed to minify.

### Usage

To use this script, place it in the root directory of your website project and run it with ./sssb. The script will move the the existing `.www` directory (if it exists) to the trash, create a new .www directory, minify the default.css file in the site/templates directory, and iterate over all files in the site directory, converting Markdown files to HTML and copying over other files. The generated website will be placed in the .www directory.

### Configuration

The script uses the "default.html" and "default.css" files in the site/templates directory as templates for the generated HTML pages and the CSS styles, respectively. You can modify these files to customize the appearance of the generated website.

The script also uses `sed` to minify the CSS file by removing unnecessary space. You can modify the sed command in the script to customize the minification process or disable it altogether.

### Dependencies

This script requires the following dependencies to be installed on your system:

- [Pandoc](https://pandoc.org/)
- [trash-cli](https://github.com/andreafrancia/trash-cli)
- sed (part of GNU core utils should be there by default)

### License

This script is licensed under the MIT License. See the LICENSE file for more information. The method is a modified version of one originally written by [dylanaraps](https://github.com/dylanaraps) under the MIT License. The source is long dead and had minimal documentation but was extremely useful at the time.

The CSS includes a site background I made using [svgbackgrounds](https://www.svgbackgrounds.com/#flat-mountains) under CC BY 4.0.

_These liscense cover the styles and script but do not apply to the site's content or pages on my website not generated with this method. Please erase existing page contents for your own use._
