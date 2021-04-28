---
description: CBaseFilter. CBaseFilter (const TCHAR \* 、LPUNKNOWN、CCritSec \* 、REFCLSID) （函式）函數方法。
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: 'CBaseFilter. CBaseFilter (const TCHAR *、LPUNKNOWN、CCritSec*、REFCLSID)  (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099826"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>CBaseFilter. CBaseFilter (const TCHAR \* 、LPUNKNOWN、CCritSec \* 、REFCLSID) 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseFilter(
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

包含篩選名稱之字串的指標，用於進行調試。

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

篩選準則 (CLSID) 的類別識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

針對重要區段物件，您通常會執行下列其中一項：

-   衍生繼承 **CBaseFilter** 和 **CCritSec** 的類別。 若為 *pLock*，請傳遞 `this` 指標。
-   衍生繼承 **CBaseFilter** 的類別，並包含 **CCritSec** 成員變數。 若為 *pLock*，請傳遞該變數的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




