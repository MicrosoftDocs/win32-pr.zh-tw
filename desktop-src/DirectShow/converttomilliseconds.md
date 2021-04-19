---
description: ConvertToMilliseconds 函數會將參考時間轉換成毫秒。
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: 'ConvertToMilliseconds 函式 (Refclock) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984310"
---
# <a name="converttomilliseconds-function"></a>ConvertToMilliseconds 函式

`ConvertToMilliseconds`函數會將參考時間轉換成毫秒。

## <a name="syntax"></a>語法


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RT* \[裁判\]
</dt> <dd>

參考時間，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回轉換為毫秒的參考時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




