---
description: 註冊篩選準則的指導方針
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: 註冊篩選準則的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221cadf6fb4806a2fa5c5b2cc4fd9abf423cec426ec23cd76b0bc642080852af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905358"
---
# <a name="guidelines-for-registering-filters"></a>註冊篩選準則的指導方針

篩選登錄資訊會決定篩選 Graph Manager 在[智慧型連線](intelligent-connect.md)期間的功能。 因此，它會影響針對 DirectShow 所撰寫的每個應用程式，而不只是將使用您篩選的應用程式。 您應該遵循下列指導方針，以確定您的篩選行為正確。

1.  您是否需要登錄中的篩選資料？ 針對許多自訂篩選，沒有理由讓篩選器或系統裝置列舉值看不到篩選。 只要您註冊 DLL，您的應用程式就可以使用 **CoCreateInstance** 建立篩選器。 在這種情況下，只需省略 factory 範本中的 [**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md) 結構。  (一個缺點是您的篩選器將不會顯示在 GraphEdit 中。 若要解決此問題，您可以使用 [**IFilterMapper2：： CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) 方法建立私用「測試」類別。 您應該只針對 debug 組建進行此作業。 ) 
2.  選擇正確的篩選準則分類。 預設的「DirectShow 篩選準則」類別適用于一般用途的篩選準則。 在適當的情況下，在更明確的類別中註冊您的篩選準則。 當 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 搜尋篩選器時，它會忽略任何其業績不會 \_ \_ \_ 使用或小於的類別。 不適用於正常播放的類別具有較低的優點。
3.  避免 \_ \_ \_ 在 pin 的 [**AMOVIESETUP \_ 媒體**](amoviesetup-mediatype.md) 資訊中指定媒體類型 None、MEDIASUBTYPE none 或 GUID Null。 **IFilterMapper2** 會將這些視為萬用字元，這可能會使圖形建立進程變慢。
4.  選擇最小的可能值。 以下是一些指導方針：

    | 濾波器類型                                                                                       | 建議的優點                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | 預設轉譯器                                                                                     | \_慣用。 不過，對於標準媒體類型，自訂轉譯器絕對不應該是預設值。 |
    | 非預設轉譯器                                                                                 | \_ \_ 不 \_ 太可能使用或不 \_ 太可能的業績                                                              |
    | Mux                                                                                                  | \_ \_ 未 \_ 使用的業績                                                                                 |
    | 解碼器                                                                                              | 一般的業績 \_                                                                                       |
    | Spitter，剖析器                                                                                      | \_正常或較低的業績                                                                              |
    | 特殊用途篩選;由應用程式直接建立的任何篩選                       | \_ \_ 未 \_ 使用的業績                                                                                 |
    | 擷取                                                                                              | \_ \_ 未 \_ 使用的業績                                                                                 |
    | 「Fallback」篩選;例如， [色彩空間轉換器篩選](color-space-converter-filter.md) | 不 \_ 太可能                                                                                     |

    

     

    如果您提供的篩選準則 \_ \_ 不 \_ 使用，請考慮您是否需要在一開始就註冊這項資訊。  (請參閱專案 1. ) 

5.  請勿在接受24位 RGB 的「DirectShow 篩選準則」類別中註冊篩選。 您的篩選準則會干擾色彩空間轉換器篩選。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何註冊 DirectShow 篩選準則](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



