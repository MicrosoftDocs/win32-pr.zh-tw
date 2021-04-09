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
# <a name="enumerating-pins"></a>列舉釘選

篩選準則支援 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法，該方法會列舉篩選器上可用的釘選。 它會傳回 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面的指標。 [**IEnumPins：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next)方法會捕獲 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面指標。

下列範例顯示的函式會在指定的篩選準則下找出具有指定方向 (輸入或輸出) 的釘選。 它會使用 [**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction) 列舉來指定釘選方向，以及使用 [**IPin：： QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) 方法來尋找每個列舉圖釘的方向。 如果此函式找到相符的 pin，則會傳回具有未處理之參考計數的 **IPin** 介面指標。 呼叫端負責釋放介面。


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



您可以輕鬆地修改此函式，以傳回具有指定方向的第 n 個 pin，或 *n* 個未連接的 pin。  (，以找出 pin 是否已連接到另一個 pin，請呼叫 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) 方法。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列舉篩選圖形中的物件](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[在篩選器上尋找未連接的 Pin](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[一般 Graph-Building 技術](general-graph-building-techniques.md)
</dt> <dt>

[釘選屬性集](pin-property-set.md)
</dt> </dl>

 

 



