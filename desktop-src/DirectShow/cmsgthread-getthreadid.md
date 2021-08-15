---
description: 抓取執行緒的識別碼。
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: 'CMsgThread. GetThreadID 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3b0837a7f050f09794b06e490f45012e0704e187b02668cd2af2a5bf8edf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214097"
---
# <a name="cmsgthreadgetthreadid-method"></a>CMsgThread. GetThreadID 方法

抓取執行緒的識別碼。

## <a name="syntax"></a>語法


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **m \_ ThreadId** 私用資料成員。

## <a name="remarks"></a>備註

此函數會傳回工作者執行緒的 Microsoft Win32 識別碼。 您可以在背景工作執行緒或用戶端執行緒上呼叫這個成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




