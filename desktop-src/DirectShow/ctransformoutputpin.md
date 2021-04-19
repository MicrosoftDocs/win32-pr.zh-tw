---
description: CTransformOutputPin 類別會實 CTransformFilter 類別所使用的輸出圖釘。
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: 'CTransformOutputPin 類別 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993650"
---
# <a name="ctransformoutputpin-class"></a>CTransformOutputPin 類別

![ctransformoutputpin 類別階層](images/tfrm02.png)

`CTransformOutputPin`類別會實 [**CTransformFilter**](ctransformfilter.md)類別所使用的輸出圖釘。

一般而言，您不需要從此類別衍生。 此類別中大部分的方法會呼叫 **CTransformFilter** 類別上的對應方法，而您可以覆寫這個方法。 如果您衍生自這個類別，您必須覆寫篩選的 [**CTransformFilter：： GetPin**](ctransformfilter-getpin.md) 方法，以建立衍生類別的實例。

這個類別會透過 [**CPosPassThru**](cpospassthru.md)物件公開 **IMediaSeeking** 和 **IMediaPosition** 介面。 它會將所有搜尋要求傳遞至下一個篩選上游。



| 受保護的成員變數                                               | Description                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransformoutputpin-m-ptransformfilter.md)    | 擁有篩選準則的指標。                            |
| Public 成員變數                                                  | Description                                              |
| [**m \_ pPosition**](ctransformoutputpin-m-pposition.md)                  | 要傳遞向上游傳遞搜尋命令的 Helper 物件。            |
| 公用方法                                                           | Description                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | 函式方法。                                      |
| [**~ CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | 函式方法。                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | 判斷 pin 連接是否合適。         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | 釋放連接的 pin。                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | 完成與另一個 pin 的連接。                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | 判斷 pin 是否接受特定的媒體類型。     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | 設定連接的媒體類型。                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | 設定緩衝區需求。                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | 依索引值抓取慣用的媒體類型。        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | 抓取目前 pin 連接的媒體類型。 |
| IPin 方法                                                             | Description                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | 抓取 pin 的識別碼。                     |
| IQualityControl 方法                                                  | Description                                              |
| [**Notify**](ctransformoutputpin-notify.md)                             | 通知 pin 已要求品質變更。     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




