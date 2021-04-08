---
description: 如何從網路來源取得事件
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: 如何從網路來源取得事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691468"
---
# <a name="how-to-get-events-from-the-network-source"></a><span data-ttu-id="d5198-103">如何從網路來源取得事件</span><span class="sxs-lookup"><span data-stu-id="d5198-103">How to Get Events from the Network Source</span></span>

<span data-ttu-id="d5198-104">來源解析程式可讓應用程式建立網路來源，並開啟特定 URL 的連接。</span><span class="sxs-lookup"><span data-stu-id="d5198-104">The source resolver enables an application to create a network source and open a connection to a specific URL.</span></span> <span data-ttu-id="d5198-105">網路來源會引發事件，以標示開啟連接之非同步作業的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="d5198-105">The network source raises events to mark the beginning and the end of the asynchronous operation of opening a connection.</span></span> <span data-ttu-id="d5198-106">應用程式可以使用 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面來註冊這些事件。</span><span class="sxs-lookup"><span data-stu-id="d5198-106">An application can register for these events by using the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>

<span data-ttu-id="d5198-107">此介面會公開 [**IMFSourceOpenMonitor：： OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) 方法，當網路來源以非同步方式開啟 URL 時，會直接呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="d5198-107">This interface exposes the [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method that the network source calls directly when it opens the URL asynchronously.</span></span> <span data-ttu-id="d5198-108">網路來源會在應用程式開始開啟 URL 時，藉由引發 [MEConnectStart](meconnectstart.md) 事件來通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5198-108">The network source notifies the application when it starts opening the URL by raising the [MEConnectStart](meconnectstart.md) event.</span></span> <span data-ttu-id="d5198-109">然後，當網路來源完成開啟作業時，就會引發 [MEConnectEnd](meconnectend.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d5198-109">The network source then raises the [MEConnectEnd](meconnectend.md) event when it completes the open operation.</span></span>

> [!Note]  
> <span data-ttu-id="d5198-110">為了將這些事件傳送至應用程式，網路來源不會使用 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面，因為系統會在建立網路來源之前引發這些事件。</span><span class="sxs-lookup"><span data-stu-id="d5198-110">To send these events to the application, the network source does not use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface because these events are raised before the network source is created.</span></span> <span data-ttu-id="d5198-111">應用程式可以使用媒體會話的 **IMFMediaEventGenerator** 介面來取得所有其他網路來源事件。</span><span class="sxs-lookup"><span data-stu-id="d5198-111">The application can get all other network source events by using the Media Session's **IMFMediaEventGenerator** interface.</span></span>

 

## <a name="to-get-events-from-the-network-source"></a><span data-ttu-id="d5198-112">從網路來源取得事件</span><span class="sxs-lookup"><span data-stu-id="d5198-112">To get events from the network source</span></span>

1.  <span data-ttu-id="d5198-113">執行 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面。</span><span class="sxs-lookup"><span data-stu-id="d5198-113">Implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span> <span data-ttu-id="d5198-114">在 [**IMFSourceOpenMonitor：： OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) 方法的執行中，執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d5198-114">In your implementation of [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, do the following:</span></span>
    1.  <span data-ttu-id="d5198-115">藉由呼叫 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)來取得事件狀態。</span><span class="sxs-lookup"><span data-stu-id="d5198-115">Get the event status by calling [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span></span> <span data-ttu-id="d5198-116">這個方法會指出觸發事件的作業是否成功，例如來源解析程式方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="d5198-116">This method indicates whether the operation that triggered the event, such as a source resolver method call, succeeded.</span></span> <span data-ttu-id="d5198-117">如果作業不成功，則狀態為失敗碼。</span><span class="sxs-lookup"><span data-stu-id="d5198-117">If the operation is not successful, the status is a failure code.</span></span>
    2.  <span data-ttu-id="d5198-118">根據事件種類來處理事件： [MEConnectStart](meconnectstart.md) 或 [MEConnectEnd](meconnectend.md)，應用程式可以藉由呼叫 [**IMFMediaEvent：： GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)來取得該事件。</span><span class="sxs-lookup"><span data-stu-id="d5198-118">Process the event based on the event type: [MEConnectStart](meconnectstart.md) or [MEConnectEnd](meconnectend.md), which the application can get by calling [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span></span>
2.  <span data-ttu-id="d5198-119">設定屬性存放區物件中的索引鍵/值組，將指標儲存至步驟1中所述的 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 執行。</span><span class="sxs-lookup"><span data-stu-id="d5198-119">Configure a key-value pair in a property store object to store a pointer to the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementation described in step 1.</span></span>
    1.  <span data-ttu-id="d5198-120">藉由呼叫 **PSCreateMemoryPropertyStore** 函數來建立屬性存放區物件。</span><span class="sxs-lookup"><span data-stu-id="d5198-120">Create a property store object by calling the **PSCreateMemoryPropertyStore** function.</span></span>
    2.  <span data-ttu-id="d5198-121">在 **PROPERTYKEY** 結構中設定 [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="d5198-121">Set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property in a **PROPERTYKEY** structure.</span></span>
    3.  <span data-ttu-id="d5198-122">藉 \_ 由將 **IUnknown** 指標設定為應用程式 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)介面的執行，在 **PROPVARIANT** 結構中提供 VT 未知的類型資料值。</span><span class="sxs-lookup"><span data-stu-id="d5198-122">Provide the VT\_UNKNOWN type data value in a **PROPVARIANT** structure by setting the **IUnknown** pointer to the application's implementation of the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>
    4.  <span data-ttu-id="d5198-123">藉由呼叫 **IPropertyStore：： SetValue**，在屬性存放區中設定機碼值組。</span><span class="sxs-lookup"><span data-stu-id="d5198-123">Set the key-value pair in the property store by calling **IPropertyStore::SetValue**.</span></span>
3.  <span data-ttu-id="d5198-124">將屬性存放區指標傳遞至應用程式用來建立網路來源的來源解析程式方法，例如 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 及其他。</span><span class="sxs-lookup"><span data-stu-id="d5198-124">Pass the property store pointer to the source resolver methods that the application is using to create the network source, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) and others.</span></span>

## <a name="example"></a><span data-ttu-id="d5198-125">範例</span><span class="sxs-lookup"><span data-stu-id="d5198-125">Example</span></span>

<span data-ttu-id="d5198-126">下列範例顯示如何執行 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面，以從網路來源取得事件。</span><span class="sxs-lookup"><span data-stu-id="d5198-126">The following example shows how to implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface to get events from the network source.</span></span>


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



<span data-ttu-id="d5198-127">下列範例顯示當您開啟 URL 時，如何在網路來源上設定 [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) 屬性：</span><span class="sxs-lookup"><span data-stu-id="d5198-127">The following example shows how to set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property on the network source when you open the URL:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d5198-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5198-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5198-129">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="d5198-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



