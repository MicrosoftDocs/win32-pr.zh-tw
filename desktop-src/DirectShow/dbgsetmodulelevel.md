---
description: DbgSetModuleLevel 函數會設定一或多個訊息類型的記錄層級。 在零售組建中略過。
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: 'DbgSetModuleLevel 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983018"
---
# <a name="dbgsetmodulelevel-function"></a>DbgSetModuleLevel 函式

**DbgSetModuleLevel** 函數會設定一或多個訊息類型的記錄層級。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* 
</dt> <dd>

一或多個訊息類型的位元組合。

</dd> <dt>

*Level* 
</dt> <dd>

指定訊息類型的記錄層級。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




