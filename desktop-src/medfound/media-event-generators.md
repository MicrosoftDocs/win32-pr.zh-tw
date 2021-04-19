---
description: 媒體事件產生器
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: 媒體事件產生器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992641"
---
# <a name="media-event-generators"></a><span data-ttu-id="7a04e-103">媒體事件產生器</span><span class="sxs-lookup"><span data-stu-id="7a04e-103">Media Event Generators</span></span>

<span data-ttu-id="7a04e-104">媒體基礎為物件提供一致的方式來傳送事件。</span><span class="sxs-lookup"><span data-stu-id="7a04e-104">Media Foundation provides a consistent way for objects to send events.</span></span> <span data-ttu-id="7a04e-105">物件可以使用事件來指示非同步方法的完成，或通知應用程式有關物件狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="7a04e-105">An object can use events to signal the completion of an asynchronous method, or to notify the application about a change in the object's state.</span></span>

<span data-ttu-id="7a04e-106">如果物件傳送事件，它會公開 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="7a04e-106">If an object sends events, it exposes the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="7a04e-107">每當物件傳送新事件時，該事件就會放置在佇列中。</span><span class="sxs-lookup"><span data-stu-id="7a04e-107">Whenever the object sends a new event, the event is placed in a queue.</span></span> <span data-ttu-id="7a04e-108">應用程式可以藉由呼叫下列其中一種方法，從佇列要求下一個事件：</span><span class="sxs-lookup"><span data-stu-id="7a04e-108">The application can request the next event from the queue by calling one of the following methods:</span></span>

