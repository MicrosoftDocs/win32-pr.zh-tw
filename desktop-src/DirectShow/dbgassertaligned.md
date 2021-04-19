---
description: 測試指標是否對齊指定的界限。 如果沒有，此宏會叫用 ASSERT 宏。 在零售組建中略過。
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: 'DbgAssertAligned 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979571"
---
# <a name="dbgassertaligned-macro"></a>DbgAssertAligned 宏

測試指標是否對齊指定的界限。 如果沒有，此宏會叫用 [**ASSERT**](assert.md) 宏。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ptr* 
</dt> <dd>

指標變數。

</dd> <dt>

*對準* 
</dt> <dd>

需要的對齊方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個宏不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Assert 和中斷點宏](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




