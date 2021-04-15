---
title: '狀態列 (設計基本概念) '
description: 狀態列是主視窗底部的區域，可顯示目前視窗狀態的相關資訊 (例如，正在查看的內容，以及) 、背景工作 (例如列印、掃描和格式化) ，或其他內容資訊 (例如選取專案和鍵盤狀態) 。
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8f65d104f59cd0aec0c242d623f83c410c22f48d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195679"
---
# <a name="status-bars-design-basics"></a><span data-ttu-id="f9d9a-103">狀態列 (設計基本概念) </span><span class="sxs-lookup"><span data-stu-id="f9d9a-103">Status Bars (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="f9d9a-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="f9d9a-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="f9d9a-106">狀態列是主視窗底部的區域，可顯示目前視窗狀態的相關資訊 (例如，正在查看的內容，以及) 、背景工作 (例如列印、掃描和格式化) ，或其他內容資訊 (例如選取專案和鍵盤狀態) 。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-106">A status bar is an area at the bottom of a primary window that displays information about the current window's state (such as what is being viewed and how), background tasks (such as printing, scanning, and formatting), or other contextual information (such as selection and keyboard state).</span></span>

<span data-ttu-id="f9d9a-107">狀態列通常會透過文字和圖示來指出狀態，但也可以有進度指標，以及與狀態相關的命令和選項功能表。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-107">Status bars typically indicate status through text and icons, but they can also have progress indicators, as well as menus for commands and options related to status.</span></span>

