---
description: BeginFlush 方法會通知擁有篩選以排清下游篩選。 衍生的類別必須執行此方法。
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: 'CPullPin. BeginFlush 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c7998c1c38a533d67edcd2cc237188a627ec8258a8b0349066e31ecf0fbaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687748"
---
# <a name="cpullpinbeginflush-method"></a>CPullPin. BeginFlush 方法

`BeginFlush`方法會通知擁有篩選以排清下游篩選。 衍生的類別必須執行此方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

[**CPullPin：： Seek**](cpullpin-seek.md)方法會呼叫這個方法。 在每個從這個物件接收資料的下游輸入 pin 上，執行此方法以呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。 如果您篩選的輸出 pin (s) 衍生自 [**CBaseOutputPin**](cbaseoutputpin.md)，請呼叫 [**CBaseOutputPin：:D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) 方法。

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

 

 




