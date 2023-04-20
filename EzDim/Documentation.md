
<br />

# Easy Dimension Measurement System For Unity

[//]: # (-----------------------------------Introduction----------------------------------)

<a name="Introduction">
  </a>
  
<p>
  <img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" width="64" height="64" align="right" hspace="0">
  <h1>Introduction :</h1>
</p>

<br/>

Our unity plugin is a comprehensive solution for creating dimensions in your projects. With compatibility for mobile devices, AR and VR, you can easily bring dimensioning to any environment. The plugin supports dynamic transforms, meaning changes to your objects in real-time will be accurately reflected in the dimensions. A variety of units including custom units, and full control over materials, color, and text parameters, make it easy to customize the appearance of your dimensions. Our selection system and highlight feature, along with trigger events for hover and selection, makes it easy to interact with your dimensions. Lastly, our offset options ensure that your dimensions are always visible and clearly legible, no matter the background.



<table width="100%" cellpadding="10" cellspacing="0" style="border-collapse: collapse;">
  <tr>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/216851375-caaf83e1-1bf9-4e11-a058-665a60579b6b.gif" alt="Image 1" width="100%"></td>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/216858764-47cbd7af-16ce-4935-914c-8ba57de36b06.gif" alt="Image 2" width="100%"></td>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/216859337-ce20a36f-f6c0-4ae9-97d0-0ac5f3d5530a.gif" alt="Image 3" width="100%"></td>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/217530740-b7539441-4389-40d2-a8d1-77c1abff63c3.gif" alt="Image 4" width="100%"></td>
  </tr>
</table>

<table width="100%" cellpadding="10" cellspacing="0" style="border-collapse: collapse;">
  <tr>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/217532878-b0909a77-cae2-4537-bbb8-2112ced2d468.gif" alt="Image 1" width="100%"></td>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/217531103-d6c8ef1d-aef6-416e-9cf3-f17dae02b457.gif" alt="Image 2" width="100%"></td>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/219002268-f06758bf-9ec8-4f4d-80d3-5e44fb0e0240.gif" alt="Image 3" width="100%"></td>
    <td style="padding: 10px; border: none;"><img src="https://user-images.githubusercontent.com/88411269/217533595-2ab4127b-b9b7-4083-9a4d-45febe300334.gif" alt="Image 4" width="100%"></td>
  </tr>
</table>

---

<br/><br/>




[//]: # (-----------------------------------## MeasurementTypes----------------------------------)

<br/>
<a name="Introduction_MeasurementTypes">
  </a>
  
  
## MeasurementTypes :


<br/>
 
|Types         |                       What To Measure          |MainLine          |Guide 	          | Arrows           | Number           |Border            |Arc               |Surface           |
|--------------|------------------------------------------------|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|:----------------:|
|Point To Point| Direct distance of two points                  |:heavy_check_mark:|                  |:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Linear        | Distance of two points along XYZ Axis          |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Aligned       | Distance of two points along their orientation |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|                  |                  |                  |
|Angle         | The angle between three points                 |:heavy_check_mark:|                  |                  |:heavy_check_mark:|                  |:heavy_check_mark:|                  |
|Area          | The area between selected points               |:heavy_check_mark:|                  |                  |:heavy_check_mark:|:heavy_check_mark:|                  |:heavy_check_mark:|

<br/>

![image](https://user-images.githubusercontent.com/88411269/216851590-bd33ad4a-d12c-492e-b990-029453dee0c6.png) 

<br /><br />


<a name="Introduction_KeyFeatures">
  </a>
  

[//]: # (-----------------------------------## Key Features----------------------------------)


## Key Features

* Compatible by Mobile Devices, AR & VR.
* support dynamic transforms. if you move, rotate or scale the target objects in runtime, the dimension start and end will update correctly.
* Support Units (Milimeters, Centimeters, Meters, Inch, Foot, Yard).
* Support Custom Unit if you need a unit that was not in the units list.
* Update TextPosition manually and automatic based on camera position .
* Having control on the materials of each part.
* Having control on color of each part.
* Highlight dimension when mouse or XR ray interactor hovers on the text any dimension.
* selection system.
* full control of texts size, lines thickness, arrows size , etc... .
* change the parameters for all dimensions or disconnect some of them to have individual properties.
* Trigger event when selection changed and when mouse hovered on a dimension.
* different types of offset to avoid Zfighting and text coverage behind the scene objects.

---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")


---

<br /><br />



[//]: # (-----------------------------------# ListOfContents----------------------------------)

<a name="ListOfContents">
  </a>
  
<p>
  <img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" width="64" height="64" align="right" hspace="0">
  <h1>List Of Contents:</h1>
</p>



<details>
 
<summary>Introduction</summary>

* [Measurement Types](#Introduction_MeasurementTypes)
* [Key Features](#Introduction_KeyFeatures)

</details>

<details>
<summary>Road Map And Limits </summary>

* [Road Map](#RoadMap)
* [Known Limitations of Easy Dimension](#Limits)

</details>


<details>
<summary>Dependencies</summary>

* [Input System](#Dependencies_InputSystem)
* [Text Mesh Pro](#Dependencies_TextMeshPro)
* [XR Interaction Toolkit](#Dependencies_XRInteractionToolkit)

</details>

<details>
<summary>Quick Start</summary>
 
* [Start Using EzDimension](#QuickStart)

</details>

<details>
<summary>Settings Notes</summary>

* [General Parameters](#SettingsNotes_GeneralParameters)
* [Colors](#SettingsNotes_Colors)

</details>

<details>
<summary>Dimension Types</summary>

* [PointToPoint Dimension](#DimensionTypes_PointToPointDimension)
* [Linear Dimension](#DimensionTypes_LinearDimension)
* [Aligned Dimension](#DimensionTypes_AlignedDimension) 
* [Angle Dimension](#DimensionTypes_AngleDimension) 
* [Area Measure](#DimensionTypes_AreaMeasure) 
 
</details>

<details>
<summary>Scripting Manual</summary>

* [Code Architecture](#ScriptingManual_CodeArchitecture)
* [Mouse Input](#ScriptingManual_MouseInput)
* [VR Input](#ScriptingManual_VR)

</details>

<details>
<summary>Scripting API</summary>

* [PointToPointDimension](#ScriptingAPI_PointToPointDimension)
* [LinearDimension](#ScriptingAPI_LinearDimension)
* [AlignedDimension](#ScriptingAPI_AlignedDimension)
* [AngleDimension](#ScriptingAPI_AngleDimension)
* [LinearAreaMeasure](#ScriptingAPI_AreaMeasure)
* [EzDimFunctions](#ScriptingAPI_EzDimFunctions)
* [EzDynamicTargetObject](#ScriptingAPI_EzDynamicTargetObject)
* [EzDimStarter](#ScriptingAPI_EzDimStarter)
* [DrawInVR](#ScriptingAPI_DrawInVR)
 
 </details>
 
 <details>
<summary>Contact / Download </summary>

* [Contact](#Contact)
* [Download](#Download)

 
 </details>
  
</details>


---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")


---
<br/><br/>


[//]: # (-----------------------------------# Road Map----------------------------------)

<a name="RoadMap">
  </a>

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" width="64" height="64" align="right" hspace="0">
  <h1>Road Map : </h1>
</p>


Easy Dimension is a constantly evolving tool, and we are committed to improving it over time. To make Easy Dimension even better, we need your support and feedback. Our development roadmap is driven by user requests, so we encourage you to reach out to us for any questions, bug reports, or feature requests.

Here's a look at some of the features we plan to implement in future versions:

* Editor Support.
* Fix the aligned dimension dynamic target in free mode.
* Create more sample scenes by integrating with popular virtual reality platforms.
* Add input for the grab interactor component for target objects.
* Enhance the text position control for area measures.
* Include perimeter calculation for area measures.
* Add interactive measures, such as rulers, plummets, bubble levels, and other cool measurement tools for VR usage.
* Write more comments inside the scripts and make them more organized.
* Add Preset Manager for Customized Settings
* Improve the overall user interface and user experience.

Thank you for your support, and we look forward to improving Easy Dimension with your feedback.

---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

---

<br/><br/>


[//]: # (-----------------------------------# Known Limitations of Easy Dimension----------------------------------)

<a name="Limits">
  </a>

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" width="64" height="64" align="right" hspace="0">
  <h1>Known Limitations of Easy Dimension : </h1>
</p>

As with any software package, there are some limitations to what you can do with Easy Dimension. We are committed to continually improving the package based on user feedback, and will update this section over time. Here are some limitations you should be aware of:

* This package is currently only functional during runtime. Editor support is on the roadmap, but if you require it sooner, please make a request.
* There may be some bugs when using aligned and angle dimensions in free mode, especially if you rotate the target object. It will be fixed soon.
* The VR scripts are prepared for XR Interaction Toolkit 2.2.0. If you use another VR package, you may need to edit the VR script.
* You can't specify the hovered and selected color for the dimensions. The color will always lerp to its original color.
* We haven't worked on the settings preset manager yet, and if you need to have settings preset, you need to edit the scripts on your own until we implement it. If you have any questions, don't hesitate to ask.
* We used TextMeshPro and Unity Default Line. Consider that we are limited to their boundary.
* The VR scene is not included in this version. If you want to use it in VR, you need to download the sample VR script and follow the documentation to set up the VR based on your pipeline.

We welcome your feedback and reports of any issues or limitations you encounter while using Easy Dimension. Together, we can continue to improve the package and make it the best it can be.

---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

---


<br/><br/>



[//]: # (-----------------------------------# Dependencies----------------------------------)

<a name="Dependencies">
  </a>

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" width="64" height="64" align="right" hspace="0">
  <h1>Dependencies :</h1>
</p>



<a name="Dependencies_InputSystem">
  </a>


## Input System :

After install **input System** from package manager create an **Event System** and select it in the hierarchy, then in the inspector click on the **Replace with InputSystemUIInputModule** button. You can read the [**input system documentation**](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.5/manual/index.html).


<img src="https://user-images.githubusercontent.com/88411269/216845364-046d6af5-094a-490e-9da4-8f453f10e764.png" width="500">


<br/>

<a name="Dependencies_TextMeshPro">
  </a>

## Text Mesh Pro :
This package uses **TextMeshPro** too. Install it from package manager if you do not have it already.read the [**TextMeshPro documentation**](https://docs.unity3d.com/Manual/com.unity.textmeshpro.html).

<br/>

<a name="Dependencies_XRInteractionToolkit">
  </a>
  
## XR Interaction Toolkit (Optional) :

if you need to use this package inside a **VR** game or app, there is a **Sample VR Script** that you can download it from package manager in the sample section. before downloading it you need to install **XR Interaction Toolkit 2.2.0** to use this sample. also you can write your own **VR Script** sample. We recommend to check the sample script because the **VR Script** should work with the starter Script properly. for more details about using this package for **HMD** check the [**Using EzDimension in VR**](#ScriptingManual_VR).


---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")


---

<br/><br/>

[//]: # (-----------------------------------# Quick Start----------------------------------)

<a name="QuickStart">
  </a>

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" width="64" height="64" align="right" hspace="0">
  <h1>Quick Start :</h1>
</p>

<br/>


1. Create an empty game object and rename it to **StarterGO** and add **EzDimStarter** component on it.

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

<br/><br/>

3. Select the **StarterGO**, then fill the references and set the parameters. If it’s your first run, we recommend to check the sample scene first.
Consider that the first field should be empty to test the dimensions with mouse input. We’ll explain how to use it in VR in the [**Using VR Input**](#ScriptingManual_VR) section.


<img src="https://user-images.githubusercontent.com/88411269/218296772-9659a633-d6a8-4f21-82d6-1022a765fe88.jpg" width="926">

<br/><br/>

4 . When you fill the references and set the parameters, create a ground object and another two objects, check them having “Collider” component. you can create your first dimension by click on the button that you connected to “EzPointToPointDimension()” void.

<img src="https://user-images.githubusercontent.com/88411269/216851375-caaf83e1-1bf9-4e11-a058-665a60579b6b.gif" width="500">

<br/>

congratulations, you made your first dimension!


----

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

----

<br/><br/>


  
[//]: # (-----------------------------------# Settings Notes----------------------------------)

<a name="SettingsNotes">
  </a>


<p>
  <img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" width="64" height="64" align="right" hspace="0">
  <h1>Settings Notes :</h1>
</p>



<a name="SettingsNotes_GeneralParameters">
  </a>
  
## General Parameters :

<img src="https://user-images.githubusercontent.com/88411269/216851756-74f0d795-6e22-4bc3-9b59-5e47a110b82a.png" width="500">

The general settings for the dimensions are found in the starter script. To view these settings, select the StarterGO `gameObject` in the inspector. 

These settings are shared between multiple dimensions. For example, the **Tex tSize** is shared between all of the dimensions, and the **arrow radius** is shared between the `Point to Point`, `Linear`, and `Aligned` dimensions. 

For more information about each option, refer to the [**Scripting API**](#ScriptingAPI) section.

<br/>

<a name="SettingsNotes_Colors">
  </a>

## Colors :

<img src="https://user-images.githubusercontent.com/88411269/216856990-c7379445-a363-4cf6-a997-085c27e341cb.png" width="500">

The Color section in the StarterGO script is also shared among all dimensions. Any changes made to the "Number Color" setting will affect all dimensions, except those marked as individual. We will cover the individuality of each dimension in further sections. 

The last three colors are used to multiply the dimension's color, either when selected or when the mouse or VR-Interactor hovers over the dimension's number. This is achieved through the use of a Lerp function. 


    if (mouse hovered on a text of a dimension)
          Color = Color.Lerp( numberColor, hoveredTint, 0.5f );


---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

---

<br/><br/>


[//]: # (-----------------------------------# Dimension Types----------------------------------)

<a name="DimensionTypes">
  </a>


<p>
  <img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" width="64" height="64" align="right" hspace="0">
  <h1>Dimension Types :</h1>
</p>



<a name="DimensionTypes_PointToPointDimension">
  </a>



## Point To Point Dimension :

Point to point dimension is a simple type of measurement. It calculates the direct distance between two `Vector3` positions.

- When you run the void `EzPointToPointDimension()` by clicking on the button in your UI, the `EzPointToPointDimension` gameobject will be created under the **StarterGO**.
- However, all of its children are invisible until you make the first click on an object that has a collider.
- After that, while you haven't made the second click, the dimension measures the first click and the current mouse position (if the mouse hovers over an object with a collider).
- Once you make the second click, your dimension will be added to the `dimensionsList` in the starter script and it's done.
- If you select the `EzPointToPointDimension` gameobject under the **StarterGO** and take a look at the inspector, you can see that the dimension copied the parameters from the starter script inside itself.

<br/>

<a name="DimensionTypes_PointToPointDimension_Parameters">
  </a>

### Parameters :


<img src="https://user-images.githubusercontent.com/88411269/216855671-748c5473-5272-4f18-b502-b36fb1254dc5.png" width="500">

There are two types of parameters in all dimensions.

Some parameters are always individual, while others get their value from the `ValueReference Component` (which is the **StarterGO** script) until you mark `IsIndividual`.

For example, in this type of dimension, everything under the `IsIndividual` toggle (all parameters except `ValueReference`) can have its local value if you turn on this Boolean.

So, if you need to have control from another script on a dimension separately, you first need to turn on this option at the beginning. If you turn it off again, everything is fine, and the values will be set to your settings from the **StarterGO** script because each script carries the **StarterGO** script with itself in the `ValueReference` field.


<br/>

<a name="DimensionTypes_PointToPointDimension_Individuality">
  </a>

### Individuality :

<img src="https://user-images.githubusercontent.com/88411269/216858500-332b98f0-fa90-4e30-99cf-a9736b64d2f9.png" width="500">

By turning on “IsIndividual”, we can have the same dimension type with different settings.


<br/>

<a name="DimensionTypes_PointToPointDimension_DynamicTransform">
  </a>
  
### Dynamic Transform :

<img src="https://user-images.githubusercontent.com/88411269/216858764-47cbd7af-16ce-4935-914c-8ba57de36b06.gif" width="500">

There is another option named "Is Dynamic". 
If this option is set to `True`, the dimension will automatically update if the target objects undergo any transformations. 

<br/>

> **Note**<br/>
> If the dimension is not set as individual, it will be determined by the "IsDynamic" setting in the `StarterScript` > `General` section.

<br/>

You can review other parameters in the [**ScriptingAPI/PointToPointDimension**](#ScriptingAPI_PointToPointDimension) section.


<br/><br/>


<a name="DimensionTypes_LinearDimension">
  </a>
  
## Linear Dimension :
 
The **Linear Dimension** is used to measure the distance between two points along a main axis. It will not rotate, even if the target points have different positions in R3. The measurement direction is determined by the "Measurement Direction" parameter.


<br/>

<a name="DimensionTypes_LinearDimension_Parameters">
  </a>

### Parameters :

<img src="https://user-images.githubusercontent.com/88411269/216859029-48c5485b-bb39-40af-b0d3-4ef62724e09a.png" width="500">

For example, if you choose the `X` direction, it will measure the line between the two target points in the `X` direction. You can also choose an offset direction in one of the other two directions. 
Note that the measurement direction and offset direction cannot have the same value, so if you choose the same value, the code will replace the offset direction to avoid an error.

<br/>

<a name="DimensionTypes_LinearDimension_DirectionAndOffset">
  </a>

### Direction And Offset :
<img src="https://user-images.githubusercontent.com/88411269/216859217-7a73bc02-3be8-4b59-a71e-656e628cf588.png" width="1000">

## Left
Measurement Direction = X, Offset Direction = Z. 

## Right
Measurement Direction = Z, Offset Direction = X.

We have the same rule in Y direction. If you choose to measure the height of an object, the measurement direction will be “Y” and you can choose the offset direction between “X” or “Z”.

<br/>


<img src="https://user-images.githubusercontent.com/88411269/216859258-fda2327b-bcdd-47ab-972d-7f9e93efa05d.png" width="500">

If the offset distance is less than the distance between two target points, the dimension will automatically change the secondary lines to ensure that it always connects the target points.

<br/>


<img src="https://user-images.githubusercontent.com/88411269/216859337-ce20a36f-f6c0-4ae9-97d0-0ac5f3d5530a.gif" width="500">

Linear Dimension in Z Axis with X Offset

The Linear Dimension can be drawn in the Z axis and offset to the X axis, allowing you to change the offset distance.

- Measurement Direction: Z 
- Offset Direction: X

<br/>

<a name="DimensionTypes_LinearDimension_AutoTextPosition">
  </a>

### Auto Text Position :

<img src="https://user-images.githubusercontent.com/88411269/216859356-eeec3929-5b8b-4f1e-b2f7-7e8d55269389.png" width="500">

If the measured distance is less than the distance between the two target points along the measured direction, the dimension will automatically change the dimension appearance if you activate ``autoTextPositin`` option.

---
<br/><br/>



<a name="DimensionTypes_AlignedDimension">
  </a>

## Aligned Dimension :



Aligned dimension is useful for measuring the distance between two points in one of the main coordinate planes or a custom plane. It also supports measuring distances for rotated objects.

<a name="DimensionTypes_AlignedDimension_Parameters">
  </a>
  
### Parameters : 

<img src="https://user-images.githubusercontent.com/88411269/217420788-0f777d3d-d8e8-4a7b-b790-066b0a7410b3.png" width="500">

The settings for Aligned dimension are similar to those of Linear dimension. The main difference is the addition of a `Measurement Plane` option, instead of a `Measurement Direction` option. 


<br/>

<a name="DimensionTypes_AlignedDimension_ReverseDirection">
  </a>

### Reverse Direction :

<img src="https://user-images.githubusercontent.com/88411269/217422629-662161ee-1547-44ee-941a-1f5e9b4b1752.png" width="500">


In addition, there is an option named "Reverse Direction." The function of this Boolean is exactly the same as multiplying the offset distance by -1. 

In this type of dimension, the positive direction of the offset distance is based on which target point is hit first. Depending on which point is clicked first, the positive direction is different. With this Boolean, you can avoid having a negative offset distance to reverse the offset direction's positive side.


<br/><br/>


<a name="DimensionTypes_AlignedDimension_FreeDirection">
  </a>

### Customizable Offset Direction Plane in Free Mode :

<img src="https://user-images.githubusercontent.com/88411269/219002268-f06758bf-9ec8-4f4d-80d3-5e44fb0e0240.gif" width="500">

There are four states for the direction plane (XZ, XY, ZY, Free). If you set the direction offset to Free before creating the dimension, after selecting points A and B, a plane appears, and you can dictate your custom offset direction by clicking on the appeared plane, which is the input of the "Aligned Dim Free Mode Plane Prefab". The position of this point will be stored in "Direction Point in Free Mode". So, if you don’t change this value and switch the direction plane, you can change it to Free mode again later. Alternatively, you can change the direction by editing this value. However, please be aware that if you use the free mode, it does not support transform change yet. Turn off "Is Dynamic" if you want to use it on any moving object. We have this on our roadmap, and we will make it possible in the next updates.


<br/>

> **Warning**
> aligned dimensions in free mode are not currently supported target objects rotation. it will fix in updates soon.


<br/><br/>

<a name="DimensionTypes_AngleDimension">
  </a>

## Angle Dimension :

<br/>

Angle dimension measures the angle between three points. These points can be in the main planes (XZ, XY, YZ) or in a custom plane. It measures angles from 0 to 180 degrees.

<br/>

<a name="DimensionTypes_AngleDimension_Parameters">
  </a>
  
### Parameters :

<img src="https://user-images.githubusercontent.com/88411269/217425866-5e915710-f361-4adf-8a24-31f90e317901.png" width="500">


<br/>

<a name="DimensionTypes_AngleDimension_Components">
  </a>
  
### Components :

<img src="https://user-images.githubusercontent.com/88411269/217530046-9374c24e-05d7-4091-bafe-1512d90aa8b3.png" width="500">

The angle dimension consists of four components:

1. **Lines**: Two lines that form the angle.
2. **Number**: The numeric value of the angle in degrees.
3. **Arc**: A plane with a transparent material to draw the arc between the two lines.
4. **Arc Scale Parameter**: A parameter to control the scale of the arc GameObject.

<a name="DimensionTypes_AngleDimension_ArcAppearance">
  </a>
  
### Arc Appearance :

The arc of the angle dimension is beautifully crafted with the help of its material shader, which offers the essential options of color and degree, as well as additional options to cater to individual requirements.

<br/>

<a name="DimensionTypes_AngleDimension_TextPosIfNotFit">
  </a>

### Automatic Text Adjustment for Tight Angles :

<img src="https://user-images.githubusercontent.com/88411269/217530372-34f0c439-9dfe-4baa-abd5-494372b8c63c.png" width="500">

When the angle between two lines is too tight, the text may overflow and not fit between them. In this case, the script will automatically move and rotate the text, setting its position above one of the lines in a proper way and aligning the rotation to the direction of the line that the text is placed above.

To customize the position of the text when it overflows and moves to a new position, you can use the `Text Offset If Not Fit` parameter, which is a Vector2 input.

<br/>

<a name="DimensionTypes_AngleDimension_DynamicTransform">
  </a>
  
### Dynamic Transform Support for Angle Dimension :

<img src="https://user-images.githubusercontent.com/88411269/217530740-b7539441-4389-40d2-a8d1-77c1abff63c3.gif" width="500">

Similar to other dimensions, the angle dimension also supports dynamic transform if you check the `isDynamic` option. This allows the dimension to adjust and update itself based on the changing positions and orientations of the objects it is measuring.

By enabling this option, you can use the angle dimension with moving or changing objects without needing to recreate it each time.

<br/>

<a name="DimensionTypes_AngleDimension_FreeDirection">
  </a>
  
### Drawing an Angle Dimension on a Custom Plane :

![AngleDimension_Free](https://user-images.githubusercontent.com/88411269/217531103-d6c8ef1d-aef6-416e-9cf3-f17dae02b457.gif)

The angle dimension can be drawn in the main planes (XZ, XY, YZ) or on a custom plane. To draw an angle dimension on a custom plane, simply change the `angleMeasurementPlane` parameter to `Free`, and then click on the points that you need to measure.

This allows you to measure angles on planes that are not aligned with the main coordinate axes. By selecting the appropriate points, you can define any plane and measure angles on it with the angle dimension.


> **Note**<br/>
> To reduce any intersection between the dimension and target objects, you can increase the`normalOffset` parameter if the dimension is individual or `hitNormalOffset` in the starter script if it's not individual. This parameter will get the first hit point normal and move the dimension along it forward. It will also help to avoid Z-fighting. Always set it to a small amount.

---

<br/><br/>



<a name="DimensionTypes_AreaMeasure">
  </a>

## Area Measure :


<br/>

Area Measure is a dimension tool that can calculate the area between some points. There are options to control the orientation of the text that is displayed for the area measurement.

> **Note**<br/>
> The number always lays down on the surface of the measured area.

<br/>

> **Note**<br/>
> 
> The area measure tool creates a surface between the points. To perform triangulation, we utilize "EarCut Master". Please visit the EarCut Master Github page for more information. <br/> 
> https://github.com/mapbox/earcut
> <br/> <br/> 
> its using "ISC License". <br/> 
> ![image](https://user-images.githubusercontent.com/88411269/220639279-bbe72170-fc93-4a15-bf76-4411c9fcb8c4.png)

<br/>

<a name="DimensionTypes_AreaMeasure_Parameters">
  </a>
  
### Parameters : 

<img src="https://user-images.githubusercontent.com/88411269/217532089-f0f665e7-58f7-486a-badd-ce7a1575f31e.png" width="500">

<br/>

<a name="DimensionTypes_AreaMeasure_OverView">
  </a>
  
### Overview :

<img src="https://user-images.githubusercontent.com/88411269/217532420-782710b7-e115-4416-b440-8c89d16e1456.png" width="500">

The "Area Measure" tool consists of four main parts: handles, surface, border, and the number text. When you click on a surface, the handle prefab will instantiate where you clicked. If you press the right-click button, the draw function will be called and the area measure will be created.

<br/>


<a name="DimensionTypes_AreaMeasure_DynamicTransform">
  </a>


### Dynamic Transform :

<img src="https://user-images.githubusercontent.com/88411269/217532878-b0909a77-cae2-4537-bbb8-2112ced2d468.gif" width="500">

The "Area Measure" component supports dynamic transform, which means that it updates the area automatically when you move any of its handles. If you have made the handle prefab selectable or moveable in your project, the area measure will be able to track changes made to the handle positions. It's important to note that there is no "IsDynamic" Boolean in this component. So, as long as you change the position of any handle, the area will be updated automatically.

<br/>

> **Warning**
> Area dimensions for dynamic objects are not currently supported. They are only updated when the handle position is changed and will not connect automatically to the target objects.

<br/>

<a name="DimensionTypes_AreaMeasure_FreeDirection">
  </a>

### Drawing an Area Measure on Main or Custom Planes :

<img src="https://user-images.githubusercontent.com/88411269/217533595-2ab4127b-b9b7-4083-9a4d-45febe300334.gif" width="500">

Similar to the Angle Dimension and Aligned Dimension, the Area Measure can be drawn on the main planes (XZ, XY, ZY) or on a custom plane. To draw on a custom plane, set the "Area Measurement Plane" to "Free" and start drawing the area measure where you need it.

If you start drawing the area measure on an inclined plane or a ramp, the script will get the normal of the first hit point and define the custom draw plane based on that. This makes it possible to draw the area measure on any surface or plane, as long as you start the drawing process on a valid point.

<br/>


---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

---
  
  
<br/><br/>
  

[//]: # (-----------------------------------# Scripting Manual----------------------------------)

<a name="ScriptingManual">
  </a>

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" width="64" height="64" align="right" hspace="0">
  <h1>Scripting Manual :</h1>
</p>



<a name="ScriptingManual_CodeArchitecture">
  </a>
  
## Code Architecture :

![FlowChart_Mouse_VR](https://user-images.githubusercontent.com/88411269/218064085-cd827ca6-4782-4548-ad83-ad6cc4e22485.png)

The EzDimStarter component serves as the central hub for other inputs and components, as illustrated in the accompanying flow chart. This script offers nine public void methods which are connected to buttons for creating, hiding, unhiding, deleting, and updating dimensions, as outlined in the "Quick Start" section.

If using the script in VR, it is necessary to add the "DrawInVR" component to the same object as the "EzDimStarter." More information on using EzDimension in VR is provided in the "Using EzDimension in VR" section.

<a name="ScriptingManual_MouseInput">
  </a>

## Using Mouse Input :

If only working with mouse input, there is no need for "DrawInVR." As a result, the flow chart would appear as follows:

![FlowChart_Mouse](https://user-images.githubusercontent.com/88411269/218064249-752e9671-75f6-4add-8593-45dc156e83d3.png)

<br/>

<a name="ScriptingManual_MouseInput_CreationProcess">
  </a>

### Creation Process in EzDimStarter Component :

 When one of the public void functions inside the `EzDimStarter` component is called by pressing a UI button, such as the "Point To Point" button, the corresponding code will run.
 
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
 
At the beginning, it checks that the `isCreating` Boolean is off to avoid the duplication of the creation process. Then, it will turn on `isCreating` and will deselect the selected dimensions by clearing the `selectionList`. After that, it calls the `updateAll` function from `EzDimFunctions` to update the dimensions' appearance based on the new cleared `selectionList`. Now everything is ready to create a GameObject as a child of this GameObject to add the `PointToPointDimension` component. Then, the code will loop inside the `IEnumerator CreatePointToPointDimension()` while the added `PointToPointDimension` component `isDone` Boolean is not true. This Boolean will be set to true at the end of this IEnumerator. When this part is passed, the new dimension will be added to the `dimensionsList` as a new dimension.

Let's check what is inside the `IEnumerator CreatePointToPointDimension()`:
 
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
 
Inside the IEnumerator, several steps are executed after each mouse click. On the first click, a `rayCast` is used to obtain the first `hitPoint` and `hit.transform.gameObject`, which defines the first point. The script then unhides every part of the dimension by running the `Funcs.SetActiveAllChilds()` function from the `EzDimension` namespace inside the `EzDimFunctions` component. Next, the second point is defined by moving the mouse and clicking again.

After the second click, every frame, the `rayCast` of `Camera.ScreenPointToRay(Mouse.current.position.ReadValue())` defines the second point of the dimension. The `UpdateDimension()` function from the added `pointToPointDimension` component updates the dimension based on the second point, which updates every frame depending on the mouse position. After the second click, the `isDone` boolean inside the added `pointToPointDimension` component will be set to true, and the `isCreating` boolean inside the `EzDimStarter` will be set to false, which indicates the end of the creation process.

This process has the same logic for all dimensions. The `EzDimStarter` always creates a set of `gameObjects` and adds the Dimension Component on their parents. It gets and sets the required position from mouse input and updates the dimension until the creation process is complete. Note that the Create and Update dimension functions are inside the dimension components (`pointToPointDimension.cs`). The Create function is only called once since it's in the start void of the dimension component.

<br/>

<a name="ScriptingManual_MouseInput_DimensionComponents">
  </a>

### Overview of Dimension Components and Functions :

 ```C#
 
     void Start()
    {
        CreateDimension(mainParent, arrowPrefab);
        Funcs.SetActiveAllChilds(this.transform, false);
    }
    
```

There are `CreateDimension()` and `UpdateDimension()` voids inside all of the dimension components except for the area measure. Some dimensions also have additional functions, such as `UpdateTextTransform()` in `pointToPointDimension.cs`, `LinearDimension.cs`, and `AlignedDimension.cs`, and `UpdateTextAndIndicator()` in `AngleDimension.cs`.

The `LinearAreaMeasure.cs` component does not have `CreateDimension()`, `Start()`, or `Update()` voids. Instead, required gameObjects are created in the `Awake()` void, and there are five other voids named `UpdatePointsList()`, `UpdateBorderLine()`, `DrawArea()`, `UpdateAreaNumber()`, and `UpdateNumberPositionAndRotation()`.

The `EzDimFunctions.cs` component contains most of the functions and is under the `EzDimension` namespace. Other components that use any of these functions need to include `using EzDimension`.

There are more specific details in the [Scripting API](#ScriptingAPI) section.

 
<br/><br/>

<a name="ScriptingManual_VR">
  </a>

## Using VR Input

<br/>

<a name="ScriptingManual_VR_SampleScript">
  </a>
  
### Using the VR Sample Script with XR Interaction Toolkit :

![FlowChart_VR](https://user-images.githubusercontent.com/88411269/218101925-17dd1bf1-86c5-4565-b7af-bd6e18f5ee11.png)

To use Easy Dimension Measurement System in VR, you can download the **VR Sample Script** from the package manager to see how to set up the system for VR. This script is fully compatible with **XR Interaction Toolkit 2.2.0**. Since there are various VR integration packages, we won't include the VR scene inside the package to avoid any conflict and messy errors in your scene. Instead, we will look at the main logic of using Easy Dimension inside your VR scene.

<br/>

> **Note**<br/>
> To get started, go back to the [**Quick Start**](#QuickStart) section and look at the inspector when **StarterGO** is selected. You will see that the first field is **Draw In Vr Comp**. To use Easy Dimension in VR, you need to add the **DrawInVR.cs** component to the **StarterGO** and drag and drop the **StarterGO** inside the **Draw In Vr Comp** section.

<br/>

<a name="ScriptingManual_VR_MouseVSVR">
  </a>

### Comparing Mouse Input and VR Input in Easy Dimension Measurement System : 

In Easy Dimension, there are some differences between using mouse input and VR input. When using mouse input, a draw step occurs for every dimension, and each step passes after a mouse click. The `Camera.ScreenPointToRay(Mouse.current.position.ReadValue())` method is used to catch the `raycastHit`. However, when using VR input, this approach is not possible as we cannot use screen coordinates or mouse clicks to pass draw steps. Instead, we should use `bool ray = rayInteractor.TryGetCurrent3DRaycastHit(out hit)` to catch the hit, and we need to have a boolean that turns true after a desired button is pressed. To achieve this, we need to get one of our ray interactors from one hand and feed it to the `DrawInVR.rayInteractor`. For more information, please see the Scripting Manual section.<br/>

<img src="https://user-images.githubusercontent.com/88411269/218111506-6520f279-2f57-46c8-a271-a3ce448310cc.jpg" width="500">

<br/>


> **Note**<br/>
> **DrawInVR.cs** works dependently with **EzDimStarter** component. They should both be added to the same GameObject, which we have called **StarterGO**. You need to drag and drop **StarterGO** inside the **Draw In Vr Comp** field.

<br/>

<a name="ScriptingManual_VR_PracticalExample">
  </a>

### Practical Example :

To ensure that you understand how to use the **DrawInVR.cs** component, let's look at an example. You can download the **DrawInVR.cs** sample from the package manager and open it. In this sample, you will find some public void functions that are similar to the ones we saw in the **EzDimStarter** component.

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

It's quite similar to the previous example we discussed. Note that we didn't have a separate dimension list and we still send some data to the EzDimStarter script.

The creation process happens inside the `IEnumerator CreatePointToPointDimension()` function, which is quite similar to what we did before when using mouse input.


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

The only differences are the condition of going to the next step and how we get the `raycastHit`. Other steps are almost similar to what we did with mouse input.

 
---
 
[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

---
 
 
<br/><br/>





[//]: # (-----------------------------------# Scripting API----------------------------------)

<a name="ScriptingAPI">
  </a>

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" width="64" height="64" align="right" hspace="0">
  <h1>Scripting API :</h1>
</p>


<a name="ScriptingAPI_PointToPointDimension">
  </a>

## Point To Point Dimension :

<br/>

| Name                  | Type        | Description                                      |
|:----------------------|:-----------|:-------------------------------------------------|
| `valuesReference`     | `EzDimStarter` | Global parameters reference                    |
| `isIndividual`        | `bool`      | Allow dimension to have local attributes        |
| `isDynamic`           | `bool`      | Make dimension dynamic                           |
| `lineThickness`       | `float`     | Thickness of the line                            |
| `arrowHeight`         | `float`     | Arrow prefab's scale                             |
| `textSize`            | `float`     | TextMesh font size                               |
| `NormalOffset`        | `float`     | Offset dimension along normal of first hitPoint |
| `textTowardsCameraOffset` | `float` | Offset dimension towards camera to avoid masking or intersection with other objects in the scene |
| `textOffset`          | `float`     | Offset number's textMesh to its local Y axis     |
| `numberColor`         | `Color`     | Color of number's textMesh                        |
| `mainColor`           | `Color`     | Color of line material                            |
| `arrowColor`          | `Color`     | Color of arrow material                           |
| `hoveredTint`         | `Color`     | Color of hovered dimensions                       |
| `selectedTint`        | `Color`     | Color of selected dimensions                      |
| `hoveredOnSelectedTint` | `Color`   | Color of selected dimension when hovered         |
| `mainLineMat`         | `Material`  | Material of line                                  |
| `arrowMat`            | `Material`  | Material of arrows                                |
| `arrowPrefab`         | `GameObject`| Prefab containing the arrow object                |
| `cameraTransform`     | `Transform` | Transform of camera                               |
| `rendererCamera`      | `Camera`    | Camera component of our renderer camera           |
| `mainParent`          | `GameObject`| Dimension main parent                             |
| `pointA`              | `Vector3`   | Initial position of the first hitPoint            |
| `pointB`              | `Vector3`   | Initial position of the second hitPoint           |
| `secondDrawStep`      | `bool`      | This bool turns true after first click            |
| `isDone`              | `bool`      | This bool turns true at the end of creation process|
| `firstPointHitNormal` | `Vector3`   | Normal of first hitPoint                          |
| `objectATransformGO`  | `GameObject`| GameObject at the Position of first hitObject's center |
| `objectBTransformGO`  | `GameObject`| GameObject at the Position of second hitObject's center |
| `pointATransformGO`   | `GameObject`| GameObject at the position of first hitPoint     |
| `pointBTransformGO`   | `GameObject`| GameObject at the position of second hitPoint    |
| `objectA`             | `GameObject`| First hitObject                                   |
| `objectB`             | `GameObject`| Second hitObject                                  |
| `CreateDimension()`   | `Method`    | This void creates the dimension's parts           |
| `UpdateDimension()`   | `Method`    | This void updates the dimension's main features  |
| `UpdateTextTransform()`| `Method`   | This void updates the dimension's text transform |



<br/><br/>



<a name="ScriptingAPI_LinearDimension">
  </a>

## Linear Dimension :
 
<br/>

|Name                   |Type                      |Description                            |
|-----------------------|--------------------------|---------------------------------------|
|`valuesReference`        |`EzDimStarter`              |Global parameters reference |
|`measurementDirection`   |`Funcs.MeasurementDirection`|Measure the distance on this specific axis |
|`offsetDirection`        |`Funcs.OffsetDirection`     |Offset mainLine in this direction |
|`offsetDistance`         |`float`                     |Distance between mainLine from the first hitPoint |
|`isIndividual`           |`bool`                      |Allow dimension to have local attributes |
|`isDynamic`              |`bool`                      |Make dimension dynamic. If target objects moving, the dimension will update it's length |
|`mainLineThickness`      |`float`                     |Thickness of the mainLine |
|`arrowHeight`            |`float`                     |Arrow prefab's scale |
|`textSize`               |`float`                     |TextMesh font size |
|`NormalOffset`           |`float`                     |Offset dimension along normal of first hitPoint to avoid Z-Fighting |
|`textTowardsCameraOffset`|`float`                     |Offset dimension towards camera to avoid masking or intersection with other objects in the scene |
|`textOffset`             |`float`                     |Offset number's textMesh to it's local Y axis. it control the distance between number and mainLine |
|`secondaryLinesThickness`|`float`                     |Thickness of the sedondary lines |
|`secondaryLinesExtend`   |`float`                     |Length of secondary lines extend |
|`autoTextPosition`       |`bool`                      |change text and arrows position if text's width and arrows height was bigger than distance of measured points |
|`flipTextPosition`       |`bool`                      |flip position when autoTextPosition affected the dimension text and arrows position |
|`numberColor`            |`Color`                     |Color of number's textMesh |
|`mainColor`              |`Color`                     |Color of mainLine material. other material features can control by a costum script |
|`secondaryColor`         |`Color`                     |Color of secondaryLine material. other material features can control by a costum script |
|`arrowColor`             |`Color`                     |Color of arrow material. other material features can control by a costum script |
|`hoveredTint`            |`Color`                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|`selectedTint`           |`Color`                     |Color of selected dimensions |
|`hoveredOnSelectedTint`  |`Color`                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|`mainLineMat`            |`Material`                  |Material of mainLine |
|`secondaryLinesMat`      |`Material`                  |Material of secondaryLine |
|`arrowMat`               |`Material`                  |Material of arrows |
|`arrowPrefab`            |`GameObject`                |Prefab contain the arrow object.pivot should set to the center of it's base |
|`cameraTransform`        |`Transform`                 |Transform of camera |
|`mainParent`             |`GameObject`                |Dimension main parent |
|`pointA`                 |`Vector3`                   |Initial Position of the first hitPoint |
|`pointB`                 |`Vector3`                   |Initial Position of the second hitPoint |
|`isDone`                 |`bool`                      |This bool turns true at the end of creation process |
|`firstPointHitNormal`    |`Vector3`                   |Normal of first hitPoint |
|`objectATransformGO`     |`GameObject`                |GameObject at the Position of first hitObject's center |
|`objectBTransformGO`     |`GameObject`                |GameObject at the Position of second hitObject's center |
|`pointATransformGO`      |`GameObject`                |GameObject at the position of first hitPoint |
|`pointBTransformGO`      |`GameObject`                |GameObject at the position of second hitPoint |
|`objectA`                |`GameObject`                |First hitObject |
|`objectB`                |`GameObject`                |Second hitObject |
|`CreateDimension()`      |`Method`                    |This void creates the dimension's parts |
|`UpdateDimension()`      |`Method`                    |This void updates the dimension's main features |
|`UpdateTextTransform()`  |`Method`                    |This void updates the dimension's text transform |  




<br/><br/>



<a name="ScriptingAPI_AlignedDimension">
  </a>

## Aligned Dimension :

<br/>

  

|Name                   |Type                      |Description                            |
|-----------------------|--------------------------|---------------------------------------|
|`valuesReference`         |`EzDimStarter`              |Global parameters reference  |
|`measurementPlane`        |`Funcs.MeasurementPlane`    |Measure the distance on this specific plane |
|`offsetDistance`          |`float`                     |Distance between mainLine from the first hitPoint |
|`reverseDirection`        |`bool`                      |Multiply offset distance to -1 |
|`isIndividual`            |`bool`                      |Allow dimension to have local attributes |
|`isDynamic`               |`bool`                      |Make dimension dynamic. If target objects moving, the dimension will update it's length |
|`mainLineThickness`       |`float`                     |Thickness of the mainLine |
|`arrowHeight`             |`float`                     |Arrow prefab's scale |
|`textSize`                |`float`                     |TextMesh font size |
|`NormalOffset`            |`float`                     |Offset dimension along normal of first hitPoint to avoid Z-Fighting |
|`textTowardsCameraOffset` |`float`                     |Offset dimension towards camera to avoid masking or intersection with other objects in the scene |
|`textOffset`              |`float`                     |Offset number's textMesh to it's local Y axis. it control the distance between number and mainLine |
|`secondaryLinesThickness` |`float`                     |Thickness of the sedondary lines |
|`secondaryLinesExtend`    |`float`                     |Length of secondary lines extend |
|`DirectionPointInFreeMode`|`Vector3`                   |Position of direction point when draw in free mode |
|`autoTextPosition`        |`bool`                      |change text and arrows position if text's width and arrows height was bigger than distance of measured points |
|`flipTextPosition`        |`bool`                      |flip position when autoTextPosition affected the dimension text and arrows position |
|`numberColor`             |`Color`                     |Color of number's textMesh |
|`mainColor`               |`Color`                     |Color of mainLine material. other material features can control by a costum script |
|`secondaryColor`          |`Color`                     |Color of secondaryLine material. other material features can control by a costum script |
|`arrowColor`              |`Color`                     |Color of arrow material. other material features can control by a costum script |
|`hoveredTint`             |`Color`                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|`selectedTint`            |`Color`                     |Color of selected dimensions |
|`hoveredOnSelectedTint`   |`Color`                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|`mainLineMat`             |`Material`                  |Material of mainLine |
|`secondaryLinesMat`       |`Material`                  |Material of secondaryLine |
|`arrowMat`                |`Material`                  |Material of arrows |
|`arrowPrefab`             |`GameObject`                |Prefab contain the arrow object.pivot should set to the center of it's base |
|`mainParent`              |`GameObject`                |Dimension main parent |
|`cameraTransform`         |`Transform`                 |Transform of camera |
|`firstPointHitNormal`     |`Vector3`                   |Normal of first hitPoint |
|`pointA`                  |`Vector3`                   |Initial Position of the first hitPoint |
|`pointB`                  |`Vector3`                   |Initial Position of the second hitPoint |
|`secondDrawStep`          |`bool`                      |This bool turns true after first click in creation process and always remain true |
|`isDone`                  |`bool`                      |This bool turns true at the end of creation process |
|`objectATransformGO`      |`GameObject`                |GameObject at the Position of first hitObject's center |
|`objectBTransformGO`      |`GameObject`                |GameObject at the Position of second hitObject's center |
|`pointATransformGO`       |`GameObject`                |GameObject at the position of first hitPoint |
|`pointBTransformGO`       |`GameObject`                |GameObject at the position of second hitPoint |
|`objectA`                 |`GameObject`                |First hitObject |
|`objectB`                 |`GameObject`                |Second hitObject |
|`CreateDimension()`       |`Method`                    |This void creates the dimension's parts |
|`UpdateDimension()`       |`Method`                    |This void updates the dimension's main features |
|`UpdateTextTransform()`   |`Method`                    |This void updates the dimension's text transform |  

<br/><br/>




<a name="ScriptingAPI_AngleDimension">
  </a>

## Angle Dimension :

<br/>

|Name                    |Type                      |Description                            |
|------------------------|--------------------------|---------------------------------------|
|`valuesReference`         |`EzDimStarter`              |Global parameters reference  |
|`angleMeasurementPlane`   |`Funcs.AngleMeasurmentPlane`|Measure the distance on this specific plane |
|`rotateTextBy180`         |`bool`                      |Rotate text on the normal of angle measurement plane by 180 degree|
|`reverseTextPosIfNotFit`  |`bool`                      |Change not fitted text to other side |
|`isIndividual`            |`bool`                      |Allow dimension to have local attributes |
|`isDynamic`               |`bool`                      |Make dimension dynamic. If target objects moving, the dimension will update it's length |
|`linesThickness`          |`float`                     |Thickness of the lines |
|`textSize`                |`float`                     |TextMesh font size |
|`arcScale`                |`float`                     |Scale of the arc plane object |
|`textOffsetFromCenter`    |`float`                     |Offset number's textMesh from center of the angle |
|`NormalOffset`            |`float`                     |Offset dimension along normal of first hitPoint to avoid Z-Fighting |
|`textOffsetIfNotFit`      |`Vector2`                   |Offset to new position of the text in the angleMeasurementPlane if it was not fit |
|`numberColor`             |`Color`                     |Color of number's textMesh |
|`mainColor`               |`Color`                     |Color of the lines. other material features can control by a costum script |
|`arcColor`                |`Color`                     |Color of arc material. other material features can control by a costum script |
|`hoveredTint`             |`Color`                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|`selectedTint`            |`Color`                     |Color of selected dimensions |
|`hoveredOnSelectedTint`   |`Color`                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|`mainLinesMat`            |`Material`                  |Material of lines |
|`arcMat`                  |`Material`                  |Material of arc plane |
|`pointA`                  |`Vector3`                   |Initial Position of the first hitPoint |
|`pointB`                  |`Vector3`                   |Initial Position of the second hitPoint |
|`pointC`                  |`Vector3`                   |Initial Position of the third hitPoint |
|`mainParent`              |`GameObject`                |Dimension main parent |
|`cameraTransform`         |`Transform`                 |Transform of camera |
|`trueOnFirstStep`         |`Bool`                      |This bool turns true after first click in creation process and always remain true |
|`trueOnSecoundStep`       |`Bool`                      |This bool turns true after second click in creation process and always remain true |
|`isDone`                  |`Bool`                      |This bool turns true at the end of creation process |
|`lineAGO`                 |`GameObject`                |Line A ``` gameObject ```|
|`lineBGO`                 |`GameObject`                |Line B ``` gameObject ```|
|`pointBProxy`             |`Vector3`                   |Projected pointB to the angleMeasurementPlane with the same local height of pointA |
|`pointCProxy`             |`Vector3`                   |Projected pointC to the angleMeasurementPlane with the same local height of pointA |
|`arcParentGO`             |`GameObject`                |Parent of the arc plane ``` gameObject ``` |
|`plane`                   |`Plane`                     |Intersected plane by pointA, pointB and pointC |
|`numberGO`                |`GameObject`                |Number ``` gameObject ``` |
|`objectATransformGO`      |`GameObject`                |GameObject at the Position of first hitObject's center |
|`objectBTransformGO`      |`GameObject`                |GameObject at the Position of second hitObject's center |
|`objectCTransformGO`      |`GameObject`                |GameObject at the Position of third hitObject's center |
|`pointATransformGO`       |`GameObject`                |GameObject at the position of first hitPoint |
|`pointBTransformGO`       |`GameObject`                |GameObject at the position of second hitPoint |
|`pointBTransformGO`       |`GameObject`                |GameObject at the position of third hitPoint |
|`objectA`                 |`GameObject`                |First hitObject |
|`objectB`                 |`GameObject`                |Second hitObject |
|`objectC`                 |`GameObject`                |third hitObject |
|`CreateDimension()`       |`Method`                    |This void creates the dimension's parts |
|`UpdateDimension()`       |`Method`                    |This void updates the dimension's main features |
|`UpdateTextAndIndicator()`|`Method`                    |This void updates the dimension's text transform and ``` Angle``` parameter of arc material|




<br/><br/>




<a name="ScriptingAPI_AreaMeasure">
  </a>

## Area Measure :

<br/>

|Name                    |Type                      |Description                            |
|------------------------|--------------------------|---------------------------------------|
|`valuesReference`         |`EzDimStarter`              |Global parameters reference  |
|`cameraBaseNumberInXYDir` |`bool`                      |Update text rotation based on camera position |
|`rotateText180LocalY`     |`bool`                      |flip text in local Y |
|`rotateText180LocalZ`     |`bool`                      |flip text in local Z  |
|`rotateText180LocalX`     |`bool`                      |flip text in local X  |
|`isIndividual`            |`bool`                      |Allow dimension to have local attributes |
|`textSize`                |`float`                     |TextMesh font size |
|`localYOffset`            |`float`                     |Push the dimension in local Y direction to avoid Z-fighting with the underlying surface |
|`textLocalYOffset`        |`float`                     |Push the text in it's local Y direction to avoid Z-fighting with the area highlighting plane |
|`borderLocalYOffset`      |`float`                     |Push the border in local Y direction to avoid Z-fighting with the area highlighting plane |
|`borderThickness`         |`float`                     |Thickness of the border line |
|`positionOffset`          |`Vector2`                   |2d offset of the number in the surface |
|`enableBorderLine`        |`bool`                      |Show line around measured area |
|`numberColor`             |`Color`                     |Color of number's textMesh |
|`borderColor`             |`Color`                     |Color of border material. other material features can control by a costum script |
|`surfaceColor`            |`Color`                     |Color of surface material. other material features can control by a costum script |
|`hoveredTint`             |`Color`                     |This color multiplies to other colors if we hovered on any dimension when using mouse or VR |
|`selectedTint`            |`Color`                     |Color of selected dimensions |
|`hoveredOnSelectedTint`   |`Color`                     |Color of selected dimension when we hovered on it when using mouse or VR  |
|`surfaceMaterial`         |`Material`                  |Material of area highlighting plane |
|`BorderMaterial`          |`Material`                  |Material of area border |
|`handlesParent`           |`GameObject`                |Parent ``` gameObject ``` of area corners object
|`cameraTransform`         |`Transform`                 |Transform of camera |
|`points`                  |`List<Vector2>`            |List of area corners in a 2d plane|
|`handlesList`             |`List<GameObject>`         |List of area corners object |
|`area`                    |`float`                     |Calculated area stores in this float |
|`borderLineGO`            |`GameObject`                |Border line ``` gameObject ``` |
|`borderLine`              |`LineRenderer`              | ``` LineRenderer ``` component to draw borderLine|
|`meshCenter`              |`Vector3`                   |Center of the measured area |
|`allowDrawSurface`        |`bool`                      |Allow to update surface when corne's handles position are changing |
|`hitNormal`               |`Vector3`                   |Get the normal of the surface to avoid flip normal using EzdimFunctions.InternalFunctions.FlipNormal() |
|`measurementPlane`        |`Funcs.MeasurementPlane`    |Measure the area on this specific plane |
|`isDone`                  |`bool`                      |This bool turns true at the end of creation process |
|`drawMode`                |`bool`                      |This bool turns true at the end of creation process |
|`updatePointsList()`      |`Method`                  |Get the ``` List<Vector2> ``` of area corners position on 2d plane and rearrange them based on measurement plane |
|`UpdateBorderLine()`      |`Method`                    |Update border line based on measurement plane and points position |
|`DrawArea()`              |`Method`                    |Draw, update and triangulate the highlighting plane mesh |
|`UpdateNumberPosAndRot()` |`Method`                    |Update area number position and rotation |


  
<br/><br/>




<a name="ScriptingAPI_EzDimFunctions">
  </a>

## EzDimFunctions :

<br/>

|Name                    |Type                      |Description                            |
|------------------------|--------------------------|---------------------------------------|
|`Funcs`                   |`Class`                     |Contain the main functions |
|`InternalFunctions`       |`Class`                     |Contain the side functions that are not using frequently |
|`MeasurementDirection`    |`enum`                      |Main axis {X, Y, Z} |
|`OffsetDirection`         |`enum`                      |Main axis {X, Y, Z} |
|`MeasurementPlane`        |`enum`                      |Main planes  { XZ, XY, ZY, Free } |
|`AngleMeasurmentPlane`    |`enum`                      |Main planes  { XZ, XY, ZY, Free } |
|`MeasurmentType`          |`enum`                      |Main measurement types { Length, Area, Volume } |
|`UpdateArea`              |`static void`               |Update area measure |
|`UpdateAngle`             |`static void`               |Update angle dimension |
|`UpdateLength`            |`static void`               |Update the length of pointToPoint Dimension. using this when the start or end point position has changed |
|`UpdateLength`            |`static void`               |Update the length of Linear Dimension |
|`UpdateLength`            |`static void`               |Update the length of Aligned Dimension |
|`UpdateAll`               |`static void`               |Update all dimensions main features |
|`UpdateValues`            |`static void`               |Update all dimensions main features (depricated) |
|`UpdateNumbersRotation`   |`static void`               |Update all numbers rotation |
|`SelectDimension`         |`static void`               |Add hitObject to selection List |
|`HighlightSelectedDims`   |`static void`               |Highlight available dimensions in selection list and de-emphasize the deselected dimensions |
|`IsHoveredOnDimension`    |`static void`               |Manage highlighting and de-emphasizeing hovered dimensions |
|`SetActiveAllChilds`      |`static void`               |Activate all children of given ``` gameObject ``` |
|`HideSelectedDimensions`  |`static void`               |Hide selected Dimension |
|`UnhideAllDimensions`     |`static void`               |Unhide all dimensions inside a given starter script and dimension list |
|`DeleteDimensions`        |`static void`               |Delete selected dimensions |
|`Units`                   |`enum`                      |Measurement units { Millimetre, centimeter, meter, inch, foot, yard, custom } |
|`numberOfDecimal`         |`enum`                     |Number of decimals { none, one, two, three, four, five, six } |
|`LengthUnitCalculator`    |`static float`              |Return the multiplier of diffrent units for length |
|`AreaUnitCalculator`      |`static float`              |Returns the multiplier of diffrent units for area |
|`DecimalCalculator`       |`static string`             |Returns the decimal number for diffrent decimal numbers |
|`GetUnitTextShortForm`    |`static string`             |Returns the short form of the units text |
|`AngleBisectorPoint`      |`static Vector3`            |Calculate the bisector of three points |
|`HighlightColor`          |`static Color`              |Highlight a color with given percentage |
|`Remap`                   |`static float`              |Remap a value from one range to another range |
|`FlipNormal`              |`static bool`               |Custom function to calculate area surface normal to avoid reversed normal |
|`TriangulatePoints`       |`static mesh`               |Return triangulate mesh from given vector2 array of points |


<br/><br/>


<a name="ScriptingAPI_EzDynamicTargetObject">
  </a>
  
## EzDynamicTargetObject

<br/>

This component will add to all target objects. if any transform change happends and dimension's ``` isDynamic ``` option was true, this component call ``` updateLength() ``` function for the related dimension. 

<br/>

|Name                    |Type                        |Description                            |
|------------------------|----------------------------|---------------------------------------|
|`starterScript`           |`EzDimStarter`                |EzDimStarter component that created dimension on this target object |
|`areaMeasureRoot`         |`LinearAreaMeasure`           |``` LinearAreaMeasure ``` component (if exist) |
|`p2PDimComponentsList`    |`List<PointToPointDimension>` |List of ```PointToPointDimension ``` components (if exist) |
|`linDimComponentsList`    |`List<LinearDimension>`      |List of ```LinearDimension ``` components (if exist) |
|`alignDimComponentsList`  |`List<AlignedDimension>`     |List of ```AlignedDimension ``` components (if exist) |
|`angleDimComponentsList`  |`List<AngleDimension>`       |List of ```AngleDimension ``` components (if exist) |


<br/><br/>



<a name="ScriptingAPI_EzDimStarter">
  </a>

## EzDimStarter :

<br/>


|Name                         |Type                         |Description                            |
|-----------------------------|-----------------------------|---------------------------------------|
|`drawInVrComp`                 |`Component`                    |VR Component ( Null = Use Mouse Input ) |
|`unit`                         |`InternalFunctions.Units`      |Unit’s Enum { Millimetre, centimeter, meter, inch, foot, yard, custom } |
|`customUnitMultiplier`         |`float`                        |If Unit = Custom, this number will multipliy to default unit |
|`customUnitName`               |`string`                       |If Unit = Custom, Name of custom unit |
|`showUnitAfterNumber`          |`bool`                         |Show short form of the unit name after dimension’s number in runtime |
|`numberOfDecimal`              |`internalFuncs.numberOfDecimal`|Decimal Enum { none, one, two, three, four, five, six } |
|`cameraTransform`              |`Transform`                    |Camera based texts using this transform |
|`rendererCamera`               |`Camera`                       |RayCasts using this camera (normally its same as camera transform) |
|`mainLineMaterial`             |`Material`                     |Material of the “mainLine” (line between two arrows in dimensions) |
|`secondaryLinesMaterial`       |`Material`                     |Material of secondary lines in “Linear” and “Aligned” dimensions |
|`arrowMaterial`                |`Material`                     |Material of Arrows in “PointToPoint”, “Linear” and “Aligned” dimensions |
|`arcMaterial`                  |`Material`                     |Material of indicator arc of “Angle” dimension |
|`areaSurfaceMaterial`          |`Material`                     |Material of “Area” measure’s surface |
|`areaBorderMaterial`           |`Material`                     |Material of “Area” measure’s border |
|`arrowPrefab`                  |`GameObject`                   |Arrow Prefab for “PointToPoint”, “Linear” & “Aligned” dimensions |
|`areaHandlesPrefab`            |`GameObject`                   |It will attach to every corners of “Area” measure |
|`alignedDimFreeModeDirPointer` |`GameObject`                   |Direction pointer object appears when creating free “aligned” dimension |
|`alignedDimFreeModePlanePrefab`|`GameObject`                   |Direction plane object appears when creating free “aligned” dimension |
|`planePrefabScaleMultiplier`   |`float`                        |Scale direction plane to mouse position multiplier. Zero = turnOf |
|`areaHandlesScale`             |`float`                        |Scale of ``` areaHandlesPrefab ``` |
|`pointerScale`                 |`float`                        |Scale of ``` alignedDimFreeModeDirPointer ``` |
|`isDynamic`                    |`bool`                         |If true, start and end of dimension will follow the “hit point” transform |
|`linesThickness`               |`float`                        |Thickness of the “mainLine”(line between two arrows) |
|`textSize`                     |`float`                        |The size of number’s text (it’s based on “textMeshPro” font size) |
|`textOffset`                   |`float`                        |Offset between “main line” and number’s text |
|`arrowHeight`                  |`float`                        |Coefficient of arrow size. final size depends on “arrowPrefab” scale |
|`measurementDirection`         |`Funcs.MeasurementDirection`   |Direction of “Linear” dimension (multiply direction to “offsetDistance”) |
|`offsetDirection`              |`Funcs.OffsetDirection`        |Direction of offset in the “Linear” dimension |
|`measurementPlane`             |`Funcs.MeasurementPlane`       |Measurement plane for “Aligned” dimensions - { XZ, XY, ZY, Free } |
|`reverseDirection`             |`bool`                         |Flip “Aligned” dimensions in cross vector of the measurement plane |
|`offsetDistance`               |`float`                        |Length of “secondary lines” |
|`secondaryLinesThickness`      |`float`                        |Thickness of “secondary lines” |
|`secondaryLinesExtend`         |`float`                        |Length of “extends” in secondary lines |
|`autoTextPosition`             |`bool`                         |Change number’s position if distance was too short and number can’t fit |
|`flipTextPosition`             |`bool`                         |If “AutoTextPosition” was true, mirror text position |
|`angleMeasurmentPlane`         |`Funcs.AngleMeasurmentPlane`   |Measurement plane of “Angle” dimension - { XZ, XY, ZY, Free } |
|`arcScale`                     |`float`                        |Scale of the plane that carries the dimension arc |
|`angleDimTextOffsetFromCenter` |`float`                        |Distance of number from the center of the angle dimension |
|`angleDimHitNormalOffset`      |`float`                        |Offset to normal direction of the first hit point to avoid ZFighting |
|`textOffsetWhenNotFit`         |`Vector2`                      |When angle is too short, this is offset of new position |
|`areaMeasurementPlane`         |`Funcs.MeasurementPlane`       |Measurement plane of “Area” measure - { XZ, XY, ZY, Free } |
|`enableAreaBorderLine`         |`bool`                         |Show border line |
|`areaLocalYOffset`             |`float`                        |Offset in local Y direction to avoid Z-fighting |
|`areaTextLocalYOffset`         |`float`                        |Space between number’s text and area surface |
|`areaBorderLocalYOffset`       |`float`                        |Space between border and area surface |
|`areaBorderLineThickness`      |`float`                        |Thickness of the border line mesh |
|`areaNumberPositionOffset`     |`Vector2`                      |2d offset of number position |
|`numberColor`                  |`Color`                        |Color of “textMeshPro” that generates the number |
|`mainColor`                    |`Color`                        |Color of line between arrows in “PointToPoint”, “Linear” & “Aligned” dims  |
|`secondaryColor`               |`Color`                        |Color of guiding lines of “Linear” & “Aligned” dimension |
|`arrowColor`                   |`Color`                        |Color of arrows in “PointToPoint”, “Linear” & “Aligned”  dimensions  |
|`arcColor`                     |`Color`                        |Color of indicator arc of “Angle” dimension |
|`areaBorderColor`              |`Color`                        |Color of border of “Area” measure |
|`areaSurfaceColor`             |`Color`                        |Color of surface of “Area” measure |
|`hoveredTint`                  |`Color`                        |Lerp this color to colors of “hovered” dimension |
|`selectedTint`                 |`Color`                        |Lerp this color to colors of “selected” dimensions |
|`hoveredOnSelectedTint`        |`Color`                        |Lerp this color to colors of “hovered dimensions” if it was selected |
|`hitNormalOffset`              |`float`                        |Offset to normal direction of first hit point to avoid ZFighting |
|`textTowardsCameraOffset`      |`float`                        |Offset the number towards the camera to avoid intersection |
|`onSelectionChanged`           |`UnityEvent<List<GameObject>>` |Events added here will trigger when selection changes (Mouse & VR) |
|`onHovered`                    |`UnityEvent<GameObject>`       |Events added here will trigger when hovers on a dimension (Mouse & VR) |
|`pointA`                       |`Vector3`                      |Initial Position of the first hitPoint |
|`pointB`                       |`Vector3`                      |Initial Position of the second hitPoin |
|`isCreating`                   |`bool`                         |This bool turns true while creation process otherwise is false |
|`DimensionsList`               |`List<GameObject>`            |List of dimensions created from this ``` EzDimStarter ``` component |
|`SelectionList`                |`List<GameObject>`            |List of selected dimensions that created from this ``` EzDimStarter ``` component |
|`oldHoveredGo`                 |`GameObject`                   |List hovered dimension |
|`hit`                          |`RaycastHit`                   |raycast hit (feed by mouse or VR) |
|`isOldSelectionListEmpty`      |`bool`                         |This bool returns true if selection list was empty |
|`planePrefab`                  |`GameObject`                   |Plane Prefab that shows when creating aligned dimension in free mode |
|`createDimensionCort`          |`Coroutine`                    |Coroutine for creation process |
|`CreatePointToPointDimension()`|`IEnumerator`                  |Using this part of code while creating ```PointToPointDimension ``` . |
|`CreateLinearDimension()`      |`IEnumerator`                  |Using this part of code while creating ```LinearDimension ``` . |
|`CreateAlignedDimension()`     |`IEnumerator`                  |Using this part of code while creating ```AlignedDimension ``` . |
|`CreateAngleDimension()`       |`IEnumerator`                  |Using this part of code while creating ```AngleDimension ``` . |
|`CreateAreaMeasure()`          |`IEnumerator`                  |Using this part of code while creating ```AreaMeasure  ``` . |
|`EzPointToPointDimension()`    |`Method`                       |Call this void to create ```PointToPointDimension ``` when using mouse input |
|`EzLinearDimension()`          |`Method`                       |Call this void to create ```LinearDimension ``` when using mouse input |
|`EzAlignedDimension()`         |`Method`                       |Call this void to create ```AlignedDimension ``` when using mouse input |
|`EzAngledDimension()`          |`Method`                       |Call this void to create ```AngleDimension ``` when using mouse input |
|`EzAreaMeasure()`              |`Method`                       |Call this void to create ```AreaMeasure ``` when using mouse input |
|`HideSelectedDimensions()`     |`Method`                       |Call this void to hide selected dimensions when using mouse or VR input |
|`UnhideAll()`                  |`Method`                       |Call this void to unhide all dimensions when using mouse or VR input |
|`DeleteSelectedDimensions()`   |`Method`                       |Call this void to delete selected dimensions when using mouse or VR input  |
|`UpdateAll()`                  |`Method`                       |Call this void to update all dimensions when using mouse or VR input |




  
<br/><br/>




<a name="ScriptingAPI_DrawInVR">
  </a>

## DrawInVR :

<br/>

|Name                          |Type                         |Description                            |
|------------------------------|-----------------------------|---------------------------------------|
|`hoveredHit`                    |`RaycastHit`                   |``` RaycastHit ``` from ``` XRRayInteractor ```. it should send to EzDimStarter.hit |
|`rayInteractor`                 |`XRRayInteractor`              |Feed this input field by ``` XRRayInteractor ``` from one of VR controller |
|`primaryButtonPress`            |`PrimaryButtonEvent`           |Event for primary button press |
|`CreatePointToPointDimension()` |`IEnumerator`                  |Using this part of code while creating ```PointToPointDimension ``` . |
|`CreateLinearDimension()`       |`IEnumerator`                  |Using this part of code while creating ```LinearDimension ``` . |
|`CreateAlignedDimension()`      |`IEnumerator`                  |Using this part of code while creating ```AlignedDimension ``` . |
|`CreateAngleDimension()`        |`IEnumerator`                  |Using this part of code while creating ```AngleDimension ``` . |
|`CreateAreaMeasure()`           |`IEnumerator`                  |Using this part of code while creating ```AreaMeasure  ``` . |
|`VR_EzPointToPointDimension()`  |`Method`                       |Call this void to create ```PointToPointDimension ``` when using VR input |
|`VR_EzLinearDimension()`        |`Method`                       |Call this void to create ```LinearDimension ``` when using VR input |
|`VR_EzAlignedDimension()`       |`Method`                       |Call this void to create ```AlignedDimension ``` when using VR input |
|`VR_EzAngledDimension()`        |`Method`                       |Call this void to create ```AngleDimension ``` when using VR input |
|`VR_EzAreaMeasure()`            |`Method`                       |Call this void to create ```AreaMeasure ``` when using VR input |
|`VR_HighlightHoveredDimension()`|`Method`                       |This void will call when using VR from ``` EzDimStarter ``` using ``` gameObject.SendMessage() ``` |
|`VR_SelectDimension()`          |`Method`                       |This void will call when using VR from ``` EzDimStarter ``` using ``` gameObject.SendMessage() ```  |
  
<br/><br/>

---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

---

<br/><br/>

[//]: # (-----------------------------------# Contact :----------------------------------)

<a name="Contact">
  </a>
  

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" width="64" height="64" align="right" hspace="0">
  <h1>Contact :</h1>
</p>

If you require immediate assistance, you can contact me through Telegram Messenger. However, please only use this method in urgent situations. For general inquiries, please email me, and I will try to respond your message within 24 hours. If there is any delay in my response, please do not worry as I will get back to you as soon as possible.

You can send me a direct message or email by CTRL+click (on Windows and Linux) or CMD+click (on MacOS) on the icons below. Your feedback and bug reports are valuable to us, and we appreciate your input.

Thank you,
Eisa Shadmani.

<a href="mailto:isa.shademani@gmail.com" title="Send e-mail"><img src="https://user-images.githubusercontent.com/88411269/219762727-974e0a58-b667-4f1a-bd55-2a6a94624194.png" alt="image with tooltip" width="40" height="40"></a>
[<img src="https://user-images.githubusercontent.com/88411269/219762446-6a47512e-251b-4135-841e-ee4e1f5e3d0f.png" alt="image with tooltip" width="40" height="40">](https://t.me/itseisa "Send Message")

---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")


---

<br/><br/>

[//]: # (-----------------------------------# Download :----------------------------------)

<a name="Download">
  </a>
  

<p>
  <img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" width="64" height="64" align="right" hspace="0">
  <h1>Download :</h1>
</p>

This package will soon be available on the Unity Asset Store. We will provide the purchase link as soon as it is published.

---

[<img src="https://user-images.githubusercontent.com/88411269/219645282-c0306215-ca1e-4197-96c7-8379672f75b4.png" alt="image with tooltip" width="40" height="40">](#Introduction "Go to introduction")
[<img src="https://user-images.githubusercontent.com/88411269/219619899-da8e937c-7bae-48a0-8992-acfacd1df29f.png" alt="image with tooltip" width="40" height="40">](#ListOfContents "Go to list of contents")
[<img src="https://user-images.githubusercontent.com/88411269/219728907-9b61862e-e35b-4d91-8d96-62dbc890d7f8.png" alt="image with tooltip" width="40" height="40">](#RoadMap "Go to Road Map")
[<img src="https://user-images.githubusercontent.com/88411269/219729075-a7d27fc6-9c34-42be-adc3-f610c0d77f40.png" alt="image with tooltip" width="40" height="40">](#Limits "Go to Known Limitations of Easy Dimension")
[<img src="https://user-images.githubusercontent.com/88411269/219647914-f014ed12-2e5c-425d-b604-0da18453ef06.png" alt="image with tooltip" width="40" height="40">](#Dependencies "Go to dependencies")
[<img src="https://user-images.githubusercontent.com/88411269/219648415-9919a52a-e5eb-45bd-97ee-581fca6f0cee.png" alt="image with tooltip" width="40" height="40">](#QuickStart "Go to quick start")
[<img src="https://user-images.githubusercontent.com/88411269/219654869-d21de237-5422-4ff4-93dc-ff2e0d1d417c.png" alt="image with tooltip" width="40" height="40">](#SettingsNotes "Go to Settings Notes")
[<img src="https://user-images.githubusercontent.com/88411269/219646219-e6a6bcaf-617a-4eee-a909-485c5692c3ff.png" alt="image with tooltip" width="40" height="40">](#DimensionTypes "Go to Dimension Types")
[<img src="https://user-images.githubusercontent.com/88411269/219649472-5ad5a904-a434-4bc6-900f-2d645ec347fb.png" alt="image with tooltip" width="40" height="40">](#ScriptingManual "Go to Scripting Manual")
[<img src="https://user-images.githubusercontent.com/88411269/219649947-165046ae-42cc-4375-ad01-574a4c3a2f27.png" alt="image with tooltip" width="40" height="40">](#ScriptingAPI "Go to Scripting API")
[<img src="https://user-images.githubusercontent.com/88411269/219780402-4d6a2eeb-d44d-4f62-aad0-7775a103f6c7.png" alt="image with tooltip" width="40" height="40">](#Contact "Go to Contact")
[<img src="https://user-images.githubusercontent.com/88411269/219781010-26fb9216-8f4e-4eb8-ae74-6a2ca40af537.png" alt="image with tooltip" width="40" height="40">](#Download "Go to Download")

---


[//]: # (#-----------------------------------images used in unity forum ----------------------------------)

[//]: # (#https://user-images.githubusercontent.com/88411269/232197492-8bad87f7-77d5-493c-a542-18fcefc7dd9e.jpg)

[//]: # (#https://user-images.githubusercontent.com/88411269/232197536-8bace0f7-aad9-43b4-8da0-d0e45b9978f1.jpg)

[//]: # (#https://user-images.githubusercontent.com/88411269/232197641-c7b9c4c2-d6f0-4366-aea1-db047b5d5809.jpg)

[//]: # (#https://user-images.githubusercontent.com/88411269/232197692-6b67abc0-3b58-4de9-a1db-eff21bc92d1d.jpg)

[//]: # (#https://user-images.githubusercontent.com/88411269/232197719-0cd96446-d4d3-4b17-8fbe-61e471f266f9.jpg)

[//]: # (#https://user-images.githubusercontent.com/88411269/232197770-65adf740-3588-43d9-9d4d-292fa70dccbe.jpg)

[//]: # (#https://user-images.githubusercontent.com/88411269/232197793-badeea7a-c911-4063-a99c-2f6f5661bf6d.jpg)

[//]: # (#https://user-images.githubusercontent.com/88411269/232199336-1ee90735-a6d9-457b-acf7-eaf9e3244477.png)
