---
description: 動態重新連接
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: 動態重新連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467724"
---
# <a name="dynamic-reconnection"></a><span data-ttu-id="bdf52-103">動態重新連接</span><span class="sxs-lookup"><span data-stu-id="bdf52-103">Dynamic Reconnection</span></span>

<span data-ttu-id="bdf52-104">在大部分的 DirectShow 篩選中，當圖形正在主動串流資料時，無法重新連線 pin。</span><span class="sxs-lookup"><span data-stu-id="bdf52-104">In most DirectShow filters, pins cannot be reconnected while the graph is actively streaming data.</span></span> <span data-ttu-id="bdf52-105">應用程式必須在重新連接釘選之前停止圖形。</span><span class="sxs-lookup"><span data-stu-id="bdf52-105">The application must stop the graph before reconnecting the pins.</span></span> <span data-ttu-id="bdf52-106">不過，某些篩選器在圖形執行時支援 pin 重新連接，這項程式稱為動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="bdf52-106">However, some filters do support pin reconnections while the graph is running, a process known as dynamic reconnection.</span></span> <span data-ttu-id="bdf52-107">這可以透過應用程式或圖形中的篩選來完成。</span><span class="sxs-lookup"><span data-stu-id="bdf52-107">This can be done either by the application, or by a filter in the graph.</span></span>

<span data-ttu-id="bdf52-108">例如，請考慮下圖中的圖表。</span><span class="sxs-lookup"><span data-stu-id="bdf52-108">As an example, consider the graph in the following illustration.</span></span>

![動態圖形-建立圖表](images/dyngraph.png)

<span data-ttu-id="bdf52-110">動態重新連線的其中一個案例可能是在圖形執行時從圖形移除篩選2，然後將它取代為另一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="bdf52-110">One scenario for dynamic reconnection might be to remove Filter 2 from the graph, while the graph is running, and replace it with another filter.</span></span> <span data-ttu-id="bdf52-111">若要讓此案例正常運作，必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="bdf52-111">For this scenario to work, the following must be true:</span></span>

-   <span data-ttu-id="bdf52-112">篩選 3 (pin D) 的輸入 pin 必須支援 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) 介面。</span><span class="sxs-lookup"><span data-stu-id="bdf52-112">The input pin on Filter 3 (pin D) must support the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="bdf52-113">此介面可讓您在不停止篩選的情況下重新連接 pin。</span><span class="sxs-lookup"><span data-stu-id="bdf52-113">This interface enables the pin to be reconnected without stopping the filter.</span></span>
-   <span data-ttu-id="bdf52-114">篩選 1 (釘選) 的輸出釘選，必須能夠在進行重新連線時封鎖媒體資料的流程。</span><span class="sxs-lookup"><span data-stu-id="bdf52-114">The output pin on Filter 1 (pin A) must be able to block the flow of media data while the reconnection occurs.</span></span> <span data-ttu-id="bdf52-115">在重新連線期間，pin A 與 pin D 之間不會有任何資料移動。</span><span class="sxs-lookup"><span data-stu-id="bdf52-115">No data can travel between pin A and pin D during the reconnection.</span></span> <span data-ttu-id="bdf52-116">一般來說，這表示輸出的 pin 必須支援 [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="bdf52-116">Generally, this means the output pin must support the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) interface.</span></span> <span data-ttu-id="bdf52-117">但是，如果篩選1是起始重新連線的篩選，它可能會有一些內部機制來封鎖其本身的資料流程。</span><span class="sxs-lookup"><span data-stu-id="bdf52-117">However, if Filter 1 is the filter that initiates the reconnection, it might have some internal mechanism to block its own data flow.</span></span>

<span data-ttu-id="bdf52-118">動態重新連接將牽涉到下列步驟：</span><span class="sxs-lookup"><span data-stu-id="bdf52-118">The dynamic reconnection will involve the following steps:</span></span>

