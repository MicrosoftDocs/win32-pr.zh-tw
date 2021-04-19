---
description: 確認呼叫進程具有記憶體區塊的讀取/寫入存取權。 如果沒有，宏就會呼叫 DbgBreak 宏。
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: 'ValidateReadWritePtr 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979593"
---
# <a name="validatereadwriteptr-macro"></a>ValidateReadWritePtr 宏

確認呼叫進程具有記憶體區塊的讀取/寫入存取權。 如果沒有，宏就會呼叫 [**DbgBreak**](dbgbreak.md) 宏。

> [!Note]  
> 這個宏已被取代。 在 Windows Vista (和更新版本的 Windows SDK 中) 此宏不會執行任何動作。

 

## <a name="syntax"></a>語法


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*P* 
</dt> <dd>

記憶體區塊的指標。

</dd> <dt>

*Cb* 
</dt> <dd>

記憶體區塊的大小（以位元組為單位）。

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

 

 




