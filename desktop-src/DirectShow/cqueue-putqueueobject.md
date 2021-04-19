---
description: 將專案放在佇列上。
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: 'CQueue. PutQueueObject 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995421"
---
# <a name="cqueueputqueueobject-method"></a>CQueue. PutQueueObject 方法

將專案放在佇列上。

## <a name="syntax"></a>語法


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*object* 
</dt> <dd>

**T** 類型的物件 (範本類型) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會封鎖，直到專案的佇列中有空間為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CQueue 類別**](cqueue.md)
</dt> </dl>

 

 




