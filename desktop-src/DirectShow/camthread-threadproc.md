---
description: ThreadProc 方法是執行緒程式。
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: 'CAMThread. ThreadProc 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990725"
---
# <a name="camthreadthreadproc-method"></a>CAMThread. ThreadProc 方法

`ThreadProc`方法是執行緒程式。

## <a name="syntax"></a>語法


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回由衍生類別定義其意義的 **DWORD** 值。

## <a name="remarks"></a>備註

這是單純的虛擬方法。 在您的衍生類別中執行此方法，以提供執行緒程式。 當 [**CAMThread：： Create**](camthread-create.md) 方法建立執行緒時，它會提供 [**CAMThread：： InitialThreadProc**](camthread-initialthreadproc.md) 方法的位址，然後再呼叫您的 ThreadProc 方法。

一般來說，您的 ThreadProc 方法會進入迴圈，藉由呼叫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 或 [**CAMThread：： CheckRequest**](camthread-checkrequest.md) 方法) 和處理資料來抓取要求 (。

當此方法傳回時，就會結束執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




