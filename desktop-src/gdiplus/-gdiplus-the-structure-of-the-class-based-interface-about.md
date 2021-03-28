---
description: Windows GDI + 的 c + + 介面包含大約40個類別、50列舉和6個結構。 另外還有一些函數不是任何類別的成員。
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: 以類別為基礎的介面結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2627d695330c316a57c2593e75233d73b27a1524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991094"
---
# <a name="the-structure-of-the-class-based-interface"></a>以類別為基礎的介面結構

Windows GDI + 的 c + + 介面包含大約40個類別、50列舉和6個結構。 另外還有一些函數不是任何類別的成員。

在呼叫任何 GDI + 函式之前，您必須先指出命名空間 Gdiplus.dll 正在使用中。 下列語句表示應用程式中正在使用 Gdiplus.dll 命名空間。

`using namespace Gdiplus;`

[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別是 gdi + 介面的核心;它是實際繪製線條、曲線、圖形、影像和文字的類別。

許多類別都與 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別一起運作。 例如， [Graphics：:D rawline](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) 方法會接收 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件的指標，以保存屬性 (色彩、寬度、虛線樣式，以及要繪製之線條的類似) 。 [Graphics：： graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_))方法可以接收 [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)物件的指標，此物件可與 **圖形** 物件搭配使用，以逐漸變更的色彩填滿矩形。 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 和 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) 物件會影響 **圖形** 物件繪製文字的方式。 [**矩陣**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)物件會儲存並操作 **圖形** 物件的全球轉換，以用來旋轉、縮放和翻轉影像。

某些類別主要是做為結構化資料類型。 其中有些類別 (例如， [**矩形**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect)、 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)和 [**大小**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)) 適用于一般用途。 其他則適用于專用用途，並被視為 helper 類別。 例如， [**BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) 類別是 [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 類別的協助程式，而 [**PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) 類別是 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 類別的 helper。 GDI + 也會定義一些用於組織資料的結構。 例如， [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) 結構會保存一組在色彩轉換表中形成一個專案的 [**色彩**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 物件。

GDI + 定義數個列舉，也就是相關常數的集合。 例如， [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) 列舉包含元素 [* * * * LineJoinBevel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *、* * * * [LineJoinMiter * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* * 和 * * * * [LineJoinRound *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* * *，這會指定可用來聯結兩行的樣式。

GDI + 提供幾個不屬於任何類別的函式。 其中兩個函數是 [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) 和 [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown)。 您必須在進行任何其他 GDI + 呼叫之前呼叫 **GdiplusStartup** ，而且當您使用 gdi + 完成時，必須呼叫 **GdiplusShutdown** 。

 

 
