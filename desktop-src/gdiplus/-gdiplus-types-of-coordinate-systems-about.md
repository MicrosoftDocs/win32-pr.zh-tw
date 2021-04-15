---
description: Windows GDI + 會使用三個座標空間：世界、頁面和裝置。
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: 座標系統類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05908196662918eb93f4fa6e2b356a6989ed5a58
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104561546"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="1f7a0-103">座標系統類型</span><span class="sxs-lookup"><span data-stu-id="1f7a0-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="1f7a0-104">Windows GDI + 會使用三個座標空間：世界、頁面和裝置。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="1f7a0-105">當您進行呼叫時 `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` ，您傳遞給圖形的點 [**：:D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) 方法（ (0、0) 和 (160、80) ）位於全局座標空間中。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="1f7a0-106">在 GDI + 可以在螢幕上繪製線條之前，座標會傳遞一連串的轉換。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="1f7a0-107">一個轉換會將全局座標轉換成頁面座標，而另一個轉換會將頁面座標轉換成裝置座標。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="1f7a0-108">假設您想要使用在用戶端區域主體中，而不是左上角的座標系統。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="1f7a0-109">例如，假設您想要原點從工作區的左邊緣到100圖元，並從工作區的最上方取得50圖元。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="1f7a0-110">下圖顯示這類座標系統。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-110">The following illustration shows such a coordinate system.</span></span>

![包含標示座標軸之視窗的螢幕擷取畫面](images/aboutgdip05-art01.png)

<span data-ttu-id="1f7a0-112">當您進行呼叫時 `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` ，會取得下圖所示的行。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![上一個視窗的螢幕擷取畫面，但具有從原點對角線擴充的藍線](images/aboutgdip05-art02.png)

<span data-ttu-id="1f7a0-114">在三個座標空間中，線條的端點座標如下所示：</span><span class="sxs-lookup"><span data-stu-id="1f7a0-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="1f7a0-115">World</span><span class="sxs-lookup"><span data-stu-id="1f7a0-115">World</span></span>  | <span data-ttu-id="1f7a0-116"> (0、0)  (160、80) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-116">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="1f7a0-117">頁面</span><span class="sxs-lookup"><span data-stu-id="1f7a0-117">Page</span></span>   | <span data-ttu-id="1f7a0-118"> (100、50)  (260、130) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-118">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="1f7a0-119">裝置</span><span class="sxs-lookup"><span data-stu-id="1f7a0-119">Device</span></span> | <span data-ttu-id="1f7a0-120"> (100、50)  (260、130) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-120">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="1f7a0-121">請注意，頁面座標空間的原點位於工作區的左上角;這一律會是這種情況。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-121">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="1f7a0-122">另請注意，由於測量單位是圖元，因此裝置座標與頁面座標相同。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-122">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="1f7a0-123">如果您將量值的單位設定為圖元以外的某個值 (例如，[英寸]) ，則裝置座標將會與頁面座標不同。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-123">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="1f7a0-124">將全局座標對應到頁面座標的轉換稱為「 *世界」轉換* ，而且是由 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件所維護。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-124">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="1f7a0-125">在上述範例中，全球轉換是 x 方向的平移100單位和 y 方向的50單位。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-125">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="1f7a0-126">下列範例會設定 **圖形** 物件的世界轉換，然後使用該 **圖形** 物件來繪製上圖所示的線條。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-126">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="1f7a0-127">將頁面座標對應至裝置座標的轉換稱為「 *頁面」轉換*。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-127">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="1f7a0-128">[**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別提供四種方法來操作和檢查頁面轉換： [**Graphics：： SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit)、 [**graphics：： GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit)、 [**graphics：： SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)和 [**Graphics：： GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale)。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-128">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="1f7a0-129">**Graphics** 類別也提供兩種方法，也就是 [**圖形：： GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix)和 [**Graphics：： GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy)，用於檢查顯示裝置的每英寸水準和垂直點。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-129">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="1f7a0-130">您可以使用 [**graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [**Graphics：： SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit)方法來指定測量單位。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-130">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="1f7a0-131">下列範例會從 (0、0) 到 (2、1) ，其中 point (2，1) 是2英寸左右，1英寸從點 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-131">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="1f7a0-132">如果您在建立畫筆時未指定畫筆寬度，則上一個範例會繪製寬度為一的線條。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-132">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="1f7a0-133">您可以將第二個引數中的畫筆寬度指定為 [**畫筆**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 的函式：</span><span class="sxs-lookup"><span data-stu-id="1f7a0-133">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="1f7a0-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="1f7a0-135">如果我們假設顯示裝置的水準方向有96個點，而垂直方向的96點為每英寸，則上一個範例中的線條端點在三個座標空間中具有下列座標：</span><span class="sxs-lookup"><span data-stu-id="1f7a0-135">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                     |
|--------|---------------------|
| <span data-ttu-id="1f7a0-136">World</span><span class="sxs-lookup"><span data-stu-id="1f7a0-136">World</span></span>  | <span data-ttu-id="1f7a0-137"> (0、0) 至 (2、1) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-137">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="1f7a0-138">頁面</span><span class="sxs-lookup"><span data-stu-id="1f7a0-138">Page</span></span>   | <span data-ttu-id="1f7a0-139"> (0、0) 至 (2、1) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-139">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="1f7a0-140">裝置</span><span class="sxs-lookup"><span data-stu-id="1f7a0-140">Device</span></span> | <span data-ttu-id="1f7a0-141"> (0、0、 (192、96) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-141">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="1f7a0-142">您可以結合世界和頁面轉換來達成各種效果。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-142">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="1f7a0-143">例如，假設您想要使用英寸作為度量單位，而您想要將座標系統的原點從工作區的左邊緣到2英寸，從工作區的最上方開始為1/2 英寸。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-143">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="1f7a0-144">下列範例會設定 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界和頁面轉換，然後從 (0，0) 到 (2，1) 繪製線條。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-144">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="1f7a0-145">下圖顯示線條和座標系統。</span><span class="sxs-lookup"><span data-stu-id="1f7a0-145">The following illustration shows the line and coordinate system.</span></span>

![上一個視窗的螢幕擷取畫面，但範圍較寬，且軸位於左方且標示不同](images/aboutgdip05-art03.png)

<span data-ttu-id="1f7a0-147">如果我們假設顯示裝置的水準方向有96個點，而垂直方向的96點為每英寸，則上一個範例中的線條端點在三個座標空間中具有下列座標：</span><span class="sxs-lookup"><span data-stu-id="1f7a0-147">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="1f7a0-148">World</span><span class="sxs-lookup"><span data-stu-id="1f7a0-148">World</span></span>  | <span data-ttu-id="1f7a0-149"> (0、0) 至 (2、1) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-149">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="1f7a0-150">頁面</span><span class="sxs-lookup"><span data-stu-id="1f7a0-150">Page</span></span>   | <span data-ttu-id="1f7a0-151"> (2、0.5) 至 (4、1.5) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-151">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="1f7a0-152">裝置</span><span class="sxs-lookup"><span data-stu-id="1f7a0-152">Device</span></span> | <span data-ttu-id="1f7a0-153"> (192、48)  (384、144) </span><span class="sxs-lookup"><span data-stu-id="1f7a0-153">(192, 48) to (384, 144)</span></span> |



 

 

 
