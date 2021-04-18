---
description: 使用 Microsoft Win32 SuspendThread 函式來暫止執行中線程的操作。
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: 'CMsgThread. SuspendThread 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996302"
---
# <a name="cmsgthreadsuspendthread-method"></a>CMsgThread. SuspendThread 方法

使用 Microsoft Win32 **SuspendThread** 函式來暫止執行中線程的操作。

## <a name="syntax"></a>語法


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成員函式成功，則傳回值為執行緒的先前暫止計數。 如果成員函式失敗，則傳回值為0xFFFFFFFF。 若要取得延伸錯誤資訊，請呼叫 Microsoft Win32 **GetLastError** 函數。

## <a name="remarks"></a>備註

用戶端執行緒會呼叫這個成員函式，以暫止工作者執行緒的作業。 背景工作執行緒會保持暫止狀態，而且在呼叫 [**CMsgThread：： ResumeThread**](cmsgthread-resumethread.md) 成員函式之前，將不會執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




