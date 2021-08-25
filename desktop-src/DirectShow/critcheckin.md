---
description: 如果目前的執行緒是指定之重要區段的擁有者，則傳回 TRUE。
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: 'CritCheckIn 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f4e9ff0078f6efe8dee9b060e61858c24aea0a64e7e35b9fb867125b8612ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908078"
---
# <a name="critcheckin-function"></a>CritCheckIn 函式

如果目前的執行緒是指定之重要區段的擁有者，則傳回 **TRUE** 。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcCrit* 
</dt> <dd>

[**CCritSec**](ccritsec.md)重要區段的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

在 debug 組建中，如果目前的執行緒是此重要區段的擁有者， **則傳回 TRUE** ，否則傳回 **FALSE** 。 在零售組建中，一律會傳回 **TRUE**。

## <a name="remarks"></a>備註

這個函式在 [**ASSERT**](assert.md) 宏內特別有用，可測試執行緒是否擁有指定的鎖定。

## <a name="examples"></a>範例

下列程式碼範例示範如何使用此函式：


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[重要區段調試函數](critical-section-debugging-functions.md)
</dt> </dl>

 

 




