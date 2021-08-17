---
description: DbgDumpObjectRegister 函式會顯示作用中物件的相關資訊。 在零售組建中略過。
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: 'DbgDumpObjectRegister 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d82d7b419949210e19460880126a07ad52f63ae59f6055e5a2b968a2dd5c7beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821575"
---
# <a name="dbgdumpobjectregister-function"></a>DbgDumpObjectRegister 函式

此函式會 `DbgDumpObjectRegister` 顯示作用中物件的相關資訊。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

在 debug 組建中，debug 程式庫會維護使用中物件的清單。 此清單包含任何衍生自 [**CBaseObject**](cbaseobject.md)的物件、目前的模組所建立的物件，而且尚未終結。 **CBaseObject** 的函式和析構函數方法會更新清單。

此函數會產生數個記錄檔 \_ 記憶體訊息。 在記錄層級1，此函數只會顯示物件的總數。 在記錄層級2或更高層級，它會顯示物件的清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




