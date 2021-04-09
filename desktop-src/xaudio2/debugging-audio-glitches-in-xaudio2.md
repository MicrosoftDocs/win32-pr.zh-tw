---
description: 問題可能會發生在 XAudio2 中，本主題會說明如何報告這些問題，以及解決這些問題的一些方法。
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: 對 XAudio2 中的音訊問題進行偵錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850379"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a><span data-ttu-id="25893-103">對 XAudio2 中的音訊問題進行偵錯</span><span class="sxs-lookup"><span data-stu-id="25893-103">Debugging Audio Glitches in XAudio2</span></span>

<span data-ttu-id="25893-104">問題可能會發生在 XAudio2 中，本主題會說明如何報告這些問題，以及解決這些問題的一些方法。</span><span class="sxs-lookup"><span data-stu-id="25893-104">Glitches can occur in XAudio2, this topic covers how they are reported and some approaches to fixing them.</span></span>

<span data-ttu-id="25893-105">本總覽涵蓋下列主題：</span><span class="sxs-lookup"><span data-stu-id="25893-105">This overview covers the following topics:</span></span>

-   [<span data-ttu-id="25893-106">音訊輸出問題或問題的原因</span><span class="sxs-lookup"><span data-stu-id="25893-106">Causes of audio output problems or glitches</span></span>](#causes-of-audio-output-problems-or-glitches)
-   [<span data-ttu-id="25893-107">XAudio2 如何報告問題</span><span class="sxs-lookup"><span data-stu-id="25893-107">How XAudio2 reports problems</span></span>](#how-xaudio2-reports-problems)
-   [<span data-ttu-id="25893-108">修正問題的方法</span><span class="sxs-lookup"><span data-stu-id="25893-108">Approaches to fixing problems</span></span>](#approaches-to-fixing-problems)
-   [<span data-ttu-id="25893-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="25893-109">Related topics</span></span>](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a><span data-ttu-id="25893-110">音訊輸出問題或問題的原因</span><span class="sxs-lookup"><span data-stu-id="25893-110">Causes of audio output problems or glitches</span></span>

<span data-ttu-id="25893-111">XAudio2 輸出可能發生問題的原因有好幾個。</span><span class="sxs-lookup"><span data-stu-id="25893-111">Glitches can occur in XAudio2 output for several reasons.</span></span>

-   <span data-ttu-id="25893-112">XAudio2 來源語音為耗盡。</span><span class="sxs-lookup"><span data-stu-id="25893-112">An XAudio2 source voice is starved.</span></span> <span data-ttu-id="25893-113">用戶端不會將新音訊提交到足夠的速度。</span><span class="sxs-lookup"><span data-stu-id="25893-113">The client is not submitting fresh audio to it fast enough.</span></span> <span data-ttu-id="25893-114">因為沒有任何資料可供播放，所以您會收到無回應。</span><span class="sxs-lookup"><span data-stu-id="25893-114">You get silence because it has no data to play.</span></span>
-   <span data-ttu-id="25893-115">XAudio2 整體會有過重的負擔。</span><span class="sxs-lookup"><span data-stu-id="25893-115">XAudio2 as a whole is overburdened.</span></span> <span data-ttu-id="25893-116">產生 *x* 毫秒的音訊需要比 *x* 毫秒更長的時間。</span><span class="sxs-lookup"><span data-stu-id="25893-116">It takes longer than *X* ms to produce *X* ms of audio.</span></span> <span data-ttu-id="25893-117">您會收到中斷，因為 XAudio2 無法像音訊裝置需要一樣快速產生資料。</span><span class="sxs-lookup"><span data-stu-id="25893-117">You get dropouts because XAudio2 can't produce data as fast as the audio device needs it.</span></span> <span data-ttu-id="25893-118">您可能一次執行太多聲音或效果、在 XAudio2 回呼中執行太多工作，或太頻繁地進行 XAudio2 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="25893-118">You might be running too many voices or effects at a time, doing too much work in XAudio2 callbacks, or making XAudio2 API calls too frequently.</span></span>
-   <span data-ttu-id="25893-119">音訊處理執行緒很拖延，因為用戶端在執行某些 XAudio2 回呼時，會執行一些作業來封鎖執行緒。</span><span class="sxs-lookup"><span data-stu-id="25893-119">The audio processing thread is stalling because the client's implementation of some XAudio2 callback is doing things that can block the thread.</span></span> <span data-ttu-id="25893-120">例如，它可能會存取磁片、與其他執行緒進行同步處理，或呼叫可能封鎖的其他函式。</span><span class="sxs-lookup"><span data-stu-id="25893-120">For example, it might be accessing the disk, synchronizing with other threads, or calling other functions that may block.</span></span> <span data-ttu-id="25893-121">使用回呼可發出的較低優先順序背景執行緒來執行這類工作。</span><span class="sxs-lookup"><span data-stu-id="25893-121">Use a lower-priority background thread that the callback can signal to perform such tasks.</span></span>
-   <span data-ttu-id="25893-122">整個系統都會超載。</span><span class="sxs-lookup"><span data-stu-id="25893-122">The system as a whole is overloaded.</span></span> <span data-ttu-id="25893-123">執行的其他執行緒與 XAudio2 相同或更高的優先順序正在執行太多工作。</span><span class="sxs-lookup"><span data-stu-id="25893-123">Other threads running at the same or higher priority than XAudio2 are doing too much work.</span></span> <span data-ttu-id="25893-124">它們會與音訊執行緒爭用 CPU 時間。</span><span class="sxs-lookup"><span data-stu-id="25893-124">They are competing with the audio thread for CPU time.</span></span>

## <a name="how-xaudio2-reports-problems"></a><span data-ttu-id="25893-125">XAudio2 如何報告問題</span><span class="sxs-lookup"><span data-stu-id="25893-125">How XAudio2 reports problems</span></span>

<span data-ttu-id="25893-126">XAudio2 可以透過數種方式來傳達 debug 組建中的問題。</span><span class="sxs-lookup"><span data-stu-id="25893-126">XAudio2 can communicate glitches in the debug build in several ways.</span></span>

-   <span data-ttu-id="25893-127">如果正在耗盡語音，XAudio2 會顯示此表單中的訊息。</span><span class="sxs-lookup"><span data-stu-id="25893-127">If a voice is being starved, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   <span data-ttu-id="25893-128">如果音訊執行緒執行太長的時間，XAudio2 會顯示此表單中的訊息。</span><span class="sxs-lookup"><span data-stu-id="25893-128">If the audio thread runs for too long, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    <span data-ttu-id="25893-129">一般來說，此訊息會出現在下一個訊息中。</span><span class="sxs-lookup"><span data-stu-id="25893-129">Typically, this message occurs with the next message.</span></span>

-   <span data-ttu-id="25893-130">如果音訊驅動程式無法及時送入新的音訊資料，XAudio2 會顯示此表單中的訊息。</span><span class="sxs-lookup"><span data-stu-id="25893-130">If the audio driver can't be fed new audio data on time, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   <span data-ttu-id="25893-131">呼叫 [**IXAudio2：： GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) 會提供 XAudio2 的效能資料，包括自 XAudio2 引擎啟動以來的問題總數。</span><span class="sxs-lookup"><span data-stu-id="25893-131">Calling [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) provides XAudio2 performance data, including the total number of glitches since the XAudio2 engine started.</span></span>

## <a name="approaches-to-fixing-problems"></a><span data-ttu-id="25893-132">修正問題的方法</span><span class="sxs-lookup"><span data-stu-id="25893-132">Approaches to fixing problems</span></span>

<span data-ttu-id="25893-133">減少音訊問題的可能方式包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="25893-133">Possible ways to reduce audio glitches include the following.</span></span>

-   <span data-ttu-id="25893-134">在語音耗盡案例中：增加聲音上排入佇列的音訊資料量。</span><span class="sxs-lookup"><span data-stu-id="25893-134">In the voice starvation case: Increase the amount of audio data that is queued ahead on a voice.</span></span> <span data-ttu-id="25893-135">您可以使用 [**IXAudio2SourceVoice：： >getstate**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) 來探索任何時間佇列的緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="25893-135">You can use [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) to discover the number of buffers queued at any moment.</span></span> <span data-ttu-id="25893-136">如果您仍然看到「聲音耗盡」的錯誤，但聽不到任何問題，請確定您正在設定 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)。在音效的 \_ \_ \_ 最終緩衝區上 XAUDIO2 資料流程結尾的旗標。</span><span class="sxs-lookup"><span data-stu-id="25893-136">If you still see voice starvation errors, but can't hear any glitch, make sure you are setting [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flags** to XAUDIO2\_END\_OF\_STREAM on the final buffer of a sound.</span></span> <span data-ttu-id="25893-137">如此一來，XAudio2 就不會預期任何緩衝區都必須在這個動作完成後立即可用。</span><span class="sxs-lookup"><span data-stu-id="25893-137">This tells XAudio2 not to expect any more buffers necessarily to be available as soon as this one completes.</span></span>

    <span data-ttu-id="25893-138">在其他情況下：</span><span class="sxs-lookup"><span data-stu-id="25893-138">In the other cases:</span></span>

    -   <span data-ttu-id="25893-139">減少圖形中的作用中語音和效果的數目，特別是高成本的效果，例如「回音」。</span><span class="sxs-lookup"><span data-stu-id="25893-139">Reduce the number of active voices and effects in the graph, especially expensive effects like reverb.</span></span>
    -   <span data-ttu-id="25893-140">停用您未使用的語音和效果。</span><span class="sxs-lookup"><span data-stu-id="25893-140">Disable voices and effects you're not using.</span></span>
    -   <span data-ttu-id="25893-141">盡可能 \_ \_ \_ \_ 在 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)中使用 XAUDIO2 voice NOSRC 和 XAUDIO2 voice NOPITCH 旗標。</span><span class="sxs-lookup"><span data-stu-id="25893-141">Use the XAUDIO2\_VOICE\_NOSRC and XAUDIO2\_VOICE\_NOPITCH flags in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), whenever possible.</span></span> <span data-ttu-id="25893-142">取樣率轉換很昂貴。</span><span class="sxs-lookup"><span data-stu-id="25893-142">Sample rate conversion is costly.</span></span>
    -   <span data-ttu-id="25893-143">減少個別聲音的取樣率。</span><span class="sxs-lookup"><span data-stu-id="25893-143">Reduce the sample rate of individual voices.</span></span> <span data-ttu-id="25893-144">例如，submix 聲音裝載的「回音」效果，其取樣率會低於傳送給它的來源語音。</span><span class="sxs-lookup"><span data-stu-id="25893-144">For example, a submix voice hosting a reverb effect can have a lower sample rate than the source voice sending to it.</span></span> <span data-ttu-id="25893-145">不需要高精確度的音效（例如爆炸和 gunshots）也可以記錄較低的取樣率。</span><span class="sxs-lookup"><span data-stu-id="25893-145">Sounds such as explosions and gunshots that don't need high fidelity can also be recorded at lower sample rates.</span></span>
    -   <span data-ttu-id="25893-146">確定回呼的執行工作盡可能少，而且永遠不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="25893-146">Ensure that callback implementations do as little work as possible and never block.</span></span>
    -   <span data-ttu-id="25893-147">對 XAudio2 發出較少的呼叫。</span><span class="sxs-lookup"><span data-stu-id="25893-147">Make fewer calls to XAudio2.</span></span> <span data-ttu-id="25893-148">音訊參數通常不需要針對每個影片畫面更新。</span><span class="sxs-lookup"><span data-stu-id="25893-148">Audio parameters usually don't need to be updated for every video frame.</span></span> <span data-ttu-id="25893-149">每隔30毫秒就夠了。</span><span class="sxs-lookup"><span data-stu-id="25893-149">Every 30 ms or so is sufficient.</span></span> <span data-ttu-id="25893-150">您應消除重複的呼叫，例如快速連續地設定磁片區數次。</span><span class="sxs-lookup"><span data-stu-id="25893-150">You should eliminate redundant calls, such as setting volume several times in quick succession.</span></span>
    -   <span data-ttu-id="25893-151">減少遊戲的整體 CPU 使用率。</span><span class="sxs-lookup"><span data-stu-id="25893-151">Reduce the game's overall CPU usage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25893-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="25893-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25893-153">調試功能</span><span class="sxs-lookup"><span data-stu-id="25893-153">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="25893-154">XAudio2 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="25893-154">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
