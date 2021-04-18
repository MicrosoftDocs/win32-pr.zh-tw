---
description: Close 方法會等候執行緒結束，然後釋放其資源。
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: 'CAMThread. Close 方法 (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976197"
---
# <a name="camthreadclose-method"></a>CAMThread. Close 方法

`Close`方法會等候執行緒結束，然後釋放其資源。

## <a name="syntax"></a>語法


```C++
void Close();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

在呼叫這個方法之前，您必須提供方法讓執行緒結束。 例如，在您的 [**CAMThread：： ThreadProc**](camthread-threadproc.md) 方法中，定義通知執行緒結束的要求。 然後以該值呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法。

[**~ CAMThread**](camthread--camthread.md)的「函式」方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




