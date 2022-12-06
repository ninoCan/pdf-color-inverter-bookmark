# PDF color inverter for browser

> **Disclaimer**
> I decline authorship of this snippet. I was provided with it asking for support from the Mozilla team after the builtin color inversion feature was disable from Firefox.

## How to use it

Create a bookmark for Firefox and copy paste the snippet into the field URL

    javascript:(function(){var S='#outerContainer>#mainContainer>#viewerContainer>#viewer>.page{filter:%20invert(100%);color:white}',SS,E=document.querySelector('style[id="style_!!!"]');if(E){S=E.disabled;E.disabled=(S==true)?false:true}else{SS=document.createElement('style');SS.setAttribute('type','text/css');SS.id='style_!!!';SS.innerHTML=S;document.querySelector('head').appendChild(SS);}})()
