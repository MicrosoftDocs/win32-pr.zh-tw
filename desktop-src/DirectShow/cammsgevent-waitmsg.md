---
description: WaitMsg 方法會在分派傳送的訊息時，等候事件收到信號。
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: 'CAMMsgEvent. WaitMsg 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a2169d9938a8c2ff8a1961eee0895fefd7cc8a2dd487a4193d8053d27d98ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955447"
---
# <a name="cammsgeventwaitmsg-method"></a>CAMMsgEvent. WaitMsg 方法

`WaitMsg`方法會在分派傳送的訊息時，等候事件收到信號。

## <a name="syntax"></a>語法


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwTimeOut* 
</dt> <dd>

選擇性超時值（以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果事件已收到信號，則傳回 **TRUE** ; 如果發生超時，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會呼叫 PeekMessage 函數來處理訊息。 如果您的執行緒需要在等候事件時處理訊息，請呼叫這個方法，而不是 [**CAMEvent：： Wait**](camevent-wait.md) 。 如果執行緒沒有處理訊息，而另一個執行緒傳送訊息，則可能會發生鎖死。

例如，假設您建立執行緒，然後封鎖直到執行緒初始化為止。 如果執行緒藉由呼叫 SendMessage 函式，將訊息傳送至您的視窗，則會產生鎖死。 這是因為在處理訊息之前，SendMessage 不會傳回。 呼叫 WaitMsg 可讓 SendMessage 呼叫傳回，防止鎖死。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMMsgEvent 類別**](cammsgevent.md)
</dt> </dl>

 

 




