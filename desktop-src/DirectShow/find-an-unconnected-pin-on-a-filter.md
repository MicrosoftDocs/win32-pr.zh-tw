---
description: 本主題說明如何在篩選器上尋找未連接的 pin。 當您連接篩選器時，尋找未連接的 pin 會很有用。
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: 在篩選器上尋找未連接的 Pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a76100622f0398c58eb10f2dda041ba074f4610efbd1c649d48199ea2c676eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401752"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>在篩選器上尋找未連接的 Pin

本主題說明如何在篩選器上尋找未連接的 pin。 當您連接篩選器時，尋找未連接的 pin 會很有用。

在典型的 DirectShow 圖建立案例中，您需要一個連接的 pin，以符合特定的釘選方向 (輸入或輸出) 。 例如，當您連接兩個篩選器時，您會將某個篩選的輸出接點連接到輸入圖釘。 這兩個 pin 都必須在連接之前都沒有連線。

首先，我們需要一個函式來測試 pin 是否已連接到另一個 pin。 此函式會呼叫 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) 方法，測試 pin 是否已連接到另一個 pin。


```C++
// Query whether a pin is connected to another pin.
//
// Note: This function does not return a pointer to the connected pin.

HRESULT IsPinConnected(IPin *pPin, BOOL *pResult)
{
    IPin *pTmp = NULL;
    HRESULT hr = pPin->ConnectedTo(&pTmp);
    if (SUCCEEDED(hr))
    {
        *pResult = TRUE;
    }
    else if (hr == VFW_E_NOT_CONNECTED)
    {
        // The pin is not connected. This is not an error for our purposes.
        *pResult = FALSE;
        hr = S_OK;
    }

    SafeRelease(&pTmp);
    return hr;
}
```



> [!Note]  
> 此範例會使用 [SafeRelease](/windows/desktop/medfound/saferelease) 函式來釋放介面指標。

 

接下來，我們需要一個函式來測試 pin 是否符合指定的 pin 方向。 此函數會呼叫 [**IPin：： QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) 方法來取得釘選方向。


```C++
// Query whether a pin has a specified direction (input / output)
HRESULT IsPinDirection(IPin *pPin, PIN_DIRECTION dir, BOOL *pResult)
{
    PIN_DIRECTION pinDir;
    HRESULT hr = pPin->QueryDirection(&pinDir);
    if (SUCCEEDED(hr))
    {
        *pResult = (pinDir == dir);
    }
    return hr;
}
```



下一個函式會依條件 (釘選方向和連接狀態) 來比對 pin。


```C++
// Match a pin by pin direction and connection state.
HRESULT MatchPin(IPin *pPin, PIN_DIRECTION direction, BOOL bShouldBeConnected, BOOL *pResult)
{
    assert(pResult != NULL);

    BOOL bMatch = FALSE;
    BOOL bIsConnected = FALSE;

    HRESULT hr = IsPinConnected(pPin, &bIsConnected);
    if (SUCCEEDED(hr))
    {
        if (bIsConnected == bShouldBeConnected)
        {
            hr = IsPinDirection(pPin, direction, &bMatch);
        }
    }

    if (SUCCEEDED(hr))
    {
        *pResult = bMatch;
    }
    return hr;
}
```



最後，下列函式會使用 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面來迴圈顯示篩選上的釘選。 呼叫端會指定所需的釘選方向。 針對每個釘選，函式 `MatchPin` 會呼叫以測試釘選是否相符。 如果方向符合且 pin 未連接，則函式會在 *ppPin* 參數中傳回相符的釘選指標。


```C++
// Return the first unconnected input pin or output pin.
HRESULT FindUnconnectedPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    BOOL bFound = FALSE;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = MatchPin(pPin, PinDir, FALSE, &bFound);
        if (FAILED(hr))
        {
            goto done;
        }
        if (bFound)
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();
            break;
        }
        SafeRelease(&pPin);
    }

    if (!bFound)
    {
        hr = VFW_E_NOT_FOUND;
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    return hr;
}
```



如需如何使用此函數的範例，請參閱[連線兩個篩選準則](connect-two-filters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列舉釘選](enumerating-pins.md)
</dt> <dt>

[一般 Graph-Building 技術](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
