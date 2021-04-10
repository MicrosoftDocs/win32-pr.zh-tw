---
description: 依 CLSID 新增篩選
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: 依 CLSID 新增篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f880ab1cb3b88fbe6d889acdd192bba341ce2acf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109717"
---
# <a name="add-a-filter-by-clsid"></a>依 CLSID 新增篩選

下列函式會使用指定的類別識別碼 (CLSID) 來建立篩選，並將其新增至篩選圖形：


```C++
// Create a filter by CLSID and add it to the graph.

HRESULT AddFilterByCLSID(
    IGraphBuilder *pGraph,      // Pointer to the Filter Graph Manager.
    REFGUID clsid,              // CLSID of the filter to create.
    IBaseFilter **ppF,          // Receives a pointer to the filter.
    LPCWSTR wszName             // A name for the filter (can be NULL).
    )
{
    *ppF = 0;

    IBaseFilter *pFilter = NULL;
    
    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pFilter, wszName);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppF = pFilter;
    (*ppF)->AddRef();

done:
    SafeRelease(&pFilter);
    return hr;
}
```



> [!Note]  
> 此範例使用 [SafeRelease](/windows/desktop/medfound/saferelease) 函式來釋放 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 指標。

 

此函數會呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立篩選準則，然後呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將篩選新增至圖形。 下列程式碼範例會使用此函式，將 [AVI Mux](avi-mux-filter.md) 篩選器新增至圖形：


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



請注意，某些篩選器無法使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)建立。 這通常是管理其他軟體元件的篩選準則。 例如， [AVI 壓縮](avi-compressor-filter.md) 程式篩選器是適用于影片編解碼器的包裝函式，而 [wdm 影片捕獲](wdm-video-capture-filter.md) 篩選器是適用于 wdm Capture 驅動程式的包裝函式。 您必須使用 [系統裝置列舉](system-device-enumerator.md) 值或 [篩選器](filter-mapper.md)對應程式來建立這些篩選器。 如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般 Graph-Building 技術](general-graph-building-techniques.md)
</dt> </dl>

 

 
