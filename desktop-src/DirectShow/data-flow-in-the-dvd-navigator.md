---
description: DVD 導覽器中的資料流程
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: DVD 導覽器中的資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a981d2d7b528163abb53478e9e8f2ab88d46c0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688391"
---
# <a name="data-flow-in-the-dvd-navigator"></a><span data-ttu-id="beba8-103">DVD 導覽器中的資料流程</span><span class="sxs-lookup"><span data-stu-id="beba8-103">Data Flow in the DVD Navigator</span></span>

<span data-ttu-id="beba8-104">DVD 導覽器有停止和暫停播放的方法。</span><span class="sxs-lookup"><span data-stu-id="beba8-104">The DVD Navigator has methods to stop and pause playback.</span></span> <span data-ttu-id="beba8-105">這些方法與 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)中的 **Stop** 和 **Pause** 方法類似（但不完全相同）。</span><span class="sxs-lookup"><span data-stu-id="beba8-105">These methods are similar — but not identical — to the **Stop** and **Pause** methods in [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="beba8-106">兩者之間的差異如下：</span><span class="sxs-lookup"><span data-stu-id="beba8-106">Here is the difference between them:</span></span>

-   <span data-ttu-id="beba8-107">**IDvdControl2** 方法會變更 DVD 導覽器從磁片讀取的內容。</span><span class="sxs-lookup"><span data-stu-id="beba8-107">The **IDvdControl2** methods change what the DVD Navigator reads from the disk.</span></span> <span data-ttu-id="beba8-108">它們不會變更圖形的狀態。</span><span class="sxs-lookup"><span data-stu-id="beba8-108">They do not change the state of the graph.</span></span>
-   <span data-ttu-id="beba8-109">**IMediaControl** 方法會變更圖形的狀態。</span><span class="sxs-lookup"><span data-stu-id="beba8-109">The **IMediaControl** methods change the state of the graph.</span></span> <span data-ttu-id="beba8-110">它們不會變更 DVD 導覽器從磁片讀取的內容。</span><span class="sxs-lookup"><span data-stu-id="beba8-110">They do not change what the DVD Navigator reads from the disk.</span></span> <span data-ttu-id="beba8-111"> (下一節中說明的一個重要例外狀況，與 **Stop** 方法相關。 ) </span><span class="sxs-lookup"><span data-stu-id="beba8-111">(There is one important exception, explained in the next section, related to the **Stop** method.)</span></span>

<span data-ttu-id="beba8-112">例如， [**IDvdControl2：:P ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) 方法會發出附錄 J "Pause \_ On" 命令，但不會暫停篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="beba8-112">For example, [**IDvdControl2::Pause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) method issues the Annex J "Pause\_On" command, but does not pause the filter graph.</span></span> <span data-ttu-id="beba8-113">另一方面， [**IMediaControl：:P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) 方法會暫停圖形，但不會發出任何 DVD 命令。</span><span class="sxs-lookup"><span data-stu-id="beba8-113">The [**IMediaControl::Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) method, on the other hand, pauses the graph but does not issue any DVD command.</span></span>

<span data-ttu-id="beba8-114">一般情況下，請使用 **IMediaControl：:P ause** 和 **Stop** 方法，而不是對應的 **IDvdControl2** 方法。</span><span class="sxs-lookup"><span data-stu-id="beba8-114">In general, use the **IMediaControl::Pause** and **Stop** methods instead of the corresponding **IDvdControl2** methods.</span></span> <span data-ttu-id="beba8-115">**IMediaControl** 方法有極小的延遲，而 **IDvdControl2** 方法的延遲最多可達二秒。</span><span class="sxs-lookup"><span data-stu-id="beba8-115">The **IMediaControl** methods have very small latencies, whereas the **IDvdControl2** methods can have up to two seconds of latency.</span></span>

<span data-ttu-id="beba8-116">停止播放</span><span class="sxs-lookup"><span data-stu-id="beba8-116">Stopping Playback</span></span>

<span data-ttu-id="beba8-117">[**IMediaControl：： Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)的行為取決於您可以使用 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)方法設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="beba8-117">The behavior of [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) depends on a flag that you can set with the [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method.</span></span>

-   <span data-ttu-id="beba8-118">如果 DVD \_ ResetOnStop 旗標為 **FALSE**， **IMediaControl：： Stop** 會停止圖形，但不會變更 DVD Navigator 的網域。</span><span class="sxs-lookup"><span data-stu-id="beba8-118">If the DVD\_ResetOnStop flag is **FALSE**, **IMediaControl::Stop** stops the graph, but does not change the DVD Navigator's domain.</span></span> <span data-ttu-id="beba8-119">當您再次呼叫 [執行] 時，會從目前的位置繼續播放。</span><span class="sxs-lookup"><span data-stu-id="beba8-119">When you call run again, playback resumes from the current position.</span></span>
-   <span data-ttu-id="beba8-120">如果 DVD \_ ResetOnStop 為 **TRUE**， **IMediaControl：： Stop** 會導致 dvd Navigator 重設。</span><span class="sxs-lookup"><span data-stu-id="beba8-120">If DVD\_ResetOnStop is **TRUE**, **IMediaControl::Stop** causes the DVD Navigator to reset.</span></span> <span data-ttu-id="beba8-121">當您再次呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 時，Dvd 導覽器會從第一個 Play 網域播放，如同您第一次插入 dvd 一樣。</span><span class="sxs-lookup"><span data-stu-id="beba8-121">When you call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) again, the DVD Navigator plays from the First Play domain, as if you were inserting the DVD for the first time.</span></span>

