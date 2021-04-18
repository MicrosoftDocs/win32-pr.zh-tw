---
description: GetPrivateTime 方法會從時鐘中取出即時時間。
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: 'CBaseReferenceClock. GetPrivateTime 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976223"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>CBaseReferenceClock. GetPrivateTime 方法

`GetPrivateTime`方法會從時鐘中取出即時時間。

## <a name="syntax"></a>語法


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回目前的時鐘時間，以 100-毫微秒單位表示。

## <a name="remarks"></a>備註

這個方法會傳回由時鐘回報的即時時間。 外部呼叫端會使用 [**CBaseReferenceClock：： GetTime**](cbasereferenceclock-gettime.md) 方法，它會呼叫這個方法。 與 **GetTime** 方法不同的是，可以使用內部時鐘來向前移動。 如果發生這種情況， **GetTime** 方法會繼續傳回上次回報的時間，直到 `GetPrivateTime` 方法趕上為止。

這個方法會傳回系統時間。 如果您的時鐘從另一個來源取得時間，請覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




