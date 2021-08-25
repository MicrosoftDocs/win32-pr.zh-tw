---
title: DirectShow 中的多頻道音訊播放
description: DirectShow 中的多頻道音訊播放
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows媒體格式 SDK，DirectShow
- Windows媒體格式 SDK，多頻道音訊播放
- Windows媒體格式 SDK，音訊播放
- Advanced Systems Format (ASF) ，DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、多頻道音訊播放
- ASF (Advanced Systems Format) 、多頻道音訊播放
- Advanced Systems Format (ASF) 、音訊播放
- ASF (Advanced 系統格式) 、音訊播放
- DirectShow，多頻道音訊播放
- DirectShow，音訊播放
- 多頻道音訊，播放
- 音訊播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99734ddf32be6e0340e26fafef0f22f1127ec3652cc0db0a9d2e94ce2f694b96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808158"
---
# <a name="multichannel-audio-playback-in-directshow"></a>DirectShow 中的多頻道音訊播放

若要在 DirectShow 中播放多重通道 Windows Media 音訊檔案，您必須在已 \_ 連接到 WM ASF 讀取器之後，直接在該解碼器上設定 "HIRESOUTPUT" 屬性。 不需要設定 Reader 物件。 不過，若要直接使用 DMO，您需要範例程式碼中的 wmcodecconst，[以使用 Windows Media 音訊和影片編解碼器介面](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en)下載套件。

**注意** 只有未受數位 Rights Management 保護的檔案才支援此設定程式。

啟用多重通道輸出的基本步驟如下：

1.  呼叫 RenderFile 以建立篩選圖形。
2.  取得 DMO 包裝函式篩選的指標
3.  中斷 DMO 包裝函式與音訊轉譯器的連線
4.  在 \_ 解碼器上設定 "HIRESOUTPUT" 屬性。
5.  重新連接 DMO 包裝函式和音訊轉譯器。
6.  執行圖形。

下列程式碼片段示範這些步驟。  (為了簡潔起見，已省略所有錯誤檢查。 如果您在應用程式中使用此程式碼，您應該新增適當的錯誤處理常式。 ) 


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



先前程式碼片段中的 GetDMOWrapper 和 GetPin 函式會依照下列方式執行：


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



 

 




