---
description: DbgInitialise 函式會初始化 debug 程式庫。 在零售組建中略過。
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: 'DbgInitialise 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995717"
---
# <a name="dbginitialise-function"></a>DbgInitialise 函式

**DbgInitialise** 函式會初始化 debug 程式庫。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hInst* 
</dt> <dd>

模組實例的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

在可執行檔中，請先呼叫這個方法，再使用 DirectShow debug 功能。 在可執行檔結束之前，呼叫 [**DbgTerminate**](dbgterminate.md) 函式來清除偵錯工具程式庫。

在連結至基類程式庫 (Strmbase .lib) 的 DLL 中，不需要呼叫此函式。 載入 DLL 時，會自動呼叫函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




