---
title: 如何使用快取
description: 本主題包含範例程式碼，示範如何使用快取 (或大量提取 Microsoft 消費者介面自動化樹狀結構的) 功能。
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965575"
---
# <a name="how-to-use-caching"></a><span data-ttu-id="73224-103">如何使用快取</span><span class="sxs-lookup"><span data-stu-id="73224-103">How to Use Caching</span></span>

<span data-ttu-id="73224-104">本主題包含範例程式碼，示範如何使用快取 (或大量提取 Microsoft 消費者介面自動化樹狀結構的) 功能。</span><span class="sxs-lookup"><span data-stu-id="73224-104">This topic contains example code that shows how to use the caching (or bulk fetching) capabilities of Microsoft UI Automation tree.</span></span> <span data-ttu-id="73224-105">本主題將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="73224-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="73224-106">將屬性和控制項模式提取至快取</span><span class="sxs-lookup"><span data-stu-id="73224-106">Fetching Properties and Control Patterns into the Cache</span></span>](#fetching-properties-and-control-patterns-into-the-cache)
-   [<span data-ttu-id="73224-107">從快取中取出屬性和控制項模式</span><span class="sxs-lookup"><span data-stu-id="73224-107">Retrieving Properties and Control Patterns from the Cache</span></span>](#retrieving-properties-and-control-patterns-from-the-cache)
-   [<span data-ttu-id="73224-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="73224-108">Related topics</span></span>](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a><span data-ttu-id="73224-109">將屬性和控制項模式提取至快取</span><span class="sxs-lookup"><span data-stu-id="73224-109">Fetching Properties and Control Patterns into the Cache</span></span>

<span data-ttu-id="73224-110">下列程式碼範例示範一個函式，該函式會從清單控制項取出專案，並快取每個專案的 SelectionItem 控制項模式和名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="73224-110">The following code example shows a function that retrieves items from a list control and caches the SelectionItem control pattern and Name property for each item.</span></span> <span data-ttu-id="73224-111">依預設，會傳回具有完整參考的清單專案，如此一來，所有目前的屬性仍可供使用。</span><span class="sxs-lookup"><span data-stu-id="73224-111">By default, the list items are returned with a full reference, so that all current properties are still available.</span></span>


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a><span data-ttu-id="73224-112">從快取中取出屬性和控制項模式</span><span class="sxs-lookup"><span data-stu-id="73224-112">Retrieving Properties and Control Patterns from the Cache</span></span>

<span data-ttu-id="73224-113">下列程式碼示範如何從快取中取出屬性和控制項模式。</span><span class="sxs-lookup"><span data-stu-id="73224-113">The following code demonstrates how to retrieve properties and control patterns from the cache.</span></span> <span data-ttu-id="73224-114">它會抓取清單專案的 SelectionItem 控制項模式和名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="73224-114">It retrieves the SelectionItem control pattern and Name property for a list item.</span></span>


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="73224-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="73224-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="73224-116">**概念**</span><span class="sxs-lookup"><span data-stu-id="73224-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73224-117">快取消費者介面自動化屬性和控制項模式</span><span class="sxs-lookup"><span data-stu-id="73224-117">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
</dt> <dt>

[<span data-ttu-id="73224-118">消費者介面自動化用戶端的使用說明主題</span><span class="sxs-lookup"><span data-stu-id="73224-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




