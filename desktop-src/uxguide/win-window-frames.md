---
title: 窗框
description: 大部分的程式都應該使用標準的視窗框架。 沉浸式應用程式可以有隱藏視窗框架的全螢幕模式。 請考慮策略性地使用半透明，以提供更簡單、更淺、更緊密的外觀。
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104566080"
---
# <a name="window-frames"></a><span data-ttu-id="57311-105">窗框</span><span class="sxs-lookup"><span data-stu-id="57311-105">Window Frames</span></span>

> [!NOTE]
> <span data-ttu-id="57311-106">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="57311-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="57311-107">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="57311-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="57311-108">大部分的程式都應該使用標準的視窗框架。</span><span class="sxs-lookup"><span data-stu-id="57311-108">Most programs should use standard window frames.</span></span> <span data-ttu-id="57311-109">沉浸式應用程式可以有隱藏視窗框架的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="57311-109">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="57311-110">請考慮策略性地使用半透明，以提供更簡單、更淺、更緊密的外觀。</span><span class="sxs-lookup"><span data-stu-id="57311-110">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span>

<span data-ttu-id="57311-111">在視窗框架中，使用者可以操作視窗並查看標題和圖示，以識別其內容。</span><span class="sxs-lookup"><span data-stu-id="57311-111">With a window frame, users can manipulate a window and view the title and icon to identify its contents.</span></span>

