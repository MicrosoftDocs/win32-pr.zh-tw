---
description: 使用 Microsoft Win32 ResumeThread 函式，在前一次呼叫 CMsgThread：： SuspendThread 成員函式之後，繼續執行背景工作執行緒的操作。
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: 'CMsgThread. ResumeThread 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994897"
---
# <a name="cmsgthreadresumethread-method"></a>CMsgThread. ResumeThread 方法

使用 Microsoft Win32 **ResumeThread** 函式，在前一次呼叫 [**CMsgThread：： SuspendThread**](cmsgthread-suspendthread.md) 成員函式之後，繼續執行背景工作執行緒的操作。

## <a name="syntax"></a>語法


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成員函式成功，則傳回值為執行緒的先前暫止計數。 如果成員函式失敗，則傳回值為0xFFFFFFFF。 若要取得延伸錯誤資訊，請呼叫 Microsoft Win32 **GetLastError** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




