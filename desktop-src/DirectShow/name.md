---
description: NAME 宏會產生僅限 debug 的字串。
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: '名稱 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fa3d9c7e343dcbc8c6959a1ead025cafb3e4722382d7fd61c085bcff05347ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107678"
---
# <a name="name"></a>名稱

**NAME** 宏會產生僅限 debug 的字串。

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

文字字串。

</dd> </dl>

## <a name="remarks"></a>備註

在 debug 組建中，此宏相當於 **文字** 宏。 在零售組建中，它會解析為 (TCHAR \*) **Null**。 宣告衍生自 [**CBaseObject**](cbaseobject.md) 類別的物件名稱時，這個宏很有用。


```C++
pObject = new CBaseObject(NAME("My Object"));
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

 

 




