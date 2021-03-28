---
description: 圖形類別的其中一個屬性是裁剪區域。 給定繪圖物件所完成的所有繪製，都會限制為該繪圖物件的裁剪區域。 您可以藉由呼叫 SetClip 方法來設定裁剪區域。
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: 使用區域裁剪
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa19426d62d5d3af99150bf9ac8e8099628fe2f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551548"
---
# <a name="clipping-with-a-region"></a>使用區域裁剪

[**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的其中一個屬性是裁剪區域。 給定 **圖形** 物件所完成的所有繪製，都會限制為該 **圖形** 物件的裁剪區域。 您可以藉由呼叫 **SetClip** 方法來設定裁剪區域。

下列範例會建立包含單一多邊形的路徑。 然後，程式碼會根據該路徑來建立區域。 區域的位址會傳遞給 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 **SetClip** 方法，然後繪製兩個字串。


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



下圖顯示已裁剪的字串。

![顯示四邊形內出現的兩個句子部分的圖例](images/clip1.png)

 

 



