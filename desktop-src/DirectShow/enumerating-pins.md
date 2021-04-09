---
description: 列舉釘選
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: 列舉釘選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846255"
---
# <a name="enumerating-pins"></a><span data-ttu-id="4af61-103">列舉釘選</span><span class="sxs-lookup"><span data-stu-id="4af61-103">Enumerating Pins</span></span>

<span data-ttu-id="4af61-104">篩選準則支援 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法，該方法會列舉篩選器上可用的釘選。</span><span class="sxs-lookup"><span data-stu-id="4af61-104">Filters support the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method, which enumerates the pins available on the filter.</span></span> <span data-ttu-id="4af61-105">它會傳回 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4af61-105">It returns a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="4af61-106">[**IEnumPins：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next)方法會捕獲 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面指標。</span><span class="sxs-lookup"><span data-stu-id="4af61-106">The [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method retrieves [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointers.</span></span>

<span data-ttu-id="4af61-107">下列範例顯示的函式會在指定的篩選準則下找出具有指定方向 (輸入或輸出) 的釘選。</span><span class="sxs-lookup"><span data-stu-id="4af61-107">The following example shows a function that locates a pin with a given direction (input or output) on a given filter.</span></span> <span data-ttu-id="4af61-108">它會使用 [**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction) 列舉來指定釘選方向，以及使用 [**IPin：： QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) 方法來尋找每個列舉圖釘的方向。</span><span class="sxs-lookup"><span data-stu-id="4af61-108">It uses the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration to specify the pin direction, and the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to find the direction of each enumerated pin.</span></span> <span data-ttu-id="4af61-109">如果此函式找到相符的 pin，則會傳回具有未處理之參考計數的 **IPin** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="4af61-109">If this function finds a matching pin, it returns an **IPin** interface pointer with an outstanding reference count.</span></span> <span data-ttu-id="4af61-110">呼叫端負責釋放介面。</span><span class="sxs-lookup"><span data-stu-id="4af61-110">The caller is responsible for releasing the interface.</span></span>


```C++
HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins  *pEnum = NULL;
    IPin       *pPin = NULL;
    HRESULT    hr;

    if (ppPin == NULL)
    {
        return E_POINTER;
    }

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        hr = pPin->QueryDirection(&PinDirThis);
        if (FAILED(hr))
        {
            pPin->Release();
            pEnum->Release();
            return hr;
        }
        if (PinDir == PinDirThis)
        {
            // Found a match. Return the IPin pointer to the caller.
            *ppPin = pPin;
            pEnum->Release();
            return S_OK;
        }
        // Release the pin for the next time through the loop.
        pPin->Release();
    }
    // No more pins. We did not find a match.
    pEnum->Release();
    return E_FAIL;  
}
```



<span data-ttu-id="4af61-111">您可以輕鬆地修改此函式，以傳回具有指定方向的第 n 個 pin，或 *n* 個未連接的 pin。</span><span class="sxs-lookup"><span data-stu-id="4af61-111">This function could easily be modified to return the nth pin with the specified direction, or the *n* th unconnected pin.</span></span> <span data-ttu-id="4af61-112"> (，以找出 pin 是否已連接到另一個 pin，請呼叫 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) 方法。 ) </span><span class="sxs-lookup"><span data-stu-id="4af61-112">(To find out if a pin is connected to another pin, call the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4af61-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="4af61-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4af61-114">列舉篩選圖形中的物件</span><span class="sxs-lookup"><span data-stu-id="4af61-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="4af61-115">在篩選器上尋找未連接的 Pin</span><span class="sxs-lookup"><span data-stu-id="4af61-115">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[<span data-ttu-id="4af61-116">一般 Graph-Building 技術</span><span class="sxs-lookup"><span data-stu-id="4af61-116">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="4af61-117">釘選屬性集</span><span class="sxs-lookup"><span data-stu-id="4af61-117">Pin Property Set</span></span>](pin-property-set.md)
</dt> </dl>

 

 



