---
description: DbgCheckModuleLevel 函式會檢查是否已針對指定的訊息類型和層級啟用記錄功能。 在零售組建中略過。
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: 'DbgCheckModuleLevel 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd6d7c61e7989987401c22386054c02f87410ce66dbb98bb6e20a813f2c851be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823698"
---
# <a name="dbgcheckmodulelevel-function"></a>DbgCheckModuleLevel 函式

`DbgCheckModuleLevel`函數會檢查是否已針對指定的訊息類型和層級啟用記錄。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
BOOL DbgCheckModuleLevel(
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

記錄層級

</dd> </dl>

## <a name="return-value"></a>傳回值

如果指定之任何訊息類型的記錄設定為指定的層級或更高的層級，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




