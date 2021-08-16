---
description: SetTimeDelta 方法會調整內部時鐘時間。
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: 'CBaseReferenceClock. SetTimeDelta 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9eba5337fa43e43e3b7a45a7a92263fd4e6d69388185a2096c1a270590e482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403437"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>CBaseReferenceClock. SetTimeDelta 方法

`SetTimeDelta`方法會調整內部時鐘時間。

## <a name="syntax"></a>語法


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TimeDelta* \[裁判\]
</dt> <dd>

要調整時鐘時間的數量，以 100-毫微秒單位表示。 正值會將時鐘往前移動，負值會將時鐘向後移動。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

如果從提供時間資訊的裝置偏離，衍生類別可以使用這個方法來調整內部時鐘。

[**CBaseReferenceClock：： GetTime**](cbasereferenceclock-gettime.md)方法永遠不會傳回遞減的值。 如果您將時鐘向後調整， **GetTime** 會傳回先前的值，直到時鐘再次到達該值為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




