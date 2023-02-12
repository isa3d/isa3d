<br />

# Easy Dimension Measurement System For Unity


# Introduction :



![image](https://user-images.githubusercontent.com/88411269/216851590-bd33ad4a-d12c-492e-b990-029453dee0c6.png) 

Using EzDimension is quite easy. It works with both mouse and VR inputs. There are five types of measurements available :
 
 
|Types         |                       What To Measure          |MainLine          |Guide 	          | Arrows           | Number           |Border            |Arc               |Surface           |
|--------------|------------------------------------------------|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|
|Point To Point| The direct distance between two points.                  |:heavy_check_mark:|                  |:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Linear        | The distance between two points along the X, Y, and Z axes.          |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Aligned       | The distance between two points along their orientation. |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Angle         | The angle between three points.                |:heavy_check_mark:|                  |                  |:heavy_check_mark:|                  |:heavy_check_mark:|                  |
|Area          | The area between selected points.               |:heavy_check_mark:|                  |                  |:heavy_check_mark:|:heavy_check_mark:|                  |:heavy_check_mark:|

<br /><br />

 ## key Features :
* Compatible with Mobile Devices, AR, and VR.
* Supports dynamic transforms. If you move, rotate, or scale the target objects during runtime, the dimension start and end will update correctly.
* Supports units of millimeters, centimeters, meters, inches, feet, and yards.
* Supports custom units if needed.
* Updates text position both manually and automatically based on the camera position.
* Offers control over the materials of each part.
* Offers control over the color of each part.
* Highlights dimensions when the mouse or XR ray interactor hovers over the dimension text.
* Has a selection system.
* Offers full control over text size, line thickness, arrow size, and more.
* Allows for adjusting parameters for all dimensions or disconnecting some to have individual properties.
* Triggers an event when selection changes and when the mouse hovers over a dimension.
* Offers different types of offsets to avoid Z-fighting and text coverage behind scene objects.

---

<br />

# Dependencies :

## Input System:
To set up the **Input System**, follow these steps:
1. Install the Input System from the package manager. 
2. Create an **Event System** and select it in the hierarchy. 
3. In the inspector, click the button labeled "Replace with InputSystemUIInputModule". 

For further information, refer to the [**Input System documentation**](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.5/manual/index.html).


<img src="https://user-images.githubusercontent.com/88411269/216845364-046d6af5-094a-490e-9da4-8f453f10e764.png" width="500">


<br/>

## TextMeshPro :
This package requires **TextMeshPro** to be installed. If you do not already have it, please install it from the package manager. For more information, refer to the [**TextMeshPro documentation**](https://docs.unity3d.com/Manual/com.unity.textmeshpro.html).

<br/>

## XR Interaction Toolkit (Optional):
This package provides the option to use the toolkit in virtual reality (VR) applications. If you plan to use this package in a VR environment, you must have the **XR Interaction Toolkit 2.2.0** installed. 

A sample VR script is available for download in the sample section of the package manager. This script serves as a starting point for integrating the package into a VR environment, and we highly recommend reviewing the script to ensure proper compatibility with the starter script. 

For further information on using the package with head-mounted displays (HMDs), please refer to the section on [**Using EzDimension in VR**](#VRSetting) in this documentation.

---

<br/>


<a name="QuickStart">
  </a>
  
# Quick Start :

1. Create an empty game object and rename it to **StarterGO**. Then, add the `EzDimStarter` component to it.

2. Create nine **UI buttons** and drag the `StarterGO` object into each button. Assign the following voids to each button, respectively:

- `EzPointToPointDimension()`
- `EzLinearDimension()`
- `EzAlignedDimension()`
- `EzAngledDimension()`
- `EzAreaMeasure()`
- `HideSelectedDimensions()`
- `UnhideAll()`
- `DeleteSelectedDimensions()`
- `UpdateAll()`

![Button Configuration](https://user-images.githubusercontent.com/88411269/216846372-5bf205e8-d45c-462c-90d9-feb1da2fc6d5.png)

<br/><br/>

3. Select the `StarterGO` object and fill in the required references and set the necessary parameters. If this is your first time using the package, it is recommended to review the sample scene before proceeding. Note that the first field should be left empty for testing the dimensions with mouse input. The procedure for using it in VR is explained in the [Using EzDimension in VR](#VRSetting) section.

![Reference Configuration](https://user-images.githubusercontent.com/88411269/218296772-9659a633-d6a8-4f21-82d6-1022a765fe88.jpg)

<br/><br/>

4. After filling in the references and setting the parameters, create a ground object and two additional objects with collider components. Then, you can create your first dimension by clicking the button that is connected to the `EzPointToPointDimension()` void.

![First Dimension Creation](https://user-images.githubusercontent.com/88411269/216851375-caaf83e1-1bf9-4e11-a058-665a60579b6b.gif)

Congratulations, you have successfully created your first dimension!

---

<br/>

# Settings Notes :
## General Parameters :

<img src="https://user-images.githubusercontent.com/88411269/216851756-74f0d795-6e22-4bc3-9b59-5e47a110b82a.png" width="500">

Each dimension has general settings in the Starter script, which can be accessed in the inspector when `StarterGO` is selected. In the `General` section, you will find options that are shared between multiple dimensions. For example, the `Text Size` setting is shared between all dimensions, while the arrow radius is shared between `Point To Point`, `Linear`, and `Aligned` dimensions. For more information on each option, see the [General References](#GeneralReferences) section.

<br/>

## Colors :

<img src="https://user-images.githubusercontent.com/88411269/216856990-c7379445-a363-4cf6-a997-085c27e341cb.png" width="500">

The color section is also shared between the dimensions in the ``` EzDimStarter ``` component. If you change the "Number Color", it changes the color of all the dimension numbers, except for those dimensions that are marked as individual. The individuality of each dimension will be explained along the way. The last three colors will multiply with the dimension's color when they are selected or when the mouse or VR-Interactor hovers over the number of an object. This is achieved using the following Lerp function:


    if (mouse hovered on a text of a dimension)
         Color = Color.Lerp( numberColor, hoveredTint, 0.5f );

---

<br/>



# Dimension Types :






## Point To Point Dimension :

Point to point dimension is a simple type of measurement. It calculates the direct distance between two Vector3 positions.

When you run the `EzPointToPointDimension()` void by clicking on the button in your UI, the EzPointToPointDimension `gameoOject` will be created under the StarterGO, but all of its child objects will be invisible until you first click on an object with a collider. From that point, while you haven't yet clicked a second time, the dimension will measure the first click and the current mouse position (if the mouse is hovering over an object with a collider). After you hit the second click, your dimension will be added to the `dimensionsList` in the starter script, and it's done.

If you select the EzPointToPointDimension `gameObject` under the StarterGO and examine the inspector, you will see that the dimension has copied the parameters from the starter script into itself.


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
  
<a name="ScriptingManual">
  </a>
  
# Scripting Manual :
![FlowChart_Mouse_VR](https://user-images.githubusercontent.com/88411269/218064085-cd827ca6-4782-4548-ad83-ad6cc4e22485.png)

As you can see in the flow chart, EzDimStarter component is the core of other inputs and components. Inside this script we have nine public void that we connected them to the buttons to create, hide, unhide, delete and update dimensions as we mentioned in “”Quick Start”” section. 
If you need to use this script in VR, you should add “DrawInVR” component on the same object that you added “EzDimStarter” . we will explain how it works in VR in the “” Using EzDimension in VR”” section.
If you want to work just with Mouse input, there is no need to have “”DrawInVR””, so our chart will be like this : 

![FlowChart_Mouse](https://user-images.githubusercontent.com/88411269/218064249-752e9671-75f6-4add-8593-45dc156e83d3.png)

 When one of the mentioned voids inside “EzDimStarter” called by pressing a UI button, for example assume you pressed “Point To Point”,  this code will run :
 
 ```C#
 
    public void EzPointToPointDimension()
    {
        if (!isCreating)
        {
            isCreating = true;  // this bool will set to false after draw the dimension.
            SelectionList.Clear(); // deselect selected dimensions
            Funcs.UpdateAll(this, DimensionsList, SelectionList);
            GameObject EzPointToPointDimensionGO = new GameObject("EzPointToPointDimension");
            EzPointToPointDimensionGO.transform.parent = this.transform;
            var p2PDim = EzPointToPointDimensionGO.AddComponent<PointToPointDimension>();

            if (createDimensionCort != null)
                StopCoroutine(createDimensionCort);

            createDimensionCort = StartCoroutine(CreatePointToPointDimension(p2PDim));

            DimensionsList.Add(EzPointToPointDimensionGO.gameObject); // add the parent GO to the list.
        }
    }
 
 ````
 
 At the beginning it checkes that isCreating bool is off to avoid duplicate of creation process. Then it will turn on isCreating and it will deselect the selected dimensions by clearing the “selectionList” list. Then it call the “updateAll” function from “EzDimFunctions” to update dimensions color based on new cleared “selectionList”. Now everything is ready to create a gameObject as child of this gameObject to add “pointToPointDimension” component. No the code will loop inside the “IEnumerator CreatePointToPointDimension” while added “pointToPointDimension” component “isDone” bool is not true. This Boolean will true at the end of this IEnumerator. When this part passed, the new dimension will add to “dimensionsList” list as a new dimension.
 
 Lets check what is inside the “IEnumerator CreatePointToPointDimension” :
 
 ```C#
     IEnumerator CreatePointToPointDimension(PointToPointDimension _p2PDim)
    {
        bool secondDrawStep = false;
        Vector2 p0MousePosOnScreen = Vector2.zero;

        while (_p2PDim.isDone != true)
        {
            if (Mouse.current.leftButton.wasPressedThisFrame && !secondDrawStep && !_p2PDim.isDone && isCreating == true)
            {
                p0MousePosOnScreen = Mouse.current.position.ReadValue();
                RaycastHit hit;
                Ray ray = rendererCamera.gameObject.GetComponent<Camera>().ScreenPointToRay(Mouse.current.position.ReadValue());
                if (Physics.Raycast(ray, out hit, Mathf.Infinity))
                {
                    _p2PDim.firstPointHitNormal = hit.normal;
                    _p2PDim.pointA = hit.point;
                    _p2PDim.objectA = hit.transform.gameObject;
                    _p2PDim.objectATransformGO.transform.position = hit.transform.position;
                    _p2PDim.objectATransformGO.transform.rotation = hit.transform.rotation;
                    _p2PDim.objectATransformGO.transform.localScale = hit.transform.localScale;
                    _p2PDim.pointATransformGO.transform.position = _p2PDim.pointA;

                    if (!hit.transform.gameObject.TryGetComponent<EzDynamicTargetObject>(out EzDynamicTargetObject EzDynamicTarget))
                    {
                        hit.transform.gameObject.AddComponent<EzDynamicTargetObject>().p2PDimComponentsList.Add(_p2PDim);
                        hit.transform.gameObject.GetComponent<EzDynamicTargetObject>().starterScript = this;
                    }
                    else
                    {
                        var p2PDimComp = hit.transform.gameObject.GetComponent<EzDynamicTargetObject>();
                        p2PDimComp.p2PDimComponentsList.Add(_p2PDim);
                    }

                    secondDrawStep = true;
                }
            }
            else if (secondDrawStep && p0MousePosOnScreen != Mouse.current.position.ReadValue())
            {
                Funcs.SetActiveAllChilds(_p2PDim.gameObject.transform, true);
                RaycastHit hit;
                Ray ray = rendererCamera.gameObject.GetComponent<Camera>().ScreenPointToRay(Mouse.current.position.ReadValue());

                if (Physics.Raycast(ray, out hit, Mathf.Infinity))
                {
                    _p2PDim.pointB = hit.point;
                    _p2PDim.objectB = hit.transform.gameObject;
                    _p2PDim.objectBTransformGO.transform.position = hit.transform.position;
                    _p2PDim.objectBTransformGO.transform.rotation = hit.transform.rotation;
                    _p2PDim.objectBTransformGO.transform.localScale = hit.transform.localScale;
                    _p2PDim.pointBTransformGO.transform.position = _p2PDim.pointB;

                    _p2PDim.UpdateDimension(_p2PDim.pointA, _p2PDim.pointB, _p2PDim.lineThickness, _p2PDim.textSize, _p2PDim.textOffset,
                        _p2PDim.numberColor, _p2PDim.mainColor, _p2PDim.arrowColor,
                        _p2PDim.mainLineMat, _p2PDim.arrowMat, _p2PDim.cameraTransform, _p2PDim.mainParent, _p2PDim.arrowHeight,
                        InternalFunctions.LengthUnitCalculator(this), textTowardsCameraOffset, hitNormalOffset);

                    if (Mouse.current.leftButton.wasPressedThisFrame && secondDrawStep)
                    {
                        if (!hit.transform.gameObject.TryGetComponent<EzDynamicTargetObject>(out EzDynamicTargetObject EzDynamicTarget))
                        {
                            hit.transform.gameObject.AddComponent<EzDynamicTargetObject>().p2PDimComponentsList.Add(_p2PDim);
                            hit.transform.gameObject.GetComponent<EzDynamicTargetObject>().starterScript = this;
                        }
                        else
                        {
                            var p2PDimComp = hit.transform.gameObject.GetComponent<EzDynamicTargetObject>();
                            p2PDimComp.p2PDimComponentsList.Add(_p2PDim);
                        }

                        secondDrawStep = false;
                        _p2PDim.isDone = true;
                        isCreating = false; // end of drawing of the dimension.
                    }
                }
            }

            yield return null;
        }

    }

 ```
 
 Inside the IEnumerator there is some steps that passed after each mouse click. by the first click a ``` rayCast ``` will get the first ``` hitPoint ``` and ```hit.transform.gameObject ``` and the first point will, then the script unhides every parts of the dimension by running ``` Funcs.SetActiveAllChilds() ``` function from ```EzDimension``` name space inside ``` EzDimFunctions ``` component. now it's time to define the second point by moving the mouse and hit the second click.
 After pressing the second click now every frame ``` rayCast``` of ``` Camera.ScreenPointToRay(Mouse.current.position.ReadValue())``` defines the secound point of dimension and ``` UpdateDimension ``` function from added ``` pointToPointDimension ``` component will run every frame to update the dimension based on second point that update each frame depends on mouse position. after the second click ``` isDone ``` boolean inside the added ``` pointToPointDimension ``` will set to true and ``` isCreating ``` boolean inside the ``` EzDimStarter ``` sets to false. that means the end of creation.
 
 this process has the same logic for all of dimensions. ``` EzDimStarter ``` always Create a set of ```gameObjects``` and add the Dimension Component on their parents, it get and set required position from mouse input and update the dimension untill creation process ended. consider that Create and Update dimension are inside the dimension components(pointToPointDimension.cs). create function calls just once because it's at the start void of dimension component.
 
 ```C#
 
     void Start()
    {
        CreateDimension(mainParent, arrowPrefab);
        Funcs.SetActiveAllChilds(this.transform, false);
    }
    
```

As mensioned before in addition to ``` CreateDimension() ```  there is an ``` UpdateDimension ``` void inside all of dimensions components. these two voids are in all types of dimensions except area measure. and there is another void named ``` UpdateTextTransform ``` in **pointToPointDimension.cs**, **LinearDimension.cs** and **AlignedDimension.cs**. the **AngleDimension.cs** is quite similar but instead of ``` UpdateTextTransform ``` there is a voide named ``` UpdateTextAndIndicator ``` .the **LinearAreaMeasure.cs** works a bit diffrent and there is no ``` CreateDimension``` and ``` Start() ``` and ``` Update ``` void. instead of those, required gameObjects creating in ``` Awake() ``` void and we have five other voide named ``` UpdatePointsList() ```, ``` UpdateBorderLine() ```, ``` DrawArea() ```, ``` UpdateAreaNumber ``` and ``` UpdateNumberPositionAndRotation ```. 

Another component that contained most of functions is ``` EzDimFunctions.cs ```. all of the functions inside this component are under the **EzDimension** namespace.that means all of other components that using any functions need to indcloud ``` using EzDimension ``` .

There is more specific details in [**Scripting API**](#ScriptingAPI) section.
 
<br/><br/>

<a name="VRSetting">
  </a>

# Using EzDimension in VR :

<br/>

![FlowChart_VR](https://user-images.githubusercontent.com/88411269/218101925-17dd1bf1-86c5-4565-b7af-bd6e18f5ee11.png)

To use VR first you can download **VR Sample Script** from package manager to see how you should setUp the **Easy Dimension Measurement System** for VR.this script is fully compatible with **XR Interaction Toolkit 2.2.0**.because there is various VR integration package we won't incloud the VR scene inside the package to avoid any conflict and messy errors in your scene.instead of this we will look at the main logic of using **Easy Dimension** inside your VR scene.

If you go back to the [**Quick Start**](#QuickStart) section and look at the inspector when **StarterGO** is selected, you can see that the first field is **Draw In Vr Comp**. so please add the **DrawInVR.cs** on the **StarterGO** and drag and drop **StarterGO** inside the **Draw In Vr Comp** section. 

<br/>

There is some difference between **Mouse Input** and **VR Input**. As We explained in the [**Scripting Manual**](#ScriptingManual) section, when using the **Mouse Input** we have some draw step for every dimensions and each step will pass after mouse click. we used ``` Camera.ScreenPointToRay(Mouse.current.position.ReadValue()) ``` to catch ``` raycastHit ``` . when using VR obviously can't use ``` ScreenPointToRay() ```, mouse position and click to pass draw steps. instead of thouse we should use ``` bool ray = rayInteractor.TryGetCurrent3DRaycastHit(out hit) ``` to catch our hit and instead of mouse click we need to have some boolean that turns true after each desiered button pressed. As you can guess, we need to get one of our ** ray interactors** from one hand and feed it to the **DrawInVR.rayInteractor**.<br/>

<img src="https://user-images.githubusercontent.com/88411269/218111506-6520f279-2f57-46c8-a271-a3ce448310cc.jpg" width="500">

<br/>

<br/>

> **Note** <br/>
> **DrawInVR.cs** works dependently with **EzDimStarter** component. they should add on the same gameObject that we called it **StarterGO** and you need to drag and drop **StarterGO** inside the **Draw In Vr Comp** field.

<br/><br/>

Let's have one example to make sure everything is clear. if you download the **DrawInVR.cs** sample from package manager and open it you can see there is some public void like what we had inside the **EzDimStarter**. 

```C#

    public void VR_EzPointToPointDimension(EzDimStarter _starterScript)
    {
        if (!_starterScript.isCreating)
        {
            firstStep = true;
            secoundStep = thirdStep = fourthStep = fifthStep = sixthStep = false;
            _starterScript.isCreating = true;  // this bool will set to false after draw the dimension.
            _starterScript.SelectionList.Clear();
            Funcs.UpdateAll(_starterScript, _starterScript.DimensionsList, _starterScript.SelectionList);
            GameObject EzPointToPointDimensionGO = new GameObject("VR_EzPointToPointDimension");
            EzPointToPointDimensionGO.transform.parent = _starterScript.transform;
            var p2PDim = EzPointToPointDimensionGO.AddComponent<PointToPointDimension>();

            if (_starterScript.createDimensionCort != null)
                StopCoroutine(_starterScript.createDimensionCort);

            _starterScript.createDimensionCort = StartCoroutine(CreatePointToPointDimension(_starterScript, p2PDim));

            _starterScript.DimensionsList.Add(EzPointToPointDimensionGO.gameObject); // add the parent GO to the list.
        }
    }
    
```

<br/>

it's quite similar than what we did before. note that we didn't have a separate dimension list and we still send some data to the **Starter Script**.

the creation process happends inside the ``` IEnumerator CreatePointToPointDimension() ```. it's quite similar to what we did before when using mouse input too.

<br/>

```C#

    IEnumerator CreatePointToPointDimension(EzDimStarter _starterScript, PointToPointDimension _p2PDim)
    {
        _p2PDim.secondDrawStep = false;

        while (_p2PDim.isDone != true)
        {
            if (firstStep && secoundStep && !thirdStep && !_p2PDim.secondDrawStep && _starterScript.isCreating)
            {
                RaycastHit hit;
                bool ray = rayInteractor.TryGetCurrent3DRaycastHit(out hit);
                if (ray)
                {
                    _p2PDim.pointA = hit.point;
                    _p2PDim.objectA = hit.transform.gameObject;
                    _p2PDim.objectATransformGO.transform.position = hit.transform.position;
                    _p2PDim.objectATransformGO.transform.rotation = hit.transform.rotation;
                    _p2PDim.objectATransformGO.transform.localScale = hit.transform.localScale;
                    _p2PDim.pointATransformGO.transform.position = _p2PDim.pointA;

                    if (!hit.transform.gameObject.TryGetComponent<EzDynamicTargetObject>(out EzDynamicTargetObject EzDynamicTarget))
                    {
                        hit.transform.gameObject.AddComponent<EzDynamicTargetObject>().p2PDimComponentsList.Add(_p2PDim);
                        hit.transform.gameObject.GetComponent<EzDynamicTargetObject>().starterScript = _starterScript;
                    }
                    else
                    {
                        var p2PDimComp = hit.transform.gameObject.GetComponent<EzDynamicTargetObject>();
                        p2PDimComp.p2PDimComponentsList.Add(_p2PDim);
                    }

                    _p2PDim.secondDrawStep = true;
                }

            }
            else if (_p2PDim.secondDrawStep == true)
            {
                Funcs.SetActiveAllChilds(_p2PDim.gameObject.transform, true);

                RaycastHit hit;
                bool ray = rayInteractor.TryGetCurrent3DRaycastHit(out hit);
                if (ray)
                {
                    _p2PDim.pointB = hit.point;
                    _p2PDim.objectB = hit.transform.gameObject;
                    _p2PDim.objectBTransformGO.transform.position = hit.transform.position;
                    _p2PDim.objectBTransformGO.transform.rotation = hit.transform.rotation;
                    _p2PDim.objectBTransformGO.transform.localScale = hit.transform.localScale;
                    _p2PDim.pointBTransformGO.transform.position = _p2PDim.pointB;

                    _p2PDim.UpdateDimension(_p2PDim.pointA, _p2PDim.pointB, _p2PDim.lineThickness, _p2PDim.textSize, _p2PDim.textOffset,
                        _p2PDim.numberColor, _p2PDim.mainColor, _p2PDim.arrowColor,
                        _p2PDim.mainLineMat, _p2PDim.arrowMat, _p2PDim.cameraTransform, _p2PDim.mainParent, _p2PDim.arrowHeight,
                        InternalFunctions.LengthUnitCalculator(_starterScript), _p2PDim.textTowardsCameraOffset, _p2PDim.NormalOffset);

                    if (firstStep && secoundStep && thirdStep)
                    {
                        if (!hit.transform.gameObject.TryGetComponent<EzDynamicTargetObject>(out EzDynamicTargetObject EzDynamicTarget))
                        {
                            hit.transform.gameObject.AddComponent<EzDynamicTargetObject>().p2PDimComponentsList.Add(_p2PDim);
                            hit.transform.gameObject.GetComponent<EzDynamicTargetObject>().starterScript = _starterScript;
                        }
                        else
                        {
                            var p2PDimComp = hit.transform.gameObject.GetComponent<EzDynamicTargetObject>();
                            p2PDimComp.p2PDimComponentsList.Add(_p2PDim);
                        }
                        _starterScript.isCreating = false; // end of drawing of the dimension.
                        _p2PDim.secondDrawStep = false;
                        _p2PDim.isDone = true;
                    }
                }
            }
            yield return null;
        }
    }

```
the only diffrences are condition of going to the next step and how we get the ``` raycastHit ```. other steps are almost similar than what we did with mouse input.


 --- 
 
<br/><br/>







<a name="GeneralReferences">
  </a>

# General References :
  
  
  


<br/>

 --- 
 
<br/><br/>








<a name="ScriptingAPI">
  </a>

# Scripting API :

## Point To Point Dimension :

<br/>

|    Name               |Type        |      Description                                  |
|:----------------------|:-----------|:--------------------------------------------------|
|valuesReference        |EzDimStarter|Global parameters reference. |
|isIndividual           |Bool        |Allow dimension to have local attributes |
|isDynamic              |Bool        |Make dimension dynamic. If target objects moving, the dimension will update it's length |
|lineThickness          |Float       |Thickness of the line |
|arrowHeight            |Float       |Arrow prefab's scale |
|textSize               |Float       |TextMesh font size |
|NormalOffset           |Float       |Offset dimension along normal of first hitPoint to avoid Z-Fighting  |
|textTowardsCameraOffset|Float       |Offset dimension towards camera to avoid masking or intersection with other objects in the scene |
|textOffset             |Float       |Offset number's textMesh to it's local Y axis. it control the distance between number and line |
|numberColor            |Color       |Color of number's textMesh |
|mainColor              |Color       |Color of line material. other material features can control by a costum script |
|arrowColor             |Color       |Color of arrow material. other material features can control by a costum script |
|hoveredTint            |Color       |This color multiplies to other colors if we hovered on any dimension when using mouse or VR|
|selectedTint           |Color       |Color of selected dimensions |
|hoveredOnSelectedTint  |Color       |Color of selected dimension when we hovered on it when using mouse or VR |
|mainLineMat            |Material    |Material of line |
|arrowMat               |Material    |Material of arrows |
|arrowPrefab            |GameObject  |Prefab contain the arrow object.pivot should set to the center of it's base |
|cameraTransform        |Transform   |Transform of camera,Normally equal to rendererCamera |
|rendererCamera         |Camera      |Camera Component of our renderer camera.Normally equal to cameraTransform |
|mainParent             |GameObject  |Dimension main parent |
|pointA                 |Vector3     |Initial Position of the first hitPoint |
|pointB                 |Vector3     |Initial Position of the second hitPoint |
|secondDrawStep         |Bool        |This bool turns true after first click in creation process and always remain true |
|isDone                 |Bool        |This bool turns true at the end of creation process |
|firstPointHitNormal    |Vector3     |Normal of first hitPoint |
|objectATransformGO     |GameObject  |GameObject at the Position of first hitObject's center |
|objectBTransformGO     |GameObject  |GameObject at the Position of second hitObject's center |
|pointATransformGO      |GameObject  |GameObject at the position of first hitPoint |
|pointBTransformGO      |GameObject  |GameObject at the position of second hitPoint |
|objectA                |GameObject  |First hitObject |
|objectB                |GameObject  |Second hitObject |
|CreateDimension()      |Method      |This void creates the dimension's parts |
|UpdateDimension()      |Method      |This void updates the dimension's main features |
|UpdateTextTransform()  |Method      |This void updates the dimension's text transform |    


<br/><br/>





## Linear Dimension :
 
<br/>

|Name                   |Type                      |Description                            |
|-----------------------|--------------------------|---------------------------------------|
|valuesReference        |EzDimStarter              |Global parameters reference |
|measurementDirection   |Funcs.MeasurementDirection|Measure the distance on this specific axis |
|offsetDirection        |Funcs.OffsetDirection     |Offset mainLine in this direction |
|offsetDistance         |float                     |Distance between mainLine from the first hitPoint |
|isIndividual           |bool                      |Allow dimension to have local attributes |
|isDynamic              |bool                      |Make dimension dynamic. If target objects moving, the dimension will update it's length |
|mainLineThickness      |float                     |Thickness of the mainLine |
|arrowHeight            |float                     |Arrow prefab's scale |
|textSize               |float                     |TextMesh font size |
|NormalOffset           |float                     |Offset dimension along normal of first hitPoint to avoid Z-Fighting |
|textTowardsCameraOffset|float                     |Offset dimension towards camera to avoid masking or intersection with other objects in the scene |
|textOffset             |float                     |Offset number's textMesh to it's local Y axis. it control the distance between number and mainLine |
|secondaryLinesThickness|float                     |Thickness of the sedondary lines |
|secondaryLinesExtend   |float                     |Length of secondary lines extend |
|autoTextPosition       |bool                      |change text and arrows position if text's width and arrows height was bigger than distance of measured points |
|flipTextPosition       |bool                      |flip position when autoTextPosition affected the dimension text and arrows position |
|numberColor            |Color                     |Color of number's textMesh |
|mainColor              |Color                     |Color of mainLine material. other material features can control by a costum script |
|secondaryColor         |Color                     |Color of secondaryLine material. other material features can control by a costum script |
|arrowColor             |Color                     |Color of arrow material. other material features can control by a costum script |
|hoveredTint            |Color                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|selectedTint           |Color                     |Color of selected dimensions |
|hoveredOnSelectedTint  |Color                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|mainLineMat            |Material                  |Material of mainLine |
|secondaryLinesMat      |Material                  |Material of secondaryLine |
|arrowMat               |Material                  |Material of arrows |
|arrowPrefab            |GameObject                |Prefab contain the arrow object.pivot should set to the center of it's base |
|cameraTransform        |Transform                 |Transform of camera |
|mainParent             |GameObject                |Dimension main parent |
|pointA                 |Vector3                   |Initial Position of the first hitPoint |
|pointB                 |Vector3                   |Initial Position of the second hitPoint |
|isDone                 |bool                      |This bool turns true at the end of creation process |
|firstPointHitNormal    |Vector3                   |Normal of first hitPoint |
|objectATransformGO     |GameObject                |GameObject at the Position of first hitObject's center |
|objectBTransformGO     |GameObject                |GameObject at the Position of second hitObject's center |
|pointATransformGO      |GameObject                |GameObject at the position of first hitPoint |
|pointBTransformGO      |GameObject                |GameObject at the position of second hitPoint |
|objectA                |GameObject                |First hitObject |
|objectB                |GameObject                |Second hitObject |
|CreateDimension()      |Method                    |This void creates the dimension's parts |
|UpdateDimension()      |Method                    |This void updates the dimension's main features |
|UpdateTextTransform()  |Method                    |This void updates the dimension's text transform |  




<br/><br/>





## Aligned Dimension :

<br/>

|Name                    |Type                      |Description                            |
|------------------------|--------------------------|---------------------------------------|
|valuesReference         |EzDimStarter              |Global parameters reference  |
|measurementPlane        |Funcs.MeasurementPlane    |Measure the distance on this specific plane |
|offsetDistance          |float                     |Distance between mainLine from the first hitPoint |
|reverseDirection        |bool                      |Multiply offset distance to -1 |
|isIndividual            |bool                      |Allow dimension to have local attributes |
|isDynamic               |bool                      |Make dimension dynamic. If target objects moving, the dimension will update it's length |
|mainLineThickness       |float                     |Thickness of the mainLine |
|arrowHeight             |float                     |Arrow prefab's scale |
|textSize                |float                     |TextMesh font size |
|NormalOffset            |float                     |Offset dimension along normal of first hitPoint to avoid Z-Fighting |
|textTowardsCameraOffset |float                     |Offset dimension towards camera to avoid masking or intersection with other objects in the scene |
|textOffset              |float                     |Offset number's textMesh to it's local Y axis. it control the distance between number and mainLine |
|secondaryLinesThickness |float                     |Thickness of the sedondary lines |
|secondaryLinesExtend    |float                     |Length of secondary lines extend |
|DirectionPointInFreeMode|Vector3                   |Position of direction point when draw in free mode |
|autoTextPosition        |bool                      |change text and arrows position if text's width and arrows height was bigger than distance of measured points |
|flipTextPosition        |bool                      |flip position when autoTextPosition affected the dimension text and arrows position |
|numberColor             |Color                     |Color of number's textMesh |
|mainColor               |Color                     |Color of mainLine material. other material features can control by a costum script |
|secondaryColor          |Color                     |Color of secondaryLine material. other material features can control by a costum script |
|arrowColor              |Color                     |Color of arrow material. other material features can control by a costum script |
|hoveredTint             |Color                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|selectedTint            |Color                     |Color of selected dimensions |
|hoveredOnSelectedTint   |Color                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|mainLineMat             |Material                  |Material of mainLine |
|secondaryLinesMat       |Material                  |Material of secondaryLine |
|arrowMat                |Material                  |Material of arrows |
|arrowPrefab             |GameObject                |Prefab contain the arrow object.pivot should set to the center of it's base |
|mainParent              |GameObject                |Dimension main parent |
|cameraTransform         |Transform                 |Transform of camera |
|firstPointHitNormal     |Vector3                   |Normal of first hitPoint |
|pointA                  |Vector3                   |Initial Position of the first hitPoint |
|pointB                  |Vector3                   |Initial Position of the second hitPoint |
|secondDrawStep          |bool                      |This bool turns true after first click in creation process and always remain true |
|isDone                  |bool                      |This bool turns true at the end of creation process |
|objectATransformGO      |GameObject                |GameObject at the Position of first hitObject's center |
|objectBTransformGO      |GameObject                |GameObject at the Position of second hitObject's center |
|pointATransformGO       |GameObject                |GameObject at the position of first hitPoint |
|pointBTransformGO       |GameObject                |GameObject at the position of second hitPoint |
|objectA                 |GameObject                |First hitObject |
|objectB                 |GameObject                |Second hitObject |
|CreateDimension()       |Method                    |This void creates the dimension's parts |
|UpdateDimension()       |Method                    |This void updates the dimension's main features |
|UpdateTextTransform()   |Method                    |This void updates the dimension's text transform |  


<br/><br/>






## Angle Dimension :

<br/>

|Name                    |Type                      |Description                            |
|------------------------|--------------------------|---------------------------------------|
|valuesReference         |EzDimStarter              |Global parameters reference  |
|angleMeasurementPlane   |Funcs.AngleMeasurmentPlane|Measure the distance on this specific plane |
|rotateTextBy180         |bool                      |Rotate text on the normal of angle measurement plane by 180 degree|
|reverseTextPosIfNotFit  |bool                      |Change not fitted text to other side |
|isIndividual            |bool                      |Allow dimension to have local attributes |
|isDynamic               |bool                      |Make dimension dynamic. If target objects moving, the dimension will update it's length |
|linesThickness          |float                     |Thickness of the lines |
|textSize                |float                     |TextMesh font size |
|arcScale                |float                     |Scale of the arc plane object |
|textOffsetFromCenter    |float                     |Offset number's textMesh from center of the angle |
|NormalOffset            |float                     |Offset dimension along normal of first hitPoint to avoid Z-Fighting |
|textOffsetIfNotFit      |Vector2                   |Offset to new position of the text in the angleMeasurementPlane if it was not fit |
|numberColor             |Color                     |Color of number's textMesh |
|mainColor               |Color                     |Color of the lines. other material features can control by a costum script |
|arcColor                |Color                     |Color of arc material. other material features can control by a costum script |
|hoveredTint             |Color                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|selectedTint            |Color                     |Color of selected dimensions |
|hoveredOnSelectedTint   |Color                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|mainLinesMat            |Material                  |Material of lines |
|arcMat                  |Material                  |Material of arc plane |
|pointA                  |Vector3                   |Initial Position of the first hitPoint |
|pointB                  |Vector3                   |Initial Position of the second hitPoint |
|pointC                  |Vector3                   |Initial Position of the third hitPoint |
|mainParent              |GameObject                |Dimension main parent |
|cameraTransform         |Transform                 |Transform of camera |
|trueOnFirstStep         |Bool                      |This bool turns true after first click in creation process and always remain true |
|trueOnSecoundStep       |Bool                      |This bool turns true after second click in creation process and always remain true |
|isDone                  |Bool                      |This bool turns true at the end of creation process |
|lineAGO                 |GameObject                |Line A ``` gameObject ```|
|lineBGO                 |GameObject                |Line B ``` gameObject ```|
|pointBProxy             |Vector3                   |Projected pointB to the angleMeasurementPlane with the same local height of pointA |
|pointCProxy             |Vector3                   |Projected pointC to the angleMeasurementPlane with the same local height of pointA |
|arcParentGO             |GameObject                |Parent of the arc plane ``` gameObject ``` |
|plane                   |Plane                     |Intersected plane by pointA, pointB and pointC |
|numberGO                |GameObject                |Number ``` gameObject ``` |
|objectATransformGO      |GameObject                |GameObject at the Position of first hitObject's center |
|objectBTransformGO      |GameObject                |GameObject at the Position of second hitObject's center |
|objectCTransformGO      |GameObject                |GameObject at the Position of third hitObject's center |
|pointATransformGO       |GameObject                |GameObject at the position of first hitPoint |
|pointBTransformGO       |GameObject                |GameObject at the position of second hitPoint |
|pointBTransformGO       |GameObject                |GameObject at the position of third hitPoint |
|objectA                 |GameObject                |First hitObject |
|objectB                 |GameObject                |Second hitObject |
|objectC                 |GameObject                |third hitObject |
|CreateDimension()       |Method                    |This void creates the dimension's parts |
|UpdateDimension()       |Method                    |This void updates the dimension's main features |
|UpdateTextAndIndicator()|Method                    |This void updates the dimension's text transform and ``` Angle``` parameter of arc material|  




<br/><br/>






## Area Measure :

<br/>

|Name                    |Type                      |Description                            |
|------------------------|--------------------------|---------------------------------------|
|valuesReference         |EzDimStarter              |Global parameters reference  |
|cameraBaseNumberInXYDir |bool                      |Update text rotation based on camera position |
|rotateText180LocalY     |bool                      |flip text in local Y |
|rotateText180LocalZ     |bool                      |flip text in local Z  |
|rotateText180LocalX     |bool                      |flip text in local X  |
|isIndividual            |bool                      |Allow dimension to have local attributes |
|textSize                |float                     |TextMesh font size |
|localYOffset            |float                     |Push the dimension in local Y direction to avoid Z-fighting with the underlying surface |
|textLocalYOffset        |float                     |Push the text in it's local Y direction to avoid Z-fighting with the area highlighting plane |
|borderLocalYOffset      |float                     |Push the border in local Y direction to avoid Z-fighting with the area highlighting plane |
|borderThickness         |float                     |Thickness of the border line |
|positionOffset          |Vector2                   |2d offset of the number in the surface |
|enableBorderLine        |bool                      |Show line around measured area |
|numberColor             |Color                     |Color of number's textMesh |
|borderColor             |Color                     |Color of border material. other material features can control by a costum script |
|surfaceColor            |Color                     |Color of surface material. other material features can control by a costum script |
|hoveredTint             |Color                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|selectedTint            |Color                     |Color of selected dimensions |
|hoveredOnSelectedTint   |Color                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|surfaceMaterial         |Material                  |Material of area highlighting plane |
|BorderMaterial          |Material                  |Material of area border |
|handlesParent           |GameObject                |Parent ``` gameObject ``` of area corners object
|cameraTransform         |Transform                 |Transform of camera |
|points                  |List\<Vector2>            |List of area corners in a 2d plane|
|handlesList             |List\<GameObject>         |List of area corners object |
|area                    |float                     |Calculated area stores in this float |
|borderLineGO            |GameObject                |Border line ``` gameObject ``` |
|borderLine              |LineRenderer              | ``` LineRenderer ``` component to draw borderLine|
|meshCenter              |Vector3                   |Center of the measured area |
|allowDrawSurface        |bool                      |Allow to update surface when corne's handles position are changing |
|hitNormal               |Vector3                   |Get the normal of the surface to avoid flip normal using EzdimFunctions.InternalFunctions.FlipNormal() |
|measurementPlane        |Funcs.MeasurementPlane    |Measure the area on this specific plane |
|isDone                  |bool                      |This bool turns true at the end of creation process |
|drawMode                |bool                      |This bool turns true at the end of creation process |
|updatePointsList()      |Method	                |Get the ``` List<Vector2> ``` of area corners position on 2d plane and rearrange them based on measurement plane |
|UpdateBorderLine()      |Method                    |Update border line based on measurement plane and points position |
|DrawArea()              |Method                    |Draw, update and triangulate the highlighting plane mesh |
|UpdateNumberPosAndRot() |Method                    |Update area number position and rotation |



  
<br/><br/>






## EzDimFunctions :

<br/>

|Name                    |Type                      |Description                            |
|------------------------|--------------------------|---------------------------------------|
|Funcs                   |Class                     |Contain the main functions |
|InternalFunctions       |Class                     |Contain the side functions that are not using frequently |
|MeasurementDirection    |enum                      |Main axis {X, Y, Z} |
|OffsetDirection         |enum                      |Main axis {X, Y, Z} |
|MeasurementPlane        |enum                      |Main planes  { XZ, XY, ZY, Free } |
|AngleMeasurmentPlane    |enum                      |Main planes  { XZ, XY, ZY, Free } |
|MeasurmentType          |enum                      |Main measurement types { Length, Area, Volume } |
|UpdateArea              |static void               |Update area measure |
|UpdateAngle             |static void               |Update angle dimension |
|UpdateLength            |static void               |Update the length of pointToPoint Dimension. using this when the start or end point position has changed |
|UpdateLength            |static void               |Update the length of Linear Dimension |
|UpdateLength            |static void               |Update the length of Aligned Dimension |
|UpdateAll               |static void               |Update all dimensions main features |
|UpdateValues            |static void               |Update all dimensions main features (depricated) |
|UpdateNumbersRotation   |static void               |Update all numbers rotation |
|SelectDimension         |static void               |Add hitObject to selection List |
|HighlightSelectedDims   |static void               |Highlight available dimensions in selection list and de-emphasize the deselected dimensions |
|IsHoveredOnDimension    |static void               |Manage highlighting and de-emphasizeing hovered dimensions |
|SetActiveAllChilds      |static void               |Activate all children of given ``` gameObject ``` |
|HideSelectedDimensions  |static void               |Hide selected Dimension |
|UnhideAllDimensions     |static void               |Unhide all dimensions inside a given starter script and dimension list |
|DeleteDimensions        |static void               |Delete selected dimensions |
|Units                   |enum                      |Measurement units { Millimetre, centimeter, meter, inch, foot, yard, custom } |
|numberOfDecimal         |enum                      |Number of decimals { none, one, two, three, four, five, six } |
|LengthUnitCalculator    |static float              |Return the multiplier of diffrent units for length |
|AreaUnitCalculator      |static float              |Returns the multiplier of diffrent units for area |
|DecimalCalculator       |static string             |Returns the decimal number for diffrent decimal numbers |
|GetUnitTextShortForm    |static string             |Returns the short form of the units text |
|AngleBisectorPoint      |static Vector3            |Calculate the bisector of three points |
|HighlightColor          |static Color              |Highlight a color with given percentage |
|Remap                   |static float              |Remap a value from one range to another range |
|FlipNormal              |static bool               |Custom function to calculate area surface normal to avoid reversed normal |
|TriangulatePoints       |static mesh               |Return triangulate mesh from given vector2 array of points |


<br/><br/>



  
## EzDynamicTargetObject

<br/>

This component will add to all target objects. if any transform change happends and dimension's ``` isDynamic ``` option was true, this component call ``` updateLength() ``` function for the related dimension. 

<br/>

|Name                    |Type                        |Description                            |
|------------------------|----------------------------|---------------------------------------|
|starterScript           |EzDimStarter                |EzDimStarter component that created dimension on this target object |
|areaMeasureRoot         |LinearAreaMeasure           |``` LinearAreaMeasure ``` component (if exist) |
|p2PDimComponentsList    |List\<PointToPointDimension>|List of ```PointToPointDimension ``` components (if exist) |
|linDimComponentsList    |List\<LinearDimension>      |List of ```LinearDimension ``` components (if exist) |
|alignDimComponentsList  |List\<AlignedDimension>     |List of ```AlignedDimension ``` components (if exist) |
|angleDimComponentsList  |List\<AngleDimension>       |List of ```AngleDimension ``` components (if exist) |





<br/><br/>





## EzDimStarter :

<br/>

|Name                         |Type                         |Description                            |
|-----------------------------|-----------------------------|---------------------------------------|
|drawInVrComp                 |Component                    |VR Component ( Null = Use Mouse Input ) |
|unit                         |InternalFunctions.Units      |Unit’s Enum { Millimetre, centimeter, meter, inch, foot, yard, custom } |
|customUnitMultiplier         |float                        |If Unit = Custom, this number will multipliy to default unit |
|customUnitName               |string                       |If Unit = Custom, Name of custom unit |
|showUnitAfterNumber          |bool                         |Show short form of the unit name after dimension’s number in runtime |
|numberOfDecimal              |internalFuncs.numberOfDecimal|Decimal Enum { none, one, two, three, four, five, six } |
|cameraTransform              |Transform                    |Camera based texts using this transform |
|rendererCamera               |Camera                       |RayCasts using this camera (normally its same as camera transform) |
|mainLineMaterial             |Material                     |Material of the “mainLine” (line between two arrows in dimensions) |
|secondaryLinesMaterial       |Material                     |Material of secondary lines in “Linear” and “Aligned” dimensions |
|arrowMaterial                |Material                     |Material of Arrows in “PointToPoint”, “Linear” and “Aligned” dimensions |
|arcMaterial                  |Material                     |Material of indicator arc of “Angle” dimension |
|areaSurfaceMaterial          |Material                     |Material of “Area” measure’s surface |
|areaBorderMaterial           |Material                     |Material of “Area” measure’s border |
|arrowPrefab                  |GameObject                   |Arrow Prefab for “PointToPoint”, “Linear” & “Aligned” dimensions |
|areaHandlesPrefab            |GameObject                   |It will attach to every corners of “Area” measure |
|alignedDimFreeModeDirPointer |GameObject                   |Direction pointer object appears when creating free “aligned” dimension |
|alignedDimFreeModePlanePrefab|GameObject                   |Direction plane object appears when creating free “aligned” dimension |
|planePrefabScaleMultiplier   |float                        |Scale direction plane to mouse position multiplier. Zero = turnOf |
|areaHandlesScale             |float                        |Scale of ``` areaHandlesPrefab ``` |
|pointerScale                 |float                        |Scale of ``` alignedDimFreeModeDirPointer ``` |
|isDynamic                    |bool                         |If true, start and end of dimension will follow the “hit point” transform |
|linesThickness               |float                        |Thickness of the “mainLine”(line between two arrows) |
|textSize                     |float                        |The size of number’s text (it’s based on “textMeshPro” font size) |
|textOffset                   |float                        |Offset between “main line” and number’s text |
|arrowHeight                  |float                        |Coefficient of arrow size. final size depends on “arrowPrefab” scale |
|measurementDirection         |Funcs.MeasurementDirection   |Direction of “Linear” dimension (multiply direction to “offsetDistance”) |
|offsetDirection              |Funcs.OffsetDirection        |Direction of offset in the “Linear” dimension |
|measurementPlane             |Funcs.MeasurementPlane       |Measurement plane for “Aligned” dimensions - { XZ, XY, ZY, Free } |
|reverseDirection             |bool                         |Flip “Aligned” dimensions in cross vector of the measurement plane |
|offsetDistance               |float                        |Length of “secondary lines” |
|secondaryLinesThickness      |float                        |Thickness of “secondary lines” |
|secondaryLinesExtend         |float                        |Length of “extends” in secondary lines |
|autoTextPosition             |bool                         |Change number’s position if distance was too short and number can’t fit |
|flipTextPosition             |bool                         |If “AutoTextPosition” was true, mirror text position |
|angleMeasurmentPlane         |Funcs.AngleMeasurmentPlane   |Measurement plane of “Angle” dimension - { XZ, XY, ZY, Free } |
|arcScale                     |float                        |Scale of the plane that carries the dimension arc |
|angleDimTextOffsetFromCenter |float                        |Distance of number from the center of the angle dimension |
|angleDimHitNormalOffset      |float                        |Offset to normal direction of the first hit point to avoid ZFighting |
|textOffsetWhenNotFit         |Vector2                      |When angle is too short, this is offset of new position |
|areaMeasurementPlane         |Funcs.MeasurementPlane       |Measurement plane of “Area” measure - { XZ, XY, ZY, Free } |
|enableAreaBorderLine         |bool                         |Show border line |
|areaLocalYOffset             |float                        |Offset in local Y direction to avoid Z-fighting |
|areaTextLocalYOffset         |float                        |Space between number’s text and area surface |
|areaBorderLocalYOffset       |float                        |Space between border and area surface |
|areaBorderLineThickness      |float                        |Thickness of the border line mesh |
|areaNumberPositionOffset     |Vector2                      |2d offset of number position |
|numberColor                  |Color                        |Color of “textMeshPro” that generates the number |
|mainColor                    |Color                        |Color of line between arrows in “PointToPoint”, “Linear” & “Aligned” dims  |
|secondaryColor               |Color                        |Color of guiding lines of “Linear” & “Aligned” dimension |
|arrowColor                   |Color                        |Color of arrows in “PointToPoint”, “Linear” & “Aligned”  dimensions  |
|arcColor                     |Color                        |Color of indicator arc of “Angle” dimension |
|areaBorderColor              |Color                        |Color of border of “Area” measure |
|areaSurfaceColor             |Color                        |Color of surface of “Area” measure |
|hoveredTint                  |Color                        |Lerp this color to colors of “hovered” dimension |
|selectedTint                 |Color                        |Lerp this color to colors of “selected” dimensions |
|hoveredOnSelectedTint        |Color                        |Lerp this color to colors of “hovered dimensions” if it was selected |
|hitNormalOffset              |float                        |Offset to normal direction of first hit point to avoid ZFighting |
|textTowardsCameraOffset      |float                        |Offset the number towards the camera to avoid intersection |
|onSelectionChanged           |UnityEvent<List<GameObject>> |Events added here will trigger when selection changes (Mouse & VR) |
|onHovered                    |UnityEvent<GameObject>       |Events added here will trigger when hovers on a dimension (Mouse & VR) |
|pointA                       |Vector3                      |Initial Position of the first hitPoint |
|pointB                       |Vector3                      |Initial Position of the second hitPoin |
|isCreating                   |bool                         |This bool turns true while creation process otherwise is false |
|DimensionsList               |List\<GameObject>            |List of dimensions created from this ``` EzDimStarter ``` component |
|SelectionList                |List\<GameObject>            |List of selected dimensions that created from this ``` EzDimStarter ``` component |
|oldHoveredGo                 |GameObject                   |List hovered dimension |
|hit                          |RaycastHit                   |raycast hit (feed by mouse or VR) |
|isOldSelectionListEmpty      |bool                         |This bool returns true if selection list was empty |
|planePrefab                  |GameObject                   |Plane Prefab that shows when creating aligned dimension in free mode |
|createDimensionCort          |Coroutine                    |Coroutine for creation process |
|CreatePointToPointDimension()|IEnumerator                  |Using this part of code while creating ```PointToPointDimension ``` . |
|CreateLinearDimension()      |IEnumerator                  |Using this part of code while creating ```LinearDimension ``` . |
|CreateAlignedDimension()     |IEnumerator                  |Using this part of code while creating ```AlignedDimension ``` . |
|CreateAngleDimension()       |IEnumerator                  |Using this part of code while creating ```AngleDimension ``` . |
|CreateAreaMeasure()          |IEnumerator                  |Using this part of code while creating ```AreaMeasure  ``` . |
|EzPointToPointDimension()    |Method                       |Call this void to create ```PointToPointDimension ``` when using mouse input |
|EzLinearDimension()          |Method                       |Call this void to create ```LinearDimension ``` when using mouse input |
|EzAlignedDimension()         |Method                       |Call this void to create ```AlignedDimension ``` when using mouse input |
|EzAngledDimension()          |Method                       |Call this void to create ```AngleDimension ``` when using mouse input |
|EzAreaMeasure()              |Method                       |Call this void to create ```AreaMeasure ``` when using mouse input |
|HideSelectedDimensions()     |Method                       |Call this void to hide selected dimensions when using mouse or VR input |
|UnhideAll()                  |Method                       |Call this void to unhide all dimensions when using mouse or VR input |
|DeleteSelectedDimensions()   |Method                       |Call this void to delete selected dimensions when using mouse or VR input  |
|UpdateAll()                  |Method                       |Call this void to update all dimensions when using mouse or VR input |



  
<br/><br/>






## DrawInVR :

<br/>

|Name                          |Type                         |Description                            |
|------------------------------|-----------------------------|---------------------------------------|
|hoveredHit                    |RaycastHit                   |``` RaycastHit ``` from ``` XRRayInteractor ```. it should send to EzDimStarter.hit |
|rayInteractor                 |XRRayInteractor              |Feed this input field by ``` XRRayInteractor ``` from one of VR controller |
|primaryButtonPress            |PrimaryButtonEvent           |Event for primary button press |
|CreatePointToPointDimension() |IEnumerator                  |Using this part of code while creating ```PointToPointDimension ``` . |
|CreateLinearDimension()       |IEnumerator                  |Using this part of code while creating ```LinearDimension ``` . |
|CreateAlignedDimension()      |IEnumerator                  |Using this part of code while creating ```AlignedDimension ``` . |
|CreateAngleDimension()        |IEnumerator                  |Using this part of code while creating ```AngleDimension ``` . |
|CreateAreaMeasure()           |IEnumerator                  |Using this part of code while creating ```AreaMeasure  ``` . |
|VR_EzPointToPointDimension()  |Method                       |Call this void to create ```PointToPointDimension ``` when using VR input |
|VR_EzLinearDimension()        |Method                       |Call this void to create ```LinearDimension ``` when using VR input |
|VR_EzAlignedDimension()       |Method                       |Call this void to create ```AlignedDimension ``` when using VR input |
|VR_EzAngledDimension()        |Method                       |Call this void to create ```AngleDimension ``` when using VR input |
|VR_EzAreaMeasure()            |Method                       |Call this void to create ```AreaMeasure ``` when using VR input |
|VR_HighlightHoveredDimension()|Method                       |This void will call when using VR from ``` EzDimStarter ``` using ``` gameObject.SendMessage() ``` |
|VR_SelectDimension()          |Method                       |This void will call when using VR from ``` EzDimStarter ``` using ``` gameObject.SendMessage() ```  |


  
<br/><br/>
