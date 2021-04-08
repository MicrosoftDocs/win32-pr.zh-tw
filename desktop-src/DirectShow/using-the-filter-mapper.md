---
description: 使用篩選器對應程式
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: 使用篩選器對應程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850336"
---
# <a name="using-the-filter-mapper"></a><span data-ttu-id="aace3-103">使用篩選器對應程式</span><span class="sxs-lookup"><span data-stu-id="aace3-103">Using the Filter Mapper</span></span>

<span data-ttu-id="aace3-104">[篩選器](filter-mapper.md)對應程式是一種 COM 物件，可根據各種搜尋準則來列舉 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="aace3-104">The [Filter Mapper](filter-mapper.md) is a COM object that enumerates DirectShow filters based on various search criteria.</span></span> <span data-ttu-id="aace3-105">篩選對應程式可能比系統裝置列舉值低，因此，如果您需要特定類別的篩選，則應該使用系統裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="aace3-105">The Filter Mapper can be less efficient than the System Device Enumerator, so if you need filters from a particular category, you should use the System Device Enumerator.</span></span> <span data-ttu-id="aace3-106">但是，如果您需要尋找支援特定媒體類型組合的篩選器，但不屬於清除的類別，您可能需要使用篩選器對應程式。</span><span class="sxs-lookup"><span data-stu-id="aace3-106">But if you need to locate a filter that supports a certain combination of media types, but does not fall into a clear-cut category, you might need to use the Filter Mapper.</span></span> <span data-ttu-id="aace3-107"> (範例是轉譯器篩選器或解碼篩選器。 ) </span><span class="sxs-lookup"><span data-stu-id="aace3-107">(An example would be a renderer filter or a decoder filter.)</span></span>

<span data-ttu-id="aace3-108">篩選器對應程式會公開 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 介面。</span><span class="sxs-lookup"><span data-stu-id="aace3-108">The Filter Mapper exposes the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span> <span data-ttu-id="aace3-109">若要搜尋篩選準則，請呼叫 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) 方法。</span><span class="sxs-lookup"><span data-stu-id="aace3-109">To search for a filter, call the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method.</span></span> <span data-ttu-id="aace3-110">這個方法會採用數個定義搜尋準則的參數，並傳回相符篩選準則的枚舉器。</span><span class="sxs-lookup"><span data-stu-id="aace3-110">This method takes several parameters that define the search criteria, and returns an enumerator for the matching filters.</span></span> <span data-ttu-id="aace3-111">列舉值支援 [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) 介面，並為每個相符的篩選器提供唯一的標記。</span><span class="sxs-lookup"><span data-stu-id="aace3-111">The enumerator supports the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface, and supplies a unique moniker for each matching filter.</span></span>

<span data-ttu-id="aace3-112">下列範例會列舉接受數位視訊 (DV) 輸入的篩選器，並至少有一個輸出釘選任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="aace3-112">The following example enumerates filters that accept digital video (DV) input and have at least one output pin, of any media type.</span></span> <span data-ttu-id="aace3-113"> ([DV 影片解碼](dv-video-decoder-filter.md) 篩選準則符合這些準則。 ) </span><span class="sxs-lookup"><span data-stu-id="aace3-113">(The [DV Video Decoder](dv-video-decoder-filter.md) filter matches these criteria.)</span></span>


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



<span data-ttu-id="aace3-114">[**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)方法有相當大量的參數，在範例中會加上批註。</span><span class="sxs-lookup"><span data-stu-id="aace3-114">The [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method has a fairly large number of parameters, which are commented in the example.</span></span> <span data-ttu-id="aace3-115">此範例中的重要專案包括：</span><span class="sxs-lookup"><span data-stu-id="aace3-115">The significant ones for this example include:</span></span>

-   <span data-ttu-id="aace3-116">最小的最小值：篩選準則必須有高於 [ \_ 未使用] 的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="aace3-116">Minimum merit value: The filter must have a merit value above MERIT\_DO\_NOT\_USE.</span></span>
-   <span data-ttu-id="aace3-117">輸入類型：呼叫端會傳遞包含主要類型和子類型配對的陣列。</span><span class="sxs-lookup"><span data-stu-id="aace3-117">Input types: The caller passes an array containing pairs of major types and subtypes.</span></span> <span data-ttu-id="aace3-118">只有支援至少一組的篩選準則才會相符。</span><span class="sxs-lookup"><span data-stu-id="aace3-118">Only filters that support at least one of these pairs will match.</span></span>
-   <span data-ttu-id="aace3-119">完全相符：篩選準則可以為主要類型、子類型、釘選類別或媒體註冊 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="aace3-119">Exact match: A filter can register **NULL** values for major type, subtype, pin category, or medium.</span></span> <span data-ttu-id="aace3-120">除非您指定完全相符，否則 **Null** 值會作為萬用字元，以符合您指定的任何值。</span><span class="sxs-lookup"><span data-stu-id="aace3-120">Unless you specify exact matching, a **NULL** value acts as a wildcard, matching any value that you specify.</span></span> <span data-ttu-id="aace3-121">在完全相符的情況下，篩選準則必須完全符合您的條件。</span><span class="sxs-lookup"><span data-stu-id="aace3-121">With exact matching, the filter must exactly match your criteria.</span></span> <span data-ttu-id="aace3-122">但是，如果您在搜尋準則中提供 **Null** 參數，它一律會作為萬用字元或「不在意」值，以符合任何篩選準則。</span><span class="sxs-lookup"><span data-stu-id="aace3-122">However, if you give a **NULL** parameter in the search criteria, it always acts as a wildcard or "don't care" value, matching any filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aace3-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="aace3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aace3-124">列舉裝置和篩選器</span><span class="sxs-lookup"><span data-stu-id="aace3-124">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="aace3-125">智慧型連接</span><span class="sxs-lookup"><span data-stu-id="aace3-125">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 
