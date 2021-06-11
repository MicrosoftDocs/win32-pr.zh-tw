---
description: 瞭解如何使用 DirectShow 中的 IWMReaderAdvanced2 介面，取得 Windows Media Format SDK 的 Reader 物件指標。
ms.assetid: d1292e2f-bd0e-4961-a6fa-8cdaeb28b692
title: '取得讀取器物件的指標 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e131b9e111aa5e779d1208b68e04c9979e3b1d7f
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989104"
---
# <a name="obtaining-a-pointer-to-the-reader-object-directshow"></a>取得讀取器物件的指標 (DirectShow) 

在某些情況下，例如，當您在指定的資料流程上設定哪些資料單位延伸模組時，您可能需要直接存取 Windows Media Format SDK 的 Reader 物件。 下列函式顯示如何取得讀取器物件本身的 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) 介面：


```C++
#include <wmsdk.h>
HRESULT GetReaderAdvanced(IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
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
    // Only the WM ASF Reader will have interface. 
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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
