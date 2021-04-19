---
description: GetDefaultTimerResolution 方法會傳回參考時鐘計時器目前的解析度。
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: 'CBaseReferenceClock. GetDefaultTimerResolution 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978706"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a>CBaseReferenceClock. GetDefaultTimerResolution 方法

方法會傳回 `GetDefaultTimerResolution` 目前的參考時鐘計時器解析度。

## <a name="syntax"></a>語法


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTimerResolution* 
</dt> <dd>

接收要求的計時器解析度（100-毫微秒單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會實 [**IReferenceClockTimerControl：： GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




