---
description: 建立執行緒。
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: 'CMsgThread. CreateThread 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3681716af79d0c47ae08371caa2d03d236b9748d98b08098d7a6834a93ed9b2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831868"
---
# <a name="cmsgthreadcreatethread-method"></a>CMsgThread. CreateThread 方法

建立執行緒。

## <a name="syntax"></a>語法


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                              | 描述                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | 已成功建立執行緒。<br/>     |
| <dl> <dt>FALSE * * * *</dt> </dl> | 未成功建立執行緒。<br/> |



 

## <a name="remarks"></a>備註

執行緒將會透過 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md)) 成員函式來迴圈、封鎖直到要求排入佇列 (，然後使用每個訊息來呼叫 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




