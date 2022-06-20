
**GINQO QlikSense Thumbnail generator** is a bookmarklet to take screenshot of your QlikSense app in proper size ratio and download it into JPEG.
It depends on the [dom-to-image](https://github.com/tsayen/dom-to-image) Javascript library by Anatolii Saienko, Paul Bakaus (original idea) that is hardcoded in the script. It generates an image from the QlikSense app sheet in Base64 format with javascript without create external calls to any server or anything on every modern browser.




**About bookmarklet**

A [bookmarklet](https://en.wikipedia.org/wiki/Bookmarklet) is like a bookmark, but instead of loading a specific page, it injects JavaScript into the current page in your browser for added functionality. 





**Installation** 

Installation of this bookmarklet is performed by creating a new bookmark, and pasting the bookmarklet.js code above into the URL destination field. 
Or go to [https://ginqo.com/thumbnail](https://ginqo.com/thumbnail) and drag the button to your bookmarks bar.


**Note**  
-   Before installing a Bookmarklet, make sure your browser’s bookmarks toolbar is visible.
-   To remove a Bookmarklet, simply right click on it and hit delete.
-   The bookmarklet code (bookmarklet.js) was simplifed from source.js using https://www.digitalocean.com/community/tools/minify and converted to bookmarklet using https://caiorss.github.io/bookmarklet-maker/

**How to use**
-   Open a QlikSense app sheet whether its on QlikCloud or on-premise
-   Click on the "Thumbnail Generator" bookmarklet
-   It will temporarily resize your sheet content dimension with the optimal aspect ratio of a thumbnail 8:5 then automatically takes screenshot of it
-   The screenshot jpg  file should be ready and automatically be downloaded within a few seconds

**Known limitations**
-   Works on Chrome, Edge and Firefox. Internet Explorer and Safari are not supported.
-   Due of the browser CORS policy, it might not be able to take screenshot of sheet that contains some complex visualization [https://github.com/tsayen/dom-to-image/issues/205](Issue #205)


**v.1.0 (2022-06-20)**
-   Initial release
