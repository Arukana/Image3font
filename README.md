# Image3font
A image's converter to font written in Fontforge/FontTools's [Hy](https://github.com/hylang/hy) language.

[![travis-badge][]][travis] [![license-badge][]][license]

[travis-badge]: https://travis-ci.org/adjivas/Image3font.svg?branch=master&style=flat
[travis]: https://travis-ci.org/adjivas/Image3font
[license-badge]: http://img.shields.io/badge/license-GPLv3-blue.svg?style=flat-square
[license]: https://github.com/limaconoob/Image2font/blob/master/LICENSE

### Usage
See command help:
```
usage: image3font [-h] [-v] [-m MANIFEST]

Create color fonts from a set of glyphes.

optional arguments:
* -h, --help            show this help message and exit
* -v, --version         show the version and exit
* -m MANIFEST, --manifest MANIFEST specify the manifest
```

### Manifest
The image3font.toml file for each font is called its manifest. Every manifest file consists of two fields and two sections.

* *path* field (optional)
* *source* field (default = "src")
*source* field can be used to configure the SVG's directory, 
#### [fontforge] section
* *path* field.
* *fontname* field - name contained in the postscript FontName field.
* *familyname* field (default = "fontname") - name contained in the postscript FamilyName field. If not specified this will be inferred as *fontname*.
* *fullname* field (default = "fontname") - name contained in the postscript FullName field. If not specified this will be inferred as *fontname*.
* *weight* field (optional) - name contained in the postscript Weight field.
* *copyright* field (optional) - name contained in the postscript Notice field.
* *version* field (optional)
* *encoding* field (default = "UnicodeFull")
* *em* field (default = 2028)
#### [fonttools] section
* *copyright* - copyright string from the font vendor. © Copyright the Monotype Corporation plc, 1990
* *familyname* - name the user sees. Times New Roman
* *subfamilyname* - name of the style. Bold
* *unique_id* - A unique identifier that applications can store to identify the font being used. Monotype: Times New Roman Bold:1990
* *full_name* - complete, unique, human readable name of the font. This name is used by Windows. Times New Roman Bold
* *version* - Release and version information from the font vendor. Version 1.00 June 1, 1990, initial release
* *postscript_name* - name the font will be known by on a PostScript printer. TimesNewRoman-Bold
* *trademark* - Trademark string. Times New Roman is a registered trademark of the Monotype Corporation.
* *manufacturer* - Manufacturer. Monotype Corporation plc
* *designer* - Designer. Stanley Morison
* *description* - Description. Designed in 1932 for the Times of London newspaper. Excellent readability and a narrow overall width, allowing more words per line than most fonts.
* *url_vendor* - URL of Vendor. http://www.monotype.com
* *url_designer* - URL of Designer. http://www.monotype.com
* *license* - License Description. This font may be installed on all of your machines and printers, but you may not sell or give these fonts to anyone else.
* *url_license* - License Info URL. http://www.monotype.com/license
* *reserved* - Reserved.
* *preferred_familyname* - Preferred Family. No name string present, since it is the same as name ID 1 (Font Family name).
* *preferred_subfamilyname* - Preferred Subfamily. No name string present, since it is the same as name ID 2 (Font Subfamily name).
* *compatible_full* - Compatible Full (Macintosh only). No name string present, since it is the same as name ID 4 (Full name).
* *sample_text* - Sample text. quick brown fox jumps over the lazy dog.
* *postscript_cid* - PostScript CID findfont name. No name string present. Thus, the PostScript Name defined by name ID 6 should be used with the “findfont” invocation for locating the font in the context of a PostScript interpreter.
* *wws_familyname* - WWS family name: Since Times New Roman is a WWS font, this field does not need to be specified. If the font contained styles such as “caption”, “display”, “handwriting”, etc, that would be noted here.
* *wws_subfamilyname* - WWS subfamily name: Since Times New Roman is a WWS font, this field does not need to be specified.
* *light_background* - Light background palette name. No name string present, since this is not a color font.
* *dark_background* - Dark background palette name. No name string present, since this is not a color font.
* *variations_postscript* - Variations PostScript name prefix. No name string present, since this is not a variable font.

### License
**image3font**'s code in this repo uses the [GNU GPL v3](http://www.gnu.org/licenses/gpl-3.0.html) [license](https://raw.githubusercontent.com/adjivas/Image3font/master/LICENSE).

#### Dependencies
Many thanks goes to **command/etc**'s project:
* [FontForge](https://github.com/fontforge/fontforge)
* [FontTools](https://github.com/fonttools/fonttools)
* [Wand](https://github.com/dahlia/wand)
* [Wikipedia (for the picture **neko**!)](https://en.wikipedia.org/wiki/Catgirl)
