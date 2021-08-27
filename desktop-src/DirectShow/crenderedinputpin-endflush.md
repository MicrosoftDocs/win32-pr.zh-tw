---
description: CRenderedInputPin. EndFlush 方法-EndFlush 方法會結束清除作業。 這個方法會實 IPin：： EndFlush 方法。
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: 'CRenderedInputPin. EndFlush 方法 (Amextra .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 723ba917d7fc9c0a1d7ac0bb0c2e8dcaf1510212b0811d6e608d10f3a0a88224
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108018"
---
# <a name="crenderedinputpinendflush-method"></a>CRenderedInputPin. EndFlush 方法

`EndFlush`方法會結束清除作業。 這個方法會實 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則傳回錯誤碼。

## <a name="remarks"></a>備註

此方法會清除任何暫止的 [**EC \_ 完成**](ec-complete.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amextra (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRenderedInputPin 類別**](crenderedinputpin.md)
</dt> </dl>

 

 




