# OpenStreetMap Promotional Leaflets

![photo](https://raw.github.com/alexkemp9/openstreetmap-promotional-leaflets/master/leaflets.jpg)

![photo](https://raw.github.com/alexkemp9/openstreetmap-promotional-leaflets/master/leaflets2.jpg)

This repository contains the source files for an OSM flyer (in English) that was
originally created by Frederik Ramm <frederik@remote.org> and
contributors from the talk-de list in January 2008, and subsequently
updated, translated, re-updated and re-translated over the
years. This version was made by Andy Allan <andy@gravitystorm.co.uk>

All contents are in the public domain except for those derived from OSM
which are CC BY-SA, and except for non-OSM logos.

The flyer is designed for DIN A7 as the final size (105mm high and
74mm wide), with 8 pages in a zig-zag ("Leporello") fold, and full
colour printing. 

The flyer was made with Inkscape; osmflyer1.pdf and osmflyer2.pdf
are the front and reverse side.

## *HowTo print*:

See https://www.openstreetmap.org/user/alexkemp/diary/47536

## *Directories*:

***Inkscape-r15371***: The most recent SVG/PDF files have been updated under Inkscape v0.92.1 r15371    
***Inkscape-r9886***: The original SVG files were created under Inkscape v0.48.3.1 r9886     

## *Files*:

***PDFs***: page size: A7 Portrait; 105mm high x 296mm wide; 3mm bleed    
***./osmflyer.pdf***: r15371 combo of osmflyer1.pdf + osmflyer2.pdf    
***SVGs***: Inkscape stores it’s work within SVG v1.2 files; those files are NOT web-compatible    
***README.md***:  this text with Unix line-endings    
***README.txt***: this text with Windows line-endings

## *Fonts*:

***Ubuntu***: https://assets.ubuntu.com/v1/fad7939b-ubuntu-font-family-0.83.zip    
***Open Sans***: https://github.com/onitake/fonts-open-sans    
***Bitstream Vera Sans***: http://ftp.gnome.org/pub/GNOME/sources/ttf-bitstream-vera/1.10/

## *Program*:

***Inkscape***: https://inkscape.org/release/

## *Updates*:

- ***2018-12-30***: (AK) the main work was to update the r9886 SVGs for Inkscape r15371
(see https://www.openstreetmap.org/user/alexkemp/diary/47345).
- ***2019-01-30***: (AK) correcting padding errors discovered after printing the updated PDFs
+ added sub-dirs

Some notes in case you want to re-create something yourself:

* `berlin-background.png` is basically a 4-year-old Osmarender rendering
of Berlin, using a standard stylesheet but with all captions removed,
and the resulting PNG file processed with the Gimp roughly like this:

  First convert to grayscale, then use `colors->curves` to narrow down
contrast, then convert back to RGB, then use `colors->colorify` to give
it a nice hue.

* The cover globe image was made with Marble, the technique is roughly
outlined here: http://wiki.openstreetmap.org/wiki/Marble

* To generate the high-res png maps, use the following commands
`~/src/nik2img/nik2img.py -d 2479 1356 -z 14 -c -0.128056 51.508056 --scale-factor 3 ~/src/openstreetmap-carto/osm-carto.xml london.png`
`~/src/nik2img/nik2img.py -d 1974 2902 -z 15 -c -3.19864 55.95 --scale-factor 3 ~/src/openstreetmap-carto/osm-carto.xml edinburgh.png`