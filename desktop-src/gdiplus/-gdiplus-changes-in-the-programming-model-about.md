---
description: 下列各節說明使用 Windows GDI + 進行程式設計的幾種方式，與 Windows 圖形裝置介面 (GDI) 的程式設計不同。
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: 程式設計模型中的變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90cd6f1c3a6ebab1e55562e67cb4926f0ffedf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026600"
---
# <a name="changes-in-the-programming-model"></a><span data-ttu-id="358c0-103">程式設計模型中的變更</span><span class="sxs-lookup"><span data-stu-id="358c0-103">Changes in the Programming Model</span></span>

<span data-ttu-id="358c0-104">下列各節說明使用 Windows GDI + 進行程式設計的幾種方式，與 Windows 圖形裝置介面 (GDI) 的程式設計不同。</span><span class="sxs-lookup"><span data-stu-id="358c0-104">The following sections describe several ways that programming with Windows GDI+ is different from programming with Windows Graphics Device Interface (GDI).</span></span>

-   [<span data-ttu-id="358c0-105">裝置內容、控制碼和繪圖物件</span><span class="sxs-lookup"><span data-stu-id="358c0-105">Device Contexts, Handles, and Graphics Objects</span></span>](#device-contexts-handles-and-graphics-objects)
-   [<span data-ttu-id="358c0-106">繪製線條的兩種方式</span><span class="sxs-lookup"><span data-stu-id="358c0-106">Two Ways to Draw a Line</span></span>](#two-ways-to-draw-a-line)
    -   [<span data-ttu-id="358c0-107">使用 GDI 繪製線條</span><span class="sxs-lookup"><span data-stu-id="358c0-107">Drawing a line with GDI</span></span>](#drawing-a-line-with-gdi)
    -   [<span data-ttu-id="358c0-108">使用 GDI + 和 c + + 類別介面繪製線條</span><span class="sxs-lookup"><span data-stu-id="358c0-108">Drawing a line with GDI+ and the C++ class interface</span></span>](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [<span data-ttu-id="358c0-109">畫筆、筆刷、路徑、影像和字型作為參數</span><span class="sxs-lookup"><span data-stu-id="358c0-109">Pens, Brushes, Paths, Images, and Fonts as Parameters</span></span>](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [<span data-ttu-id="358c0-110">方法多載</span><span class="sxs-lookup"><span data-stu-id="358c0-110">Method Overloading</span></span>](#method-overloading)
-   [<span data-ttu-id="358c0-111">目前沒有最新位置</span><span class="sxs-lookup"><span data-stu-id="358c0-111">No More Current Position</span></span>](#no-more-current-position)
-   [<span data-ttu-id="358c0-112">個別繪製和填滿方法</span><span class="sxs-lookup"><span data-stu-id="358c0-112">Separate Methods for Draw and Fill</span></span>](#separate-methods-for-draw-and-fill)
-   [<span data-ttu-id="358c0-113">建立區域</span><span class="sxs-lookup"><span data-stu-id="358c0-113">Constructing Regions</span></span>](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a><span data-ttu-id="358c0-114">裝置內容、控制碼和繪圖物件</span><span class="sxs-lookup"><span data-stu-id="358c0-114">Device Contexts, Handles, and Graphics Objects</span></span>

<span data-ttu-id="358c0-115">如果您已經使用 GDI 撰寫程式 (舊版 Windows) 中所包含的圖形裝置介面，您就會熟悉裝置內容 (DC) 的概念。</span><span class="sxs-lookup"><span data-stu-id="358c0-115">If you have written programs using GDI (the graphics device interface included in previous versions of Windows), you are familiar with the idea of a device context (DC).</span></span> <span data-ttu-id="358c0-116">裝置內容是 Windows 用來儲存特定顯示裝置功能相關資訊的結構，以及指定如何在該裝置上繪製專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="358c0-116">A device context is a structure used by Windows to store information about the capabilities of a particular display device and attributes that specify how items will be drawn on that device.</span></span> <span data-ttu-id="358c0-117">影片顯示器的裝置內容也會與顯示畫面上的特定視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="358c0-117">A device context for a video display is also associated with a particular window on the display.</span></span> <span data-ttu-id="358c0-118">首先，您會取得 (HDC) 的裝置內容控制碼，然後將該控制碼當作引數傳遞至實際進行繪圖的 GDI 函數。</span><span class="sxs-lookup"><span data-stu-id="358c0-118">First you obtain a handle to a device context (HDC), and then you pass that handle as an argument to GDI functions that actually do the drawing.</span></span> <span data-ttu-id="358c0-119">您也會將控制碼當作引數傳遞至 GDI 函數，以取得或設定裝置內容的屬性。</span><span class="sxs-lookup"><span data-stu-id="358c0-119">You also pass the handle as an argument to GDI functions that obtain or set the attributes of the device context.</span></span>

<span data-ttu-id="358c0-120">當您使用 GDI + 時，您不必擔心控制碼和裝置內容，就像使用 GDI 一樣。</span><span class="sxs-lookup"><span data-stu-id="358c0-120">When you use GDI+, you don't have to be as concerned with handles and device contexts as you do when you use GDI.</span></span> <span data-ttu-id="358c0-121">您只需建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，然後使用熟悉的物件導向樣式（MyGraphicsObject. *DrawLine ()* 中的方法來叫用其方法。</span><span class="sxs-lookup"><span data-stu-id="358c0-121">You simply create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then invoke its methods in the familiar object-oriented style — myGraphicsObject.DrawLine(*parameters*).</span></span> <span data-ttu-id="358c0-122">**圖形** 物件是 gdi + 的核心，就像裝置內容是 gdi 的核心一樣。</span><span class="sxs-lookup"><span data-stu-id="358c0-122">The **Graphics** object is at the core of GDI+ just as the device context is at the core of GDI.</span></span> <span data-ttu-id="358c0-123">裝置內容和 **圖形** 物件會扮演類似的角色，但搭配裝置內容使用的以控制碼為基礎的程式設計模型之間有一些基本差異 (gdi) 以及與 **圖形** 物件搭配使用的面向物件模型 (gdi +) 。</span><span class="sxs-lookup"><span data-stu-id="358c0-123">The device context and the **Graphics** object play similar roles, but there are some fundamental differences between the handle-based programming model used with device contexts (GDI) and the object-oriented model used with **Graphics** objects (GDI+).</span></span>

<span data-ttu-id="358c0-124">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件（例如裝置內容）會與畫面上的特定視窗相關聯，並包含屬性 (例如，平滑模式和文字轉譯提示) ，指定如何繪製專案。</span><span class="sxs-lookup"><span data-stu-id="358c0-124">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, like the device context, is associated with a particular window on the screen and contains attributes (for example, smoothing mode and text rendering hint) that specify how items are to be drawn.</span></span> <span data-ttu-id="358c0-125">不過， **圖形** 物件不會系結至畫筆、筆刷、路徑、影像或字型，因為裝置內容是。</span><span class="sxs-lookup"><span data-stu-id="358c0-125">However, the **Graphics** object is not tied to a pen, brush, path, image, or font as a device context is.</span></span> <span data-ttu-id="358c0-126">例如，在 GDI 中，您必須先呼叫 [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) ，以將畫筆物件與裝置內容產生關聯，才能使用裝置內容來繪製線條。</span><span class="sxs-lookup"><span data-stu-id="358c0-126">For example, in GDI, before you can use a device context to draw a line, you must call [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) to associate a pen object with the device context.</span></span> <span data-ttu-id="358c0-127">這稱為在裝置內容中選取畫筆。</span><span class="sxs-lookup"><span data-stu-id="358c0-127">This is referred to as selecting the pen into the device context.</span></span> <span data-ttu-id="358c0-128">在裝置內容中繪製的所有線條都將使用該畫筆，直到您選取不同的畫筆為止。</span><span class="sxs-lookup"><span data-stu-id="358c0-128">All lines drawn in the device context will use that pen until you select a different pen.</span></span> <span data-ttu-id="358c0-129">使用 GDI + 時，您會將 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件當作引數傳遞至 **Graphics** 類別的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal))方法。</span><span class="sxs-lookup"><span data-stu-id="358c0-129">With GDI+, you pass a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object as an argument to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) method of the **Graphics** class.</span></span> <span data-ttu-id="358c0-130">您可以在每一系列的 DrawLine 呼叫中使用不同的 **畫筆** 物件，而不需要將指定的 **畫筆** 物件與 **圖形** 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="358c0-130">You can use a different **Pen** object in each of a series of DrawLine calls without having to associate a given **Pen** object with a **Graphics** object.</span></span>

## <a name="two-ways-to-draw-a-line"></a><span data-ttu-id="358c0-131">繪製線條的兩種方式</span><span class="sxs-lookup"><span data-stu-id="358c0-131">Two Ways to Draw a Line</span></span>

<span data-ttu-id="358c0-132">下列兩個範例都會從位置 (20、10) 到位置 (200100) ，繪製一個寬度為3的紅線。</span><span class="sxs-lookup"><span data-stu-id="358c0-132">The following two examples each draw a red line of width 3 from location (20, 10) to location (200,100).</span></span> <span data-ttu-id="358c0-133">第一個範例會呼叫 GDI，而第二個範例會透過 c + + 類別介面呼叫 GDI +。</span><span class="sxs-lookup"><span data-stu-id="358c0-133">The first example calls GDI, and the second calls GDI+ through the C++ class interface.</span></span>

-   [<span data-ttu-id="358c0-134">使用 GDI 繪製線條</span><span class="sxs-lookup"><span data-stu-id="358c0-134">Drawing a line with GDI</span></span>](#drawing-a-line-with-gdi)
-   [<span data-ttu-id="358c0-135">使用 GDI + 和 c + + 類別介面繪製線條</span><span class="sxs-lookup"><span data-stu-id="358c0-135">Drawing a line with GDI+ and the C++ class interface</span></span>](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a><span data-ttu-id="358c0-136">使用 GDI 繪製線條</span><span class="sxs-lookup"><span data-stu-id="358c0-136">Drawing a line with GDI</span></span>

<span data-ttu-id="358c0-137">若要使用 GDI 來繪製線條，您需要兩個物件：裝置內容和畫筆。</span><span class="sxs-lookup"><span data-stu-id="358c0-137">To draw a line with GDI, you need two objects: a device context and a pen.</span></span> <span data-ttu-id="358c0-138">您可以藉由呼叫 [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)來取得裝置內容的控制碼，並藉由呼叫 [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen)來取得畫筆的控制碼。</span><span class="sxs-lookup"><span data-stu-id="358c0-138">You get a handle to a device context by calling [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint), and a handle to a pen by calling [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen).</span></span> <span data-ttu-id="358c0-139">接下來，您會呼叫 [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) ，以在裝置內容中選取畫筆。</span><span class="sxs-lookup"><span data-stu-id="358c0-139">Next, you call [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) to select the pen into the device context.</span></span> <span data-ttu-id="358c0-140">您可以藉由呼叫 [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) ，將畫筆位置設定為 (20，10) ，然後藉由呼叫 **LineTo**，從畫筆位置將線條拖曳至 (200，100) 。</span><span class="sxs-lookup"><span data-stu-id="358c0-140">You set the pen position to (20, 10) by calling [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) and then draw a line from that pen position to (200, 100) by calling **LineTo**.</span></span> <span data-ttu-id="358c0-141">請注意，MoveToEx 和 [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) 都是以引數的形式接收 **hdc** 。</span><span class="sxs-lookup"><span data-stu-id="358c0-141">Note that MoveToEx and [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) both receive **hdc** as an argument.</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a><span data-ttu-id="358c0-142">使用 GDI + 和 c + + 類別介面繪製線條</span><span class="sxs-lookup"><span data-stu-id="358c0-142">Drawing a line with GDI+ and the C++ class interface</span></span>

<span data-ttu-id="358c0-143">若要繪製具有 GDI + 和 c + + 類別介面的線條，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。</span><span class="sxs-lookup"><span data-stu-id="358c0-143">To draw a line with GDI+ and the C++ class interface, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="358c0-144">請注意，您不會要求 Windows 提供這些物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="358c0-144">Note that you don't ask Windows for handles to these objects.</span></span> <span data-ttu-id="358c0-145">相反地，您會使用函式來建立圖形 **類別的實例， (** **圖形** 物件) ，而 **畫筆類別的** 實例 () 的 **畫筆** 物件。</span><span class="sxs-lookup"><span data-stu-id="358c0-145">Instead, you use constructors to create an instance of the **Graphics** class (a **Graphics** object) and an instance of the **Pen** class (a **Pen** object).</span></span> <span data-ttu-id="358c0-146">繪製線條需要呼叫 **圖形類別的**[**圖形：:D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal))方法。</span><span class="sxs-lookup"><span data-stu-id="358c0-146">Drawing a line involves calling the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) method of the **Graphics** class.</span></span> <span data-ttu-id="358c0-147">**Graphics：:D rawline** 方法的第一個參數是您的 **Pen** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="358c0-147">The first parameter of the **Graphics::DrawLine** method is a pointer to your **Pen** object.</span></span> <span data-ttu-id="358c0-148">這是較簡單且更有彈性的配置，比在裝置內容中選取畫筆更簡單且更有彈性，如先前的 GDI 範例所示。</span><span class="sxs-lookup"><span data-stu-id="358c0-148">This is a simpler and more flexible scheme than selecting a pen into a device context as shown in the preceding GDI example.</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a><span data-ttu-id="358c0-149">畫筆、筆刷、路徑、影像和字型作為參數</span><span class="sxs-lookup"><span data-stu-id="358c0-149">Pens, Brushes, Paths, Images, and Fonts as Parameters</span></span>

<span data-ttu-id="358c0-150">上述範例顯示 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件可以與提供繪圖方法的 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件分開建立和維護。</span><span class="sxs-lookup"><span data-stu-id="358c0-150">The preceding examples show that [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) objects can be created and maintained separately from the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, which supplies the drawing methods.</span></span> <span data-ttu-id="358c0-151">[**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)、 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath)、 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)和 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 物件也可以與 **圖形** 物件分開建立和維護。</span><span class="sxs-lookup"><span data-stu-id="358c0-151">[**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush), [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath), [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image), and [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) objects can also be created and maintained separately from the **Graphics** object.</span></span> <span data-ttu-id="358c0-152">**圖形** 類別所提供的許多繪圖方法都會接收 **筆刷**、 **GraphicsPath**、**影像** 或 **字型** 物件做為引數。</span><span class="sxs-lookup"><span data-stu-id="358c0-152">Many of the drawing methods provided by the **Graphics** class receive a **Brush**, **GraphicsPath**, **Image**, or **Font** object as an argument.</span></span> <span data-ttu-id="358c0-153">例如， **筆刷** 物件的位址會做為引數傳遞至 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) 方法，並將 **GraphicsPath** 物件的位址當作引數傳遞給 [**圖形：:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) 方法。</span><span class="sxs-lookup"><span data-stu-id="358c0-153">For example, the address of a **Brush** object is passed as an argument to the [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) method, and the address of a **GraphicsPath** object is passed as an argument to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="358c0-154">同樣地，會將 **影像** 和 **字型** 物件的位址傳遞給 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) 和 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) 方法。</span><span class="sxs-lookup"><span data-stu-id="358c0-154">Similarly, addresses of **Image** and **Font** objects are passed to the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods.</span></span> <span data-ttu-id="358c0-155">這與您在裝置內容中選取筆刷、路徑、影像或字型，然後將控制碼傳遞給裝置內容以做為繪圖函式引數的 GDI 相反。</span><span class="sxs-lookup"><span data-stu-id="358c0-155">This is in contrast to GDI where you select a brush, path, image, or font into the device context and then pass a handle to the device context as an argument to a drawing function.</span></span>

## <a name="method-overloading"></a><span data-ttu-id="358c0-156">方法多載</span><span class="sxs-lookup"><span data-stu-id="358c0-156">Method Overloading</span></span>

<span data-ttu-id="358c0-157">許多 GDI + 方法都有多載;也就是說，有數個方法共用相同名稱，但有不同的參數清單。</span><span class="sxs-lookup"><span data-stu-id="358c0-157">Many of the GDI+ methods are overloaded; that is, several methods share the same name but have different parameter lists.</span></span> <span data-ttu-id="358c0-158">例如， [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal))方法有下列形式：</span><span class="sxs-lookup"><span data-stu-id="358c0-158">For example, the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class comes in the following forms:</span></span>


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



<span data-ttu-id="358c0-159">上方的四個 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) 變化都會收到 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件的指標、起點的座標，以及結束點的座標。</span><span class="sxs-lookup"><span data-stu-id="358c0-159">All four of the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) variations above receive a pointer to a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, the coordinates of the starting point, and the coordinates of the ending point.</span></span> <span data-ttu-id="358c0-160">前兩個變化會以浮點數的形式接收座標，最後兩個變化會以整數的形式接收座標。</span><span class="sxs-lookup"><span data-stu-id="358c0-160">The first two variations receive the coordinates as floating point numbers, and the last two variations receive the coordinates as integers.</span></span> <span data-ttu-id="358c0-161">第一個和第三個變化會以四個不同數位的清單來接收座標，而第二個和第四個變化會以一對 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (或 [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) 物件的方式接收座標。</span><span class="sxs-lookup"><span data-stu-id="358c0-161">The first and third variations receive the coordinates as a list of four separate numbers, while the second and fourth variations receive the coordinates as a pair of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span>

## <a name="no-more-current-position"></a><span data-ttu-id="358c0-162">目前沒有最新位置</span><span class="sxs-lookup"><span data-stu-id="358c0-162">No More Current Position</span></span>

<span data-ttu-id="358c0-163">請注意，在先前顯示的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) 方法中，會以引數的形式接收該行的起始點和結束點。</span><span class="sxs-lookup"><span data-stu-id="358c0-163">Note that in the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) methods shown previously both the starting point and the ending point of the line are received as arguments.</span></span> <span data-ttu-id="358c0-164">這是來自 GDI 配置的 MoveToEx，您可以在其中呼叫來設定目前的畫筆位置 **和 LineTo** ，以便繪製從 (**x1** 開始的線條、 **y1**) ，並在 (**x2**， **y2**) 結束。</span><span class="sxs-lookup"><span data-stu-id="358c0-164">This is a departure from the GDI scheme where you call **MoveToEx** to set the current pen position followed by **LineTo** in order to draw a line starting at (**x1**, **y1**) and ending at (**x2**, **y2**).</span></span> <span data-ttu-id="358c0-165">以 GDI + 作為整體，已放棄目前位置的概念。</span><span class="sxs-lookup"><span data-stu-id="358c0-165">GDI+ as a whole has abandoned the notion of current position.</span></span>

