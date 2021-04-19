---
description: 使用指定的字串、來源檔案的名稱和行號，顯示訊息方塊。 使用者可以忽略訊息、輸入偵錯工具，或結束應用程式。 在零售組建中略過。
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: 'DbgBreak 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983204"
---
# <a name="dbgbreak-macro"></a>DbgBreak 宏

使用指定的字串、來源檔案的名稱和行號，顯示訊息方塊。 使用者可以忽略訊息、輸入偵錯工具，或結束應用程式。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgBreak(
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

## <a name="examples"></a>範例


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Assert 和中斷點宏](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




