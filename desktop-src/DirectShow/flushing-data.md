---
description: 清除資料
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: 清除資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687495"
---
# <a name="flushing-data"></a><span data-ttu-id="b59ee-103">清除資料</span><span class="sxs-lookup"><span data-stu-id="b59ee-103">Flushing Data</span></span>

<span data-ttu-id="b59ee-104">下列虛擬虛擬顯示如何執行 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法：</span><span class="sxs-lookup"><span data-stu-id="b59ee-104">The following pseudocode shows how to implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method:</span></span>


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



<span data-ttu-id="b59ee-105">當排清開始時， **BeginFlush** 方法會採用篩選鎖定，以序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="b59ee-105">When flushing starts, the **BeginFlush** method takes the filter lock, which serializes the state change.</span></span> <span data-ttu-id="b59ee-106">由於清除作業會在應用程式執行緒上進行，而且串流執行緒可能會在 **接收** 呼叫的過程中，因此無法安全地使用串流鎖定。</span><span class="sxs-lookup"><span data-stu-id="b59ee-106">It is not yet safe to take the streaming lock, because flushing happens on the application thread, and the streaming thread might be in the middle of a **Receive** call.</span></span> <span data-ttu-id="b59ee-107">Pin 必須保證 **接收** 未遭到封鎖，且任何後續的 **接收** 呼叫都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b59ee-107">The pin needs to guarantee that **Receive** is not blocked, and that any subsequent calls to **Receive** will fail.</span></span> <span data-ttu-id="b59ee-108">[**CBaseInputPin：： BeginFlush**](cbaseinputpin-beginflush.md)方法會設定內部旗標（ [**CBaseInputPin：： m \_ bFlushing**](cbaseinputpin-m-bflushing.md)）。</span><span class="sxs-lookup"><span data-stu-id="b59ee-108">The [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method sets an internal flag, [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md).</span></span> <span data-ttu-id="b59ee-109">當旗標為 **TRUE** 時， **Receive** 方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="b59ee-109">When the flag is **TRUE**, the **Receive** method fails.</span></span>

<span data-ttu-id="b59ee-110">藉由提供下游的 **BeginFlush** 呼叫，pin 可保證所有下游篩選器都會釋放其範例，並從 **接收** 呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="b59ee-110">By delivering the **BeginFlush** call downstream, the pin guarantees that all downstream filters release their samples and return from **Receive** calls.</span></span> <span data-ttu-id="b59ee-111">這接著保證輸入的 pin 不會被封鎖等候 **GetBuffer** 或 **接收**。</span><span class="sxs-lookup"><span data-stu-id="b59ee-111">This in turn guarantees that the input pin is not blocked waiting for **GetBuffer** or **Receive**.</span></span> <span data-ttu-id="b59ee-112">如果您的 pin **接收方法會** 等待事件 (例如，若要取得資源) ， **BeginFlush** 方法應藉由設定事件來強制終止等候。</span><span class="sxs-lookup"><span data-stu-id="b59ee-112">If your pin's **Receive** method ever waits on an event (for example, to get resources), the **BeginFlush** method should force the wait to terminate by setting the event.</span></span> <span data-ttu-id="b59ee-113">此時， **Receive** 方法保證會傳回，而 **m \_ bFlushing** 旗標會防止新的 **接收** 呼叫執行任何工作。</span><span class="sxs-lookup"><span data-stu-id="b59ee-113">At this point, the **Receive** method is guaranteed to return, and the **m\_bFlushing** flag prevents new **Receive** calls from doing any work.</span></span>

<span data-ttu-id="b59ee-114">針對某些篩選器，所有 **BeginFlush** 都需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="b59ee-114">For some filters, that is all **BeginFlush** needs to do.</span></span> <span data-ttu-id="b59ee-115">**EndFlush** 方法會向篩選發出通知，讓它可以再次開始接收範例。</span><span class="sxs-lookup"><span data-stu-id="b59ee-115">The **EndFlush** method will signal to the filter that it can start receiving samples again.</span></span> <span data-ttu-id="b59ee-116">其他篩選器可能需要在 **BeginFlush** 中使用也可用於 **接收** 的變數或資源。</span><span class="sxs-lookup"><span data-stu-id="b59ee-116">Other filters may need to use variables or resources in **BeginFlush** that are also used in **Receive**.</span></span> <span data-ttu-id="b59ee-117">在這種情況下，篩選應先保存串流鎖定。</span><span class="sxs-lookup"><span data-stu-id="b59ee-117">In that case, the filter should hold the streaming lock first.</span></span> <span data-ttu-id="b59ee-118">在上述任何步驟之前，請務必不要這麼做，因為您可能會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="b59ee-118">Be sure not to do this before any of the previous steps, because you might cause a deadlock.</span></span>

<span data-ttu-id="b59ee-119">**EndFlush** 方法會保存篩選鎖定，並傳播呼叫下游：</span><span class="sxs-lookup"><span data-stu-id="b59ee-119">The **EndFlush** method holds the filter lock and propagates the call downstream:</span></span>


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



<span data-ttu-id="b59ee-120">[**CBaseInputPin：： EndFlush**](cbaseinputpin-endflush.md)方法會將 **m \_ bFlushing** 旗標重設為 **FALSE**，讓 **Receive** 方法再次開始接收範例。</span><span class="sxs-lookup"><span data-stu-id="b59ee-120">The [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method resets the **m\_bFlushing** flag to **FALSE**, which allows the **Receive** method to start receiving samples again.</span></span> <span data-ttu-id="b59ee-121">這應該是 **EndFlush** 中的最後一個步驟，因為 pin 必須等到清除完成，而且所有下游篩選都收到通知，才能接收任何範例。</span><span class="sxs-lookup"><span data-stu-id="b59ee-121">This should be the last step in **EndFlush**, because the pin must not receive any samples until flushing is complete and all downstream filters are notified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b59ee-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="b59ee-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b59ee-123">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="b59ee-123">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



