---
description: 當串流執行緒即將結束時，會呼叫 OnThreadDestroy 方法。
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: 'CSourceStream. OnThreadDestroy 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994987"
---
# <a name="csourcestreamonthreaddestroy-method"></a>CSourceStream. OnThreadDestroy 方法

`OnThreadDestroy`當串流執行緒即將結束時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

Thread 程式 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md)會在結束之前呼叫這個方法。 方法不會在基類中執行任何動作;它可供衍生類別覆寫。 如果衍生類別傳回錯誤碼，執行緒就會結束併發生錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




