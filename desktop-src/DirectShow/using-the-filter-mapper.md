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
# <a name="using-the-filter-mapper"></a>使用篩選器對應程式

[篩選器](filter-mapper.md)對應程式是一種 COM 物件，可根據各種搜尋準則來列舉 DirectShow 篩選。 篩選對應程式可能比系統裝置列舉值低，因此，如果您需要特定類別的篩選，則應該使用系統裝置枚舉器。 但是，如果您需要尋找支援特定媒體類型組合的篩選器，但不屬於清除的類別，您可能需要使用篩選器對應程式。  (範例是轉譯器篩選器或解碼篩選器。 ) 

篩選器對應程式會公開 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 介面。 若要搜尋篩選準則，請呼叫 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) 方法。 這個方法會採用數個定義搜尋準則的參數，並傳回相符篩選準則的枚舉器。 列舉值支援 [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) 介面，並為每個相符的篩選器提供唯一的標記。

下列範例會列舉接受數位視訊 (DV) 輸入的篩選器，並至少有一個輸出釘選任何媒體類型。  ([DV 影片解碼](dv-video-decoder-filter.md) 篩選準則符合這些準則。 ) 


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



[**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)方法有相當大量的參數，在範例中會加上批註。 此範例中的重要專案包括：

-   最小的最小值：篩選準則必須有高於 [ \_ 未使用] 的值 \_ \_ 。
-   輸入類型：呼叫端會傳遞包含主要類型和子類型配對的陣列。 只有支援至少一組的篩選準則才會相符。
-   完全相符：篩選準則可以為主要類型、子類型、釘選類別或媒體註冊 **Null** 值。 除非您指定完全相符，否則 **Null** 值會作為萬用字元，以符合您指定的任何值。 在完全相符的情況下，篩選準則必須完全符合您的條件。 但是，如果您在搜尋準則中提供 **Null** 參數，它一律會作為萬用字元或「不在意」值，以符合任何篩選準則。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列舉裝置和篩選器](enumerating-devices-and-filters.md)
</dt> <dt>

[智慧型連接](intelligent-connect.md)
</dt> </dl>

 

 
