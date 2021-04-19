---
description: 等候指定物件的任何 (或所有) 都收到信號。
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: 'DbgWaitForMultipleObjects 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990834"
---
# <a name="dbgwaitformultipleobjects-function"></a>DbgWaitForMultipleObjects 函式

等候指定物件的任何 (或所有) 都收到信號。

在 debug 組建中，如果逾時間隔在物件收到信號之前過期，此函式就會觸發判斷提示。 若要設定逾時間隔，請呼叫 [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) 函數。

在零售組建中，此函式相當於具有無限逾時間隔的 **WaitForMultipleObjects** 函數。

## <a name="syntax"></a>語法


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nCount* 
</dt> <dd>

物件數目。

</dd> <dt>

*lpHandles* 
</dt> <dd>

物件之控制碼的陣列，大小為 *nCount*。

</dd> <dt>

*bWaitAll* 
</dt> <dd>

指定是否等候所有物件的布林值。 若為 **TRUE**，則函式會等候所有物件收到信號。 否則，它會等候至少一個物件收到信號。

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

 

 




