
**GINQO QlikSense Thumbnail generator** is a bookmarklet to take screenshot of your QlikSense app in proper size ratio and download it into JPEG.
It depends on the [dom-to-image](https://github.com/tsayen/dom-to-image) Javascript library by Anatolii Saienko, Paul Bakaus (original idea) that is hardcoded in the script. It generates an image from the QlikSense app sheet in Base64 format with javascript without create external calls to any server or anything on every modern browser.




**About bookmarklet**

A [bookmarklet](https://en.wikipedia.org/wiki/Bookmarklet) is like a bookmark, but instead of loading a specific page, it injects JavaScript into the current page in your browser for added functionality. 





**Installation** 

Installation of this bookmarklet is performed by creating a new bookmark, and pasting the code below into  the URL destination field. Or go to [https://ginqo.com/thumbnail](https://ginqo.com/thumbnail) and drag the button to your bookmarks bar.

    javascript:(function()%7B!function(e)%7B%22use%20strict%22%3Bvar%20t%3Dfunction()%7Breturn%7Bescape%3Afunction(e)%7Breturn%20e.replace(%2F(%5B.*%2B%3F%5E%24%7B%7D()%7C%5C%5B%5C%5D%5C%2F%5C%5C%5D)%2Fg%2C%22%5C%5C%241%22)%7D%2CparseExtension%3At%2CmimeType%3Afunction(e)%7Bvar%20n%3Dt(e).toLowerCase()%3Breturn(r%3D%22application%2Ffont-woff%22%2Co%3D%22image%2Fjpeg%22%2C%7Bwoff%3Ar%2Cwoff2%3Ar%2Cttf%3A%22application%2Ffont-truetype%22%2Ceot%3A%22application%2Fvnd.ms-fontobject%22%2Cpng%3A%22image%2Fpng%22%2Cjpg%3Ao%2Cjpeg%3Ao%2Cgif%3A%22image%2Fgif%22%2Ctiff%3A%22image%2Ftiff%22%2Csvg%3A%22image%2Fsvg%2Bxml%22%7D)%5Bn%5D%7C%7C%22%22%3Bvar%20r%2Co%7D%2CdataAsUrl%3Afunction(e%2Ct)%7Breturn%22data%3A%22%2Bt%2B%22%3Bbase64%2C%22%2Be%7D%2CisDataUrl%3Afunction(e)%7Breturn-1!%3D%3De.search(%2F%5E(data%3A)%2F)%7D%2CcanvasToBlob%3Afunction(e)%7Breturn%20e.toBlob%3Fnew%20Promise((function(t)%7Be.toBlob(t)%7D))%3Afunction(e)%7Breturn%20new%20Promise((function(t)%7Bfor(var%20n%3Dwindow.atob(e.toDataURL().split(%22%2C%22)%5B1%5D)%2Cr%3Dn.length%2Co%3Dnew%20Uint8Array(r)%2Ci%3D0%3Bi%3Cr%3Bi%2B%2B)o%5Bi%5D%3Dn.charCodeAt(i)%3Bt(new%20Blob(%5Bo%5D%2C%7Btype%3A%22image%2Fpng%22%7D))%7D))%7D(e)%7D%2CresolveUrl%3Afunction(e%2Ct)%7Bvar%20n%3Ddocument.implementation.createHTMLDocument()%2Cr%3Dn.createElement(%22base%22)%3Bn.head.appendChild(r)%3Bvar%20o%3Dn.createElement(%22a%22)%3Breturn%20n.body.appendChild(o)%2Cr.href%3Dt%2Co.href%3De%2Co.href%7D%2CgetAndEncode%3Afunction(e)%7Bvar%20t%3D3e4%3Bu.impl.options.cacheBust%26%26(e%2B%3D(%2F%5C%3F%2F.test(e)%3F%22%26%22%3A%22%3F%22)%2B(new%20Date).getTime())%3Breturn%20new%20Promise((function(n)%7Bvar%20r%2Co%3Dnew%20XMLHttpRequest%3Bif(o.onreadystatechange%3Dc%2Co.ontimeout%3Da%2Co.responseType%3D%22blob%22%2Co.timeout%3Dt%2Co.open(%22GET%22%2Ce%2C!0)%2Co.send()%2Cu.impl.options.imagePlaceholder)%7Bvar%20i%3Du.impl.options.imagePlaceholder.split(%2F%2C%2F)%3Bi%26%26i%5B1%5D%26%26(r%3Di%5B1%5D)%7Dfunction%20c()%7Bif(4%3D%3D%3Do.readyState)if(200%3D%3D%3Do.status)%7Bvar%20t%3Dnew%20FileReader%3Bt.onloadend%3Dfunction()%7Bvar%20e%3Dt.result.split(%2F%2C%2F)%5B1%5D%3Bn(e)%7D%2Ct.readAsDataURL(o.response)%7Delse%20r%3Fn(r)%3Al(%22cannot%20fetch%20resource%3A%20%22%2Be%2B%22%2C%20status%3A%20%22%2Bo.status)%7Dfunction%20a()%7Br%3Fn(r)%3Al(%22timeout%20of%20%22%2Bt%2B%22ms%20occured%20while%20fetching%20resource%3A%20%22%2Be)%7Dfunction%20l(e)%7Bconsole.error(e)%2Cn(%22%22)%7D%7D))%7D%2Cuid%3A(e%3D0%2Cfunction()%7Breturn%22u%22%2Bt()%2Be%2B%2B%3Bfunction%20t()%7Breturn(%220000%22%2B(Math.random()*Math.pow(36%2C4)%3C%3C0).toString(36)).slice(-4)%7D%7D)%2Cdelay%3Afunction(e)%7Breturn%20function(t)%7Breturn%20new%20Promise((function(n)%7BsetTimeout((function()%7Bn(t)%7D)%2Ce)%7D))%7D%7D%2CasArray%3Afunction(e)%7Bfor(var%20t%3D%5B%5D%2Cn%3De.length%2Cr%3D0%3Br%3Cn%3Br%2B%2B)t.push(e%5Br%5D)%3Breturn%20t%7D%2CescapeXhtml%3Afunction(e)%7Breturn%20e.replace(%2F%23%2Fg%2C%22%2523%22).replace(%2F%5Cn%2Fg%2C%22%250A%22)%7D%2CmakeImage%3Afunction(e)%7Breturn%20new%20Promise((function(t%2Cn)%7Bvar%20r%3Dnew%20Image%3Br.onload%3Dfunction()%7Bt(r)%7D%2Cr.onerror%3Dn%2Cr.src%3De%7D))%7D%2Cwidth%3Afunction(e)%7Bvar%20t%3Dn(e%2C%22border-left-width%22)%2Cr%3Dn(e%2C%22border-right-width%22)%3Breturn%20e.scrollWidth%2Bt%2Br%7D%2Cheight%3Afunction(e)%7Bvar%20t%3Dn(e%2C%22border-top-width%22)%2Cr%3Dn(e%2C%22border-bottom-width%22)%3Breturn%20e.scrollHeight%2Bt%2Br%7D%7D%3Bvar%20e%3Bfunction%20t(e)%7Bvar%20t%3D%2F%5C.(%5B%5E%5C.%5C%2F%5D*%3F)%24%2Fg.exec(e)%3Breturn%20t%3Ft%5B1%5D%3A%22%22%7Dfunction%20n(e%2Ct)%7Bvar%20n%3Dwindow.getComputedStyle(e).getPropertyValue(t)%3Breturn%20parseFloat(n.replace(%22px%22%2C%22%22))%7D%7D()%2Cn%3Dfunction()%7Bvar%20e%3D%2Furl%5C(%5B'%22%5D%3F(%5B%5E'%22%5D%2B%3F)%5B'%22%5D%3F%5C)%2Fg%3Breturn%7BinlineAll%3Afunction(e%2Ct%2Ci)%7Breturn%20u()%3FPromise.resolve(e)%3APromise.resolve(e).then(r).then((function(n)%7Bvar%20r%3DPromise.resolve(e)%3Breturn%20n.forEach((function(e)%7Br%3Dr.then((function(n)%7Breturn%20o(n%2Ce%2Ct%2Ci)%7D))%7D))%2Cr%7D))%3Bfunction%20u()%7Breturn!n(e)%7D%7D%2CshouldProcess%3An%2Cimpl%3A%7BreadUrls%3Ar%2Cinline%3Ao%7D%7D%3Bfunction%20n(t)%7Breturn-1!%3D%3Dt.search(e)%7Dfunction%20r(n)%7Bfor(var%20r%2Co%3D%5B%5D%3Bnull!%3D%3D(r%3De.exec(n))%3B)o.push(r%5B1%5D)%3Breturn%20o.filter((function(e)%7Breturn!t.isDataUrl(e)%7D))%7Dfunction%20o(e%2Cn%2Cr%2Co)%7Breturn%20Promise.resolve(n).then((function(e)%7Breturn%20r%3Ft.resolveUrl(e%2Cr)%3Ae%7D)).then(o%7C%7Ct.getAndEncode).then((function(e)%7Breturn%20t.dataAsUrl(e%2Ct.mimeType(n))%7D)).then((function(r)%7Breturn%20e.replace(function(e)%7Breturn%20new%20RegExp(%22(url%5C%5C(%5B'%5C%22%5D%3F)(%22%2Bt.escape(e)%2B%22)(%5B'%5C%22%5D%3F%5C%5C))%22%2C%22g%22)%7D(n)%2C%22%241%22%2Br%2B%22%243%22)%7D))%7D%7D()%2Cr%3Dfunction()%7Breturn%7BresolveAll%3Afunction()%7Breturn%20e(document).then((function(e)%7Breturn%20Promise.all(e.map((function(e)%7Breturn%20e.resolve()%7D)))%7D)).then((function(e)%7Breturn%20e.join(%22%5Cn%22)%7D))%7D%2Cimpl%3A%7BreadAll%3Ae%7D%7D%3Bfunction%20e()%7Breturn%20Promise.resolve(t.asArray(document.styleSheets)).then((function(e)%7Bvar%20n%3D%5B%5D%3Breturn%20e.forEach((function(e)%7Btry%7Bt.asArray(e.cssRules%7C%7C%5B%5D).forEach(n.push.bind(n))%7Dcatch(t)%7Bconsole.log(%22Error%20while%20reading%20CSS%20rules%20from%20%22%2Be.href%2Ct.toString())%7D%7D))%2Cn%7D)).then((function(e)%7Breturn%20e.filter((function(e)%7Breturn%20e.type%3D%3D%3DCSSRule.FONT_FACE_RULE%7D)).filter((function(e)%7Breturn%20n.shouldProcess(e.style.getPropertyValue(%22src%22))%7D))%7D)).then((function(t)%7Breturn%20t.map(e)%7D))%3Bfunction%20e(e)%7Breturn%7Bresolve%3Afunction()%7Bvar%20t%3D(e.parentStyleSheet%7C%7C%7B%7D).href%3Breturn%20n.inlineAll(e.cssText%2Ct)%7D%2Csrc%3Afunction()%7Breturn%20e.style.getPropertyValue(%22src%22)%7D%7D%7D%7D%7D()%2Co%3Dfunction()%7Breturn%7BinlineAll%3Afunction%20r(o)%7Breturn%20o%20instanceof%20Element%3Fi(o).then((function()%7Breturn%20o%20instanceof%20HTMLImageElement%3Fe(o).inline()%3APromise.all(t.asArray(o.childNodes).map((function(e)%7Breturn%20r(e)%7D)))%7D))%3APromise.resolve(o)%3Bfunction%20i(e)%7Bvar%20t%3De.style.getPropertyValue(%22background%22)%3Breturn%20t%3Fn.inlineAll(t).then((function(t)%7Be.style.setProperty(%22background%22%2Ct%2Ce.style.getPropertyPriority(%22background%22))%7D)).then((function()%7Breturn%20e%7D))%3APromise.resolve(e)%7D%7D%2Cimpl%3A%7BnewImage%3Ae%7D%7D%3Bfunction%20e(e)%7Breturn%7Binline%3Afunction(n)%7Breturn%20t.isDataUrl(e.src)%3FPromise.resolve()%3APromise.resolve(e.src).then(n%7C%7Ct.getAndEncode).then((function(n)%7Breturn%20t.dataAsUrl(n%2Ct.mimeType(e.src))%7D)).then((function(t)%7Breturn%20new%20Promise((function(n%2Cr)%7Be.onload%3Dn%2Ce.onerror%3Dr%2Ce.src%3Dt%7D))%7D))%7D%7D%7D%7D()%2Ci%3D%7BimagePlaceholder%3Avoid%200%2CcacheBust%3A!1%7D%2Cu%3D%7BtoSvg%3Ac%2CtoPng%3Afunction(e%2Ct)%7Breturn%20a(e%2Ct%7C%7C%7B%7D).then((function(e)%7Breturn%20e.toDataURL()%7D))%7D%2CtoJpeg%3Afunction(e%2Ct)%7Breturn%20a(e%2Ct%3Dt%7C%7C%7B%7D).then((function(e)%7Breturn%20e.toDataURL(%22image%2Fjpeg%22%2Ct.quality%7C%7C1)%7D))%7D%2CtoBlob%3Afunction(e%2Cn)%7Breturn%20a(e%2Cn%7C%7C%7B%7D).then(t.canvasToBlob)%7D%2CtoPixelData%3Afunction(e%2Cn)%7Breturn%20a(e%2Cn%7C%7C%7B%7D).then((function(n)%7Breturn%20n.getContext(%222d%22).getImageData(0%2C0%2Ct.width(e)%2Ct.height(e)).data%7D))%7D%2Cimpl%3A%7BfontFaces%3Ar%2Cimages%3Ao%2Cutil%3At%2Cinliner%3An%2Coptions%3A%7B%7D%7D%7D%3Bfunction%20c(e%2Cn)%7Breturn%20function(e)%7Bvoid%200%3D%3D%3De.imagePlaceholder%3Fu.impl.options.imagePlaceholder%3Di.imagePlaceholder%3Au.impl.options.imagePlaceholder%3De.imagePlaceholder%3Bvoid%200%3D%3D%3De.cacheBust%3Fu.impl.options.cacheBust%3Di.cacheBust%3Au.impl.options.cacheBust%3De.cacheBust%7D(n%3Dn%7C%7C%7B%7D)%2CPromise.resolve(e).then((function(e)%7Breturn%20l(e%2Cn.filter%2C!0)%7D)).then(s).then(f).then((function(e)%7Bn.bgcolor%26%26(e.style.backgroundColor%3Dn.bgcolor)%3Bn.width%26%26(e.style.width%3Dn.width%2B%22px%22)%3Bn.height%26%26(e.style.height%3Dn.height%2B%22px%22)%3Bn.style%26%26Object.keys(n.style).forEach((function(t)%7Be.style%5Bt%5D%3Dn.style%5Bt%5D%7D))%3Breturn%20e%7D)).then((function(r)%7Breturn%20function(e%2Cn%2Cr)%7Breturn%20Promise.resolve(e).then((function(e)%7Breturn%20e.setAttribute(%22xmlns%22%2C%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxhtml%22)%2C(new%20XMLSerializer).serializeToString(e)%7D)).then(t.escapeXhtml).then((function(e)%7Breturn'%3CforeignObject%20x%3D%220%22%20y%3D%220%22%20width%3D%22100%25%22%20height%3D%22100%25%22%3E'%2Be%2B%22%3C%2FforeignObject%3E%22%7D)).then((function(e)%7Breturn'%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%22'%2Bn%2B'%22%20height%3D%22'%2Br%2B'%22%3E'%2Be%2B%22%3C%2Fsvg%3E%22%7D)).then((function(e)%7Breturn%22data%3Aimage%2Fsvg%2Bxml%3Bcharset%3Dutf-8%2C%22%2Be%7D))%7D(r%2Cn.width%7C%7Ct.width(e)%2Cn.height%7C%7Ct.height(e))%7D))%7Dfunction%20a(e%2Cn)%7Breturn%20c(e%2Cn).then(t.makeImage).then(t.delay(100)).then((function(r)%7Bvar%20o%3Dfunction(e)%7Bvar%20r%3Ddocument.createElement(%22canvas%22)%3Bif(r.width%3Dn.width%7C%7Ct.width(e)%2Cr.height%3Dn.height%7C%7Ct.height(e)%2Cn.bgcolor)%7Bvar%20o%3Dr.getContext(%222d%22)%3Bo.fillStyle%3Dn.bgcolor%2Co.fillRect(0%2C0%2Cr.width%2Cr.height)%7Dreturn%20r%7D(e)%3Breturn%20o.getContext(%222d%22).drawImage(r%2C0%2C0)%2Co%7D))%7Dfunction%20l(e%2Cn%2Cr)%7Breturn%20r%7C%7C!n%7C%7Cn(e)%3FPromise.resolve(e).then((function(e)%7Breturn%20e%20instanceof%20HTMLCanvasElement%3Ft.makeImage(e.toDataURL())%3Ae.cloneNode(!1)%7D)).then((function(r)%7Breturn%20function(e%2Cn%2Cr)%7Bvar%20o%3De.childNodes%3Breturn%200%3D%3D%3Do.length%3FPromise.resolve(n)%3Ai(n%2Ct.asArray(o)%2Cr).then((function()%7Breturn%20n%7D))%3Bfunction%20i(e%2Ct%2Cn)%7Bvar%20r%3DPromise.resolve()%3Breturn%20t.forEach((function(t)%7Br%3Dr.then((function()%7Breturn%20l(t%2Cn)%7D)).then((function(t)%7Bt%26%26e.appendChild(t)%7D))%7D))%2Cr%7D%7D(e%2Cr%2Cn)%7D)).then((function(n)%7Breturn%20function(e%2Cn)%7Breturn%20n%20instanceof%20Element%3FPromise.resolve().then(r).then(o).then(i).then(u).then((function()%7Breturn%20n%7D))%3An%3Bfunction%20r()%7Bfunction%20r(e%2Cn)%7Bfunction%20r(e%2Cn)%7Bt.asArray(e).forEach((function(t)%7Bn.setProperty(t%2Ce.getPropertyValue(t)%2Ce.getPropertyPriority(t))%7D))%7De.cssText%3Fn.cssText%3De.cssText%3Ar(e%2Cn)%7Dr(window.getComputedStyle(e)%2Cn.style)%7Dfunction%20o()%7Bfunction%20r(r)%7Bvar%20o%3Dwindow.getComputedStyle(e%2Cr)%2Ci%3Do.getPropertyValue(%22content%22)%3Bif(%22%22!%3D%3Di%26%26%22none%22!%3D%3Di)%7Bvar%20u%3Dt.uid()%3Bn.className%3Dn.className%2B%22%20%22%2Bu%3Bvar%20c%3Ddocument.createElement(%22style%22)%3Bc.appendChild(a(u%2Cr%2Co))%2Cn.appendChild(c)%7Dfunction%20a(e%2Cn%2Cr)%7Bvar%20o%3D%22.%22%2Be%2B%22%3A%22%2Bn%2Ci%3Dr.cssText%3Fu(r)%3Ac(r)%3Breturn%20document.createTextNode(o%2B%22%7B%22%2Bi%2B%22%7D%22)%3Bfunction%20u(e)%7Bvar%20t%3De.getPropertyValue(%22content%22)%3Breturn%20e.cssText%2B%22%20content%3A%20%22%2Bt%2B%22%3B%22%7Dfunction%20c(e)%7Breturn%20t.asArray(e).map(n).join(%22%3B%20%22)%2B%22%3B%22%3Bfunction%20n(t)%7Breturn%20t%2B%22%3A%20%22%2Be.getPropertyValue(t)%2B(e.getPropertyPriority(t)%3F%22%20!important%22%3A%22%22)%7D%7D%7D%7D%5B%22%3Abefore%22%2C%22%3Aafter%22%5D.forEach((function(e)%7Br(e)%7D))%7Dfunction%20i()%7Be%20instanceof%20HTMLTextAreaElement%26%26(n.innerHTML%3De.value)%2Ce%20instanceof%20HTMLInputElement%26%26n.setAttribute(%22value%22%2Ce.value)%7Dfunction%20u()%7Bn%20instanceof%20SVGElement%26%26(n.setAttribute(%22xmlns%22%2C%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22)%2Cn%20instanceof%20SVGRectElement%26%26%5B%22width%22%2C%22height%22%5D.forEach((function(e)%7Bvar%20t%3Dn.getAttribute(e)%3Bt%26%26n.style.setProperty(e%2Ct)%7D)))%7D%7D(e%2Cn)%7D))%3APromise.resolve()%7Dfunction%20s(e)%7Breturn%20r.resolveAll().then((function(t)%7Bvar%20n%3Ddocument.createElement(%22style%22)%3Breturn%20e.appendChild(n)%2Cn.appendChild(document.createTextNode(t))%2Ce%7D))%7Dfunction%20f(e)%7Breturn%20o.inlineAll(e).then((function()%7Breturn%20e%7D))%7D%22undefined%22!%3Dtypeof%20module%3Fmodule.exports%3Du%3Ae.domtoimage%3Du%7D(this)%3Bvar%20node%3Ddocument.querySelector(%22.qv-panel-sheet%22)%2Cnode_height%3Dnode.clientHeight%2Cnode_width%3Dnode.clientWidth%2CaspectRatio%3D1.6%3Bnode.style.width%3Dnode_height*aspectRatio%2B%22px%22%2Cdomtoimage.toJpeg(node%2C%7Bquality%3A.95%2Cwidth%3Anode_height*aspectRatio%2Cheight%3Anode_height%7D).then((function(e)%7Bvar%20t%3Ddocument.createElement(%22a%22)%3Bt.download%3Ddocument.title%2B%22.jpeg%22%2Ct.href%3De%2Ct.click()%2Ct.remove()%7D)).catch((e%3D%3E%7Bconsole.log(e)%2Calert(%22Sorry%2C%20this%20sheet%20could%20not%20be%20captured.%20Please%20try%20other%20sheets.%22)%7D))%2CsetTimeout((function()%7Bnode.style.width%3Dnode_width%2B%22px%22%2Cnode.style.width%3Dnull%7D)%2C3e3)%3B%7D)()%3B

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
