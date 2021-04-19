---
description: CEnumPins 類別會為 pin 實作為列舉值。
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: 'CEnumPins 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994363"
---
# <a name="cenumpins-class"></a>CEnumPins 類別

![cenumpins 類別階層](images/filter03.png)

`CEnumPins`類別會為 pin 實作為列舉值。

這個類別會實 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面。 它會呼叫下列 [**CBaseFilter**](cbasefilter.md) 方法：

-   [**CBaseFilter：： GetPin**](cbasefilter-getpin.md)：抓取篩選上的釘選，以零為基底的索引參考。
-   [**CBaseFilter：： GetPinCount**](cbasefilter-getpincount.md)：抓取篩選上的釘選總數。
-   [**CBaseFilter：： GetPinVersion**](cbasefilter-getpinversion.md)：判斷釘選是否已變更。

如果篩選動態建立或終結 pin，則會在 pin 變更時遞增 pin 版本。 如果版本號碼變更，列舉值物件就不會再與篩選準則同步。 列舉值不同步之後，中的方法會傳回 `CEnumPins` VFW \_ E \_ 列舉不 \_ \_ \_ 同步。 呼叫 [**CEnumPins：： Reset**](cenumpins-reset.md) 方法來重新同步處理列舉值。



| 公用方法                             | Description                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | 函式方法。                                             |
| [**~ CEnumPins**](cenumpins--cenumpins.md) | 函式方法。 虛擬。                                     |
| IEnumPins 方法                          | Description                                                     |
| [**克隆**](cenumpins-clone.md)           | 使用相同的列舉狀態建立列舉值的複本。 |
| [**下一步**](cenumpins-next.md)             | 抓取指定的 pin 數目。                           |
| [**重設**](cenumpins-reset.md)           | 將列舉序列重設為開頭。               |
| [**跳過**](cenumpins-skip.md)             | 略過指定的 pin 數目。                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




