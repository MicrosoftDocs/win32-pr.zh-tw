---
title: 'do 語句 (Ocidl) '
description: 持續執行一連串的語句，直到條件運算式失敗為止。
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- do 語句 HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118783"
---
# <a name="do-statement"></a>do 語句

持續執行一連串的語句，直到條件運算式失敗為止。

\[*屬性* \] (*條件* 式 ) 時，請進行 {*語句區塊*;}



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*
</dt> <dd>

可控制如何編譯語句的選擇性參數。



| 屬性 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | 減少編譯時間，但不會產生較不積極的優化。 如果您使用這個屬性，編譯器將不會展開迴圈。<br/> 這個屬性只會影響支援 [break](dx-graphics-hlsl-break.md) 指令的著色器模型目標。 此屬性適用于著色器模型 [與 \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md) （含）以後版本。 當編譯器編譯迴圈時，此功能特別適用于 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更新版本。 編譯器預設會模擬迴圈，以評估它是否可以展開它們。 如果您不想讓編譯器展開迴圈，請使用這個屬性來減少編譯時間。<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*
</dt> <dd>

一或多個 [語句](dx-graphics-hlsl-statement-blocks.md)。

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*
</dt> <dd>

條件 [運算式](dx-graphics-hlsl-expressions.md)。 語句區塊會在評估運算式之前執行。 當運算式評估為 false 時，就會結束迴圈。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Ocidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[流程式控制制](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





