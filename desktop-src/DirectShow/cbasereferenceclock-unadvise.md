---
description: Unadvise 方法會移除暫止的建議要求。 這個方法會實 IReferenceClock：： Unadvise 方法。
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: 'CBaseReferenceClock. Unadvise 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e6519d1a94091c0afc0bafffe40fdaac47364d25f54e068ae503f32abccbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652448"
---
# <a name="cbasereferenceclockunadvise-method"></a>CBaseReferenceClock. Unadvise 方法

`Unadvise`方法會移除暫止的建議要求。 這個方法會實 [**IReferenceClock：： Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwAdviseToken* 
</dt> <dd>

要移除之要求的識別碼。 在 *pdwAdviseToken* 參數中使用 [**CBaseReferenceClock：： AdviseTime**](cbasereferenceclock-advisetime.md)或 [**CBaseReferenceClock：： AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)方法所傳回的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | 描述           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 找不到。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