-   [<span data-ttu-id="7a04e-109">**IMFMediaEventGenerator::GetEvent**</span><span class="sxs-lookup"><span data-stu-id="7a04e-109">**IMFMediaEventGenerator::GetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [<span data-ttu-id="7a04e-110">**IMFMediaEventGenerator::BeginGetEvent**</span><span class="sxs-lookup"><span data-stu-id="7a04e-110">**IMFMediaEventGenerator::BeginGetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

<span data-ttu-id="7a04e-111">[**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)方法是同步的。</span><span class="sxs-lookup"><span data-stu-id="7a04e-111">The [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) method is synchronous.</span></span> <span data-ttu-id="7a04e-112">如果事件已在佇列中，則此方法會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="7a04e-112">If an event is already in the queue, the method returns immediately.</span></span> <span data-ttu-id="7a04e-113">如果佇列中沒有任何事件，則方法會立即失敗，或封鎖直到下一個事件排入佇列，視您傳遞至 **GetEvent** 的旗標而定。</span><span class="sxs-lookup"><span data-stu-id="7a04e-113">If there is no event in the queue, the method either fails immediately, or blocks until the next event is queued, depending on which flag you pass into **GetEvent**.</span></span>

<span data-ttu-id="7a04e-114">[**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)方法是非同步，因此永遠不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="7a04e-114">The [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method is asynchronous, so it never blocks.</span></span> <span data-ttu-id="7a04e-115">這個方法會採用應用程式必須執行之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7a04e-115">This method takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which the application must implement.</span></span> <span data-ttu-id="7a04e-116">叫用回呼時，應用程式會呼叫 [**IMFMediaEventGenerator：： EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) 以從佇列取得事件。</span><span class="sxs-lookup"><span data-stu-id="7a04e-116">When the callback is invoked, the application calls [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event from the queue.</span></span> <span data-ttu-id="7a04e-117">如需 **IMFAsyncCallback** 的詳細資訊，請參閱 [非同步回呼方法](asynchronous-callback-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="7a04e-117">For more information about **IMFAsyncCallback**, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="7a04e-118">事件是由 [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="7a04e-118">Events are represented by the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span> <span data-ttu-id="7a04e-119">此介面有下列方法：</span><span class="sxs-lookup"><span data-stu-id="7a04e-119">This interface has the following methods:</span></span>

-   <span data-ttu-id="7a04e-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)：抓取事件種類。</span><span class="sxs-lookup"><span data-stu-id="7a04e-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Retrieves the event type.</span></span> <span data-ttu-id="7a04e-121">事件種類表示觸發事件發生的狀況。</span><span class="sxs-lookup"><span data-stu-id="7a04e-121">The event type indicates what happened to trigger the event.</span></span>

-   <span data-ttu-id="7a04e-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)：抓取 **HRESULT** 值，指出觸發事件的作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="7a04e-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Retrieves an **HRESULT** value, indicating whether the operation that triggered the event was successful.</span></span> <span data-ttu-id="7a04e-123">如果非同步作業失敗， **GetStatus** 會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="7a04e-123">If an operation fails asynchronously, **GetStatus** returns a failure code.</span></span>

-   <span data-ttu-id="7a04e-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)：抓取包含事件資料的 **PROPVARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="7a04e-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Retrieves a **PROPVARIANT** that contains event data.</span></span> <span data-ttu-id="7a04e-125">事件資料取決於事件種類。</span><span class="sxs-lookup"><span data-stu-id="7a04e-125">The event data depends on the event type.</span></span> <span data-ttu-id="7a04e-126">某些事件沒有任何資料。</span><span class="sxs-lookup"><span data-stu-id="7a04e-126">Some events do not have any data.</span></span>

-   <span data-ttu-id="7a04e-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)：抓取 **GUID**。</span><span class="sxs-lookup"><span data-stu-id="7a04e-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Retrieves a **GUID**.</span></span> <span data-ttu-id="7a04e-128">這個方法會套用至 [MEExtendedType 事件](meextendedtype.md)，並提供定義自訂事件的方式。</span><span class="sxs-lookup"><span data-stu-id="7a04e-128">This method applies to the [MEExtendedType Event](meextendedtype.md), and provides a way to define custom events.</span></span>

<span data-ttu-id="7a04e-129">[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)介面也會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面。</span><span class="sxs-lookup"><span data-stu-id="7a04e-129">The [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface also inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="7a04e-130">有些事件會以屬性形式傳送其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7a04e-130">Some events carry additional information as attributes.</span></span>

<span data-ttu-id="7a04e-131">如需事件種類及其相關資料和屬性的清單，請參閱 [媒體基礎事件](media-foundation-events.md)。</span><span class="sxs-lookup"><span data-stu-id="7a04e-131">For a list of event types and their associated data and attributes, see [Media Foundation Events](media-foundation-events.md).</span></span>

## <a name="implementing-imfmediaeventgenerator"></a><span data-ttu-id="7a04e-132">執行 IMFMediaEventGenerator</span><span class="sxs-lookup"><span data-stu-id="7a04e-132">Implementing IMFMediaEventGenerator</span></span>

<span data-ttu-id="7a04e-133">如果您要撰寫媒體基礎的外掛程式元件，例如自訂媒體來源或媒體接收器，您可能需要執行 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)。</span><span class="sxs-lookup"><span data-stu-id="7a04e-133">If you are writing a plug-in component for Media Foundation, such as a custom media source or media sink, you might need to implement [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span></span> <span data-ttu-id="7a04e-134">為了簡化此作業，媒體基礎提供可執行事件佇列的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="7a04e-134">To make this easier, Media Foundation provides a helper object that implements an event queue.</span></span> <span data-ttu-id="7a04e-135">藉由呼叫 [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) 函數來建立事件佇列。</span><span class="sxs-lookup"><span data-stu-id="7a04e-135">Create the event queue by calling the [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) function.</span></span> <span data-ttu-id="7a04e-136">事件佇列會公開 [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) 介面。</span><span class="sxs-lookup"><span data-stu-id="7a04e-136">The event queue exposes the [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) interface.</span></span> <span data-ttu-id="7a04e-137">在物件的 **IMFMediaEventGenerator** 方法執行中，呼叫事件佇列上的對應方法。</span><span class="sxs-lookup"><span data-stu-id="7a04e-137">In your object's implementation of the **IMFMediaEventGenerator** methods, call the corresponding method on the event queue.</span></span>

<span data-ttu-id="7a04e-138">事件佇列物件是安全線程。</span><span class="sxs-lookup"><span data-stu-id="7a04e-138">The event queue object is thread safe.</span></span> <span data-ttu-id="7a04e-139">呼叫 [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) 和 [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent)時，永遠不會保留相同的重要區段物件，因為 **GetEvent** 可能會無限期地封鎖等候 [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)。</span><span class="sxs-lookup"><span data-stu-id="7a04e-139">Never hold the same critical section object when calling [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) and [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), because **GetEvent** might block indefinitely waiting for [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span></span> <span data-ttu-id="7a04e-140">如果這兩種方法都有相同的重要區段，則會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="7a04e-140">If you hold the same critical section for both methods, it will cause a deadlock.</span></span>

<span data-ttu-id="7a04e-141">釋放事件佇列之前，請呼叫 [**IMFMediaEventQueue：： Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) 釋放物件所保存的資源。</span><span class="sxs-lookup"><span data-stu-id="7a04e-141">Before releasing the event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) to release the resources that the object holds.</span></span>

<span data-ttu-id="7a04e-142">當您的物件需要引發事件時，請在事件佇列上呼叫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="7a04e-142">When your object needs to raise an event, call one of the following methods on the event queue:</span></span>

-   [<span data-ttu-id="7a04e-143">**IMFMediaEventQueue::QueueEvent**</span><span class="sxs-lookup"><span data-stu-id="7a04e-143">**IMFMediaEventQueue::QueueEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [<span data-ttu-id="7a04e-144">**IMFMediaEventQueue::QueueEventParamVar**</span><span class="sxs-lookup"><span data-stu-id="7a04e-144">**IMFMediaEventQueue::QueueEventParamVar**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [<span data-ttu-id="7a04e-145">**IMFMediaEventQueue::QueueEventParamUnk**</span><span class="sxs-lookup"><span data-stu-id="7a04e-145">**IMFMediaEventQueue::QueueEventParamUnk**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

<span data-ttu-id="7a04e-146">這些方法會將新的事件放在佇列上，併發出等候下一個事件的任何呼叫端。</span><span class="sxs-lookup"><span data-stu-id="7a04e-146">These methods put a new event on the queue and signal any caller that is waiting for the next event.</span></span>

<span data-ttu-id="7a04e-147">下列程式碼顯示使用這個 helper 物件來執行 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 的類別。</span><span class="sxs-lookup"><span data-stu-id="7a04e-147">The following code shows a class that implements [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) using this helper object.</span></span> <span data-ttu-id="7a04e-148">這個類別會定義公開 **關機** 方法，以關閉事件佇列並釋放事件佇列指標。</span><span class="sxs-lookup"><span data-stu-id="7a04e-148">This class defines a public **Shutdown** method that shuts down the event queue and releases the event queue pointer.</span></span> <span data-ttu-id="7a04e-149">此行為對於媒體來源和媒體接收器（一律具有 **關機** 方法）而言是正常的。</span><span class="sxs-lookup"><span data-stu-id="7a04e-149">This behavior would be typical for media sources and media sinks, which always have a **Shutdown** method.</span></span>


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a><span data-ttu-id="7a04e-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a04e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a04e-151">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="7a04e-151">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



