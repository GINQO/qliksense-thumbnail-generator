
**GINQO QlikSense Thumbnail generator** is a bookmarklet to take screenshot of your QlikSense app in proper size ratio and download it into JPEG.
It depends on the [dom-to-image](https://github.com/tsayen/dom-to-image) Javascript library by Anatolii Saienko, Paul Bakaus (original idea) that is hardcoded in the script. It generates an image from the QlikSense sheet app in Base64 format with javascript without create external calls to any server or anything on every modern browser.




**About bookmarklet**

A [bookmarklet](https://en.wikipedia.org/wiki/Bookmarklet) is like a bookmark, but instead of loading a specific page, it injects JavaScript into the current page in your browser for added functionality. 





**Installation** 

Installation of this bookmarklet is performed by creating a new bookmark, and pasting the code below into  the URL destination field. Or go to [https://ginqo.com/thumbnail](https://ginqo.com/thumbnail) and drag the button to your bookmarks bar.

    javascript:(function()%7B!function(e)%7B"use strict"%3Bvar t%3Dfunction()%7Breturn%7Bescape%3Afunction(e)%7Breturn e.replace(%2F(%5B.*%2B%3F%5E%24%7B%7D()%7C%5C%5B%5C%5D%5C%2F%5C%5C%5D)%2Fg%2C"%5C%5C%241")%7D%2CparseExtension%3At%2CmimeType%3Afunction(e)%7Bvar n%3Dt(e).toLowerCase()%3Breturn(r%3D"application%2Ffont-woff"%2Co%3D"image%2Fjpeg"%2C%7Bwoff%3Ar%2Cwoff2%3Ar%2Cttf%3A"application%2Ffont-truetype"%2Ceot%3A"application%2Fvnd.ms-fontobject"%2Cpng%3A"image%2Fpng"%2Cjpg%3Ao%2Cjpeg%3Ao%2Cgif%3A"image%2Fgif"%2Ctiff%3A"image%2Ftiff"%2Csvg%3A"image%2Fsvg%2Bxml"%7D)%5Bn%5D%7C%7C""%3Bvar r%2Co%7D%2CdataAsUrl%3Afunction(e%2Ct)%7Breturn"data%3A"%2Bt%2B"%3Bbase64%2C"%2Be%7D%2CisDataUrl%3Afunction(e)%7Breturn-1!%3D%3De.search(%2F%5E(data%3A)%2F)%7D%2CcanvasToBlob%3Afunction(e)%7Breturn e.toBlob%3Fnew Promise((function(t)%7Be.toBlob(t)%7D))%3Afunction(e)%7Breturn new Promise((function(t)%7Bfor(var n%3Dwindow.atob(e.toDataURL().split("%2C")%5B1%5D)%2Cr%3Dn.length%2Co%3Dnew Uint8Array(r)%2Ci%3D0%3Bi<r%3Bi%2B%2B)o%5Bi%5D%3Dn.charCodeAt(i)%3Bt(new Blob(%5Bo%5D%2C%7Btype%3A"image%2Fpng"%7D))%7D))%7D(e)%7D%2CresolveUrl%3Afunction(e%2Ct)%7Bvar n%3Ddocument.implementation.createHTMLDocument()%2Cr%3Dn.createElement("base")%3Bn.head.appendChild(r)%3Bvar o%3Dn.createElement("a")%3Breturn n.body.appendChild(o)%2Cr.href%3Dt%2Co.href%3De%2Co.href%7D%2CgetAndEncode%3Afunction(e)%7Bvar t%3D3e4%3Bu.impl.options.cacheBust%26%26(e%2B%3D(%2F%5C%3F%2F.test(e)%3F"%26"%3A"%3F")%2B(new Date).getTime())%3Breturn new Promise((function(n)%7Bvar r%2Co%3Dnew XMLHttpRequest%3Bif(o.onreadystatechange%3Dc%2Co.ontimeout%3Da%2Co.responseType%3D"blob"%2Co.timeout%3Dt%2Co.open("GET"%2Ce%2C!0)%2Co.send()%2Cu.impl.options.imagePlaceholder)%7Bvar i%3Du.impl.options.imagePlaceholder.split(%2F%2C%2F)%3Bi%26%26i%5B1%5D%26%26(r%3Di%5B1%5D)%7Dfunction c()%7Bif(4%3D%3D%3Do.readyState)if(200%3D%3D%3Do.status)%7Bvar t%3Dnew FileReader%3Bt.onloadend%3Dfunction()%7Bvar e%3Dt.result.split(%2F%2C%2F)%5B1%5D%3Bn(e)%7D%2Ct.readAsDataURL(o.response)%7Delse r%3Fn(r)%3Al("cannot fetch resource%3A "%2Be%2B"%2C status%3A "%2Bo.status)%7Dfunction a()%7Br%3Fn(r)%3Al("timeout of "%2Bt%2B"ms occured while fetching resource%3A "%2Be)%7Dfunction l(e)%7Bconsole.error(e)%2Cn("")%7D%7D))%7D%2Cuid%3A(e%3D0%2Cfunction()%7Breturn"u"%2Bt()%2Be%2B%2B%3Bfunction t()%7Breturn("0000"%2B(Math.random()*Math.pow(36%2C4)<<0).toString(36)).slice(-4)%7D%7D)%2Cdelay%3Afunction(e)%7Breturn function(t)%7Breturn new Promise((function(n)%7BsetTimeout((function()%7Bn(t)%7D)%2Ce)%7D))%7D%7D%2CasArray%3Afunction(e)%7Bfor(var t%3D%5B%5D%2Cn%3De.length%2Cr%3D0%3Br<n%3Br%2B%2B)t.push(e%5Br%5D)%3Breturn t%7D%2CescapeXhtml%3Afunction(e)%7Breturn e.replace(%2F%23%2Fg%2C"%2523").replace(%2F%5Cn%2Fg%2C"%250A")%7D%2CmakeImage%3Afunction(e)%7Breturn new Promise((function(t%2Cn)%7Bvar r%3Dnew Image%3Br.onload%3Dfunction()%7Bt(r)%7D%2Cr.onerror%3Dn%2Cr.src%3De%7D))%7D%2Cwidth%3Afunction(e)%7Bvar t%3Dn(e%2C"border-left-width")%2Cr%3Dn(e%2C"border-right-width")%3Breturn e.scrollWidth%2Bt%2Br%7D%2Cheight%3Afunction(e)%7Bvar t%3Dn(e%2C"border-top-width")%2Cr%3Dn(e%2C"border-bottom-width")%3Breturn e.scrollHeight%2Bt%2Br%7D%7D%3Bvar e%3Bfunction t(e)%7Bvar t%3D%2F%5C.(%5B%5E%5C.%5C%2F%5D*%3F)%24%2Fg.exec(e)%3Breturn t%3Ft%5B1%5D%3A""%7Dfunction n(e%2Ct)%7Bvar n%3Dwindow.getComputedStyle(e).getPropertyValue(t)%3Breturn parseFloat(n.replace("px"%2C""))%7D%7D()%2Cn%3Dfunction()%7Bvar e%3D%2Furl%5C(%5B'"%5D%3F(%5B%5E'"%5D%2B%3F)%5B'"%5D%3F%5C)%2Fg%3Breturn%7BinlineAll%3Afunction(e%2Ct%2Ci)%7Breturn u()%3FPromise.resolve(e)%3APromise.resolve(e).then(r).then((function(n)%7Bvar r%3DPromise.resolve(e)%3Breturn n.forEach((function(e)%7Br%3Dr.then((function(n)%7Breturn o(n%2Ce%2Ct%2Ci)%7D))%7D))%2Cr%7D))%3Bfunction u()%7Breturn!n(e)%7D%7D%2CshouldProcess%3An%2Cimpl%3A%7BreadUrls%3Ar%2Cinline%3Ao%7D%7D%3Bfunction n(t)%7Breturn-1!%3D%3Dt.search(e)%7Dfunction r(n)%7Bfor(var r%2Co%3D%5B%5D%3Bnull!%3D%3D(r%3De.exec(n))%3B)o.push(r%5B1%5D)%3Breturn o.filter((function(e)%7Breturn!t.isDataUrl(e)%7D))%7Dfunction o(e%2Cn%2Cr%2Co)%7Breturn Promise.resolve(n).then((function(e)%7Breturn r%3Ft.resolveUrl(e%2Cr)%3Ae%7D)).then(o%7C%7Ct.getAndEncode).then((function(e)%7Breturn t.dataAsUrl(e%2Ct.mimeType(n))%7D)).then((function(r)%7Breturn e.replace(function(e)%7Breturn new RegExp("(url%5C%5C(%5B'%5C"%5D%3F)("%2Bt.escape(e)%2B")(%5B'%5C"%5D%3F%5C%5C))"%2C"g")%7D(n)%2C"%241"%2Br%2B"%243")%7D))%7D%7D()%2Cr%3Dfunction()%7Breturn%7BresolveAll%3Afunction()%7Breturn e(document).then((function(e)%7Breturn Promise.all(e.map((function(e)%7Breturn e.resolve()%7D)))%7D)).then((function(e)%7Breturn e.join("%5Cn")%7D))%7D%2Cimpl%3A%7BreadAll%3Ae%7D%7D%3Bfunction e()%7Breturn Promise.resolve(t.asArray(document.styleSheets)).then((function(e)%7Bvar n%3D%5B%5D%3Breturn e.forEach((function(e)%7Btry%7Bt.asArray(e.cssRules%7C%7C%5B%5D).forEach(n.push.bind(n))%7Dcatch(t)%7Bconsole.log("Error while reading CSS rules from "%2Be.href%2Ct.toString())%7D%7D))%2Cn%7D)).then((function(e)%7Breturn e.filter((function(e)%7Breturn e.type%3D%3D%3DCSSRule.FONT_FACE_RULE%7D)).filter((function(e)%7Breturn n.shouldProcess(e.style.getPropertyValue("src"))%7D))%7D)).then((function(t)%7Breturn t.map(e)%7D))%3Bfunction e(e)%7Breturn%7Bresolve%3Afunction()%7Bvar t%3D(e.parentStyleSheet%7C%7C%7B%7D).href%3Breturn n.inlineAll(e.cssText%2Ct)%7D%2Csrc%3Afunction()%7Breturn e.style.getPropertyValue("src")%7D%7D%7D%7D%7D()%2Co%3Dfunction()%7Breturn%7BinlineAll%3Afunction r(o)%7Breturn o instanceof Element%3Fi(o).then((function()%7Breturn o instanceof HTMLImageElement%3Fe(o).inline()%3APromise.all(t.asArray(o.childNodes).map((function(e)%7Breturn r(e)%7D)))%7D))%3APromise.resolve(o)%3Bfunction i(e)%7Bvar t%3De.style.getPropertyValue("background")%3Breturn t%3Fn.inlineAll(t).then((function(t)%7Be.style.setProperty("background"%2Ct%2Ce.style.getPropertyPriority("background"))%7D)).then((function()%7Breturn e%7D))%3APromise.resolve(e)%7D%7D%2Cimpl%3A%7BnewImage%3Ae%7D%7D%3Bfunction e(e)%7Breturn%7Binline%3Afunction(n)%7Breturn t.isDataUrl(e.src)%3FPromise.resolve()%3APromise.resolve(e.src).then(n%7C%7Ct.getAndEncode).then((function(n)%7Breturn t.dataAsUrl(n%2Ct.mimeType(e.src))%7D)).then((function(t)%7Breturn new Promise((function(n%2Cr)%7Be.onload%3Dn%2Ce.onerror%3Dr%2Ce.src%3Dt%7D))%7D))%7D%7D%7D%7D()%2Ci%3D%7BimagePlaceholder%3Avoid 0%2CcacheBust%3A!1%7D%2Cu%3D%7BtoSvg%3Ac%2CtoPng%3Afunction(e%2Ct)%7Breturn a(e%2Ct%7C%7C%7B%7D).then((function(e)%7Breturn e.toDataURL()%7D))%7D%2CtoJpeg%3Afunction(e%2Ct)%7Breturn a(e%2Ct%3Dt%7C%7C%7B%7D).then((function(e)%7Breturn e.toDataURL("image%2Fjpeg"%2Ct.quality%7C%7C1)%7D))%7D%2CtoBlob%3Afunction(e%2Cn)%7Breturn a(e%2Cn%7C%7C%7B%7D).then(t.canvasToBlob)%7D%2CtoPixelData%3Afunction(e%2Cn)%7Breturn a(e%2Cn%7C%7C%7B%7D).then((function(n)%7Breturn n.getContext("2d").getImageData(0%2C0%2Ct.width(e)%2Ct.height(e)).data%7D))%7D%2Cimpl%3A%7BfontFaces%3Ar%2Cimages%3Ao%2Cutil%3At%2Cinliner%3An%2Coptions%3A%7B%7D%7D%7D%3Bfunction c(e%2Cn)%7Breturn function(e)%7Bvoid 0%3D%3D%3De.imagePlaceholder%3Fu.impl.options.imagePlaceholder%3Di.imagePlaceholder%3Au.impl.options.imagePlaceholder%3De.imagePlaceholder%3Bvoid 0%3D%3D%3De.cacheBust%3Fu.impl.options.cacheBust%3Di.cacheBust%3Au.impl.options.cacheBust%3De.cacheBust%7D(n%3Dn%7C%7C%7B%7D)%2CPromise.resolve(e).then((function(e)%7Breturn l(e%2Cn.filter%2C!0)%7D)).then(s).then(f).then((function(e)%7Bn.bgcolor%26%26(e.style.backgroundColor%3Dn.bgcolor)%3Bn.width%26%26(e.style.width%3Dn.width%2B"px")%3Bn.height%26%26(e.style.height%3Dn.height%2B"px")%3Bn.style%26%26Object.keys(n.style).forEach((function(t)%7Be.style%5Bt%5D%3Dn.style%5Bt%5D%7D))%3Breturn e%7D)).then((function(r)%7Breturn function(e%2Cn%2Cr)%7Breturn Promise.resolve(e).then((function(e)%7Breturn e.setAttribute("xmlns"%2C"http%3A%2F%2Fwww.w3.org%2F1999%2Fxhtml")%2C(new XMLSerializer).serializeToString(e)%7D)).then(t.escapeXhtml).then((function(e)%7Breturn'<foreignObject x%3D"0" y%3D"0" width%3D"100%25" height%3D"100%25">'%2Be%2B"<%2FforeignObject>"%7D)).then((function(e)%7Breturn'<svg xmlns%3D"http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg" width%3D"'%2Bn%2B'" height%3D"'%2Br%2B'">'%2Be%2B"<%2Fsvg>"%7D)).then((function(e)%7Breturn"data%3Aimage%2Fsvg%2Bxml%3Bcharset%3Dutf-8%2C"%2Be%7D))%7D(r%2Cn.width%7C%7Ct.width(e)%2Cn.height%7C%7Ct.height(e))%7D))%7Dfunction a(e%2Cn)%7Breturn c(e%2Cn).then(t.makeImage).then(t.delay(100)).then((function(r)%7Bvar o%3Dfunction(e)%7Bvar r%3Ddocument.createElement("canvas")%3Bif(r.width%3Dn.width%7C%7Ct.width(e)%2Cr.height%3Dn.height%7C%7Ct.height(e)%2Cn.bgcolor)%7Bvar o%3Dr.getContext("2d")%3Bo.fillStyle%3Dn.bgcolor%2Co.fillRect(0%2C0%2Cr.width%2Cr.height)%7Dreturn r%7D(e)%3Breturn o.getContext("2d").drawImage(r%2C0%2C0)%2Co%7D))%7Dfunction l(e%2Cn%2Cr)%7Breturn r%7C%7C!n%7C%7Cn(e)%3FPromise.resolve(e).then((function(e)%7Breturn e instanceof HTMLCanvasElement%3Ft.makeImage(e.toDataURL())%3Ae.cloneNode(!1)%7D)).then((function(r)%7Breturn function(e%2Cn%2Cr)%7Bvar o%3De.childNodes%3Breturn 0%3D%3D%3Do.length%3FPromise.resolve(n)%3Ai(n%2Ct.asArray(o)%2Cr).then((function()%7Breturn n%7D))%3Bfunction i(e%2Ct%2Cn)%7Bvar r%3DPromise.resolve()%3Breturn t.forEach((function(t)%7Br%3Dr.then((function()%7Breturn l(t%2Cn)%7D)).then((function(t)%7Bt%26%26e.appendChild(t)%7D))%7D))%2Cr%7D%7D(e%2Cr%2Cn)%7D)).then((function(n)%7Breturn function(e%2Cn)%7Breturn n instanceof Element%3FPromise.resolve().then(r).then(o).then(i).then(u).then((function()%7Breturn n%7D))%3An%3Bfunction r()%7Bfunction r(e%2Cn)%7Bfunction r(e%2Cn)%7Bt.asArray(e).forEach((function(t)%7Bn.setProperty(t%2Ce.getPropertyValue(t)%2Ce.getPropertyPriority(t))%7D))%7De.cssText%3Fn.cssText%3De.cssText%3Ar(e%2Cn)%7Dr(window.getComputedStyle(e)%2Cn.style)%7Dfunction o()%7Bfunction r(r)%7Bvar o%3Dwindow.getComputedStyle(e%2Cr)%2Ci%3Do.getPropertyValue("content")%3Bif(""!%3D%3Di%26%26"none"!%3D%3Di)%7Bvar u%3Dt.uid()%3Bn.className%3Dn.className%2B" "%2Bu%3Bvar c%3Ddocument.createElement("style")%3Bc.appendChild(a(u%2Cr%2Co))%2Cn.appendChild(c)%7Dfunction a(e%2Cn%2Cr)%7Bvar o%3D"."%2Be%2B"%3A"%2Bn%2Ci%3Dr.cssText%3Fu(r)%3Ac(r)%3Breturn document.createTextNode(o%2B"%7B"%2Bi%2B"%7D")%3Bfunction u(e)%7Bvar t%3De.getPropertyValue("content")%3Breturn e.cssText%2B" content%3A "%2Bt%2B"%3B"%7Dfunction c(e)%7Breturn t.asArray(e).map(n).join("%3B ")%2B"%3B"%3Bfunction n(t)%7Breturn t%2B"%3A "%2Be.getPropertyValue(t)%2B(e.getPropertyPriority(t)%3F" !important"%3A"")%7D%7D%7D%7D%5B"%3Abefore"%2C"%3Aafter"%5D.forEach((function(e)%7Br(e)%7D))%7Dfunction i()%7Be instanceof HTMLTextAreaElement%26%26(n.innerHTML%3De.value)%2Ce instanceof HTMLInputElement%26%26n.setAttribute("value"%2Ce.value)%7Dfunction u()%7Bn instanceof SVGElement%26%26(n.setAttribute("xmlns"%2C"http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg")%2Cn instanceof SVGRectElement%26%26%5B"width"%2C"height"%5D.forEach((function(e)%7Bvar t%3Dn.getAttribute(e)%3Bt%26%26n.style.setProperty(e%2Ct)%7D)))%7D%7D(e%2Cn)%7D))%3APromise.resolve()%7Dfunction s(e)%7Breturn r.resolveAll().then((function(t)%7Bvar n%3Ddocument.createElement("style")%3Breturn e.appendChild(n)%2Cn.appendChild(document.createTextNode(t))%2Ce%7D))%7Dfunction f(e)%7Breturn o.inlineAll(e).then((function()%7Breturn e%7D))%7D"undefined"!%3Dtypeof module%3Fmodule.exports%3Du%3Ae.domtoimage%3Du%7D(this)%3Bvar node%3Ddocument.querySelector(".qv-panel-sheet")%2Cnode_height%3Dnode.clientHeight%2Cnode_width%3Dnode.clientWidth%2CaspectRatio%3D1.6%3Bnode.style.width%3Dnode_height*aspectRatio%2B"px"%2Cdomtoimage.toJpeg(node%2C%7Bquality%3A.95%2Cwidth%3Anode_height*aspectRatio%2Cheight%3Anode_height%7D).then((function(e)%7Bvar t%3Ddocument.createElement("a")%3Bt.download%3Ddocument.title%2B".jpeg"%2Ct.href%3De%2Ct.click()%2Ct.remove()%7D)).catch((e%3D>%7Bconsole.log(e)%2Calert("Sorry%2C this sheet could not be captured. Please try other sheets.")%7D))%2CsetTimeout((function()%7Bnode.style.width%3Dnode_width%2B"px"%2Cnode.style.width%3Dnull%7D)%2C3e3)%3B%7D)()%3B

**Note**  
-   Before installing a Bookmarklet, make sure your browser’s bookmarks toolbar is visible.
-   To remove a Bookmarklet, simply right click on it and hit delete.

**How to use**
-   Open a QlikSense app sheet whether its on QlikCloud or on-premise
-   Click on the "Thumbnail Generator" bookmarklet
-   It will temporarily resize your sheet content dimension with the optimal aspect ratio of a thumbnail 8:5 then automatically takes screenshot of it
-   The screenshot jpg  file should be ready and automatically be downloaded within a few seconds

