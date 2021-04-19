---
description: CTransInPlaceFilter 類別是針對就地轉換篩選所設計，而篩選準則會修改輸入資料，而不是跨緩衝區複製資料。若要使用此類別，請從 CTransInPlaceFilter 衍生新的類別，並執行下列方法：
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: 'CTransInPlaceFilter 類別 (Transip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f59dd312adbb95797caf695aecea082f296df5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983135"
---
# <a name="ctransinplacefilter-class"></a>CTransInPlaceFilter 類別

![ctransinplacefilter 類別階層](images/tsip03.png)

`CTransInPlaceFilter`類別是針對就地轉換篩選所設計，而這些篩選準則是修改輸入資料的篩選，而不是跨緩衝區複製資料。若要使用這個類別，請從衍生新的類別， `CTransInPlaceFilter` 並執行下列方法：

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransInPlaceFilter：： Transform**](ctransinplacefilter-transform.md)

這個類別會針對其輸入的 pin 使用 [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) 類別，並使用其輸出圖釘的 [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) 類別。 一般而言，您不需要覆寫這些釘選類別。 此篩選器會在 [**CTransInPlaceFilter：： GetPin**](ctransinplacefilter-getpin.md) 方法中建立這兩個 pin。 如果您確實覆寫了釘選類別，則必須覆寫 **GetPin** 以建立自訂 pin。

此類別的設計目的是讓輸入類型永遠符合輸出類型。 如果可能的話，篩選器會針對這兩個 pin 連接使用單一配置器。

## <a name="preferred-media-types"></a>慣用的媒體類型

如果輸出釘選已連接，則輸入 pin 會提供下游篩選器的慣用類型。  (事實上，它只會傳回下游篩選器的列舉值物件 ) 。否則，就不會有任何慣用的類型。 輸出 pin 具有相同的行為，但反向：如果輸入的連接已連接，則輸出 pin 會提供上游篩選器的慣用類型。 否則，它沒有慣用的類型

## <a name="pin-connections"></a>Pin 連接

當一個 pin 連線時，篩選通常會重新連接其他 pin，以確定這兩個 pin 都使用相同的媒體類型和相同的配置器。  (重新連接的 [pin](reconnecting-pins.md)會描述重新連接 pin 的機制 ) 。可能的方法有兩種：輸入 pin 會先連接，或輸出 pin 會先連接。

假設輸入 pin 會先連接。 會進行下列步驟：

1.  輸入的 pin 會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。
2.  上游篩選器會選取配置器。 此時，輸入 pin 沒有配置器需求，而且會接受連接的任何配置器。 如果上游篩選要求配置器，則 pin 會建立一個新的配置器。 基於稍後所述的原因，此配置器將不會用於最終連接。 它僅提供協助完成此連接程式階段。

稍後，當輸出 pin 連接時：

1.  輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。 它也會呼叫上游篩選器上的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。 這可確保輸入 pin 可以變更其媒體類型以符合。
2.  輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。 它也會呼叫上游篩選器上的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。 這可確保輸入 pin 可以變更其媒體類型以符合。
3.  輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。 它也會呼叫上游篩選器上的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。 這可確保輸入 pin 可以變更其媒體類型以符合。
4.  這次，輸入 pin 的 [**GetAllocator**](ctransinplaceinputpin-getallocator.md) 方法會傳回下游配置器，而 [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) 會傳回下游篩選器的配置器需求。 輸入 pin 會接受上游篩選器選擇的任何配置器。
5.  這次，輸入 pin 的 [**GetAllocator**](ctransinplaceinputpin-getallocator.md) 方法會傳回下游配置器，而 [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) 會傳回下游篩選器的配置器需求。 輸入 pin 會接受上游篩選器選擇的任何配置器。

現在請考慮相反的案例，其中的輸出圖釘是要連接的第一個 pin。

1.  輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。
2.  它會選取配置器，並偏好使用下游篩選器的配置器。

然後，當輸入 pin 連接時：

1.  輸入 pin 會藉由在篩選上呼叫 [**CheckInputType**](ctransformfilter-checkinputtype.md) ，以及在下游篩選器的輸出圖釘上呼叫 [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ，來檢查媒體類型。
2.  如果輸入類型與輸出類型不符，則篩選會重新連接輸出的釘選。
3.  上游篩選器會選取配置器。 輸入 pin 的 [**GetAllocator**](ctransinplaceinputpin-getallocator.md) 方法會傳回下游配置器，而輸入 pin 會接受上游篩選器所選取的任何配置器。
4.  此篩選器會使用相同的配置器進行下游連接，可能會覆寫原始的下游配置器。

如果任何相關的配置器是唯讀的，這一系列的事件就會稍微變更，因為下游配置器必須是可寫入的。 在此情況下，篩選可能會使用兩個不同的配置器。

如需使用這個類別的詳細資訊，請參閱 [寫入轉換篩選](writing-transform-filters.md)。



| 受保護的成員變數                                                        | Description                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**m \_ bModifiesData**](ctransinplacefilter-m-bmodifiesdata.md)                   | 指出篩選準則是否修改範例資料。                           |
| 保護方法                                                                 | Description                                                                      |
| [**複製**](ctransinplacefilter-copy.md)                                          | 複製媒體範例。                                                           |
| [**InputPin**](ctransinplacefilter-inputpin.md)                                  | 抓取篩選的輸入圖釘指標。                                   |
| [**OutputPin**](ctransinplacefilter-outputpin.md)                                | 抓取篩選的輸出圖釘指標。                                  |
| [**TypesMatch**](ctransinplacefilter-typesmatch.md)                              | 判斷輸入媒體類型是否符合輸出媒體類型。           |
| [**UsingDifferentAllocators**](ctransinplacefilter--usingdifferentallocators.md) | 判斷輸入和輸出圖釘是否使用不同的配置器。     |
| 公用方法                                                                    | Description                                                                      |
| [**CTransInPlaceFilter**](ctransinplacefilter-ctransinplacefilter.md)            | 函式方法。                                                              |
| [**GetPin**](ctransinplacefilter-getpin.md)                                      | 捕獲 pin。                                                                 |
| [**GetMediaType**](ctransinplacefilter-getmediatype.md)                          | 抓取輸出圖釘的慣用媒體類型。                             |
| [**DecideBufferSize**](ctransinplacefilter-decidebuffersize.md)                  | 設定輸出釘選的緩衝區需求。                                       |
| [**CheckTransform**](ctransinplacefilter-checktransform.md)                      | 檢查輸入媒體類型是否與輸出媒體類型相容。      |
| [**CompleteConnect**](ctransinplacefilter-completeconnect.md)                    | 完成 pin 連接。                                                      |
| [**收到**](ctransinplacefilter-receive.md)                                    | 接收媒體範例、進行處理，並將其傳遞至下游篩選器。 |
| 純虛擬方法                                                              | Description                                                                      |
| [**Transform**](ctransinplacefilter-transform.md)                                | 就地轉換範例。                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




