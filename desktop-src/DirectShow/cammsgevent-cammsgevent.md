---
description: CAMMsgEvent。 CAMMsgEvent 函式-函數方法。
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: 'CAMMsgEvent. CAMMsgEvent (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fc2eeaab10134022388e6a57628d1c3c5a87fc0e0a443efab19f016a1e5c27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955497"
---
# <a name="cammsgeventcammsgevent-constructor"></a>CAMMsgEvent. CAMMsgEvent 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 如果函式失敗，此參數會收到錯誤碼。 如果發生這種情況，則物件不是處於有效的狀態。

為了與舊版 strmbase 回溯相容，此參數預設為 **Null**。 不過，最好是傳遞非 **Null** 值，讓呼叫端可以檢查物件的狀態。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMMsgEvent 類別**](cammsgevent.md)
</dt> </dl>

 

 




