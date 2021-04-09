---
description: 移除圖形中的所有篩選
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: 移除圖形中的所有篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687828"
---
# <a name="remove-all-the-filters-in-the-graph"></a>移除圖形中的所有篩選

若要移除篩選圖形中的所有篩選，最簡單的方式就是釋出篩選圖形管理員並建立一個新的。 請務必釋放應用程式對篩選圖形管理員上任何介面的每個指標，以及圖形中物件的指標，包括篩選、釘選、參考時鐘等等。

或者，您也可以使用 [**IFilterGraph：： RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) 方法，一次移除一個篩選：


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



此範例會使用 [**IFilterGraph：： EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) 方法來列舉圖形中的篩選。 移除篩選會導致列舉值物件與圖形不同步。 使用 [**IEnumFilters：： reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) 方法來重設列舉值。 否則，後續對 [**IEnumFilters：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) 的呼叫將會失敗。

 

 



