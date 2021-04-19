---
description: 導致中斷點例外狀況，並使用 DbgLog 宏來記錄指定的字串。 在零售組建中略過。
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: 'KDbgBreak 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985974"
---
# <a name="kdbgbreak-macro"></a>KDbgBreak 宏

導致中斷點例外狀況，並使用 [**DbgLog**](dbglog.md) 宏來記錄指定的字串。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*strLiteral* 
</dt> <dd>

文字字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個宏不會傳回值。

## <a name="remarks"></a>備註

與 [**DbgBreak**](dbgbreak.md) 宏不同的是，此宏不會顯示提示使用者的訊息方塊。 在 debug 組建中，它會自動產生中斷點例外狀況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Assert 和中斷點宏](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




