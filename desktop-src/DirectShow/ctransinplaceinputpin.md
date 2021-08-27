---
description: CTransInPlaceInputPin 類別會實 CTransInPlaceFilter 類別所使用的輸入 pin。
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: 'CTransInPlaceInputPin 類別 (Transip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04d30b18d115e7ef03e88deb47355bafc795532a91afa14cf2f4392e658954f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076191"
---
# <a name="ctransinplaceinputpin-class"></a>CTransInPlaceInputPin 類別

![ctransinplaceinputpin 類別階層](images/tsip01.png)

`CTransInPlaceInputPin`類別會實 [**CTransInPlaceFilter**](ctransinplacefilter.md)類別所使用的輸入 pin。

一般而言，您不需要從此類別衍生。 如果您這麼做，就必須覆寫篩選的 [**CTransInPlaceFilter：： GetPin**](ctransinplacefilter-getpin.md) 方法，以建立衍生類別的實例。



| 受保護的成員變數                                                          | 描述                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md)                           | 指定輸入資料流程是否為唯讀的旗標。 |
| [**m \_ pTIPFilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | 建立此釘選之篩選準則的指標。               |
| 公用方法                                                                      | 描述                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | 函式方法。                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | 判斷 pin 是否接受特定的媒體類型。       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | 捕獲釘選配置器的指標。                |
| [**ReadOnly**](ctransinplaceinputpin-readonly.md)                                  | 指出輸入資料流程是否為唯讀。           |
| IPin 方法                                                                        | 描述                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | 列舉釘選的慣用媒體類型。                |
| IMemInputPin 方法                                                                | 描述                                                |
| [**GetAllocator**](ctransinplaceinputpin-getallocator.md)                          | 抓取此 pin 提議的記憶體配置器。       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | 指定連接的配置器。                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | 抓取 pin 所要求的配置器屬性。   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




