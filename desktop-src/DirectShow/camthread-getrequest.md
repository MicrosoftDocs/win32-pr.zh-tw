---
description: GetRequest 方法會等候下一個要求。
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: 'CAMThread. GetRequest 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978777"
---
# <a name="camthreadgetrequest-method"></a>CAMThread. GetRequest 方法

`GetRequest`方法會等候下一個要求。

## <a name="syntax"></a>語法


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回衍生類別所定義的值。

## <a name="remarks"></a>備註

這個方法會封鎖，直到另一個執行緒呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法為止。 然後，它會傳回傳遞給 CallWorker 的參數。 呼叫 [**CAMThread：： Reply**](camthread-reply.md) 方法以釋放要求的執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




