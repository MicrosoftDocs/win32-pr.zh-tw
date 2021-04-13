---
title: DirectShow 中的多頻道音訊播放
description: DirectShow 中的多頻道音訊播放
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，多頻道音訊播放
- Windows Media Format SDK，音訊播放
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、多頻道音訊播放
- ASF (Advanced Systems Format) 、多頻道音訊播放
- Advanced Systems Format (ASF) 、音訊播放
- ASF (Advanced 系統格式) 、音訊播放
- DirectShow、多頻道音訊播放
- DirectShow、音訊播放
- 多頻道音訊，播放
- 音訊播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c6eec473c8bbbff81d35f4127d5d132d0b6cd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374594"
---
# <a name="multichannel-audio-playback-in-directshow"></a><span data-ttu-id="66a75-116">DirectShow 中的多頻道音訊播放</span><span class="sxs-lookup"><span data-stu-id="66a75-116">Multichannel Audio Playback in DirectShow</span></span>

<span data-ttu-id="66a75-117">若要在 DirectShow 中播放多重通道 Windows Media 音訊檔案，您必須在已 \_ 連接到 WM ASF 讀取器之後，直接在此解碼器上設定 "HIRESOUTPUT" 屬性。</span><span class="sxs-lookup"><span data-stu-id="66a75-117">To play back a multichannel Windows Media Audio file in DirectShow, you must set the "\_HIRESOUTPUT" property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="66a75-118">不需要設定 Reader 物件。</span><span class="sxs-lookup"><span data-stu-id="66a75-118">No configuration of the Reader Object is necessary.</span></span> <span data-ttu-id="66a75-119">不過，若要直接使用 SQL-DMO，您需要範例程式碼中的 wmcodecconst，才能 [使用 Windows Media 音訊和影片編解碼器介面](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) 下載套件。</span><span class="sxs-lookup"><span data-stu-id="66a75-119">However, to work with the DMO directly, you need wmcodecconst.h from the [Sample Code for Using the Windows Media Audio and Video Codec Interfaces](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) download package.</span></span>

<span data-ttu-id="66a75-120">**注意** 只有未受數位 Rights Management 保護的檔案才支援此設定程式。</span><span class="sxs-lookup"><span data-stu-id="66a75-120">**Note** This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

<span data-ttu-id="66a75-121">啟用多重通道輸出的基本步驟如下：</span><span class="sxs-lookup"><span data-stu-id="66a75-121">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="66a75-122">呼叫 RenderFile 以建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="66a75-122">Call RenderFile to create the filter graph.</span></span>
2.  <span data-ttu-id="66a75-123">取得 a 的 < i 包裝函式篩選準則指標</span><span class="sxs-lookup"><span data-stu-id="66a75-123">Obtain a pointer to the DMO Wrapper filter</span></span>
3.  <span data-ttu-id="66a75-124">從音訊轉譯器中斷連接的 i 包裝函式</span><span class="sxs-lookup"><span data-stu-id="66a75-124">Disconnect the DMO Wrapper from the Audio Renderer</span></span>
4.  <span data-ttu-id="66a75-125">在 \_ 解碼器上設定 "HIRESOUTPUT" 屬性。</span><span class="sxs-lookup"><span data-stu-id="66a75-125">Set the "\_HIRESOUTPUT" property on the decoder.</span></span>
5.  <span data-ttu-id="66a75-126">重新連接 SQL-DMO 包裝函式和音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="66a75-126">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="66a75-127">執行圖形。</span><span class="sxs-lookup"><span data-stu-id="66a75-127">Run the graph.</span></span>

<span data-ttu-id="66a75-128">下列程式碼片段示範這些步驟。</span><span class="sxs-lookup"><span data-stu-id="66a75-128">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="66a75-129"> (為了簡潔起見，已省略所有錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="66a75-129">(All error checking has been omitted for the sake of simplicity.</span></span> <span data-ttu-id="66a75-130">如果您在應用程式中使用此程式碼，您應該新增適當的錯誤處理常式。 ) </span><span class="sxs-lookup"><span data-stu-id="66a75-130">You should add proper error handling routines if you use this code in an application.)</span></span>


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



<span data-ttu-id="66a75-131">先前程式碼片段中的 GetDMOWrapper 和 GetPin 函式會依照下列方式執行：</span><span class="sxs-lookup"><span data-stu-id="66a75-131">The GetDMOWrapper and GetPin functions from the previous code snippet are implemented as follows:</span></span>


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




