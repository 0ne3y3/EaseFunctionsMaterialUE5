# Easing functions for UE4/5

Easing material functions for your UE material. All parameters are exposed :

![Easing function image](https://i.postimg.cc/zvbgwDQD/Ease-Functions.png)
Based on :
https://gist.github.com/mattatz/d7b8decb481947d2e37eab98aff2d0ad

I added a parabola curve because why not.

![Parabola easing function](https://i.postimg.cc/0jrX8tGy/Parabola-Curve.png)
## Installation

Download the content folder and just drag and drop uasset to your project content directory. Or download this whole git and place it in plugin folder.

**Important Note**
EaseInOutBounce and EaseInBounce functions may have a problem because it depend of the function EaseOutBounce.
You need to open material function and fix dependency manually.
## Something good to know

1) Some material functions may be more expensive as node based than direct hlsl code. Because of the nature of HLSL "if" branching. I didn't do any performance test so you may want to try swapping between node or hlsl custom code :

![HLSL custom code node](https://i.postimg.cc/zfKrNfzc/HLSLCode.png)

2) You can easily change the function to use vector2, vector3 or vector4 instead of scalar. Duplicate the material function and change the input type.
