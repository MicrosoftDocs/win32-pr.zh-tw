---
description: DbgOutString 函式會將字串傳送至調試輸出位置。 在零售組建中略過。
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: 'DbgOutString 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998794"
---
# <a name="dbgoutstring-function"></a>DbgOutString 函式

**DbgOutString** 函式會將字串傳送至調試輸出位置。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*psz* 
</dt> <dd>

要輸出的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

在 debug 組建中，此函式一律會輸出字串，而不論目前的偵錯工具輸出層級為何。 若要更精確地控制輸出，請使用 [**DbgLog**](dbglog.md) 宏。

## <a name="examples"></a>範例


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




