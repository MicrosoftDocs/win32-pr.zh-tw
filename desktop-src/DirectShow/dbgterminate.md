---
description: DbgTerminate 函式會清除 debug 程式庫。 在零售組建中略過。
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: 'DbgTerminate 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6846f6899730a8b9d128d1bc0a6069fd8a67a5f4f9d8a5a3d618bebad67b0468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821563"
---
# <a name="dbgterminate-function"></a>DbgTerminate 函式

**DbgTerminate** 函式會清除 debug 程式庫。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

如果您呼叫 [**DbgInitialise**](dbginitialise.md) 函數，請呼叫此函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




