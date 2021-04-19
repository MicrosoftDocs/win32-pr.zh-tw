---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟4。
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 步驟4：新增影片轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992620"
---
# <a name="step-4-add-the-video-renderer"></a>步驟4：新增影片轉譯器

本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟4。 完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。

DirectShow 提供數種可轉譯影片的不同篩選：

-   [**增強的影片轉譯器篩選器**](enhanced-video-renderer-filter.md) (EVR) 
-   [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 
-   [影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) 

如需這些篩選之間差異的詳細資訊，請參閱 [選擇正確的影片](choosing-the-right-renderer.md)轉譯器。

在本教學課程中，每個影片轉譯器篩選都是由類別所包裝，以摘要它們之間的部分差異。 這些類別都是衍生自名為的抽象基類 `CVideoRenderer` 。 的宣告 `CVideoRenderer` 會在 [步驟2： Declare CVideoRenderer 和衍生類別](step-2--declare-cvideorenderer-and-derived-classes.md)中顯示。

下列方法會先嘗試依序建立每個影片轉譯器、EVR、VMR-9 和最後一個 VMR-7。


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a>EVR 篩選

下列程式碼會建立 EVR 篩選，並將其新增至篩選圖形。 `AddFilterByCLSID`此範例中使用的函式會顯示在主題[依 CLSID 新增篩選器](add-a-filter-by-clsid.md)中。


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



`InitializeEVR`函數會初始化 EVR 篩選。 此函式會執行下列步驟。

1.  查詢 [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) 介面的篩選準則。
2.  呼叫 [**IMFGetService：： GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) 介面的指標。
3.  呼叫 [**IMFVideoDisplayControl：： SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) 來設定影片視窗。
4.  呼叫 [**IMFVideoDisplayControl：： SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) 來設定 EVR，以保持影片的外觀比例。

下列程式碼顯示 `InitializeEVR` 函數。


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



建立圖表之後，會 `DShowPlayer::RenderStreams` 呼叫 `CVideoRenderer::FinalizeGraph` 。 這個方法會執行任何最終初始化或清除。 下列程式碼示範 `CEVR` 此方法的執行方式。


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



如果 EVR 未連接到任何其他篩選，這個方法會從圖形中移除 EVR。 如果媒體檔案未包含影片資料流程，就會發生這種情況。

### <a name="vmr-9-filter"></a>VMR-9 篩選

下列程式碼會建立 VMR 9 篩選器，並將它新增至篩選圖形。


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



此函 `InitWindowlessVMR9` 式會初始化無視窗模式的 VMR-9。  (如需無視窗模式的詳細資訊，請參閱 [VMR 無視窗模式](vmr-windowless-mode.md)。 ) 此函式會執行下列步驟。

1.  查詢 VMR-9 篩選器的 [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) 介面。
2.  呼叫 [**IVMRFilterConfig9：： SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) 方法來設定無視窗模式。
3.  查詢 VMR-9 篩選器的 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面。
4.  呼叫 [**IVMRWindowlessControl9：： SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) 方法來設定影片視窗。
5.  呼叫 [**IVMRWindowlessControl9：： SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) 方法以保存影片外觀比例。

下列程式碼顯示 `InitWindowlessVMR9` 函數。


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



`CVMR9::FinalizeGraph`方法會檢查 VMR-9 篩選是否已連接，如果不是，則會將它從篩選圖形中移除。


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a>VMR-7 篩選

VMR-7 篩選器的步驟幾乎與 VMR 9 的步驟相同，但會改用 VMR-7 介面。 下列程式碼會建立 VMR-7 篩選器，並將它新增至篩選圖形。


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



`InitWindowlessVMR`函數會初始化無視窗模式的 VMR-7。 此函式會執行下列步驟。

1.  查詢 [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) 介面的 VMR-7 篩選。
2.  呼叫 [**IVMRFilterConfig：： SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) 方法來設定無視窗模式。
3.  查詢 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面的 VMR-7 篩選。
4.  呼叫 [**IVMRWindowlessControl：： SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) 方法來設定影片視窗。
5.  呼叫 [**IVMRWindowlessControl：： SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) 方法以保存影片外觀比例。

下列程式碼顯示 `InitWindowlessVMR` 函數。


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



`CVMR7::FinalizeGraph`方法會檢查 VMR-7 篩選是否已連接，如果不是，則會將它從篩選圖形中移除。


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 播放範例](directshow-playback-example.md)
</dt> <dt>

[使用 DirectShow EVR 篩選器](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[使用影片混合轉譯器](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
