SimpleRounded-HTMLexport
========================

This is a kipi-html-export theme that uses flat shapes with rounded corners.

Preview
-------
There is a sample gallery at: http://enaut.github.com/Kipi-SimpleRounded-HTMLexport/

A Screenshot of a resulting gallery:

![Preview Gallery](https://raw.github.com/enaut/Kipi-SimpleRounded-HTMLexport/master/SimpleRounded/previewBig.png)

Install
-------
To use this theme you must install the kipi-plugins in your image software. I tested and used this theme with [Digikam](http://www.digikam.org/) which is a pretty impressive open source image management software.

To install copy the `SimpleRounded` directory to:
```
    ~/.kde/share/apps/kipiplugin_htmlexport/themes/
```
If that does not exist create it using:
```
    mkdir -p ~/.kde/share/apps/kipiplugin_htmlexport/themes/
```
You might have to restart the kipiplugin-capable application before the Gallery shows up.

If it does not show up look for your distribution specific path of the kipi plugins.

Features
--------
  * boxes with rounded corners - but without images.
  * pretty compatible with a lot of browsers (not IE < 5.5)
  * xhtml strict compatible
  * multipage support - if the collection is bigger than a configurable limit then it will create a new page and a navigation. (for the collection thumb page as well as the collections list page)
  * already a lot of the options user configurable.

Advanced Stuff
--------------
### Alternate installation
If You want to install the theme for all users just as the native themes just copy the `SimpleRounded` directory to:
```
/usr/share/kde4/apps/kipiplugin_htmlexport/themes/
```

### Manual invocation
Since the HTML-export is just an invocation of a .xslt file you can do this manually.
This is especially good if you want to regenerate the html files without resizing all the images over and over again
or if you want to translate some strings differently (at least the german translation is somewhat ugly).
```
xsltproc -o index.html --stringparam i18nOriginalImage Original --stringparam i18nNext next --stringparam i18nPrevious previous --stringparam i18nCollectionList collection --stringparam titlebar Titel --param background "'#AAA'" --param thumbBorderColor "'#00F'" --param urlColor "'#F00'" --param content-bgc "'#0F0'" --param listBackground "'#FF0'" --param navigationColor "'#855'" --param thumbnailsPerPage "'15'" --stringparam homepage SimpleRounded --stringparam homepageUrl https://github.com/enaut/SimpleRounded-HTMLexport ~/.kde/share/apps/kipiplugin_htmlexport/themes/SimpleRounded/template.xsl gallery.xml
```
You will have to make some adjustments of the colors and Strings!

If you have any Questions on how to use this or how to extend this theme feel free to file an issue in the [issue-tracker](https://github.com/enaut/SimpleRounded-HTMLexport/issues) or contact me via email.

Have fun!
