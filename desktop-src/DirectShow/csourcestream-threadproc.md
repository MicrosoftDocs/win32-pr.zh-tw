---
description: ThreadProc 方法是工作者執行緒的執行緒程式。 這個方法會實作為純虛擬 CAMThread：： ThreadProc 方法。
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: 'CSourceStream. ThreadProc 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987020"
---
# <a name="csourcestreamthreadproc-method"></a>CSourceStream. ThreadProc 方法

`ThreadProc`方法是工作者執行緒的執行緒程式。 這個方法會實作為純虛擬 [**CAMThread：： ThreadProc**](camthread-threadproc.md) 方法。

## <a name="syntax"></a>語法


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果執行緒已成功完成，則傳回0，否則會傳回1。 如果傳回值為1，可能仍會配置執行緒的資源。

## <a name="remarks"></a>備註

這個方法會呼叫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 方法，無限期等候執行緒要求。 如果它收到 [**CSourceStream：： Run**](csourcestream-run.md) 或 [**CSourceStream：:P ause**](csourcestream-pause.md) 要求，它會呼叫 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法。 **DoBufferProcessingLoop** 方法會推送資料，直到收到 [**CSourceStream：： Stop**](csourcestream-stop.md)要求為止。 執行緒程式會在收到 [**CSourceStream：： Exit**](csourcestream-exit.md) 要求時結束。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




