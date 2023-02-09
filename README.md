<br />

# Easy Dimension Measurement System For Unity


# Introduction :



![image](https://user-images.githubusercontent.com/88411269/216851590-bd33ad4a-d12c-492e-b990-029453dee0c6.png) 

Using **EzDimension** is quite easy. it works with **Mouse** or **VR** input.
 We have 5 types of measurement :
 
 
|Types         |                       What To Measure          |MainLine          |Guide 	          | Arrows           | Number           |Border            |Arc               |Surface           |
|--------------|------------------------------------------------|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|
|Point To Point| Direct distance of two points                  |:heavy_check_mark:|                  |:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Linear        | Distance of two points along XYZ Axis          |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Aligned       | Distance of two points along their orientation |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Angle         | The angle between three points                 |:heavy_check_mark:|                  |                  |:heavy_check_mark:|                  |:heavy_check_mark:|                  |
|Area          | The area between selected points               |:heavy_check_mark:|                  |                  |:heavy_check_mark:|:heavy_check_mark:|                  |:heavy_check_mark:|

<br /><br />

 ## key Features :
* Compatible by Mobile Devices, AR & VR
* support dynamic transforms. if you move, rotate or scale the target objects in runtime, the dimension start and end will update correctly.
* Support Units (Milimeters, Centimeters, Meters, Inch, Foot, Yard)
* Support Custom Unit if you need a unit that was not in the units list.
* Update TextPosition manually and automatic based on camera position .
* Having control on the materials of each part.
* Having control on color of each part.
* Highlight dimension when mouse or XR ray interactor hovers on the text any dimension.
* selection system.
* full control of texts size, lines thickness, arrows size , etc... .
* change the parameters for all dimensions or disconnect some of them to have individual properties.
* Trigger event when selection changed and when mouse hovered on a dimension.
* diffrent types of offset to avoid Zfighting and text coverage behind the scene objects.

---

<br />

# Dependencies :

## Input System :

After install **input System** from package manager create an **Event System** and select it in the hierarchy, then in the inspector click on the **Replace with InputSystemUIInputModule** button. You can read the [**input system documentation**](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.5/manual/index.html).


<img src="https://user-images.githubusercontent.com/88411269/216845364-046d6af5-094a-490e-9da4-8f453f10e764.png" width="500">


<br/>

## Text Mesh Pro :
This package uses **TextMeshPro** too. Install it from package manager if you do not have it already.read the [**TextMeshPro documentation**](https://docs.unity3d.com/Manual/com.unity.textmeshpro.html).

<br/>

## XR Interaction Toolkit (Optional) :

if you need to use this package inside a **VR** game or app, there is a **Sample VR Script** that you can download it from package manager in the sample section. before downloading it you need to install **XR Interaction Toolkit 2.2.0** to use this sample. also you can write your own **VR Script** sample. We recommend to check the sample script because the **VR Script** should work with the starter Script properly. for more details about using this package for **HMD** check the [**Using EzDimension in VR**](#VRSetting).

---

<br/>

# Quick start :

1. Create an empty game object and rename it to **StarterGO** and add **EzDimStarter** component on it:

2. Create nine **UI buttons** and drag the **StarterGO** script inside the button. Then select these voids for each button :

* EzPointToPointDimension()
* EzLinearDimension()
* EzAlignedDimension()
* EzAngledDimension()
* EzAreaMeasure()
* HideSelectedDimensions()
* UnhideAll()
* DeleteSelectedDimensions()
* UpdateAll()


<img src="https://user-images.githubusercontent.com/88411269/216846372-5bf205e8-d45c-462c-90d9-feb1da2fc6d5.png" width="500">

<br/>

3. Select the **StarterGO**, then fill the references and set the parameters. If it’s your first run, we recommend to check the sample scene first.
Consider that the first field should be empty to test the dimensions with mouse input. We’ll explain how to use it in VR in the [**Using EzDimension in VR**](#VRSetting) section.

<img src="https://user-images.githubusercontent.com/88411269/216846440-11e8cad1-d26a-451e-83a6-f01bbbef0c4a.png" width="926">

<br/>

4 . When you fill the references and set the parameters, create a ground object and another two objects, check them having “Collider” component. you can create your first dimension by click on the button that you connected to “EzPointToPointDimension()” void.

<img src="https://user-images.githubusercontent.com/88411269/216851375-caaf83e1-1bf9-4e11-a058-665a60579b6b.gif" width="500">

congratulations, you made your first dimension!

---

<br/>

# Settings Notes :
## General Parameters :

<img src="https://user-images.githubusercontent.com/88411269/216851756-74f0d795-6e22-4bc3-9b59-5e47a110b82a.png" width="500">

For each dimensions we have some general settings in the starter script. if you take a look at the inspector when **StarterGO** is selected, you can find the **General** section.
these settings are share between more than one dimension. For example **Text Size** is share between all of them and arrow radius is share between **Point To Point**, **Linear** and **Aligned** dimension. You can read about the details of each option in the [**General References**](#GeneralReferences) section.

<br/>

## Colors :

<img src="https://user-images.githubusercontent.com/88411269/216856990-c7379445-a363-4cf6-a997-085c27e341cb.png" width="500">

the color section is shared between the dimensions too. . If you change the “Number Color”, It changes all of the dimensions number’s color except which dimensions that mark as individual. We’ll explain individuality of each dimension along the way. Last three colors will multiply with the dimension’s color when they are selected or when we hover mouse or VR-Interactor on number of an object. It works with a Lerp function line this : 




    if (mouse hovered on a text of a dimension)
          Color = Color.Lerp( numberColor, hoveredTint, 0.5f );

---

<br/>



# Dimension Types :






## Point To Point Dimension :

Point to point dimension is simple type of the measurement. It takes two Vector3 position and calculate the direct distance between these two points.
When run the void “EzPointToPointDimension()” by click on the button in your UI, The “EzPointToPointDimension” gameobject will create under the StarterGO but all of its child are invisible till you hit the first click on an object that has a collider. After that while you didn’t hit the second click, the dimension it measure the first click and the current mouse position (if mouse hovers on an object with collider). after hit the second click your dimension will add to the “dimensionsList” in the starter script and its done.
If you select the “EzPointToPointDimension” gameobject under the “StarterGO” and take a look at the inspector you can see that the dimension copied the parameters from starter script inside itself.


<br/>

<img src="https://user-images.githubusercontent.com/88411269/216855671-748c5473-5272-4f18-b502-b36fb1254dc5.png" width="500">


There are two types of parameters in all of the dimensions. Some of them are always individual and some of them get their value from ValueReference Component (which is the starter script), until you didn’t mark “Is Individual”. For example in this type of dimension, everything under the “IsIndividual” toggle (all parameters except “ValueReference”) can have its local value if you turn on this Boolean.so if you need to have control from another script on a dimension separately, first of all you need to turn on this option at the beginning.if you turn it off again, everything is fine and the values sets to your settings from the starter script because each scripts carries the starter script with itself in the “ValueReference” field.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/216858500-332b98f0-fa90-4e30-99cf-a9736b64d2f9.png" width="500">


By turning on “IsIndividual” We can have same dimension type with different settings.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/216858764-47cbd7af-16ce-4935-914c-8ba57de36b06.gif" width="500">

There is another option named “Is Dynamic”. If this option be true the dimension will update if target objects transforms changes. 
(If dimension is not individual it’s depend on starterScript/General/IsDynamic).You can check other parameters in [**General References**](#GeneralReferences) .

<br/>





 ## Linear Dimension :
 
linear dimension used to measure distance between two points in one main Axis. Its never rotate to any direction even if the target points have different position in R3. Measurement direction parameter determine the direction of measurement. 

<br/>

<img src="https://user-images.githubusercontent.com/88411269/216859029-48c5485b-bb39-40af-b0d3-4ef62724e09a.png" width="500">

For example if you choose “X” direction, it will measure the line between two target points in X direction. Also we can always choose the offset direction to other two direction. (measurement direction and offset direction can’t have same value, so if you choose same value, to avoid error code will replace the offset direction to one of other directions)

<br/>

<img src="https://user-images.githubusercontent.com/88411269/216859217-7a73bc02-3be8-4b59-a71e-656e628cf588.png" width="1000">

1-Measurement Direction = X, Offset Direction = Z. <br />
2-Measurement Direction = Z, Offset Direction = X.<br />
We have the same rule in Y direction. If you choose to measure the height of an object, the measurement direction will be “Y” and you can choose the offset direction between “X” or “Z”.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/216859258-fda2327b-bcdd-47ab-972d-7f9e93efa05d.png" width="500">

If the offset distance be less than the distance between two target points, the dimension will automatically change the secondary lines to be sure that it always connect target points

<br/>

<img src="https://user-images.githubusercontent.com/88411269/216859337-ce20a36f-f6c0-4ae9-97d0-0ac5f3d5530a.gif" width="500">

Draw the Linear Direction in “Z” axis and offset to "X" axis and changing the offset distance.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/216859356-eeec3929-5b8b-4f1e-b2f7-7e8d55269389.png" width="500">

If measured points where too close and text can’t feet between the secondary lines, there is an option to change the text position and arrow direction.

<br/>





## Aligned Dimension :

<br/>

Aligned dimension is useful to measure distance between two points in one of main coordinate planes or a costume plane.it support rotated objects as well.

<img src="https://user-images.githubusercontent.com/88411269/217420788-0f777d3d-d8e8-4a7b-b790-066b0a7410b3.png" width="500">

The settings are almost similar to linear dimension. Instead of measurement in “Linear Dimension” there is measurement plane option. 

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217422629-662161ee-1547-44ee-941a-1f5e9b4b1752.png" width="500">

Also, we have an option named “Reverse Direction”. The function of this Boolean is exactly same as multiply offset distance by -1. In this type of dimension the positive direction of offset distance is based on which target point hit first. Assume we have “point A” and “point B”. during the creating this dimension if click on “point A” and then click on “point B”, the positive offset direction is different the left side of the border of AB. So depends on witch point is first, the positive direction is different.by this Boolean you can avoid to have negative offset distance to reverse offset direction positive side.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217424746-44af1c23-6ea0-4869-be44-cd3c76990a0f.gif" width="500">

There is four states for direction plane (XZ, XY, ZY, Free). If you set the direction offset to Free before creating the dimension, after selecting A and B points, a plane appears and you can dictate your custom offset direction. by click on the appeared plane which is the input of the “Aligned Dim Free Mode Plane Prefab”, the position of this point will store into “Direction Point in Free Mode”. So if you don’t change this value and switch the Direction plane, you can change it to Free mode again later. Or by editing this value you can change the direction. be aware that if you use free mode, it does not support transform change yet. Turn off “Is Dynamic” if you want to use it in any moving object. We have this on our road map and we will make it possible in the next updates.





## Angle Dimension :

<br/>

Angle dimension measures the angle between three points. These points can be in the main planes (XZ, XY, YZ) or in the custom plane.
It measures 0 to 180 degrees. 
 
<br/>

<img src="https://user-images.githubusercontent.com/88411269/217425866-5e915710-f361-4adf-8a24-31f90e317901.png" width="500">


<br/>

<img src="https://user-images.githubusercontent.com/88411269/217530046-9374c24e-05d7-4091-bafe-1512d90aa8b3.png" width="500">

There is four parts in an angle dimension. two lines, a number and a plane with a transparent material to draw the arc between two lines. The arc GameObject scale can controls by the “Arc Scale” parameter. Other features depend on its material shader. The shader have to has Color and Degree option. Other options are optional based what we need.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217530372-34f0c439-9dfe-4baa-abd5-494372b8c63c.png" width="500">

If the text’s width was larger than the space between two curve, text position and rotation will change and it goes outside. 
There is a vector2 input named “Text Offset If Not Fit”. You can control the position of the text by changing this input.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217530740-b7539441-4389-40d2-a8d1-77c1abff63c3.gif" width="500">

The angle dimension like others supports dynamic transform If you check “Is Dynamic”.

<br/>

![AngleDimension_Free](https://user-images.githubusercontent.com/88411269/217531103-d6c8ef1d-aef6-416e-9cf3-f17dae02b457.gif)

The angle dimension can draw in main planes or in custom plane. To draw it on custom plane change the “Angle Measurement Plane” to “Free” and just click where you need to measure.

<br/>

To reduce the any intersection between the dimension and target objects you can increase the “Normal Offset” if the dimension is individual or “Hit Normal Offset” in the starter script if it’s not individual. It will get the first hit point normal and move the dimension along it forward. Also this parameters helps to avoid Z-fighting. Always set it to a small amount.

<br/><br/>







## Area Measure :

<br/>

Area Measure can calculate the area between some points. There is some option to make the text camera base or rotate it. Because they are public variables you can control them from other script for example based on your camera transform. It’s up to you how you want control the text orientation on the surface. The always has lay down to the area surface.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217532089-f0f665e7-58f7-486a-badd-ce7a1575f31e.png" width="500">

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217532420-782710b7-e115-4416-b440-8c89d16e1456.png" width="500">

The “Area Measure” has four main parts. handles, surface, border and the number text. 
When you click on a surface, the handle prefab will instantiate where you clicked. and if you press right click, the draw function will call and the area measure will create. 

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217532878-b0909a77-cae2-4537-bbb8-2112ced2d468.gif" width="500">

If you make the handle prefab selectable or moveable in your project, the area measure supports dynamic transform and will update if you changed any handle. Consider that there is no “IsDynamic” Boolean and if you change the position of any handle it always updates the area.

<br/>

<img src="https://user-images.githubusercontent.com/88411269/217533595-2ab4127b-b9b7-4083-9a4d-45febe300334.gif" width="500">

Same as angle dimension and aligned dimension, the area measure also can draw on the main planes ( XZ, XY, ZY ) and on a custom plane if you set the “Area Measurement Plane” to “Free”. When you choose “Free” and start to draw an area measure on an inclined plane or a ramp, the script get the first hit point normal and define the custom draw plane based on that. 

<br/>

 --- 
 
<br/><br/>
  
<a name="Scripting Manual">
  </a>
  
# Scripting Manual :
 
![FlowChart](https://user-images.githubusercontent.com/88411269/217855770-6beb9c7a-ac8d-42e5-befd-e4c23f1217f3.png)


 
<br/><br/>

<a name="VRSetting">
  </a>

### Using EzDimension in VR :





<br/>

 --- 
 
<br/><br/>

<a name="GeneralReferences">
  </a>

### General References :
  
  
  