![<span data-ttu-id="57311-112">[記事本] 視窗周圍視窗框架的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-112">screen shot of window frame around notepad window</span></span> ](images/win-window-frames-image1.png)

<span data-ttu-id="57311-113">典型的視窗框架。</span><span class="sxs-lookup"><span data-stu-id="57311-113">A typical window frame.</span></span>

<span data-ttu-id="57311-114">**注意：** 與 [視窗管理](win-window-mgt.md) 和 [商標](exper-branding.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="57311-114">**Note:** Guidelines related to [window management](win-window-mgt.md) and [branding](exper-branding.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="57311-115">設計概念</span><span class="sxs-lookup"><span data-stu-id="57311-115">Design concepts</span></span>

### <a name="glass-window-frames"></a><span data-ttu-id="57311-116">半透明視窗框架</span><span class="sxs-lookup"><span data-stu-id="57311-116">Glass window frames</span></span>

<span data-ttu-id="57311-117">半透明視窗框架是 Microsoft Windows 美觀嶄新的一環，也就是吸引人和輕量。</span><span class="sxs-lookup"><span data-stu-id="57311-117">The glass window frames are a striking new aspect of the Microsoft Windows aesthetic, aiming to be both attractive and lightweight.</span></span> <span data-ttu-id="57311-118">這些半透明框架提供 windows 開放式且較不侵入的外觀，協助使用者專注于內容和功能，而不是周圍的介面。</span><span class="sxs-lookup"><span data-stu-id="57311-118">These translucent frames give windows an open, less intrusive appearance, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

![<span data-ttu-id="57311-119">圍繞計算機之半透明畫面格的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-119">screen shot of glass frame around calculator</span></span> ](images/win-window-frames-image2.png)

<span data-ttu-id="57311-120">半透明視窗框架。</span><span class="sxs-lookup"><span data-stu-id="57311-120">Glass window frames.</span></span>

<span data-ttu-id="57311-121">您可以策略性地在觸控視窗框架的視窗內的小型區域中使用半透明。</span><span class="sxs-lookup"><span data-stu-id="57311-121">You can use glass strategically in small regions within a window that touch the window frame.</span></span> <span data-ttu-id="57311-122">這類區域似乎是視窗框架的一部分，雖然技術上而言，它們是視窗工作區的一部分。</span><span class="sxs-lookup"><span data-stu-id="57311-122">Such regions appear to be part of the window frame, even though technically they are part of the window's client area.</span></span>

![<span data-ttu-id="57311-123">具有半透明邊緣之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-123">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)

<span data-ttu-id="57311-124">在此範例中，會在工作區中使用半透明，使其看起來像框架的一部分。</span><span class="sxs-lookup"><span data-stu-id="57311-124">In this example, glass is used in the client area to make it look like part of the frame.</span></span>

### <a name="hidden-frames"></a><span data-ttu-id="57311-125">隱藏的框架</span><span class="sxs-lookup"><span data-stu-id="57311-125">Hidden frames</span></span>

<span data-ttu-id="57311-126">有時候，最佳的視窗框架根本不是畫面格。</span><span class="sxs-lookup"><span data-stu-id="57311-126">Sometimes the best window frame is no frame at all.</span></span> <span data-ttu-id="57311-127">這種情況通常是因為沒有與其他程式（例如 media player、遊戲和 kiosk 應用程式）一起使用的沉浸式[全螢幕](glossary.md)應用程式[主視窗](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="57311-127">This is often the case for the [primary window](glossary.md) of immersive [full screen](glossary.md) applications that aren't used in conjunction with other programs, such as media players, games, and kiosk applications.</span></span>

<span data-ttu-id="57311-128">內容檢視器通常可讓您選擇顯示全螢幕內容的選項。</span><span class="sxs-lookup"><span data-stu-id="57311-128">Content viewers often benefit from having the option to show content full screen.</span></span> <span data-ttu-id="57311-129">範例包括 Windows Internet Explorer、Windows Live 影像中心、Windows Movie Maker HD、Microsoft PowerPoint 和 Microsoft Word。</span><span class="sxs-lookup"><span data-stu-id="57311-129">Examples include Windows Internet Explorer , Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint , and Microsoft Word.</span></span>

![<span data-ttu-id="57311-130">全螢幕視圖中媒體播放程式的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-130">screen shot of media player in full-screen view</span></span> ](images/win-window-frames-image4.png)

<span data-ttu-id="57311-131">在此範例中，Windows Media Player 可以全螢幕顯示其內容。</span><span class="sxs-lookup"><span data-stu-id="57311-131">In this example, Windows Media Player can display its content full screen.</span></span>

### <a name="custom-frames"></a><span data-ttu-id="57311-132">自訂框架</span><span class="sxs-lookup"><span data-stu-id="57311-132">Custom frames</span></span>

<span data-ttu-id="57311-133">大部分的 Windows 應用程式都應該使用標準的視窗框架。</span><span class="sxs-lookup"><span data-stu-id="57311-133">Most Windows applications should use the standard window frames.</span></span> <span data-ttu-id="57311-134">不過，對於沉浸式全螢幕的獨立應用程式（如遊戲和 kiosk 應用程式），可能適合將自訂框架用於任何未顯示全螢幕的視窗。</span><span class="sxs-lookup"><span data-stu-id="57311-134">However, for immersive, full screen, stand-alone applications like games and kiosk applications, it may be appropriate to use custom frames for any windows that aren't shown full screen.</span></span> <span data-ttu-id="57311-135">使用自訂框架的動機應該是為整體體驗提供獨特的感覺，而不只是針對 [商標](exper-branding.md)。</span><span class="sxs-lookup"><span data-stu-id="57311-135">The motivation to use custom frames should be to give the overall experience a unique feel, not just for [branding](exper-branding.md).</span></span>

![<span data-ttu-id="57311-136">影像謎題和框架的插圖</span><span class="sxs-lookup"><span data-stu-id="57311-136">illustration of scrambled picture puzzle and frame</span></span> ](images/win-window-frames-image5.png)

<span data-ttu-id="57311-137">自訂框架適用于沉浸式全螢幕、獨立的應用程式（例如遊戲）。</span><span class="sxs-lookup"><span data-stu-id="57311-137">Custom frames are appropriate for immersive, full screen, stand-alone applications such as games.</span></span>

## <a name="guidelines"></a><span data-ttu-id="57311-138">指導方針</span><span class="sxs-lookup"><span data-stu-id="57311-138">Guidelines</span></span>

### <a name="window-frames"></a><span data-ttu-id="57311-139">窗框</span><span class="sxs-lookup"><span data-stu-id="57311-139">Window frames</span></span>

-   <span data-ttu-id="57311-140">使用標準視窗框架。</span><span class="sxs-lookup"><span data-stu-id="57311-140">Use standard window frames.</span></span>
    -   <span data-ttu-id="57311-141">**例外狀況：** 為了提供沉浸式全螢幕的獨立應用程式，獨特的風格如下：</span><span class="sxs-lookup"><span data-stu-id="57311-141">**Exception:** To give immersive full screen, stand-alone applications a unique feel:</span></span>
        -   <span data-ttu-id="57311-142">請考慮隱藏 [主視窗](glossary.md)的視窗框架。</span><span class="sxs-lookup"><span data-stu-id="57311-142">Consider hiding the window frame of the [primary window](glossary.md).</span></span>
        -   <span data-ttu-id="57311-143">考慮針對 [次要視窗](glossary.md)使用自訂框架。</span><span class="sxs-lookup"><span data-stu-id="57311-143">Consider using custom frames for [secondary window](glossary.md).</span></span>
        -   <span data-ttu-id="57311-144">如果有適當的自訂框架，請選擇輕量的設計，而不會對本身太有太多的關注。</span><span class="sxs-lookup"><span data-stu-id="57311-144">If a custom frame is appropriate, choose a design that is lightweight and doesn't draw too much attention to itself.</span></span>

            <span data-ttu-id="57311-145">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="57311-145">**Incorrect:**</span></span>

            ![<span data-ttu-id="57311-146">分散畫面格的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-146">screen shot of distracting frame</span></span> ](images/win-window-frames-image6.png)

            <span data-ttu-id="57311-147">在此範例中，自訂框架會將太多注意力吸引到本身。</span><span class="sxs-lookup"><span data-stu-id="57311-147">In this example, the custom frame draws too much attention to itself.</span></span>
-   <span data-ttu-id="57311-148">請勿將控制項加入至視窗框架。</span><span class="sxs-lookup"><span data-stu-id="57311-148">Don't add controls to a window frame.</span></span> <span data-ttu-id="57311-149">請改將控制項放在視窗中。</span><span class="sxs-lookup"><span data-stu-id="57311-149">Put the controls within the window instead.</span></span>

    <span data-ttu-id="57311-150">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="57311-150">**Incorrect:**</span></span>

    ![<span data-ttu-id="57311-151">視窗框架中控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-151">screen shot of control in window frame</span></span> ](images/win-window-frames-image7.png)

    <span data-ttu-id="57311-152">**正確：**</span><span class="sxs-lookup"><span data-stu-id="57311-152">**Correct:**</span></span>

    ![<span data-ttu-id="57311-153">在工作區中控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-153">screen shot of control in client area</span></span> ](images/win-window-frames-image8.png)

    <span data-ttu-id="57311-154">在正確的範例中，控制項位於工作區，而不是視窗框架內。</span><span class="sxs-lookup"><span data-stu-id="57311-154">In the correct example, the control is within the client area instead of the window frame.</span></span>

### <a name="full-screen-mode"></a><span data-ttu-id="57311-155">全螢幕模式</span><span class="sxs-lookup"><span data-stu-id="57311-155">Full screen mode</span></span>

-   <span data-ttu-id="57311-156">針對具有選擇性全螢幕模式的程式，啟用全螢幕模式：</span><span class="sxs-lookup"><span data-stu-id="57311-156">For programs that have an optional full screen mode, to enable full screen mode:</span></span>
    -   <span data-ttu-id="57311-157">在功能表列或工具列中具有模式全螢幕命令。</span><span class="sxs-lookup"><span data-stu-id="57311-157">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="57311-158">當使用者按一下命令時，會在其選取的狀態中顯示命令。</span><span class="sxs-lookup"><span data-stu-id="57311-158">When the user clicks the command, show the command in its selected state.</span></span>

        ![<span data-ttu-id="57311-159">具有全螢幕功能表項目之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-159">screen shot of window with full screen menu item</span></span> ](images/win-window-frames-image9.png)

        <span data-ttu-id="57311-160">此範例會顯示全螢幕命令及其標準快速鍵。</span><span class="sxs-lookup"><span data-stu-id="57311-160">This example shows the full screen command along with its standard shortcut key.</span></span>

-   <span data-ttu-id="57311-161">使用 F11 鍵來取得全螢幕快速鍵。</span><span class="sxs-lookup"><span data-stu-id="57311-161">Use F11 for the full screen shortcut key.</span></span>
-   <span data-ttu-id="57311-162">如果有工具列和全螢幕模式經常使用，也有一個具有全螢幕工具提示的圖形工具列按鈕。</span><span class="sxs-lookup"><span data-stu-id="57311-162">If there is a toolbar and full screen mode is commonly used, also have a graphic toolbar button with a Full screen tooltip.</span></span>

    ![<span data-ttu-id="57311-163">全螢幕和 [還原] 按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-163">screen shot of full screen and revert buttons</span></span> ](images/win-window-frames-image10.png)

    <span data-ttu-id="57311-164">全螢幕工具列按鈕的範例。</span><span class="sxs-lookup"><span data-stu-id="57311-164">Examples of full screen toolbar buttons.</span></span>

-   <span data-ttu-id="57311-165">若要從全螢幕模式還原：</span><span class="sxs-lookup"><span data-stu-id="57311-165">To revert back from full screen mode:</span></span>
    -   <span data-ttu-id="57311-166">在功能表列或工具列中具有模式全螢幕命令。</span><span class="sxs-lookup"><span data-stu-id="57311-166">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="57311-167">當使用者按一下命令時，會以其已清除的狀態顯示命令。</span><span class="sxs-lookup"><span data-stu-id="57311-167">When the user clicks the command, show the command in its cleared state.</span></span>
    -   <span data-ttu-id="57311-168">使用 F11 鍵來取得全螢幕快速鍵。</span><span class="sxs-lookup"><span data-stu-id="57311-168">Use F11 for the full screen shortcut key.</span></span> <span data-ttu-id="57311-169">如果尚未指派，也可以使用 Esc 來進行此用途。</span><span class="sxs-lookup"><span data-stu-id="57311-169">If not already assigned, Esc can also be used for this purpose.</span></span>

### <a name="glass"></a><span data-ttu-id="57311-170">玻璃</span><span class="sxs-lookup"><span data-stu-id="57311-170">Glass</span></span>

<span data-ttu-id="57311-171">標準視窗框架會在視窗中自動使用玻璃，但您也可以在接觸視窗框架的區域中使用玻璃。</span><span class="sxs-lookup"><span data-stu-id="57311-171">Standard window frames use glass automatically in Windows, but you can also use glass in regions that touch the window frame.</span></span>

-   <span data-ttu-id="57311-172">**在不使用文字的情況下，于小型區域中策略性地使用半透明的範圍。**</span><span class="sxs-lookup"><span data-stu-id="57311-172">**Consider using glass strategically in small regions touching the window frame without text.**</span></span> <span data-ttu-id="57311-173">這樣做可以讓某個程式更簡單、更淺、更緊密的外觀，讓區域看起來像是框架的一部分。</span><span class="sxs-lookup"><span data-stu-id="57311-173">Doing so can give a program a simpler, lighter, more cohesive look by making the region appear to be part of the frame.</span></span>
-   ![<span data-ttu-id="57311-174">具有半透明邊緣之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-174">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)
-   <span data-ttu-id="57311-175">在此範例中，玻璃著重于使用者對內容的關注，而不是控制項。</span><span class="sxs-lookup"><span data-stu-id="57311-175">In this example, glass focuses the user's attention on the content instead of the controls.</span></span>
-   <span data-ttu-id="57311-176">**請勿在一般視窗背景更吸引人或更容易使用的情況下使用半透明。**</span><span class="sxs-lookup"><span data-stu-id="57311-176">**Don't use glass in situations where a plain window background would be more attractive or easier to use.**</span></span>

<span data-ttu-id="57311-177">**正確：**</span><span class="sxs-lookup"><span data-stu-id="57311-177">**Correct:**</span></span>

![<span data-ttu-id="57311-178">具有四個圖形和標籤之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-178">screen shot of window with four graphics and label</span></span> ](images/win-window-frames-image11.png)

<span data-ttu-id="57311-179">在此範例中，會使用半透明來為 Alt + Tab 視窗提供輕量外觀。</span><span class="sxs-lookup"><span data-stu-id="57311-179">In this example, glass is used to give the Alt+Tab window a lightweight appearance.</span></span> <span data-ttu-id="57311-180">玻璃適用于此視窗，因為它包含圖形和單一的強式文字標籤。</span><span class="sxs-lookup"><span data-stu-id="57311-180">Glass works for this window because it consists of graphics and a single, strong text label.</span></span>

<span data-ttu-id="57311-181">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="57311-181">**Incorrect:**</span></span>

![<span data-ttu-id="57311-182">具有十二個圖形之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="57311-182">screen shot of window with twelve graphics</span></span> ](images/win-window-frames-image12.png)

<span data-ttu-id="57311-183">在此不正確的範例中，使用半透明會造成干擾。</span><span class="sxs-lookup"><span data-stu-id="57311-183">In this incorrect example, the use of glass is distracting.</span></span> <span data-ttu-id="57311-184">一般視窗背景是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="57311-184">A plain window background would be a better choice.</span></span>

 

 