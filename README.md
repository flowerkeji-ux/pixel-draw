# pixel-draw

A lightweight, minimal **HTML-based pixel art drawing game** into a data URI. This allows the entire application to be played instantly **directly from a URL**, eliminating the need for traditional hosting or servers.

## Quick Start
1. Copy the generated data URL.
2. Paste it into your browsers address bar
3. Start drawing your pixel art!



##  How It Was Made

1. **Source Development:**
 Written using  **HTML**, **CSS** grid layouts, and native **JavaScript** for state management and click-and-drag mechanics
2. **Minification:**
3.  The source code was compressed to remove unnecessary spaces, comments, and line breaks to minimize characters
 **Base64 Encoding:** The minified HTML string was converted into a Base64 string and prefixed with `data:text/html;base64,` to create the final executable URL.

## Easy
Easily readable and editable

"data:text/html,<meta name=viewport content="width=device-width"><title>Pixel Art</title><body style="font-family:sans-serif;text-align:center;user-select:none"><h1>Pixel Art</h1><p>Choose a color and drag to draw.</p><input id=color type=color> <button id=clear>Clear</button><br><br><div id=board style="display:grid;grid-template-columns:repeat(16,1fr);width:90vw;max-width:400px;margin:auto;touch-action:none"></div><script>let b=document.getElementById('board'),c=document.getElementById('color'),d=0;function paint(e){let p=document.elementFromPoint(e.clientX,e.clientY);if(p&&p.parentNode==b)p.style.background=c.value}for(let i=256;i--;){let p=document.createElement('div');p.style='aspect-ratio:1;border:1px solid lightgray;background:white';b.append(p)}b.onpointerdown=e=>{d=1;paint(e)};b.onpointermove=e=>{if(d)paint(e)};document.onpointerup=document.onpointercancel=()=>d=0;document.getElementById('clear').onclick=()=>[...b.children].forEach(p=>p.style.background='white')</script>"

<!--this is one of my first README.md so the format might be wrong-->





---
