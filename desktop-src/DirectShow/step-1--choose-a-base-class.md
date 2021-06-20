---
description: 選擇基類作為撰寫轉換篩選的一部分。 瞭解哪些類別適合轉換篩選。
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: 步驟 1： 選擇基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a2bbf704bb2247034bc2ba3a6f35812f46aaaa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406461"
---
# <a name="step-1-choose-a-base-class"></a>步驟 1： 選擇基類

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟1。

假設您決定要撰寫篩選而不是，則第一個步驟是選擇要使用的基類。 下列類別適用于轉換篩選：

-   [**CTransformFilter**](ctransformfilter.md) 是針對使用不同輸入和輸出緩衝區的轉換篩選所設計。 這種篩選有時稱為複製轉換篩選。 當複製轉換篩選收到輸入範例時，它會將新的資料寫入至輸出範例，並將輸出範例傳遞給下一個篩選準則。
-   [**CTransInPlaceFilter**](ctransinplacefilter.md) 是針對修改原始緩衝區中資料的篩選準則所設計，也稱為「就地記錄篩選準則」。 當就地篩選收到範例時，它會變更該範例內的資料，並傳遞相同的範例下游。 篩選器的輸入釘選和輸出 pin 一律會與相符的媒體類型連接。
-   [**CVideoTransformFilter**](cvideotransformfilter.md) 主要是針對影片解碼器所設計。 它衍生自 **CTransformFilter**，但是如果下游轉譯器落在後方，則包含卸載框架的功能。
-   [**CBaseFilter**](cbasefilter.md) 是泛型篩選類別。 這份清單中的其他類別全都衍生自 **CBaseFilter**。 如果它們都不適用，您可以回到這個類別。 不過，此類別也需要您最多的工作。
-   \[!重要\]  
    > 就地影片轉換可能會對轉譯效能產生嚴重的影響。 就地轉換需要緩衝區上的讀寫寫入作業。 如果記憶體位於圖形配接器上，讀取作業的速度會明顯較慢。 此外，即使您不小心執行複製轉換，也可能會造成非預期的讀取作業。 因此，如果您撰寫影片轉換，則應該一律執行效能測試。

     

若為範例 RLE 編碼器，最佳選擇是 **CTransformFilter** 或 **CVideoTransformFilter**。 事實上，它們之間的差異大多是內部的，因此很容易就能從一個轉換成另一個。 因為這兩個 pin 上的媒體類型必須不同，所以 **CTransInPlaceFilter** 類別不適合此篩選器。 此範例會使用 **CTransformFilter**。

下一 [步：步驟2。宣告篩選類別](step-2--declare-the-filter-class.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