<span data-ttu-id="beba8-122">DVD \_ ResetOnStop 旗標預設為 **TRUE** ，以與繼承應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="beba8-122">The DVD\_ResetOnStop flag is **TRUE** by default, for compatibility with older applications.</span></span> <span data-ttu-id="beba8-123">不過，一般而言，您應該覆寫預設值，並將旗標設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="beba8-123">Generally, however, you should override the default and set the flag to **FALSE**.</span></span> <span data-ttu-id="beba8-124">原因是某些事件可能會導致圖形在播放期間停止。</span><span class="sxs-lookup"><span data-stu-id="beba8-124">The reason is that certain events can cause the graph to stop during playback.</span></span> <span data-ttu-id="beba8-125">例如，如果顯示解析度變更，則篩選圖形會停止，重新連接影片轉譯器並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="beba8-125">For example, if the display resolution changes, the filter graph stops, reconnects the video renderer, and restarts.</span></span> <span data-ttu-id="beba8-126">如果 DVD \_ ResetOnStop 為 **TRUE**，播放將會從光碟的開頭重新開機。這可能不是使用者預期的。</span><span class="sxs-lookup"><span data-stu-id="beba8-126">If DVD\_ResetOnStop is **TRUE**, playback will restart from the beginning of the disc. That is probably not what the user expects.</span></span>

<span data-ttu-id="beba8-127">因此，在您的應用程式開始時，將 DVD ResetOnStop 的 **SetOption** 呼叫 \_ 設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="beba8-127">At the beginning of your application, therefore, call **SetOption** with DVD\_ResetOnStop set to **FALSE**.</span></span> <span data-ttu-id="beba8-128">如果您想要停止播放，並讓它從相同的位置繼續，請呼叫 **IMediaControl：： stop** 或 **IMediaControl：:P ause**。</span><span class="sxs-lookup"><span data-stu-id="beba8-128">If you want to stop playback and have it resume from the same location, call **IMediaControl::Stop** or **IMediaControl::Pause**.</span></span> <span data-ttu-id="beba8-129">如果您想要停止播放和重設磁片，請呼叫具有等於 TRUE 之 DVD ResetOnStop 的 **setoption** \_ ; 然後呼叫 **IMediaControl：： stop**; 最後，再次呼叫 **setoption** ，然後將 DVD ResetOnStop 重設 \_ 為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="beba8-129">If you want to stop playback and reset the disk, call **SetOption** with DVD\_ResetOnStop equal to **TRUE**; then call **IMediaControl::Stop**; finally, call **SetOption** again and reset DVD\_ResetOnStop to **FALSE**.</span></span>

