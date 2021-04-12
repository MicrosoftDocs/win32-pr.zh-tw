---
description: 尋找篩選對等
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: 尋找篩選對等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025606"
---
# <a name="find-a-filters-peer"></a><span data-ttu-id="65943-103">尋找篩選對等</span><span class="sxs-lookup"><span data-stu-id="65943-103">Find a Filters Peer</span></span>

<span data-ttu-id="65943-104">提供篩選準則之後，您可以藉由尋找已連接的篩選來進行圖形。</span><span class="sxs-lookup"><span data-stu-id="65943-104">Given a filter, you can traverse the graph by finding the filters to which it is connected.</span></span> <span data-ttu-id="65943-105">從列舉篩選器的釘選。</span><span class="sxs-lookup"><span data-stu-id="65943-105">Start by enumerating the filter's pins.</span></span> <span data-ttu-id="65943-106">針對每個 pin，檢查該 pin 是否已連接到另一個 pin。</span><span class="sxs-lookup"><span data-stu-id="65943-106">For each pin, check whether that pin is connected to another pin.</span></span> <span data-ttu-id="65943-107">若是如此，請查詢其擁有篩選準則的其他 pin。</span><span class="sxs-lookup"><span data-stu-id="65943-107">If so, query the other pin for it's owning filter.</span></span> <span data-ttu-id="65943-108">您可以藉由列舉輸出圖釘來列舉篩選的輸入圖釘，或在下游方向中，以上游方向來流覽圖形。</span><span class="sxs-lookup"><span data-stu-id="65943-108">You can walk the graph in the upstream direction by enumerating the filter's input pins, or in the downstream direction by enumerating the output pins.</span></span>

<span data-ttu-id="65943-109">下列函式會針對已連線的篩選準則搜尋上游或下游。</span><span class="sxs-lookup"><span data-stu-id="65943-109">The following function searches upstream or downstream for a connected filter.</span></span> <span data-ttu-id="65943-110">它會傳回所找到的第一個相符篩選準則：</span><span class="sxs-lookup"><span data-stu-id="65943-110">It returns the first matching filter that it finds:</span></span>


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



<span data-ttu-id="65943-111">此函數會呼叫 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 來列舉第一個篩選器的釘選。</span><span class="sxs-lookup"><span data-stu-id="65943-111">The function calls [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) to enumerate the first filter's pins.</span></span> <span data-ttu-id="65943-112">針對每個 pin，它會呼叫 [**IPin：： QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) 來檢查釘選是否符合指定的方向 (輸入或輸出) 。</span><span class="sxs-lookup"><span data-stu-id="65943-112">For each pin, it calls [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) to check whether the pin matches the specified direction (input or output).</span></span> <span data-ttu-id="65943-113">如果是，則函式會藉由呼叫 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) 方法，判斷該 pin 是否已連接到另一個 pin。</span><span class="sxs-lookup"><span data-stu-id="65943-113">If so, the function determines whether that pin is connected to another pin, by calling the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span> <span data-ttu-id="65943-114">最後，它會在連線的 pin 上呼叫 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) 。</span><span class="sxs-lookup"><span data-stu-id="65943-114">Finally, it calls [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) on the connected pin.</span></span> <span data-ttu-id="65943-115">這個方法會傳回結構，其中包含該釘選之擁有篩選準則的指標，還有其他專案。</span><span class="sxs-lookup"><span data-stu-id="65943-115">This method returns a structure that contains, among other things, a pointer to that pin's owning filter.</span></span> <span data-ttu-id="65943-116">這個指標會傳回給呼叫端的 *ppNext* 參數。</span><span class="sxs-lookup"><span data-stu-id="65943-116">This pointer is returned to the caller in the *ppNext* parameter.</span></span> <span data-ttu-id="65943-117">呼叫端必須釋放指標。</span><span class="sxs-lookup"><span data-stu-id="65943-117">The caller must release the pointer.</span></span>

<span data-ttu-id="65943-118">下列程式碼示範如何呼叫這個函式：</span><span class="sxs-lookup"><span data-stu-id="65943-118">The following code shows how to call this function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



<span data-ttu-id="65943-119">篩選器可能會連接到兩個或多個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="65943-119">A filter might be connected to two or more filters in either direction.</span></span> <span data-ttu-id="65943-120">例如，它可能是分隔器篩選，其中有數個來自它的下游篩選。</span><span class="sxs-lookup"><span data-stu-id="65943-120">For example, it might be a splitter filter, with several filters downstream from it.</span></span> <span data-ttu-id="65943-121">或者，它可能是 mux 篩選器，其中有多個來自它的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="65943-121">Or it might be a mux filter, with several filters upstream from it.</span></span> <span data-ttu-id="65943-122">因此，您可能會想要將它們全部收集到清單中。</span><span class="sxs-lookup"><span data-stu-id="65943-122">Therefore, you might want to collect all of them into a list.</span></span>

<span data-ttu-id="65943-123">下列程式碼顯示一種可能的方法來執行這類函數。</span><span class="sxs-lookup"><span data-stu-id="65943-123">The following code shows one possible way to implement such a function.</span></span> <span data-ttu-id="65943-124">它會使用 DirectShow [**CGenericList**](cgenericlist.md) 類別;您可以使用其他資料結構來撰寫對等函數。</span><span class="sxs-lookup"><span data-stu-id="65943-124">It uses the DirectShow [**CGenericList**](cgenericlist.md) class; you could write an equivalent function using some other data structure.</span></span>


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



<span data-ttu-id="65943-125">若要稍微複雜一點，篩選器可以有多個連接至相同篩選的 pin。</span><span class="sxs-lookup"><span data-stu-id="65943-125">To complicate matters somewhat, a filter can have multiple pin connections to the same filter.</span></span> <span data-ttu-id="65943-126">若要避免將重複專案放入清單中，請查詢 **iunknown** 的每個 **IBaseFilter** 指標，並比較 **iunknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="65943-126">To avoid putting duplicates into the list, query each **IBaseFilter** pointer for **IUnknown** and compare the **IUnknown** pointers.</span></span> <span data-ttu-id="65943-127">根據 COM 的規則，如果有兩個介面指標傳回相同的 **IUnknown** 指標，則會參考相同的物件。</span><span class="sxs-lookup"><span data-stu-id="65943-127">By the rules of COM, two interface pointers refer to the same object if and only if they return identical **IUnknown** pointers.</span></span> <span data-ttu-id="65943-128">在上述範例中，AddFilterUnique 函式會處理此詳細資料。</span><span class="sxs-lookup"><span data-stu-id="65943-128">In the previous example, the AddFilterUnique function handles this detail.</span></span>

<span data-ttu-id="65943-129">下列範例顯示如何使用 GetPeerFilters 函數：</span><span class="sxs-lookup"><span data-stu-id="65943-129">The following example shows how to use the GetPeerFilters function:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="65943-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="65943-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65943-131">一般 Graph-Building 技術</span><span class="sxs-lookup"><span data-stu-id="65943-131">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 



