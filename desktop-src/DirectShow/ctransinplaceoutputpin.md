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
ms.openlocfilehash: 2462843f9ad42793a9e0666dd96aaf7387a1f5f0f1749f97cc4e2ca4d3ed051a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076150"
---
# <a name="ctransinplaceoutputpin-class"></a>CTransInPlaceOutputPin 類別

![ctransinplaceoutputpin 類別階層](images/tsip02.png)

`CTransInPlaceOutputPin`類別會實 [**CTransInPlaceFilter**](ctransinplacefilter.md)類別所使用的輸出圖釘。

一般而言，您不需要從此類別衍生。 如果您這麼做，就必須覆寫篩選的 [**CTransInPlaceFilter：： GetPin**](ctransinplacefilter-getpin.md) 方法，以建立衍生類別的實例。



| 受保護的成員變數                                                      | 描述                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | 建立此釘選之篩選準則的指標。         |
| 公用方法                                                                  | 描述                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | 函式方法。                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | 判斷 pin 是否接受特定的媒體類型。 |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | 指定連接的配置器。           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | 抓取下游輸入圖釘的指標。     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | 捕獲釘選配置器的指標。          |
| IPin 方法                                                                    | 描述                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | 列舉釘選的慣用媒體類型。          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