<span data-ttu-id="beba8-130">暫停播放</span><span class="sxs-lookup"><span data-stu-id="beba8-130">Pausing Playback</span></span>

<span data-ttu-id="beba8-131">如果您在圖形暫停時提供 DVD 導覽器命令，則在圖形再次執行之前，命令可能無法完成。</span><span class="sxs-lookup"><span data-stu-id="beba8-131">If you give the DVD Navigator a command while the graph is paused, the command may not complete until the graph runs again.</span></span> <span data-ttu-id="beba8-132">在某些情況下，這可能會在您的應用程式中造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="beba8-132">In some situations, this can cause a deadlock in your application.</span></span> <span data-ttu-id="beba8-133">您應該遵循兩個規則來避免鎖死：</span><span class="sxs-lookup"><span data-stu-id="beba8-133">There are two rules you should follow to avoid deadlocks:</span></span>

-   <span data-ttu-id="beba8-134">暫停時，請勿發出一個以上的非同步 DVD 命令。</span><span class="sxs-lookup"><span data-stu-id="beba8-134">While paused, do not issue more than one asynchronous DVD command.</span></span>
-   <span data-ttu-id="beba8-135">暫停時，不會封鎖應用程式的 UI 執行緒或變更圖形狀態的執行緒。</span><span class="sxs-lookup"><span data-stu-id="beba8-135">While paused, do not block the application's UI thread or the thread that changes the state of the graph.</span></span>

<span data-ttu-id="beba8-136">第二個規則值得詳細檢查。</span><span class="sxs-lookup"><span data-stu-id="beba8-136">The second rule is worth examining in more detail.</span></span> <span data-ttu-id="beba8-137">以下是一些可能會造成鎖死的特定案例：</span><span class="sxs-lookup"><span data-stu-id="beba8-137">Here are some specific scenarios that may cause a deadlock:</span></span>

-   <span data-ttu-id="beba8-138">**案例**：在暫停的情況下，應用程式會發出具有封鎖旗標的 DVD 命令。</span><span class="sxs-lookup"><span data-stu-id="beba8-138">**Scenario**: While paused, the application issues a DVD command with the blocking flag.</span></span> <span data-ttu-id="beba8-139">如果發出 DVD 命令的執行緒是發出執行命令的相同執行緒，這可能會導致鎖死。</span><span class="sxs-lookup"><span data-stu-id="beba8-139">This can cause a deadlock if the thread that issues the DVD command is the same thread that issues the run command.</span></span> <span data-ttu-id="beba8-140">DVD 命令會封鎖，直到圖形執行為止，但在命令完成之前，圖形無法執行。</span><span class="sxs-lookup"><span data-stu-id="beba8-140">The DVD command blocks until the graph runs, but the graph cannot run until the command completes.</span></span>

    <span data-ttu-id="beba8-141">**建議**：在個別的背景工作執行緒上發出 DVD 命令，或不要使用封鎖旗標。</span><span class="sxs-lookup"><span data-stu-id="beba8-141">**Recommendation**: Issue the DVD command on a separate worker thread, or don't use the blocking flag.</span></span>

-   <span data-ttu-id="beba8-142">**案例**：在暫停的情況下，應用程式會發出 DVD 命令，然後在命令物件上呼叫 [**IDvdCmd：： WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) 。</span><span class="sxs-lookup"><span data-stu-id="beba8-142">**Scenario**: While paused, the application issues a DVD command, then calls [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) on the command object.</span></span> <span data-ttu-id="beba8-143">這種情況相當於先前的範例。</span><span class="sxs-lookup"><span data-stu-id="beba8-143">This situation is equivalent to the previous example.</span></span> <span data-ttu-id="beba8-144">如果您從 UI 執行緒呼叫 **wait** ，ui 執行緒將無法執行圖形，直到 **等候** 方法解除封鎖為止，但 **等候** 方法將不會解除封鎖，直到圖形執行為止。</span><span class="sxs-lookup"><span data-stu-id="beba8-144">If you call **Wait** from the UI thread, the UI thread cannot run the graph until the **Wait** method unblocks, but the **Wait** method will not unblock until the graph runs.</span></span>

    <span data-ttu-id="beba8-145">**建議**：在背景工作執行緒上呼叫 **Wait** 。</span><span class="sxs-lookup"><span data-stu-id="beba8-145">**Recommendation**: Call **Wait** on a worker thread.</span></span>

