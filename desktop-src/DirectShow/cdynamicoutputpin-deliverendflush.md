---
description: CDynamicOutputPin. DeliverEndFlush 方法-DeliverEndFlush 方法會要求連接的輸入 pin，以結束清除作業。
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: 'CDynamicOutputPin. DeliverEndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cdd7e26b0c08b154c6cffd08066e8ae841a6aa849db4751ffa0cdf252848719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055948"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>CDynamicOutputPin. DeliverEndFlush 方法

`DeliverEndFlush`方法會要求連接的輸入 pin 以結束排清作業。

## <a name="syntax"></a>語法


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseOutputPin：:D eliverendflush**](cbaseoutputpin-deliverendflush.md) 方法。 它會重設 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




