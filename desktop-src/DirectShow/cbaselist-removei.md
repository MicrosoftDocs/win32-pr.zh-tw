---
description: RemoveI 方法會在指定的位置移除專案。
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: 'CBaseList. RemoveI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994796"
---
# <a name="cbaselistremovei-method"></a>CBaseList. RemoveI 方法

`RemoveI`方法會移除指定位置上的專案。

## <a name="syntax"></a>語法


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

指出要移除之專案的位置值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回專案的指標。

## <a name="remarks"></a>備註

這個方法會從清單中刪除節點，但不會刪除該節點中包含的專案。

如果 *pos* 是 **null**，則方法會傳回 **null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




