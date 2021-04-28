---
description: CAMThread。 CAMThread 函式-函數方法。
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: 'CAMThread. CAMThread (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096406"
---
# <a name="camthreadcamthread-constructor"></a>CAMThread. CAMThread 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 如果函式失敗，此參數會收到錯誤碼。 如果發生這種情況，則物件不是處於有效的狀態。

為了與舊版 strmbase 回溯相容，此參數預設為 **Null**。 不過，最好是傳遞非 **Null** 值，讓呼叫端可以檢查物件的狀態。

</dd> </dl>

## <a name="remarks"></a>備註

此函數不會建立執行緒。 若要建立執行緒，請呼叫 [**CAMThread：： create**](camthread-create.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




