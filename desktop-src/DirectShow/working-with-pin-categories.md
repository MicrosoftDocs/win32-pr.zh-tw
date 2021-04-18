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
# <a name="working-with-pin-categories"></a>使用 Pin 類別

若要在篩選準則中搜尋具有指定 pin 類別的 pin，您可以使用 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法。 下列範例會搜尋影片預覽 pin：


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



第一個參數是篩選準則 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。 接下來的三個參數會指定方向、釘選類別和媒體類型。 第五個參數中的 **FALSE** 值表示 pin 可以連接或未連接。  (如需這些參數的確切定義，請參閱方法的檔。 ) 如果方法找到相符的 pin，則會傳回 *pPin* 參數中 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面的指標。

雖然 [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法很方便，但您也可以視需要撰寫自己的 helper 函式。 若要判斷釘選的類別，請呼叫 [**IKsPropertySet：： Get**](ikspropertyset-get.md) 方法，如主題 [釘選屬性集](pin-property-set.md)中所述。

下列程式碼顯示 helper 函式，以檢查 pin 是否符合指定的類別：


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



下一個範例是依類別搜尋釘選的函式，類似于 [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法：


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



下列程式碼會使用上一個函式來搜尋篩選上的影片埠 pin：


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



如需屬性集的詳細資訊，請參閱 [Windows 驅動程式套件 (WDK) ](/windows-hardware/drivers/gettingstarted/) 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[釘選屬性集](pin-property-set.md)
</dt> <dt>

[DirectShow 影片捕獲篩選](directshow-video-capture-filters.md)
</dt> </dl>

 

 
