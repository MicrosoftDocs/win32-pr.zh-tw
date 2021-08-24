---
description: 尋找篩選或釘選上的介面
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: 尋找篩選或釘選上的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17314f7e44e4b2c4f412dd0d152e038203268c29d585cd684ddde9eb34992a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819560"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>尋找篩選或釘選上的介面

針對 DirectShow 中的許多作業，應用程式會在篩選 Graph 管理員上呼叫方法。 不過，在某些情況下，應用程式必須直接呼叫篩選或釘選上的方法。 例如，許多篩選器會公開用來設定篩選準則的特殊介面。

在篩選介面的案例中，您可能已有篩選準則 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。 在這種情況下，只要使用 **QueryInterface** 來取得其他介面即可。 但篩選 Graph 管理員可能會將某些篩選新增至圖形。  (需詳細資訊，請參閱 [智慧型連線](intelligent-connect.md)。 ) 在該情況下，請使用 [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)介面對圖形中的所有篩選進行迴圈，然後逐一查詢。 下列函式會示範這項功能：


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



若要在 pin 上尋找介面，請使用 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面，在篩選上的釘選迴圈。 下列函式顯示如何執行這項操作：


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



下一個函數會搜尋篩選或釘選上的介面：


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



請注意，此處顯示的所有函式都會在第一個成功的 **QueryInterface** 停止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列舉篩選](enumerating-filters.md)
</dt> <dt>

[列舉釘選](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



