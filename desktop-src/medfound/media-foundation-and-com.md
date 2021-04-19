---
description: Microsoft 媒體基礎使用混合的 COM 結構，但不是以 COM 為基礎的完整 API。
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: 媒體基礎和 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975602"
---
# <a name="media-foundation-and-com"></a>媒體基礎和 COM

Microsoft 媒體基礎使用混合的 COM 結構，但不是以 COM 為基礎的完整 API。 本主題說明 COM 與媒體基礎之間的互動。 它也會定義開發媒體基礎外掛程式元件的一些最佳作法。 遵循這些做法可協助您避免一些常見但微妙的程式設計錯誤。

-   [應用程式的最佳作法](#best-practices-for-applications)
-   [媒體基礎元件的最佳作法](#best-practices-for-media-foundation-components)
-   [總結](#summary)
-   [相關主題](#related-topics)

## <a name="best-practices-for-applications"></a>應用程式的最佳作法

在媒體基礎中， [工作佇列](work-queues.md)會處理非同步處理和回呼。 工作佇列一律會有多執行緒的單元 (MTA) 執行緒，因此，如果應用程式也在 MTA 執行緒上執行，則會有更簡單的執行。 因此，建議使用 **COINIT \_ 多執行緒** 旗標來呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 。

媒體基礎不會將單一執行緒的單元 (STA) 物件封送處理至工作佇列執行緒。 也不會確保不會維護 STA 變異。 因此，STA 應用程式必須小心不要將 STA 物件或 proxy 傳遞給媒體基礎 Api。 媒體基礎中不支援僅限 STA 的物件。

如果您有 MTA 或無限制執行緒物件的 STA proxy，則可以使用工作佇列回呼將物件封送處理至 MTA proxy。 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函數可以傳回原始指標或 STA proxy，視該 CLSID 的登錄中定義的物件模型而定。 如果傳回 STA proxy，您就不能將指標傳遞至媒體基礎 API。

例如，假設您想要將 **IPropertyStore** 指標傳遞至 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) 方法。 您可以呼叫 **PSCreateMemoryPropertyStore** 來建立 **IPropertyStore** 指標。 如果您是從 STA 呼叫，則必須先封送處理指標，再將它傳遞給 **BeginCreateObjectFromURL**。

下列程式碼說明如何將 STA proxy 封送處理至媒體基礎 API。


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



如需全域介面表的詳細資訊，請參閱 [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable)。

如果您使用媒體基礎同進程，從媒體基礎方法和函式傳回的物件就是物件的直接指標。 若為跨進程媒體基礎，這些物件可能是 MTA proxy，如果需要，則應該封送處理至 STA 執行緒。 同樣地，在回呼中取得的物件（例如，來自 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件的拓撲）是在同進程中使用媒體基礎時的直接指標，而當使用媒體基礎的跨進程時，則是 MTA proxy。

> [!Note]  
> 使用媒體基礎跨進程的最常見案例是使用 [受保護的媒體路徑](protected-media-path.md) (PMP) 。 不過，這些備註適用于透過 RPC 使用媒體基礎 Api 時的任何情況。

 

[**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)的所有實施都應與 MTA 相容。 這些物件完全不需要是 COM 物件。 但如果是，則無法在 STA 中執行。 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)函式將會在 MTA workqueue 執行緒上叫用，而提供的 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)物件將會是直接物件指標或 MTA proxy。

## <a name="best-practices-for-media-foundation-components"></a>媒體基礎元件的最佳作法

有兩個類別的媒體基礎物件需要考慮 COM。 某些元件（例如轉換或位元組資料流程處理常式）是 CLSID 所建立的完整 COM 物件。 這些物件必須遵循 COM 單元的規則，同時適用于同進程和跨進程的媒體基礎。 其他媒體基礎元件並非完整的 COM 物件，但需要 COM proxy 才能進行跨進程播放。 此類別中的物件包含媒體來源和啟用物件。 如果這些物件只會用於同進程媒體基礎，這些物件可能會忽略這些問題。

雖然並非所有媒體基礎物件都是 COM 物件，但所有媒體基礎介面都是衍生自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)。 因此，所有媒體基礎物件都必須根據 COM 規格來執行 **IUnknown** ，包括參考計數和 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的規則。 所有參考計數的物件也應該確保在物件仍然存在時， [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) 不會允許卸載模組。

媒體基礎的元件不能是 STA 物件。 許多媒體基礎物件都不需要是 COM 物件。 但如果是，則無法在 STA 中執行。 所有媒體基礎元件都必須是安全線程。 某些媒體基礎的物件也必須是無限制執行緒或非中立的。 下表指定自訂介面的需求：



| 介面                                                          | 類別            | 必要的單元       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | 跨進程 proxy | 無限制執行緒或中立 |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | COM 物件          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | 跨進程 proxy | 無限制執行緒或中立 |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | COM 物件          | 無限制執行緒或中立 |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | 跨進程 proxy | 無限制執行緒或中立 |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | COM 物件          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | COM 物件          | 無限制執行緒或中立 |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | COM 物件          | MTA                      |



 

視執行而定，可能會有其他需求。 例如，如果媒體接收器所執行的另一個介面可讓應用程式對接收器進行直接函式呼叫，則接收器必須是無限制執行緒或中性，才能處理直接的跨進程呼叫。 任何物件都可以自由執行緒;下表指定最低需求。

執行無限制執行緒或中性物件的建議方式，是藉由匯總無限制執行緒封送處理器。 如需詳細資訊，請參閱 [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)上的 MSDN 檔。 根據不需要將 STA 物件或 proxy 傳遞給媒體基礎 Api 的需求，無限制執行緒的物件不需要擔心在自由執行緒元件中封送處理 STA 輸入指標。

使用長期函式工作佇列 (**MFASYNC \_ 回呼 \_ 佇列 \_ 長期 \_** 函式的元件) 必須更小心。 Long 函數中的執行緒 workqueue 建立自己的 STA。 使用 long 函式 workqueue 回呼的元件應避免在這些執行緒上建立 COM 物件，並視需要小心將 proxy 封送處理至 STA。

## <a name="summary"></a>總結

如果應用程式與來自 MTA 執行緒的媒體基礎互動，則應用程式會有更多的時間，但是使用來自 STA 執行緒的媒體基礎可能會有一些小心。 媒體基礎不會處理 STA 元件，而且應用程式應該小心不要將 STA 物件傳遞給媒體基礎 Api。 有些物件有額外的需求，特別是在跨進程的情況下執行的物件。 遵循這些指導方針將有助於避免發生 COM 錯誤、鎖死和非預期的媒體處理延遲。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> <dt>

[媒體基礎架構](media-foundation-architecture.md)
</dt> </dl>

 

 
