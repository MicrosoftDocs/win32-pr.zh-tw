---
description: 列舉篩選
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: 列舉篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d584ddf74a13b06e99d9a7e0a34ac802c6da881d87cb163411100ea7772e1df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819661"
---
# <a name="enumerating-filters"></a>列舉篩選

篩選 Graph 管理員支援 [**IFilterGraph：： EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters)方法，該方法會列舉篩選圖形中的所有篩選準則。 它會傳回 [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) 介面的指標。 [**IEnumFilters：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next)方法會捕獲 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面指標。

下列範例顯示的函式會列舉圖形中的篩選器，並顯示包含每個篩選器名稱的訊息方塊。 它會使用 [**IBaseFilter：： QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) 方法來取出篩選器的名稱。 請注意函式在介面上呼叫 **釋放** 的位置，以遞減參考計數。


```C++
HRESULT EnumFilters (IFilterGraph *pGraph) 
{
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        FILTER_INFO FilterInfo;
        hr = pFilter->QueryFilterInfo(&FilterInfo);
        if (FAILED(hr))
        {
            MessageBox(NULL, TEXT("Could not get the filter info"),
                TEXT("Error"), MB_OK | MB_ICONERROR);
            continue;  // Maybe the next one will work.
        }

#ifdef UNICODE
        MessageBox(NULL, FilterInfo.achName, TEXT("Filter Name"), MB_OK);
#else
        char szName[MAX_FILTER_NAME];
        int cch = WideCharToMultiByte(CP_ACP, 0, FilterInfo.achName,
            MAX_FILTER_NAME, szName, MAX_FILTER_NAME, 0, 0);
        if (cch > 0)
            MessageBox(NULL, szName, TEXT("Filter Name"), MB_OK);
#endif

        // The FILTER_INFO structure holds a pointer to the Filter Graph
        // Manager, with a reference count that must be released.
        if (FilterInfo.pGraph != NULL)
        {
            FilterInfo.pGraph->Release();
        }
        pFilter->Release();
    }

    pEnum->Release();
    return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[列舉篩選 Graph 中的物件](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



