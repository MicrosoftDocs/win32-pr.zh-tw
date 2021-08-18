---
description: 確認呼叫進程具有寬字元字串的讀取權限。 如果沒有，宏就會呼叫 DbgBreak 宏。
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: 'ValidateStringPtrW 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 71567070618796ad564b7f7fb5e8d854f580d482e91d9f4fd7381a582e32495c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755668"
---
# <a name="validatestringptrw-macro"></a>ValidateStringPtrW 宏

確認呼叫進程具有寬字元字串的讀取權限。 如果沒有，宏就會呼叫 [**DbgBreak**](dbgbreak.md) 宏。

> [!Note]  
> 這個宏已被取代。 在 Windows Vista (和更新版本的 Windows SDK 中) 此宏不會執行任何動作。

 

## <a name="syntax"></a>語法


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*p* 
</dt> <dd>

以 Null 結尾的寬字元字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個宏不會傳回值。

## <a name="remarks"></a>備註

除非包含了 DirectShow 的基類標頭檔，否則會忽略這個宏，除非已定義 debug、 \_ debug 或 VFWROBUST。 此宏可能會有顯著的效能成本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[指標驗證宏](pointer-validation-macros.md)
</dt> </dl>

 

 




