---
description: Remove 方法會移除指定位置上的專案。
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: 'CGenericList： Remove 方法 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b00d0772f391978fa6e581623446c67c2f37deabb1737e2602d7da7382fbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317758"
---
# <a name="cgenericlistremove-method"></a>CGenericList 方法

`Remove`方法會移除指定位置上的專案。

## <a name="syntax"></a>語法


```C++
OBJECT* Remove(
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

傳回)  (範本型別 **物件** 之物件的指標。

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

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




