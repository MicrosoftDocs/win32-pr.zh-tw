---
description: WaitDispatchingMessages 函式會在分派視窗訊息時，等候物件收到信號。
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: 'WaitDispatchingMessages 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26442633d1a4d5187b5e53ae53e0a898f759f91dc3719f09715b570108b701f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071902"
---
# <a name="waitdispatchingmessages-function"></a>WaitDispatchingMessages 函式

`WaitDispatchingMessages`函數會在分派視窗訊息時，等候物件發出信號。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hObject* 
</dt> <dd>

要等候的物件控制碼。

</dd> <dt>

*dwWait* 
</dt> <dd>

逾時間隔（以毫秒為單位）。

</dd> <dt>

*hwnd* 
</dt> <dd>

視窗的選擇性控制碼。

</dd> <dt>

*uMsg* 
</dt> <dd>

選擇性的視窗訊息，指定要分派的訊息。

</dd> <dt>

*hEvent* 
</dt> <dd>

要等候之事件的選擇性控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

從 **WaitForMultipleObjects** 函式傳回值。

## <a name="remarks"></a>備註

如果物件擁有視窗，則應該在等候時分派視窗訊息。 這個函式可讓物件在分派訊息時等候事件、信號或其他相互排除物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[其他 Helper 函數](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




