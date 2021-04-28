---
description: CAMEvent。 CAMEvent 函式-函數方法。
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: 'CAMEvent. CAMEvent (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096528"
---
# <a name="cameventcamevent-constructor"></a>CAMEvent. CAMEvent 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fManualReset* 
</dt> <dd>

布林值，指定物件是否為手動重設事件或自動重設事件。 若 **為 TRUE**，表示物件是手動重設事件。 否則，它會是自動重設事件。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 如果函式失敗，此參數會收到錯誤碼。 如果發生這種情況，則物件不是處於有效的狀態。

為了與舊版 strmbase 回溯相容，此參數預設為 **Null**。 不過，最好是傳遞非 **Null** 值，讓呼叫端可以檢查物件的狀態。

</dd> </dl>

## <a name="remarks"></a>備註

事件會以未收到信號狀態開始。

使用自動重設事件， [**CAMEvent：： Wait**](camevent-wait.md) 方法會在方法傳回時，將事件重設為未收到信號。 若使用手動重設事件，事件會保持為信號，直到您呼叫 [**CAMEvent：： reset**](camevent-reset.md) 方法為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMEvent 類別**](camevent.md)
</dt> </dl>

 

 




