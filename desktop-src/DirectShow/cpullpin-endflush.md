---
description: EndFlush 方法會通知擁有篩選以結束清除作業。 衍生的類別必須執行此方法。
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: 'CPullPin. EndFlush 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999450"
---
# <a name="cpullpinendflush-method"></a>CPullPin. EndFlush 方法

`EndFlush`方法會通知擁有篩選以結束清除作業。 衍生的類別必須執行此方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

[**CPullPin：： Seek**](cpullpin-seek.md)方法會呼叫這個方法。 在每個從這個物件接收資料的下游輸入 pin 上，執行此方法以呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。 如果您篩選的輸出 pin (s) 衍生自 **CBaseOutputPin**，請呼叫 **CBaseOutputPin：:D eliverendflush** 方法。

這項設計可讓篩選準則直接在 **CPullPin** 物件上呼叫 **seek** 來搜尋資料流程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




