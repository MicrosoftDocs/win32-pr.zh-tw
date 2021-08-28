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
ms.openlocfilehash: f2527d43dfa59ab01bc57109bd2845e5da8286524612746067b1ff2f4cb2a3c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103198"
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

 

 




