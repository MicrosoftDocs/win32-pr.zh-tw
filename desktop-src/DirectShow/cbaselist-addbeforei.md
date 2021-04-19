---
description: AddBeforeI 方法會在指定的位置之前插入專案。
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: 'CBaseList. AddBeforeI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983059"
---
# <a name="cbaselistaddbeforei-method"></a>CBaseList. AddBeforeI 方法

方法會在 `AddBeforeI` 指定的位置之前插入專案。

## <a name="syntax"></a>語法


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要在其中加入專案的位置。

</dd> <dt>

*pObj* 
</dt> <dd>

專案的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回所插入專案的位置指標。

## <a name="remarks"></a>備註

如果 *pos* 是 **Null**，這個方法會將專案加入至清單的結尾 (相當於呼叫 [**CBaseList：： AddTailI**](cbaselist-addtaili.md) 方法) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




