---
description: AdvisePeriodic 方法會建立週期性建議要求。 這個方法會實 IReferenceClock：： AdvisePeriodic 方法。
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: 'CBaseReferenceClock. AdvisePeriodic 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993557"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>CBaseReferenceClock. AdvisePeriodic 方法

`AdvisePeriodic`方法會建立週期性建議要求。 這個方法會實 [**IReferenceClock：： AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartTime* 
</dt> <dd>

第一個通知的時間，以 100-毫微秒單位表示。 必須大於零且小於最大 \_ 時間。

</dd> <dt>

*PeriodTime* 
</dt> <dd>

通知之間的時間，以 100-毫微秒單位表示。 必須大於零。

</dd> <dt>

*hSemaphore* 
</dt> <dd>

呼叫端所建立之信號的控制碼。

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

變數的指標，此變數會接收通知要求的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 時間值無效<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 失敗<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

在每個通知時間，時鐘會釋放 *hSemaphore* 參數中指定的信號。 如果不再需要任何通知，請呼叫 [**CBaseReferenceClock：： Unadvise**](cbasereferenceclock-unadvise.md) 方法，並傳遞從此呼叫傳回的 *pdwAdviseToken* 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




