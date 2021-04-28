---
description: CBaseObject。 CBaseObject 函式-函數方法。
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: 'CBaseObject. CBaseObject (Combase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099616"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>CBaseObject. CBaseObject 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

字串，包含物件的名稱，用於進行調試。

</dd> </dl>

## <a name="remarks"></a>備註

這個方法會遞增使用中物件的計數。  (參閱 [**CBaseObject：： ObjectsActive**](cbaseobject-objectsactive.md)) 。

在靜態記憶體中配置 *pName* 參數：


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



[**名稱**](name.md)宏會在零售組建中編譯為 **Null** ，因此靜態字串只會出現在偵錯工具組建中。 如需詳細資訊，請參閱 [**DbgDumpObjectRegister**](dbgdumpobjectregister.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseObject 類別**](cbaseobject.md)
</dt> </dl>

 

 




