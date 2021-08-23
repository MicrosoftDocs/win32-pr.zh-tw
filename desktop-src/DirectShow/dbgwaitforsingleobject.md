---
description: 等候物件變成信號。
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: 'DbgWaitForSingleObject 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5e8180c905cdb7d8d1024f22a85984c17c0e12e18971499d29ed1479a79498f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749348"
---
# <a name="dbgwaitforsingleobject-function"></a>DbgWaitForSingleObject 函式

等候物件變成信號。

在 debug 組建中，如果逾時間隔在物件收到信號之前過期，此函式就會觸發判斷提示。 若要設定逾時間隔，請呼叫 [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) 函數。

在零售組建中，此函式相當於具有無限逾時間隔的 **WaitForSingleObject** 函數。

## <a name="syntax"></a>語法


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*h* 
</dt> <dd>

物件的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[等候調試函式](wait-debugging-functions.md)
</dt> </dl>

 

 




