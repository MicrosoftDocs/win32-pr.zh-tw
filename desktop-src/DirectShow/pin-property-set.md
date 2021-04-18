---
description: 釘選屬性集
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: 釘選屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385647"
---
# <a name="pin-property-set"></a>釘選屬性集

[釘選] 屬性集會傳回篩選上的釘選釘選類別。 類別會在建立 pin 時由篩選準則設定;此類別會指出 pin 由這個 pin 傳遞或接收的資料類型。



|                   |                      |
|-------------------|----------------------|
| 屬性集 GUID | **AMPROPSETID \_ 釘選** |



 



| 屬性識別碼                   | 描述                      |
|-------------------------------|----------------------------------|
| **AMPROPERTY \_ 釘選 \_ 類別** | 指定釘選的類別。 |



 

DirectShow 會在 Uuid. h 標頭檔中定義下列釘選類別。



| 類別 GUID                     | Description                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **釘選 \_ 類別 \_ ANALOGVIDEOIN**  | 接受類比並 digitizes 的捕獲篩選器的輸入 pin。                                                                                                                                                                                                                                                     |
| **釘選 \_ 類別 \_ 捕獲**        | 捕捉 pin。                                                                                                                                                                                                                                                                                                            |
| **釘選 \_ 類別 \_ CC**             | 從第21行提供隱藏式輔助字幕資料的 Pin。                                                                                                                                                                                                                                                                      |
| **釘選 \_ 類別 \_ EDS**            | Pin 提供擴充的資料服務 (行21，甚至是欄位) 。                                                                                                                                                                                                                                                            |
| **釘選 \_ 類別 \_ NABTS**          | 提供北美洲 Videotext 標準資料的 Pin。                                                                                                                                                                                                                                                                   |
| **釘選 \_ 類別 \_ 預覽**        | 預覽 pin。                                                                                                                                                                                                                                                                                                            |
| **PIN \_ 類別 \_ 仍為**          | 提供靜止影像的 Pin。 必須先連接篩選器的捕獲 pin，才能連接到靜止映射 pin。                                                                                                                                                                                                    |
| **釘選 \_ 類別 \_ TELETEXT**       | 提供 teletext (隱藏式字幕變異) 的 Pin。                                                                                                                                                                                                                                                                   |
| **釘選 \_ 類別時間 \_ 碼**       | 提供時間碼資料的 Pin。                                                                                                                                                                                                                                                                                            |
| **釘選 \_ 類別 \_ VBI**            | 提供垂直空白間隔資料的 Pin。                                                                                                                                                                                                                                                                          |
| **釘選 \_ 類別 \_ VIDEOPORT**      | 要連接到重迭 [混音](overlay-mixer-filter.md)器上輸入 pin 零的影片輸出圖釘。                                                                                                                                                                                                                    |
| **釘選 \_ 類別 \_ VIDEOPORT \_ VBI** | 釘選到連接到 [VBI 介面](vbi-surface-allocator.md)配置器，這是在使用影片埠的情況下，為隱藏式字幕重迭等事物配置正確視訊記憶體所需的 VBI surface 配置器篩選器。 PCI、IEEE 1394 和 USB 案例都不會使用此篩選器。 |
| **PINNAME \_ 影片 \_ 副本 \_ CAPTURE**   | 硬體切割已關閉-字幕釘選                                                                                                                                                                                                                                                                                  |



 

這是唯讀的屬性。

### <a name="example-code"></a>範例程式碼

下列程式碼示範如何檢查 pin 是否支援此屬性集，如果是，如何取得釘選類別：


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> 此範例會使用 [SafeRelease](../medfound/saferelease.md) 函式來釋放介面指標。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[捕獲篩選準則的 Pin 需求](pin-requirements-for-capture-filters.md)
</dt> <dt>

[屬性集](property-sets.md)
</dt> <dt>

[使用 Pin 類別](working-with-pin-categories.md)
</dt> </dl>

 

 
