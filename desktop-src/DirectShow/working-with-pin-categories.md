---
description: 使用 Pin 類別
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: 使用 Pin 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983369"
---
# <a name="working-with-pin-categories"></a><span data-ttu-id="cf9cb-103">使用 Pin 類別</span><span class="sxs-lookup"><span data-stu-id="cf9cb-103">Working with Pin Categories</span></span>

<span data-ttu-id="cf9cb-104">若要在篩選準則中搜尋具有指定 pin 類別的 pin，您可以使用 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-104">To search on a filter the the for a pin with a given pin category, you can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method.</span></span> <span data-ttu-id="cf9cb-105">下列範例會搜尋影片預覽 pin：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-105">The following example searches for a video preview pin:</span></span>


```C++
int i = 0;
hr = pBuild->FindPin(
    pFilter,               // Pointer to a filter to search.
    PINDIR_OUTPUT,         // Which pin direction?
    &PIN_CATEGORY_PREVIEW, // Which category? (NULL means "any category")
    &MEDIATYPE_Video,      // What media type? (NULL means "any type")
    FALSE,                 // Must be connected?
    i,                     // Get the i'th matching pin (0 = first match)
    &pPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="cf9cb-106">第一個參數是篩選準則 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-106">The first parameter is a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="cf9cb-107">接下來的三個參數會指定方向、釘選類別和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-107">The next three parameters specify the direction, pin category, and media type.</span></span> <span data-ttu-id="cf9cb-108">第五個參數中的 **FALSE** 值表示 pin 可以連接或未連接。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-108">The value **FALSE** in the fifth parameter indicates that the pin can be either connected or unconnected.</span></span> <span data-ttu-id="cf9cb-109"> (如需這些參數的確切定義，請參閱方法的檔。 ) 如果方法找到相符的 pin，則會傳回 *pPin* 參數中 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-109">(For the exact definitions of these parameters, refer to the documentation for the method.) If the method finds a matching pin, it returns a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface in the *pPin* parameter.</span></span>

<span data-ttu-id="cf9cb-110">雖然 [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法很方便，但您也可以視需要撰寫自己的 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-110">Although the [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method is convenient, you can also write your own helper functions if you prefer.</span></span> <span data-ttu-id="cf9cb-111">若要判斷釘選的類別，請呼叫 [**IKsPropertySet：： Get**](ikspropertyset-get.md) 方法，如主題 [釘選屬性集](pin-property-set.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-111">To determine a pin's category, call the [**IKsPropertySet::Get**](ikspropertyset-get.md) method as described in the topic [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="cf9cb-112">下列程式碼顯示 helper 函式，以檢查 pin 是否符合指定的類別：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-112">The following code shows a helper function that checks whether a pin matches a specified category:</span></span>


```C++
// Returns TRUE if a pin matches the specified pin category.

BOOL PinMatchesCategory(IPin *pPin, REFGUID Category)
{
    BOOL bFound = FALSE;

    IKsPropertySet *pKs = NULL;
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (SUCCEEDED(hr))
    {
        GUID PinCategory;
        DWORD cbReturned;
        hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
            &PinCategory, sizeof(GUID), &cbReturned);
        if (SUCCEEDED(hr) && (cbReturned == sizeof(GUID)))
        {
            bFound = (PinCategory == Category);
        }
        pKs->Release();
    }
    return bFound;
}
```



<span data-ttu-id="cf9cb-113">下一個範例是依類別搜尋釘選的函式，類似于 [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-113">The next example is a function that searches for a pin by category, similar to the [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method:</span></span>


```C++
// Finds the first pin that matches a specified pin category and direction.

HRESULT FindPinByCategory(
    IBaseFilter *pFilter, // Pointer to the filter to search.
    PIN_DIRECTION PinDir, // Direction of the pin.
    REFGUID Category,     // Pin category.
    IPin **ppPin)         // Receives a pointer to the pin.
{
    *ppPin = 0;

    HRESULT hr = S_OK;
    BOOL bFound = FALSE;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (hr = pEnum->Next(1, &pPin, 0), hr == S_OK)
    {
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            goto done;
        }
        if ((ThisPinDir == PinDir) && 
            PinMatchesCategory(pPin, Category))
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();   // The caller must release the interface.
            bFound = TRUE;
            break;
        }
        SafeRelease(&pPin);
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    if (SUCCEEDED(hr) && !bFound)
    {
        hr = E_FAIL;
    }
    return hr;
}
```



<span data-ttu-id="cf9cb-114">下列程式碼會使用上一個函式來搜尋篩選上的影片埠 pin：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-114">The following code uses the previous function to search for a video port pin on a filter:</span></span>


```C++
IPin *pVP; 
hr = FindPinByCategory(pFilter, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT, &pVP);
if (SUCCEEDED(hr))
{
    // Use pVP ... 
    // Release when you are done.
    pVP->Release();
}
```



<span data-ttu-id="cf9cb-115">如需屬性集的詳細資訊，請參閱 [Windows 驅動程式套件 (WDK) ](/windows-hardware/drivers/gettingstarted/) 檔。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-115">For more information about property sets, refer to the [Windows Driver Kit (WDK)](/windows-hardware/drivers/gettingstarted/) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf9cb-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf9cb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf9cb-117">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="cf9cb-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="cf9cb-118">釘選屬性集</span><span class="sxs-lookup"><span data-stu-id="cf9cb-118">Pin Property Set</span></span>](pin-property-set.md)
</dt> <dt>

[<span data-ttu-id="cf9cb-119">DirectShow 影片捕獲篩選</span><span class="sxs-lookup"><span data-stu-id="cf9cb-119">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> </dl>

 

 
