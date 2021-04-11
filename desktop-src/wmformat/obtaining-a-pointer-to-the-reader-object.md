---
title: '取得讀取器物件的指標 (Windows Media Format 11 SDK) '
description: 取得讀取器物件的指標
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media 格式 SDK，讀取器物件
- Windows Media Format SDK，IWMReaderAdvanced2 介面
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、reader 物件
- ASF (Advanced Systems Format) 、reader 物件
- Advanced Systems Format (ASF) ，IWMReaderAdvanced2 介面
- ASF (Advanced Systems Format) ，IWMReaderAdvanced2 介面
- DirectShow，讀取器物件
- DirectShow，讀取器物件的指標
- DirectShow、IWMReaderAdvanced2 介面
- 讀取器物件，取得指標
- 資料流程，讀取器物件
- 資料流程，讀取器物件的指標
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e0bb6611ba1d4e3c41fb2c00a68dd9c898505f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317019"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>取得讀取器物件的指標 (Windows Media Format 11 SDK) 

在某些情況下，例如，當您在指定的資料流程上設定哪些資料單位延伸模組時，您可能需要直接存取 Windows Media Format SDK 的 [Reader 物件](reader-object.md) 。 下列函式顯示如何取得讀取器物件本身的 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) 介面：


```C++
HRESULT GetReaderAdvanced (IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  // We use CComPtr's to avoid headaches at cleanup time
  CComPtr<IEnumFilters> pEnum;
  CComPtr<IBaseFilter> pFilter;
  ULONG cFetched;

  HRESULT hr = pGraph->EnumFilters(&pEnum);
  if (FAILED(hr)) 
  {
    return hr;
  }

  while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
  {
    IWMHeaderInfo *pHI = NULL;
    // Only the WM ASF Reader will have interface. This filter should be
    // the first one returned in this loop.
    hr = pFilter->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHI);
    if (SUCCEEDED(hr))
    {
      // We use the IWMDRMReader interface only as a way to get
      // a pointer to the Reader Object.
      CComPtr<IWMDRMReader> pWMDRMReader;
      CComQIPtr<IServiceProvider, &IID_IServiceProvider> pSP;

      hr = pHI->QueryInterface(__uuidof(IServiceProvider), (void**)&pSP);
      if (!pSP)
      {
        return E_NOINTERFACE;
      }
      
      hr = pSP->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader);
      if (FAILED(hr))
      {
        return hr;
      }

      CComQIPtr<IWMReaderAdvanced2, &IID_IWMReaderAdvanced2> pRA2(pWMDRMReader);
      if (pRA2)
      {
        *pReaderAdvanced2 = pRA2.Detach();
        return S_OK;
      }

    }
    pFilter.Release();
  }
  
  //if we get here, we didn't find the WM ASF Reader
  return E_FAIL;
}
```



 

 




