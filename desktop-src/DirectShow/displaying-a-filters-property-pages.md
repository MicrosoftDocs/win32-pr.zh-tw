---
description: 顯示篩選的屬性頁
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: 顯示篩選的屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385573"
---
# <a name="displaying-a-filters-property-pages"></a><span data-ttu-id="92398-103">顯示篩選的屬性頁</span><span class="sxs-lookup"><span data-stu-id="92398-103">Displaying a Filter's Property Pages</span></span>

<span data-ttu-id="92398-104">屬性頁是篩選準則的一種方式，可支援使用者可設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="92398-104">A property page is one way for a filter to support properties that the user can set.</span></span> <span data-ttu-id="92398-105">本文說明如何在應用程式中顯示篩選的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="92398-105">This article describes how to display a filter's property pages in an application.</span></span> <span data-ttu-id="92398-106">如需屬性頁的詳細資訊，請參閱 Platform SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="92398-106">For more information about property pages, see the Platform SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="92398-107">雖然 DirectShow 提供的許多篩選準則都支援屬性頁，但它們的目的是要進行偵錯工具，而不建議應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="92398-107">Although many of the filters provided with DirectShow support property pages, they are intended for debugging purposes, and are not recommended for application use.</span></span> <span data-ttu-id="92398-108">在大部分情況下，會透過篩選上的自訂介面提供對等的功能。</span><span class="sxs-lookup"><span data-stu-id="92398-108">In most cases the equivalent functionality is provided through a custom interface on the filter.</span></span> <span data-ttu-id="92398-109">應用程式應以程式設計方式控制這些篩選器，而不是向使用者公開其屬性頁。</span><span class="sxs-lookup"><span data-stu-id="92398-109">An application should control these filters programmatically, rather than expose their property pages to users.</span></span>

 

<span data-ttu-id="92398-110">具有屬性頁的篩選會公開 **ISpecifyPropertyPages** 介面。</span><span class="sxs-lookup"><span data-stu-id="92398-110">Filters with property pages expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="92398-111">若要判斷篩選是否要定義屬性頁，請使用 **QueryInterface** 查詢此介面的篩選。</span><span class="sxs-lookup"><span data-stu-id="92398-111">To determine whether a filter defines a property page, query the filter for this interface using **QueryInterface**.</span></span>

<span data-ttu-id="92398-112">如果您直接透過呼叫 **CoCreateInstance**) 來建立篩選 (的實例，您就已經有篩選的指標。</span><span class="sxs-lookup"><span data-stu-id="92398-112">If you directly created an instance of a filter (by calling **CoCreateInstance**), you already have a pointer to the filter.</span></span> <span data-ttu-id="92398-113">如果沒有，您可以使用 [**IFilterGraph：： EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) 方法來列舉圖形中的篩選。</span><span class="sxs-lookup"><span data-stu-id="92398-113">If not, you can enumerate the filters in the graph, using the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method.</span></span> <span data-ttu-id="92398-114">如需詳細資訊，請參閱 [列舉篩選圖形中的物件](enumerating-objects-in-a-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="92398-114">For details, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span>

<span data-ttu-id="92398-115">當您擁有 **ISpecifyPropertyPages** 介面指標之後，請呼叫 **ISpecifyPropertyPages：： GetPages** 方法來取出篩選的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="92398-115">Once you have the **ISpecifyPropertyPages** interface pointer, retrieve the filter's property pages by calling the **ISpecifyPropertyPages::GetPages** method.</span></span> <span data-ttu-id="92398-116">這個方法會將全域唯一識別碼的計數陣列 (Guid) ，其中包含每個屬性頁 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="92398-116">This method fills a counted array of globally unique identifiers (GUIDs) with the class identifier (CLSID) of each property page.</span></span> <span data-ttu-id="92398-117">計數陣列是由 **CAUUID** 結構所定義，您必須加以配置但不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="92398-117">A counted array is defined by a **CAUUID** structure, which you must allocate but do not have to initialize.</span></span> <span data-ttu-id="92398-118">**GetPages** 方法會配置陣列，該陣列包含在 **CAUUID** 結構的 **pElems** 成員中。</span><span class="sxs-lookup"><span data-stu-id="92398-118">The **GetPages** method allocates the array, which is contained in the **pElems** member of the **CAUUID** structure.</span></span> <span data-ttu-id="92398-119">當您完成時，請呼叫 **CoTaskMemFree** 函式來釋放陣列。</span><span class="sxs-lookup"><span data-stu-id="92398-119">When you are done, free the array by calling the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="92398-120">**OleCreatePropertyFrame** 函式提供簡單的方式，讓您在強制回應對話方塊內顯示內容頁。</span><span class="sxs-lookup"><span data-stu-id="92398-120">The **OleCreatePropertyFrame** function provides a simple way to display the property pages inside a modal dialog box.</span></span>


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a><span data-ttu-id="92398-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="92398-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92398-122">基本的 DirectShow 工作</span><span class="sxs-lookup"><span data-stu-id="92398-122">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



