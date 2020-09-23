<div align="center">

## A Colorful Ball of Light Function


</div>

### Description

This code will allow you to make a ball of light of any size and color, ready to go in a module! Please vote.
 
### More Info
 
frm As Form, originx As Integer, originy As Integer, radius As Integer, red As Integer, green As Integer, blue As Integer

Returns a filled ball of light on your form that displays a white center that ascends to any color of your choice.

Somewhat slow.. the bigger/more balls of light the slower it will get.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[SethMicah](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/sethmicah.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 6\.0
**Category**       |[Graphics](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics__1-46.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/sethmicah-a-colorful-ball-of-light-function__1-21250/archive/master.zip)





### Source Code

```
Public Function MakeLight(frm As Form, originx As Integer, originy As Integer, radius As Integer, red As Integer, green As Integer, blue As Integer)
For tiltx = -0.5 To 0.5 Step 0.5 ' offset it a tad to get the pixels not colored
For tilty = -0.5 To 0.5 Step 0.5 ' offset it a tad to get the pixels not colored
For tempradius = 0 To radius Step 1 ' colors multiple circles with origins from the origin to origin + radius
Randomize
circlecolor = Int(Rnd * (1 * (radius / 255))) + (tempradius / (radius / 255)) + 1 ' gets a random color in a specific range, give it the light effect
circlecolor = Abs(circlecolor - 255) ' inverts the colors from white outside to white inside
frm.Circle (originx + tiltx, originy + tilty), tempradius, RGB(circlecolor + red, circlecolor + green, circlecolor + blue) ' makes the circle
Next tempradius
Next tilty
Next tiltx
End Function
```

