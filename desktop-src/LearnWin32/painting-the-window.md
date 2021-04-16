---
title: 繪製視窗
description: 您已建立您的視窗。 現在您想要在其中顯示某個東西。 在 Windows 術語中，這稱為繪製視窗。 為了混合使用，視窗是空白畫布，等候您填滿。
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104566225"
---
# <a name="painting-the-window"></a><span data-ttu-id="7d7f8-106">繪製視窗</span><span class="sxs-lookup"><span data-stu-id="7d7f8-106">Painting the Window</span></span>

<span data-ttu-id="7d7f8-107">您已建立您的視窗。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-107">You've created your window.</span></span> <span data-ttu-id="7d7f8-108">現在您想要在其中顯示某個東西。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-108">Now you want to show something inside it.</span></span> <span data-ttu-id="7d7f8-109">在 Windows 術語中，這稱為繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-109">In Windows terminology, this is called painting the window.</span></span> <span data-ttu-id="7d7f8-110">為了混合使用，視窗是空白畫布，等候您填滿。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-110">To mix metaphors, a window is a blank canvas, waiting for you to fill it.</span></span>

<span data-ttu-id="7d7f8-111">有時候您的程式會起始繪製，以更新視窗的外觀。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-111">Sometimes your program will initiate painting to update the appearance of the window.</span></span> <span data-ttu-id="7d7f8-112">在其他情況下，作業系統會通知您必須重新繪製視窗的一部分。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-112">At other times, the operating system will notify you that you must repaint a portion of the window.</span></span> <span data-ttu-id="7d7f8-113">發生這種情況時，作業系統會傳送 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息給視窗。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-113">When this occurs, the operating system sends the window a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="7d7f8-114">必須繪製之視窗的部分稱為「 *更新區域*」。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-114">The portion of the window that must be painted is called the *update region*.</span></span>

<span data-ttu-id="7d7f8-115">第一次顯示視窗時，必須繪製視窗的整個工作區。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-115">The first time a window is shown, the entire client area of the window must be painted.</span></span> <span data-ttu-id="7d7f8-116">因此，當您顯示視窗時，一律會收到至少一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-116">Therefore, you will always receive at least one [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message when you show a window.</span></span>

![顯示視窗更新區域的圖例](images/painting01.png)

<span data-ttu-id="7d7f8-118">您只需負責繪製工作區。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-118">You are only responsible for painting the client area.</span></span> <span data-ttu-id="7d7f8-119">周圍的框架（包括標題列）會自動由作業系統繪製。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-119">The surrounding frame, including the title bar, is automatically painted by the operating system.</span></span> <span data-ttu-id="7d7f8-120">在您完成工作區的繪製之後，請清除更新區域，這會告知作業系統不需要傳送另一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，直到發生變更為止。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-120">After you finish painting the client area, you clear the update region, which tells the operating system that it does not need to send another [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message until something changes.</span></span>

<span data-ttu-id="7d7f8-121">現在假設使用者移動另一個視窗，使其遮蔽視窗的一部分。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-121">Now suppose the user moves another window so that it obscures a portion of your window.</span></span> <span data-ttu-id="7d7f8-122">當遮蔽部分再次變成可見時，該部分會新增至更新區域，而您的視窗會收到另一個 [**WM \_ 繪製**](/windows/desktop/gdi/wm-paint) 訊息。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-122">When the obscured portion becomes visible again, that portion is added to the update region, and your window receives another [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

![圖例顯示當兩個 windows 重迭時，更新區域的變更方式](images/painting02.png)

<span data-ttu-id="7d7f8-124">如果使用者將視窗伸展，更新區域也會變更。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-124">The update region also changes if the user stretches the window.</span></span> <span data-ttu-id="7d7f8-125">在下圖中，使用者將視窗向右延伸。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-125">In the following diagram, the user stretches the window to the right.</span></span> <span data-ttu-id="7d7f8-126">視窗右邊的新公開區域會新增至更新區域：</span><span class="sxs-lookup"><span data-stu-id="7d7f8-126">The newly exposed area on the right side of the window is added to the update region:</span></span>

![圖例顯示調整大小視窗時更新區域的變更方式](images/painting03.png)

<span data-ttu-id="7d7f8-128">在我們的第一個範例程式中，繪製常式非常簡單。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-128">In our first example program, the painting routine is very simple.</span></span> <span data-ttu-id="7d7f8-129">它只會以純色填滿整個工作區。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-129">It just fills the entire client area with a solid color.</span></span> <span data-ttu-id="7d7f8-130">同樣地，此範例也足以示範一些重要的概念。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-130">Still, this example is enough to demonstrate some of the important concepts.</span></span>

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

<span data-ttu-id="7d7f8-131">藉由呼叫 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) 函數來啟動繪製作業。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-131">Start the painting operation by calling the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span> <span data-ttu-id="7d7f8-132">此函式會在 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) 結構中填入重新繪製要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-132">This function fills in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure with information on the repaint request.</span></span> <span data-ttu-id="7d7f8-133">目前的更新區域是在 **PAINTSTRUCT** 的 **rcPaint** 成員中提供。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-133">The current update region is given in the **rcPaint** member of **PAINTSTRUCT**.</span></span> <span data-ttu-id="7d7f8-134">此更新區域的定義是相對於工作區：</span><span class="sxs-lookup"><span data-stu-id="7d7f8-134">This update region is defined relative to the client area:</span></span>

![顯示工作區來源的圖例](images/painting04.png)

<span data-ttu-id="7d7f8-136">在您的繪圖程式碼中，您有兩個基本選項：</span><span class="sxs-lookup"><span data-stu-id="7d7f8-136">In your painting code, you have two basic options:</span></span>

- <span data-ttu-id="7d7f8-137">無論更新區域的大小為何，都要繪製整個工作區。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-137">Paint the entire client area, regardless of the size of the update region.</span></span> <span data-ttu-id="7d7f8-138">任何落在更新區域以外的地方都會裁剪。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-138">Anything that falls outside of the update region is clipped.</span></span> <span data-ttu-id="7d7f8-139">也就是說，作業系統會忽略它。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-139">That is, the operating system ignores it.</span></span>
- <span data-ttu-id="7d7f8-140">藉由只繪製更新區域內視窗的部分來優化。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-140">Optimize by painting just the portion of the window inside the update region.</span></span>

<span data-ttu-id="7d7f8-141">如果您一律繪製整個工作區，則程式碼會比較簡單。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-141">If you always paint the entire client area, the code will be simpler.</span></span> <span data-ttu-id="7d7f8-142">但是，如果您有複雜的繪製邏輯，則略過更新區域以外的區域可能更有效率。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-142">If you have complicated painting logic, however, it can be more efficient to skip the areas outside of the update region.</span></span>

<span data-ttu-id="7d7f8-143">下列程式程式碼使用系統定義的視窗背景色彩 (**色彩 \_ 視窗**) ，以單一色彩填滿更新區域。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-143">The following line of code fills the update region with a single color, using the system-defined window background color (**COLOR\_WINDOW**).</span></span> <span data-ttu-id="7d7f8-144">**色彩 \_ 視窗** 所指出的實際色彩取決於使用者目前的色彩配置。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-144">The actual color indicated by **COLOR\_WINDOW** depends on the user's current color scheme.</span></span>

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

<span data-ttu-id="7d7f8-145">在此範例中， [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) 的詳細資料並不重要，但第二個參數會提供矩形的座標來填滿。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-145">The details of [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) are not important for this example, but the second parameter gives the coordinates of the rectangle to fill.</span></span> <span data-ttu-id="7d7f8-146">在此情況下，我們會將整個更新區域傳入 ([**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)) 的 **rcPaint** 成員。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-146">In this case, we pass in the entire update region (the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)).</span></span> <span data-ttu-id="7d7f8-147">在第一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息上，必須繪製整個工作區，因此 **rcPaint** 將包含整個工作區。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-147">On the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, the entire client area needs to be painted, so **rcPaint** will contain the entire client area.</span></span> <span data-ttu-id="7d7f8-148">在後續的 **WM \_ 油漆** 訊息上， **rcPaint** 可能會包含較小的矩形。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-148">On subsequent **WM\_PAINT** messages, **rcPaint** might contain a smaller rectangle.</span></span>

