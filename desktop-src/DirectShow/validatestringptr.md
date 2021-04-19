---
description: 確認呼叫進程具有字串的讀取存取權。 如果沒有，宏就會呼叫 DbgBreak 宏。
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: 'ValidateStringPtr 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997801"
---
# <a name="validatestringptr-macro"></a>ValidateStringPtr 宏

確認呼叫進程具有字串的讀取存取權。 如果沒有，宏就會呼叫 [**DbgBreak**](dbgbreak.md) 宏。

> [!Note]  
> 這個宏已被取代。 在 Windows Vista (和更新版本的 Windows SDK 中) 此宏不會執行任何動作。

 

## <a name="syntax"></a>語法


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*P* 
</dt> <dd>

以 Null 終止的 **TCHAR** 字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個宏不會傳回值。

## <a name="remarks"></a>備註

除非包含了 DirectShow 基類標頭檔，否則會忽略這個宏，除非已定義 DEBUG、 \_ debug 或 VFWROBUST。 此宏可能會有顯著的效能成本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[指標驗證宏](pointer-validation-macros.md)
</dt> </dl>

 

 




