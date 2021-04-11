---
description: DirectShow 中的多重通道 WMA 音訊播放
ms.assetid: 99c69290-545a-4368-8f51-74e547c9466d
title: DirectShow 中的多重通道 WMA 音訊播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400ee9f0cede6c7268bcd3632365db1b423d114e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317727"
---
# <a name="multichannel-wma-audio-playback-in-directshow"></a><span data-ttu-id="14486-103">DirectShow 中的多重通道 WMA 音訊播放</span><span class="sxs-lookup"><span data-stu-id="14486-103">Multichannel WMA Audio Playback in DirectShow</span></span>

<span data-ttu-id="14486-104">若要在 DirectShow 中播放多重通道 Windows Media 音訊檔案，您必須在將 **MFPKEY \_ WMADEC \_ HIRESOUTPUT** 屬性連接到 WM ASF 讀取器之後，直接在該解碼器上設定它。</span><span class="sxs-lookup"><span data-stu-id="14486-104">To play back a multichannel Windows Media Audio file in DirectShow, you must set the **MFPKEY\_WMADEC\_HIRESOUTPUT** property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="14486-105">這個屬性是在標頭檔 wmcodecdsp 中定義，在 Windows SDK 中提供。</span><span class="sxs-lookup"><span data-stu-id="14486-105">This property is defined in the header file wmcodecdsp.h, which is available in the Windows SDK.</span></span>

> [!Note]  
> <span data-ttu-id="14486-106">只有未受數位 Rights Management 保護的檔案才支援此設定程式。</span><span class="sxs-lookup"><span data-stu-id="14486-106">This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

 

<span data-ttu-id="14486-107">啟用多重通道輸出的基本步驟如下：</span><span class="sxs-lookup"><span data-stu-id="14486-107">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="14486-108">呼叫 **RenderFile** 以建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="14486-108">Call **RenderFile** to create the filter graph.</span></span>
2.  <span data-ttu-id="14486-109">取得 SQL-DMO 包裝函式篩選的指標。</span><span class="sxs-lookup"><span data-stu-id="14486-109">Obtain a pointer to the DMO Wrapper filter.</span></span>
3.  <span data-ttu-id="14486-110">從音訊轉譯器中斷連接的中的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="14486-110">Disconnect the DMO Wrapper from the Audio Renderer.</span></span>
4.  <span data-ttu-id="14486-111">您可以使用 **IPropertyBag** 介面來設定解碼器上的 **MFPKEY \_ WMADEC \_ HIRESOUTPUT** 屬性。</span><span class="sxs-lookup"><span data-stu-id="14486-111">Use the **IPropertyBag** interface to set the **MFPKEY\_WMADEC\_HIRESOUTPUT** property on the decoder.</span></span> <span data-ttu-id="14486-112">屬性名稱是由全域常數 **g \_ wszWMACHiResOutput** 所定義。</span><span class="sxs-lookup"><span data-stu-id="14486-112">The property name is defined by the global constant **g\_wszWMACHiResOutput**.</span></span>
5.  <span data-ttu-id="14486-113">重新連接 SQL-DMO 包裝函式和音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="14486-113">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="14486-114">執行圖形。</span><span class="sxs-lookup"><span data-stu-id="14486-114">Run the graph.</span></span>

<span data-ttu-id="14486-115">下列程式碼片段示範這些步驟。</span><span class="sxs-lookup"><span data-stu-id="14486-115">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="14486-116">這段程式碼假設來源檔案包含音訊資料流程，而沒有影片串流。</span><span class="sxs-lookup"><span data-stu-id="14486-116">This code assumes that the source file contains an audio stream and no video stream.</span></span> <span data-ttu-id="14486-117">Video 編解碼器 SQL-DMO 不支援 **MFPKEY \_ WMADEC \_ HIRESOUTPUT** 屬性。</span><span class="sxs-lookup"><span data-stu-id="14486-117">The video codec DMO does not support the **MFPKEY\_WMADEC\_HIRESOUTPUT** property.</span></span>


```C++
HRESULT BuildGraph(IGraphBuilder *pGraph, const WCHAR *wFileName)
{
    HRESULT hr = S_OK;
    IBaseFilter       *pDmoWrapper = NULL;
    IPin              *pDmoOut = NULL;
    IPin              *pRendererIn = NULL;
    IPropertyBag      *pPropBag = NULL;

    hr = pGraph->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    if (SUCCEEDED(hr))
    {
        hr = GetDMOWrapper(pGraph, &pDmoWrapper); 
    }

    //Disconnect the DMO Wrapper from the Audio Renderer.
    if (SUCCEEDED(hr))
    {
        hr = GetPin(pDmoWrapper, PINDIR_OUTPUT, &pDmoOut);
    }
    if (SUCCEEDED(hr))
    {
        hr = DisconnectPin(pGraph, pDmoOut, &pRendererIn);
    }

    //Set the property on the DMO.
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;

    if (SUCCEEDED(hr))
    {
        hr = pDmoWrapper->QueryInterface(IID_IPropertyBag, (void**)&pPropBag);
    }
    if (SUCCEEDED(hr))
    {
        hr = pPropBag->Write(g_wszWMACHiResOutput, &varg);
    }

    // Reconnect the DMO Wrapper and the Audio Renderer
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Connect(pDmoOut, pRendererIn);
    }

    SAFE_RELEASE(pDmoWrapper);
    SAFE_RELEASE(pDmoOut);
    SAFE_RELEASE(pRendererIn);
    SAFE_RELEASE(pPropBag);
    return hr;
}
```



<span data-ttu-id="14486-118">上述程式碼片段中的 helper 函式會依照下列方式執行：</span><span class="sxs-lookup"><span data-stu-id="14486-118">The helper functions from the previous code snippet are implemented as follows:</span></span>


```C++
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** ppFilter) 
{
    BOOL bFound = FALSE;

    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter = NULL;
    IDMOWrapperFilter *pWrapper = NULL;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pFilter, NULL) == S_OK)
        {
            // If we find the IDMOWrapperFilter interface, that means we 
            // have the DMO Wrapper filter. 
            hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
            if (SUCCEEDED(hr))
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pFilter);
        }
    }

    if (bFound)
    {
        *ppFilter = pFilter;
        (*ppFilter)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pEnum);
    SAFE_RELEASE(pFilter);
    SAFE_RELEASE(pWrapper);
    return hr;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    BOOL bFound = FALSE;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pPin, 0) == S_OK)
        {
            PIN_DIRECTION PinDirThis;
            hr = pPin->QueryDirection(&PinDirThis);
            if (FAILED(hr))
            {
                break;
            }
            if (PinDir == PinDirThis)
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pPin);
        }
    }

    if (bFound)
    {
        *ppPin = pPin;
        (*ppPin)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pPin);
    SAFE_RELEASE(pEnum);
    return hr;
}

HRESULT DisconnectPin(IGraphBuilder *pGraph, IPin *pPin, IPin **ppConnected)
{
    IPin *pConnected = NULL;

    HRESULT hr = pPin->ConnectedTo(&pConnected);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pPin);
    }
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pConnected);
    }
    if (SUCCEEDED(hr))
    {
        *ppConnected = pConnected;
        (*ppConnected)->AddRef();
    }

    SAFE_RELEASE(pConnected);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="14486-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="14486-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14486-120">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="14486-120">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



