---
description: CheckRequest 方法會檢查是否有要求，而不會封鎖。
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: 'CAMThread. CheckRequest 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 292f8a7fb1ed4f12ad558993d6b1932b2ddff4656bada5e0a89067bac1baa9c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662354"
---
# <a name="camthreadcheckrequest-method"></a>CAMThread. CheckRequest 方法

`CheckRequest`方法會檢查是否有要求，而不會封鎖。

## <a name="syntax"></a>語法


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pParam* 
</dt> <dd>

變數的指標，此變數會接收最後呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法時所傳遞的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果有暫止的要求，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法是 [**CAMThread：： GetRequest**](camthread-getrequest.md) 方法的非封鎖版本。

如果另一個執行緒正在等候呼叫 CallWorker，這個方法會抓取要求參數，並傳回 **TRUE**。 否則，它會傳回 **FALSE**。 如果方法傳回 **TRUE**，則呼叫 [**CAMThread：： Reply**](camthread-reply.md) 方法以釋放要求的執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




