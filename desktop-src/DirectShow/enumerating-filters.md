---
description: 列舉篩選
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: 列舉篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de0f979973d339b790b04a8a5d4d98fc52c95c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973742"
---
# <a name="enumerating-filters"></a><span data-ttu-id="6307a-103">列舉篩選</span><span class="sxs-lookup"><span data-stu-id="6307a-103">Enumerating Filters</span></span>

<span data-ttu-id="6307a-104">篩選圖形管理員支援 [**IFilterGraph：： EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) 方法，該方法會列舉篩選圖形中的所有篩選準則。</span><span class="sxs-lookup"><span data-stu-id="6307a-104">The Filter Graph Manager supports the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method, which enumerates all the filters in the filter graph.</span></span> <span data-ttu-id="6307a-105">它會傳回 [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6307a-105">It returns a pointer to the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface.</span></span> <span data-ttu-id="6307a-106">[**IEnumFilters：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next)方法會捕獲 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面指標。</span><span class="sxs-lookup"><span data-stu-id="6307a-106">The [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) method retrieves [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointers.</span></span>

<span data-ttu-id="6307a-107">下列範例顯示的函式會列舉圖形中的篩選器，並顯示包含每個篩選器名稱的訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="6307a-107">The following example shows a function that enumerates the filters in a graph and displays a message box with each filter's name.</span></span> <span data-ttu-id="6307a-108">它會使用 [**IBaseFilter：： QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) 方法來取出篩選器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6307a-108">It uses the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method to retrieve the name of the filter.</span></span> <span data-ttu-id="6307a-109">請注意函式在介面上呼叫 **釋放** 的位置，以遞減參考計數。</span><span class="sxs-lookup"><span data-stu-id="6307a-109">Note the places where the function calls **Release** on an interface to decrement the reference count.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6307a-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6307a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6307a-111">列舉篩選圖形中的物件</span><span class="sxs-lookup"><span data-stu-id="6307a-111">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



