---
description: CBaseMediaFilter。 CBaseMediaFilter 函式-函數方法。
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: 'CBaseMediaFilter. CBaseMediaFilter (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096316"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>CBaseMediaFilter. CBaseMediaFilter 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

包含物件名稱之字串的指標。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*pLock* 
</dt> <dd>

[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。

</dd> <dt>

*Clsid* 
</dt> <dd>

物件的類別識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

如果另一個物件包含或匯總 `CBaseMediaFilter` 物件， **CCritSec** 鎖定可能會在 `CBaseMediaFilter` 物件外部。 在此情況下，請將指標傳遞至 *pLock* 中的鎖定。

否則，您可以：

-   衍生繼承和 CCritSec 的類別 `CBaseMediaFilter` 。  若為 *pLock*，請傳遞 this 指標。
-   衍生繼承 `CBaseMediaFilter` 並包含 **CCritSec** 成員變數的類別。 若為 *pLock*，請傳遞該變數的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseMediaFilter 類別**](cbasemediafilter.md)
</dt> </dl>

 

 




