---
description: 'QueryAccept (下游) '
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: 'QueryAccept (下游) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ec5c26209839f0dcd8351cc9a7ca84227faa2289d44d46c2c321fce0429e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747730"
---
# <a name="queryaccept-downstream"></a>QueryAccept (下游) 

這種機制可讓輸出釘選將新格式提議至其下游對等。 新的格式不能需要較大的緩衝區大小。 輸出圖釘會執行下列動作：

1.  在下游 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 或 [**IPinConnection：:D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) ，以驗證另一個 pin 是否可以接受新的媒體類型 (請參閱說明，步驟) 。
2.  如果步驟1中的傳回值是 \_ [確定]，則 pin 會將媒體類型附加至下一個範例。 若要這樣做，請先呼叫 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 來取得範例 (B) 。 然後，它會呼叫 [**IMediaSample：： SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) ，將媒體類型附加至 (C) 的範例。 藉由將媒體類型附加至範例，篩選器會指出格式已變更，從該範例開始。
3.  Pin 可傳遞範例 (D) 。
4.  當下游篩選器收到範例時，它會呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 來取出新的媒體類型。

    ![queryaccept (下游) ](images/dynformat3.png)

所有 pin 都支援此 `QueryAccept` 方法。 不過，這個方法會稍微不明確，因為 S 的傳回值 \_ 不一定保證您可以在圖形作用時變更格式。 某些篩選器可能會傳回 \_ [確定]，但如果圖形正在使用中，則會拒絕變更。 某些輸入圖釘所支援的 **DynamicQueryAccept** 方法，會明確定義 S OK， \_ 以表示 pin 可以在使用中時變更格式。 如果輸入 pin 支援 **IPinConnection** 介面，您應該呼叫 **DynamicQueryAccept** 而不是 `QueryAccept` 。

在大部分的情況下，此機制不允許對格式進行重大變更，例如變更位深度。 您可以使用的其中一種方式是當影片解碼器切換調色板時。 格式的基本詳細資料會保持不變，例如影像尺寸和位深度，但新的媒體類型會有一組不同的調色板專案。

**執行附注**

在 DirectShow 基類中， [**CBasePin：： QueryAccept**](cbasepin-queryaccept.md)會呼叫 **CheckMediaType** 方法，這個方法也會在初始 pin 連接期間呼叫。 在轉換篩選準則的案例中，輸入 pin 的 **CheckMediaType** 方法應該一律檢查輸出釘選是否已連接，如果是，輸入媒體類型是否與輸出媒體類型相容。 因此，此實作為的可能會是有效的 `QueryAccept` 。 如果沒有，您應該覆寫以便 `QueryAccept` 執行任何其他必要的檢查。 另請注意， [**CTransformFilter**](ctransformfilter.md) 類別會在 **CheckInputType** 和 **CheckTransform** 方法中封裝此邏輯。 另一方面， [**CTransInPlaceFilter**](ctransinplacefilter.md) 類別一律會呼叫 `QueryAccept` 下一個上游或下游篩選。

[**CBaseInputPin：： Receive**](cbaseinputpin-receive.md)方法會檢查傳入範例上的媒體類型，如果有的話，則會呼叫 **CheckMediaType**。 但是，它並不會更新釘選的 **m \_ mt** 成員，它會保留目前的媒體類型。 當您的篩選器處理範例時，您應該檢查範例中的媒體類型。 如果有新的類型，您可能需要在 pin 上呼叫 **SetMediaType** ，或直接設定 **m \_ mt** 的值來儲存它。 另一方面， [**CVideoTransformFilter**](cvideotransformfilter.md) 類別是針對影片轉換篩選而設計，它會在變更時儲存媒體類型。 如需詳細資訊，請參閱 DirectShow 基礎類別庫中的 [**CVideoTransformFilter：： Receive**](cvideotransformfilter-receive.md)的原始程式碼。

在某些情況下，您可以直接將 `QueryAccept` 呼叫傳遞給下游，然後將媒體類型附加至輸出範例，並讓下游篩選器處理格式變更。

 

 



