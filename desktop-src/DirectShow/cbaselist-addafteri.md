---
description: AddAfterI 方法會在指定的位置之後插入專案。
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: 'CBaseList. AddAfterI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b72be7342e6085b773ef2493f5ad138f73349dffcdafc1a60a380692df3f16ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016986"
---
# <a name="cbaselistaddafteri-method"></a>CBaseList. AddAfterI 方法

方法會在 `AddAfterI` 指定的位置之後插入專案。

## <a name="syntax"></a>語法


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要在其後加入專案的位置。

</dd> <dt>

*pObj* 
</dt> <dd>

要加入之專案的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回所插入專案的位置指標。

## <a name="remarks"></a>備註

如果 *pos* 是 **Null**，這個方法會將專案加入至清單的開頭 (相當於呼叫 [**CBaseList：： AddHeadI**](cbaselist-addheadi.md) 方法) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




