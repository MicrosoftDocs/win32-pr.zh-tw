---
description: SetClockDelta 方法會調整時鐘時間。 這個方法會實 IAMClockAdjust：： SetClockDelta 方法。
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: 'CSystemClock. SetClockDelta 方法 (Sysclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c98ccf35e41886594a3aab8c3abec6737128d8d7e22f6dfb75d0ac88ac3b7a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538658"
---
# <a name="csystemclocksetclockdelta-method"></a>CSystemClock. SetClockDelta 方法

`SetClockDelta`方法會調整時鐘時間。 這個方法會實 [**IAMClockAdjust：： SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rtDelta* 
</dt> <dd>

指定用來調整時鐘的量，作為 [**參考 \_ 時間**](reference-time.md) 值。 正值會將時鐘往前移動，負值會將時鐘向後移動。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法只會呼叫 [**CBaseReferenceClock：： SetTimeDelta**](cbasereferenceclock-settimedelta.md)。

[**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)所傳回的時間值會以單純方式遞增。 如果您將時鐘設定回來， **GetTime** 會繼續回報舊的時間，直到內部時鐘趕上為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | CSystemClock 類別<br/>                                                                                                                                                              |
| 標頭<br/>  | <dl> <dt>Sysclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




