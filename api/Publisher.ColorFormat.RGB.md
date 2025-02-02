---
title: ColorFormat.RGB property (Publisher)
keywords: vbapb10.chm2555904
f1_keywords:
- vbapb10.chm2555904
ms.prod: publisher
api_name:
- Publisher.ColorFormat.RGB
ms.assetid: aeff1962-b855-7c3f-1f4d-a336e0739ade
ms.date: 06/06/2019
ms.localizationpriority: medium
---


# ColorFormat.RGB property (Publisher)

Returns or sets a **[PbColorType](publisher.pbcolortype.md)** constant that represents the red-green-blue (RGB) value of the specified color. Read/write.


## Syntax

_expression_.**RGB**

_expression_ A variable that represents a **[ColorFormat](Publisher.ColorFormat.md)** object.


## Return value

PbColorType


## Example

This example creates a new shape on the first page of the active publication and sets the fill color to red.

```vb
Sub SetFill() 
 ActiveDocument.Pages(1).Shapes.AddShape(Type:=msoShape5pointStar, _ 
 Left:=100, Top:=100, Width:=100, Height:=100).Fill.ForeColor _ 
 .RGB = RGB(Red:=255, Green:=0, Blue:=0) 
End Sub
```

<br/>

This example returns the value of the foreground color of the first shape on the first page of the active document. This example assumes that there is at least one shape on the first page of the active publication.

```vb
Sub ShowFillColor() 
 MsgBox "The RGB fill value of this shape is " & _ 
 ActiveDocument.Pages(1).Shapes(1).Fill.ForeColor.RGB & "." 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]