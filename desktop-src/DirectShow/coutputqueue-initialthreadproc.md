---
description: 建立執行緒時，InitialThreadProc 方法會呼叫 COutputQueue：： ThreadProc 方法。
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: " (Outputq 的 COutputQueue.InitialThreadProc 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a80561ae652df7168ad09c1cf6e9fde767154e6c72a8fe5360a5d09c784941f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813588"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.InitialThreadProc 方法

`InitialThreadProc`當建立執行緒時，此方法會呼叫 [**COutputQueue：： ThreadProc**](coutputqueue-threadproc.md)方法。

## <a name="syntax"></a>語法


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*光伏* 
</dt> <dd>

`this` 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**COutputQueue：： ThreadProc**](coutputqueue-threadproc.md) 方法所傳回的值。

## <a name="remarks"></a>備註

這個方法是物件的背景工作執行緒的執行緒程式。 物件的 `this` 指標是執行緒參數。 方法會將此方法取值為呼叫 **ThreadProc**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