## <a name="separate-methods-for-draw-and-fill"></a><span data-ttu-id="358c0-166">個別繪製和填滿方法</span><span class="sxs-lookup"><span data-stu-id="358c0-166">Separate Methods for Draw and Fill</span></span>

<span data-ttu-id="358c0-167">當您繪製外框和填滿矩形的內部形狀時，GDI + 比 GDI 更有彈性。</span><span class="sxs-lookup"><span data-stu-id="358c0-167">GDI+ is more flexible than GDI when it comes to drawing the outlines and filling the interiors of shapes like rectangles.</span></span> <span data-ttu-id="358c0-168">GDI 有一個 [矩形](/windows/win32/api/wingdi/nf-wingdi-rectangle) 函式，可在一個步驟中繪製輪廓並填滿矩形的內部。</span><span class="sxs-lookup"><span data-stu-id="358c0-168">GDI has a [Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) function that draws the outline and fills the interior of a rectangle all in one step.</span></span> <span data-ttu-id="358c0-169">大綱會以目前選取的畫筆繪製，而內部會填入目前選取的筆刷。</span><span class="sxs-lookup"><span data-stu-id="358c0-169">The outline is drawn with the currently selected pen, and the interior is filled with the currently selected brush.</span></span>


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



<span data-ttu-id="358c0-170">GDI + 有個別的方法來繪製外框，並填滿矩形的內部。</span><span class="sxs-lookup"><span data-stu-id="358c0-170">GDI+ has separate methods for drawing the outline and filling the interior of a rectangle.</span></span> <span data-ttu-id="358c0-171">[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [Graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal))方法具有 Pen 物件的位址做為它的其中一個參數，而 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal))方法將 [**筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)[**刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)物件的位址當作其中一個參數。</span><span class="sxs-lookup"><span data-stu-id="358c0-171">The [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object as one of its parameters, and the [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) method has the address of a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object as one of its parameters.</span></span>


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



<span data-ttu-id="358c0-172">請注意，GDI + 中的 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) 和 [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) 方法會接收引數，以指定矩形的左邊緣、頂端、寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="358c0-172">Note that the [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) methods in GDI+ receive arguments that specify the rectangle's left edge, top, width, and height.</span></span> <span data-ttu-id="358c0-173">這與 GDI[矩形](/windows/win32/api/wingdi/nf-wingdi-rectangle) 函式相反，它接受的引數會指定矩形的左邊緣、右邊緣、頂端和底部。</span><span class="sxs-lookup"><span data-stu-id="358c0-173">This is in contrast to the GDI[Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) function, which takes arguments that specify the rectangle's left edge, right edge, top, and bottom.</span></span> <span data-ttu-id="358c0-174">另請注意，GDI + 中 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 類別的函式有四個參數。</span><span class="sxs-lookup"><span data-stu-id="358c0-174">Also note that the constructor for the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class in GDI+ has four parameters.</span></span> <span data-ttu-id="358c0-175">最後三個參數是一般的紅色、綠色和藍色值;第一個參數是 Alpha 值，指定要繪製的色彩與背景色彩混合的範圍。</span><span class="sxs-lookup"><span data-stu-id="358c0-175">The last three parameters are the usual red, green, and blue values; the first parameter is the alpha value, which specifies the extent to which the color being drawn is blended with the background color.</span></span>

