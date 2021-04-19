---
description: 函式方法。
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: 'CSystemClock. CSystemClock (Sysclock. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fea99d95aa4c1b1cadefbb95384fb871374362f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999623"
---
# <a name="csystemclockcsystemclock-constructor"></a>CSystemClock. CSystemClock 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

包含物件之偵錯工具名稱的字串。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 如果發生錯誤，方法會在此參數中傳回錯誤碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Sysclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