<span data-ttu-id="7d7f8-149">[**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect)函式是圖形裝置介面的 (GDI) 的一部分，而這項功能的 Windows 圖形有很長的時間。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-149">The [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) function is part of the Graphics Device Interface (GDI), which has powered Windows graphics for a very long time.</span></span> <span data-ttu-id="7d7f8-150">在 Windows 7 中，Microsoft 引進了一個名為 Direct2D 的新圖形引擎，它可支援高效能圖形作業，例如硬體加速。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-150">In Windows 7, Microsoft introduced a new graphics engine, named Direct2D, which supports high-performance graphics operations, such as hardware acceleration.</span></span> <span data-ttu-id="7d7f8-151">Windows Vista 的 Direct2D 也適用于 windows Vista，以及透過 windows Server 2008 的平臺更新的 windows Server 2008 [平臺更新](../win7ip/platform-update-for-windows-vista-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-151">Direct2D is also available for Windows Vista through the [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) and for Windows Server 2008 through the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="7d7f8-152">仍完全支援 (GDI。 ) </span><span class="sxs-lookup"><span data-stu-id="7d7f8-152">(GDI is still fully supported.)</span></span>

<span data-ttu-id="7d7f8-153">完成繪製之後，請呼叫 [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) 函數。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-153">After you are done painting, call the [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) function.</span></span> <span data-ttu-id="7d7f8-154">此函式會清除更新區域，這會向 Windows 發出信號，表示視窗已完成繪圖本身。</span><span class="sxs-lookup"><span data-stu-id="7d7f8-154">This function clears the update region, which signals to Windows that the window has completed painting itself.</span></span>

## <a name="next"></a><span data-ttu-id="7d7f8-155">下一個</span><span class="sxs-lookup"><span data-stu-id="7d7f8-155">Next</span></span>

[<span data-ttu-id="7d7f8-156">關閉視窗</span><span class="sxs-lookup"><span data-stu-id="7d7f8-156">Closing the Window</span></span>](closing-the-window.md)