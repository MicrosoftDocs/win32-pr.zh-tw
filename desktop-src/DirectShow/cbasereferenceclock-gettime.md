---
description: GetTime 方法會抓取目前的參考時間。 這個方法會實 IReferenceClock：： GetTime 方法。
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: 'CBaseReferenceClock. GetTime 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999489"
---
# <a name="cbasereferenceclockgettime-method"></a>CBaseReferenceClock. GetTime 方法

`GetTime`方法會捕獲目前的參考時間。 這個方法會實 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTime* 
</dt> <dd>

接收目前時間的變數指標，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數。<br/>                       |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | 傳回的時間與前一個值相同。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 成功。<br/>                                         |



 

## <a name="remarks"></a>備註

這個方法會呼叫 [**CBaseReferenceClock：： GetPrivateTime**](cbasereferenceclock-getprivatetime.md) 方法來判斷實際的時鐘時間。 如果時鐘時間嚴格大於先前的值，則會 `GetTime` 使用時鐘時間，並傳回 S \_ OK。 否則，會 `GetTime` 使用先前的值並傳回 \_ FALSE。 因此，內部時鐘可能會在短時間內執行，而不會導致參考時間回溯執行。 相反地，參考時間會「停止」相同的值，直到內部時鐘趕上為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




