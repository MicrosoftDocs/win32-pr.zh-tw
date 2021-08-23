---
description: CTransformFilter 類別是用來執行轉換篩選準則的基類。
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: 'CTransformFilter 類別 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9d199a406fa1934fb63625cd258baee8d69c20c17992a7d1d3bbd2c83956a1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633890"
---
# <a name="ctransformfilter-class"></a>CTransformFilter 類別

![ctransformfilter 類別階層](images/tfrm03.png)

`CTransformFilter`類別是用來執行轉換篩選準則的基類。 此類別的設計目的是要使用一個輸入釘選和一個輸出圖釘來執行轉換篩選。 它會針對輸入的 pin 和輸出 pin 使用不同的配置器。 若要建立可就地處理資料的篩選，請使用 [**CTransInPlaceFilter**](ctransinplacefilter.md) 類別。

此篩選器會使用 [**CTransformInputPin**](ctransforminputpin.md) 類別做為其輸入的 pin，並使用其輸出圖釘的 [**CTransformOutputPin**](ctransformoutputpin.md) 類別。 一般而言，您不需要覆寫這些釘選類別。 大部分的 pin 方法會在類別上呼叫對應 `CTransformFilter` 的方法，因此您可以視需要覆寫篩選準則方法。 此篩選器會在 [**CTransformFilter：： GetPin**](ctransformfilter-getpin.md) 方法中建立這兩個 pin。 如果您確實覆寫了釘選類別，則必須覆寫 **GetPin** 以建立自訂 pin。

若要使用這個類別，請從衍生新的類別， `CTransformFilter` 並執行下列方法：

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter：:D ecideBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter：： Transform**](ctransformfilter-transform.md)

您可能也需要覆寫其他方法，視篩選準則的需求而定。

## <a name="media-types"></a>媒體類型

此篩選器的輸入 pin 不會建議任何媒體類型;它依賴上游篩選器來提議媒體類型以進行連線。 這種設計的原因是，在大部分情況下，上游篩選器可以提供有關格式的詳細資訊。 例如，使用影片格式時，上游篩選器會得知影片尺寸和畫面播放速率，而轉換篩選無法判斷這種資訊。 如果您想要變更此行為，請覆寫輸入釘選的 [**GetMediaType**](ctransformfilter-getmediatype.md) 方法。 當上游篩選提議媒體類型時，輸入 pin 會將篩選的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法 (單純的虛擬) 來呼叫。

在輸入 pin 連線之前，輸出 pin 會拒絕所有連線，而且不會傳回任何慣用的媒體類型。 連接輸入連接之後，輸出圖釘會藉由呼叫篩選器的 [**GetMediaType**](ctransformfilter-getmediatype.md) 方法來傳回慣用類型清單。 它會透過篩選的 [**CheckTransform**](ctransformfilter-checktransform.md) 方法來檢查連接的輸出類型。  (兩種方法都是純虛擬的。 ) 通常，輸入類型會部分決定可接受的輸出類型。

根據篩選準則，您可能會想要註冊某些篩選器支援的媒體類型，讓 [篩選器](filter-mapper.md) 對應程式物件可以找到您的篩選準則。 如需詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。

## <a name="streaming"></a>串流

此類別不會將輸出資料排在佇列中。 每個輸出範例都會在 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法內傳遞。 **Receive 方法會** 呼叫篩選準則的 [**轉換**](ctransformfilter-transform.md)方法， (也是單純的虛擬) 來處理資料。

如需使用這個類別的詳細資訊，請參閱 [寫入轉換篩選](writing-transform-filters.md)。



| 受保護的成員變數                                                | 描述                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ bEOSDelivered**](ctransformfilter-m-beosdelivered.md)              | 指出篩選是否已傳送資料流程結束通知的旗標。                          |
| [**m \_ bSampleSkipped**](ctransformfilter-m-bsampleskipped.md)            | 指出最近樣本是否已卸載的旗標。                                         |
| [**m \_ bQualityChanged**](ctransformfilter-m-bqualitychanged.md)          | 指出品質是否已變更的旗標。                                                    |
| [**m \_ csFilter**](ctransformfilter-m-csfilter.md)                        | 保護篩選狀態的重要區段。                                                        |
| [**m \_ csReceive**](ctransformfilter-m-csreceive.md)                      | 保護串流狀態的重要區段。                                                     |
| [**m \_ pInput**](ctransformfilter-m-pinput.md)                            | 輸入釘選的指標。                                                                               |
| [**m \_ pOutput**](ctransformfilter-m-poutput.md)                          | 輸出圖釘的指標。                                                                              |
| 公用方法                                                            | 描述                                                                                             |
| [**CTransformFilter**](ctransformfilter-ctransformfilter.md)             | 函式方法。                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | 函式方法。                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | 抓取篩選上的釘選數目。 虛擬。                                                    |
| [**GetPin**](ctransformfilter-getpin.md)                                 | 捕獲 pin。 虛擬。                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | 轉換輸入範例以產生輸出範例。 虛擬。                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | 當篩選參數切換為暫停狀態時呼叫。 虛擬。                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | 當篩選參數切換至 [已停止] 狀態時呼叫。 虛擬。                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | 通知篩選準則要求品質變更。 虛擬。                                        |
| [**SetMediaType**](ctransformfilter-setmediatype.md)                     | 當媒體類型設定于其中一個篩選器的 pin 時呼叫。 虛擬。                                 |
| [**CheckConnect**](ctransformfilter-checkconnect.md)                     | 判斷 pin 連接是否合適。 虛擬。                                               |
| [**BreakConnect**](ctransformfilter-breakconnect.md)                     | 釋放連接的 pin。 虛擬。                                                              |
| [**CompleteConnect**](ctransformfilter-completeconnect.md)               | 完成 pin 連接。 虛擬。                                                                    |
| [**收到**](ctransformfilter-receive.md)                               | 接收媒體範例、處理它，然後將輸出範例傳遞給下游篩選器。 虛擬。 |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | 捕獲新的輸出範例，並將它初始化。                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | 通知篩選準則，輸入 pin 不需要任何其他資料。 虛擬。                    |
| [**BeginFlush**](ctransformfilter-beginflush.md)                         | 開始清除作業。 虛擬。                                                                      |
| [**EndFlush**](ctransformfilter-endflush.md)                             | 結束清除操作。 虛擬。                                                                        |
| [**NewSegment**](ctransformfilter-newsegment.md)                         | 通知篩選此呼叫之後所收到的媒體範例會分組為區段。 虛擬。      |
| 純虛擬方法                                                      | 描述                                                                                             |
| [**CheckInputType**](ctransformfilter-checkinputtype.md)                 | 檢查輸入是否可接受指定的媒體類型。                                          |
| [**CheckTransform**](ctransformfilter-checktransform.md)                 | 檢查輸入媒體類型是否與輸出媒體類型相容。                             |
| [**DecideBufferSize**](ctransformfilter-decidebuffersize.md)             | 設定輸出釘選的緩衝區需求。                                                              |
| [**GetMediaType**](ctransformfilter-getmediatype.md)                     | 抓取輸出圖釘的慣用媒體類型。                                                    |
| IMediaFilter 方法                                                      | 描述                                                                                             |
| [**停止**](ctransformfilter-stop.md)                                     | 停止篩選。                                                                                       |
| [**暫停**](ctransformfilter-pause.md)                                   | 暫停篩選。                                                                                      |
| IBaseFilter 方法                                                       | 描述                                                                                             |
| [**FindPin**](ctransformfilter-findpin.md)                               | 使用指定的識別碼抓取 pin。                                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




