---
description: CQueue 類別範本會執行簡單、靜態大小的佇列。
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: 'CQueue 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf6c6225a393f8f6ff1848acc66c68b6d260b0c839f2cc9f1e24d06a11e88219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953977"
---
# <a name="cqueue-class"></a>CQueue 類別

**CQueue** 類別範本會執行簡單、靜態大小的佇列。



| 公用方法                                  | 描述                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | 函式方法。                     |
| [**~ CQueue**](cqueue--cqueue.md)               | 函式方法。                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | 從佇列中取出下一個專案。 |
| [**PutQueueObject**](cqueue-putqueueobject.md) | 將專案放在佇列上。            |



 

## <a name="remarks"></a>備註

類別的函式會指定佇列的大小。 使用 [**CQueue：:P utqueueobject**](cqueue-putqueueobject.md) 將專案放在佇列上，並使用 [**CQueue：： GetQueueObject**](cqueue-getqueueobject.md) 方法清除專案。 如果佇列已滿，則 **PutQueueObject** 方法會封鎖，直到清除某個專案為止。 如果佇列是空的， **GetQueueObject** 會封鎖，直到某個專案排入佇列為止。 範本參數會指定專案的類型。 例如：


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



類別會使用兩個信號來控制佇列作業、「取得」信號和「put」信號。 [**GetQueueObject**](cqueue-getqueueobject.md)方法會使用) **WaitForSingleObject** 函式來等候 "get" 信號 (，並使用 **ReleaseSemaphore** 函數) 釋放「put」信號 (。 [**PutQueueObject**](cqueue-putqueueobject.md)方法會等候「put」信號，並釋放「get」信號。 類別會使用重要區段來序列化多個執行緒之間的佇列作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




