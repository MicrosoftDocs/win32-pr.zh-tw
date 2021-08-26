---
description: SetWaiting 方法會遞增等候執行緒的計數。
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: 'CBaseAllocator. SetWaiting 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 674528b6da53b7835e437afac9a0564f91785b2f9a13f132e87a6763b80881c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057458"
---
# <a name="cbaseallocatorsetwaiting-method"></a>CBaseAllocator. SetWaiting 方法

`SetWaiting`方法會遞增等候中線程的計數。

## <a name="syntax"></a>語法


```C++
void SetWaiting();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會遞增 [**CBaseAllocator：： m \_ lWaiting**](cbaseallocator-m-lwaiting.md) 成員變數。 如果執行緒在 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法中遭到封鎖，配置器 `SetWaiting` 就會呼叫，然後等候 [**CBaseAllocator：： m \_ hSem**](cbaseallocator-m-hsem.md) 信號發出信號。 [**CBaseAllocator：： ReleaseBuffer**](cbaseallocator-releasebuffer.md)方法會表示信號，並將 *m \_ lWaiting* 設回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