![<span data-ttu-id="f9d9a-108">一般狀態列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-108">screen shot of typical status bar</span></span> ](images/ctrl-status-bars-image1.png)

<span data-ttu-id="f9d9a-109">一般狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-109">A typical status bar.</span></span>

> [!Note]  
> <span data-ttu-id="f9d9a-110">與 [通知區域](winenv-notification.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-110">Guidelines related to the [notification area](winenv-notification.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="f9d9a-111">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="f9d9a-111">Is this the right user interface?</span></span>

<span data-ttu-id="f9d9a-112">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="f9d9a-112">To decide, consider these questions:</span></span>

-   <span data-ttu-id="f9d9a-113">**當使用者主動使用其他程式時，狀態是否相關？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-113">**Is the status relevant when users are actively using other programs?**</span></span> <span data-ttu-id="f9d9a-114">若是如此，請使用 [通知區域圖示](winenv-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-114">If so, use a [notification area icons](winenv-notification.md).</span></span>
-   <span data-ttu-id="f9d9a-115">**狀態專案是否需要顯示通知？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-115">**Does the status item need to display notifications?**</span></span> <span data-ttu-id="f9d9a-116">如果是，您必須使用通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-116">If so, you must use a notification area icon.</span></span>
-   <span data-ttu-id="f9d9a-117">**視窗是否為主視窗？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-117">**Is the window a primary window?**</span></span> <span data-ttu-id="f9d9a-118">如果沒有，請不要使用狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-118">If not, don't use a status bar.</span></span> <span data-ttu-id="f9d9a-119">對話方塊、嚮導、控制台和屬性工作表不應該有狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-119">Dialog boxes, wizards, control panels, and property sheets shouldn't have status bars.</span></span>
-   <span data-ttu-id="f9d9a-120">**資訊的主要狀態為何？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-120">**Is the information primarily status?**</span></span> <span data-ttu-id="f9d9a-121">如果沒有，請不要使用狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-121">If not, don't use a status bar.</span></span> <span data-ttu-id="f9d9a-122">狀態列不能用來做為次要 [功能表列](cmd-menus.md) 或 [工具列](cmd-toolbars.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-122">Status bars must not be used as a secondary [menu bar](cmd-menus.md) or [toolbar](cmd-toolbars.md).</span></span>
-   <span data-ttu-id="f9d9a-123">**資訊會說明如何使用選取的控制項？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-123">**Does the information explain how to use the selected control?**</span></span> <span data-ttu-id="f9d9a-124">若是如此，請改為使用補充說明或指令標籤，在相關聯的控制項旁邊顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-124">If so, display the information next to the associated control using a supplemental explanation or instruction label instead.</span></span>
-   <span data-ttu-id="f9d9a-125">**狀態是否有用且相關？也就是說，使用者是否有可能因為這項資訊而變更其行為？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-125">**Is the status useful and relevant? That is, are users likely to change their behavior as a result of this information?**</span></span> <span data-ttu-id="f9d9a-126">如果不是，則不會顯示狀態，也不會將它放入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-126">If not, either don't display the status, or put it in a log file.</span></span>
-   <span data-ttu-id="f9d9a-127">**狀態是否危急？是否需要立即採取動作？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-127">**Is the status critical? Is immediate action required?**</span></span> <span data-ttu-id="f9d9a-128">如果是的話，請以需要注意的形式來顯示資訊，而且無法輕易地忽略，例如 [對話方塊](win-dialog-box.md) 或主視窗本身內。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-128">If so, display the information in a form that demands attention and cannot be easily ignored, such as a [dialog box](win-dialog-box.md) or within the primary window itself.</span></span>

    ![<span data-ttu-id="f9d9a-129">紅色 [憑證錯誤] 狀態列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-129">screen shot of red 'certificate error' status bar</span></span> ](images/ctrl-status-bars-image2.png)

    <span data-ttu-id="f9d9a-130">Windows Internet Explorer 中的紅色位址列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-130">A red address bar in Windows Internet Explorer.</span></span>

-   <span data-ttu-id="f9d9a-131">**程式主要是供新手使用者的用嗎？**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-131">**Is the program intended primarily for novice users?**</span></span> <span data-ttu-id="f9d9a-132">缺乏經驗的使用者通常不知道狀態列，因此在此情況下請重新考慮使用狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-132">Inexperienced users are generally unaware of status bars, so reconsider the use of status bars in this case.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="f9d9a-133">設計概念</span><span class="sxs-lookup"><span data-stu-id="f9d9a-133">Design concepts</span></span>

<span data-ttu-id="f9d9a-134">狀態列是在不中斷使用者或中斷其流程的情況下提供狀態資訊的絕佳方式。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-134">Status bars are a great way to provide status information without interrupting users or breaking their flow.</span></span> <span data-ttu-id="f9d9a-135">不過，狀態列很容易忽略。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-135">However, status bars are easy to overlook.</span></span> <span data-ttu-id="f9d9a-136">很簡單，事實上許多使用者都不會注意到狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-136">So easy, in fact, that many users don't notice status bars at all.</span></span>

<span data-ttu-id="f9d9a-137">這個問題的解決方法，不是使用花俏圖示、動畫或閃爍來設計這項限制，而不需要使用者注意。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-137">The solution to this problem isn't to demand the user's attention by using garish icons, animation, or flashing, but to design for this limitation.</span></span> <span data-ttu-id="f9d9a-138">您可以這麼做來達到此目的：</span><span class="sxs-lookup"><span data-stu-id="f9d9a-138">You can do this by:</span></span>

-   <span data-ttu-id="f9d9a-139">**確定狀態資訊有説明且相關。**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-139">**Making sure that the status information is useful and relevant.**</span></span> <span data-ttu-id="f9d9a-140">如果沒有，請完全不提供狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-140">If not, don't provide a status bar at all.</span></span>
-   <span data-ttu-id="f9d9a-141">**請勿使用狀態列來取得重要資訊。**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-141">**Not using status bars for crucial information.**</span></span> <span data-ttu-id="f9d9a-142">使用者永遠都不需要知道狀態列中的內容。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-142">Users should never have to know what is in the status bar.</span></span> <span data-ttu-id="f9d9a-143">如果使用者必須看到它，請不要將它放在狀態列中。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-143">If users must see it, don't put it in a status bar.</span></span>

<span data-ttu-id="f9d9a-144">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-144">**If you do only one thing...**</span></span>

<span data-ttu-id="f9d9a-145">請確定狀態列資訊有説明且相關，但不重要。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-145">Make sure that the status bar information is useful and relevant but not crucial.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="f9d9a-146">使用模式</span><span class="sxs-lookup"><span data-stu-id="f9d9a-146">Usage patterns</span></span>

<span data-ttu-id="f9d9a-147">狀態列有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="f9d9a-147">Status bars have several usage patterns:</span></span>



|                                                                                                                                    |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d9a-148">**目前的視窗狀態**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-148">**Current window status**</span></span><br/> <span data-ttu-id="f9d9a-149">顯示正在顯示的內容和任何視圖模式的來源</span><span class="sxs-lookup"><span data-stu-id="f9d9a-149">Show the source of what is being displayed along with any view modes</span></span> <br/>              | ![<span data-ttu-id="f9d9a-150">[位置] 狀態列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-150">screen shot of a 'location' status bar</span></span> ](images/ctrl-status-bars-image3.png)<br/> <span data-ttu-id="f9d9a-151">在此範例中，狀態列會顯示檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-151">In this example, the status bar displays the path to the document.</span></span><br/>                                                         |
| <span data-ttu-id="f9d9a-152">**Progress**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-152">**Progress**</span></span><br/> <span data-ttu-id="f9d9a-153">使用確定進度列或動畫來顯示背景工作的進度。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-153">Show the progress of background tasks, either with a determinate progress bar or an animation.</span></span> <br/> | ![<span data-ttu-id="f9d9a-154">具有進度列狀態列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-154">screen shot of status bar with progress bar</span></span> ](images/ctrl-status-bars-image4.png)<br/> <span data-ttu-id="f9d9a-155">在此範例中，狀態列包含一個進度列，可顯示網頁載入 Internet Explorer 視窗。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-155">In this example, the status bar includes a progress bar to show the Web page loading into a Internet Explorer window.</span></span><br/> |
| <span data-ttu-id="f9d9a-156">**內容相關的資訊**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-156">**Contextual information**</span></span><br/> <span data-ttu-id="f9d9a-157">顯示使用者目前正在執行之工作的相關內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-157">Show contextual information about what the user is currently doing.</span></span> <br/>              | ![<span data-ttu-id="f9d9a-158">顯示圖元數目的狀態列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-158">screen shot of status bar showing number of pixels</span></span> ](images/ctrl-status-bars-image5.png)<br/> <span data-ttu-id="f9d9a-159">在此範例中，Microsoft 小畫家會顯示選取大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-159">In this example, Microsoft Paint shows the selection size in pixels.</span></span><br/>                                           |



 

## <a name="guidelines"></a><span data-ttu-id="f9d9a-160">指導方針</span><span class="sxs-lookup"><span data-stu-id="f9d9a-160">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="f9d9a-161">一般</span><span class="sxs-lookup"><span data-stu-id="f9d9a-161">General</span></span>

-   <span data-ttu-id="f9d9a-162">如果只有部分使用者需要狀態列資訊，請考慮提供 [View] 狀態列命令。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-162">Consider providing a View Status Bar command if only some users will need the status bar information.</span></span> <span data-ttu-id="f9d9a-163">如果大部分的使用者都不需要，請依預設隱藏狀態列。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-163">Hide the status bar by default if most users won't need it.</span></span>
-   <span data-ttu-id="f9d9a-164">請勿使用狀態列來說明功能表列專案。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-164">Don't use the status bar to explain menu bar items.</span></span> <span data-ttu-id="f9d9a-165">無法探索此說明模式。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-165">This help pattern isn't discoverable.</span></span>

### <a name="presentation"></a><span data-ttu-id="f9d9a-166">簡報</span><span class="sxs-lookup"><span data-stu-id="f9d9a-166">Presentation</span></span>

-   <span data-ttu-id="f9d9a-167">停用不適用的強制回應狀態。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-167">Disable modal status that doesn't apply.</span></span> <span data-ttu-id="f9d9a-168">強制回應狀態包括鍵盤和檔狀態。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-168">Modal status includes keyboard and document states.</span></span>
-   <span data-ttu-id="f9d9a-169">移除不適用的非強制回應狀態。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-169">Remove non-modal status that doesn't apply.</span></span>
-   <span data-ttu-id="f9d9a-170">以下列順序顯示狀態資訊：目前的視窗狀態;繼續和內容相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-170">Present status information in the following order: current window status; progress; and contextual information.</span></span>

### <a name="icons"></a><span data-ttu-id="f9d9a-171">圖示</span><span class="sxs-lookup"><span data-stu-id="f9d9a-171">Icons</span></span>

-   <span data-ttu-id="f9d9a-172">選擇容易辨識的狀態圖示設計。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-172">Choose easily recognizable status icon designs.</span></span> <span data-ttu-id="f9d9a-173">偏好在正方形或矩形圖示上具有唯一輪廓的圖示。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-173">Prefer icons with unique outlines over square or rectangular shaped icons.</span></span>
-   <span data-ttu-id="f9d9a-174">只使用純紅色、黃色和綠色的大量來傳達狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-174">Use swaths of pure red, yellow, and green only to communicate status information.</span></span> <span data-ttu-id="f9d9a-175">否則，這類圖示會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-175">Otherwise, such icons are confusing.</span></span>

    <span data-ttu-id="f9d9a-176">**正確：**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-176">**Correct:**</span></span>

    ![<span data-ttu-id="f9d9a-177">具有藍色圖示的狀態列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-177">screen shot of status bar with blue icons</span></span> ](images/ctrl-status-bars-image6.png)

    <span data-ttu-id="f9d9a-178">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-178">**Incorrect:**</span></span>

    ![<span data-ttu-id="f9d9a-179">具有紅色圖示的狀態列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-179">screen shot of status bar with a red icon</span></span> ](images/ctrl-status-bars-image7.png)

    <span data-ttu-id="f9d9a-180">在不正確的範例中，紅色圖示會不慎建議錯誤，因而造成混淆。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-180">In the incorrect example, the red icon unintentionally suggests an error, creating confusion.</span></span>

-   <span data-ttu-id="f9d9a-181">使用圖示變化或覆迭來指出狀態或狀態變更。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-181">Use icon variations or overlays to indicate status or status changes.</span></span> <span data-ttu-id="f9d9a-182">使用圖示變化顯示數量或強度的變更。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-182">Use icon variations to show changes in quantities or strengths.</span></span> <span data-ttu-id="f9d9a-183">針對其他類型的狀態，請使用下列標準重迭：</span><span class="sxs-lookup"><span data-stu-id="f9d9a-183">For other types of status, use these standard overlays:</span></span> 

    |                                                                                               |                                  |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="f9d9a-184">**覆蓋**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-184">**Overlay**</span></span><br/>                                                                        | <span data-ttu-id="f9d9a-185">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f9d9a-185">**Status**</span></span><br/>            |
    | ![<span data-ttu-id="f9d9a-186">警告圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-186">screen shot of warning icon</span></span> ](images/ctrl-status-bars-image8.png)<br/>                | <span data-ttu-id="f9d9a-187">警告</span><span class="sxs-lookup"><span data-stu-id="f9d9a-187">Warning</span></span><br/>               |
    | ![<span data-ttu-id="f9d9a-188">錯誤圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-188">screen shot of error icon</span></span> ](images/ctrl-status-bars-image9.png)<br/>                  | <span data-ttu-id="f9d9a-189">錯誤</span><span class="sxs-lookup"><span data-stu-id="f9d9a-189">Error</span></span><br/>                 |
    | ![<span data-ttu-id="f9d9a-190">已停用/已中斷連線圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-190">screen shot of disabled/disconnected icon</span></span> ](images/ctrl-status-bars-image10.png)<br/> | <span data-ttu-id="f9d9a-191">已停用/已中斷連線</span><span class="sxs-lookup"><span data-stu-id="f9d9a-191">Disabled/Disconnected</span></span><br/> |
    | ![<span data-ttu-id="f9d9a-192">[封鎖/離線] 圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f9d9a-192">screen shot of blocked/offline icon</span></span> ](images/ctrl-status-bars-image11.png)<br/>       | <span data-ttu-id="f9d9a-193">封鎖/離線</span><span class="sxs-lookup"><span data-stu-id="f9d9a-193">Blocked/Offline</span></span><br/>       |

    

     

-   <span data-ttu-id="f9d9a-194">請勿變更太頻繁的狀態。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-194">Don't change status too frequently.</span></span> <span data-ttu-id="f9d9a-195">狀態列圖示不應該出現雜訊、不穩定或需要注意。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-195">Status bar icons shouldn't appear noisy, unstable, or demand attention.</span></span> <span data-ttu-id="f9d9a-196">眼睛對周邊周邊領域的變化很敏感，因此狀態變更必須很微妙。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-196">The eye is sensitive to changes in the peripheral field of vision, so status changes need to be subtle.</span></span>
-   <span data-ttu-id="f9d9a-197">針對提供重要狀態資訊的圖示，建議使用就地標籤。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-197">For icons that provide important status information, prefer in-place labels.</span></span>
-   <span data-ttu-id="f9d9a-198">未標記的狀態列圖示應該有工具提示。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-198">Unlabeled status bar icons should have tooltips.</span></span>

<span data-ttu-id="f9d9a-199">如需詳細資訊，請參閱 [圖示](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-199">For more information, see [Icons](vis-icons.md).</span></span>

### <a name="interaction"></a><span data-ttu-id="f9d9a-200">互動</span><span class="sxs-lookup"><span data-stu-id="f9d9a-200">Interaction</span></span>

-   <span data-ttu-id="f9d9a-201">使狀態列區域成為互動，讓使用者能夠直接存取相關的命令和選項。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-201">Make a status bar area interactive to allow users direct access to related commands and options.</span></span>
    -   <span data-ttu-id="f9d9a-202">使用外觀和行為類似 [功能表按鈕](ctrl-command-buttons.md) 或分割按鈕的控制項。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-202">Use a control that looks and behaves like a [menu button](ctrl-command-buttons.md) or a split button.</span></span> <span data-ttu-id="f9d9a-203">這些狀態列區域必須有下拉箭號，才能表示可以按一下。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-203">These status bar areas must have a drop-down arrow to indicate that they are clickable.</span></span>
    -   <span data-ttu-id="f9d9a-204">以滑鼠右鍵按一下滑鼠，而不是滑鼠靠下顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-204">Display the menu on left-click on mouse down, not mouse up.</span></span>
    -   <span data-ttu-id="f9d9a-205">不支援按一下滑鼠右鍵或按兩下。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-205">Don't support right-clicking or double-clicking.</span></span> <span data-ttu-id="f9d9a-206">使用者不會預期狀態列中的這類互動，因此不可能嘗試這些互動。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-206">Users don't expect such interactions in a status bar, so they aren't likely to attempt them.</span></span>
-   <span data-ttu-id="f9d9a-207">停留時顯示工具提示。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-207">Display tooltips on hover.</span></span>

## <a name="text"></a><span data-ttu-id="f9d9a-208">Text</span><span class="sxs-lookup"><span data-stu-id="f9d9a-208">Text</span></span>

-   <span data-ttu-id="f9d9a-209">一般而言，使用簡潔的標籤。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-209">Generally, use concise labels.</span></span> <span data-ttu-id="f9d9a-210">剪下可以消除的任何文字。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-210">Cut any text that can be eliminated.</span></span>
-   <span data-ttu-id="f9d9a-211">偏好句子片段，不含結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-211">Prefer sentence fragments, without ending punctuation.</span></span> <span data-ttu-id="f9d9a-212">只有在句子片段沒有明顯較短的時間時，才能使用完整句子 (搭配結束標點符號) 。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-212">Use full sentences (with ending punctuation) only when sentence fragments aren't significantly shorter.</span></span>
-   <span data-ttu-id="f9d9a-213">若為選擇性的進度標籤，請使用開頭為動詞 (現在表單的標籤來指出作業的執行方式，) 並以省略號結尾。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-213">For optional progress labels, indicate what the operation is doing with a label that starts with a verb (gerund form) and ends with an ellipsis.</span></span> <span data-ttu-id="f9d9a-214">例如：「正在複製 ...」。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-214">For example: "Copying...".</span></span> <span data-ttu-id="f9d9a-215">如果作業有多個步驟或正在處理多個物件，此標籤可能會動態變更。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-215">This label may change dynamically if the operation has multiple steps or is processing multiple objects.</span></span>
-   <span data-ttu-id="f9d9a-216">請勿使用色彩、粗體或斜體來強調狀態列文字。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-216">Don't use color, bold, or italic to emphasize status bar text.</span></span>
-   <span data-ttu-id="f9d9a-217">如需工具提示片語的指導方針，請參閱 [工具提示和提示](ctrl-tooltips-and-infotips.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-217">For tooltip phrasing guidelines, see [Tooltips and Infotips](ctrl-tooltips-and-infotips.md).</span></span>

## <a name="documentation"></a><span data-ttu-id="f9d9a-218">文件</span><span class="sxs-lookup"><span data-stu-id="f9d9a-218">Documentation</span></span>

<span data-ttu-id="f9d9a-219">請將狀態列視為狀態列，而不是狀態行或其他變化。</span><span class="sxs-lookup"><span data-stu-id="f9d9a-219">Refer to status bars as status bars, not status lines or other variations.</span></span> <span data-ttu-id="f9d9a-220">範例：「狀態列上顯示目前的頁碼。」</span><span class="sxs-lookup"><span data-stu-id="f9d9a-220">Example: "The current page number is displayed on the status bar."</span></span>

 