-   <span data-ttu-id="beba8-146">**案例**：當圖形正在執行時，應用程式會以封鎖旗標發出 DVD 命令，然後呼叫另一個執行緒的暫停。</span><span class="sxs-lookup"><span data-stu-id="beba8-146">**Scenario**: While the graph is running, the application issues a DVD command with the blocking flag, and then calls pause from another thread.</span></span> <span data-ttu-id="beba8-147">這是可能的競爭情形，因為圖形可能會在發出命令之前暫停。</span><span class="sxs-lookup"><span data-stu-id="beba8-147">This is a possible race condition because the graph may pause before the command is issued.</span></span> <span data-ttu-id="beba8-148">如果這兩個執行緒中的一個執行緒是 UI 執行緒，您可能會造成類似先前兩個範例的鎖死。</span><span class="sxs-lookup"><span data-stu-id="beba8-148">If one of the two threads is the UI thread, you may cause a deadlock similar to the previous two examples.</span></span> <span data-ttu-id="beba8-149">此範例說明如果您的應用程式使用多個執行緒，撰寫安全線程程式碼的重要性。</span><span class="sxs-lookup"><span data-stu-id="beba8-149">This example illustrates the importance of writing thread-safe code if your application uses multiple threads.</span></span>

    <span data-ttu-id="beba8-150">**建議**：如果您使用背景工作執行緒，請確定您的程式碼為安全線程。</span><span class="sxs-lookup"><span data-stu-id="beba8-150">**Recommendation**: If you use worker threads, make sure your code is thread-safe.</span></span>

-   <span data-ttu-id="beba8-151">**案例**：在暫停的情況下，應用程式會停用 UI 中的 run 命令，然後發出非同步 DVD 命令。</span><span class="sxs-lookup"><span data-stu-id="beba8-151">**Scenario**: While paused, the application disables the run command from the UI, and then issues an asynchronous DVD command.</span></span> <span data-ttu-id="beba8-152">由於應用程式執行緒仍在執行中，因此這種情況並不會嚴格地產生鎖死。</span><span class="sxs-lookup"><span data-stu-id="beba8-152">This case is not strictly a deadlock, because the application thread is still running.</span></span> <span data-ttu-id="beba8-153">不過，使用者現在無法執行圖形，因此命令將永遠不會完成。</span><span class="sxs-lookup"><span data-stu-id="beba8-153">However, the user is now prevented from running the graph, and therefore the command will never complete.</span></span>

    <span data-ttu-id="beba8-154">**建議**：暫停時，一律讓 run 命令保持啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="beba8-154">**Recommendation**: When pausing, always leave the run command enabled.</span></span>

<span data-ttu-id="beba8-155">將 DVD 搜尋到指定的時間</span><span class="sxs-lookup"><span data-stu-id="beba8-155">Seeking a DVD to a Specified Time</span></span>

<span data-ttu-id="beba8-156">若要精確地搜尋光碟上的指定時間，請呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)。</span><span class="sxs-lookup"><span data-stu-id="beba8-156">To accurately seek to a specified time on a disc, call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span></span> <span data-ttu-id="beba8-157">然後呼叫 [**IDvdControl2：:P layattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)，指定時間，並將 *DWFLAGS* 設定為 DVD CMD 旗標排清 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="beba8-157">Then call [**IDvdControl2::PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), specifying the time and setting *dwFlags* to DVD\_CMD\_FLAG\_Flush.</span></span>

## <a name="related-topics"></a><span data-ttu-id="beba8-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="beba8-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beba8-159">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="beba8-159">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



