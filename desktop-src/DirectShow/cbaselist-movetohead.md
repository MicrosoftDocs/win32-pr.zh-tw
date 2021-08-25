---
description: MoveToHead 方法會分割清單，並將結尾部分插入另一個清單的開頭。
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: 'CBaseList. MoveToHead 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 18133107a3c8038780662bc39c8bd621c8b2c445a6e1e930f8fbfc015807e9fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928678"
---
# <a name="cbaselistmovetohead-method"></a>CBaseList. MoveToHead 方法

`MoveToHead`方法會分割清單，並將結尾部分插入另一個清單的開頭。

## <a name="syntax"></a>語法


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

在清單中標示分割的位置指標。

</dd> <dt>

*pList* 
</dt> <dd>

指向另一個清單的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會將清單分割于 *pos* 參數所指定的位置之前。 標題部分會保留在清單中。 結尾部分會插入另一個清單的開頭。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




