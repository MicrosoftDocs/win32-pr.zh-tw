---
description: AdviseTime 方法會建立一次建議的要求。 這個方法會實 IReferenceClock：： AdviseTime 方法。
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: 'CBaseReferenceClock. AdviseTime 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e50b864a63cdd021d82c0a2a73f4f9c3acb68d1afb1f6a2dcd8d8d575966a5fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502788"
---
# <a name="cbasereferenceclockadvisetime-method"></a>CBaseReferenceClock. AdviseTime 方法

`AdviseTime`方法會建立一次建議的要求。 這個方法會實 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*baseTime* 
</dt> <dd>

基底參考時間，以 100-毫微秒單位表示。

</dd> <dt>

*streamTime* 
</dt> <dd>

資料流程位移時間，以 100-毫微秒單位表示。

</dd> <dt>

*hEvent* 
</dt> <dd>

事件的控制碼，由呼叫端建立。

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

變數的指標，此變數會接收通知要求的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | 描述                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 時間值無效<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 失敗<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

這個方法會建立參考時間 *baseTime* streamTime 的一次建議要求  +  **。 總和必須大於零且小於最大 \_ 時間，否則方法會傳回 E \_ INVALIDARG。 在要求的時間內，時鐘表示 *hEvent* 參數中指定的事件。

若要在到達時間之前取消通知，請呼叫 [**CBaseReferenceClock：： Unadvise**](cbasereferenceclock-unadvise.md) 方法，並傳遞從此呼叫傳回的 *pdwAdviseToken* 值。 在通知發生之後，時鐘會自動將其清除，因此不需要呼叫 **Unadvise**。 不過，這樣做並不會發生錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




