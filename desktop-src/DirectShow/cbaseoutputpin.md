---
description: CBaseOutputPin 類別是一種抽象基類，可實作為輸出的釘選。
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: 'CBaseOutputPin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67a4051f904b27b75273d553e1d0604b068b3910fbfb322b5a2df716c996a1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872581"
---
# <a name="cbaseoutputpin-class"></a>CBaseOutputPin 類別

![cbaseoutputpin 類別階層](images/filter06.png)

`CBaseOutputPin`類別是一種抽象基類，可實作為輸出的釘選。

這個類別衍生自 [**CBasePin**](cbasepin.md)。 這與 **CBasePin** 的差異在於下列各方面：

-   它只會連線到支援 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的輸入圖釘。
-   它支援透過 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的本機記憶體傳輸。
-   它會拒絕資料流程結束、排清和新區段的通知。  (不應將這些傳送至輸出釘選。 ) 
-   它提供了提供下游範例的方法。

當 pin 連接時，它會向輸入 pin 要求記憶體配置器。 若失敗，則會建立新的配置器物件。 輸出針腳負責設定配置器屬性。 它會透過純虛擬方法 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md)。 在您的衍生類別中覆寫這個方法。 如果輸入 pin 具有任何緩衝區需求，則會將它們傳遞給 **DecideBufferSize** 方法。

呼叫 [**CBaseOutputPin：： GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) 方法以取得空白媒體範例。 呼叫 [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md) 方法以傳遞下游範例。

您的衍生類別必須覆寫純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，以在 pin 連接期間驗證媒體類型。



| 受保護的成員變數                                      | 描述                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseoutputpin-m-pallocator.md)            | 記憶體配置器的指標。                                           |
| [**m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md)              | 連接到此 pin 之輸入連接的指標。                            |
| 公用方法                                                  | 描述                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | 函式方法。                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | 完成輸入 pin 的連接。 虛擬。                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | 選取記憶體配置器。 虛擬。                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | 抓取包含空緩衝區的媒體範例。 虛擬。           |
| [**提供**](cbaseoutputpin-deliver.md)                       | 將媒體範例傳遞至連線的輸入 pin。 虛擬。               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | 建立記憶體配置器。 虛擬。                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | 判斷 pin 連接是否合適。                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | 釋放連接的 pin。                                        |
| [**使用中**](cbaseoutputpin-active.md)                         | 通知釘選篩選現在已啟用。                            |
| [**非使用中**](cbaseoutputpin-inactive.md)                     | 通知 pin 此篩選已不再有效。                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | 將資料流程結束通知傳遞至連線的輸入 pin。虛擬。 |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | 要求連接的輸入 pin 以開始清除作業。 虛擬。      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | 要求連接的輸入 pin 以結束排清操作。 虛擬。        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | 將新區段通知傳遞至連線的輸入 pin。 虛擬。   |
| 純虛擬方法                                            | 描述                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | 設定緩衝區需求。                                              |
| IPin 方法                                                    | 描述                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | 開始清除作業。                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | 結束清除操作。                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | 通知 pin，不需要額外的資料。                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




