---
description: AddTail 方法會將另一個清單附加至這份清單的結尾。
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: 'CBaseList. AddTail 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984085"
---
# <a name="cbaselistaddtail-method"></a>CBaseList. AddTail 方法

方法會將 `AddTail` 另一個清單附加至這份清單的結尾。

## <a name="syntax"></a>語法


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pList* 
</dt> <dd>

要附加之清單的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果方法失敗，某些專案可能已加入至清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




