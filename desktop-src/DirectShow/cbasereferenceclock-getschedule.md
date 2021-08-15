---
description: GetSchedule 方法會抓取時鐘排程物件的指標。
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: 'CBaseReferenceClock. GetSchedule 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6be5c4ed76573428967138682b478a54859e4ca97213f132ff805a0e83be0b50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822834"
---
# <a name="cbasereferenceclockgetschedule-method"></a>CBaseReferenceClock. GetSchedule 方法

方法會抓取 `GetSchedule` 時鐘排程物件的指標。

## <a name="syntax"></a>語法


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBaseReferenceClock：： m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) 成員變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




