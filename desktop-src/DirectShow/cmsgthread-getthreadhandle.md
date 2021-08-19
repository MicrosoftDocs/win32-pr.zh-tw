---
description: 在 CMsgThread 物件中抓取執行緒的控制碼。
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: 'CMsgThread. GetThreadHandle 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ecb968156302c4fd1a8c48d1c6f3175977059298d2f6af5207abc376a6e107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585688"
---
# <a name="cmsgthreadgetthreadhandle-method"></a>CMsgThread. GetThreadHandle 方法

在 [**CMsgThread**](cmsgthread.md) 物件中抓取執行緒的控制碼。

## <a name="syntax"></a>語法


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回執行緒控制碼。

## <a name="remarks"></a>備註

執行緒控制碼可以傳遞給 wait 函數，例如 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)。 執行緒已結束時，執行緒控制碼會發出信號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

