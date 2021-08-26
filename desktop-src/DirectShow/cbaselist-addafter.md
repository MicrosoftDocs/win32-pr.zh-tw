---
description: AddAfter 方法會在指定的位置之後插入清單。
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: 'CBaseList. AddAfter 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28351e1e0762b8e45bc9bf2ba1fe3624c67339e9b8bcf59ec5a919850a853061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983499"
---
# <a name="cbaselistaddafter-method"></a>CBaseList. AddAfter 方法

方法會在 `AddAfter` 指定的位置之後插入清單。

## <a name="syntax"></a>語法


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要在其後插入清單的位置。

</dd> <dt>

*pList* 
</dt> <dd>

要插入之清單的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

現有的位置指標，包括 *pos* 參數中指定的指標，會保持有效。 如果此方法失敗，可能會加入一些專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




