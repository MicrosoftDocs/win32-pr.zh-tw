---
description: AddHead 方法會在這份清單前面插入另一個清單。
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: 'CBaseList. AddHead 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8108af5f779bea4c1a1e756ab018ed9c902d3e516556c42b7899f442cb7704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814318"
---
# <a name="cbaselistaddhead-method"></a>CBaseList. AddHead 方法

`AddHead`方法會在這份清單前面插入另一個清單。

## <a name="syntax"></a>語法


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pList* 
</dt> <dd>

要加入之專案清單的指標。

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

 

 




