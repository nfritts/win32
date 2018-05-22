---
title: VML Gamma Attribute
description: VML Gamma Attribute
ms.assetid: '47a4d10e-f5ef-457b-92dd-bce5dae59b1c'
---

# VML Gamma Attribute

This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9. Webpages and applications that rely on VML should be [migrated to SVG](http://go.microsoft.com/fwlink/p/?LinkID=236964) or other widely supported standards.

> [!Note]  
> As of December 2011, this topic has been archived. As a result, it is no longer actively maintained. For more information, see [Archived Content](https://msdn.microsoft.com/library/hh772377). For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](http://go.microsoft.com/fwlink/p/?linkid=204313).

 

Defines the amount of contrast for an image. Read/write. **VgNumber**.

**Applies To**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tag Syntax**

&lt;v: *element* gamma=" *expression* "&gt;

**Script Syntax**

*element* .gamma="*expression*"

*expression*=*element*.gamma

**Remarks**

Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast. Useful values are from 0.3 to about 3. The default value is 0.

*VML Standard Attribute*

**Example**


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 



