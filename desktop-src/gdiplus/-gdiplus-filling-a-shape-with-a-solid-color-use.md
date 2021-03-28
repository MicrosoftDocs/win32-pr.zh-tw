---
description: 若要以純色填滿圖形，請建立 SolidBrush 物件，然後將該 SolidBrush 物件的位址當作引數傳遞至 Graphics 類別的其中一個 fill 方法。
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: 以純色填滿形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991354"
---
# <a name="filling-a-shape-with-a-solid-color"></a><span data-ttu-id="cb18c-103">以純色填滿形狀</span><span class="sxs-lookup"><span data-stu-id="cb18c-103">Filling a Shape with a Solid Color</span></span>

<span data-ttu-id="cb18c-104">若要以純色填滿圖形，請建立 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 物件，然後將該 **SolidBrush** 物件的位址當作引數傳遞至 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的其中一個 fill 方法。</span><span class="sxs-lookup"><span data-stu-id="cb18c-104">To fill a shape with a solid color, create a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object, and then pass the address of that **SolidBrush** object as an argument to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="cb18c-105">下列範例顯示如何使用紅色的紅色填滿橢圓形：</span><span class="sxs-lookup"><span data-stu-id="cb18c-105">The following example shows how to fill an ellipse with the color red:</span></span>


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



<span data-ttu-id="cb18c-106">在上述範例中， [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 的函式會採用 [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) 物件參考做為其唯一的引數。</span><span class="sxs-lookup"><span data-stu-id="cb18c-106">In the preceding example, the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor takes a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object reference as its only argument.</span></span> <span data-ttu-id="cb18c-107">**色彩** 的函式所使用的值代表色彩的 Alpha、紅色、綠色和藍色元件。</span><span class="sxs-lookup"><span data-stu-id="cb18c-107">The values used by the **Color** constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="cb18c-108">這些值的每一個都必須在0到255的範圍內。</span><span class="sxs-lookup"><span data-stu-id="cb18c-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="cb18c-109">第一個255表示色彩完全不透明，而第二個255表示紅色元件的強度已滿。</span><span class="sxs-lookup"><span data-stu-id="cb18c-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="cb18c-110">這兩個零表示綠色和藍色元件的強度都是0。</span><span class="sxs-lookup"><span data-stu-id="cb18c-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>

<span data-ttu-id="cb18c-111">傳遞至 [**Graphics：： FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) 方法的四個數字 (0、0、100、60) 指定橢圓形的周框矩形位置和大小。</span><span class="sxs-lookup"><span data-stu-id="cb18c-111">The four numbers (0, 0, 100, 60) passed to the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="cb18c-112">矩形左上角的 (0、0) 、寬度為100、高度為60。</span><span class="sxs-lookup"><span data-stu-id="cb18c-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>

 

 
