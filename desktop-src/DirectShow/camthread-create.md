---
description: Create 方法會建立執行緒。
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: 'CAMThread：建立方法 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 135af6dd12bb53a2fa1e7ec14425c12e1c0bcc99bf9c82ce7aeaccb72df544f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103318"
---
# <a name="camthreadcreate-method"></a>CAMThread. Create 方法

`Create`方法會建立執行緒。

## <a name="syntax"></a>語法


```C++
BOOL Create();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會使用執行緒程式和執行緒引數的 [**CAMThread：： InitialThreadProc**](camthread-initialthreadproc.md) 方法，來建立執行緒 `this` 。

如果執行緒已經存在，方法會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




