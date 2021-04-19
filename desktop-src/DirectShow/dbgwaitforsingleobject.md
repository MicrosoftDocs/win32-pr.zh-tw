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
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987967"
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

 

 




