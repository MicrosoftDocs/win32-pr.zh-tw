---
description: CallWorker 方法會向執行緒發出要求的信號。
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: 'CAMThread. CallWorker 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978456"
---
# <a name="camthreadcallworker-method"></a>CAMThread. CallWorker 方法

`CallWorker`方法會向執行緒發出要求的信號。

## <a name="syntax"></a>語法


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwParam* 
</dt> <dd>

要求參數。 衍生的類別會定義參數的意義。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回衍生類別所定義的值。

## <a name="remarks"></a>備註

[**CAMThread：： GetRequest**](camthread-getrequest.md)和 [**CAMThread：： CheckRequest**](camthread-checkrequest.md)方法會取出 *dwParam* 參數的值。 GetRequest 方法 `CallWorker` 會封鎖，直到呼叫為止。

這個方法會封鎖，直到呼叫 [**CAMThread：： Reply**](camthread-reply.md) 方法為止。 傳回值是指定要回復的參數。

這個方法會保留 [**CAMThread：： m \_ AccessLock**](camthread-m-accesslock.md) 鎖定以序列化要求。 因此，請從執行緒本身或線上程內容中執行的任何成員函式，呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




