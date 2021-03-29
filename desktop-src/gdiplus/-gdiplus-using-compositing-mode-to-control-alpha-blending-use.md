---
description: 有時候您可能會想要建立具有下列特性的非螢幕點陣圖：
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: 使用複合模式控制 Alpha 混色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972828"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="368bf-103">使用複合模式控制 Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="368bf-103">Using Compositing Mode to Control Alpha Blending</span></span>

<span data-ttu-id="368bf-104">有時候您可能會想要建立具有下列特性的非螢幕點陣圖：</span><span class="sxs-lookup"><span data-stu-id="368bf-104">There might be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>

-   <span data-ttu-id="368bf-105">色彩的 Alpha 值小於255。</span><span class="sxs-lookup"><span data-stu-id="368bf-105">Colors have alpha values that are less than 255.</span></span>
-   <span data-ttu-id="368bf-106">當您建立點陣圖時，色彩不會加上 Alpha 的混合。</span><span class="sxs-lookup"><span data-stu-id="368bf-106">Colors are not alpha blended with each other as you create the bitmap.</span></span>
-   <span data-ttu-id="368bf-107">當您顯示完成的點陣圖時，點陣圖中的色彩會與顯示裝置上的背景色彩混合使用 Alpha。</span><span class="sxs-lookup"><span data-stu-id="368bf-107">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>

<span data-ttu-id="368bf-108">若要建立這類點陣圖，請建立一個空白 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件，然後根據該點陣圖來建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。</span><span class="sxs-lookup"><span data-stu-id="368bf-108">To create such a bitmap, construct a blank [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object, and then construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on that bitmap.</span></span> <span data-ttu-id="368bf-109">將 **圖形** 物件的合成模式設定為 CompositingModeSourceCopy。</span><span class="sxs-lookup"><span data-stu-id="368bf-109">Set the compositing mode of the **Graphics** object to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="368bf-110">下列範例會根據 [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)物件建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件。</span><span class="sxs-lookup"><span data-stu-id="368bf-110">The following example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="368bf-111">程式碼會使用 **Graphics** 物件，以及兩個半透明筆刷 (Alpha = 160) 在點陣圖上繪製。</span><span class="sxs-lookup"><span data-stu-id="368bf-111">The code uses the **Graphics** object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="368bf-112">程式碼會使用半透明筆刷來填滿紅色橢圓形和綠色橢圓形。</span><span class="sxs-lookup"><span data-stu-id="368bf-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="368bf-113">綠色橢圓形與紅色橢圓形重迭，但綠色不會與紅色混合，因為 **Graphics** 物件的合成模式設定為 CompositingModeSourceCopy。</span><span class="sxs-lookup"><span data-stu-id="368bf-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the **Graphics** object is set to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="368bf-114">接下來，程式碼會呼叫 [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) ，並根據裝置內容建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，以準備在螢幕上繪製。</span><span class="sxs-lookup"><span data-stu-id="368bf-114">Next the code prepares to draw on the screen by calling [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) and creating a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a device context.</span></span> <span data-ttu-id="368bf-115">程式碼會在螢幕上繪製點陣圖兩次：一次在白色背景上，一次在彩色背景上。</span><span class="sxs-lookup"><span data-stu-id="368bf-115">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="368bf-116">點陣圖中屬於兩個省略號的圖元具有 Alpha 元件160，因此省略號會與螢幕上的背景色彩混合。</span><span class="sxs-lookup"><span data-stu-id="368bf-116">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



<span data-ttu-id="368bf-117">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="368bf-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="368bf-118">請注意，省略號會與背景混合，但是它們不會互相混合。</span><span class="sxs-lookup"><span data-stu-id="368bf-118">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>

![顯示兩個不同色彩橢圓形的圖例，其中每個橢圓形都會與彩色色彩混合](images/sourcecopy.png)

<span data-ttu-id="368bf-120">上述程式碼範例具有下列語句：</span><span class="sxs-lookup"><span data-stu-id="368bf-120">The preceding code example has the following statement:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



<span data-ttu-id="368bf-121">如果您想要讓省略號彼此混合以及背景，請將該語句變更為下列內容：</span><span class="sxs-lookup"><span data-stu-id="368bf-121">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



<span data-ttu-id="368bf-122">下圖顯示修改過的程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="368bf-122">The following illustration shows the output of the revised code.</span></span>

![使用複合模式控制 Alpha 混色圖](images/sourceover.png)

 

 



