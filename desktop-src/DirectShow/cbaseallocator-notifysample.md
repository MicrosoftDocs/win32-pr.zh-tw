---
description: NotifySample 方法會釋放任何正在等候樣本的執行緒。
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: 'CBaseAllocator. NotifySample 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1b73a54ae9b5ccabacfbb1153c5d0d91f951e83082a1bdd3c7f7551ad813804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017476"
---
# <a name="cbaseallocatornotifysample-method"></a>CBaseAllocator. NotifySample 方法

`NotifySample`方法會釋放任何正在等候樣本的執行緒。

## <a name="syntax"></a>語法


```C++
void NotifySample();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當有線程等候樣本時， [**CBaseAllocator：： m \_ lWaiting**](cbaseallocator-m-lwaiting.md) 的值大於零。 如果 *m \_ lWaiting* 大於零，則這個方法會呼叫 [**CBaseAllocator：： m \_ hSem**](cbaseallocator-m-hsem.md)信號上的 **ReleaseSemaphore** 函式，以啟用任何等候中的執行緒。 它也會將 *m \_ lWaiting* 重設為零。

當範例傳回至可用清單時，會從 [**CBaseAllocator：： ReleaseBuffer**](cbaseallocator-releasebuffer.md) 方法內呼叫這個方法;當配置器已取消認可時，從 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




