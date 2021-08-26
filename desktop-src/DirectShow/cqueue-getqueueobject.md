---
description: 從佇列中取出下一個專案。
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: 'CQueue. GetQueueObject 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c32039a82e3a0b5c086cbe18e895bdec1aaac09d4947b90d9ba18e8c6636d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108278"
---
# <a name="cqueuegetqueueobject-method"></a>CQueue. GetQueueObject 方法

從佇列中取出下一個專案。

## <a name="syntax"></a>語法


```C++
T GetQueueObject();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回類型為 **T** (範本類型) 的物件。

## <a name="remarks"></a>備註

這個方法會封鎖，直到佇列上有可用的專案為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CQueue 類別**](cqueue.md)
</dt> </dl>

 

 




