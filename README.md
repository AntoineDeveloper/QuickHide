# QuickHide

Chrome Bookmark to quickly hide a webpage and change it's title and favicon

## Instalation

Create a bookmark with the following URL
This bookmark will be to hide the webpage

```
javascript:void%20function(){javascript:(()=%3E{(function(){localStorage.INITIAL_TITLE=document.title||%22ERROR%22,localStorage.INITIAL_ICON=function(){for(var%20a=document.getElementsByTagName(%22link%22),b=[],c=0;c%3Ca.length;c++){var%20d=a[c],e=d.getAttribute(%22rel%22);if(e%26%26-1%3Ce.toLowerCase().indexOf(%22icon%22)){var%20f=d.getAttribute(%22href%22);if(f)if(-1==f.toLowerCase().indexOf(%22https:%22)%26%26-1==f.toLowerCase().indexOf(%22http:%22)%26%260!=f.indexOf(%22//%22)){var%20g=window.location.protocol+%22//%22+window.location.host;if(window.location.port%26%26(g+=%22:%22+window.location.port),0==f.indexOf(%22/%22))g+=f;else{var%20h=window.location.pathname.split(%22/%22);h.pop();var%20j=h.join(%22/%22);g+=j+%22/%22+f}b.push(g)}else%20if(0==f.indexOf(%22//%22)){var%20k=window.location.protocol+f;b.push(k)}else%20b.push(f)}}return%20b}();var%20a=document.querySelector(%22link[rel*='icon']%22)||document.createElement(%22link%22);a.type=%22image/png%22,a.rel=%22shortcut%20icon%22,a.href=%22https://store-images.s-microsoft.com/image/apps.24656.9f7ae901-2f40-470c-a423-5b70576faf49.040355ee-bbcb-46be-b1ed-2b7bd2dca550.e00d1d8f-eeef-43d1-9657-9cf471e7c2ca%22,document.getElementsByTagName(%22head%22)[0].appendChild(a),document.title=%22Pluriportail%22})()})()}();
```

Create a second bookmark with the following URL
This bookmark will be to unhide the webpage

```
javascript: (() => {
	(function () {
		var websitelogo = localStorage["INITIAL_ICON"] || "";
		(function () {
			var link =
				document.querySelector("link[rel*='icon']") ||
				document.createElement("link");
			link.type = "image/png";
			link.rel = "shortcut icon";
			link.href = websitelogo;
			document.getElementsByTagName("head")[0].appendChild(link);
			document.title = localStorage["INITIAL_TITLE"] || "ERROR";
		})();
	})();
})();
```
