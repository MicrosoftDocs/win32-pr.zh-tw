---
description: 若要繪製線條和矩形，您需要繪圖物件和 Pen 物件。 Graphics 物件提供 DrawLine 方法，而 Pen 物件會儲存線條的功能，例如色彩和寬度。
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: 使用畫筆繪製線條和矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943940"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a><span data-ttu-id="c6aad-104">使用畫筆繪製線條和矩形</span><span class="sxs-lookup"><span data-stu-id="c6aad-104">Using a Pen to Draw Lines and Rectangles</span></span>

<span data-ttu-id="c6aad-105">若要繪製線條和矩形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。</span><span class="sxs-lookup"><span data-stu-id="c6aad-105">To draw lines and rectangles, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="c6aad-106">**Graphics** 物件提供 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法，而 **Pen** 物件會儲存線條的功能，例如色彩和寬度。</span><span class="sxs-lookup"><span data-stu-id="c6aad-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores features of the line, such as color and width.</span></span>

<span data-ttu-id="c6aad-107">下列範例會繪製從 (20，10) 到 (300，100) 的行。</span><span class="sxs-lookup"><span data-stu-id="c6aad-107">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="c6aad-108">假設 **圖形** 是現有的 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。</span><span class="sxs-lookup"><span data-stu-id="c6aad-108">Assume **graphics** is an existing [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



<span data-ttu-id="c6aad-109">第一個程式碼語句會使用 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 類別的函式來建立黑色畫筆。</span><span class="sxs-lookup"><span data-stu-id="c6aad-109">The first statement of code uses the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) class constructor to create a black pen.</span></span> <span data-ttu-id="c6aad-110">傳遞給 **畫筆** 參數的一個引數是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 物件。</span><span class="sxs-lookup"><span data-stu-id="c6aad-110">The one argument passed to the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="c6aad-111">用來建立 **色彩** 物件的值（ (255、0、0、0) ）會對應至色彩的 Alpha、紅色、綠色和藍色元件。</span><span class="sxs-lookup"><span data-stu-id="c6aad-111">The values used to construct the **Color** object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="c6aad-112">這些值會定義不透明的黑色畫筆。</span><span class="sxs-lookup"><span data-stu-id="c6aad-112">These values define an opaque black pen.</span></span>

<span data-ttu-id="c6aad-113">下列範例會繪製一個矩形，其左上角位於 (10，10) 。</span><span class="sxs-lookup"><span data-stu-id="c6aad-113">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="c6aad-114">矩形的寬度為100，高度為50。</span><span class="sxs-lookup"><span data-stu-id="c6aad-114">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="c6aad-115">傳遞給 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 表示函式的第二個引數表示畫筆寬度為5圖元。</span><span class="sxs-lookup"><span data-stu-id="c6aad-115">The second argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor indicates that the pen width is 5 pixels.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



<span data-ttu-id="c6aad-116">繪製矩形時，畫筆會以矩形的界限為中心。</span><span class="sxs-lookup"><span data-stu-id="c6aad-116">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="c6aad-117">因為畫筆寬度為5，所以矩形的側邊繪製的寬度為5圖元，因此會在界限本身繪製1圖元、在內部繪製2圖元，並在外部繪製2個圖元。</span><span class="sxs-lookup"><span data-stu-id="c6aad-117">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="c6aad-118">如需畫筆對齊的詳細資訊，請參閱 [設定畫筆寬度和對齊方式](-gdiplus-setting-pen-width-and-alignment-use.md)。</span><span class="sxs-lookup"><span data-stu-id="c6aad-118">For more details on pen alignment, see [Setting Pen Width and Alignment](-gdiplus-setting-pen-width-and-alignment-use.md).</span></span>

<span data-ttu-id="c6aad-119">下圖顯示產生的矩形。</span><span class="sxs-lookup"><span data-stu-id="c6aad-119">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="c6aad-120">如果畫筆寬度為一個圖元，則虛線會顯示繪製矩形的位置。</span><span class="sxs-lookup"><span data-stu-id="c6aad-120">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="c6aad-121">矩形左上角的放大視圖會顯示黑色黑色線條會置於這些虛線的中央。</span><span class="sxs-lookup"><span data-stu-id="c6aad-121">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>

![以黑色黑色線條繪製的矩形圖例，該線條周圍會圍住細灰色的虛線](images/pens1.png)

 

 



