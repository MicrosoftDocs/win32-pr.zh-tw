---
title: 進度列
description: 使用進度列時，使用者可以追蹤長時間操作的進度。 進度列可能會顯示完成 (確定) 的大約百分比，或表示作業正在進行中 (不定) 。
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db8aca7300b309fb6929106cf97329956b7accb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555374"
---
# <a name="progress-bars"></a><span data-ttu-id="2a158-104">進度列</span><span class="sxs-lookup"><span data-stu-id="2a158-104">Progress Bars</span></span>

> [!NOTE]
> <span data-ttu-id="2a158-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="2a158-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="2a158-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="2a158-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="2a158-107">使用進度列時，使用者可以追蹤長時間操作的進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-107">With a progress bar, users can follow the progress of a lengthy operation.</span></span> <span data-ttu-id="2a158-108">進度列可能會顯示完成 (確定) 的大約百分比，或表示作業正在進行中 (不定) 。</span><span class="sxs-lookup"><span data-stu-id="2a158-108">A progress bar may either show an approximate percentage of completion (determinate), or indicate that an operation is ongoing (indeterminate).</span></span>

<span data-ttu-id="2a158-109">可用性研究顯示，使用者知道回應時間超過一秒。</span><span class="sxs-lookup"><span data-stu-id="2a158-109">Usability studies have shown that users are aware of response times of over one second.</span></span> <span data-ttu-id="2a158-110">因此，您應該考慮需要兩秒或更長時間才能完成的作業，這需要一些時間才能完成，而且需要一些類型的進度意見反應。</span><span class="sxs-lookup"><span data-stu-id="2a158-110">Consequently, you should consider operations that take two seconds or longer to complete to be lengthy and in need of some type of progress feedback.</span></span>

