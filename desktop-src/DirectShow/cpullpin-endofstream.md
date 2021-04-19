---
description: EndOfStream 方法會在物件傳遞最後一個樣本之後呼叫。 衍生的類別必須執行此方法。
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: 'CPullPin. EndOfStream 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979516"
---
# <a name="cpullpinendofstream-method"></a>CPullPin. EndOfStream 方法

在 `EndOfStream` 物件傳遞最後一個範例之後，會呼叫方法。 衍生的類別必須執行此方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

您可以使用這個方法，在每個從這個物件接收資料的下游輸入 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 。 如果您篩選的輸出 pin (s) 衍生自 [**CBaseOutputPin**](cbaseoutputpin.md)，請呼叫 [**CBaseOutputPin：:D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




