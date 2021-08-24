---
description: 媒體事件產生器
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: 媒體事件產生器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24bd37b347fb06f97448b43241a1da40123195b63b9191b97581be60d7378ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724158"
---
# <a name="media-event-generators"></a>媒體事件產生器

媒體基礎為物件提供一致的方式來傳送事件。 物件可以使用事件來指示非同步方法的完成，或通知應用程式有關物件狀態的變更。

如果物件傳送事件，它會公開 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面。 每當物件傳送新事件時，該事件就會放置在佇列中。 應用程式可以藉由呼叫下列其中一種方法，從佇列要求下一個事件：

-   [**IMFMediaEventGenerator::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

[**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)方法是同步的。 如果事件已在佇列中，則此方法會立即傳回。 如果佇列中沒有任何事件，則方法會立即失敗，或封鎖直到下一個事件排入佇列，視您傳遞至 **GetEvent** 的旗標而定。

[**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)方法是非同步，因此永遠不會封鎖。 這個方法會採用應用程式必須執行之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標。 叫用回呼時，應用程式會呼叫 [**IMFMediaEventGenerator：： EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) 以從佇列取得事件。 如需 **IMFAsyncCallback** 的詳細資訊，請參閱 [非同步回呼方法](asynchronous-callback-methods.md)。

事件是由 [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) 介面表示。 此介面有下列方法：

-   [**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)：抓取事件種類。 事件種類表示觸發事件發生的狀況。

-   [**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)：抓取 **HRESULT** 值，指出觸發事件的作業是否成功。 如果非同步作業失敗， **GetStatus** 會傳回失敗碼。

-   [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)：抓取包含事件資料的 **PROPVARIANT** 。 事件資料取決於事件種類。 某些事件沒有任何資料。

-   [**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)：抓取 **GUID**。 這個方法會套用至 [MEExtendedType 事件](meextendedtype.md)，並提供定義自訂事件的方式。

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)介面也會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面。 有些事件會以屬性形式傳送其他資訊。

如需事件種類及其相關資料和屬性的清單，請參閱 [媒體基礎事件](media-foundation-events.md)。

## <a name="implementing-imfmediaeventgenerator"></a>執行 IMFMediaEventGenerator

如果您要撰寫媒體基礎的外掛程式元件，例如自訂媒體來源或媒體接收器，您可能需要執行 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)。 為了簡化此作業，媒體基礎提供可執行事件佇列的 helper 物件。 藉由呼叫 [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) 函數來建立事件佇列。 事件佇列會公開 [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) 介面。 在物件的 **IMFMediaEventGenerator** 方法執行中，呼叫事件佇列上的對應方法。

事件佇列物件是安全線程。 呼叫 [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) 和 [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent)時，永遠不會保留相同的重要區段物件，因為 **GetEvent** 可能會無限期地封鎖等候 [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)。 如果這兩種方法都有相同的重要區段，則會造成鎖死。

釋放事件佇列之前，請呼叫 [**IMFMediaEventQueue：： Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) 釋放物件所保存的資源。

當您的物件需要引發事件時，請在事件佇列上呼叫下列其中一種方法：

-   [**IMFMediaEventQueue::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**IMFMediaEventQueue::QueueEventParamVar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**IMFMediaEventQueue::QueueEventParamUnk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

這些方法會將新的事件放在佇列上，併發出等候下一個事件的任何呼叫端。

下列程式碼顯示使用這個 helper 物件來執行 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 的類別。 這個類別會定義公開 **關機** 方法，以關閉事件佇列並釋放事件佇列指標。 此行為對於媒體來源和媒體接收器（一律具有 **關機** 方法）而言是正常的。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 



