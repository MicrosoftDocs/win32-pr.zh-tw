---
description: 如何從網路來源取得事件
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: 如何從網路來源取得事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec85877a928a2f63648ec0dedded1c383988bf80a4182f83062fd296e68bcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958318"
---
# <a name="how-to-get-events-from-the-network-source"></a>如何從網路來源取得事件

來源解析程式可讓應用程式建立網路來源，並開啟特定 URL 的連接。 網路來源會引發事件，以標示開啟連接之非同步作業的開頭和結尾。 應用程式可以使用 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面來註冊這些事件。

此介面會公開 [**IMFSourceOpenMonitor：： OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) 方法，當網路來源以非同步方式開啟 URL 時，會直接呼叫此方法。 網路來源會在應用程式開始開啟 URL 時，藉由引發 [MEConnectStart](meconnectstart.md) 事件來通知應用程式。 然後，當網路來源完成開啟作業時，就會引發 [MEConnectEnd](meconnectend.md) 事件。

> [!Note]  
> 為了將這些事件傳送至應用程式，網路來源不會使用 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面，因為系統會在建立網路來源之前引發這些事件。 應用程式可以使用媒體會話的 **IMFMediaEventGenerator** 介面來取得所有其他網路來源事件。

 

## <a name="to-get-events-from-the-network-source"></a>從網路來源取得事件

1.  執行 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面。 在 [**IMFSourceOpenMonitor：： OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) 方法的執行中，執行下列動作：
    1.  藉由呼叫 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)來取得事件狀態。 這個方法會指出觸發事件的作業是否成功，例如來源解析程式方法呼叫。 如果作業不成功，則狀態為失敗碼。
    2.  根據事件種類來處理事件： [MEConnectStart](meconnectstart.md) 或 [MEConnectEnd](meconnectend.md)，應用程式可以藉由呼叫 [**IMFMediaEvent：： GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)來取得該事件。
2.  設定屬性存放區物件中的索引鍵/值組，將指標儲存至步驟1中所述的 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 執行。
    1.  藉由呼叫 **PSCreateMemoryPropertyStore** 函數來建立屬性存放區物件。
    2.  在 **PROPERTYKEY** 結構中設定 [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md)屬性。
    3.  藉 \_ 由將 **IUnknown** 指標設定為應用程式 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)介面的執行，在 **PROPVARIANT** 結構中提供 VT 未知的類型資料值。
    4.  藉由呼叫 **IPropertyStore：： SetValue**，在屬性存放區中設定機碼值組。
3.  將屬性存放區指標傳遞至應用程式用來建立網路來源的來源解析程式方法，例如 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 及其他。

## <a name="example"></a>範例

下列範例顯示如何執行 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面，以從網路來源取得事件。


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



下列範例顯示當您開啟 URL 時，如何在網路來源上設定 [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) 屬性：


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 



