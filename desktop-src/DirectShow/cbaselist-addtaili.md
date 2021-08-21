---
description: AddTailI 方法會將專案加入至清單結尾。
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: 'CBaseList. AddTailI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3317877bfa67d2d39d469882e0b12b9fd79a923873022a51ee48712fc772743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659124"
---
# <a name="cbaselistaddtaili-method"></a>CBaseList. AddTailI 方法

`AddTailI`方法會將專案加入至清單結尾。

## <a name="syntax"></a>語法


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObj* 
</dt> <dd>

專案的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回新結尾位置的位置值。

## <a name="remarks"></a>備註

如果方法失敗，則會傳回 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




