---
description: CBaseInputPin 類別是用來執行輸入圖釘的抽象基類。 除了 CBasePin 提供的 IPin 介面支援之外，此類別還新增了 IMemInputPin 介面的支援。
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: 'CBaseInputPin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab98a2dcb1503e7593912df0e5dff51539855611311d4704e4045816fd6380e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823880"
---
# <a name="cbaseinputpin-class"></a>CBaseInputPin 類別

![cbaseinputpin 類別階層](images/filter07.png)

`CBaseInputPin`類別是用來執行輸入圖釘的抽象基類。 除了 [**CBasePin**](cbasepin.md)提供的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面支援之外，此類別還新增了 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)介面的支援。

若要使用此類別，請衍生新的類別，並至少覆寫下列方法：

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

根據 pin 的函式，您可能需要覆寫或 CBasePin 中的其他 `CBaseInputPin` 方法。



| 受保護的成員變數                                                 | 描述                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseinputpin-m-pallocator.md)                        | 記憶體配置器的指標。                                                                            |
| [**m \_ bReadOnly**](cbaseinputpin-m-breadonly.md)                          | 指出配置器是否會產生唯讀媒體範例的旗標。                                 |
| [**m \_ bFlushing**](cbaseinputpin-m-bflushing.md)                          | 指出釘選是否正在排清的旗標。                                                  |
| [**m \_ SampleProps**](cbaseinputpin-m-sampleprops.md)                      | 最新範例的屬性。                                                                       |
| 公用方法                                                             | 描述                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | 函式方法。                                                                                         |
| [**~ CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | 函式方法。                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | 釋放連接的 pin。                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | 查詢配置器是否使用唯讀媒體範例。                                                 |
| [**IsFlushing**](cbaseinputpin-isflushing.md)                             | 查詢篩選目前是否正在排清。                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | 判斷 pin 是否可以接受範例。 虛擬。                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | 將品質控制訊息傳遞至適當的物件。                                                 |
| [**非使用中**](cbaseinputpin-inactive.md)                                 | 通知 pin 此篩選已不再有效。 虛擬。                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | 抓取最新範例的屬性。                                                         |
| IPin 方法                                                               | 描述                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | 開始清除作業。                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | 結束清除操作。                                                                                     |
| IMemInputPin 方法                                                       | 描述                                                                                                 |
| [**GetAllocator**](cbaseinputpin-getallocator.md)                         | 抓取此 pin 提議的記憶體配置器。                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | 指定連接的配置器。                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | 抓取輸入 pin 所要求的配置器屬性。                                              |
| [**收到**](cbaseinputpin-receive.md)                                   | 接收資料流程中的下一個媒體範例。                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | 接收資料流程中的多個範例。                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | 判斷 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法的呼叫是否可能封鎖。 |
| IQualityControl 方法                                                    | 描述                                                                                                 |
| [**通知**](cbaseinputpin-notify.md)                                     | 接收品質控制訊息。                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