## <a name="constructing-regions"></a><span data-ttu-id="358c0-176">建立區域</span><span class="sxs-lookup"><span data-stu-id="358c0-176">Constructing Regions</span></span>

<span data-ttu-id="358c0-177">GDI 提供數個功能來建立區域： CreateRectRgn、CreateEllpticRgn、CreateRoundRectRgn、CreatePolygonRgn 和 CreatePolyPolygonRgn。</span><span class="sxs-lookup"><span data-stu-id="358c0-177">GDI provides several functions for creating regions: CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn, and CreatePolyPolygonRgn.</span></span> <span data-ttu-id="358c0-178">您可能預期 GDI + 中的 [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) 類別具有類似的函式，可採用矩形、橢圓形、圓角矩形和多邊形做為引數，但並非如此。</span><span class="sxs-lookup"><span data-stu-id="358c0-178">You might expect the [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) class in GDI+ to have analogous constructors that take rectangles, ellipses, rounded rectangles, and polygons as arguments, but that is not the case.</span></span> <span data-ttu-id="358c0-179">GDI + 中的 **Region** 類別會提供一個函式，此函式會接收 [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) 物件參考，而另一個則是接收 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件位址的函數。</span><span class="sxs-lookup"><span data-stu-id="358c0-179">The **Region** class in GDI+ provides a constructor that receives a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object reference and another constructor that receives the address of a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="358c0-180">如果您想要根據橢圓形、圓角矩形或多邊形來建立區域，您可以輕鬆地建立包含橢圓形的 **GraphicsPath** 物件 (，例如) ，然後將該 **GraphicsPath** 物件的位址傳遞至 **區域** 的函式。</span><span class="sxs-lookup"><span data-stu-id="358c0-180">If you want to construct a region based on an ellipse, rounded rectangle, or polygon, you can easily do so by creating a **GraphicsPath** object (that contains an ellipse, for example) and then passing the address of that **GraphicsPath** object to a **Region** constructor.</span></span>

