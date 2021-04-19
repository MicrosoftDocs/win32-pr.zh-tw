---
description: GetRequestHandle 方法會抓取由 CAMThread：： CallWorker 方法所發出之事件的控制碼。
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: 'CAMThread. GetRequestHandle 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999641"
---
# <a name="camthreadgetrequesthandle-method"></a>CAMThread. GetRequestHandle 方法

`GetRequestHandle`方法會抓取 [**CAMThread：： CallWorker**](camthread-callworker.md)方法所發出之事件的控制碼。

## <a name="syntax"></a>語法


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回事件控制碼。

## <a name="remarks"></a>備註

CAMEvent 類別會保留私用手動重設事件，它是由 CallWorker 所設定，並由 [**CAMThread：： Reply**](camthread-reply.md) 方法重設。

如果您呼叫 WaitForMultipleObjects 之類的函式，請使用 GetRequestHandle 來取得事件控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




