---
description: CTransformInputPin 類別會實 CTransformFilter 類別所使用的輸入 pin。
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: 'CTransformInputPin 類別 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3df5da0ee6e80dd1da147563ef698a520222531de5cee9656ec52cb14301f66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087010"
---
# <a name="ctransforminputpin-class"></a>CTransformInputPin 類別

![ctransforminputpin 類別階層](images/tfrm01.png)

`CTransformInputPin`類別會實 [**CTransformFilter**](ctransformfilter.md)類別所使用的輸入 pin。

一般而言，您不需要從此類別衍生。 此類別中大部分的方法會呼叫 **CTransformFilter** 類別上的對應方法，而您可以覆寫這個方法。 如果您衍生自這個類別，您必須覆寫篩選的 [**CTransformFilter：： GetPin**](ctransformfilter-getpin.md) 方法，以建立衍生類別的實例。



| 受保護的成員變數                                           | 描述                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransforminputpin-m-ptransformfilter.md) | 擁有篩選準則的指標。                                                          |
| 公用方法                                                       | 描述                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | 函式方法。                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | 判斷 pin 連接是否合適。                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | 釋放連接的 pin。                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | 完成與另一個 pin 的連接。                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | 判斷 pin 是否接受特定的媒體類型。                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | 設定連接的媒體類型。                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | 判斷 pin 是否可以接受範例。 虛擬。                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | 抓取目前 pin 連接的媒體類型。                               |
| IPin 方法                                                         | 描述                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | 抓取 pin 的識別碼。                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | 通知 pin，不需要額外的資料。                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | 開始清除作業。                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | 結束清除操作。                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | 通知釘選將此呼叫群組為區段之後所收到的媒體範例。 |
| IMemInputPin 方法                                                 | 描述                                                                            |
| [**收到**](ctransforminputpin-receive.md)                        | 接收資料流程中的下一個媒體範例。                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




