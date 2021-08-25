---
description: 初始化串流執行緒時，會呼叫 OnThreadCreate 方法。
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: 'CSourceStream. OnThreadCreate 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e263f0ae72838504ab6d219c71d7841291a3edd2a7d6b719d112c74fb30c23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907708"
---
# <a name="csourcestreamonthreadcreate-method"></a>CSourceStream. OnThreadCreate 方法

`OnThreadCreate`初始化串流執行緒時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

Thread 程式 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md)會在第一次收到 [**CSourceStream：： Init**](csourcestream-init.md) 要求時呼叫這個方法。 方法不會在基類中執行任何動作。 衍生類別可以覆寫這個方法，以執行執行緒初始化。 如果衍生類別傳回錯誤碼，執行緒就會結束併發生錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




