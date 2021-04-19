---
description: CTransInPlaceOutputPin 類別會實 CTransInPlaceFilter 類別所使用的輸出圖釘。
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: 'CTransInPlaceOutputPin 類別 (Transip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990040"
---
# <a name="ctransinplaceoutputpin-class"></a>CTransInPlaceOutputPin 類別

![ctransinplaceoutputpin 類別階層](images/tsip02.png)

`CTransInPlaceOutputPin`類別會實 [**CTransInPlaceFilter**](ctransinplacefilter.md)類別所使用的輸出圖釘。

一般而言，您不需要從此類別衍生。 如果您這麼做，就必須覆寫篩選的 [**CTransInPlaceFilter：： GetPin**](ctransinplacefilter-getpin.md) 方法，以建立衍生類別的實例。



| 受保護的成員變數                                                      | Description                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | 建立此釘選之篩選準則的指標。         |
| 公用方法                                                                  | Description                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | 函式方法。                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | 判斷 pin 是否接受特定的媒體類型。 |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | 指定連接的配置器。           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | 抓取下游輸入圖釘的指標。     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | 捕獲釘選配置器的指標。          |
| IPin 方法                                                                    | Description                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | 列舉釘選的慣用媒體類型。          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