<span data-ttu-id="358c0-181">GDI + 可結合圖形和路徑，讓您輕鬆形成複雜的區域。</span><span class="sxs-lookup"><span data-stu-id="358c0-181">GDI+ makes it easy to form complex regions by combining shapes and paths.</span></span> <span data-ttu-id="358c0-182">[**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region)類別具有聯 [集](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_))和 [交集](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath))方法，可讓您用來以路徑或其他區域增強現有的區域。</span><span class="sxs-lookup"><span data-stu-id="358c0-182">The [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) class has [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) and [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) methods that you can use to augment an existing region with a path or another region.</span></span> <span data-ttu-id="358c0-183">GDI + 配置有一項不錯的功能，就是當 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件做為引數傳遞至 **區域** 的函式時，不會終結該物件。</span><span class="sxs-lookup"><span data-stu-id="358c0-183">One nice feature of the GDI+ scheme is that a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object is not destroyed when it is passed as an argument to a **Region** constructor.</span></span> <span data-ttu-id="358c0-184">在 GDI 中，您可以使用 [PathToRegion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) 函式來轉換區域的路徑，但在進程中終結路徑。</span><span class="sxs-lookup"><span data-stu-id="358c0-184">In GDI, you can convert a path to a region with the [PathToRegion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) function, but the path is destroyed in the process.</span></span> <span data-ttu-id="358c0-185">此外，當 **GraphicsPath** 物件的位址做為引數傳遞至 Union 或 Intersect 方法時，不會終結該物件，因此您可以使用指定的路徑作為數個不同區域的建立區塊。</span><span class="sxs-lookup"><span data-stu-id="358c0-185">Also, a **GraphicsPath** object is not destroyed when its address is passed as an argument to a Union or Intersect method, so you can use a given path as a building block for several separate regions.</span></span> <span data-ttu-id="358c0-186">下列範例會顯示這一點。</span><span class="sxs-lookup"><span data-stu-id="358c0-186">This is shown in the following example.</span></span> <span data-ttu-id="358c0-187">假設 **onePath** 是 **GraphicsPath** 物件的指標， (已初始化的簡單或複雜) 。</span><span class="sxs-lookup"><span data-stu-id="358c0-187">Assume that **onePath** is a pointer to a **GraphicsPath** object (simple or complex) that has already been initialized.</span></span>


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
