---
description: 啟用或停用指定之重要區段的偵錯工具記錄。
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: 'DbgLockTrace 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993493"
---
# <a name="dbglocktrace-function"></a>DbgLockTrace 函式

啟用或停用指定之重要區段的偵錯工具記錄。

## <a name="syntax"></a>語法


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcCrit* 
</dt> <dd>

[**CCritSec**](ccritsec.md)重要區段的指標。

</dd> <dt>

*fTrace* 
</dt> <dd>

指定是否啟用記錄的值。 使用 **TRUE** 來啟用記錄，或使用 **FALSE** 來停用它。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

您可以使用此函數來追蹤特定的重要區段。 根據預設，重要區段的 debug 記錄已停用，因為很多重要區段。

若要追蹤重要區段，請執行下列步驟：

1.  \_在您包含 DirectShow 標頭之前，請先定義 debug 或 debug。
2.  藉由使用記錄鎖定旗標呼叫 [**DbgSetModuleLevel**](dbgsetmodulelevel.md) ，啟用重要區段的 debug 記錄 \_ 。
3.  在您想要追蹤的重要區段上呼叫 **DbgLockTrace** 。

在零售組建中， **DbgLockTrace** 函數沒有任何作用。

## <a name="examples"></a>範例

下列程式碼範例顯示如何追蹤重要區段。


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
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

 

 




