---
description: CEnumMediaTypes 類別會實作為慣用媒體類型的列舉值。
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: 'CEnumMediaTypes 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990065"
---
# <a name="cenummediatypes-class"></a>CEnumMediaTypes 類別

![cenummediatypes 類別階層](images/filter04.png)

類別會實 `CEnumMediaTypes` 作為慣用媒體類型的列舉值。

這個類別會實 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面。 它會呼叫下列 [**CBasePin**](cbasepin.md) 方法：

-   [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md)：抓取以零為基底之索引所參考的媒體類型。
-   [**CBasePin：： GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)：判斷慣用類型集合是否已變更。

只要 pin 改變其慣用媒體類型的清單，pin 就會遞增媒體類型的版本號碼。 當這種情況發生時，列舉值物件就不會再與釘選同步，而類別方法會傳回 VFW \_ E \_ 列舉不 \_ \_ \_ 同步。 呼叫 [**CEnumMediaTypes：： Reset**](cenummediatypes-reset.md) 方法來重新同步處理列舉值。



| 公用方法                                               | Description                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | 函式方法。                                             |
| [**~ CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | 函式方法。 虛擬。                                     |
| IEnumMediaTypes 方法                                      | Description                                                     |
| [**克隆**](cenummediatypes-clone.md)                       | 使用相同的列舉狀態建立列舉值的複本。 |
| [**下一步**](cenummediatypes-next.md)                         | 抓取指定的媒體類型數目。                    |
| [**重設**](cenummediatypes-reset.md)                       | 將列舉序列重設為開頭。               |
| [**跳過**](cenummediatypes-skip.md)                         | 略過指定數目的媒體類型。                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




