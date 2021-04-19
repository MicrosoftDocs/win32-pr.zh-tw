---
description: 函式方法。
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: 'CBaseList. CBaseList (Wxlist. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994313"
---
# <a name="cbaselistcbaselist-constructor"></a>CBaseList. CBaseList 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

清單名稱的指標。

</dd> </dl>

## <a name="remarks"></a>備註

為了提高效率， `CBaseList` 類別會維護清單節點的快取。 此版本的函式會使用預設快取大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




