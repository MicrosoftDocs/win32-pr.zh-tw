---
description: Graphics 類別是 Windows GDI + 的核心。 若要繪製任何內容，您可以建立繪圖物件、設定其屬性，以及呼叫其方法 ( DrawLine、DrawImage、DrawString 和 like) 。
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: 圖形物件的狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550626"
---
# <a name="the-state-of-a-graphics-object"></a><span data-ttu-id="1fba6-104">圖形物件的狀態</span><span class="sxs-lookup"><span data-stu-id="1fba6-104">The State of a Graphics Object</span></span>

<span data-ttu-id="1fba6-105">[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別是 WINDOWS gdi + 的核心。</span><span class="sxs-lookup"><span data-stu-id="1fba6-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is at the heart of Windows GDI+.</span></span> <span data-ttu-id="1fba6-106">若要繪製任何內容，您可以建立 **圖形** 物件、設定其屬性，以及呼叫其方法 ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))、 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))、 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))和 like) 。</span><span class="sxs-lookup"><span data-stu-id="1fba6-106">To draw anything, you create a **Graphics** object, set its properties, and call its methods ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)), and the like).</span></span>

<span data-ttu-id="1fba6-107">下列範例會建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件，然後呼叫 **graphics 物件** 的 [**graphics：:D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))方法：</span><span class="sxs-lookup"><span data-stu-id="1fba6-107">The following example constructs a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and then calls the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object:</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



<span data-ttu-id="1fba6-108">在上述程式碼中， [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) 方法會將控制碼傳回至裝置內容，並將該控制碼傳遞給 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。</span><span class="sxs-lookup"><span data-stu-id="1fba6-108">In the preceding code, the [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) method returns a handle to a device context, and that handle is passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="1fba6-109">裝置內容是由 Windows) 所維護的結構 (，其中保存所使用之特定顯示裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1fba6-109">A device context is a structure (maintained by Windows) that holds information about the particular display device being used.</span></span>

## <a name="graphics-state"></a><span data-ttu-id="1fba6-110">圖形狀態</span><span class="sxs-lookup"><span data-stu-id="1fba6-110">Graphics State</span></span>

<span data-ttu-id="1fba6-111">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件會比提供繪圖方法更多，例如 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))和 [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))。</span><span class="sxs-lookup"><span data-stu-id="1fba6-111">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object does more than provide drawing methods, such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span></span> <span data-ttu-id="1fba6-112">**圖形** 物件也會維持圖形狀態，可分為下列類別：</span><span class="sxs-lookup"><span data-stu-id="1fba6-112">A **Graphics** object also maintains graphics state, which can be divided into the following categories:</span></span>

-   <span data-ttu-id="1fba6-113">裝置內容的連結</span><span class="sxs-lookup"><span data-stu-id="1fba6-113">A link to a device context</span></span>
-   <span data-ttu-id="1fba6-114">品質設定</span><span class="sxs-lookup"><span data-stu-id="1fba6-114">Quality settings</span></span>
-   <span data-ttu-id="1fba6-115">轉換</span><span class="sxs-lookup"><span data-stu-id="1fba6-115">Transformations</span></span>
-   <span data-ttu-id="1fba6-116">裁剪區域</span><span class="sxs-lookup"><span data-stu-id="1fba6-116">A clipping region</span></span>

### <a name="device-context"></a><span data-ttu-id="1fba6-117">裝置內容</span><span class="sxs-lookup"><span data-stu-id="1fba6-117">Device Context</span></span>

<span data-ttu-id="1fba6-118">作為應用程式的程式設計人員，您不需要考慮 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件與其裝置內容之間的互動。</span><span class="sxs-lookup"><span data-stu-id="1fba6-118">As an application programmer, you don't have to think about the interaction between a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and its device context.</span></span> <span data-ttu-id="1fba6-119">這項互動是由 GDI + 在幕後處理。</span><span class="sxs-lookup"><span data-stu-id="1fba6-119">This interaction is handled by GDI+ behind the scenes.</span></span>

### <a name="quality-settings"></a><span data-ttu-id="1fba6-120">品質設定</span><span class="sxs-lookup"><span data-stu-id="1fba6-120">Quality Settings</span></span>

<span data-ttu-id="1fba6-121">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件有數個屬性，會影響在螢幕上繪製的專案品質。</span><span class="sxs-lookup"><span data-stu-id="1fba6-121">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object has several properties that influence the quality of the items that are drawn on the screen.</span></span> <span data-ttu-id="1fba6-122">您可以藉由呼叫 get 和 set 方法來查看和操作這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1fba6-122">You can view and manipulate these properties by calling get and set methods.</span></span> <span data-ttu-id="1fba6-123">例如，您可以呼叫 [**Graphics：： SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) 方法來指定要套用至文字的任何) 的消除鋸齒類型 (。</span><span class="sxs-lookup"><span data-stu-id="1fba6-123">For example, you can call the [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="1fba6-124">影響品質的其他 set 方法如下 [**： graphics：： SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode)、 [**Graphics：： SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode)、 [**Graphics：： SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)和 [**Graphics：： SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode)。</span><span class="sxs-lookup"><span data-stu-id="1fba6-124">Other set methods that influence quality are [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality), and [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span></span>

