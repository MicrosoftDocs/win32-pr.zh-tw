---
description: 提醒宏會在編譯時期產生提醒。 此宏會產生字串，其中包含參數字串、原始程式檔的名稱，以及行號。
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: '提醒 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c17ec8fac190cd98803a0dfa85acff015d0ac2c18ce712cc87316dd2dca181bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952117"
---
# <a name="remind"></a>提醒

`REMIND`宏會在編譯時期產生提醒。 此宏會產生字串，其中包含參數字串、原始程式檔的名稱，以及行號。

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

文字字串。

</dd> </dl>

## <a name="remarks"></a>備註

此宏適用于產生編譯時期警告：


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
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

 

 




