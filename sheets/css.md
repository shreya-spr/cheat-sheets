---
title: CSS
description: Cascading Style Sheets --> used to simplify making webpages and styling them. 
---  


## Center anything  
```
.center {
    display: flex;
    align-items: center;
    justify-content: center;
}
```  

## Filters in CSS with example 

Let's apply <b>blur</b> effect to a box  
```
.box {
    width: 100px;
    height: 100px;
    background-color: red;
    filter: blur(4px);
}
```

Let's apply <b>brightness</b> effect to a box  
```
.box {
    width: 100px;
    height: 100px;
    background-color: red;
    filter: brightness(67%);
}
```  
  
Let's apply <b>contrast</b> effect to a box  
```
.box {
    width: 100px;
    height: 100px;
    background-color: red;
    filter: contrast(67%);
}
```  
Let's apply <b>drop shadow</b> effect to a box  
```
.box {
    width: 100px;
    height: 100px;
    background-color: red;
    filter: drop-shadow(0 0 10px);
}
```  


Let's apply <b>grayscale</b> effect to a box  
```
.box {
    width: 100px;
    height: 100px;
    background-color: red;
    filter: grayscale(57%);
}
```  
## Additive rgb model  

_Syntax: `rgb(redhue, greenhue, bluehue)`_  
- hues can be changed to get the shade
- values range from 0 to 255
- eg: `rgb(0,0,0)` = pure black & `rgb(255,255,255)` = pure white
- So to mix *pure* blue and *pure* red: `rgb(255,0,255)`