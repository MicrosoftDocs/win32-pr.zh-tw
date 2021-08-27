---
description: SetDefaultTimerResolution 方法會設定參考時鐘計時器的解析度。
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: 'CBaseReferenceClock. SetDefaultTimerResolution 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 980f31856aba14079da0f5b9625dca40846255d6f02361b2798d7c38c1cd4f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087418"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>CBaseReferenceClock. SetDefaultTimerResolution 方法

`SetDefaultTimerResolution`方法會設定參考時鐘計時器的解析度。

## <a name="syntax"></a>語法


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*timerResolution* 
</dt> <dd>

最小計時器解析度（100-毫微秒單位）。 如果值為零，則參考時鐘會取消其先前的要求。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會實 [**IReferenceClockTimerControl：： SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




