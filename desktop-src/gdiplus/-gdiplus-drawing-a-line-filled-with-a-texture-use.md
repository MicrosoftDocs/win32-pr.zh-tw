---
description: 您可以使用材質繪製，而不是以純色繪製線條或曲線。
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: 繪製填滿材質的線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6a061399791009fd7c1b645bb09dbba25362f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972897"
---
# <a name="drawing-a-line-filled-with-a-texture"></a><span data-ttu-id="1617c-103">繪製填滿材質的線條</span><span class="sxs-lookup"><span data-stu-id="1617c-103">Drawing a Line Filled with a Texture</span></span>

<span data-ttu-id="1617c-104">您可以使用材質繪製，而不是以純色繪製線條或曲線。</span><span class="sxs-lookup"><span data-stu-id="1617c-104">Instead of drawing a line or curve with a solid color, you can draw with a texture.</span></span> <span data-ttu-id="1617c-105">若要使用材質繪製線條和曲線，請建立 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 物件，並將該 **TextureBrush** 物件的位址傳遞給 [**畫筆**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 的函式。</span><span class="sxs-lookup"><span data-stu-id="1617c-105">To draw lines and curves with a texture, create a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and pass the address of that **TextureBrush** object to a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor.</span></span> <span data-ttu-id="1617c-106">與材質筆刷相關聯的影像會用來將平面 (為不可見的) ，而且當畫筆繪製線條或曲線時，畫筆的筆觸會顯示磚材質的特定圖元。</span><span class="sxs-lookup"><span data-stu-id="1617c-106">The image associated with the texture brush is used to tile the plane (invisibly), and when the pen draws a line or curve, the stroke of the pen uncovers certain pixels of the tiled texture.</span></span>

<span data-ttu-id="1617c-107">下列範例會從檔案 Texture1.jpg 建立 [**映射**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="1617c-107">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Texture1.jpg.</span></span> <span data-ttu-id="1617c-108">該映射是用來建立 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 物件，而 **TextureBrush** 物件則是用來建立 [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 物件。</span><span class="sxs-lookup"><span data-stu-id="1617c-108">That image is used to construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and the **TextureBrush** object is used to construct a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="1617c-109">圖形的呼叫 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) 會繪製影像，其左上角為 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="1617c-109">The call to [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) draws the image with its upper-left corner at (0, 0).</span></span> <span data-ttu-id="1617c-110">對圖形的呼叫 [**：:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 使用 **Pen** 物件來繪製有紋理的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="1617c-110">The call to [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) uses the **Pen** object to draw a textured ellipse.</span></span>


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



<span data-ttu-id="1617c-111">下圖顯示影像和紋理橢圓形。</span><span class="sxs-lookup"><span data-stu-id="1617c-111">The following illustration shows the image and the textured ellipse.</span></span>

![顯示小型矩形影像的圖例，以及填滿原始影像的橢圓線條區段](images/pens7.png)

 

 
