---
description: CBaseReferenceClock。 CBaseReferenceClock 函式-函數方法。
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: 'CBaseReferenceClock. CBaseReferenceClock (Refclock. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ea08e5555aa6286dac80642f19969e6e669a4ec6ccddb4e530d13e0253b4bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954987"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>CBaseReferenceClock. CBaseReferenceClock 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

包含物件名稱之字串的指標。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 IUnknown 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 如果發生錯誤，方法會在此參數中傳回錯誤碼。 請勿將此參數設定為 **Null**。

</dd> <dt>

*Psched.sys* 
</dt> <dd>

[**CAMSchedule**](camschedule.md)物件的指標。 如果是 **Null**，這個方法會建立新的 **CAMSchedule** 物件。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




