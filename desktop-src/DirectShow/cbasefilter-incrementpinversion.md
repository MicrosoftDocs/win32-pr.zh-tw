---
description: IncremementPinVersion 方法會在一組 pin 上遞增版本號碼。
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: 'CBaseFilter. IncrementPinVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01c82a5f506673b6145b468004bbc900d3acdb051f525df20930344137618e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824105"
---
# <a name="cbasefilterincrementpinversion-method"></a>CBaseFilter. IncrementPinVersion 方法

`IncremementPinVersion`方法會在一組 pin 上遞增版本號碼。

## <a name="syntax"></a>語法


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會遞增 [**CBaseFilter：： m \_ PinVersion**](cbasefilter-m-pinversion.md) 成員變數。 如果篩選動態建立或終結 pin，請在 pin 變更時呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