![<span data-ttu-id="2a158-111">一般進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-111">screen shot of a typical progress bar</span></span> ](images/progress-bars-image1.png)

<span data-ttu-id="2a158-112">一般的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-112">A typical progress bar.</span></span>

> [!Note]  
> <span data-ttu-id="2a158-113">與 [版面](vis-layout.md) 配置相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="2a158-113">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="2a158-114">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="2a158-114">Is this the right control?</span></span>

<span data-ttu-id="2a158-115">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="2a158-115">To decide, consider these questions:</span></span>

-   <span data-ttu-id="2a158-116">**作業會在五秒內完成嗎？**</span><span class="sxs-lookup"><span data-stu-id="2a158-116">**Will the operation complete in about five seconds or less?**</span></span> <span data-ttu-id="2a158-117">若是如此，請改為使用 [活動指標](inter-mouse.md) ，因為顯示短暫期間的進度列會造成干擾。</span><span class="sxs-lookup"><span data-stu-id="2a158-117">If so, use an [activity indicator](inter-mouse.md) instead, because displaying a progress bar for such a short duration would be distracting.</span></span> <span data-ttu-id="2a158-118">如果作業通常需要五秒或更少，但有時需要更多時間，請從忙碌指標開始，然後在五秒後轉換成進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-118">If the operation usually takes five seconds or less but sometimes takes more, start with a busy pointer and convert to a progress bar after five seconds.</span></span>
-   <span data-ttu-id="2a158-119">**是否有不定的進度列可用來等候使用者完成工作？**</span><span class="sxs-lookup"><span data-stu-id="2a158-119">**Is an indeterminate progress bar used to wait for the user to complete a task?**</span></span> <span data-ttu-id="2a158-120">如果是，請不要使用進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-120">If so, don't use a progress bar.</span></span> <span data-ttu-id="2a158-121">進度列適用于電腦進度，而不是使用者進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-121">Progress bars are for computer progress, not user progress.</span></span>
-   <span data-ttu-id="2a158-122">**是否與動畫結合不定的進度列？**</span><span class="sxs-lookup"><span data-stu-id="2a158-122">**Is an indeterminate progress bar combined with an animation?**</span></span> <span data-ttu-id="2a158-123">若是如此，請改用動畫。</span><span class="sxs-lookup"><span data-stu-id="2a158-123">If so, use just the animation instead.</span></span> <span data-ttu-id="2a158-124">不定的進度列實際上是泛型動畫，不會將任何值新增至動畫。</span><span class="sxs-lookup"><span data-stu-id="2a158-124">The indeterminate progress bar is effectively a generic animation and adds no value to the animation.</span></span>
-   <span data-ttu-id="2a158-125">**這項作業的 (長達兩分鐘的時間，) 背景工作是否比進度更有興趣完成？**</span><span class="sxs-lookup"><span data-stu-id="2a158-125">**Is the operation a very lengthy (longer than two minutes) background task for which users are more interested in completion than progress?**</span></span> <span data-ttu-id="2a158-126">若是如此，請改為使用 [通知](mess-notif.md) 。</span><span class="sxs-lookup"><span data-stu-id="2a158-126">If so, use a [notifications](mess-notif.md) instead.</span></span> <span data-ttu-id="2a158-127">在此情況下，使用者會在此同時執行其他工作，且不會監視進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-127">In this case, users do other tasks in the meantime and are not monitoring the progress.</span></span> <span data-ttu-id="2a158-128">使用通知可讓使用者在不中斷的情況下執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="2a158-128">Using a notification allows users to perform other tasks without disruption.</span></span> <span data-ttu-id="2a158-129">這類冗長作業的範例包括列印、備份、系統掃描，以及大量資料傳輸或轉換。</span><span class="sxs-lookup"><span data-stu-id="2a158-129">Examples of such lengthy operations include printing, backup, system scans, and bulk data transfers or conversions.</span></span>
-   <span data-ttu-id="2a158-130">**當作業完成時，使用者是否能夠重新播放結果？**</span><span class="sxs-lookup"><span data-stu-id="2a158-130">**When the operation is complete, will users be able to replay the results?**</span></span> <span data-ttu-id="2a158-131">如果是的話，請改用滑杆。</span><span class="sxs-lookup"><span data-stu-id="2a158-131">If so, use a slider instead.</span></span> <span data-ttu-id="2a158-132">這類作業的範例包括影片和音訊錄製和播放。</span><span class="sxs-lookup"><span data-stu-id="2a158-132">Examples of such operations include video and audio recording and playback.</span></span>

    ![<span data-ttu-id="2a158-133">media player 和滑杆的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-133">screen shot of media player and slider</span></span> ](images/progress-bars-image2.png)

    <span data-ttu-id="2a158-134">在此範例中，滑杆可用來指出播放音效的進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-134">In this example, a slider is used to indicate progress while playing sound.</span></span> <span data-ttu-id="2a158-135">這麼做可讓使用者在稍後重新執行結果。</span><span class="sxs-lookup"><span data-stu-id="2a158-135">Doing so allows users to replay the results later.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="2a158-136">設計概念</span><span class="sxs-lookup"><span data-stu-id="2a158-136">Design concepts</span></span>

<span data-ttu-id="2a158-137">在冗長的作業期間，使用者需要對作業進行作業的一般概念。</span><span class="sxs-lookup"><span data-stu-id="2a158-137">During a lengthy operation, users need a general idea of what the operation is doing.</span></span> <span data-ttu-id="2a158-138">他們也需要知道：</span><span class="sxs-lookup"><span data-stu-id="2a158-138">They also need to know:</span></span>

-   <span data-ttu-id="2a158-139">這是一段冗長的作業已開始。</span><span class="sxs-lookup"><span data-stu-id="2a158-139">That a lengthy operation has started.</span></span>
-   <span data-ttu-id="2a158-140">正在進行該進度，而且作業最後會完成 (，因此未鎖定) 。</span><span class="sxs-lookup"><span data-stu-id="2a158-140">That progress is being made and that the operation will eventually complete (and therefore hasn't locked up).</span></span>
-   <span data-ttu-id="2a158-141">已 (完成的作業大約百分比，因此是剩餘的百分比) 。</span><span class="sxs-lookup"><span data-stu-id="2a158-141">The approximate percentage of the operation that has been completed (and therefore the percentage remaining).</span></span>
-   <span data-ttu-id="2a158-142">如果不值得繼續等候，則應取消作業。</span><span class="sxs-lookup"><span data-stu-id="2a158-142">If they should cancel the operation if it isn't worth continuing to wait.</span></span>
-   <span data-ttu-id="2a158-143">當作業完成時，應該繼續等候或執行其他作業。</span><span class="sxs-lookup"><span data-stu-id="2a158-143">If they should continue to wait or do something else while the operation completes.</span></span>

<span data-ttu-id="2a158-144">**針對需要限制時間的作業使用確定進度列，** 即使該時間量無法準確預測也一樣。</span><span class="sxs-lookup"><span data-stu-id="2a158-144">**Use determinate progress bars for operations that require a bounded amount of time,** even if that amount of time cannot be accurately predicted.</span></span> <span data-ttu-id="2a158-145">不定的進度列會顯示正在進行的進度，但不提供任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2a158-145">Indeterminate progress bars show that progress is being made, but provide no other information.</span></span> <span data-ttu-id="2a158-146">請勿只根據可能缺少的精確度來選擇不定的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-146">Don't choose an indeterminate progress bar based only on the possible lack of accuracy alone.</span></span>

<span data-ttu-id="2a158-147">例如，假設某項作業需要五個步驟，且每個步驟都需要限定的時間量，但每個步驟的時間量可能會有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="2a158-147">For example, suppose an operation requires five steps and each of those steps requires a bounded amount of time, but the amount of time for each step can vary greatly.</span></span> <span data-ttu-id="2a158-148">在此情況下，請使用確定進度列，並在每個步驟完成時顯示進度，並與每個步驟通常花費的時間量成正比。</span><span class="sxs-lookup"><span data-stu-id="2a158-148">In this case, use a determinate progress bar and show progress when each step completes proportional to the amount of time each step usually takes.</span></span> <span data-ttu-id="2a158-149">只有在確定進度列會導致使用者不正確地結束作業已被鎖定時，才使用不定的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-149">Use an indeterminate progress bar only if a determinate progress bar would cause users to conclude incorrectly that the operation has locked up.</span></span>

<span data-ttu-id="2a158-150">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="2a158-150">**If you do only one thing...**</span></span>

<span data-ttu-id="2a158-151">請確定您提供冗長作業的進度意見反應，並清楚傳達上述資訊。</span><span class="sxs-lookup"><span data-stu-id="2a158-151">Make sure that you provide progress feedback for lengthy operations and that the above information is clearly communicated.</span></span> <span data-ttu-id="2a158-152">盡可能使用確定進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-152">Use determinate progress bars whenever possible.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="2a158-153">使用模式</span><span class="sxs-lookup"><span data-stu-id="2a158-153">Usage patterns</span></span>

<span data-ttu-id="2a158-154">進度列有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="2a158-154">Progress bars have several usage patterns:</span></span>

### <a name="determinate-progress-bars"></a><span data-ttu-id="2a158-155">確定進度列</span><span class="sxs-lookup"><span data-stu-id="2a158-155">Determinate progress bars</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a158-156"><strong>強制回應確定進度列</strong></span><span class="sxs-lookup"><span data-stu-id="2a158-156"><strong>Modal determinate progress bars</strong></span></span><br/> <span data-ttu-id="2a158-157">藉由從左至右填滿來指出作業的進度，並在作業完成時完整填滿。</span><span class="sxs-lookup"><span data-stu-id="2a158-157">Indicate an operation's progress by filling from left to right and filling completely when the operation is complete.</span></span> <br/></td>
<td><span data-ttu-id="2a158-158">因為這是強制 <a href="glossary.md">回應的意見</a>反應，所以使用者無法在視窗 (或其父代中執行其他工作（如果在模式) 對話方塊中顯示），直到作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="2a158-158">Because this feedback is <a href="glossary.md">modal</a>, users cannot perform other tasks in the window (or its parent if displayed in a modal dialog box) until the operation is complete.</span></span> <br/> <img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br/> <span data-ttu-id="2a158-159">在此範例中，進度列會在設定期間提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="2a158-159">In this example, the progress bar gives feedback during configuration.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a158-160"><strong>具有 [取消] 或 [停止] 按鈕的強制回應確定進度列</strong></span><span class="sxs-lookup"><span data-stu-id="2a158-160"><strong>Modal determinate progress bars with a Cancel or Stop button</strong></span></span><br/> <span data-ttu-id="2a158-161">允許使用者停止作業，可能是因為作業花費的時間太長，或不值得等候。</span><span class="sxs-lookup"><span data-stu-id="2a158-161">Allow users to halt the operation, perhaps because the operation is taking too long or isn't worth the wait.</span></span><br/></td>
<td><img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br/> <span data-ttu-id="2a158-162">在此範例中，使用者可以按一下 [停止] 以停止作業，並讓環境維持目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a158-162">In this example, users can click Stop to halt the operation and leave the environment in its current state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a158-163"><strong>具有 [取消] 或 [停止] 按鈕和動畫的強制回應確定進度列</strong></span><span class="sxs-lookup"><span data-stu-id="2a158-163"><strong>Modal determinate progress bars with a Cancel or Stop button and animation</strong></span></span><br/> <span data-ttu-id="2a158-164">允許使用者停止作業，並包含可協助使用者視覺化作業效果的動畫。</span><span class="sxs-lookup"><span data-stu-id="2a158-164">Allow users to halt the operation, and include an animation to help users visualize the effect of an operation.</span></span><br/></td>
<td><img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br/> <span data-ttu-id="2a158-165">在此範例中，使用者可以按一下 [停止] 以停止作業，並讓環境維持目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a158-165">In this example, users can click Stop to halt the operation and leave the environment in its current state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a158-166"><strong>強制回應確定雙重進度列</strong></span><span class="sxs-lookup"><span data-stu-id="2a158-166"><strong>Modal determinate double progress bars</strong></span></span><br/> <span data-ttu-id="2a158-167">藉由在第一個進度列中顯示目前步驟的進度，以及第二列的整體進度，來指出多步驟作業的進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-167">Indicate the progress of a multi-step operation by showing the progress of the current step in the first progress bar, and the overall progress in the second bar.</span></span><br/></td>
<td><span data-ttu-id="2a158-168">因為第一個進度列提供一些額外的資訊，而且可能很大的混淆，所以不建議使用此模式。</span><span class="sxs-lookup"><span data-stu-id="2a158-168">Because the first progress bar provides little additional information and can be quite distracting, this pattern is not recommended.</span></span> <span data-ttu-id="2a158-169">相反地，請讓作業中的所有步驟共用進度的一部分，並讓單一進度列移至完成一次。</span><span class="sxs-lookup"><span data-stu-id="2a158-169">Instead, have all the steps in the operation share a portion of the progress and have a single progress bar go to completion once.</span></span> <br/> <img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br/> <span data-ttu-id="2a158-170">在此範例中，第一個進度列會顯示目前步驟的進度，而第二個進度列會顯示整體進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-170">In this example, the first progress bar shows the progress of the current step and the second progress bar shows the overall progress.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2a158-171">這種模式通常是不必要的，因此應予以避免。</span><span class="sxs-lookup"><span data-stu-id="2a158-171">This pattern is usually unnecessary and should be avoided.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a158-172"><strong>無模式確定進度列</strong></span><span class="sxs-lookup"><span data-stu-id="2a158-172"><strong>Modeless determinate progress bars</strong></span></span><br/> <span data-ttu-id="2a158-173">藉由從左至右填滿來指出作業的進度，並在作業完成時完整填滿。</span><span class="sxs-lookup"><span data-stu-id="2a158-173">Indicate an operation's progress by filling from left to right and filling completely when the operation is complete.</span></span><br/></td>
<td><span data-ttu-id="2a158-174">不同于模式進度列，使用者可以在作業進行時執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="2a158-174">Unlike with modal progress bars, users can perform other tasks while the operation is in progress.</span></span> <span data-ttu-id="2a158-175">這些進度列可以顯示在內容中，也可以顯示在狀態列上。</span><span class="sxs-lookup"><span data-stu-id="2a158-175">These progress bars can be displayed in context or on a status bar.</span></span> <br/> <img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br/> <span data-ttu-id="2a158-176">在此範例中，Windows Internet ExplorerWindows Internet Explorer 會顯示其在狀態列上載入網頁的進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-176">In this example, Windows Internet ExplorerWindows Internet Explorer displays its progress for loading a Web page on the status bar.</span></span> <span data-ttu-id="2a158-177">使用者可以在頁面載入時執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="2a158-177">Users can perform other tasks while the page is loading.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="indeterminate-progress-bars"></a><span data-ttu-id="2a158-178">不定的進度列</span><span class="sxs-lookup"><span data-stu-id="2a158-178">Indeterminate progress bars</span></span>



|                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a158-179">**強制不定的進度列**</span><span class="sxs-lookup"><span data-stu-id="2a158-179">**Modal indeterminate progress bars**</span></span><br/> <span data-ttu-id="2a158-180">藉由顯示從左至右連續迴圈的動畫，表示作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="2a158-180">indicate an operation is in progress by showing an animation that continuously cycles across the bar from left to right.</span></span> <br/>   | <span data-ttu-id="2a158-181">僅供無法判斷整體進度的作業使用，因此沒有完整性的概念。</span><span class="sxs-lookup"><span data-stu-id="2a158-181">Used only for operations whose overall progress cannot be determined, so there is no notion of completeness.</span></span> <span data-ttu-id="2a158-182">確定進度列較適合，因為它們表示已完成之作業的大約百分比，並且可協助使用者判斷作業是否值得繼續等候。</span><span class="sxs-lookup"><span data-stu-id="2a158-182">determinate progress bars are preferable because they indicate the approximate percentage of the operation that has been completed, and help users determine if the operation is worth continuing to wait.</span></span> <span data-ttu-id="2a158-183">它們的視覺效果也比較少。</span><span class="sxs-lookup"><span data-stu-id="2a158-183">they are also less visually distracting.</span></span> <br/> ![模式、不定進度列的螢幕擷取畫面](images/progress-bars-image8.png)<br/> <span data-ttu-id="2a158-185">在此範例中，Windows Update 會使用強制回應不定進度列來指出進度，同時尋找更新。</span><span class="sxs-lookup"><span data-stu-id="2a158-185">In this example, Windows Update uses a modal indeterminate progress bar to indicate progress while it looks for updates.</span></span><br/> |
| <span data-ttu-id="2a158-186">**無狀態不定進度列**</span><span class="sxs-lookup"><span data-stu-id="2a158-186">**Modeless indeterminate progress bars**</span></span><br/> <span data-ttu-id="2a158-187">藉由顯示從左至右連續迴圈的動畫，表示作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="2a158-187">indicate an operation is in progress by showing an animation that continuously cycles across the bar from left to right.</span></span><br/> | <span data-ttu-id="2a158-188">不同于強制回應的進度列，使用者可以在進行處理時執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="2a158-188">Unlike modal progress bars, users can perform other tasks while the processing is in progress.</span></span> <span data-ttu-id="2a158-189">這些進度列可以顯示在內容中，也可以顯示在狀態列上。</span><span class="sxs-lookup"><span data-stu-id="2a158-189">these progress bars can be displayed in context or on a status bar.</span></span> <br/> ![<span data-ttu-id="2a158-190">outlook 視窗中精簡進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-190">screen shot of thin progress bar in outlook window</span></span> ](images/progress-bars-image9.png)<br/> <span data-ttu-id="2a158-191">在此範例中，Microsoft Outlook 在填寫連絡人屬性時，會使用非強制回應的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-191">In this example, Microsoft Outlook uses a modeless indeterminate progress bar while filling in contact properties.</span></span> <span data-ttu-id="2a158-192">當此工作正在進行時，使用者可以繼續使用屬性視窗。</span><span class="sxs-lookup"><span data-stu-id="2a158-192">Users can continue to use the property window while this work is in progress.</span></span><br/>                                                                                                                    |



 

### <a name="meters"></a><span data-ttu-id="2a158-193">米</span><span class="sxs-lookup"><span data-stu-id="2a158-193">Meters</span></span>



|                                                                                          |                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a158-194">**米**</span><span class="sxs-lookup"><span data-stu-id="2a158-194">**Meters**</span></span><br/> <span data-ttu-id="2a158-195">指出與進度無關的百分比。</span><span class="sxs-lookup"><span data-stu-id="2a158-195">indicate a percentage that is not related to progress.</span></span> <br/> | <span data-ttu-id="2a158-196">這種模式不是進度列，但會使用進度列控制項來執行。</span><span class="sxs-lookup"><span data-stu-id="2a158-196">This pattern isn't a progress bar, but it is implemented using the progress bar control.</span></span> <span data-ttu-id="2a158-197">計量表具有不同的外觀，可區別它們與真正的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-197">meters have a distinct look to differentiate them from true progress bars.</span></span> <br/> ![<span data-ttu-id="2a158-198">顯示可用磁碟空間的計量螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-198">screen shot of meter showing free disk space</span></span> ](images/progress-bars-image10.png)<br/> <span data-ttu-id="2a158-199">在此範例中，計量會顯示所使用的磁片磁碟機空間百分比。</span><span class="sxs-lookup"><span data-stu-id="2a158-199">In this example, the meter shows the percentage of disk drive space used.</span></span><br/> |



 

## <a name="guidelines"></a><span data-ttu-id="2a158-200">指導方針</span><span class="sxs-lookup"><span data-stu-id="2a158-200">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="2a158-201">一般</span><span class="sxs-lookup"><span data-stu-id="2a158-201">General</span></span>

-   <span data-ttu-id="2a158-202">**在執行冗長的作業時提供進度回饋。**</span><span class="sxs-lookup"><span data-stu-id="2a158-202">**Provide progress feedback when performing a lengthy operation.**</span></span> <span data-ttu-id="2a158-203">使用者永遠不需要猜測進度是否正在進行。</span><span class="sxs-lookup"><span data-stu-id="2a158-203">Users should never have to guess if progress is being made.</span></span>
-   <span data-ttu-id="2a158-204">**明確指出真正的進度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-204">**Clearly indicate real progress.**</span></span> <span data-ttu-id="2a158-205">進度列必須在進行進度時繼續進行。</span><span class="sxs-lookup"><span data-stu-id="2a158-205">The progress bar must advance if progress is being made.</span></span> <span data-ttu-id="2a158-206">如果預期的完成時間範圍很大，請考慮使用非線性尺規來指出較長時間的進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-206">If the range of expected completion times is large, consider using a non-linear scale to indicate progress for the longer times.</span></span> <span data-ttu-id="2a158-207">您不想讓使用者在程式未完成時，結束程式的鎖定。</span><span class="sxs-lookup"><span data-stu-id="2a158-207">You don't want users to conclude that your program has locked up when it hasn't.</span></span>
-   <span data-ttu-id="2a158-208">**明確指出沒有進度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-208">**Clearly indicate lack of progress.**</span></span> <span data-ttu-id="2a158-209">如果未進行任何進度，就不能事先前進進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-209">The progress bar must not advance if no progress is being made.</span></span> <span data-ttu-id="2a158-210">您不想讓使用者無限期地等候永遠不會完成的作業。</span><span class="sxs-lookup"><span data-stu-id="2a158-210">You don't want users to wait indefinitely for an operation that is never going to complete.</span></span>
-   <span data-ttu-id="2a158-211">**提供有用的進度詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="2a158-211">**Provide useful progress details.**</span></span> <span data-ttu-id="2a158-212">提供其他的進度資訊，但僅限使用者可以使用它來執行某些動作。</span><span class="sxs-lookup"><span data-stu-id="2a158-212">Provide additional progress information, but only if users can do something with it.</span></span> <span data-ttu-id="2a158-213">請確定文字顯示的時間夠長，讓使用者能夠讀取該文字。</span><span class="sxs-lookup"><span data-stu-id="2a158-213">Make sure the text is displayed long enough for users to be able to read it.</span></span>

    ![<span data-ttu-id="2a158-214">顯示傳輸速率的進度列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-214">screen shot of progress bar showing transfer rate</span></span> ](images/progress-bars-image11.png)

    <span data-ttu-id="2a158-215">在此範例中，使用者可以查看傳送速率。</span><span class="sxs-lookup"><span data-stu-id="2a158-215">In this example, users can see the transfer rate.</span></span> <span data-ttu-id="2a158-216">這裡的低傳輸速率建議您需要使用高頻寬的網路連接。</span><span class="sxs-lookup"><span data-stu-id="2a158-216">The low transfer rate here suggests the need for using a high-bandwidth network connection.</span></span>

-   <span data-ttu-id="2a158-217">**請勿提供不必要的詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="2a158-217">**Don't provide unnecessary details.**</span></span> <span data-ttu-id="2a158-218">通常使用者並不在意正在執行之作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2a158-218">Generally users don't care about the details of the operation being performed.</span></span> <span data-ttu-id="2a158-219">例如，安裝程式的使用者不在意要複製的特定檔案，或系統元件因為沒有這些詳細資料的預期而註冊。</span><span class="sxs-lookup"><span data-stu-id="2a158-219">For example, users of a setup program don't care about the specific file being copied or that system components are being registered because they have no expectations about these details.</span></span> <span data-ttu-id="2a158-220">通常，標示正確的進度列會提供足夠的資訊，因此，只有在使用者可以利用它來執行某些動作時，才提供其他的進度資訊。</span><span class="sxs-lookup"><span data-stu-id="2a158-220">Typically, a well-labeled progress bar alone provides sufficient information, so provide additional progress information only if users can do something with it.</span></span> <span data-ttu-id="2a158-221">提供使用者不在意的詳細資料，讓使用者體驗變得過於複雜和技術性。</span><span class="sxs-lookup"><span data-stu-id="2a158-221">Providing details that users don't care about makes the user experience overly complicated and technical.</span></span> <span data-ttu-id="2a158-222">如果您需要更詳細的偵錯工具資訊，請勿將它顯示在發行組建中。</span><span class="sxs-lookup"><span data-stu-id="2a158-222">If you need more detailed information for debugging, don't display it in release builds.</span></span>

    <span data-ttu-id="2a158-223">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-223">**Correct:**</span></span>

    ![<span data-ttu-id="2a158-224">安裝進度的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-224">screen shot of installation progress</span></span> ](images/progress-bars-image12.png)

    <span data-ttu-id="2a158-225">在此範例中，只需要標記的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-225">In this example, the labeled progress bar is all that is needed.</span></span>

    <span data-ttu-id="2a158-226">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-226">**Correct:**</span></span>

    ![<span data-ttu-id="2a158-227">顯示傳輸速率的進度列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-227">screen shot of progress bar showing transfer rate</span></span> ](images/progress-bars-image11.png)

    <span data-ttu-id="2a158-228">在此範例中，Windows 檔案總管正在複製使用者選取的檔案，因此顯示覆制的檔案名有意義。</span><span class="sxs-lookup"><span data-stu-id="2a158-228">In this example, Windows Explorer is copying files the user selected, so displaying the filenames being copied is meaningful.</span></span>

    <span data-ttu-id="2a158-229">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-229">**Incorrect:**</span></span>

    ![<span data-ttu-id="2a158-230">註冊進度的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-230">screen shot of progress of registration</span></span> ](images/progress-bars-image13.png)

    <span data-ttu-id="2a158-231">在此範例中，安裝程式會提供對使用者沒有意義的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2a158-231">In this example, a setup program is providing details that are meaningless to the user.</span></span>

-   <span data-ttu-id="2a158-232">**提供有用的動畫。**</span><span class="sxs-lookup"><span data-stu-id="2a158-232">**Provide useful animations.**</span></span> <span data-ttu-id="2a158-233">如果順利完成，動畫可以協助使用者將作業視覺化，以改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="2a158-233">If done well, animations improve the user experience by helping users visualize the operation.</span></span> <span data-ttu-id="2a158-234">良好的動畫會對單獨的文字產生更大的影響。</span><span class="sxs-lookup"><span data-stu-id="2a158-234">Good animations have more impact than text alone.</span></span> <span data-ttu-id="2a158-235">例如，如果可以復原檔案，Outlook Delete 命令的進度列會顯示目的地的資源回收筒，但如果無法復原檔案，則不會資源回收筒。</span><span class="sxs-lookup"><span data-stu-id="2a158-235">For example, the progress bar for the Outlook Delete command displays the Recycle Bin for the destination if the files can be recovered, but no Recycle Bin if the files can't be recovered.</span></span>

    ![<span data-ttu-id="2a158-236">刪除進度的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-236">screen shot of progress of deletion</span></span> ](images/progress-bars-image14.png)

    <span data-ttu-id="2a158-237">在此範例中，缺少資源回收筒會強化檔案的永久刪除。</span><span class="sxs-lookup"><span data-stu-id="2a158-237">In this example, the lack of a Recycle Bin reinforces that the files are being permanently deleted.</span></span> <span data-ttu-id="2a158-238">這種額外資訊不會以單獨使用的文字來傳達。</span><span class="sxs-lookup"><span data-stu-id="2a158-238">This additional information wouldn't be communicated as effectively using text alone.</span></span>

-   <span data-ttu-id="2a158-239">**請勿使用不必要的動畫。**</span><span class="sxs-lookup"><span data-stu-id="2a158-239">**Don't use unnecessary animations.**</span></span> <span data-ttu-id="2a158-240">動畫可能會產生誤導，因為它們通常會在與實際工作不同的執行緒中執行，因此即使作業已鎖定，也可以建議進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-240">Animations can be misleading because they usually run in a separate thread from the actual task and therefore can suggest progress even if the operation has locked up.</span></span> <span data-ttu-id="2a158-241">此外，如果作業的速度低於預期，使用者有時會假設動畫是原因的一部分。</span><span class="sxs-lookup"><span data-stu-id="2a158-241">Also, if the operation is slower than expected, users sometimes assume that the animation is part of the reason.</span></span> <span data-ttu-id="2a158-242">因此，只有在有清楚的理由時，才使用動畫;請勿使用它們來嘗試榮幸使用者。</span><span class="sxs-lookup"><span data-stu-id="2a158-242">Consequently, only use animations when there is a clear justification; don't use them to try to entertain users.</span></span>
-   <span data-ttu-id="2a158-243">**將動畫置於進度列的中央。**</span><span class="sxs-lookup"><span data-stu-id="2a158-243">**Position animations centered over the progress bar.**</span></span> <span data-ttu-id="2a158-244">將動畫放在進度列標籤上方（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2a158-244">Put the animation above the progress bar labels, if you have any.</span></span> <span data-ttu-id="2a158-245">如果進度列右邊有 [取消] 或 [停止] 按鈕，請在決定中心時包含按鈕。</span><span class="sxs-lookup"><span data-stu-id="2a158-245">If there is a Cancel or Stop button to the right of the progress bar, include the button when determining the center.</span></span>
-   <span data-ttu-id="2a158-246">**只有當作業的長度很長時，才會在作業完成時播放音效效果 (超過兩分鐘) 、不頻繁且重要。**</span><span class="sxs-lookup"><span data-stu-id="2a158-246">**Play a sound effect at the completion of an operation only if it is very lengthy (longer than two minutes), infrequent, and important.**</span></span> <span data-ttu-id="2a158-247">如果使用者可能會在處理過程中離開重要的作業，則音效效果會還原使用者的注意力。</span><span class="sxs-lookup"><span data-stu-id="2a158-247">If the user is likely to walk away from an important operation while it is processing, a sound effect restores the user's attention.</span></span> <span data-ttu-id="2a158-248">在其他情況下，在完成時使用音效效果可能會造成干擾。</span><span class="sxs-lookup"><span data-stu-id="2a158-248">Using a sound effect upon completion in other circumstances would be a distracting annoyance.</span></span>
-   <span data-ttu-id="2a158-249">**請勿竊取輸入焦點來顯示進度更新或完成。**</span><span class="sxs-lookup"><span data-stu-id="2a158-249">**Don't steal input focus to show a progress update or completion.**</span></span> <span data-ttu-id="2a158-250">使用者通常會在等候但不想中斷時切換至其他程式。</span><span class="sxs-lookup"><span data-stu-id="2a158-250">Users often switch to other programs while waiting and don't want to be interrupted.</span></span> <span data-ttu-id="2a158-251">背景工作必須停留在背景中。</span><span class="sxs-lookup"><span data-stu-id="2a158-251">Background tasks must stay in the background.</span></span>
-   <span data-ttu-id="2a158-252">**別擔心技術支援。**</span><span class="sxs-lookup"><span data-stu-id="2a158-252">**Don't worry about technical support.**</span></span> <span data-ttu-id="2a158-253">由於進度列所提供的意見不一定是正確的，而且是 fleeting 的，所以進度列不是提供技術支援資訊的絕佳機制。</span><span class="sxs-lookup"><span data-stu-id="2a158-253">Because the feedback provided by progress bars isn't necessarily accurate and is fleeting, progress bars aren't a good mechanism for providing information for technical support.</span></span> <span data-ttu-id="2a158-254">因此，如果作業可能會因為安裝程式) 而失敗 (，請不要提供僅適用于技術支援的額外進度資訊。</span><span class="sxs-lookup"><span data-stu-id="2a158-254">Consequently, if the operation can fail (as with a setup program), don't provide additional progress information that is only useful to technical support.</span></span> <span data-ttu-id="2a158-255">相反地，請提供替代機制（例如記錄檔）來記錄技術支援資訊。</span><span class="sxs-lookup"><span data-stu-id="2a158-255">Instead, provide an alternative mechanism such as a log file to record technical support information.</span></span>

    <span data-ttu-id="2a158-256">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-256">**Incorrect:**</span></span>

    ![<span data-ttu-id="2a158-257">進度列的螢幕擷取畫面，顯示伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="2a158-257">screen shot of progress bar showing server name</span></span> ](images/progress-bars-image15.png)

    <span data-ttu-id="2a158-258">在此範例中，進度列會顯示適用于技術支援的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2a158-258">In this example, the progress bar is showing details intended for technical support.</span></span>

-   <span data-ttu-id="2a158-259">**請勿將完成百分比或任何其他文字放在進度列上。**</span><span class="sxs-lookup"><span data-stu-id="2a158-259">**Don't put the percentage complete or any other text on a progress bar.**</span></span> <span data-ttu-id="2a158-260">這類文字無法存取，而且與使用主題不相容。</span><span class="sxs-lookup"><span data-stu-id="2a158-260">Such text isn't accessible and isn't compatible with using themes.</span></span>

    <span data-ttu-id="2a158-261">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-261">**Incorrect:**</span></span>

    ![<span data-ttu-id="2a158-262">橫條圖上含有文字的進度列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-262">screen shot of progress bar with text on the bar</span></span> ](images/progress-bars-image16.png)

    <span data-ttu-id="2a158-263">在此範例中，無法存取進度列上的百分比文字。</span><span class="sxs-lookup"><span data-stu-id="2a158-263">In this example, the percentage text on the progress bar isn't accessible.</span></span>

-   <span data-ttu-id="2a158-264">**請勿將進度列與忙碌指標合併。**</span><span class="sxs-lookup"><span data-stu-id="2a158-264">**Don't combine a progress bar with a busy pointer.**</span></span> <span data-ttu-id="2a158-265">請使用其中一種，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="2a158-265">Use one or the other, but not both at the same time.</span></span>
-   <span data-ttu-id="2a158-266">**請勿使用垂直進度列。**</span><span class="sxs-lookup"><span data-stu-id="2a158-266">**Don't use vertical progress bars.**</span></span> <span data-ttu-id="2a158-267">水準進度列具有更自然的對應和更好的流程。</span><span class="sxs-lookup"><span data-stu-id="2a158-267">Horizontal progress bars have a more natural mapping and better flow.</span></span>

### <a name="determinate-progress-bars"></a><span data-ttu-id="2a158-268">確定進度列</span><span class="sxs-lookup"><span data-stu-id="2a158-268">Determinate progress bars</span></span>

-   <span data-ttu-id="2a158-269">**針對需要限制時間的作業使用確定進度列，** 即使該時間量無法準確預測也一樣。</span><span class="sxs-lookup"><span data-stu-id="2a158-269">**Use determinate progress bars for operations that require a bounded amount of time,** even if that amount of time cannot be accurately predicted.</span></span> <span data-ttu-id="2a158-270">不定的進度列會顯示正在進行的進度，但不提供任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2a158-270">Indeterminate progress bars show that progress is being made, but provide no other information.</span></span> <span data-ttu-id="2a158-271">請勿只根據可能缺少的精確度來選擇不定的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-271">Don't choose an indeterminate progress bar based only on the possible lack of accuracy alone.</span></span>
-   <span data-ttu-id="2a158-272">**明確指出進度階段。**</span><span class="sxs-lookup"><span data-stu-id="2a158-272">**Clearly indicate the progress phase.**</span></span> <span data-ttu-id="2a158-273">進度列必須能夠指出作業是在作業的開頭、中間或結尾。</span><span class="sxs-lookup"><span data-stu-id="2a158-273">The progress bar must be able to indicate if the operation is in the beginning, middle, or end of an operation.</span></span> <span data-ttu-id="2a158-274">例如，進度列會立即獲得99% 的完成，然後長時間保持在最大的 uninformative 和討厭。</span><span class="sxs-lookup"><span data-stu-id="2a158-274">For example, progress bars that immediately shoot to 99 percent completion, then stay there for a long time are particularly uninformative and annoying.</span></span> <span data-ttu-id="2a158-275">在這些情況下，進度列應一開始設定為最高33%，表示作業仍在開始階段。</span><span class="sxs-lookup"><span data-stu-id="2a158-275">In these cases, the progress bar should be set initially to at most 33 percent to indicate that the operation is still in the beginning phase.</span></span>
-   <span data-ttu-id="2a158-276">**明確指出完成。**</span><span class="sxs-lookup"><span data-stu-id="2a158-276">**Clearly indicate completion.**</span></span> <span data-ttu-id="2a158-277">除非作業已完成，否則不要讓進度列移至100%。</span><span class="sxs-lookup"><span data-stu-id="2a158-277">Don't let a progress bar go to 100 percent unless the operation has completed.</span></span>
-   <span data-ttu-id="2a158-278">**如果您可以正確地完成，請提供剩餘的預估時間。**</span><span class="sxs-lookup"><span data-stu-id="2a158-278">**Provide a time remaining estimate if you can do so accurately.**</span></span> <span data-ttu-id="2a158-279">精確度較高的估計值會很有用，但從標示或跳動開始的估計值卻很有用。</span><span class="sxs-lookup"><span data-stu-id="2a158-279">Time remaining estimates that are accurate are useful, but estimates that are way off the mark or bounce around significantly aren't helpful.</span></span> <span data-ttu-id="2a158-280">您可能需要先執行一些處理，才能提供精確的估計值。</span><span class="sxs-lookup"><span data-stu-id="2a158-280">You may need to perform some processing before you can give accurate estimates.</span></span> <span data-ttu-id="2a158-281">如果是這種情況，請不要在此初始期間顯示可能不准確的估計值。</span><span class="sxs-lookup"><span data-stu-id="2a158-281">If so, don't display potentially inaccurate estimates during this initial period.</span></span>
-   <span data-ttu-id="2a158-282">**請勿重新開機進度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-282">**Don't restart progress.**</span></span> <span data-ttu-id="2a158-283">如果進度列在重新開機時遺失其值 (可能是因為作業中的步驟完成) ，因為使用者無法得知作業何時會完成。</span><span class="sxs-lookup"><span data-stu-id="2a158-283">A progress bar loses its value if it restarts (perhaps because a step in the operation completes) because users have no way of knowing when the operation will complete.</span></span> <span data-ttu-id="2a158-284">相反地，請讓作業中的所有步驟共用進度的一部分，並讓進度列移至完成一次。</span><span class="sxs-lookup"><span data-stu-id="2a158-284">Instead, have all the steps in the operation share a portion of the progress and have the progress bar go to completion once.</span></span>

    <span data-ttu-id="2a158-285">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-285">**Incorrect:**</span></span>

    ![<span data-ttu-id="2a158-286">已重新開機之進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-286">screen shot of progress bar that restarted</span></span> ](images/progress-bars-image17.png)

    <span data-ttu-id="2a158-287">在此範例中，作業會移至複製檔案的步驟，並重設該步驟的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-287">In this example, the operation moved to the step of copying files and reset the progress bar for that step.</span></span> <span data-ttu-id="2a158-288">現在使用者已不知道有多少進度，或剩下多少時間。</span><span class="sxs-lookup"><span data-stu-id="2a158-288">Now users have no idea how much progress has been made or how much time is left.</span></span>

-   <span data-ttu-id="2a158-289">**不要備份進度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-289">**Don't back up progress.**</span></span> <span data-ttu-id="2a158-290">在重新開機時，如果進度列備份，進度列就會失去其值。</span><span class="sxs-lookup"><span data-stu-id="2a158-290">As with a restart, a progress bar loses its value if it backs up.</span></span> <span data-ttu-id="2a158-291">一律以單純的進度增加進度。</span><span class="sxs-lookup"><span data-stu-id="2a158-291">Always increase progress monotonically.</span></span> <span data-ttu-id="2a158-292">不過，您可以有剩餘的估計值來增加 (以及減少) ，因為進度的比率可能不同。</span><span class="sxs-lookup"><span data-stu-id="2a158-292">However, you can have a time remaining estimate that increases (as well as decreases) because the rate of progress may vary.</span></span>

### <a name="indeterminate-progress-bars"></a><span data-ttu-id="2a158-293">不定的進度列</span><span class="sxs-lookup"><span data-stu-id="2a158-293">Indeterminate progress bars</span></span>

-   <span data-ttu-id="2a158-294">**請僅針對無法判斷其整體進度的作業使用不定進度列。**</span><span class="sxs-lookup"><span data-stu-id="2a158-294">**Use indeterminate progress bars only for operations whose overall progress cannot be determined.**</span></span> <span data-ttu-id="2a158-295">針對需要無限制時間或存取未知物件數目的作業，請使用不定的進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-295">Use indeterminate progress bars for operations that require an unbounded amount of time or that access an unknown number of objects.</span></span> <span data-ttu-id="2a158-296">使用超時來提供以時間為基礎之作業的界限。</span><span class="sxs-lookup"><span data-stu-id="2a158-296">Use timeouts to give bounds to time-based operations.</span></span>
-   <span data-ttu-id="2a158-297">**一旦可以決定整體進度，請轉換成確定進度列。**</span><span class="sxs-lookup"><span data-stu-id="2a158-297">**Convert to a determinate progress bar once the overall progress can be determined.**</span></span> <span data-ttu-id="2a158-298">例如，如果花了很長的時間來判斷物件的數目，您可以在計算物件時使用不定的進度列，然後轉換成確定進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-298">For example, if it takes significantly longer than two seconds to determine the number of objects, you can use an indeterminate progress bar while the objects are counted, and then convert to a determinate progress bar.</span></span>
-   <span data-ttu-id="2a158-299">**請勿將不定的進度列合併為完成或剩餘時間的估計值。**</span><span class="sxs-lookup"><span data-stu-id="2a158-299">**Don't combine indeterminate progress bars with percent complete or time remaining estimates.**</span></span> <span data-ttu-id="2a158-300">如果您可以提供這種資訊，請改用確定進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-300">If you can provide this information, use a determinate progress bar instead.</span></span>
-   <span data-ttu-id="2a158-301">**請勿將不定的進度列與動畫結合在一起。**</span><span class="sxs-lookup"><span data-stu-id="2a158-301">**Don't combine indeterminate progress bars with animations.**</span></span> <span data-ttu-id="2a158-302">不定的進度列實際上是一般動畫，因此您應該使用其中一個，但絕不會使用兩者。</span><span class="sxs-lookup"><span data-stu-id="2a158-302">An indeterminate progress bar is effectively a generic animation, so you should use one or the other but never both.</span></span>

    <span data-ttu-id="2a158-303">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-303">**Correct:**</span></span>

    ![<span data-ttu-id="2a158-304">偵測伺服器中進度的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-304">screen shot of progress in detecting server</span></span> ](images/progress-bars-image18.png)

    <span data-ttu-id="2a158-305">在此範例中，只會使用動畫來顯示作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="2a158-305">In this example, only an animation is used to show that an operation is ongoing.</span></span>

### <a name="modeless-progress-bars"></a><span data-ttu-id="2a158-306">非模式進度列</span><span class="sxs-lookup"><span data-stu-id="2a158-306">Modeless progress bars</span></span>

-   <span data-ttu-id="2a158-307">**如果使用者可以在作業進行時提高生產力，請提供無狀態的意見反應。**</span><span class="sxs-lookup"><span data-stu-id="2a158-307">**If users can do something productive while the operation is in progress, provide modeless feedback.**</span></span> <span data-ttu-id="2a158-308">您可能需要停用需要完成此作業的功能子集。</span><span class="sxs-lookup"><span data-stu-id="2a158-308">You might need to disable a subset of functionality that requires the operation to complete.</span></span>
-   <span data-ttu-id="2a158-309">**如果視窗有網址列，請在網址列中顯示非模式進度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-309">**If the window has an address bar, display the modeless progress in the address bar.**</span></span>

    ![<span data-ttu-id="2a158-310">作為網址列一部分的進度列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-310">screen shot of progress bar as part of address bar</span></span> ](images/progress-bars-image19.png)

    <span data-ttu-id="2a158-311">在此範例中，非模式進度會顯示在網址列中。</span><span class="sxs-lookup"><span data-stu-id="2a158-311">In this example, modeless progress is shown in the address bar.</span></span>

-   <span data-ttu-id="2a158-312">否則， **如果視窗有狀態列，請在狀態列中顯示非模式進度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-312">Otherwise, **if the window has a status bar, display the modeless progress in the status bar.**</span></span> <span data-ttu-id="2a158-313">將任何對應的文字放在狀態列的左邊。</span><span class="sxs-lookup"><span data-stu-id="2a158-313">Put any corresponding text to its left in the status bar.</span></span>

    ![<span data-ttu-id="2a158-314">進度列的螢幕擷取畫面，作為狀態列的一部分</span><span class="sxs-lookup"><span data-stu-id="2a158-314">screen shot of progress bar as part of status bar</span></span> ](images/progress-bars-image7.png)

    <span data-ttu-id="2a158-315">在此範例中，無狀態的進度會顯示在狀態列中。</span><span class="sxs-lookup"><span data-stu-id="2a158-315">In this example, modeless progress is shown in the status bar.</span></span>

### <a name="modal-progress-bars"></a><span data-ttu-id="2a158-316">模式進度列</span><span class="sxs-lookup"><span data-stu-id="2a158-316">Modal progress bars</span></span>

-   <span data-ttu-id="2a158-317">**將強制回應進度列放在進度頁面或**[進度對話方塊](win-dialog-box.md)上。</span><span class="sxs-lookup"><span data-stu-id="2a158-317">**Place modal progress bars on progress pages or** [progress dialog boxes](win-dialog-box.md).</span></span>
-   <span data-ttu-id="2a158-318">**如果需要超過幾秒鐘的時間才能完成作業，或有可能永遠無法完成，請提供命令按鈕來停止作業。**</span><span class="sxs-lookup"><span data-stu-id="2a158-318">**Provide a command button to halt the operation if it takes more than a few seconds to complete, or has the potential never to complete.**</span></span> <span data-ttu-id="2a158-319">如果取消將環境傳回至先前的狀態，請將按鈕標示為 [取消] (不會) 任何副作用，否則請將按鈕標示為停止，表示它會讓部分完成的作業保持不變。</span><span class="sxs-lookup"><span data-stu-id="2a158-319">Label the button Cancel if canceling returns the environment to its previous state (leaving no side effects), otherwise label the button Stop to indicate that it leaves the partially completed operation intact.</span></span> <span data-ttu-id="2a158-320">在某個時間點，您可以將按鈕標籤從 [取消] 變更為 [停止]，如果在某個時間點，則無法將環境回復為先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a158-320">You can change the button label from Cancel to Stop in the middle of the operation if at some point it isn't possible to return the environment to its previous state.</span></span> <span data-ttu-id="2a158-321">以進度列垂直置中命令按鈕，而不是對齊其頂端。</span><span class="sxs-lookup"><span data-stu-id="2a158-321">Center the command button vertically with the progress bar instead of aligning their tops.</span></span>

    <span data-ttu-id="2a158-322">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-322">**Correct:**</span></span>

    ![<span data-ttu-id="2a158-323">等候網路進度的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-323">screen shot of progress of waiting for network</span></span> ](images/progress-bars-image20.png)

    <span data-ttu-id="2a158-324">在此範例中，停止網路連線沒有任何副作用，所以會使用 Cancel。</span><span class="sxs-lookup"><span data-stu-id="2a158-324">In this example, halting the network connection has no side effect so Cancel is used.</span></span>

    <span data-ttu-id="2a158-325">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-325">**Correct:**</span></span>

    ![<span data-ttu-id="2a158-326">進度列的螢幕擷取畫面，顯示剩餘的複製時間</span><span class="sxs-lookup"><span data-stu-id="2a158-326">screen shot of progress bar showing copy time left</span></span> ](images/progress-bars-image21.png)

    <span data-ttu-id="2a158-327">在此範例中，暫停複製會保留任何複製的檔案，因此命令按鈕會標示為 [停止]。</span><span class="sxs-lookup"><span data-stu-id="2a158-327">In this example, halting the copy leaves any copied files, so the command button is labeled Stop.</span></span>

    <span data-ttu-id="2a158-328">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-328">**Incorrect:**</span></span>

    ![<span data-ttu-id="2a158-329">[搜尋進度列] 和 [停止] 按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-329">screen shot of search progress bar and stop button</span></span> ](images/progress-bars-image22.png)

    <span data-ttu-id="2a158-330">在此範例中，暫停搜尋不會有副作用，因此命令按鈕應標示為 [取消]。</span><span class="sxs-lookup"><span data-stu-id="2a158-330">In this example, halting the search leaves no side effect, so the command button should be labeled Cancel.</span></span>

### <a name="time-remaining"></a><span data-ttu-id="2a158-331">剩餘時間</span><span class="sxs-lookup"><span data-stu-id="2a158-331">Time remaining</span></span>

<span data-ttu-id="2a158-332">針對確定進度列：</span><span class="sxs-lookup"><span data-stu-id="2a158-332">For determinate progress bars:</span></span>

-   <span data-ttu-id="2a158-333">**使用下列時間格式。**</span><span class="sxs-lookup"><span data-stu-id="2a158-333">**Use the following time formats.**</span></span> <span data-ttu-id="2a158-334">從最大時間單位不是零的下列其中一種格式開始，然後在最大時間單位變成零之後變更為下一個格式。</span><span class="sxs-lookup"><span data-stu-id="2a158-334">Start with the first of the following formats where the largest time unit isn't zero, and then change to the next format once the largest time unit becomes zero.</span></span>

    <span data-ttu-id="2a158-335">**針對進度列：**</span><span class="sxs-lookup"><span data-stu-id="2a158-335">**For progress bars:**</span></span>

    <span data-ttu-id="2a158-336">**如果相關資訊顯示為冒號格式：**</span><span class="sxs-lookup"><span data-stu-id="2a158-336">**If related information is shown in a colon format:**</span></span>

    <span data-ttu-id="2a158-337">剩餘時間： h 小時、m 分鐘</span><span class="sxs-lookup"><span data-stu-id="2a158-337">Time remaining: h hours, m minutes</span></span>

    <span data-ttu-id="2a158-338">剩餘時間： m 分鐘、秒</span><span class="sxs-lookup"><span data-stu-id="2a158-338">Time remaining: m minutes, s seconds</span></span>

    <span data-ttu-id="2a158-339">剩餘時間：秒</span><span class="sxs-lookup"><span data-stu-id="2a158-339">Time remaining: s seconds</span></span>

    <span data-ttu-id="2a158-340">**如果螢幕空間位於 premium：**</span><span class="sxs-lookup"><span data-stu-id="2a158-340">**If screen space is at a premium:**</span></span>

    <span data-ttu-id="2a158-341">h 小時，剩餘 m 分鐘</span><span class="sxs-lookup"><span data-stu-id="2a158-341">h hrs, m mins remaining</span></span>

    <span data-ttu-id="2a158-342">分鐘，剩餘的秒數</span><span class="sxs-lookup"><span data-stu-id="2a158-342">m mins, s secs remaining</span></span>

    <span data-ttu-id="2a158-343">秒數</span><span class="sxs-lookup"><span data-stu-id="2a158-343">s seconds remaining</span></span>

    <span data-ttu-id="2a158-344">**否則：**</span><span class="sxs-lookup"><span data-stu-id="2a158-344">**Otherwise:**</span></span>

    <span data-ttu-id="2a158-345">小時，剩餘 m 分鐘</span><span class="sxs-lookup"><span data-stu-id="2a158-345">h hours, m minutes remaining</span></span>

    <span data-ttu-id="2a158-346">分鐘，剩餘秒數</span><span class="sxs-lookup"><span data-stu-id="2a158-346">m minutes, s seconds remaining</span></span>

    <span data-ttu-id="2a158-347">秒數</span><span class="sxs-lookup"><span data-stu-id="2a158-347">s seconds remaining</span></span>

    <span data-ttu-id="2a158-348">**針對標題列：**</span><span class="sxs-lookup"><span data-stu-id="2a158-348">**For title bars:**</span></span>

    <span data-ttu-id="2a158-349">hh： mm 剩餘</span><span class="sxs-lookup"><span data-stu-id="2a158-349">hh:mm remaining</span></span>

    <span data-ttu-id="2a158-350">mm：剩餘的 ss</span><span class="sxs-lookup"><span data-stu-id="2a158-350">mm:ss remaining</span></span>

    <span data-ttu-id="2a158-351">0： ss 剩餘</span><span class="sxs-lookup"><span data-stu-id="2a158-351">0:ss remaining</span></span>

    <span data-ttu-id="2a158-352">此壓縮格式會先顯示最重要的資訊，使其不會在工作列上被截斷。</span><span class="sxs-lookup"><span data-stu-id="2a158-352">This compact format shows the most important information first so that it isn't truncated on the taskbar.</span></span>

-   <span data-ttu-id="2a158-353">**讓預估結果正確無誤，但不提供 false 精確度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-353">**Make estimates accurate, but don't give false precision.**</span></span> <span data-ttu-id="2a158-354">如果最大單位為小時，請在有意義的) （而不是秒）時，提供分鐘 (。</span><span class="sxs-lookup"><span data-stu-id="2a158-354">If largest unit is hours, give minutes (if meaningful) but not seconds.</span></span>

    <span data-ttu-id="2a158-355">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-355">**Incorrect:**</span></span>

    <span data-ttu-id="2a158-356">hh 小時、mm 分鐘、ss 秒</span><span class="sxs-lookup"><span data-stu-id="2a158-356">hh hours, mm minutes, ss seconds</span></span>

-   <span data-ttu-id="2a158-357">**將預估保持在最新狀態。**</span><span class="sxs-lookup"><span data-stu-id="2a158-357">**Keep the estimate up-to-date.**</span></span> <span data-ttu-id="2a158-358">更新剩餘時間至少每5秒估計一次。</span><span class="sxs-lookup"><span data-stu-id="2a158-358">Update time remaining estimates at least every 5 seconds.</span></span>
-   <span data-ttu-id="2a158-359">將 **焦點放在剩餘的時間**，因為這是使用者最在意的資訊。</span><span class="sxs-lookup"><span data-stu-id="2a158-359">**Focus on the time remaining** because that is the information users care about most.</span></span> <span data-ttu-id="2a158-360">只有在某些情況下，已耗用時間很有説明 (例如工作可能重複) 時，才提供總經過時間。</span><span class="sxs-lookup"><span data-stu-id="2a158-360">Give total elapsed time only when there are scenarios where elapsed time is helpful (such as when the task is likely to be repeated).</span></span> <span data-ttu-id="2a158-361">如果剩餘的預估時間與進度列相關聯，則沒有百分比的完成文字，因為該資訊是由進度列本身所傳達。</span><span class="sxs-lookup"><span data-stu-id="2a158-361">If the time remaining estimate is associated with a progress bar, don't have percent complete text because that information is conveyed by the progress bar itself.</span></span>
-   <span data-ttu-id="2a158-362">**語法正確。**</span><span class="sxs-lookup"><span data-stu-id="2a158-362">**Be grammatically correct.**</span></span> <span data-ttu-id="2a158-363">當數位為1時，請使用單一單位。</span><span class="sxs-lookup"><span data-stu-id="2a158-363">Use singular units when the number is one.</span></span>

    <span data-ttu-id="2a158-364">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-364">**Incorrect:**</span></span>

    <span data-ttu-id="2a158-365">1分鐘，1秒</span><span class="sxs-lookup"><span data-stu-id="2a158-365">1 minutes, 1 seconds</span></span>

-   <span data-ttu-id="2a158-366">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="2a158-366">**Use sentence-style capitalization.**</span></span>

### <a name="progress-bar-colors"></a><span data-ttu-id="2a158-367">進度列色彩</span><span class="sxs-lookup"><span data-stu-id="2a158-367">Progress bar colors</span></span>

-   <span data-ttu-id="2a158-368">**只使用紅色或黃色的進度列來指出進度狀態，而不是工作的最終結果。**</span><span class="sxs-lookup"><span data-stu-id="2a158-368">**Use red or yellow progress bars only to indicate the progress status, not the final results of a task.**</span></span> <span data-ttu-id="2a158-369">紅色或黃色的進度清單示使用者需要採取一些動作才能完成工作。</span><span class="sxs-lookup"><span data-stu-id="2a158-369">A red or yellow progress bar indicates that users need to take some action to complete the task.</span></span> <span data-ttu-id="2a158-370">如果條件無法復原，請將進度列保持為綠色，並顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2a158-370">If the condition isn't recoverable, leave the progress bar green and display an error message.</span></span>
-   <span data-ttu-id="2a158-371">**當有使用者可復原的狀況，以防止進一步的進度時，請將進度列設為紅色。**</span><span class="sxs-lookup"><span data-stu-id="2a158-371">**Turn the progress bar red when there is a user recoverable condition that prevents making further progress.**</span></span> <span data-ttu-id="2a158-372">顯示訊息來說明問題並建議解決方案。</span><span class="sxs-lookup"><span data-stu-id="2a158-372">Display a message to explain the problem and recommend a solution.</span></span>
-   <span data-ttu-id="2a158-373">將 **進度列設為黃色，表示使用者已暫停工作，或有正在阻礙進度** 但進度 (仍在進行中的狀況，例如，具有網路連線能力不佳) 。</span><span class="sxs-lookup"><span data-stu-id="2a158-373">**Turn the progress bar yellow to indicate either that the user has paused the task or that there is a condition that is impeding progress** but progress is still taking place (as, for example, with poor network connectivity).</span></span> <span data-ttu-id="2a158-374">如果使用者已暫停，請將 [暫停] 按鈕標籤變更為 [繼續]。</span><span class="sxs-lookup"><span data-stu-id="2a158-374">If the user has paused, change the Pause button label to Resume.</span></span> <span data-ttu-id="2a158-375">如果進度是阻礙，則顯示訊息來說明問題並建議解決方案。</span><span class="sxs-lookup"><span data-stu-id="2a158-375">If progress is impeded, display a message to explain the problem and recommend a solution.</span></span>

### <a name="meters"></a><span data-ttu-id="2a158-376">米</span><span class="sxs-lookup"><span data-stu-id="2a158-376">Meters</span></span>

-   <span data-ttu-id="2a158-377">**只使用進度列進行進度。**</span><span class="sxs-lookup"><span data-stu-id="2a158-377">**Use progress bars only for progress.**</span></span> <span data-ttu-id="2a158-378">使用計量來指出與進度無關的百分比。</span><span class="sxs-lookup"><span data-stu-id="2a158-378">Use meters to indicate percentages that aren't related to progress.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="2a158-379">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="2a158-379">Recommended sizing and spacing</span></span>

![<span data-ttu-id="2a158-380">顯示進度列調整大小和間距的圖表</span><span class="sxs-lookup"><span data-stu-id="2a158-380">diagram showing progress-bar sizing and spacing</span></span> ](images/progress-bars-image23.png)

<span data-ttu-id="2a158-381">進度列的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="2a158-381">Recommended sizing and spacing for progress bars.</span></span>

-   <span data-ttu-id="2a158-382">一律使用建議的進度列高度。</span><span class="sxs-lookup"><span data-stu-id="2a158-382">Always use the recommended progress bar height.</span></span>
    -   <span data-ttu-id="2a158-383">**例外狀況：** 如果父視窗不支援建議的高度，您可能會使用不同的高度。</span><span class="sxs-lookup"><span data-stu-id="2a158-383">**Exception:** You may use a different height if the parent window doesn't support the recommended height.</span></span>
-   <span data-ttu-id="2a158-384">如果您想要讓進度列不顯眼，請使用最小寬度。</span><span class="sxs-lookup"><span data-stu-id="2a158-384">Use the minimum width if you want to make the progress bar unobtrusive.</span></span>
-   <span data-ttu-id="2a158-385">請勿使用長度超過建議的最大寬度。</span><span class="sxs-lookup"><span data-stu-id="2a158-385">Don't use widths longer than the maximum recommended.</span></span> <span data-ttu-id="2a158-386">進度列不需要填滿可用的空間。</span><span class="sxs-lookup"><span data-stu-id="2a158-386">The progress bar doesn't have to fill the available space.</span></span>
-   <span data-ttu-id="2a158-387">如果視窗寬度超過建議的最大寬度，則水準置中進度列。</span><span class="sxs-lookup"><span data-stu-id="2a158-387">Center the progress bar horizontally if the window is much wider than the maximum recommended width.</span></span>

## <a name="labels"></a><span data-ttu-id="2a158-388">標籤</span><span class="sxs-lookup"><span data-stu-id="2a158-388">Labels</span></span>

### <a name="progress-bar-labels"></a><span data-ttu-id="2a158-389">進度列標籤</span><span class="sxs-lookup"><span data-stu-id="2a158-389">Progress bar labels</span></span>

-   <span data-ttu-id="2a158-390">**使用具有靜態文字控制項的精簡標籤來指出作業的執行狀況。**</span><span class="sxs-lookup"><span data-stu-id="2a158-390">**Use a concise label with a static text control to indicate what the operation is doing.**</span></span> <span data-ttu-id="2a158-391">使用動詞來開機磁碟區標 (例如，複製) ，並以省略號結尾。</span><span class="sxs-lookup"><span data-stu-id="2a158-391">Start the label with a verb (for example, Copying) and end with an ellipsis.</span></span> <span data-ttu-id="2a158-392">如果作業有多個步驟或正在處理多個物件，此標籤可能會動態變更。</span><span class="sxs-lookup"><span data-stu-id="2a158-392">This label may change dynamically if the operation has multiple steps or is processing multiple objects.</span></span>
-   <span data-ttu-id="2a158-393">請勿指派唯一的 [存取金鑰](glossary.md) ，因為控制項不是互動式的。</span><span class="sxs-lookup"><span data-stu-id="2a158-393">Don't assign a unique [access key](glossary.md) because the control isn't interactive.</span></span>
-   <span data-ttu-id="2a158-394">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="2a158-394">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="2a158-395">如果作業不是由使用者直接起始，您可以包含額外的標籤來提供內容，以及造成中斷的抱歉。</span><span class="sxs-lookup"><span data-stu-id="2a158-395">If the operation was not directly initiated by the user, you can include an additional label to give the context and apologize for the interruption.</span></span> <span data-ttu-id="2a158-396">使用片語啟動此額外標籤，請稍候。</span><span class="sxs-lookup"><span data-stu-id="2a158-396">Start this extra label with the phrase, Please wait while.</span></span> <span data-ttu-id="2a158-397">在作業期間，此標籤不應變更。</span><span class="sxs-lookup"><span data-stu-id="2a158-397">This label should not change during the operation.</span></span>

    ![<span data-ttu-id="2a158-398">具有標籤之進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-398">screen shot of progress bar with label</span></span> ](images/progress-bars-image24.png)

    <span data-ttu-id="2a158-399">在此範例中，系統會要求使用者等候，因為使用者未直接起始作業。</span><span class="sxs-lookup"><span data-stu-id="2a158-399">In this example, the user is being asked to please wait because the user didn't directly initiate the operation.</span></span>

-   <span data-ttu-id="2a158-400">將標籤置於進度列上方，並將標籤與進度列的左邊緣對齊。</span><span class="sxs-lookup"><span data-stu-id="2a158-400">Position the label above the progress bar and align the label with the left edge of the progress bar.</span></span>

### <a name="progress-bar-details"></a><span data-ttu-id="2a158-401">進度列詳細資料</span><span class="sxs-lookup"><span data-stu-id="2a158-401">Progress bar details</span></span>

-   <span data-ttu-id="2a158-402">提供靜態文字中的詳細資料，並在資料前面加上以冒號結尾的標籤。</span><span class="sxs-lookup"><span data-stu-id="2a158-402">Provide details in static text, preceding the data with a label ending with a colon.</span></span> <span data-ttu-id="2a158-403">在詳細資料文字之後) 指定單位 (秒、kb 等等。</span><span class="sxs-lookup"><span data-stu-id="2a158-403">Specify units (seconds, kilobytes, and so on) after the details text.</span></span>

    <span data-ttu-id="2a158-404">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-404">**Correct:**</span></span>

    ![<span data-ttu-id="2a158-405">顯示傳輸速率的進度列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-405">screen shot of progress bar showing transfer rate</span></span> ](images/progress-bars-image11.png)

    <span data-ttu-id="2a158-406">在此範例中，會正確地標示詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2a158-406">In this example, the details are properly labeled.</span></span>

    <span data-ttu-id="2a158-407">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-407">**Incorrect:**</span></span>

    ![<span data-ttu-id="2a158-408">進度列沒有適當標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-408">screen shot of progress bar without proper label</span></span> ](images/progress-bars-image25.png)

    <span data-ttu-id="2a158-409">在此範例中，不會標示詳細資料，因此需要使用者判斷其意義。</span><span class="sxs-lookup"><span data-stu-id="2a158-409">In this example, the details aren't labeled, thus requiring users to determine their meaning.</span></span>

-   <span data-ttu-id="2a158-410">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="2a158-410">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="2a158-411">將詳細資料放在進度列下方，然後將標籤與進度列的左邊緣對齊。</span><span class="sxs-lookup"><span data-stu-id="2a158-411">Position the details below the progress bar and align the label with the left edge of the progress bar.</span></span>
-   <span data-ttu-id="2a158-412">請勿提供完成或剩餘的百分比，因為該資訊是由進度列本身所傳達。</span><span class="sxs-lookup"><span data-stu-id="2a158-412">Don't give the percentage completed or remaining because that information is conveyed by the progress bar itself.</span></span>

### <a name="cancel-button"></a><span data-ttu-id="2a158-413">[取消] 按鈕</span><span class="sxs-lookup"><span data-stu-id="2a158-413">Cancel button</span></span>

-   <span data-ttu-id="2a158-414">如果取消將環境傳回至先前的狀態，請將按鈕標示為 [取消]， (沒有副作用) ;否則，請將按鈕標示為停止，表示它會讓部分完成的作業保持不變。</span><span class="sxs-lookup"><span data-stu-id="2a158-414">Label the button Cancel if canceling returns the environment to its previous state (leaving no side effect); otherwise, label the button Stop to indicate that it leaves the partially completed operation intact.</span></span>
-   <span data-ttu-id="2a158-415">在某個時間點，您可以將按鈕標籤從 [取消] 變更為 [停止]，如果在某個時間點，則無法將環境回復為先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a158-415">You can change the button label from Cancel to Stop in the middle of the operation if at some point it isn't possible to return the environment to its previous state.</span></span>

### <a name="progress-dialog-box-titles"></a><span data-ttu-id="2a158-416">進度對話方塊標題</span><span class="sxs-lookup"><span data-stu-id="2a158-416">Progress dialog box titles</span></span>

-   <span data-ttu-id="2a158-417">如果進度列顯示在強制回應對話方塊中，對話方塊標題應該是程式的名稱或作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a158-417">If the progress bar is displayed in a modal dialog box, the dialog box title should be the name of the program or the name of the operation.</span></span> <span data-ttu-id="2a158-418">請勿使用對話方塊標題的進度列標籤。</span><span class="sxs-lookup"><span data-stu-id="2a158-418">Don't use what should be the progress bar label for the dialog box title.</span></span>

    <span data-ttu-id="2a158-419">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-419">**Correct:**</span></span>

    ![<span data-ttu-id="2a158-420">進度列標題具有工作名稱的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-420">screen shot of progress bar title with task name</span></span> ](images/progress-bars-image26.png)

    <span data-ttu-id="2a158-421">在此範例中，工作名稱是用於對話方塊標題。</span><span class="sxs-lookup"><span data-stu-id="2a158-421">In this example, the task name is used for the dialog box title.</span></span>

    <span data-ttu-id="2a158-422">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2a158-422">**Incorrect:**</span></span>

    ![<span data-ttu-id="2a158-423">重複對話方塊標題的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2a158-423">screen shot of redundant dialog-box title</span></span> ](images/progress-bars-image27.png)

    <span data-ttu-id="2a158-424">在此範例中，對話方塊標題文字是進度列標籤的重述。</span><span class="sxs-lookup"><span data-stu-id="2a158-424">In this example, the dialog box title text is a restatement of the progress bar label.</span></span> <span data-ttu-id="2a158-425">應改為使用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2a158-425">The program name should be used instead.</span></span>

-   <span data-ttu-id="2a158-426">如果進度列顯示在非強制回應對話方塊中，請先藉由精確地放置區分的資訊來優化工作列上顯示的標題。</span><span class="sxs-lookup"><span data-stu-id="2a158-426">If the progress bar is displayed in a modeless dialog box, optimize the title for display on the taskbar by concisely placing the distinguishing information first.</span></span> <span data-ttu-id="2a158-427">範例：「66% 完成」。</span><span class="sxs-lookup"><span data-stu-id="2a158-427">Example: "66% Complete."</span></span>

 

