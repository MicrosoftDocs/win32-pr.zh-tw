---
description: IsStopped 方法會判斷是否已停止包含此 pin 的篩選。
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: 'CBasePin. IsStopped 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64e833ef495ace41a9dcd1614b69e4a081befce0e429fa7aad800a73ce490439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916388"
---
# <a name="cbasepinisstopped-method"></a>CBasePin. IsStopped 方法

`IsStopped`方法會判斷包含此 pin 的篩選是否已停止。

## <a name="syntax"></a>語法


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果篩選已停止，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

請勿在 **CBasePin** 的方法中呼叫這個方法，因為篩選可能尚未初始化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




