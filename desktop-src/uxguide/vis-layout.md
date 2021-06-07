---
title: Layout
description: 版面配置是視窗或頁面中內容的大小調整、間距和位置。
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8577843f3e54744cabe970e3b9132df1d9fb45df
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444879"
---
# <a name="layout"></a><span data-ttu-id="4e13e-103">Layout</span><span class="sxs-lookup"><span data-stu-id="4e13e-103">Layout</span></span>

> [!NOTE]
> <span data-ttu-id="4e13e-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="4e13e-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="4e13e-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="4e13e-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="4e13e-106">版面配置是視窗或頁面中內容的大小調整、間距和位置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-106">Layout is the sizing, spacing, and placement of content within a window or page.</span></span> <span data-ttu-id="4e13e-107">有效的版面配置對於協助使用者找到所需的內容，以及讓外觀以視覺效果吸引人來說非常重要。</span><span class="sxs-lookup"><span data-stu-id="4e13e-107">Effective layout is crucial in helping users find what they are looking for quickly, as well as making the appearance visually appealing.</span></span> <span data-ttu-id="4e13e-108">有效的版面配置可讓使用者立即瞭解的設計，以及讓使用者感覺 puzzled 和不知所措的不同。</span><span class="sxs-lookup"><span data-stu-id="4e13e-108">Effective layout can make the difference between designs that users immediately understand and those that leave users feeling puzzled and overwhelmed.</span></span>

<span data-ttu-id="4e13e-109">**注意：** 與 [視窗管理](win-window-mgt.md) 相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="4e13e-109">**Note:** Guidelines related to [window management](win-window-mgt.md) are presented in a separate article.</span></span> <span data-ttu-id="4e13e-110">建議的特定控制項大小調整和間距會顯示在其各自的指導文章中。</span><span class="sxs-lookup"><span data-stu-id="4e13e-110">Recommended specific control sizing and spacing are presented in their respective guideline articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="4e13e-111">設計概念</span><span class="sxs-lookup"><span data-stu-id="4e13e-111">Design concepts</span></span>

### <a name="visual-hierarchy"></a><span data-ttu-id="4e13e-112">視覺化階層</span><span class="sxs-lookup"><span data-stu-id="4e13e-112">Visual hierarchy</span></span>

<span data-ttu-id="4e13e-113">當視窗或頁面的外觀指出其元素的關聯性和優先權時，它會有一個清楚的視覺階層。</span><span class="sxs-lookup"><span data-stu-id="4e13e-113">A window or page has a clear visual hierarchy when its appearance indicates the relationship and priority of its elements.</span></span> <span data-ttu-id="4e13e-114">如果沒有視覺化階層，使用者就必須自行瞭解這些關聯性和優先權。</span><span class="sxs-lookup"><span data-stu-id="4e13e-114">Without a visual hierarchy, users would have to figure out these relationships and priorities themselves.</span></span>

<span data-ttu-id="4e13e-115">視覺化階層是藉由 skillfully 結合下列屬性來達成：</span><span class="sxs-lookup"><span data-stu-id="4e13e-115">Visual hierarchy is achieved by skillfully combining the following attributes:</span></span>

-   <span data-ttu-id="4e13e-116">**重點。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-116">**Focus.**</span></span> <span data-ttu-id="4e13e-117">版面配置會指出使用者需要先查看的位置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-117">The layout indicates where users need to look first.</span></span>
-   <span data-ttu-id="4e13e-118">**流。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-118">**Flow.**</span></span> <span data-ttu-id="4e13e-119">您可以透過介面中的清楚路徑，以流暢且自然的方式處理視覺流程，並依適當的順序尋找使用者介面 (UI) 元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-119">The eye flows smoothly and naturally by a clear path through the surface, finding user interface (UI) elements in the order appropriate for their use.</span></span>
-   <span data-ttu-id="4e13e-120">**分組。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-120">**Grouping.**</span></span> <span data-ttu-id="4e13e-121">邏輯相關的 UI 元素具有明確的視覺化關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e13e-121">Logically related UI elements have a clear visual relationship.</span></span> <span data-ttu-id="4e13e-122">相關專案會群組在一起;不相關的專案是分開的。</span><span class="sxs-lookup"><span data-stu-id="4e13e-122">Related items are grouped together; unrelated items are separate.</span></span>
-   <span data-ttu-id="4e13e-123">**重點。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-123">**Emphasis.**</span></span> <span data-ttu-id="4e13e-124">UI 元素會根據其相對重要性強調。</span><span class="sxs-lookup"><span data-stu-id="4e13e-124">UI elements are emphasized based on their relative importance.</span></span>
-   <span data-ttu-id="4e13e-125">**對準。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-125">**Alignment.**</span></span> <span data-ttu-id="4e13e-126">UI 元素有協調的放置，因此很容易掃描並依序顯示。</span><span class="sxs-lookup"><span data-stu-id="4e13e-126">The UI elements have coordinated placement, so they are easy to scan and appear orderly.</span></span>

<span data-ttu-id="4e13e-127">此外，有效的版面配置具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="4e13e-127">Additionally, effective layout has these attributes:</span></span>

-   <span data-ttu-id="4e13e-128">**裝置獨立性。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-128">**Device independence.**</span></span> <span data-ttu-id="4e13e-129">無論字型的字型或大小、每英寸 (DPI) 、顯示器或圖形介面卡，版面配置都會顯示為預期。</span><span class="sxs-lookup"><span data-stu-id="4e13e-129">The layout appears as intended regardless of the font typeface or size, dots per inch (dpi), display, or graphic adaptor.</span></span>
-   <span data-ttu-id="4e13e-130">**易於掃描。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-130">**Easy to scan.**</span></span> <span data-ttu-id="4e13e-131">使用者可以找到他們正在尋找的內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-131">Users can find the content they are looking for at a glance.</span></span>
-   <span data-ttu-id="4e13e-132">**效率。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-132">**Efficiency.**</span></span> <span data-ttu-id="4e13e-133">需要很大的 UI 元素，以及小型工作的元素很小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-133">UI elements that are large need to be large, and elements that are small work well small.</span></span>
-   <span data-ttu-id="4e13e-134">**大小.**</span><span class="sxs-lookup"><span data-stu-id="4e13e-134">**Resizability.**</span></span> <span data-ttu-id="4e13e-135">如果有説明，視窗可以調整大小，而且其內容版面配置有效，而不論介面的大小或小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-135">If helpful, a window is resizable and its content layout is effective no matter how large or small the surface is.</span></span>
-   <span data-ttu-id="4e13e-136">**平衡。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-136">**Balance.**</span></span> <span data-ttu-id="4e13e-137">內容會平均分散在表面上。</span><span class="sxs-lookup"><span data-stu-id="4e13e-137">The content appears evenly distributed across the surface.</span></span>
-   <span data-ttu-id="4e13e-138">**Visual 簡潔。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-138">**Visual simplicity.**</span></span> <span data-ttu-id="4e13e-139">您認為配置的情況不如需要的複雜。</span><span class="sxs-lookup"><span data-stu-id="4e13e-139">The perception that a layout is not more complicated than it needs to be.</span></span> <span data-ttu-id="4e13e-140">使用者不會覺得版面配置的外觀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-140">Users don't feel overwhelmed by the layout's appearance.</span></span>
-   <span data-ttu-id="4e13e-141">**一致性。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-141">**Consistency.**</span></span> <span data-ttu-id="4e13e-142">類似的視窗或頁面使用類似的版面配置，因此使用者一律會感覺導向。</span><span class="sxs-lookup"><span data-stu-id="4e13e-142">Similar windows or pages use a similar layout, so users always feel oriented.</span></span>

<span data-ttu-id="4e13e-143">雖然調整大小、間距和位置是簡單的概念，但使用版面配置的挑戰是為了達成這些屬性的適當組合。</span><span class="sxs-lookup"><span data-stu-id="4e13e-143">While sizing, spacing, and placement are simple concepts, the challenge with layout is to achieve the right mixture of these attributes.</span></span>

<span data-ttu-id="4e13e-144">在 Windows 中，會使用與裝置無關的計量（例如對話單位 (Dlu) 和相對圖元）來傳達版面配置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-144">In Windows, layout is communicated using device independent metrics such as dialog units (DLUs) and relative pixels.</span></span>

### <a name="a-design-model-for-reading"></a><span data-ttu-id="4e13e-145">用於讀取的設計模型</span><span class="sxs-lookup"><span data-stu-id="4e13e-145">A design model for reading</span></span>

<span data-ttu-id="4e13e-146">**使用者可以選擇內容外觀和組織所讀取的內容。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-146">**Users choose what they read by the content's appearance and organization.**</span></span> <span data-ttu-id="4e13e-147">若要建立有效的版面配置，您必須瞭解使用者通常會看到哪些內容，以及原因。</span><span class="sxs-lookup"><span data-stu-id="4e13e-147">To create an effective layout, you'll need to understand what users tend to read and why.</span></span>

<span data-ttu-id="4e13e-148">您可以使用此設計模型來進行版面配置決策，以進行讀取：</span><span class="sxs-lookup"><span data-stu-id="4e13e-148">You can make layout decisions using this design model for reading:</span></span>

-   <span data-ttu-id="4e13e-149">人們以左至右、由上到下的順序讀取 (西方文化特性) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-149">People read in a left-to-right, top-to-bottom order (in Western cultures).</span></span>
-   <span data-ttu-id="4e13e-150">讀取的模式有兩種：沉浸式閱讀和掃描。</span><span class="sxs-lookup"><span data-stu-id="4e13e-150">There are two modes of reading: immersive reading and scanning.</span></span> <span data-ttu-id="4e13e-151">沉浸式閱讀的目標是要理解。</span><span class="sxs-lookup"><span data-stu-id="4e13e-151">The goal of immersive reading is comprehension.</span></span>

    ![<span data-ttu-id="4e13e-152">等量朗讀模式的紅色箭號圖</span><span class="sxs-lookup"><span data-stu-id="4e13e-152">figure of red arrow in zigzag reading pattern</span></span> ](images/vis-layout-image1.png)

    <span data-ttu-id="4e13e-153">此圖表會將沉浸式閱讀模型。</span><span class="sxs-lookup"><span data-stu-id="4e13e-153">This diagram models immersive reading.</span></span>

    <span data-ttu-id="4e13e-154">相反地，掃描的目標是找出事物。</span><span class="sxs-lookup"><span data-stu-id="4e13e-154">By contrast, the goal of scanning is to locate things.</span></span> <span data-ttu-id="4e13e-155">整體掃描路徑看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="4e13e-155">The overall scan path looks like this:</span></span>

    ![<span data-ttu-id="4e13e-156">對角線閱讀模式的紅色箭號圖</span><span class="sxs-lookup"><span data-stu-id="4e13e-156">figure of red arrow in diagonal reading pattern</span></span> ](images/vis-layout-image2.png)

    <span data-ttu-id="4e13e-157">此圖表會將掃描模型。</span><span class="sxs-lookup"><span data-stu-id="4e13e-157">This diagram models scanning.</span></span>

    ![<span data-ttu-id="4e13e-158">向下和弧形模式中的紅色箭號圖</span><span class="sxs-lookup"><span data-stu-id="4e13e-158">figure of red arrow in a down and arc pattern</span></span> ](images/vis-layout-image3.png)

    <span data-ttu-id="4e13e-159">如果頁面的左邊緣有文字正在執行，使用者會先掃描左邊緣。</span><span class="sxs-lookup"><span data-stu-id="4e13e-159">If there is text running along the left edge of a page, users scan the left edge first.</span></span>

-   <span data-ttu-id="4e13e-160">使用軟體時，使用者不會在 UI 本身的工作中可以沉浸。</span><span class="sxs-lookup"><span data-stu-id="4e13e-160">When using software, users aren't immersed in the UI itself but in their work.</span></span> <span data-ttu-id="4e13e-161">因此，使用者通常不會讀取其掃描的 UI 文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-161">Consequently, users usually don't read UI text they scan it.</span></span> <span data-ttu-id="4e13e-162">然後，他們只會在他們認為需要的時候，全面讀取文字的部分。</span><span class="sxs-lookup"><span data-stu-id="4e13e-162">They then read bits of text comprehensively only when they believe they need to.</span></span>
-   <span data-ttu-id="4e13e-163">使用者傾向于略過頁面左側或右側的導覽窗格。</span><span class="sxs-lookup"><span data-stu-id="4e13e-163">Users tend to skip over navigation panes on the left or right side of a page.</span></span> <span data-ttu-id="4e13e-164">使用者辨識了它們，但只在想要流覽的時候查看流覽窗格。</span><span class="sxs-lookup"><span data-stu-id="4e13e-164">Users recognize that they are there, but look at navigation panes only when they want to navigate.</span></span>
-   <span data-ttu-id="4e13e-165">使用者傾向于略過大型未格式化的文字區塊，而不需要完全讀取。</span><span class="sxs-lookup"><span data-stu-id="4e13e-165">Users tend to skip over large blocks of unformatted text without reading them at all.</span></span>

    ![<span data-ttu-id="4e13e-166">顯示掃描文字之箭號的文字圖表</span><span class="sxs-lookup"><span data-stu-id="4e13e-166">figure of text with arrows showing scanning text</span></span> ](images/vis-layout-image4.png)

    <span data-ttu-id="4e13e-167">使用者通常會在掃描時跳過大型的文字和流覽窗格。</span><span class="sxs-lookup"><span data-stu-id="4e13e-167">Users tend to skip over large blocks of text and navigation panes when they scan.</span></span>

-   <span data-ttu-id="4e13e-168">所有專案都相等，使用者會先查看視窗的左上角，在頁面上掃描，然後在右下角結束掃描。</span><span class="sxs-lookup"><span data-stu-id="4e13e-168">All things being equal, users first look in the upper left corner of a window, scan across the page, and end their scan in the lower right corner.</span></span> <span data-ttu-id="4e13e-169">它們通常會忽略左下角。</span><span class="sxs-lookup"><span data-stu-id="4e13e-169">They tend to ignore the lower left corner.</span></span>

    ![<span data-ttu-id="4e13e-170">頁面和左上至右下箭號的圖表</span><span class="sxs-lookup"><span data-stu-id="4e13e-170">figure of page and upper-left to lower-right arrow</span></span> ](images/vis-layout-image5.png)

    <span data-ttu-id="4e13e-171">所有專案都相等，使用者將依下列順序讀取這些數位：1、2、4和3。</span><span class="sxs-lookup"><span data-stu-id="4e13e-171">All things being equal, users will read these numbers in the following order: 1, 2, 4, and 3.</span></span>

-   <span data-ttu-id="4e13e-172">但是在互動式 UI 中，並非所有專案都相等，因此不同的 UI 元素會收到不同的注意層級。</span><span class="sxs-lookup"><span data-stu-id="4e13e-172">But in interactive UI, not all things are equal so different UI elements receive different levels of attention.</span></span> <span data-ttu-id="4e13e-173">使用者傾向于查看互動式控制項，尤其是視窗左上角的控制項和醒目顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-173">Users tend to look at interactive controls especially controls in the upper left and center of the window and prominent text first.</span></span>

![<span data-ttu-id="4e13e-174">具有清晰和模糊文字的畫面圖</span><span class="sxs-lookup"><span data-stu-id="4e13e-174">figure of screen with sharp and blurred text</span></span> ](images/vis-layout-image6.png)

<span data-ttu-id="4e13e-175">使用者將焦點放在主要的互動式控制項和重要的主要指示，並只在需要時才查看其他專案。</span><span class="sxs-lookup"><span data-stu-id="4e13e-175">Users focus on the main interactive controls and the prominent main instruction, and look at other things only when they need to.</span></span>

-   <span data-ttu-id="4e13e-176">使用者傾向于讀取互動式控制項標籤，特別是與完成工作相關的程式。</span><span class="sxs-lookup"><span data-stu-id="4e13e-176">Users tend to read interactive control labels, especially those that appear relevant to completing the task at hand.</span></span> <span data-ttu-id="4e13e-177">相較之下，使用者通常會在他們認為需要時才讀取靜態文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-177">By contrast, users tend to read static text only when they think they need to.</span></span>
-   <span data-ttu-id="4e13e-178">出現的專案會有不同的吸引。</span><span class="sxs-lookup"><span data-stu-id="4e13e-178">Items that appear different attract attention.</span></span> <span data-ttu-id="4e13e-179">粗體文字和大型文字會從一般文字呈現出來。</span><span class="sxs-lookup"><span data-stu-id="4e13e-179">Bold text and large text stands out from normal text.</span></span> <span data-ttu-id="4e13e-180">色彩或彩色背景上的 UI 專案會顯得不上。具有圖示的專案會從沒有圖示的專案中移除。</span><span class="sxs-lookup"><span data-stu-id="4e13e-180">UI items with color or on a colored background stand out. Items with icons stand out from items without icons.</span></span>
-   <span data-ttu-id="4e13e-181">除非使用者有原因，否則不會進行滾動。</span><span class="sxs-lookup"><span data-stu-id="4e13e-181">Users don't scroll unless they have a reason to.</span></span> <span data-ttu-id="4e13e-182">如果 [超過折](glossary.md) 迭的內容沒有提供要滾動的原因，它們就不會出現。</span><span class="sxs-lookup"><span data-stu-id="4e13e-182">If the content [above the fold](glossary.md) doesn't provide a reason to scroll, they won't.</span></span>
-   <span data-ttu-id="4e13e-183">一旦使用者決定要做什麼之後，他們會立即停止掃描並進行。</span><span class="sxs-lookup"><span data-stu-id="4e13e-183">Once users have decided what to do, they immediately stop scanning and do it.</span></span>
-   <span data-ttu-id="4e13e-184">因為使用者在認為已完成時才會停止掃描，所以通常會忽略超出完成點的任何內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-184">Because users stop scanning when they think they are done, they tend to ignore anything beyond what appears to be the point of completion.</span></span>