<span data-ttu-id="1fba6-125">下列範例會繪製兩個省略號，一個將平滑模式設定為 [\* \* \* \* SmoothingModeAntiAlias \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) \* *，另一個則將平滑模式設定為 [\* \* \* \* SmoothingModeHighSpeed \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* \* \*：</span><span class="sxs-lookup"><span data-stu-id="1fba6-125">The following example draws two ellipses, one with the smoothing mode set to [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) and one with the smoothing mode set to [\*\*\*\*SmoothingModeHighSpeed\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a><span data-ttu-id="1fba6-126">轉換</span><span class="sxs-lookup"><span data-stu-id="1fba6-126">Transformations</span></span>

<span data-ttu-id="1fba6-127">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件會維護兩個轉換 (世界和頁面) ，並套用至該 **圖形** 物件所繪製的所有專案。</span><span class="sxs-lookup"><span data-stu-id="1fba6-127">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains two transformations (world and page) that are applied to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="1fba6-128">任何仿射轉換都可以儲存在全球轉換中。</span><span class="sxs-lookup"><span data-stu-id="1fba6-128">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="1fba6-129">仿射轉換包括調整、旋轉、反映、扭曲和轉譯。</span><span class="sxs-lookup"><span data-stu-id="1fba6-129">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="1fba6-130">頁面轉換可用於調整規模，以及變更單位 (例如，圖元到英寸) 。</span><span class="sxs-lookup"><span data-stu-id="1fba6-130">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="1fba6-131">如需轉換的詳細資訊，請參閱 [座標系統和轉換](-gdiplus-coordinate-systems-and-transformations-about.md)。</span><span class="sxs-lookup"><span data-stu-id="1fba6-131">For more information on transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="1fba6-132">下列範例會設定 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界和頁面轉換。</span><span class="sxs-lookup"><span data-stu-id="1fba6-132">The following example sets the world and page transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="1fba6-133">「世界」轉換是設定為30度的旋轉。</span><span class="sxs-lookup"><span data-stu-id="1fba6-133">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="1fba6-134">已設定頁面轉換，以便將座標傳遞給第二個 [**圖形：:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 會被視為毫米而不是圖元。</span><span class="sxs-lookup"><span data-stu-id="1fba6-134">The page transformation is set so that the coordinates passed to the second [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="1fba6-135">此程式碼會對圖形進行兩個相同的呼叫 **：:D rawellipse** 方法。</span><span class="sxs-lookup"><span data-stu-id="1fba6-135">The code makes two identical calls to the **Graphics::DrawEllipse** method.</span></span> <span data-ttu-id="1fba6-136">全球轉換會套用至第一個 **圖形：:D rawellipse** 呼叫，而 (世界和頁面) 的轉換都會套用至第二個 **圖形：:D rawellipse** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="1fba6-136">The world transformation is applied to the first **Graphics::DrawEllipse** call, and both transformations (world and page) are applied to the second **Graphics::DrawEllipse** call.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



<span data-ttu-id="1fba6-137">下圖顯示兩個省略號。</span><span class="sxs-lookup"><span data-stu-id="1fba6-137">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="1fba6-138">請注意，30度的旋轉是關於座標系統的原點 (工作區) 的左上角，而非省略號的中心。</span><span class="sxs-lookup"><span data-stu-id="1fba6-138">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="1fba6-139">另請注意，畫筆寬度1表示第一個橢圓形為1圖元，第二個橢圓形則為1毫米。</span><span class="sxs-lookup"><span data-stu-id="1fba6-139">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>

![視窗的螢幕擷取畫面，其中包含小型、細橢圓形和大型、較粗的橢圓形](images/graphicsascon1.png)

 

### <a name="clipping-region"></a><span data-ttu-id="1fba6-141">裁剪區域</span><span class="sxs-lookup"><span data-stu-id="1fba6-141">Clipping Region</span></span>

<span data-ttu-id="1fba6-142">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件會維護套用至該 **圖形** 物件所繪製之所有專案的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="1fba6-142">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains a clipping region that applies to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="1fba6-143">您可以藉由呼叫 [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) 方法來設定裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="1fba6-143">You can set the clipping region by calling the [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method.</span></span>

<span data-ttu-id="1fba6-144">下列範例會建立兩個矩形的聯集，藉以建立一個形狀區域。</span><span class="sxs-lookup"><span data-stu-id="1fba6-144">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="1fba6-145">該區域會指定為 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="1fba6-145">That region is designated as the clipping region of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="1fba6-146">然後，程式碼會繪製兩行，限制為裁剪區域的內部。</span><span class="sxs-lookup"><span data-stu-id="1fba6-146">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



<span data-ttu-id="1fba6-147">下圖顯示已裁剪的行。</span><span class="sxs-lookup"><span data-stu-id="1fba6-147">The following illustration shows the clipped lines.</span></span>

![圖例顯示以兩條對角線（紅線）交叉的彩色形狀](images/graphicsascon2.png)

 

 
