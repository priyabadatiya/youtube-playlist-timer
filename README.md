# Youtube Playlist Snippet to generate total playlist time.
```js
var total=Array.from(document.querySelectorAll('.playlist-items')[0].childNodes).map(a=>a.children[0].children[0].children[1].innerText.split('\n')[0]);

var ts= total.map((cv)=>(+cv.split(":")[0])*60+(+cv.split(":")[1]));


var totalSec = ts.reduce((acc,cv)=>{
return acc+=cv},0)

var hours = Math.floor(totalSec / 3600);
totalSec %= 3600;
 var minutes = Math.floor(totalSec / 60);
 var seconds = totalSec % 60;

alert (`Total Time of this Playlist is ${hours}:${minutes}:${seconds}`)
```

# Instructions.
- Use the above snippet until your whole page will be loaded.