![<span data-ttu-id="4e13e-185">鍵盤選項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-185">screen shot of keyboard options</span></span> ](images/vis-layout-image7.png)

<span data-ttu-id="4e13e-186">使用者認為完成時，會停止掃描。</span><span class="sxs-lookup"><span data-stu-id="4e13e-186">Users stop scanning when they think they're done.</span></span>

<span data-ttu-id="4e13e-187">當然，這個一般模型會有一些例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4e13e-187">Of course, there will be exceptions to this general model.</span></span> <span data-ttu-id="4e13e-188">眼睛追蹤裝置表示實際使用者的行為相當不穩定。</span><span class="sxs-lookup"><span data-stu-id="4e13e-188">Eye tracking devices indicate that real users' behavior is quite erratic.</span></span> <span data-ttu-id="4e13e-189">此模型的目標是要協助您做出良好的決策和取捨，而不是精確地建立使用者行為的模型。</span><span class="sxs-lookup"><span data-stu-id="4e13e-189">The goal of this model is to help you make good decisions and tradeoffs, not to model user behavior accurately.</span></span> <span data-ttu-id="4e13e-190">但是，當您閱讀這份清單時，希望您也已辨識過許多自己的閱讀模式。</span><span class="sxs-lookup"><span data-stu-id="4e13e-190">But as you've read this list, hopefully you've recognized many of your own reading patterns, too.</span></span>

### <a name="designing-for-scanning"></a><span data-ttu-id="4e13e-191">設計掃描</span><span class="sxs-lookup"><span data-stu-id="4e13e-191">Designing for scanning</span></span>

<span data-ttu-id="4e13e-192">**使用者不會讀取、掃描，因此您應該設計 UI 介面以進行掃描。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-192">**Users don't read, they scan so you should design UI surfaces for scanning.**</span></span> <span data-ttu-id="4e13e-193">不要假設使用者會以由左至右、由上到下的順序來讀取文字，而是會查看 UI 元素以吸引他們的注意。</span><span class="sxs-lookup"><span data-stu-id="4e13e-193">Don't assume that users will read the text as written in a left-to-right, top-to-bottom order but rather that they look at the UI elements that attract their attention.</span></span>

<span data-ttu-id="4e13e-194">若要設計掃描：</span><span class="sxs-lookup"><span data-stu-id="4e13e-194">To design for scanning:</span></span>

-   <span data-ttu-id="4e13e-195">假設使用者一開始先快速掃描整個視窗，然後以大致順序讀取 UI 元素：</span><span class="sxs-lookup"><span data-stu-id="4e13e-195">Assume that users start by quickly scanning the whole window, then reading the UI elements in roughly the following order:</span></span>
    -   <span data-ttu-id="4e13e-196">中心內的互動式控制項</span><span class="sxs-lookup"><span data-stu-id="4e13e-196">Interactive controls in the center</span></span>
    -   <span data-ttu-id="4e13e-197">認可按鈕</span><span class="sxs-lookup"><span data-stu-id="4e13e-197">The commit buttons</span></span>
    -   <span data-ttu-id="4e13e-198">在其他地方找到互動式控制項</span><span class="sxs-lookup"><span data-stu-id="4e13e-198">Interactive controls found elsewhere</span></span>
    -   <span data-ttu-id="4e13e-199">主要指示</span><span class="sxs-lookup"><span data-stu-id="4e13e-199">Main instruction</span></span>
    -   <span data-ttu-id="4e13e-200">補充說明</span><span class="sxs-lookup"><span data-stu-id="4e13e-200">Supplemental explanations</span></span>
    -   <span data-ttu-id="4e13e-201">顯示警告圖示的文字</span><span class="sxs-lookup"><span data-stu-id="4e13e-201">Text presented with a warning icon</span></span>
    -   <span data-ttu-id="4e13e-202">視窗標題</span><span class="sxs-lookup"><span data-stu-id="4e13e-202">Window title</span></span>
    -   <span data-ttu-id="4e13e-203">主要主體中的其他靜態文字</span><span class="sxs-lookup"><span data-stu-id="4e13e-203">Other static text in main body</span></span>
    -   <span data-ttu-id="4e13e-204">註腳</span><span class="sxs-lookup"><span data-stu-id="4e13e-204">Footnotes</span></span>
-   <span data-ttu-id="4e13e-205">將在左上角或左上角起始工作的 UI 元素放在上方。</span><span class="sxs-lookup"><span data-stu-id="4e13e-205">Place UI elements that initiate a task in the upper-left corner or upper-center.</span></span>
-   <span data-ttu-id="4e13e-206">將完成工作的 UI 元素放在右下角。</span><span class="sxs-lookup"><span data-stu-id="4e13e-206">Place UI elements that complete a task in the lower-right corner.</span></span>
-   <span data-ttu-id="4e13e-207">可能的話，請在互動式控制項上放置重要的文字，而非靜態文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-207">Whenever possible, put crucial text on interactive controls instead of static text.</span></span>
-   <span data-ttu-id="4e13e-208">避免將重要的資訊放在左下角或長滾動控制項或頁面的底部。</span><span class="sxs-lookup"><span data-stu-id="4e13e-208">Avoid putting crucial information in the lower-left corner or at the bottom of a long scrollable control or page.</span></span>
-   <span data-ttu-id="4e13e-209">不要呈現大型的文字區塊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-209">Don't present big blocks of text.</span></span> <span data-ttu-id="4e13e-210">消除不必要的文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-210">Eliminate unnecessary text.</span></span> <span data-ttu-id="4e13e-211">使用 [反向金字塔](text-ui.md) 呈現樣式。</span><span class="sxs-lookup"><span data-stu-id="4e13e-211">Use the [inverted pyramid](text-ui.md) presentation style.</span></span>
-   <span data-ttu-id="4e13e-212">如果您採取一些動作來吸引使用者的注意，請務必注意這一點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-212">If you do something to attract users' attention, make sure that attention is warranted.</span></span>

<span data-ttu-id="4e13e-213">可能的話，請使用此模型，而不是將它對抗;但有時候您需要強調或反強調特定的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-213">Whenever possible, work with this model rather than fighting it; but there will be times when you need to either emphasize or de-emphasize particular UI elements.</span></span>

<span data-ttu-id="4e13e-214">強調主要 UI 元素：</span><span class="sxs-lookup"><span data-stu-id="4e13e-214">To emphasize primary UI elements:</span></span>

-   <span data-ttu-id="4e13e-215">將主要 UI 元素放在 [掃描路徑](glossary.md)中。</span><span class="sxs-lookup"><span data-stu-id="4e13e-215">Put primary UI elements in the [scan path](glossary.md).</span></span>
-   <span data-ttu-id="4e13e-216">將任何 UI 置於左上角或左上角，以起始工作。</span><span class="sxs-lookup"><span data-stu-id="4e13e-216">Put any UI to initiate a task in the upper-left corner or upper-center.</span></span>
-   <span data-ttu-id="4e13e-217">將認可按鈕放在右下角。</span><span class="sxs-lookup"><span data-stu-id="4e13e-217">Put commit buttons in the lower-right corner.</span></span>
-   <span data-ttu-id="4e13e-218">將其餘的主要 UI 放在中央。</span><span class="sxs-lookup"><span data-stu-id="4e13e-218">Put the remaining primary UI in the center.</span></span>
-   <span data-ttu-id="4e13e-219">使用吸引人注意的控制項，例如命令按鈕、命令連結和圖示。</span><span class="sxs-lookup"><span data-stu-id="4e13e-219">Use controls that attract attention, such as command buttons, command links, and icons.</span></span>
-   <span data-ttu-id="4e13e-220">使用顯著文字，包括大型文字和粗體文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-220">Use prominent text, including large text and bold text.</span></span>
-   <span data-ttu-id="4e13e-221">Put text 使用者必須在互動式控制項中或透過圖示或 [橫幅](vis-graphic.md)來讀取。</span><span class="sxs-lookup"><span data-stu-id="4e13e-221">Put text users must read in interactive controls, or with icons, or on [banners](vis-graphic.md).</span></span>
-   <span data-ttu-id="4e13e-222">在淺色背景使用深色文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-222">Use dark text on a light background.</span></span>
-   <span data-ttu-id="4e13e-223">以空間括住元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-223">Surround the elements with generous space.</span></span>
-   <span data-ttu-id="4e13e-224">不需要任何互動，例如指標或暫留，即可看到您要強調的元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-224">Don't require any interaction, such as pointing or hovering, to see the element you are emphasizing.</span></span>

    ![<span data-ttu-id="4e13e-225">windows 啟用選項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-225">screen shot of windows activation options</span></span> ](images/vis-layout-image8.png)

    <span data-ttu-id="4e13e-226">這個範例示範許多強調主要 UI 元素的方式。</span><span class="sxs-lookup"><span data-stu-id="4e13e-226">This example shows many ways to emphasize primary UI elements.</span></span>

<span data-ttu-id="4e13e-227">若要取消強調次要 UI 元素：</span><span class="sxs-lookup"><span data-stu-id="4e13e-227">To de-emphasize secondary UI elements:</span></span>

-   <span data-ttu-id="4e13e-228">將次要 UI 元素放在掃描路徑之外。</span><span class="sxs-lookup"><span data-stu-id="4e13e-228">Put secondary UI elements outside the scan path.</span></span>
-   <span data-ttu-id="4e13e-229">讓使用者通常不需要在視窗左下角或底部看到任何使用者。</span><span class="sxs-lookup"><span data-stu-id="4e13e-229">Put anything users usually don't need to see in the lower-left corner or bottom of the window.</span></span>
-   <span data-ttu-id="4e13e-230">使用不會吸引注意的控制項，例如工作連結，而不是命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="4e13e-230">Use controls that don't attract attention, such as task links instead of command buttons.</span></span>
-   <span data-ttu-id="4e13e-231">使用標準或灰色文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-231">Use normal or gray text.</span></span>
-   <span data-ttu-id="4e13e-232">在深色背景上使用淺文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-232">Use light text on a dark background.</span></span> <span data-ttu-id="4e13e-233">暗灰色或藍色背景上的白色文字效果很好。</span><span class="sxs-lookup"><span data-stu-id="4e13e-233">White text on a dark gray or blue background works well.</span></span>
-   <span data-ttu-id="4e13e-234">以最短的空間括住元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-234">Surround the elements with minimal space.</span></span>
-   <span data-ttu-id="4e13e-235">請考慮使用 [漸進式洩漏](ctrl-progressive-disclosure-controls.md) 來隱藏次要 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-235">Consider using [progressive disclosure](ctrl-progressive-disclosure-controls.md) to hide secondary UI elements.</span></span>

    ![<span data-ttu-id="4e13e-236">大型和小型介面元素的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-236">screen shot of large and small interface elements</span></span> ](images/vis-layout-image9.png)

    <span data-ttu-id="4e13e-237">此範例示範許多方法來消除次要 UI 元素的強調。</span><span class="sxs-lookup"><span data-stu-id="4e13e-237">This example shows many ways to de-emphasize secondary UI elements.</span></span>

### <a name="using-screen-space-effectively"></a><span data-ttu-id="4e13e-238">有效使用螢幕空間</span><span class="sxs-lookup"><span data-stu-id="4e13e-238">Using screen space effectively</span></span>

<span data-ttu-id="4e13e-239">若要有效率地使用螢幕空間，您必須平衡數個因素：使用太多空間，而視窗的負荷很高且浪費，甚至很難根據 [Fitts 的法律](inter-mouse.md)來使用。</span><span class="sxs-lookup"><span data-stu-id="4e13e-239">Using screen space effectively requires you to balance several factors: use too much space and a window feels heavy and wasteful, and even difficult to use based on [Fitts' Law](inter-mouse.md).</span></span>

<span data-ttu-id="4e13e-240">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-240">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-241">顯示太多空白字元的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-241">screen shot showing too much white space</span></span> ](images/vis-layout-image10.png)

<span data-ttu-id="4e13e-242">在此範例中，視窗對其內容而言太大。</span><span class="sxs-lookup"><span data-stu-id="4e13e-242">In this example, the window is too large for its content.</span></span>

<span data-ttu-id="4e13e-243">另一方面，使用的空間太少，而且視窗覺得 cramped、不舒服和很嚇人，而且如果需要滾動和其他操作，就很難使用。</span><span class="sxs-lookup"><span data-stu-id="4e13e-243">On the other hand, use too little space and a window feels cramped, uncomfortable, and intimidating, and difficult to use if it requires scrolling and other manipulation to use.</span></span>

<span data-ttu-id="4e13e-244">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-244">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-245">具有太多控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-245">screen shot with too many controls</span></span> ](images/vis-layout-image11.png)

<span data-ttu-id="4e13e-246">在此範例中，視窗對其內容而言太小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-246">In this example, the window is too small for its content.</span></span>

<span data-ttu-id="4e13e-247">雖然重要的 UI 必須符合最小支援的 [有效解析度](glossary.md)，但請不要假設使用螢幕空間，這表示 windows 應該盡可能地越小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-247">While critical UI must fit in the minimum supported [effective resolution](glossary.md), don't assume that using screen space effectively means that windows should be as small as possible they shouldn't be.</span></span> <span data-ttu-id="4e13e-248">**有效的版面配置與開放空間有關，且不會嘗試將所有專案 cram 到可能的最小空間。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-248">**Effective layout has respect for open space and doesn't attempt to cram everything into the smallest space possible.**</span></span> <span data-ttu-id="4e13e-249">新式顯示器有明顯的螢幕空間，如果可以的話，也可以有效地使用此空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-249">Modern displays have significant screen space and it makes sense to use this space effectively when you can.</span></span> <span data-ttu-id="4e13e-250">因此，在使用太多螢幕空間，而不是太少的情況下，錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-250">Consequently, err on the side of using too much screen space rather than too little.</span></span> <span data-ttu-id="4e13e-251">這樣做可讓您的 windows 感覺更輕且更平易近人。</span><span class="sxs-lookup"><span data-stu-id="4e13e-251">Doing so makes your windows feel lighter and more approachable.</span></span>

<span data-ttu-id="4e13e-252">您知道在下列情況中，配置會有效地使用螢幕空間：</span><span class="sxs-lookup"><span data-stu-id="4e13e-252">You know a layout is using screen space effectively when:</span></span>

-   <span data-ttu-id="4e13e-253">視窗、視窗窗格和控制項不需要調整大小就能使用。</span><span class="sxs-lookup"><span data-stu-id="4e13e-253">Windows, window panes, and controls don't have to be resized to be usable.</span></span> <span data-ttu-id="4e13e-254">如果使用者的第一件事是調整視窗、窗格或控制項的大小，其大小就會錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-254">If the first thing users do is resize a window, pane, or control, its size is wrong.</span></span>
-   <span data-ttu-id="4e13e-255">資料不會被截斷。</span><span class="sxs-lookup"><span data-stu-id="4e13e-255">Data isn't truncated.</span></span> <span data-ttu-id="4e13e-256">清單視圖和樹狀檢視中的大部分資料沒有省略號，除非資料長度很大，否則不會裁剪其他控制項中的資料。</span><span class="sxs-lookup"><span data-stu-id="4e13e-256">Most data in list views and tree views doesn't have ellipses, and data in other controls isn't clipped unless the data length is unusually large.</span></span> <span data-ttu-id="4e13e-257">必須讀取才能執行工作的資料不應截斷。</span><span class="sxs-lookup"><span data-stu-id="4e13e-257">Data that must be read to perform a task shouldn't be truncated.</span></span>
-   <span data-ttu-id="4e13e-258">視窗和控制項會適當地調整大小，以消除不必要的滾動。</span><span class="sxs-lookup"><span data-stu-id="4e13e-258">The windows and controls are sized appropriately to eliminate unnecessary scrolling.</span></span> <span data-ttu-id="4e13e-259">有少數的水準捲軸和不需要的垂直捲動條。</span><span class="sxs-lookup"><span data-stu-id="4e13e-259">There are few horizontal scrollbars and no unnecessary vertical scrollbars.</span></span>
-   <span data-ttu-id="4e13e-260">控制項大多使用其標準大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-260">Controls mostly use their standard sizes.</span></span> <span data-ttu-id="4e13e-261">例如，藉由在表面上只使用一或兩個命令按鈕寬度，來減少控制項大小的數目。</span><span class="sxs-lookup"><span data-stu-id="4e13e-261">Strive to reduce the number of control sizes, by, for example, using only one or two command button widths on a surface.</span></span>
-   <span data-ttu-id="4e13e-262">UI 介面已平衡。</span><span class="sxs-lookup"><span data-stu-id="4e13e-262">The UI surface is balanced.</span></span> <span data-ttu-id="4e13e-263">沒有大量未使用的螢幕區域。</span><span class="sxs-lookup"><span data-stu-id="4e13e-263">There aren't large unused screen areas.</span></span>

<span data-ttu-id="4e13e-264">選擇夠大的視窗大小來滿足其用途。</span><span class="sxs-lookup"><span data-stu-id="4e13e-264">Choose window sizes that are just large enough to fulfill their purpose well.</span></span> <span data-ttu-id="4e13e-265"> (如果視窗是可調整大小的，則此目標會套用至其預設大小。 ) **截斷的資料或捲軸的組合，且有足夠的可用螢幕空間，就是無效配置的清楚符號。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-265">(And if the window is resizable, this goal applies to its default size.) **A combination of truncated data or scrollbars and plenty of available screen space is a clear sign of ineffective layout.**</span></span>

### <a name="control-sizing"></a><span data-ttu-id="4e13e-266">控制項大小調整</span><span class="sxs-lookup"><span data-stu-id="4e13e-266">Control sizing</span></span>

<span data-ttu-id="4e13e-267">通常，使用螢幕空間的第一個步驟是決定各種 UI 元素的適當大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-267">Usually the first step in using screen space effectively is to determine the right size for the various UI elements.</span></span> <span data-ttu-id="4e13e-268">請參閱 [控制項大小調整表](#recommended-sizing-and-spacing) ，以及特定控制項指導方針文章中的建議大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-268">Refer to the [Control sizing table](#recommended-sizing-and-spacing) as well as the recommended sizing in the specific control guideline articles.</span></span>

<span data-ttu-id="4e13e-269">Fitts 的定律指出，目標越小，以滑鼠取得它所需的時間就愈長。</span><span class="sxs-lookup"><span data-stu-id="4e13e-269">Fitts' Law states that the smaller a target is, the longer it takes to acquire it with the mouse.</span></span> <span data-ttu-id="4e13e-270">此外，針對使用 Windows 平板電腦和觸控技術的電腦，「滑鼠」實際上可能是畫筆或使用者的手指，因此在決定小型控制項的大小時，您應該考慮替代的輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-270">Furthermore, for computers using Windows Tablet and Touch Technology, the "mouse" might actually be a pen or the user's finger, so you should consider alternative input devices when determining sizes for small controls.</span></span> <span data-ttu-id="4e13e-271">**16x16 相對圖元的控制項大小是適用于任何輸入裝置的最小大小。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-271">**A control size of 16x16 relative pixels is a good minimum size for any input device.**</span></span> <span data-ttu-id="4e13e-272">相較之下，標準15x9 相對圖元的微調控制項按鈕太小，無法供畫筆有效使用。</span><span class="sxs-lookup"><span data-stu-id="4e13e-272">By contrast, the standard 15x9 relative pixel spin control buttons are too small to be used effectively by pens.</span></span>

### <a name="spacing"></a><span data-ttu-id="4e13e-273">間距</span><span class="sxs-lookup"><span data-stu-id="4e13e-273">Spacing</span></span>

<span data-ttu-id="4e13e-274">提供大量的 (但) 空間不足，讓版面配置感覺更加舒適且更容易剖析。</span><span class="sxs-lookup"><span data-stu-id="4e13e-274">Providing generous (but not excessive) space makes the layout feel more comfortable and easier to parse.</span></span> <span data-ttu-id="4e13e-275">有效空間不是未使用的空間，它扮演的重要角色是改善使用者掃描的能力，同時也增加了設計的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="4e13e-275">Effective space isn't unused space it plays an important role in improving the ability for users to scan, and also adds to visual appeal of your design.</span></span> <span data-ttu-id="4e13e-276">如需指導方針，請參閱 [間距表](#recommended-sizing-and-spacing)。</span><span class="sxs-lookup"><span data-stu-id="4e13e-276">For guidelines, refer to the [Spacing table](#recommended-sizing-and-spacing).</span></span>

<span data-ttu-id="4e13e-277">針對使用 Windows 平板電腦和觸控技術的電腦，「滑鼠」可能會實際是畫筆或使用者的手指。</span><span class="sxs-lookup"><span data-stu-id="4e13e-277">For computers using Windows Tablet and Touch Technology, again the "mouse" might actually be a pen or the user's finger.</span></span> <span data-ttu-id="4e13e-278">使用畫筆或手指做為指標裝置時，鎖定目標會更困難，因而導致使用者在預期的目標之外進行點擊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-278">Targeting is more difficult when using a pen or finger as the pointing device, resulting in users tapping outside the intended target.</span></span> <span data-ttu-id="4e13e-279">當互動式控制項放在一起時，但實際上並不觸及時，使用者可以按一下控制項之間的非使用中空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-279">When interactive controls are placed very close together but are not actually touching, users may click on inactive space between the controls.</span></span> <span data-ttu-id="4e13e-280">由於按一下非使用中空間沒有結果或視覺效果的意見反應，因此使用者通常不確定發生什麼錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-280">Since clicking inactive space has no result or visual feedback, users are often uncertain what went wrong.</span></span> <span data-ttu-id="4e13e-281">如果小控制項的間距太大，則使用者需要利用精確的精確度來避免點擊錯誤的物件。</span><span class="sxs-lookup"><span data-stu-id="4e13e-281">If small controls are too closely spaced, the user needs to tap with precision to avoid tapping the wrong object.</span></span> <span data-ttu-id="4e13e-282">**若要解決這些問題，互動式控制項的目的地區域應該觸及或至少有3個 Dlu (5 個相對圖元之間的空間) 。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-282">**To address these issues, the target regions of interactive controls should either be touching or have at least 3 DLUs (5 relative pixels) of space between them.**</span></span>

<span data-ttu-id="4e13e-283">您知道配置在下列情況中有良好的間距：</span><span class="sxs-lookup"><span data-stu-id="4e13e-283">You know a layout has good spacing when:</span></span>

-   <span data-ttu-id="4e13e-284">整體來說，UI 介面感覺很舒適，也不會覺得 cramped。</span><span class="sxs-lookup"><span data-stu-id="4e13e-284">Overall, the UI surface feels comfortable and doesn't feel cramped.</span></span>
-   <span data-ttu-id="4e13e-285">空間會以一致且平衡的空間顯示。</span><span class="sxs-lookup"><span data-stu-id="4e13e-285">The space appears uniform and balanced.</span></span>
-   <span data-ttu-id="4e13e-286">相關的專案會彼此封閉，不相關的元素則相對較遠。</span><span class="sxs-lookup"><span data-stu-id="4e13e-286">Related elements are close together and unrelated elements are relatively far apart.</span></span>
-   <span data-ttu-id="4e13e-287">要一起的控制項（例如工具列按鈕）之間沒有任何可用的空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-287">There is no dead space between controls that are meant to be together, such as toolbar buttons.</span></span>

### <a name="resizable-windows"></a><span data-ttu-id="4e13e-288">可調整大小的視窗</span><span class="sxs-lookup"><span data-stu-id="4e13e-288">Resizable windows</span></span>

<span data-ttu-id="4e13e-289">可調整大小的視窗也是有效使用螢幕空間的因素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-289">Resizable windows are also a factor in using screen space effectively.</span></span> <span data-ttu-id="4e13e-290">有些 windows 是由固定內容所組成，且不會因為可調整大小而受益，但是具有可調整大小內容的視窗應該可以調整</span><span class="sxs-lookup"><span data-stu-id="4e13e-290">Some windows consist of fixed content and don't benefit from being resizable, but windows with resizable content should be resizable.</span></span> <span data-ttu-id="4e13e-291">當然，使用者調整視窗大小的原因是要採用額外的螢幕空間，以便將內容提供給需要的 UI 元素更多空間來擴充。</span><span class="sxs-lookup"><span data-stu-id="4e13e-291">Of course, the reason users resize a window is to take advanced of the additional screen space, so the content should expand accordingly by giving more space to the UI elements that need it.</span></span> <span data-ttu-id="4e13e-292">具有動態內容、檔、影像、清單和樹狀結構的 windows，可從可調整大小的視窗中獲益。</span><span class="sxs-lookup"><span data-stu-id="4e13e-292">Windows with dynamic content, documents, images, lists, and trees benefit the most from resizable windows.</span></span>

![<span data-ttu-id="4e13e-293">調整控制項取得捲軸大小的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-293">screen shot of resized control getting scroll bar</span></span> ](images/vis-layout-image12.png)

<span data-ttu-id="4e13e-294">在此範例中，調整視窗大小會調整清單視圖控制項的大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-294">In this example, resizing the window resizes the list view control.</span></span>

<span data-ttu-id="4e13e-295">話雖如此，windows 也可以延伸到太寬。</span><span class="sxs-lookup"><span data-stu-id="4e13e-295">That said, windows can be stretched too wide.</span></span> <span data-ttu-id="4e13e-296">例如，當內容寬度超過600的相對圖元時，許多控制台頁面都會變得很困難。</span><span class="sxs-lookup"><span data-stu-id="4e13e-296">For example, many control panel pages become unwieldy when the content is wider than 600 relative pixels.</span></span> <span data-ttu-id="4e13e-297">在此情況下，最好不要將內容區域的大小調整到超過這個最大寬度，或變更內容的原點，因為視窗的大小變大。</span><span class="sxs-lookup"><span data-stu-id="4e13e-297">In this case, it's better not to resize the content area beyond this maximum width or change the content's origin as the window is resized larger.</span></span> <span data-ttu-id="4e13e-298">相反地，請保留最大寬度和固定左上角。</span><span class="sxs-lookup"><span data-stu-id="4e13e-298">Instead, keep a maximum width and a fixed upper-left origin.</span></span>

<span data-ttu-id="4e13e-299">當行長度增加時，文字就會變得難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-299">Text becomes difficult to read as the line length increases.</span></span> <span data-ttu-id="4e13e-300">針對文字檔，請考慮使用最大的行長度80個字元，讓文字更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-300">For text documents, consider a maximum line length of 80 characters to make the text easy to read.</span></span> <span data-ttu-id="4e13e-301"> (字元包含字母、標點符號和空格。 ) </span><span class="sxs-lookup"><span data-stu-id="4e13e-301">(Characters include letters, punctuation, and spaces.)</span></span>

<span data-ttu-id="4e13e-302">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-302">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-303">寬訊息方塊的螢幕擷取畫面，包含長文字</span><span class="sxs-lookup"><span data-stu-id="4e13e-303">screen shot of wide message box with long text</span></span> ](images/vis-layout-image13.png)

<span data-ttu-id="4e13e-304">在此範例中，長文字長度會造成難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-304">In this example, the long text length makes for difficult reading.</span></span>

<span data-ttu-id="4e13e-305">最後，可調整大小的視窗也需要使用較小的螢幕空間，方法是讓可調整大小的內容變得較小，並藉由從 UI 元素移除空間，而不需要它。</span><span class="sxs-lookup"><span data-stu-id="4e13e-305">Finally, resizable windows also need to use screen space effectively when made smaller, by making resizable content smaller and by removing space from UI elements that can work effectively without it.</span></span> <span data-ttu-id="4e13e-306">在某個時間點，視窗或其 UI 專案變得太小而無法使用，因此應該將大小下限指派給這些專案，或應該完全移除部分元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-306">At some point, the window or its UI elements become too small to be usable, so they should be assigned a minimum size or some elements should be removed completely.</span></span>

![<span data-ttu-id="4e13e-307">具有高度、侵入式功能區之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-307">screen shot of window with tall, intrusive ribbon</span></span> ](images/vis-layout-image14.png)

![<span data-ttu-id="4e13e-308">沒有功能區之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-308">screen shot of window with no ribbon</span></span> ](images/vis-layout-image15.png)

<span data-ttu-id="4e13e-309">在此範例中，窗格有最小的大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-309">In this example, the pane has a minimum size.</span></span>

<span data-ttu-id="4e13e-310">有些程式受益于使用完全不同的簡報，讓內容可以使用較小的大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-310">Some programs benefit from using a completely different presentation to make the content usable at smaller sizes.</span></span>

![<span data-ttu-id="4e13e-311">中央媒體播放機按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-311">screen shot of centered media player buttons</span></span> ](images/vis-layout-image16.png)

<span data-ttu-id="4e13e-312">在此範例中，Windows Media Player 會在視窗對標準格式變得太小時變更其格式。</span><span class="sxs-lookup"><span data-stu-id="4e13e-312">In this example, Windows Media Player changes its format when the window becomes too small for the standard format.</span></span>

### <a name="focus"></a><span data-ttu-id="4e13e-313">焦點</span><span class="sxs-lookup"><span data-stu-id="4e13e-313">Focus</span></span>

<span data-ttu-id="4e13e-314">如果有一個明顯的位置要先查看，則配置具有焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-314">A layout has focus when there is one obvious place to look first.</span></span> <span data-ttu-id="4e13e-315">將焦點放在向使用者顯示開始掃描視窗或頁面的位置非常重要。</span><span class="sxs-lookup"><span data-stu-id="4e13e-315">Focus is important to show users where to start scanning your window or page.</span></span> <span data-ttu-id="4e13e-316">如果沒有清楚的焦點，使用者的眼睛將會穿梭 aimlessly。</span><span class="sxs-lookup"><span data-stu-id="4e13e-316">Without clear focus, the user's eye will wander aimlessly.</span></span> <span data-ttu-id="4e13e-317">焦點應該是使用者需要快速尋找和瞭解的重要內容，而且應該要有最大的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="4e13e-317">The focal point should be something important that users need to find and understand quickly, and should have the greatest visual emphasis.</span></span> <span data-ttu-id="4e13e-318">左上角是大多數視窗的自然焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-318">The upper-left corner is the natural focal point for most windows.</span></span>

<span data-ttu-id="4e13e-319">應該只有一個焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-319">There should be only one focal point.</span></span> <span data-ttu-id="4e13e-320">就像在現實生活中一樣，只要一次就能專注于一件事，使用者就無法同時專注在多個地方。</span><span class="sxs-lookup"><span data-stu-id="4e13e-320">Just as in real life, the eye can focus on only one thing at a time, users can't focus on multiple places simultaneously.</span></span>

<span data-ttu-id="4e13e-321">若要讓 UI 元素成為焦點，您可以透過下列方式提供視覺效果強調：</span><span class="sxs-lookup"><span data-stu-id="4e13e-321">To make a UI element the focal point, you can give it visual emphasis by:</span></span>

-   <span data-ttu-id="4e13e-322">將它放在表面的左上角或左上角部分。</span><span class="sxs-lookup"><span data-stu-id="4e13e-322">Placing it in the upper-left or upper-center portion of the surface.</span></span>
-   <span data-ttu-id="4e13e-323">使用重要且立即理解的互動式控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-323">Using interactive controls that are important and readily comprehensible.</span></span>
-   <span data-ttu-id="4e13e-324">使用顯著的文字，例如主要指令。</span><span class="sxs-lookup"><span data-stu-id="4e13e-324">Using prominent text, such as a main instruction.</span></span>
-   <span data-ttu-id="4e13e-325">提供控制項預設選取和初始輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-325">Giving the controls default selection and initial input focus.</span></span>
-   <span data-ttu-id="4e13e-326">將控制項放在不同的彩色背景。</span><span class="sxs-lookup"><span data-stu-id="4e13e-326">Placing the controls in a different colored background.</span></span>

<span data-ttu-id="4e13e-327">請考慮 Windows Search。</span><span class="sxs-lookup"><span data-stu-id="4e13e-327">Consider Windows Search.</span></span> <span data-ttu-id="4e13e-328">Windows Search 的焦點應該是 [搜尋] 方塊，因為它是工作的起點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-328">The focal point for Windows Search should be the Search box because it is the starting point for the task.</span></span> <span data-ttu-id="4e13e-329">不過，它位於右上角，與標準搜尋方塊位置一致。</span><span class="sxs-lookup"><span data-stu-id="4e13e-329">However, it is located in the upper-right corner to be consistent with the standard Search box placement.</span></span> <span data-ttu-id="4e13e-330">搜尋方塊具有輸入焦點，但在掃描路徑中會有其位置，而該線索本身並不足夠。</span><span class="sxs-lookup"><span data-stu-id="4e13e-330">The Search box has input focus, but given its location in the scan path, that clue alone isn't sufficient.</span></span>

<span data-ttu-id="4e13e-331">若要解決這個問題，視窗的中央部分會有明顯的指示，以將使用者導向至正確的位置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-331">To address this problem, there is prominent instruction in the upper-center portion of the window to direct users to the right location.</span></span>

<span data-ttu-id="4e13e-332">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-332">**Acceptable:**</span></span>

![<span data-ttu-id="4e13e-333">具有實用文字的 [搜尋] 對話方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-333">screen shot of search dialog box with helpful text</span></span> ](images/vis-layout-image17.png)

<span data-ttu-id="4e13e-334">在此範例中，視窗中央部分的顯著指示會將使用者導向至搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-334">In this example, a prominent instruction in the upper-center portion of the window directs users to the Search box.</span></span>

<span data-ttu-id="4e13e-335">如果沒有指示，視窗就不會有明顯的焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-335">Without the instructions, the window wouldn't have an obvious focal point.</span></span>

<span data-ttu-id="4e13e-336">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-336">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-337">[搜尋] 對話方塊的螢幕擷取畫面，沒有文字</span><span class="sxs-lookup"><span data-stu-id="4e13e-337">screen shot of search dialog box with no text</span></span> ](images/vis-layout-image18.png)

<span data-ttu-id="4e13e-338">此範例沒有明顯的焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-338">This example has no obvious focal point.</span></span> <span data-ttu-id="4e13e-339">使用者不知道要查看的位置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-339">Users don't know where to look.</span></span>

<span data-ttu-id="4e13e-340">如果您提供 UI 元素視覺強調，請務必注意是否有保證。</span><span class="sxs-lookup"><span data-stu-id="4e13e-340">If you give a UI element visual emphasis, make sure that attention is warranted.</span></span> <span data-ttu-id="4e13e-341">在先前的不正確 Windows Search 範例中，反白顯示的 [全部] 按鈕位於左上角，而且具有最大的視覺效果，但不是預期的焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-341">In the previous incorrect Windows Search example, the highlighted All button is in the upper-left corner and has the most visual emphasis, but it's not the intended focal point.</span></span> <span data-ttu-id="4e13e-342">使用者可能會碰到這個按鈕，試著找出該怎麼辦。</span><span class="sxs-lookup"><span data-stu-id="4e13e-342">Users may get stuck looking at this button trying to figure out what to do with it.</span></span>

<span data-ttu-id="4e13e-343">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-343">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-344">反白顯示按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-344">screen shot of highlighted all button</span></span> ](images/vis-layout-image19.png)

<span data-ttu-id="4e13e-345">如果沒有明顯的指令作為焦點，反白顯示的 [全部] 按鈕是不慎的焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-345">Without the prominent instruction as the focal point, the highlighted All button is an unintentional focal point.</span></span>

### <a name="flow"></a><span data-ttu-id="4e13e-346">流程</span><span class="sxs-lookup"><span data-stu-id="4e13e-346">Flow</span></span>

<span data-ttu-id="4e13e-347">當使用者透過其介面以明確的路徑進行逐步引導時，版面配置具有流程，並依適當的使用順序尋找 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-347">A layout has flow when users are guided smoothly and naturally by a clear path through its surface, finding UI elements in the order appropriate for their use.</span></span> <span data-ttu-id="4e13e-348">使用者識別焦點之後，他們需要決定如何完成工作。</span><span class="sxs-lookup"><span data-stu-id="4e13e-348">Once users identify the focal point, they need to determine how to complete the task.</span></span> <span data-ttu-id="4e13e-349">UI 元素的位置會傳達其關聯性，而且應該鏡像步驟來執行工作。</span><span class="sxs-lookup"><span data-stu-id="4e13e-349">The placement of the UI elements conveys their relationship and should mirror the steps to perform the task.</span></span> <span data-ttu-id="4e13e-350">一般來說，這表示工作的步驟應該以從左至右、由上到下的順序， (在西歐文化特性) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-350">Typically, this means the task's steps should flow naturally in a left-to-right, top-to-bottom order (in Western cultures).</span></span>

<span data-ttu-id="4e13e-351">您知道配置在下列情況中有良好的流程：</span><span class="sxs-lookup"><span data-stu-id="4e13e-351">You know a layout has good flow when:</span></span>

-   <span data-ttu-id="4e13e-352">UI 元素的位置會反映使用者執行工作所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="4e13e-352">The placement of the UI elements mirrors the steps users need to perform the task.</span></span>
-   <span data-ttu-id="4e13e-353">初始工作的 UI 元素位於左上角或左上角。</span><span class="sxs-lookup"><span data-stu-id="4e13e-353">UI elements that initiate a task are in the upper-left corner or upper-center.</span></span>
-   <span data-ttu-id="4e13e-354">完成工作的 UI 元素位於右下角。</span><span class="sxs-lookup"><span data-stu-id="4e13e-354">UI elements that complete a task are in the lower-right corner.</span></span>
-   <span data-ttu-id="4e13e-355">相關的 UI 元素會一起;不相關的元素是分開的。</span><span class="sxs-lookup"><span data-stu-id="4e13e-355">Related UI elements are together; unrelated elements are separate.</span></span>
-   <span data-ttu-id="4e13e-356">必要步驟位於主要流程中。</span><span class="sxs-lookup"><span data-stu-id="4e13e-356">Required steps are in the main flow.</span></span>
-   <span data-ttu-id="4e13e-357">選擇性步驟不在主要流程之外，可能會使用適當的背景或漸進式洩漏來將其反白。</span><span class="sxs-lookup"><span data-stu-id="4e13e-357">Optional steps are outside the main flow, possibly de-emphasized by using a suitable background or progressive disclosure.</span></span>
-   <span data-ttu-id="4e13e-358">常用的元素會出現在掃描路徑中不常使用的元素之前。</span><span class="sxs-lookup"><span data-stu-id="4e13e-358">Frequently used elements appear before infrequently used elements in the scan path.</span></span>
-   <span data-ttu-id="4e13e-359">使用者一律知道接下來該怎麼做。</span><span class="sxs-lookup"><span data-stu-id="4e13e-359">Users always know what to do next.</span></span> <span data-ttu-id="4e13e-360">工作流程中沒有未預期的跳躍或中斷。</span><span class="sxs-lookup"><span data-stu-id="4e13e-360">There are no unexpected jumps or breaks in the task flow.</span></span>

<span data-ttu-id="4e13e-361">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-361">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-362">混淆對話方塊版面配置的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-362">screen shot of confusing dialog box layout</span></span> ](images/vis-layout-image20.png)

<span data-ttu-id="4e13e-363">在此範例中，使用者不知道接下來該怎麼做。</span><span class="sxs-lookup"><span data-stu-id="4e13e-363">In this example, users don't know what to do next.</span></span> <span data-ttu-id="4e13e-364">工作流程中有未預期的跳躍和中斷。</span><span class="sxs-lookup"><span data-stu-id="4e13e-364">There are unexpected jumps and breaks in the task flow.</span></span>

<span data-ttu-id="4e13e-365">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-365">**Correct:**</span></span>

![<span data-ttu-id="4e13e-366">經過妥善規劃之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-366">screen shot of a well-planned dialog box</span></span> ](images/vis-layout-image21.png)

<span data-ttu-id="4e13e-367">在此範例中，UI 元素的呈現會反映執行工作的步驟。</span><span class="sxs-lookup"><span data-stu-id="4e13e-367">In this example, the presentation of the UI elements mirrors the steps to perform the task.</span></span>

### <a name="grouping"></a><span data-ttu-id="4e13e-368">群組</span><span class="sxs-lookup"><span data-stu-id="4e13e-368">Grouping</span></span>

<span data-ttu-id="4e13e-369">當邏輯上相關的 UI 元素具有明確的視覺化關聯性時，配置會進行群組。</span><span class="sxs-lookup"><span data-stu-id="4e13e-369">A layout has grouping when logically related UI elements have a clear visual relationship.</span></span> <span data-ttu-id="4e13e-370">群組很重要，因為使用者更容易瞭解並專注于一組與專案個別的相關專案。</span><span class="sxs-lookup"><span data-stu-id="4e13e-370">Groups are important because it is easier for users to understand and focus on a group of related items than the items individually.</span></span> <span data-ttu-id="4e13e-371">群組可讓版面配置更簡單且更容易剖析。</span><span class="sxs-lookup"><span data-stu-id="4e13e-371">Groups make a layout appear simpler and easier to parse.</span></span>

<span data-ttu-id="4e13e-372">您可以利用下列方式來顯示群組 (增加 heaviness) ：</span><span class="sxs-lookup"><span data-stu-id="4e13e-372">You can show grouping in the following ways (in increasing heaviness):</span></span>

-   <span data-ttu-id="4e13e-373">**佈局。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-373">**Layout.**</span></span> <span data-ttu-id="4e13e-374">您可以將相關的控制項彼此相鄰分組，並在不相關的控制項之間放置額外的間距。</span><span class="sxs-lookup"><span data-stu-id="4e13e-374">You can group related controls next to each other and put extra spacing between unrelated controls.</span></span>

    ![<span data-ttu-id="4e13e-375">四個圖示的圖，其中顯示四個工作群組</span><span class="sxs-lookup"><span data-stu-id="4e13e-375">figure of four icons showing four groups of tasks</span></span> ](images/vis-layout-image22.png)

    <span data-ttu-id="4e13e-376">在此範例中，只會使用版面配置來顯示控制項關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e13e-376">In this example, layout alone is used to show control relationships.</span></span>

-   <span data-ttu-id="4e13e-377">**分隔符號。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-377">**Separators.**</span></span> <span data-ttu-id="4e13e-378">分隔符號是統一一組控制項的水準或垂直線。</span><span class="sxs-lookup"><span data-stu-id="4e13e-378">A separator is a horizontal or vertical line that unifies a group of controls.</span></span> <span data-ttu-id="4e13e-379">分隔符號提供更簡單、更清楚的外觀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-379">Separators provide a simpler, cleaner look.</span></span> <span data-ttu-id="4e13e-380">但是，與群組方塊不同的是，當它們橫跨整個表面時，效果最好。</span><span class="sxs-lookup"><span data-stu-id="4e13e-380">However, unlike group boxes, they work best when they span the full surface.</span></span>

    ![<span data-ttu-id="4e13e-381">三個圖示和三個分隔符號的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-381">screen shot of three icons and three separators</span></span> ](images/vis-layout-image23.png)

    <span data-ttu-id="4e13e-382">在此範例中，標示的分隔符號會用來顯示控制項關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e13e-382">In this example, labeled separators are used to show control relationships.</span></span>

-   <span data-ttu-id="4e13e-383">**集成.**</span><span class="sxs-lookup"><span data-stu-id="4e13e-383">**Aggregators.**</span></span> <span data-ttu-id="4e13e-384">匯總工具是在強相關控制項之間建立視覺關聯性的圖形。</span><span class="sxs-lookup"><span data-stu-id="4e13e-384">An aggregator is a graphic that creates a visual relationship between strongly related controls.</span></span>

    ![<span data-ttu-id="4e13e-385">橢圓線條內控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-385">screen shot of controls inside an elliptical line</span></span> ](images/vis-layout-image24.png)

    <span data-ttu-id="4e13e-386">在此範例中，界限匯總工具是用來強調控制項之間的關聯性，讓它們感覺像是單一控制項，而不是八個。</span><span class="sxs-lookup"><span data-stu-id="4e13e-386">In this example, a boundary aggregator is used to emphasize the relationship between the controls and make them feel like a single control instead of eight.</span></span>

-   <span data-ttu-id="4e13e-387">**群組方塊。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-387">**Group boxes.**</span></span> <span data-ttu-id="4e13e-388">群組方塊是圍繞一組相關控制項的標記矩形框架。</span><span class="sxs-lookup"><span data-stu-id="4e13e-388">A group box is a labeled rectangular frame that surrounds a set of related controls.</span></span>

    ![<span data-ttu-id="4e13e-389">矩形框線中核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-389">screen shot of check boxes in a rectangular border</span></span> ](images/vis-layout-image25.png)

    <span data-ttu-id="4e13e-390">在此範例中，群組方塊會圍住一組相關的控制項，並為其加上標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-390">In this example, a group box surrounds and labels a set of related controls.</span></span>

-   <span data-ttu-id="4e13e-391">**背景。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-391">**Backgrounds.**</span></span> <span data-ttu-id="4e13e-392">您可以使用背景來強調或反強調不同類型的內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-392">You can use backgrounds to emphasize or de-emphasize different types of content.</span></span>

    ![<span data-ttu-id="4e13e-393">[控制台] 左側的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-393">screen shot of left side of control panel</span></span> ](images/vis-layout-image26.png)

    <span data-ttu-id="4e13e-394">在此範例中，[控制台] 工作窗格可用來將相關的工作和控制台專案分組。</span><span class="sxs-lookup"><span data-stu-id="4e13e-394">In this example, the control panel task pane is used to group related tasks and control panel items.</span></span>

    <span data-ttu-id="4e13e-395">為了避免視覺效果混亂，執行此作業的最小加權群組是最好的選擇。</span><span class="sxs-lookup"><span data-stu-id="4e13e-395">To avoid visual clutter, the lightest weight grouping that does the job well is the best choice.</span></span> <span data-ttu-id="4e13e-396">如需詳細資訊，請參閱[群組方塊](ctrl-group-boxes.md) [、索引標籤、](ctrl-tabs.md)[分隔符號和背景](vis-graphic.md)。</span><span class="sxs-lookup"><span data-stu-id="4e13e-396">For more information, see [Group Boxes](ctrl-group-boxes.md), [Tabs](ctrl-tabs.md), [Separators and Backgrounds](vis-graphic.md).</span></span>

<span data-ttu-id="4e13e-397">無論群組樣式為何，您都可以使用縮排來顯示群組內控制項的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e13e-397">Regardless of the grouping style, you can use indenting to show the relationship of the controls within a group.</span></span> <span data-ttu-id="4e13e-398">彼此相等的控制項應該靠左對齊，而相依的控制項則會縮排12個 Dlu 或18個相對圖元。</span><span class="sxs-lookup"><span data-stu-id="4e13e-398">Controls that are peers to each other should be left-aligned, and dependent controls are indented 12 DLUs or 18 relative pixels.</span></span>

![<span data-ttu-id="4e13e-399">三個縮排控制項層級的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-399">screen shot of three levels of indented controls</span></span> ](images/vis-layout-image27.png)

<span data-ttu-id="4e13e-400">相依控制項是縮排12個 DLU 或18個相對圖元，其設計是核取方塊和選項按鈕與其標籤之間的距離。</span><span class="sxs-lookup"><span data-stu-id="4e13e-400">Dependent controls are indented 12 DLUS or 18 relative pixels, which by design is the distance between check boxes and radio buttons from their labels.</span></span>

<span data-ttu-id="4e13e-401">您知道配置在下列情況中有良好的分組：</span><span class="sxs-lookup"><span data-stu-id="4e13e-401">You know a layout has good grouping when:</span></span>

-   <span data-ttu-id="4e13e-402">視窗或頁面最多有7個群組。</span><span class="sxs-lookup"><span data-stu-id="4e13e-402">The window or pages has at most 7 groups.</span></span>
-   <span data-ttu-id="4e13e-403">每個群組的用途都很明顯。</span><span class="sxs-lookup"><span data-stu-id="4e13e-403">The purpose of each group is obvious.</span></span>
-   <span data-ttu-id="4e13e-404">每個群組內的控制項關聯性很明顯，尤其是控制相依性。</span><span class="sxs-lookup"><span data-stu-id="4e13e-404">The relationship of controls within each group is obvious, especially control dependency.</span></span>
-   <span data-ttu-id="4e13e-405">群組可簡化內容，而不是讓它變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="4e13e-405">The grouping simplifies the content rather than making it more complex.</span></span>

### <a name="alignment"></a><span data-ttu-id="4e13e-406">對齊</span><span class="sxs-lookup"><span data-stu-id="4e13e-406">Alignment</span></span>

<span data-ttu-id="4e13e-407">對齊是 UI 元素的協調位置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-407">Alignment is the coordinated placement of UI elements.</span></span> <span data-ttu-id="4e13e-408">對齊很重要，因為它可讓您更輕鬆地掃描內容，並影響使用者對視覺複雜度的認知。</span><span class="sxs-lookup"><span data-stu-id="4e13e-408">Alignment is important because it makes content easier to scan and affects users' perception of visual complexity.</span></span>

<span data-ttu-id="4e13e-409">在決定對齊時，有幾個要考慮的目標：</span><span class="sxs-lookup"><span data-stu-id="4e13e-409">There are several goals to consider when determining alignment:</span></span>

-   <span data-ttu-id="4e13e-410">**簡化水準掃描。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-410">**Ease in horizontal scanning.**</span></span> <span data-ttu-id="4e13e-411">使用者可以水準讀取並尋找彼此旁的相關專案，而不會有任何麻煩的間隙。</span><span class="sxs-lookup"><span data-stu-id="4e13e-411">Users can read horizontally and find related items next to each other, without any awkward gaps.</span></span>
-   <span data-ttu-id="4e13e-412">**簡化垂直掃描。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-412">**Ease in vertical scanning.**</span></span> <span data-ttu-id="4e13e-413">使用者可以掃描相關專案的資料行，並立即找出他們要尋找的專案，並以最基本的水準眼睛移動。</span><span class="sxs-lookup"><span data-stu-id="4e13e-413">Users can scan columns of related items and immediately find what they are looking for, with minimal horizontal eye movement.</span></span>
-   <span data-ttu-id="4e13e-414">**極低的視覺效果複雜度。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-414">**Minimal visual complexity.**</span></span> <span data-ttu-id="4e13e-415">如果使用者有不必要的垂直對齊格線，則會察覺版面配置的視覺效果複雜。</span><span class="sxs-lookup"><span data-stu-id="4e13e-415">Users perceive a layout to be visually complex if it has unnecessary vertical alignment grid lines.</span></span>

### <a name="horizontal-alignment"></a><span data-ttu-id="4e13e-416">水平對齊</span><span class="sxs-lookup"><span data-stu-id="4e13e-416">Horizontal alignment</span></span>

<span data-ttu-id="4e13e-417">**靠左對齊**</span><span class="sxs-lookup"><span data-stu-id="4e13e-417">**Left alignment**</span></span>

<span data-ttu-id="4e13e-418">因為是由左至右的讀取順序，所以最適合大部分的內容使用左對齊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-418">Because of the left-to-right reading order, left alignment works well for most content.</span></span> <span data-ttu-id="4e13e-419">靠左對齊可讓您輕鬆地垂直掃描單欄式資料。</span><span class="sxs-lookup"><span data-stu-id="4e13e-419">Left alignment makes columnar data easy to scan vertically.</span></span>

<span data-ttu-id="4e13e-420">**靠右對齊**</span><span class="sxs-lookup"><span data-stu-id="4e13e-420">**Right alignment**</span></span>

<span data-ttu-id="4e13e-421">靠右對齊是數值資料的最佳選擇，特別是 [數值資料的資料行](ctrl-text-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="4e13e-421">Right alignment is the best choice for numeric data, especially [columns of numeric data](ctrl-text-boxes.md).</span></span> <span data-ttu-id="4e13e-422">靠右對齊也適用于 [認可按鈕](glossary.md) ，以及對齊右視窗邊緣的控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-422">Right alignment also works well for [commit buttons](glossary.md) as well as controls aligned with right window edge.</span></span>

![<span data-ttu-id="4e13e-423">advanced search 向下箭號按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-423">screen shot of advanced search down-arrow button</span></span> ](images/vis-layout-image28.png)

<span data-ttu-id="4e13e-424">在此範例中，「高階搜尋漸進式洩漏」控制項會靠右對齊，因為它是針對右邊的視窗邊緣所放置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-424">In this example, the Advanced search progressive disclosure control is right aligned because it is placed against the right window edge.</span></span>

<span data-ttu-id="4e13e-425">**置中對齊**</span><span class="sxs-lookup"><span data-stu-id="4e13e-425">**Center alignment**</span></span>

<span data-ttu-id="4e13e-426">置中對齊是最好的，適用于靠左或靠右對齊不適當或顯示不平衡的情況。</span><span class="sxs-lookup"><span data-stu-id="4e13e-426">Center alignment is best reserved for situations where either left or right alignment is inappropriate or appears unbalanced.</span></span>

![<span data-ttu-id="4e13e-427">中央媒體播放機控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-427">screen shot of centered media player controls</span></span> ](images/vis-layout-image29.png)

<span data-ttu-id="4e13e-428">在此範例中，media player 控制項的中心為提供平衡的外觀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-428">In this example, the media player control is centered to give a balanced appearance.</span></span>

<span data-ttu-id="4e13e-429">不要將視窗內容置中填滿空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-429">Don't center window content just to fill space.</span></span>

<span data-ttu-id="4e13e-430">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-430">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-431">具有太多泛空白字元之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-431">screen shot of a window with too much white space</span></span> ](images/vis-layout-image30.png)

<span data-ttu-id="4e13e-432">在此範例中，內容在可調整大小的視窗中不正確置中，以填滿空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-432">In this example, content is incorrectly centered in a resizable window to fill space.</span></span>

### <a name="vertical-alignment"></a><span data-ttu-id="4e13e-433">垂直對齊</span><span class="sxs-lookup"><span data-stu-id="4e13e-433">Vertical alignment</span></span>

<span data-ttu-id="4e13e-434">**元素頂端**</span><span class="sxs-lookup"><span data-stu-id="4e13e-434">**Element tops**</span></span>

<span data-ttu-id="4e13e-435">因為是由上到下的讀取順序，所以最高的對齊方式適用于大部分內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-435">Because of the top-to-bottom reading order, top alignment works well for most content.</span></span> <span data-ttu-id="4e13e-436">最上層對齊讓 UI 元素能以水準方式進行快速掃描。</span><span class="sxs-lookup"><span data-stu-id="4e13e-436">Top alignment makes UI elements easy to scan horizontally.</span></span>

<span data-ttu-id="4e13e-437">**文字基準**</span><span class="sxs-lookup"><span data-stu-id="4e13e-437">**Text baselines**</span></span>

<span data-ttu-id="4e13e-438">垂直對齊具有文字的控制項時，對齊文字基準以提供順暢的水準讀取流程。</span><span class="sxs-lookup"><span data-stu-id="4e13e-438">When vertically aligning controls with text, align the text baselines to give a smooth horizontal reading flow.</span></span>

<span data-ttu-id="4e13e-439">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-439">**Correct:**</span></span>

![<span data-ttu-id="4e13e-440">對齊按鈕和標籤文字的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-440">screen shot of button and label text aligned</span></span> ](images/vis-layout-image31.png)

<span data-ttu-id="4e13e-441">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-441">**Incorrect:**</span></span>

![<span data-ttu-id="4e13e-442">按鈕和標籤文字的螢幕擷取畫面未對齊</span><span class="sxs-lookup"><span data-stu-id="4e13e-442">screen shot of button and label text not aligned</span></span> ](images/vis-layout-image32.png)

<span data-ttu-id="4e13e-443">在正確的範例中，控制項及其標籤會根據其文字基準垂直對齊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-443">In the correct example, the control and its label are vertically aligned by their text baselines.</span></span>

<span data-ttu-id="4e13e-444">您知道配置在下列情況中有良好的對齊方式：</span><span class="sxs-lookup"><span data-stu-id="4e13e-444">You know a layout has good alignment when:</span></span>

-   <span data-ttu-id="4e13e-445">您可以輕鬆地水準和垂直掃描。</span><span class="sxs-lookup"><span data-stu-id="4e13e-445">It is easy to scan both horizontally and vertically.</span></span>
-   <span data-ttu-id="4e13e-446">它有一個簡單的視覺外觀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-446">It has a simple visual appearance.</span></span>

### <a name="label-alignment"></a><span data-ttu-id="4e13e-447">標籤對齊</span><span class="sxs-lookup"><span data-stu-id="4e13e-447">Label alignment</span></span>

<span data-ttu-id="4e13e-448">一般對齊規則適用于控制項標籤，但這是值得特別注意的一般問題。</span><span class="sxs-lookup"><span data-stu-id="4e13e-448">The general alignment rules apply to control labels, but it is a common problem worthy of specific attention.</span></span> <span data-ttu-id="4e13e-449">標籤對齊具有下列目標：</span><span class="sxs-lookup"><span data-stu-id="4e13e-449">Label alignment has these goals:</span></span>

-   <span data-ttu-id="4e13e-450">簡化垂直掃描以尋找正確的控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-450">Ease in vertical scanning to find the right control.</span></span>
-   <span data-ttu-id="4e13e-451">簡化水準掃描以將標籤與其控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4e13e-451">Ease in horizontal scanning to associate labels with their controls.</span></span>
-   <span data-ttu-id="4e13e-452">輕鬆進行當地語系化，處理跨語言的長度差異。</span><span class="sxs-lookup"><span data-stu-id="4e13e-452">Ease in localization, handling labels that differ in length across languages.</span></span>
-   <span data-ttu-id="4e13e-453">適用于混合不同的標籤長度。</span><span class="sxs-lookup"><span data-stu-id="4e13e-453">Works well with a mixture of different label lengths.</span></span>
-   <span data-ttu-id="4e13e-454">可有效率地使用可用的空間，同時避免截斷的文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-454">Makes efficient use of available space while avoiding truncated text.</span></span>

<span data-ttu-id="4e13e-455">整體目標是要減少尋找使用者可能尋找的視覺移動量，但控制項的本質和使用者所要尋找的內容，取決於內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-455">The overall goal is to reduce the amount of eye movement required to find what users are likely looking for, but the nature of the controls and what users are looking for depends on the context.</span></span>

<span data-ttu-id="4e13e-456">有四個常見的標籤位置和對齊樣式，各有其優點：</span><span class="sxs-lookup"><span data-stu-id="4e13e-456">There are four common label placement and alignment styles, each with its benefits:</span></span>

-   <span data-ttu-id="4e13e-457">控制項上方靠左對齊的標籤</span><span class="sxs-lookup"><span data-stu-id="4e13e-457">Left-justified labels above controls</span></span>
-   <span data-ttu-id="4e13e-458">控制項左邊的靠左對齊標籤</span><span class="sxs-lookup"><span data-stu-id="4e13e-458">Left-justified labels on left of controls</span></span>
-   <span data-ttu-id="4e13e-459">靠左對齊的標籤位於控制項左方，左邊的控制項靠左對齊</span><span class="sxs-lookup"><span data-stu-id="4e13e-459">Left-justified labels on left of controls, controls ragged on left</span></span>
-   <span data-ttu-id="4e13e-460">控制項左邊的靠右對齊標籤</span><span class="sxs-lookup"><span data-stu-id="4e13e-460">Right-justified labels on left of controls</span></span>

<span data-ttu-id="4e13e-461">**控制項上方靠左對齊的標籤**</span><span class="sxs-lookup"><span data-stu-id="4e13e-461">**Left-justified labels above controls**</span></span>

<span data-ttu-id="4e13e-462">這是最容易當地語系化的樣式，因為版面配置不會相依于標籤的長度，但會採用最多的垂直空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-462">This style is the easiest to localize because the layout doesn't depend upon the length of the labels, but it takes the most vertical space.</span></span>

![<span data-ttu-id="4e13e-463">清單中有兩個標籤資料行的控制項</span><span class="sxs-lookup"><span data-stu-id="4e13e-463">list with two columns of labels above controls</span></span> ](images/vis-layout-image33.png)

<span data-ttu-id="4e13e-464">此樣式會採用最垂直的空間，但最簡單的方式是當地語系化。</span><span class="sxs-lookup"><span data-stu-id="4e13e-464">This style takes the most vertical space but is easiest to localize.</span></span> <span data-ttu-id="4e13e-465">這是最適合用來標記互動式控制項的選項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-465">It's a better choice for labeling mostly interactive controls.</span></span>

<span data-ttu-id="4e13e-466">最佳使用時機：</span><span class="sxs-lookup"><span data-stu-id="4e13e-466">Best used when:</span></span>

-   <span data-ttu-id="4e13e-467">標記的控制項是互動式的 (而不只是文字) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-467">The controls being labeled are interactive (not just text).</span></span>
-   <span data-ttu-id="4e13e-468">UI 將會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="4e13e-468">The UI will be localized.</span></span> <span data-ttu-id="4e13e-469">這種樣式通常會為標籤長度的兩倍或甚至三倍的空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-469">This style often affords room to double or even triple the length of the label.</span></span>
-   <span data-ttu-id="4e13e-470">UI 使用固定的版面配置技術 (例如 Win32) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-470">The UI is using a fixed layout technology (such as Win32).</span></span>
-   <span data-ttu-id="4e13e-471">有十個或更少的控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-471">There are ten or fewer controls.</span></span> <span data-ttu-id="4e13e-472">使用更多控制項，標籤很難掃描。</span><span class="sxs-lookup"><span data-stu-id="4e13e-472">With more controls, the labels are hard to scan.</span></span>
-   <span data-ttu-id="4e13e-473">有足夠的垂直空間可容納標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-473">There is sufficient vertical space to accommodate the labels.</span></span>
-   <span data-ttu-id="4e13e-474">版面配置必須是自由格式，而不只是資料行。</span><span class="sxs-lookup"><span data-stu-id="4e13e-474">The layout needs to be free form, not just columns.</span></span>

<span data-ttu-id="4e13e-475">**控制項左邊的靠左對齊標籤**</span><span class="sxs-lookup"><span data-stu-id="4e13e-475">**Left-justified labels on left of controls**</span></span>

<span data-ttu-id="4e13e-476">此樣式是垂直掃描的最簡單方式，而且當標籤的長度很大時，也很適合用來將標籤與控制項建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4e13e-476">This style is the easiest to scan vertically and it also works well when labels differ greatly in length, but it is harder to associate the label with its control.</span></span> <span data-ttu-id="4e13e-477">如有必要，此樣式可以使用多行標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-477">This style can use multi-line labels if necessary.</span></span>

![<span data-ttu-id="4e13e-478">包含四個標籤的標籤資料行的清單</span><span class="sxs-lookup"><span data-stu-id="4e13e-478">list with four columns of labels left of controls</span></span> ](images/vis-layout-image34.png)

<span data-ttu-id="4e13e-479">這種樣式的效果很好。</span><span class="sxs-lookup"><span data-stu-id="4e13e-479">This style works well.</span></span> <span data-ttu-id="4e13e-480">不過，有兩個數據行，但視覺效果看起來像是四個讓資料顯得更複雜的資料。</span><span class="sxs-lookup"><span data-stu-id="4e13e-480">However, there are two columns but visually it looks like there are four making the data appear more complex.</span></span>

<span data-ttu-id="4e13e-481">最佳使用時機：</span><span class="sxs-lookup"><span data-stu-id="4e13e-481">Best used when:</span></span>

-   <span data-ttu-id="4e13e-482">使用者可能會垂直掃描以尋找特定標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-482">Users are likely to scan vertically to find specific labels.</span></span>
-   <span data-ttu-id="4e13e-483">使用者不太可能從左至右、由上到下的方式讀取標籤和控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-483">Users aren't likely to read the labels and controls in a left-to-right, top-to-bottom manner.</span></span>
-   <span data-ttu-id="4e13e-484">有足夠的水準空間可容納標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-484">There is sufficient horizontal space to accommodate the labels.</span></span>
-   <span data-ttu-id="4e13e-485">標籤的長度會有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="4e13e-485">The labels vary significantly in length.</span></span>
-   <span data-ttu-id="4e13e-486">有許多控制項，例如表單。</span><span class="sxs-lookup"><span data-stu-id="4e13e-486">There are many controls, such as with forms.</span></span>
-   <span data-ttu-id="4e13e-487">有幾個資料行。</span><span class="sxs-lookup"><span data-stu-id="4e13e-487">There are few columns.</span></span> <span data-ttu-id="4e13e-488">標籤和控制項會以視覺化方式顯示為兩個個別的資料行。</span><span class="sxs-lookup"><span data-stu-id="4e13e-488">Visually the labels and controls appear as two individual columns.</span></span>

<span data-ttu-id="4e13e-489">**靠左對齊的標籤位於控制項左方，左邊的控制項靠左對齊**</span><span class="sxs-lookup"><span data-stu-id="4e13e-489">**Left-justified labels on left of controls, controls ragged on left**</span></span>

<span data-ttu-id="4e13e-490">這種樣式可讓您輕鬆地垂直掃描標籤，以及水準掃描標籤和控制項，而且非常節省空間。但是更難垂直掃描控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-490">This style makes it easy to scan the labels vertically and the labels and controls horizontally, and is very space efficient; but it is harder to scan the controls vertically.</span></span> <span data-ttu-id="4e13e-491">控制項會靠右對齊，以充分利用可用的空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-491">The controls are right-justified to take full advantage of the available space.</span></span>

![<span data-ttu-id="4e13e-492">具有不完全控制項的兩個標籤資料行清單</span><span class="sxs-lookup"><span data-stu-id="4e13e-492">list of two columns of labels with ragged controls</span></span> ](images/vis-layout-image35.png)

<span data-ttu-id="4e13e-493">這種樣式是精簡且容易閱讀的，但很難垂直掃描控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-493">This style is compact and easy to read, but it's hard to scan controls vertically.</span></span>

<span data-ttu-id="4e13e-494">最佳使用時機：</span><span class="sxs-lookup"><span data-stu-id="4e13e-494">Best used when:</span></span>

-   <span data-ttu-id="4e13e-495">UI 使用變數配置技術 (例如 Windows Presentation Foundation) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-495">The UI is using a variable layout technology (such as Windows Presentation Foundation).</span></span>
-   <span data-ttu-id="4e13e-496">使用者可能會垂直掃描以尋找特定標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-496">Users are likely to scan vertically to find specific labels.</span></span>
-   <span data-ttu-id="4e13e-497">使用者很可能會以由左至右、由上到下的方式讀取標籤和控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-497">Users are likely to read the labels and controls in a left-to-right, top-to-bottom manner.</span></span>
-   <span data-ttu-id="4e13e-498">使用者不太可能會以垂直方式掃描控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-498">Users aren't likely to scan the controls vertically.</span></span>
-   <span data-ttu-id="4e13e-499">控制項文字的長度會有所不同，而且如果使用其他樣式，可能會被截斷。</span><span class="sxs-lookup"><span data-stu-id="4e13e-499">The control text varies in length and would likely be truncated if another style were used.</span></span>
-   <span data-ttu-id="4e13e-500">控制項是唯讀的，例如唯讀文字方塊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-500">The controls are read-only, such as read only text boxes.</span></span> <span data-ttu-id="4e13e-501">針對其他控制項，此對齊方式看起來會草率。</span><span class="sxs-lookup"><span data-stu-id="4e13e-501">For other controls, this alignment will look sloppy.</span></span> <span data-ttu-id="4e13e-502">不過，按一下時，控制項可能會變成可編輯。</span><span class="sxs-lookup"><span data-stu-id="4e13e-502">However, the controls may become editable on click.</span></span>
-   <span data-ttu-id="4e13e-503">有許多資料行，但資料行中有少數控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-503">There are many columns, but few controls in a column.</span></span>

<span data-ttu-id="4e13e-504">**控制項左邊的靠右對齊標籤**</span><span class="sxs-lookup"><span data-stu-id="4e13e-504">**Right-justified labels on left of controls**</span></span>

<span data-ttu-id="4e13e-505">這是水準讀取的最簡單方式，可將標籤與控制項建立關聯，但很難垂直掃描標籤，而且在 labelsList 具有縮排標籤和控制項的長度很大時，不會正常運作。</span><span class="sxs-lookup"><span data-stu-id="4e13e-505">This style is the easiest to read horizontally to associate the labels with their controls, but it is hard to scan the labels vertically and doesn't work well when labelsList with indented labels and controls differ greatly in length.</span></span>

![<span data-ttu-id="4e13e-506">具有縮排標籤和控制項的清單</span><span class="sxs-lookup"><span data-stu-id="4e13e-506">list with indented labels and controls</span></span> ](images/vis-layout-image36.png)

<span data-ttu-id="4e13e-507">這種樣式可讓您輕鬆地垂直掃描控制項，但很難垂直掃描標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-507">This style permits easy vertical scanning of the controls, but makes it hard to scan the labels vertically.</span></span>

<span data-ttu-id="4e13e-508">最佳使用時機：</span><span class="sxs-lookup"><span data-stu-id="4e13e-508">Best used when:</span></span>

-   <span data-ttu-id="4e13e-509">使用者很可能會以由左至右、由上到下的方式讀取標籤和控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-509">Users are likely to read the labels and controls in a left-to-right, top-to-bottom manner.</span></span>
-   <span data-ttu-id="4e13e-510">使用者可能無法垂直掃描以尋找特定標籤，可能是因為：</span><span class="sxs-lookup"><span data-stu-id="4e13e-510">Users aren't likely to scan vertically to find specific labels, possibly because:</span></span>
    -   <span data-ttu-id="4e13e-511">有幾個控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-511">There are few controls.</span></span>
    -   <span data-ttu-id="4e13e-512">標籤很已知。</span><span class="sxs-lookup"><span data-stu-id="4e13e-512">The labels are well known.</span></span>
    -   <span data-ttu-id="4e13e-513">控制項大多很容易理解，而且很少空白 (可能會有預設值，以防止空白控制項) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-513">The controls are mostly self explanatory and are rarely blank (possibly having default values to prevent blank controls).</span></span>
-   <span data-ttu-id="4e13e-514">有足夠的水準空間可容納標籤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-514">There is sufficient horizontal space to accommodate the labels.</span></span>
-   <span data-ttu-id="4e13e-515">標籤的長度不會有太大的差異。</span><span class="sxs-lookup"><span data-stu-id="4e13e-515">The labels don't vary significantly in length.</span></span>
-   <span data-ttu-id="4e13e-516">有許多資料行。</span><span class="sxs-lookup"><span data-stu-id="4e13e-516">There are many columns.</span></span> <span data-ttu-id="4e13e-517">標籤和控制項會以視覺化方式顯示為單一資料行。</span><span class="sxs-lookup"><span data-stu-id="4e13e-517">Visually the labels and controls appear as a single column.</span></span>

<span data-ttu-id="4e13e-518">不過，在採用上述任何一種樣式之前，請考慮兩個因素：</span><span class="sxs-lookup"><span data-stu-id="4e13e-518">Before adopting any of these styles, however, consider two more factors:</span></span>

-   <span data-ttu-id="4e13e-519">偏好可在整個程式中一致使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="4e13e-519">Prefer a style that you can use consistently across your program.</span></span>
-   <span data-ttu-id="4e13e-520">靠左對齊的標籤會位於控制項左邊的控制項上方，是最常見的樣式，因此應該獲得喜好設定。</span><span class="sxs-lookup"><span data-stu-id="4e13e-520">Left-justified labels either above controls on left of controls are the most common styles, so they should be given preference.</span></span>

### <a name="balance"></a><span data-ttu-id="4e13e-521">餘額</span><span class="sxs-lookup"><span data-stu-id="4e13e-521">Balance</span></span>

<span data-ttu-id="4e13e-522">當視窗或頁面的內容平均分佈在其表面上時，就會有平衡。</span><span class="sxs-lookup"><span data-stu-id="4e13e-522">A window or page has balance when its content appears evenly distributed across its surface.</span></span> <span data-ttu-id="4e13e-523">如果介面實際具有與視覺效果相同的加權，則平衡的版面配置不會提示至一側。</span><span class="sxs-lookup"><span data-stu-id="4e13e-523">If the surface physically had the same weighting as it has visually, a balanced layout wouldn't tip over to one side.</span></span>

<span data-ttu-id="4e13e-524">最常見的餘額問題是視窗或頁面左側有太多內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-524">The most common balance problem is having too much content on the left side of a window or page.</span></span> <span data-ttu-id="4e13e-525">您可以透過下列方式建立餘額：</span><span class="sxs-lookup"><span data-stu-id="4e13e-525">You can create balance in the following ways:</span></span>

-   <span data-ttu-id="4e13e-526">在左側使用較大的邊界，而不是右邊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-526">Using larger margins on the left side than the right.</span></span>
-   <span data-ttu-id="4e13e-527">放置用來完成右邊工作的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-527">Placing UI elements used to complete a task on the right.</span></span>
-   <span data-ttu-id="4e13e-528">將在整個工作中使用的 UI 元素放在中央。</span><span class="sxs-lookup"><span data-stu-id="4e13e-528">Placing UI elements used throughout the task in the center.</span></span>
-   <span data-ttu-id="4e13e-529">延長可調整大小或多行控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-529">Lengthening resizable or multi-line controls.</span></span>
-   <span data-ttu-id="4e13e-530">策略性地使用中央對齊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-530">Using center-alignment strategically.</span></span>

![<span data-ttu-id="4e13e-531">左邊的印表機和右邊的文字螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-531">screen shot of printer on left and text on right</span></span> ](images/vis-layout-image37.png)

<span data-ttu-id="4e13e-532">這種平衡式的 wizard 頁面版面配置會顯示較大的左邊界，以提升餘額。</span><span class="sxs-lookup"><span data-stu-id="4e13e-532">This well balanced wizard page layout shows a larger left margin than right to improve balance.</span></span>

<span data-ttu-id="4e13e-533">如果這些技術沒有達到平衡，請考慮減少視窗或頁面的寬度，使其更符合其內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-533">If these techniques don't achieve balance, consider reducing the width of the window or page to better match its content.</span></span>

<span data-ttu-id="4e13e-534">針對可調整大小的表面，請勿將內容置中以達到平衡。</span><span class="sxs-lookup"><span data-stu-id="4e13e-534">For resizable surfaces, don't center content just to achieve balance.</span></span> <span data-ttu-id="4e13e-535">相反地，請維持固定的左上原點、定義最大介面區，以及在使用的空間內平衡內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-535">Rather, maintain a fixed upper left origin, define a maximum surface area, and balance the content within the space used.</span></span>

### <a name="grids"></a><span data-ttu-id="4e13e-536">方格</span><span class="sxs-lookup"><span data-stu-id="4e13e-536">Grids</span></span>

<span data-ttu-id="4e13e-537">方格是不可見的基礎對齊系統。</span><span class="sxs-lookup"><span data-stu-id="4e13e-537">A grid is an invisible underlying alignment system.</span></span> <span data-ttu-id="4e13e-538">網格可以進行對稱，但非對稱式方格也可以運作。</span><span class="sxs-lookup"><span data-stu-id="4e13e-538">Grids can be symmetrical, but asymmetric grids work just as well.</span></span> <span data-ttu-id="4e13e-539">由單一視窗或頁面使用時，方格可協助組織介面內的內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-539">When used by a single window or page, grids help organize content within a surface.</span></span> <span data-ttu-id="4e13e-540">重複使用時，方格會跨表面建立一致的版面配置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-540">When reused, grids create consistent layout across surfaces.</span></span>

<span data-ttu-id="4e13e-541">格線數目會影響視覺複雜度的認知。</span><span class="sxs-lookup"><span data-stu-id="4e13e-541">The number of grid lines affect the perception of visual complexity.</span></span> <span data-ttu-id="4e13e-542">格線較少的版面配置會比具有更多格線的版面配置更簡單。</span><span class="sxs-lookup"><span data-stu-id="4e13e-542">A layout with fewer grid lines appears simpler than a layout with more grid lines.</span></span>

<span data-ttu-id="4e13e-543">**視覺效果複雜：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-543">**Visually complex:**</span></span>

![<span data-ttu-id="4e13e-544">雜亂對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-544">screen shot of cluttered dialog box</span></span> ](images/vis-layout-image38.png)

<span data-ttu-id="4e13e-545">**以視覺化方式簡單：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-545">**Visually simple:**</span></span>

![<span data-ttu-id="4e13e-546">[組織] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-546">screen shot of organized dialog box</span></span> ](images/vis-layout-image39.png)

<span data-ttu-id="4e13e-547">不必要的格線會造成視覺效果複雜度。</span><span class="sxs-lookup"><span data-stu-id="4e13e-547">Unnecessary grid lines create visual complexity.</span></span>

<span data-ttu-id="4e13e-548">您知道在下列情況中，版面配置會有效地使用方格：</span><span class="sxs-lookup"><span data-stu-id="4e13e-548">You know a layout is using grids effectively when:</span></span>

-   <span data-ttu-id="4e13e-549">具有類似內容或功能的 Windows 或頁面具有類似的版面配置。</span><span class="sxs-lookup"><span data-stu-id="4e13e-549">Windows or pages with similar content or function have similar layout.</span></span>
-   <span data-ttu-id="4e13e-550">重複的設計項目會出現在視窗和頁面的類似位置中。</span><span class="sxs-lookup"><span data-stu-id="4e13e-550">Repeated design elements appear in similar locations across windows and pages.</span></span>
-   <span data-ttu-id="4e13e-551">沒有不必要的垂直和水準對齊格線。</span><span class="sxs-lookup"><span data-stu-id="4e13e-551">There are no unnecessary vertical and horizontal alignment grid lines.</span></span>

### <a name="visual-simplicity"></a><span data-ttu-id="4e13e-552">視覺效果簡化</span><span class="sxs-lookup"><span data-stu-id="4e13e-552">Visual simplicity</span></span>

<span data-ttu-id="4e13e-553">視覺效果簡單明瞭的是，版面配置比所需更複雜。</span><span class="sxs-lookup"><span data-stu-id="4e13e-553">Visual simplicity is the perception that a layout is not more complicated than it needs to be.</span></span>

<span data-ttu-id="4e13e-554">當版面配置：</span><span class="sxs-lookup"><span data-stu-id="4e13e-554">You know a layout has visual simplicity when it:</span></span>

-   <span data-ttu-id="4e13e-555">消除不必要的視窗 chrome 層。</span><span class="sxs-lookup"><span data-stu-id="4e13e-555">Eliminates unnecessary layers of window chrome.</span></span>
-   <span data-ttu-id="4e13e-556">使用最多七個容易識別的群組來呈現內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-556">Presents the content using at most seven easily identifiable groups.</span></span>
-   <span data-ttu-id="4e13e-557">使用輕量群組，例如版面配置和分隔符號，而不是群組方塊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-557">Uses lightweight grouping, such as layout and separators instead of group boxes.</span></span>
-   <span data-ttu-id="4e13e-558">使用輕量控制項，例如次要命令的連結而非命令按鈕，以及下拉式清單，而不是選項的清單。</span><span class="sxs-lookup"><span data-stu-id="4e13e-558">Uses lightweight controls, such as links instead of command buttons for secondary commands, and drop-down lists instead of lists for choices.</span></span>
-   <span data-ttu-id="4e13e-559">減少垂直和水準對齊格線的數目。</span><span class="sxs-lookup"><span data-stu-id="4e13e-559">Reduces the number of vertical and horizontal alignment grid lines.</span></span>
-   <span data-ttu-id="4e13e-560">例如，在表面上只使用一或兩個命令按鈕寬度，以減少控制項大小的數目。</span><span class="sxs-lookup"><span data-stu-id="4e13e-560">Reduces the number of control sizes, by, for example, using only one or two command button widths on a surface.</span></span>
-   <span data-ttu-id="4e13e-561">在需要時，會使用漸進式洩漏來隱藏 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-561">Uses progressive disclosure to hide UI elements until they are needed.</span></span>
-   <span data-ttu-id="4e13e-562">使用足夠的空間，讓視窗或頁面不會覺得 cramped。</span><span class="sxs-lookup"><span data-stu-id="4e13e-562">Uses sufficient space so that the window or page doesn't feel cramped.</span></span>
-   <span data-ttu-id="4e13e-563">適當地調整視窗和控制項的大小，以消除不必要的滾動。</span><span class="sxs-lookup"><span data-stu-id="4e13e-563">Sizes windows and controls appropriately to eliminate unnecessary scrolling.</span></span>
-   <span data-ttu-id="4e13e-564">使用具有少量大小和文字色彩的單一字型。</span><span class="sxs-lookup"><span data-stu-id="4e13e-564">Uses a single font with a small number of sizes and text colors.</span></span>

<span data-ttu-id="4e13e-565">一般而言，如果可以消除版面配置元素而不會損害 UI 的效果，則可能會是。</span><span class="sxs-lookup"><span data-stu-id="4e13e-565">As a general rule, if a layout element can be eliminated without harming the effectiveness of the UI, it probably should be.</span></span>

## <a name="guidelines"></a><span data-ttu-id="4e13e-566">指導方針</span><span class="sxs-lookup"><span data-stu-id="4e13e-566">Guidelines</span></span>

### <a name="screen-resolution-and-dpi"></a><span data-ttu-id="4e13e-567">螢幕解析度和 DPI</span><span class="sxs-lookup"><span data-stu-id="4e13e-567">Screen resolution and dpi</span></span>

-   <span data-ttu-id="4e13e-568">**支援最小的 Windows 有效解析度（800x600 圖元）。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-568">**Support the minimum Windows effective resolution of 800x600 pixels.**</span></span> <span data-ttu-id="4e13e-569">對於必須在安全模式下運作的重要 Ui，支援有效的640x480 圖元解析度。</span><span class="sxs-lookup"><span data-stu-id="4e13e-569">For critical UIs that must work in safe mode, support an effective resolution of 640x480 pixels.</span></span> <span data-ttu-id="4e13e-570">請務必考慮工作列所使用的空間，其方式是針對顯示在工作列上的 windows 保留48垂直 [相對圖元](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-570">Be sure to account for the space used by the taskbar by reserving 48 vertical [relative pixels](glossary.md) for windows displayed with the taskbar.</span></span>
-   <span data-ttu-id="4e13e-571">**優化可調整大小的視窗版面配置，以有效解決1024圖元。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-571">**Optimize resizable window layouts for an effective resolution of 1024x768 pixels.**</span></span> <span data-ttu-id="4e13e-572">以仍可正常運作的方式，自動調整這些視窗的大小以取得較低的螢幕解析度。</span><span class="sxs-lookup"><span data-stu-id="4e13e-572">Automatically resize these windows for lower screen resolutions in a way that is still functional.</span></span>
-   <span data-ttu-id="4e13e-573">**請務必以每英寸96點測試您的 windows (DPI)  (為800x600 圖元) 、120 DPI (1024x768 圖元) ，以及 144 DPI (1200x900 圖元) 模式。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-573">**Be sure to test your windows in 96 dots per inch (dpi) (at 800x600 pixels), 120 dpi (at 1024x768 pixels), and 144 dpi (at 1200x900 pixels) modes.**</span></span> <span data-ttu-id="4e13e-574">檢查是否有版面配置問題，例如剪輯控制項、文字和視窗的裁剪，以及縮放圖示和點陣圖。</span><span class="sxs-lookup"><span data-stu-id="4e13e-574">Check for layout problems, such as clipping of controls, text, and windows, and stretching of icons and bitmaps.</span></span>
-   <span data-ttu-id="4e13e-575">**針對具有觸控和行動使用案例的程式，請針對 120 DPI 進行優化。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-575">**For programs with touch and mobile use scenarios, optimize for 120 dpi.**</span></span> <span data-ttu-id="4e13e-576">高 DPI 螢幕目前在觸控和行動電腦上很普遍。</span><span class="sxs-lookup"><span data-stu-id="4e13e-576">High-dpi screens are currently prevalent on touch and mobile PCs.</span></span>

### <a name="window-size"></a><span data-ttu-id="4e13e-577">視窗大小</span><span class="sxs-lookup"><span data-stu-id="4e13e-577">Window size</span></span>

-   <span data-ttu-id="4e13e-578">**選擇適合其內容的預設視窗大小。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-578">**Choose a default window size appropriate for its contents.**</span></span> <span data-ttu-id="4e13e-579">如果您可以有效地使用空間，請不要害怕使用較大的初始視窗大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-579">Don't be afraid to use larger initial window sizes if you can use the space effectively.</span></span>
-   <span data-ttu-id="4e13e-580">**使用對稱的高度與寬度的外觀比例。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-580">**Use a balanced height to width aspect ratio.**</span></span> <span data-ttu-id="4e13e-581">建議您最好使用3:5 和5:3 之間的外觀比例，雖然 (的外觀1:3 比例可以用於訊息對話方塊例如) 錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="4e13e-581">An aspect ratio between 3:5 and 5:3 is preferred, although an aspect ratio of 1:3 can be used for message dialog boxes (such as errors and warnings).</span></span>
-   <span data-ttu-id="4e13e-582">**請盡可能使用可調整大小的視窗，以避免捲軸和截斷的資料。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-582">**Use resizable windows whenever practical to avoid scroll bars and truncated data.**</span></span> <span data-ttu-id="4e13e-583">具有動態內容、檔、影像、清單和樹狀結構的 windows，可從可調整大小的視窗中獲益。</span><span class="sxs-lookup"><span data-stu-id="4e13e-583">Windows with dynamic content, documents, images, lists, and trees benefit the most from resizable windows.</span></span>
-   <span data-ttu-id="4e13e-584">**針對文字檔，請考慮使用最大的行長度80個字元** ，讓文字更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="4e13e-584">**For text documents, consider a maximum line length of 80 characters** to make the text easy to read.</span></span> <span data-ttu-id="4e13e-585"> (字元包含字母、標點符號和空格。 ) </span><span class="sxs-lookup"><span data-stu-id="4e13e-585">(Characters include letters, punctuation, and spaces.)</span></span>
-   <span data-ttu-id="4e13e-586">固定大小的視窗：</span><span class="sxs-lookup"><span data-stu-id="4e13e-586">Fixed-sized windows:</span></span>
    -   <span data-ttu-id="4e13e-587">**固定大小的 windows 必須是完全可見且大小調整，才能納入工作區域中。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-587">**Fixed-sized windows must be entirely visible and sized to fit within the work area.**</span></span>
-   <span data-ttu-id="4e13e-588">可調整大小的視窗：</span><span class="sxs-lookup"><span data-stu-id="4e13e-588">Resizable windows:</span></span>
    -   <span data-ttu-id="4e13e-589">**可調整大小的視窗可能已針對較高的解析度進行優化，但在顯示時視需要調整為實際螢幕解析度的大小。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-589">**Resizable windows may be optimized for higher resolutions, but sized down as needed at display time to the actual screen resolution.**</span></span>
    -   <span data-ttu-id="4e13e-590">**逐漸放大的視窗大小必須顯示漸進詳細資訊。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-590">**Progressively larger window sizes must show progressively more information.**</span></span> <span data-ttu-id="4e13e-591">請確定至少有一個視窗部分或控制項具有可調整大小的內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-591">Make sure that at least one window portion or control has resizable content.</span></span>
    -   <span data-ttu-id="4e13e-592">**當調整視窗大小時，保留內容的左上角。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-592">**Keep the upper-left origin of the content fixed as the window is resized.**</span></span> <span data-ttu-id="4e13e-593">請勿在視窗大小變更時移動來源以平衡內容。</span><span class="sxs-lookup"><span data-stu-id="4e13e-593">Don't move the origin to balance the content as the window size changes.</span></span>
    -   <span data-ttu-id="4e13e-594">**如果內容可能太寬，請設定內容大小上限。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-594">**Set a maximum content size if the content can be too stretched too wide.**</span></span> <span data-ttu-id="4e13e-595">如果內容變得很困難，請不要將內容區域的大小調整到寬度超過最大寬度，或變更內容的原點，因為視窗的大小變大。</span><span class="sxs-lookup"><span data-stu-id="4e13e-595">If the content becomes unwieldy, don't resize the content area beyond its maximum width or change the content's origin as the window is resized larger.</span></span> <span data-ttu-id="4e13e-596">相反地，請保留最大寬度和固定左上角。</span><span class="sxs-lookup"><span data-stu-id="4e13e-596">Instead, keep a maximum width and a fixed upper-left origin.</span></span>
    -   <span data-ttu-id="4e13e-597">**設定最小的視窗大小（如果大小低於此值，內容就無法再使用）。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-597">**Set a minimum window size if there is a size below which the content is no longer usable.**</span></span> <span data-ttu-id="4e13e-598">針對可調整大小的控制項，請將可調整大小下限的元素大小設定為其最小的功能大小，例如清單視圖中的最小功能性</span><span class="sxs-lookup"><span data-stu-id="4e13e-598">For resizable controls, set minimum resizable element sizes to their smallest functional sizes, such as minimum functional column widths in list views.</span></span> <span data-ttu-id="4e13e-599">選擇性的 UI 元素應完全移除。</span><span class="sxs-lookup"><span data-stu-id="4e13e-599">Optional UI elements should be removed completely.</span></span>
    -   <span data-ttu-id="4e13e-600">**請考慮改變簡報，讓內容可以使用較小的大小。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-600">**Consider altering the presentation to make the content usable at smaller sizes.**</span></span>

        ![<span data-ttu-id="4e13e-601">media player 控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-601">screen shot of media player controls</span></span> ](images/vis-layout-image16.png)

        <span data-ttu-id="4e13e-602">在此範例中，Windows Media Player 會在視窗對標準格式變得太小時變更其格式。</span><span class="sxs-lookup"><span data-stu-id="4e13e-602">In this example, Windows Media Player changes its format when the window becomes too small for the standard format.</span></span>

### <a name="control-size"></a><span data-ttu-id="4e13e-603">控制項大小</span><span class="sxs-lookup"><span data-stu-id="4e13e-603">Control size</span></span>

-   <span data-ttu-id="4e13e-604">**讓所有互動式控制項至少具有相對16x16 圖元。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-604">**Make all interactive controls at least relative 16x16 pixels.**</span></span> <span data-ttu-id="4e13e-605">如此一來，所有輸入裝置（包括 Windows 平板電腦和觸控技術）都能順利運作。</span><span class="sxs-lookup"><span data-stu-id="4e13e-605">Doing so works well for all input devices, including Windows Tablet and Touch Technology.</span></span>
-   <span data-ttu-id="4e13e-606">**大小控制項以避免截斷的資料。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-606">**Size controls to avoid truncated data.**</span></span> <span data-ttu-id="4e13e-607">請勿截斷必須讀取才能執行工作的資料。</span><span class="sxs-lookup"><span data-stu-id="4e13e-607">Don't truncate data that must be read to perform a task.</span></span> <span data-ttu-id="4e13e-608">大小清單視圖資料行，以避免截斷的資料。</span><span class="sxs-lookup"><span data-stu-id="4e13e-608">Size list view columns to avoid truncated data.</span></span>
-   <span data-ttu-id="4e13e-609">**用以消除不必要滾動的大小控制項。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-609">**Size controls to eliminate unnecessary scrolling.**</span></span> <span data-ttu-id="4e13e-610">如果這樣做會消除捲軸，讓控制項稍微放大。</span><span class="sxs-lookup"><span data-stu-id="4e13e-610">Make controls slightly larger if doing so eliminates a scrollbar.</span></span> <span data-ttu-id="4e13e-611">應該不需要太多垂直捲動條，也不需要任何不需要的水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="4e13e-611">There should be few vertical scrollbars and no unnecessary horizontal scrollbars.</span></span>

    ![<span data-ttu-id="4e13e-612">清單大小的螢幕擷取畫面，以避免捲軸</span><span class="sxs-lookup"><span data-stu-id="4e13e-612">screen shot of list sized to avoid a scrollbar</span></span> ](images/vis-layout-image40.png)

    <span data-ttu-id="4e13e-613">在此範例中，下拉式清單會調整大小以消除捲軸。</span><span class="sxs-lookup"><span data-stu-id="4e13e-613">In this example, the drop-down list is sized to eliminate the scrollbar.</span></span>

-   <span data-ttu-id="4e13e-614">**減少表面上的控制項大小數目。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-614">**Reduce the number of control sizes on a surface.**</span></span> <span data-ttu-id="4e13e-615">偏好使用 [標準建議的控制項大小](#recommended-sizing-and-spacing) ，如有必要，請使用幾個一致大小的較大或較小的控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-615">Prefer using the [standard recommended control sizes](#recommended-sizing-and-spacing) and when necessary, use a few consistently sized larger or smaller controls.</span></span> <span data-ttu-id="4e13e-616">請嘗試使用單一寬度的清單方塊和樹狀檢視，而且不超過三個命令按鈕和下拉式清單的寬度。</span><span class="sxs-lookup"><span data-stu-id="4e13e-616">Try to use a single width for list boxes and tree views, and no more than three widths for command buttons and drop-down lists.</span></span> <span data-ttu-id="4e13e-617">不過，文字方塊和下拉式方塊寬度應建議其最長或預期的輸入長度。</span><span class="sxs-lookup"><span data-stu-id="4e13e-617">However, text box and combo box widths should suggest the length of their longest or expected input.</span></span>

    ![<span data-ttu-id="4e13e-618">具有清單和按鈕之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-618">screen shot of dialog box with lists and buttons</span></span> ](images/vis-layout-image41.png)

    <span data-ttu-id="4e13e-619">在此範例中，會一致地使用一個清單方塊和命令按鈕大小。</span><span class="sxs-lookup"><span data-stu-id="4e13e-619">In this example, one list box and command button size is used consistently.</span></span>

-   <span data-ttu-id="4e13e-620">**針對以其文字為基礎調整大小的控制項，請針對將當地語系化的任何文字，在較短的文字) 中包含額外的 30% (高達200%。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-620">**For controls that are sized based on their text, include an additional 30 percent (up to 200 percent for shorter text) for any text that will be localized.**</span></span> <span data-ttu-id="4e13e-621">此指導方針假設版面配置是使用英文文字所設計。</span><span class="sxs-lookup"><span data-stu-id="4e13e-621">This guideline assumes the layout is designed using English text.</span></span> <span data-ttu-id="4e13e-622">另外也請注意，此指導方針參考當地語系化的文字，而非數位。</span><span class="sxs-lookup"><span data-stu-id="4e13e-622">Note also that this guideline refers to localized text, not numbers.</span></span>
-   <span data-ttu-id="4e13e-623">**將靜態文字控制項、核取方塊和選項按鈕擴充至版面配置所容納的最大寬度。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-623">**Extend static text controls, check boxes, and radio buttons to the maximum width that will fit in the layout.**</span></span> <span data-ttu-id="4e13e-624">這樣做可避免截斷變數長度文字和當地語系化。</span><span class="sxs-lookup"><span data-stu-id="4e13e-624">Doing so avoids truncation from variable length text and localization.</span></span>

    <span data-ttu-id="4e13e-625">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-625">**Incorrect:**</span></span>

    ![<span data-ttu-id="4e13e-626">進度控制項和部分文字的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-626">screen shot of progress control and partial text</span></span> ](images/vis-layout-image42.png)

    <span data-ttu-id="4e13e-627">在此範例中，會不必要地截斷控制項文字。</span><span class="sxs-lookup"><span data-stu-id="4e13e-627">In this example, control text is unnecessarily truncated.</span></span>

### <a name="control-spacing"></a><span data-ttu-id="4e13e-628">控制項間距</span><span class="sxs-lookup"><span data-stu-id="4e13e-628">Control spacing</span></span>

-   <span data-ttu-id="4e13e-629">**如果控制項沒有觸及，則至少有3個 Dlu (5 個相對圖元之間的空間) 。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-629">**If controls aren't touching, have at least 3 DLUs (5 relative pixels) of space between them.**</span></span> <span data-ttu-id="4e13e-630">否則，使用者可以按一下控制項之間的非使用中空間。</span><span class="sxs-lookup"><span data-stu-id="4e13e-630">Otherwise, users may click on inactive space between the controls.</span></span> <span data-ttu-id="4e13e-631">由於按一下非使用中空間沒有結果或視覺效果的意見反應，因此使用者通常不確定發生什麼錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e13e-631">Since clicking inactive space has no result or visual feedback, users are often uncertain what went wrong.</span></span>

### <a name="placement"></a><span data-ttu-id="4e13e-632">放置</span><span class="sxs-lookup"><span data-stu-id="4e13e-632">Placement</span></span>

-   <span data-ttu-id="4e13e-633">**將介面中的 UI 元素排列成自然地以左至右、由上到下的順序， (在西歐文化特性中) 。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-633">**Arrange the UI elements within a surface to flow naturally in a left-to-right, top-to-bottom order (in Western cultures).**</span></span> <span data-ttu-id="4e13e-634">UI 元素的位置會傳達其關聯性，而且應該鏡像步驟來執行工作。</span><span class="sxs-lookup"><span data-stu-id="4e13e-634">The placement of the UI elements conveys their relationship and should mirror the steps to perform the task.</span></span>
-   <span data-ttu-id="4e13e-635">**將在左上角或左上角起始工作的 UI 元素放在上方。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-635">**Place UI elements that initiate a task in the upper-left corner or upper-center.**</span></span> <span data-ttu-id="4e13e-636">提供使用者應該先查看最大視覺效果的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="4e13e-636">Give the UI element that users should look at first the greatest visual emphasis.</span></span>
-   <span data-ttu-id="4e13e-637">**將完成工作的 UI 元素放在右下角。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-637">**Place UI elements that complete a task in the lower-right corner.**</span></span>
-   <span data-ttu-id="4e13e-638">**將相關的 UI 元素放在一起，並分隔不相關的元素。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-638">**Place related UI elements together, and separate unrelated elements.**</span></span>
-   <span data-ttu-id="4e13e-639">**將必要的步驟放置在主要流程中。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-639">**Place required steps in the main flow.**</span></span>
-   <span data-ttu-id="4e13e-640">**在主要流程之外放置選擇性步驟，** 可能會使用適當的背景或漸進式洩漏來將其反白。</span><span class="sxs-lookup"><span data-stu-id="4e13e-640">**Place optional steps outside the main flow,** possibly de-emphasized by using a suitable background or progressive disclosure.</span></span>
-   <span data-ttu-id="4e13e-641">**將經常使用的元素放** 在掃描路徑中不常使用的元素之前。</span><span class="sxs-lookup"><span data-stu-id="4e13e-641">**Place frequently used elements before infrequently used elements** in the scan path.</span></span>

### <a name="focus"></a><span data-ttu-id="4e13e-642">焦點</span><span class="sxs-lookup"><span data-stu-id="4e13e-642">Focus</span></span>

-   <span data-ttu-id="4e13e-643">**選擇使用者必須先查看的單一 UI 元素，才能成為焦點。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-643">**Choose a single UI element that users need to look at first to be the focal point.**</span></span> <span data-ttu-id="4e13e-644">焦點應該是使用者需要快速尋找和瞭解的重要事項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-644">The focal point should be something important that users need to find and understand quickly.</span></span>
-   <span data-ttu-id="4e13e-645">**將焦點放在左上角或左上角。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-645">**Place the focal point in the upper-left corner or upper-center.**</span></span>
-   <span data-ttu-id="4e13e-646">**讓焦點成為最大的視覺效果，** 例如醒目的文字、預設選項或初始輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="4e13e-646">**Give the focal point the greatest visual emphasis,** such as prominent text, default selection, or initial input focus.</span></span>

### <a name="alignment"></a><span data-ttu-id="4e13e-647">對齊</span><span class="sxs-lookup"><span data-stu-id="4e13e-647">Alignment</span></span>

-   <span data-ttu-id="4e13e-648">一般來說，使用靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-648">Normally, use left alignment.</span></span>
-   <span data-ttu-id="4e13e-649">針對數值資料使用靠右對齊，尤其是數值資料的資料行。</span><span class="sxs-lookup"><span data-stu-id="4e13e-649">Use right alignment for numeric data, especially columns of numeric data.</span></span>
-   <span data-ttu-id="4e13e-650">針對認可按鈕使用靠右對齊，以及對齊右視窗邊緣的控制項。</span><span class="sxs-lookup"><span data-stu-id="4e13e-650">Use right alignment for commit buttons, as well as controls aligned with right window edge.</span></span>
-   <span data-ttu-id="4e13e-651">當靠左或靠右對齊不適當或顯示不平衡時，請使用中央對齊。</span><span class="sxs-lookup"><span data-stu-id="4e13e-651">Use center alignment when either left or right alignment is inappropriate or appears unbalanced.</span></span>
-   <span data-ttu-id="4e13e-652">垂直對齊具有文字的控制項時，對齊文字基準以提供順暢的水準讀取流程。</span><span class="sxs-lookup"><span data-stu-id="4e13e-652">When vertically aligning controls with text, align the text baselines to give a smooth horizontal reading flow.</span></span>
-   <span data-ttu-id="4e13e-653">針對標籤對齊，請參閱設計概念中的 [標籤對齊](#label-alignment) 區段。</span><span class="sxs-lookup"><span data-stu-id="4e13e-653">For label alignment, refer to the [Label alignment](#label-alignment) section in Design concepts.</span></span>

### <a name="accessibility"></a><span data-ttu-id="4e13e-654">協助工具選項</span><span class="sxs-lookup"><span data-stu-id="4e13e-654">Accessibility</span></span>

-   <span data-ttu-id="4e13e-655">**請勿使用版面配置作為傳達 UI 相關重要資訊的唯一方法。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-655">**Don't use layout as the only means to convey important information about a UI.**</span></span> <span data-ttu-id="4e13e-656">具有視覺障礙的使用者可能無法解讀此簡報。</span><span class="sxs-lookup"><span data-stu-id="4e13e-656">Users who have visual impairments may not be able to interpret this presentation.</span></span> <span data-ttu-id="4e13e-657">例如，請確定控制項標籤會將其關聯性傳達給其他專案。</span><span class="sxs-lookup"><span data-stu-id="4e13e-657">For example, make sure that controls labels communicate their relationship to other items.</span></span>
-   <span data-ttu-id="4e13e-658">**請勿將次級控制項內嵌在控制項標籤中，以建立一個句子或片語。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-658">**Don't embed subordinate controls within control labels to create a sentence or phrase.**</span></span> <span data-ttu-id="4e13e-659">這類關聯純粹是以配置為基礎，而且不是由鍵盤流覽或協助工具輔助技術來妥善處理。</span><span class="sxs-lookup"><span data-stu-id="4e13e-659">Such associations are based purely on layout and aren't handled well by keyboard navigation or accessibility assistive technologies.</span></span> <span data-ttu-id="4e13e-660">此外，這項技術並不會當地語系化，因為句子結構會因語言而異。</span><span class="sxs-lookup"><span data-stu-id="4e13e-660">Furthermore, this technique isn't localizable because sentence structure varies with language.</span></span>

    <span data-ttu-id="4e13e-661">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-661">**Incorrect:**</span></span>

    ![<span data-ttu-id="4e13e-662">句子中間文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-662">screen shot of a text box in middle of a sentence</span></span> ](images/vis-layout-image43.png)

    <span data-ttu-id="4e13e-663">在此範例中，文字方塊不正確地放在核取方塊標籤內。</span><span class="sxs-lookup"><span data-stu-id="4e13e-663">In this example, the text box is incorrectly placed within the check box label.</span></span>

    <span data-ttu-id="4e13e-664">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4e13e-664">**Correct:**</span></span>

    ![<span data-ttu-id="4e13e-665">句子結尾文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-665">screen shot of a text box at the end of a sentence</span></span> ](images/vis-layout-image44.png)

    <span data-ttu-id="4e13e-666">在此，文字方塊會置於核取方塊標籤之後。</span><span class="sxs-lookup"><span data-stu-id="4e13e-666">Here, the text box is placed after the check box label.</span></span>

-   <span data-ttu-id="4e13e-667">**將群組設為可存取。**</span><span class="sxs-lookup"><span data-stu-id="4e13e-667">**Make grouping accessible.**</span></span> <span data-ttu-id="4e13e-668">視窗窗格、群組方塊、分隔符號、文字標籤和匯總工具所定義的群組，都是由協助工具輔助程式自動處理。</span><span class="sxs-lookup"><span data-stu-id="4e13e-668">Groups defined by window panes, group boxes, separators, text labels, and aggregators are automatically handled by accessibility aids.</span></span> <span data-ttu-id="4e13e-669">不過，只有位置和背景定義的群組不是，且必須以程式設計的方式定義以供存取。</span><span class="sxs-lookup"><span data-stu-id="4e13e-669">However, groups defined only by placement and backgrounds are not, and must be defined programmatically for accessibility.</span></span>

<span data-ttu-id="4e13e-670">如需詳細指導方針，請參閱 [協助工具](inter-accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="4e13e-670">For more guidelines, see [Accessibility](inter-accessibility.md).</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="4e13e-671">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="4e13e-671">Recommended sizing and spacing</span></span>

<span data-ttu-id="4e13e-672">**控制項大小調整**</span><span class="sxs-lookup"><span data-stu-id="4e13e-672">**Control sizing**</span></span>

<span data-ttu-id="4e13e-673">下表列出 (寬度 x 高度的建議大小，或者，如果通用 UI 元素的單一數位)  (9 pt，則為高度。</span><span class="sxs-lookup"><span data-stu-id="4e13e-673">The following table lists the recommended sizes (width x height, or height if a single number) for common UI elements (for 9 pt.</span></span> <span data-ttu-id="4e13e-674">Segoe UI 96 DPI) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-674">Segoe UI at 96 dpi).</span></span> <span data-ttu-id="4e13e-675">以英文的最長專案為基礎的寬度會增加30% 的當地語系化 (，最高可達 200) % 的文字 (但不是) 將當地語系化的數位。</span><span class="sxs-lookup"><span data-stu-id="4e13e-675">The widths based on the longest item in English add 30 percent for localization (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>



| <span data-ttu-id="4e13e-676">範例</span><span class="sxs-lookup"><span data-stu-id="4e13e-676">Example</span></span> | <span data-ttu-id="4e13e-677">控制</span><span class="sxs-lookup"><span data-stu-id="4e13e-677">Control</span></span> | <span data-ttu-id="4e13e-678">對話方塊單位</span><span class="sxs-lookup"><span data-stu-id="4e13e-678">Dialog units</span></span> | <span data-ttu-id="4e13e-679">相對圖元</span><span class="sxs-lookup"><span data-stu-id="4e13e-679">Relative pixels</span></span> |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ![<span data-ttu-id="4e13e-680">核取方塊及其標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-680">screen shot of check boxes and their labels</span></span> ](images/vis-layout-image45.png)<br/>       | <span data-ttu-id="4e13e-681">核取方塊</span><span class="sxs-lookup"><span data-stu-id="4e13e-681">Check boxes</span></span><br/>     | <span data-ttu-id="4e13e-682">10</span><span class="sxs-lookup"><span data-stu-id="4e13e-682">10</span></span><br/>                                                                                     | <span data-ttu-id="4e13e-683">17</span><span class="sxs-lookup"><span data-stu-id="4e13e-683">17</span></span><br/>                                                                                              |
| ![<span data-ttu-id="4e13e-684">下拉式方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-684">screen shot of combo box</span></span> ](images/vis-layout-image46.png)<br/>                          | <span data-ttu-id="4e13e-685">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="4e13e-685">Combo boxes</span></span><br/>     | <span data-ttu-id="4e13e-686">最長專案的寬度 + 30% x 14</span><span class="sxs-lookup"><span data-stu-id="4e13e-686">width of longest item + 30% x 14</span></span><br/>                                                       | <span data-ttu-id="4e13e-687">最長專案的寬度 + 30% x 23</span><span class="sxs-lookup"><span data-stu-id="4e13e-687">width of longest item + 30% x 23</span></span><br/>                                                                |
| ![<span data-ttu-id="4e13e-688">命令按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-688">screen shot of a command button</span></span> ](images/vis-layout-image47.png)<br/>                   | <span data-ttu-id="4e13e-689">命令按鈕</span><span class="sxs-lookup"><span data-stu-id="4e13e-689">Command buttons</span></span><br/> | <span data-ttu-id="4e13e-690">50 x 14</span><span class="sxs-lookup"><span data-stu-id="4e13e-690">50 x 14</span></span><br/>                                                                                | <span data-ttu-id="4e13e-691">75 x 23</span><span class="sxs-lookup"><span data-stu-id="4e13e-691">75 x 23</span></span><br/>                                                                                         |
| ![<span data-ttu-id="4e13e-692">選取了兩個命令連結之一的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-692">screen shot of one of two command links selected</span></span> ](images/vis-layout-image48.png)<br/>  | <span data-ttu-id="4e13e-693">命令連結</span><span class="sxs-lookup"><span data-stu-id="4e13e-693">Command links</span></span><br/>   | <span data-ttu-id="4e13e-694">25 (一行) 或 35 (兩行) </span><span class="sxs-lookup"><span data-stu-id="4e13e-694">25 (one line) or 35 (two lines)</span></span><br/>                                                        | <span data-ttu-id="4e13e-695">41 (一行) 或 58 (兩行) </span><span class="sxs-lookup"><span data-stu-id="4e13e-695">41 (one line) or 58 (two lines)</span></span><br/>                                                                 |
| ![<span data-ttu-id="4e13e-696">下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-696">screen shot of a drop-down list</span></span> ](images/vis-layout-image49.png)<br/>                   | <span data-ttu-id="4e13e-697">下拉式清單</span><span class="sxs-lookup"><span data-stu-id="4e13e-697">Drop-down lists</span></span><br/> | <span data-ttu-id="4e13e-698">最長有效資料的寬度 + 30% x 14</span><span class="sxs-lookup"><span data-stu-id="4e13e-698">width of longest valid data + 30% x 14</span></span><br/>                                                 | <span data-ttu-id="4e13e-699">最長專案的寬度 + 30% x 23</span><span class="sxs-lookup"><span data-stu-id="4e13e-699">width of longest item + 30% x 23</span></span><br/>                                                                |
| ![<span data-ttu-id="4e13e-700">清單方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-700">screen shot of a list box</span></span> ](images/vis-layout-image50.png)<br/>                         | <span data-ttu-id="4e13e-701">清單方塊</span><span class="sxs-lookup"><span data-stu-id="4e13e-701">List boxes</span></span><br/>      | <span data-ttu-id="4e13e-702">最長專案的寬度 + 30% x 專案的整數 (3 個專案的最小值) </span><span class="sxs-lookup"><span data-stu-id="4e13e-702">width of longest item + 30% x an integral number of items (3 items minimum)</span></span><br/>            |                                                                                                            |
| ![<span data-ttu-id="4e13e-703">圖片檔案清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-703">screen shot of a list of picture files</span></span> ](images/vis-layout-image51.png)<br/>            | <span data-ttu-id="4e13e-704">清單檢視</span><span class="sxs-lookup"><span data-stu-id="4e13e-704">List views</span></span><br/>      | <span data-ttu-id="4e13e-705">避免截斷資料的資料行寬度 x 專案的整數數目</span><span class="sxs-lookup"><span data-stu-id="4e13e-705">columns widths that avoid truncated data x an integral number of items</span></span><br/>                 |                                                                                                            |
| ![<span data-ttu-id="4e13e-706">進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-706">screen shot of a progress bar</span></span> ](images/vis-layout-image52.png)<br/>                     | <span data-ttu-id="4e13e-707">進度列</span><span class="sxs-lookup"><span data-stu-id="4e13e-707">Progress bars</span></span><br/>   | <span data-ttu-id="4e13e-708">107或 237 x 8</span><span class="sxs-lookup"><span data-stu-id="4e13e-708">107 or 237 x 8</span></span><br/>                                                                         | <span data-ttu-id="4e13e-709">160或 355 x 15</span><span class="sxs-lookup"><span data-stu-id="4e13e-709">160 or 355 x 15</span></span><br/>                                                                                 |
| ![<span data-ttu-id="4e13e-710">選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-710">screen shot of radio buttons</span></span> ](images/vis-layout-image53.png)<br/>                      | <span data-ttu-id="4e13e-711">選項按鈕</span><span class="sxs-lookup"><span data-stu-id="4e13e-711">Radio buttons</span></span><br/>   | <span data-ttu-id="4e13e-712">10</span><span class="sxs-lookup"><span data-stu-id="4e13e-712">10</span></span><br/>                                                                                     | <span data-ttu-id="4e13e-713">17</span><span class="sxs-lookup"><span data-stu-id="4e13e-713">17</span></span><br/>                                                                                              |
| ![<span data-ttu-id="4e13e-714">滑杆控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-714">screen shot of slider control</span></span> ](images/vis-layout-image54.png)<br/>                     | <span data-ttu-id="4e13e-715">滑桿</span><span class="sxs-lookup"><span data-stu-id="4e13e-715">Sliders</span></span><br/>         | <span data-ttu-id="4e13e-716">15</span><span class="sxs-lookup"><span data-stu-id="4e13e-716">15</span></span><br/>                                                                                     | <span data-ttu-id="4e13e-717">24</span><span class="sxs-lookup"><span data-stu-id="4e13e-717">24</span></span><br/>                                                                                              |
| ![<span data-ttu-id="4e13e-718">文字的螢幕擷取畫面： [選取時區]</span><span class="sxs-lookup"><span data-stu-id="4e13e-718">screen shot of text: 'select time zone'</span></span> ](images/vis-layout-image55.png)<br/>           | <span data-ttu-id="4e13e-719">Text (靜態) </span><span class="sxs-lookup"><span data-stu-id="4e13e-719">Text (static)</span></span><br/>   | <span data-ttu-id="4e13e-720">8</span><span class="sxs-lookup"><span data-stu-id="4e13e-720">8</span></span><br/>                                                                                      | <span data-ttu-id="4e13e-721">13</span><span class="sxs-lookup"><span data-stu-id="4e13e-721">13</span></span><br/>                                                                                              |
| ![<span data-ttu-id="4e13e-722">空白文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-722">screen shot of empty text box</span></span> ](images/vis-layout-image56.png)<br/>                     | <span data-ttu-id="4e13e-723">文字方塊</span><span class="sxs-lookup"><span data-stu-id="4e13e-723">Text boxes</span></span><br/>      | <span data-ttu-id="4e13e-724">最長或預期輸入的寬度 + 30% x 14 (一行) + 10 的額外一行</span><span class="sxs-lookup"><span data-stu-id="4e13e-724">width of longest or expected input + 30% x 14 (one line) + 10 for each additional line</span></span><br/> | <span data-ttu-id="4e13e-725">最長有效資料的寬度 + 30% x 23 相對圖元 (一行) + 16 代表每個額外的線</span><span class="sxs-lookup"><span data-stu-id="4e13e-725">width of longest valid data + 30% x 23 relative pixels (one line) + 16 for each additional line</span></span><br/> |
| ![<span data-ttu-id="4e13e-726">windows explorer 中嵌套資料夾的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4e13e-726">screen shot of nested folders in windows explorer</span></span> ](images/vis-layout-image57.png)<br/> | <span data-ttu-id="4e13e-727">樹狀檢視</span><span class="sxs-lookup"><span data-stu-id="4e13e-727">Tree views</span></span><br/>      | <span data-ttu-id="4e13e-728">最長專案的寬度 + 30% x 專案的整數數目 (5 個專案的最小值) </span><span class="sxs-lookup"><span data-stu-id="4e13e-728">width of longest item + 30% x an integral number of items (5 items minimum)</span></span><br/>            |                                                                                                            |



 

<span data-ttu-id="4e13e-729">**間距**</span><span class="sxs-lookup"><span data-stu-id="4e13e-729">**Spacing**</span></span>

<span data-ttu-id="4e13e-730">下表列出一般 UI 元素 (9 pt 之間的建議間距。</span><span class="sxs-lookup"><span data-stu-id="4e13e-730">The following table lists the recommended spacing between common UI elements (for 9 pt.</span></span> <span data-ttu-id="4e13e-731">Segoe UI 96 DPI) 。</span><span class="sxs-lookup"><span data-stu-id="4e13e-731">Segoe UI at 96 dpi).</span></span>



|   &nbsp; | <span data-ttu-id="4e13e-732">元素</span><span class="sxs-lookup"><span data-stu-id="4e13e-732">Element</span></span> | <span data-ttu-id="4e13e-733">對話方塊單位</span><span class="sxs-lookup"><span data-stu-id="4e13e-733">Dialog units</span></span> | <span data-ttu-id="4e13e-734">相對圖元</span><span class="sxs-lookup"><span data-stu-id="4e13e-734">Relative pixels</span></span> |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![<span data-ttu-id="4e13e-735">顯示對話方塊邊界間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-735">Image showing spacing in dialog box margins</span></span> ](images/vis_layout_image58.jpeg)<br/>        | <span data-ttu-id="4e13e-736">對話方塊邊界</span><span class="sxs-lookup"><span data-stu-id="4e13e-736">Dialog box margins</span></span><br/>                                                                         | <span data-ttu-id="4e13e-737">所有邊7</span><span class="sxs-lookup"><span data-stu-id="4e13e-737">7 on all sides</span></span><br/>                                                                 | <span data-ttu-id="4e13e-738">11的所有邊</span><span class="sxs-lookup"><span data-stu-id="4e13e-738">11 on all sides</span></span><br/>                                                                |
| ![<span data-ttu-id="4e13e-739">顯示標籤和控制項之間間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-739">Image showing spacing between labels and controls</span></span> ](images/vis_layout_image59.jpeg)<br/>  | <span data-ttu-id="4e13e-740">在文字標籤與其相關聯控制項之間 (例如，文字方塊和清單方塊) </span><span class="sxs-lookup"><span data-stu-id="4e13e-740">Between text labels and their associated controls (for example, text boxes and list boxes)</span></span><br/> | <span data-ttu-id="4e13e-741">3</span><span class="sxs-lookup"><span data-stu-id="4e13e-741">3</span></span><br/>                                                                              | <span data-ttu-id="4e13e-742">5</span><span class="sxs-lookup"><span data-stu-id="4e13e-742">5</span></span><br/>                                                                              |
| ![<span data-ttu-id="4e13e-743">顯示相關控制項之間間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-743">Image showing spacing between related controls</span></span> ](images/vis_layout_image60.jpeg)<br/>     | <span data-ttu-id="4e13e-744">在相關控制項之間</span><span class="sxs-lookup"><span data-stu-id="4e13e-744">Between related controls</span></span><br/>                                                                   | <span data-ttu-id="4e13e-745">4</span><span class="sxs-lookup"><span data-stu-id="4e13e-745">4</span></span><br/>                                                                              | <span data-ttu-id="4e13e-746">7</span><span class="sxs-lookup"><span data-stu-id="4e13e-746">7</span></span><br/>                                                                              |
| ![<span data-ttu-id="4e13e-747">顯示不相關控制項之間間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-747">Image showing spacing between unrelated controls</span></span> ](images/vis_layout_image61.jpeg)<br/>   | <span data-ttu-id="4e13e-748">不相關的控制項</span><span class="sxs-lookup"><span data-stu-id="4e13e-748">Between unrelated controls</span></span><br/>                                                                 | <span data-ttu-id="4e13e-749">7</span><span class="sxs-lookup"><span data-stu-id="4e13e-749">7</span></span><br/>                                                                              | <span data-ttu-id="4e13e-750">11</span><span class="sxs-lookup"><span data-stu-id="4e13e-750">11</span></span><br/>                                                                             |
| ![<span data-ttu-id="4e13e-751">顯示群組中第一個控制項間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-751">Image showing spacing of first control in a group</span></span> ](images/vis_layout_image62.jpeg)<br/>  | <span data-ttu-id="4e13e-752">群組方塊中的第一個控制項</span><span class="sxs-lookup"><span data-stu-id="4e13e-752">First control in a group box</span></span><br/>                                                               | <span data-ttu-id="4e13e-753">11向下群組方塊的頂端;垂直對齊群組框標題</span><span class="sxs-lookup"><span data-stu-id="4e13e-753">11 down from the top of the group box; align vertically to the group box title</span></span><br/> | <span data-ttu-id="4e13e-754">群組方塊頂端的向下16個，垂直對齊群組框標題</span><span class="sxs-lookup"><span data-stu-id="4e13e-754">16 down from the top of the group box; align vertically to the group box title</span></span><br/> |
| ![Aa511279 與 en-us 之間的 (en-us、MSDN. 10) .jpg](images/vis_layout_image60.jpeg)<br/>         | <span data-ttu-id="4e13e-756">群組方塊中的控制項之間</span><span class="sxs-lookup"><span data-stu-id="4e13e-756">Between controls in a group box</span></span><br/>                                                            | <span data-ttu-id="4e13e-757">4</span><span class="sxs-lookup"><span data-stu-id="4e13e-757">4</span></span><br/>                                                                              | <span data-ttu-id="4e13e-758">7</span><span class="sxs-lookup"><span data-stu-id="4e13e-758">7</span></span><br/>                                                                              |
| ![<span data-ttu-id="4e13e-759">顯示按鈕之間間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-759">Image showing spacing between buttons</span></span> ](images/vis_layout_image63.jpeg)<br/>              | <span data-ttu-id="4e13e-760">水準或垂直排列的按鈕之間</span><span class="sxs-lookup"><span data-stu-id="4e13e-760">Between horizontally or vertically arranged buttons</span></span><br/>                                        | <span data-ttu-id="4e13e-761">4</span><span class="sxs-lookup"><span data-stu-id="4e13e-761">4</span></span><br/>                                                                              | <span data-ttu-id="4e13e-762">7</span><span class="sxs-lookup"><span data-stu-id="4e13e-762">7</span></span><br/>                                                                              |
| ![<span data-ttu-id="4e13e-763">顯示群組中最後一個控制項間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-763">Image showing spacing of last control in a group</span></span> ](images/vis_layout_image64.jpeg)<br/>   | <span data-ttu-id="4e13e-764">群組方塊中的最後一個控制項</span><span class="sxs-lookup"><span data-stu-id="4e13e-764">Last control in a group box</span></span><br/>                                                                | <span data-ttu-id="4e13e-765">群組方塊底部的7</span><span class="sxs-lookup"><span data-stu-id="4e13e-765">7 above the bottom of the group box</span></span><br/>                                            | <span data-ttu-id="4e13e-766">群組方塊底部的11</span><span class="sxs-lookup"><span data-stu-id="4e13e-766">11 above the bottom of the group box</span></span><br/>                                           |
| ![<span data-ttu-id="4e13e-767">顯示群組方塊左邊緣間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-767">Image showing spacing from left edge of group box</span></span> ](images/vis_layout_image65.jpeg)<br/>  | <span data-ttu-id="4e13e-768">從群組方塊的左邊緣</span><span class="sxs-lookup"><span data-stu-id="4e13e-768">From the left edge of a group box</span></span><br/>                                                          | <span data-ttu-id="4e13e-769">6</span><span class="sxs-lookup"><span data-stu-id="4e13e-769">6</span></span><br/>                                                                              | <span data-ttu-id="4e13e-770">9</span><span class="sxs-lookup"><span data-stu-id="4e13e-770">9</span></span><br/>                                                                              |
| ![<span data-ttu-id="4e13e-771">顯示控制項旁文字標籤間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-771">Image showing spacing of text label beside control</span></span> ](images/vis_layout_image66.jpeg)<br/> | <span data-ttu-id="4e13e-772">控制項旁的文字標籤</span><span class="sxs-lookup"><span data-stu-id="4e13e-772">Text label beside a control</span></span><br/>                                                                | <span data-ttu-id="4e13e-773">從控制項頂端向下3下</span><span class="sxs-lookup"><span data-stu-id="4e13e-773">3 down from the top of the control</span></span><br/>                                             | <span data-ttu-id="4e13e-774">從控制項頂端向下5下</span><span class="sxs-lookup"><span data-stu-id="4e13e-774">5 down from the top of the control</span></span><br/>                                             |
| ![<span data-ttu-id="4e13e-775">顯示文欄位落之間間距的影像</span><span class="sxs-lookup"><span data-stu-id="4e13e-775">Image showing spacing between paragraphs of text</span></span> ](images/vis_layout_image67.jpeg)<br/>   | <span data-ttu-id="4e13e-776">文欄位落之間</span><span class="sxs-lookup"><span data-stu-id="4e13e-776">Between paragraphs of text</span></span><br/>                                                                 | <span data-ttu-id="4e13e-777">7</span><span class="sxs-lookup"><span data-stu-id="4e13e-777">7</span></span><br/>                                                                              | <span data-ttu-id="4e13e-778">11</span><span class="sxs-lookup"><span data-stu-id="4e13e-778">11</span></span><br/>                                                                             |
|                                                                                                   | <span data-ttu-id="4e13e-779">互動式控制項之間的最小空間</span><span class="sxs-lookup"><span data-stu-id="4e13e-779">Smallest space between interactive controls</span></span><br/>                                                | <span data-ttu-id="4e13e-780">3或無空格</span><span class="sxs-lookup"><span data-stu-id="4e13e-780">3 or no space</span></span><br/>                                                                  | <span data-ttu-id="4e13e-781">5或無空格</span><span class="sxs-lookup"><span data-stu-id="4e13e-781">5 or no space</span></span><br/>                                                                  |
|                                                                                                   | <span data-ttu-id="4e13e-782">非互動式控制項和任何其他控制項之間的最小空間</span><span class="sxs-lookup"><span data-stu-id="4e13e-782">Smallest space between a non-interactive control and any other control</span></span><br/>                     | <span data-ttu-id="4e13e-783">2</span><span class="sxs-lookup"><span data-stu-id="4e13e-783">2</span></span><br/>                                                                              | <span data-ttu-id="4e13e-784">3</span><span class="sxs-lookup"><span data-stu-id="4e13e-784">3</span></span><br/>                                                                              |



 

 

