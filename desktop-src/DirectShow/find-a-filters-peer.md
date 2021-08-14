---
description: 尋找篩選對等
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: 尋找篩選對等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2f20a7145d2365e7ee1ec261ea861ddc5fa1eb01d0c3b2503f6f53fa25815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401762"
---
# <a name="find-a-filters-peer"></a>尋找篩選對等

提供篩選準則之後，您可以藉由尋找已連接的篩選來進行圖形。 從列舉篩選器的釘選。 針對每個 pin，檢查該 pin 是否已連接到另一個 pin。 若是如此，請查詢其擁有篩選準則的其他 pin。 您可以藉由列舉輸出圖釘來列舉篩選的輸入圖釘，或在下游方向中，以上游方向來流覽圖形。

下列函式會針對已連線的篩選準則搜尋上游或下游。 它會傳回所找到的第一個相符篩選準則：


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



此函數會呼叫 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 來列舉第一個篩選器的釘選。 針對每個 pin，它會呼叫 [**IPin：： QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) 來檢查釘選是否符合指定的方向 (輸入或輸出) 。 如果是，則函式會藉由呼叫 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) 方法，判斷該 pin 是否已連接到另一個 pin。 最後，它會在連線的 pin 上呼叫 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) 。 這個方法會傳回結構，其中包含該釘選之擁有篩選準則的指標，還有其他專案。 這個指標會傳回給呼叫端的 *ppNext* 參數。 呼叫端必須釋放指標。

下列程式碼示範如何呼叫這個函式：


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



篩選器可能會連接到兩個或多個篩選準則。 例如，它可能是分隔器篩選，其中有數個來自它的下游篩選。 或者，它可能是 mux 篩選器，其中有多個來自它的篩選準則。 因此，您可能會想要將它們全部收集到清單中。

下列程式碼顯示一種可能的方法來執行這類函數。 它會使用 DirectShow 的 [**CGenericList**](cgenericlist.md)類別;您可以使用其他資料結構來撰寫對等函數。


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



若要稍微複雜一點，篩選器可以有多個連接至相同篩選的 pin。 若要避免將重複專案放入清單中，請查詢 **iunknown** 的每個 **IBaseFilter** 指標，並比較 **iunknown** 指標。 根據 COM 的規則，如果有兩個介面指標傳回相同的 **IUnknown** 指標，則會參考相同的物件。 在上述範例中，AddFilterUnique 函式會處理此詳細資料。

下列範例顯示如何使用 GetPeerFilters 函數：


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般 Graph-Building 技術](general-graph-building-techniques.md)
</dt> </dl>

 

 



