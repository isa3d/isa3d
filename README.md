# Easy Dimension Measurement System For Unity

![image](https://user-images.githubusercontent.com/88411269/216851590-bd33ad4a-d12c-492e-b990-029453dee0c6.png)
Using **EzDimension** is quite easy. it works with **Mouse** or **VR** input. so we need to have unity **new input system** to start using it. We have 5 types of measurement :
* Point To Point
* Linear
* Aligned
* Angle
* Area
<br/><br/>

### key Features :
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


### dependencies :

After install **input System** from package manager create an **Event System** and select it in the hierarchy, then in the inspector click on the **Replace with InputSystemUIInputModule** button. You can read the [**input system documentation**](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.5/manual/index.html).

![image](https://user-images.githubusercontent.com/88411269/216845364-046d6af5-094a-490e-9da4-8f453f10e764.png)
<br/><br/>
This package uses **TextMeshPro** too. Install it from package manager if you do not have it already.read the [**TextMeshPro documentation**](https://docs.unity3d.com/Manual/com.unity.textmeshpro.html).

if you need to use this package inside a **VR** game or app, there is a **Sample VR Script** that you can download it from package manager in the sample section. before downloading it you need to install **XR Interaction Toolkit 2.2.0** to use this sample. also you can write your own **VR Script** sample. We recommend to check the sample script because the **VR Script** should work with the starter Script properly. for more details about using this package for **HMD** check the [**Using EzDimension in VR**](#VRSetting).

---

# Quick start

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

![image](https://user-images.githubusercontent.com/88411269/216846372-5bf205e8-d45c-462c-90d9-feb1da2fc6d5.png)

<br/><br/>

3. Select the **StarterGO**, then fill the references and set the parameters. If it’s your first run, we recommend to check the sample scene first.
Consider that the first field should be empty to test the dimensions with mouse input. We’ll explain how to use it in VR in the [**Using EzDimension in VR**](#VRSetting) section.

![image](https://user-images.githubusercontent.com/88411269/216846440-11e8cad1-d26a-451e-83a6-f01bbbef0c4a.png)

<br/><br/>

4 . When you fill the references and set the parameters, create a ground object and another two objects, check them having “Collider” component. you can create your first dimension by click on the button that you connected to “EzPointToPointDimension()” void:

![CreatePointToPointDimension](https://user-images.githubusercontent.com/88411269/216851375-caaf83e1-1bf9-4e11-a058-665a60579b6b.gif)

congratulations, you made your first dimension!

---

<br/><br/>

# General Settings

<br/><br/>

![image](https://user-images.githubusercontent.com/88411269/216851756-74f0d795-6e22-4bc3-9b59-5e47a110b82a.png)

For each dimensions we have some general settings in the starter script. if you take a look at the inspector when **StarterGO** is selected, you can find the **General** section.
these settings are share between more than one dimension. For example **Text Size** is share between all of them and arrow radius is share between **Point To Point**, **Linear** and **Aligned** dimension. You can read about the details of each option in the [**General References**](#GeneralReferences) section.

<br/><br/>

![image](https://user-images.githubusercontent.com/88411269/216856990-c7379445-a363-4cf6-a997-085c27e341cb.png)

the color section is shared between the dimensions too. . If you change the “Number Color”, It changes all of the dimensions number’s color except which dimensions that mark as individual. We’ll explain individuality of each dimension along the way. Last three colors will multiply with the dimension’s color when they are selected or when we hover mouse or VR-Interactor on number of an object. It works with a Lerp function line this : 

    if (mouse hovered on a text of a dimension) >> Color = Color.Lerp( numberColor, hoveredTint, 0.5f );

---

<br/><br/>

# Dimension Types
<br/><br/>
### Point To Point Dimension
Point to point dimension is simple type of the measurement. It takes two Vector3 position and calculate the direct distance between these two points.
When run the void “EzPointToPointDimension()” by click on the button in your UI, The “EzPointToPointDimension” gameobject will create under the StarterGO but all of its child are invisible till you hit the first click on an object that has a collider. After that while you didn’t hit the second click, the dimension it measure the first click and the current mouse position (if mouse hovers on an object with collider). after hit the second click your dimension will add to the “dimensionsList” in the starter script and its done.
If you select the “EzPointToPointDimension” gameobject under the “StarterGO” and take a look at the inspector you can see that the dimension copied the parameters from starter script inside itself.

![image](https://user-images.githubusercontent.com/88411269/216855671-748c5473-5272-4f18-b502-b36fb1254dc5.png)


<br/><br/>
### Linear Dimension



<br/><br/>
### Aligned Dimension



<br/><br/>
### Angle Dimension



<br/><br/>
### Area Measure





.
<details><summary>CLICK ME</summary>
<p>

#### We can hide anything, even code!

```ruby
   puts "Hello World"
```

</p>
</details>

1. A
1. A


- ![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png) `#f03c15`
- ![#c5f015](https://placehold.co/15x15/c5f015/c5f015.png) `#c5f015`
- ![#1589F0](https://placehold.co/15x15/1589F0/1589F0.png) `#1589F0`

<span style="color:orange;">Word up</span>




1. [go to heading](#VRSetting)


Text that is not a quote

> Text that is a quote


**This is bold text**


| Rank | THING-TO-RANK |
|-----:|---------------|
|     1|               |
|     2|               |
|     3|               |


```
aaa = "AAA"
bbb = "BBB"
```
  
    asda as dasddda
    

    
    
<a name="VRSetting">
  </a>
  
### Using EzDimension in VR :


<a name="GeneralReferences">
  </a>
  
### General References :
  
  
  
