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
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994697"
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

 

 