1.  <span data-ttu-id="bdf52-119">封鎖來自 pin A 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="bdf52-119">Block the data stream from pin A.</span></span>
2.  <span data-ttu-id="bdf52-120">重新連接釘選至 pin D，可能是透過新的中繼篩選。</span><span class="sxs-lookup"><span data-stu-id="bdf52-120">Reconnect pin A to pin D, possibly through a new intermediate filter.</span></span>
3.  <span data-ttu-id="bdf52-121">解除封鎖 pin A，讓資料再次開始流動。</span><span class="sxs-lookup"><span data-stu-id="bdf52-121">Unblock pin A so that data starts to flow again.</span></span>

<span data-ttu-id="bdf52-122">**步驟1。封鎖資料流程**</span><span class="sxs-lookup"><span data-stu-id="bdf52-122">**Step 1. Block the Data Stream**</span></span>

<span data-ttu-id="bdf52-123">若要封鎖資料流程，請呼叫釘選上的 [**IPinFlowControl：： block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 。您可以非同步或同步方式呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="bdf52-123">To block the data stream, call [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) on pin A. This method can be called either asynchronously or synchronously.</span></span> <span data-ttu-id="bdf52-124">若要以 *非同步* 方式呼叫方法，請建立 Win32 事件物件，並將事件控制碼傳遞給 **Block** 方法。</span><span class="sxs-lookup"><span data-stu-id="bdf52-124">To call the method *asynchronously*, create a Win32 event object and pass the event handle to the **Block** method.</span></span> <span data-ttu-id="bdf52-125">方法將會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="bdf52-125">The method will return immediately.</span></span> <span data-ttu-id="bdf52-126">使用 **WaitForSingleObject** 之類的函式，等候事件收到信號。</span><span class="sxs-lookup"><span data-stu-id="bdf52-126">Wait for the event to be signaled, using a function such as **WaitForSingleObject**.</span></span> <span data-ttu-id="bdf52-127">Pin 會在事件封鎖資料流程時發出信號。</span><span class="sxs-lookup"><span data-stu-id="bdf52-127">The pin signals the event when it has blocked the data flow.</span></span> <span data-ttu-id="bdf52-128">例如：</span><span class="sxs-lookup"><span data-stu-id="bdf52-128">For example:</span></span>


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



<span data-ttu-id="bdf52-129">若要 *同步* 呼叫方法，只要傳遞 **Null** 值，而不是事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="bdf52-129">To call the method *synchronously*, simply pass the value **NULL** instead of the event handle.</span></span> <span data-ttu-id="bdf52-130">現在方法會封鎖，直到作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="bdf52-130">Now the method will block until the operation completes.</span></span> <span data-ttu-id="bdf52-131">在 pin 準備好傳遞新的範例之前，可能不會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="bdf52-131">This may not happen until the pin is ready to deliver a new sample.</span></span> <span data-ttu-id="bdf52-132">如果已暫停篩選，這可能會花費任意的時間長度。</span><span class="sxs-lookup"><span data-stu-id="bdf52-132">If the filter is paused, this can take an arbitrary length of time.</span></span> <span data-ttu-id="bdf52-133">因此，請勿從主應用程式執行緒進行同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="bdf52-133">Therefore, do not make the synchronous call from your main application thread.</span></span> <span data-ttu-id="bdf52-134">請使用背景工作執行緒，否則請以非同步方式呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="bdf52-134">Use a worker thread, or else call the method asynchronously.</span></span>

<span data-ttu-id="bdf52-135">**步驟2。重新連接釘選**</span><span class="sxs-lookup"><span data-stu-id="bdf52-135">**Step 2. Reconnect the Pins**</span></span>

<span data-ttu-id="bdf52-136">若要重新連接釘選，請查詢 **IGraphConfig** 介面的篩選圖形管理員，然後呼叫 [**IGraphConfig：： reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) 或 [**IGraphConfig：：重新**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure)設定。</span><span class="sxs-lookup"><span data-stu-id="bdf52-136">To reconnect the pins, query the Filter Graph Manager for the **IGraphConfig** interface and call either [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) or [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span></span> <span data-ttu-id="bdf52-137">**Reconnect** 方法更容易使用;它會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="bdf52-137">The **Reconnect** method is simpler to use; it does the following:</span></span>

-   <span data-ttu-id="bdf52-138">在範例) 中停止中繼篩選 (篩選2，並將其從圖形中移除。</span><span class="sxs-lookup"><span data-stu-id="bdf52-138">Stops the intermediate filters (Filter 2 in the example) and removes them from the graph.</span></span>
-   <span data-ttu-id="bdf52-139">視需要新增中繼篩選準則。</span><span class="sxs-lookup"><span data-stu-id="bdf52-139">Adds new intermediate filters, if needed.</span></span>
-   <span data-ttu-id="bdf52-140">連接所有的釘選。</span><span class="sxs-lookup"><span data-stu-id="bdf52-140">Connects all the pins.</span></span>
-   <span data-ttu-id="bdf52-141">暫停或執行任何新的篩選準則，以符合圖形的狀態。</span><span class="sxs-lookup"><span data-stu-id="bdf52-141">Pauses or runs any new filters, to match the state of the graph.</span></span>

<span data-ttu-id="bdf52-142">**Reconnect** 方法有幾個選擇性參數，可用來指定要使用的 pin 連接和中繼篩選的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="bdf52-142">The **Reconnect** method has several optional parameters that can be used to specify the media type for the pin connection and the intermediate filter to use.</span></span> <span data-ttu-id="bdf52-143">例如：</span><span class="sxs-lookup"><span data-stu-id="bdf52-143">For example:</span></span>


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



<span data-ttu-id="bdf52-144">如需詳細資訊，請參閱參考頁面。</span><span class="sxs-lookup"><span data-stu-id="bdf52-144">For details, consult the reference page.</span></span> <span data-ttu-id="bdf52-145">如果 **重新連接** 方法沒有足夠的彈性，您可以使用 **重新** 設定方法，它會呼叫應用程式定義的回呼方法來重新連接釘選。</span><span class="sxs-lookup"><span data-stu-id="bdf52-145">If the **Reconnect** method is not flexible enough, you can use the **Reconfigure** method, which calls an application-defined callback method to reconnect the pins.</span></span> <span data-ttu-id="bdf52-146">若要使用此方法，請在您的應用程式中執行 [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="bdf52-146">To use this method, implement the [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) interface in your application.</span></span>

<span data-ttu-id="bdf52-147">在呼叫 **重新** 設定之前，請依先前所述，封鎖輸出釘選的資料流程。</span><span class="sxs-lookup"><span data-stu-id="bdf52-147">Before calling **Reconfigure**, block the data flow from the output pin, as described previously.</span></span> <span data-ttu-id="bdf52-148">然後在您要重新連接的圖表區段中，推送仍在擱置中的任何資料，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bdf52-148">Then push any data that is still pending in the section of the graph that you are reconnecting, as follows:</span></span>

1.  <span data-ttu-id="bdf52-149">在) 範例中， (pin D 的輸入 pin 上呼叫 [**IPinConnection：： NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) 。</span><span class="sxs-lookup"><span data-stu-id="bdf52-149">Call [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) on the input pin furthest downstream in the reconnection chain (pin D in the example).</span></span> <span data-ttu-id="bdf52-150">傳入 Win32 事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bdf52-150">Pass in a handle to a Win32 event.</span></span>
2.  <span data-ttu-id="bdf52-151">在輸入 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ，這會從您封鎖資料流程的輸出 pin 立即下游。</span><span class="sxs-lookup"><span data-stu-id="bdf52-151">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the input pin that is immediately downstream from the output pin where you blocked the data flow.</span></span> <span data-ttu-id="bdf52-152"> (在此範例中，資料流程被封鎖在釘選 A 上，因此您會在 pin B 上呼叫 **EndOfStream** 。 ) </span><span class="sxs-lookup"><span data-stu-id="bdf52-152">(In this example, the data flow was blocked at pin A, so you would call **EndOfStream** on pin B.)</span></span>
3.  <span data-ttu-id="bdf52-153">等候事件收到信號。</span><span class="sxs-lookup"><span data-stu-id="bdf52-153">Wait for the event to be signaled.</span></span> <span data-ttu-id="bdf52-154">輸入 pin (pin D) 在接收到資料流程結束通知時，對事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="bdf52-154">The input pin (pin D) signals the event when it receives the end-of-stream notification.</span></span> <span data-ttu-id="bdf52-155">這表示 pin 之間沒有任何資料正在移動，且呼叫者可以安全地重新連接 pin。</span><span class="sxs-lookup"><span data-stu-id="bdf52-155">This indicates that no data is traveling between the pins, and that the caller can safely reconnect the pins.</span></span>

<span data-ttu-id="bdf52-156">請注意， **IGraphConfig：： Reconnect** 方法會自動處理先前的步驟。</span><span class="sxs-lookup"><span data-stu-id="bdf52-156">Note that the **IGraphConfig::Reconnect** method automatically handles the previous steps.</span></span> <span data-ttu-id="bdf52-157">如果您使用 [ **重新** 設定] 方法，則只需要執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="bdf52-157">You only need to perform these steps if you are using the **Reconfigure** method.</span></span>

<span data-ttu-id="bdf52-158">資料透過圖形推送之後，請呼叫 **重新** 設定，並將指標傳遞至您的 **IGraphConfigCallback** 回呼介面。</span><span class="sxs-lookup"><span data-stu-id="bdf52-158">After the data is pushed through the graph, call **Reconfigure** and pass a pointer to your **IGraphConfigCallback** callback interface.</span></span> <span data-ttu-id="bdf52-159">篩選圖形管理員會呼叫您所提供的 [**IGraphConfigCallback：：重新**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) 設定方法。</span><span class="sxs-lookup"><span data-stu-id="bdf52-159">The Filter Graph Manager will call the [**IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) method that you have provided.</span></span>

<span data-ttu-id="bdf52-160">**步驟3。解除封鎖資料流程**</span><span class="sxs-lookup"><span data-stu-id="bdf52-160">**Step 3. Unblock the Data Flow**</span></span>

<span data-ttu-id="bdf52-161">當您重新連接釘選之後，請呼叫 **IPinFlowControl：： Block** ，將第一個參數的值為零，以解除封鎖資料流程。</span><span class="sxs-lookup"><span data-stu-id="bdf52-161">After you have reconnected the pins, unblock the data flow by calling **IPinFlowControl::Block** with a value of zero for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="bdf52-162">如果動態重新連接是由篩選執行，則有一些您必須注意的執行緒問題。</span><span class="sxs-lookup"><span data-stu-id="bdf52-162">If a dynamic reconnection is performed by a filter, there are some threading issues that you must be aware of.</span></span> <span data-ttu-id="bdf52-163">如果篩選圖形管理員嘗試停止篩選，它可能會鎖死，因為 Graph 會等候篩選停止，同時篩選可能會等候資料透過圖形推送。</span><span class="sxs-lookup"><span data-stu-id="bdf52-163">If the Filter Graph Manager tries to stop the filter, it can deadlock, because the graph waits for the filter to stop, while at the same time the filter may be waiting for data to be pushed through the graph.</span></span> <span data-ttu-id="bdf52-164">為了避免可能的鎖死，本節所述的部分方法會採取 Win32 事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bdf52-164">To prevent the possible deadlock, some of the methods described in this section take a handle to a Win32 event.</span></span> <span data-ttu-id="bdf52-165">如果篩選圖形管理員嘗試停止篩選，則篩選準則應該會通知事件。</span><span class="sxs-lookup"><span data-stu-id="bdf52-165">The filter should signal the event if the Filter Graph Manager attempts to stop the filter.</span></span> <span data-ttu-id="bdf52-166">如需詳細資訊，請參閱 [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) 和 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection)。</span><span class="sxs-lookup"><span data-stu-id="bdf52-166">For more information, see [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bdf52-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdf52-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdf52-168">動態圖表建立</span><span class="sxs-lookup"><span data-stu-id="bdf52-168">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



