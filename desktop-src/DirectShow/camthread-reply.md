---
description: 回復方法會回復要求。
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: 'CAMThread. Reply 方法 (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9783703d711800b8002aa0372292349d83620eafb097be2256ffde6ab2c91c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662364"
---
# <a name="camthreadreply-method"></a>CAMThread. Reply 方法

`Reply`方法會回復要求。

## <a name="syntax"></a>語法


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dw* 
</dt> <dd>

要在 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法中傳回的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

CallWorker 方法會封鎖，直到呼叫這個方法為止。 *Dw* 參數提供 CallWorker 的傳回值。 在您抓取要求之後，于執行緒程式中呼叫這個方法，以釋放要求的執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




