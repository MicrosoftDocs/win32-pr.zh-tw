---
description: AddHeadI 方法會將專案加入至清單的前方。
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: 'CBaseList. AddHeadI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c1f22434aa2c927933c36ec496d5880ca8f3f673b314d7a8197079203757427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568118"
---
# <a name="cbaselistaddheadi-method"></a>CBaseList. AddHeadI 方法

`AddHeadI`方法會將專案加入至清單的前方。

## <a name="syntax"></a>語法


```C++
POSITION AddHeadI(
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

傳回位置值，表示新的標頭位置。

## <a name="remarks"></a>備註

如果方法失敗，則傳回值為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




