---
description: 本主題說明如何使用 DirectShow 播放以 Windows Media 數位 Rights Management (DRM) 保護的媒體檔案。
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: 在 DirectShow 中讀取 DRM-Protected 的 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997319"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>在 DirectShow 中讀取 DRM-Protected 的 ASF 檔案

本主題說明如何使用 DirectShow 播放以 Windows Media 數位 Rights Management (DRM) 保護的媒體檔案。

## <a name="drm-concepts"></a>DRM 概念

使用 Windows Media DRM 保護媒體檔案牽涉到兩個不同的步驟：

-   內容提供者會封裝檔案，也就是加密檔案並將授權資訊附加至 ASF 檔案標頭。 授權資訊包括用戶端可以取得授權的 URL。
-   用戶端應用程式會取得內容的授權。

封裝會在散發檔案之前進行。 當使用者嘗試播放或複製檔案時，就會取得授權。 授權取得可能是 *無* 訊息或 *非無* 訊息。 無訊息捕獲不需要與使用者進行任何互動。 非無訊息取得需要應用程式開啟瀏覽器視窗，並向使用者顯示網頁。 屆時，使用者可能需要為內容提供者提供一種資訊。 不過，這兩種授權類型都需要用戶端向授權伺服器提交 HTTP 要求。

### <a name="drm-versions"></a>DRM 版本

有數種版本的 Windows Media DRM 存在。 從用戶端應用程式的觀點來看，它們可以分為兩類： DRM 第1版，以及 DRM 7 版或更新版本。  (第二個類別包含 DRM 9 和10版，以及第7版。 ) 以這種方式分類 DRM 版本的原因，是因為第1版的授權處理方式與7版或更新版本的授權稍有不同。 在此檔中， *第7版授權* 表示第7版或更新版本。

區分 drm 封裝與 DRM 授權也很重要。 如果是使用 Windows Media Rights Manager 7 版或更新版本來封裝檔案，DRM 標頭除了第7版授權 URL 之外，還可以包含第1版授權 URL。 第1版授權 URL 可讓不支援第7版的舊版播放程式取得內容的授權。 不過，反向並不是正確的，因此第1版封裝的檔案不能有第7版授權 URL。

### <a name="application-security-level"></a>應用程式安全性層級

若要播放受 DRM 保護的檔案，用戶端應用程式必須連結至 Microsoft 以二進位格式提供的靜態程式庫。 此程式庫可唯一識別應用程式，有時稱為存根程式庫。 存根程式庫具有指派的安全性層級，其值取決於您取得存根程式庫時簽署的授權合約。

內容提供者會設定取得授權所需的最低安全性層級。 如果存根程式庫的安全性層級小於授權伺服器所需的最低安全性層級，則應用程式無法取得授權。

### <a name="individualization"></a>個人化

為了提高安全性，應用程式可能會更新用戶端電腦上的 DRM 元件。 這個稱為「個人化」的更新，會區分使用者的應用程式複本與相同應用程式的所有其他複本。 受保護檔案的 DRM 標頭可能會指定最小的個人化層級。  (需詳細資訊，請參閱 Windows Media Rights Manager SDK 中的 WMRMHeader IndividualizedVersion 檔。 ) 

由於 Microsoft 個人級服務會處理來自使用者的資訊，因此您必須在應用程式 individualizes 之前，顯示 Microsoft 網站上的 Microsoft 隱私權原則或提供該頁面的連結： <https://go.microsoft.com/fwlink/p/?linkid=10240> 。

## <a name="provide-the-software-certificate"></a>提供軟體憑證

若要讓應用程式使用 DRM 授權，應用程式必須提供軟體憑證或 *金鑰* 給篩選圖形管理員。 此索引鍵包含在為應用程式個人化的靜態程式庫中。 如需取得個別程式庫的詳細資訊，請參閱 Windows Media Format SDK 檔中的 [取得必要的 DRM 程式庫](../wmformat/obtaining-the-required-drm-library.md) 。

若要提供軟體金鑰，請執行下列步驟：

1.  靜態程式庫的連結。
2.  執行 **IServiceProvider** 介面。
3.  查詢 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) 介面的篩選圖形管理員。
4.  使用 **IServiceProvider 的** 指標來呼叫 [**IObjectWithSite：： SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 。
5.  篩選圖形管理員會呼叫 **IServiceProvider：： QueryService**，並為服務識別碼指定 **IID \_ IWMReader** 。
6.  在 **QueryService** 的執行中，呼叫 [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) 以建立軟體金鑰。

下列程式碼顯示如何執行 **QueryService** 方法：


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



下列程式碼顯示如何在篩選圖形管理員上呼叫 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) ：


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a>建立播放圖表

若要播放受 DRM 保護的 ASF 檔案，請執行下列步驟：

1.  建立 [篩選圖形管理員](filter-graph-manager.md) ，並使用 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面註冊圖形事件。
2.  呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器的新實例。
3.  呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將篩選準則加入至篩選圖形。
4.  查詢 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) 介面的篩選準則。
5.  以檔案的 URL 呼叫 [**IFileSourceFilter：： Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) 。
6.  處理 [**EC \_ WMT \_ 事件**](ec-wmt-event.md) 事件。
7.  在第一個 [**EC \_ WMT \_ 事件**](ec-wmt-event.md)事件上，查詢 **IServiceProvider** 介面的 [WM ASF 讀取](wm-asf-reader-filter.md)器篩選器。
8.  呼叫 **IServiceProvider：： QueryService** 來取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) 介面的指標。
9.  呼叫 [**IGraphBuilder：： render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 以轉譯 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器的輸出圖釘。

> [!Note]  
> 開啟受 DRM 保護的檔案時，請勿呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 來建立篩選圖形。 在取得 DRM 授權之前，「WM ASF 讀取器」篩選器無法連線到任何其他篩選器。 此步驟需要應用程式使用 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) 介面（必須從篩選中取得），如步驟7–8所述。 因此，您必須建立篩選器，並將它新增至圖形

 

> [!Note]  
> 在將 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器新增至圖形 (步驟 3) 之前，請務必 (步驟 1) 註冊圖形事件，因為應用程式必須處理 [**EC \_ WMT \_ 事件**](ec-wmt-event.md) 事件。 呼叫 [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) 時，會傳送事件 (步驟 5) 。

 

下列程式碼顯示如何建立圖形：


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



在先前的程式碼中，此函式會 `RenderOutputPins` 列舉 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器上的輸出圖釘，並針對每個 pin 呼叫 [**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 。


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



下列程式碼說明如何從 [WM ASF 讀取器](wm-asf-reader-filter.md)取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)介面的指標：


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
