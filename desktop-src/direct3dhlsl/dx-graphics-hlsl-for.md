---
title: for 陳述式
description: 根據條件運算式的評估，反復執行一系列的語句。
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for 語句 HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092357"
---
# <a name="for-statement"></a>for 陳述式

根據條件運算式的評估，反復執行一系列的語句。



|                                                                                       |
|---------------------------------------------------------------------------------------|
| \[*屬性* \]針對 (*初始化運算式;條件式反覆運算器*) {*語句區塊*;} |



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*
</dt> <dd>

可控制如何編譯語句的選擇性參數。 未指定屬性時，編譯器會先嘗試發出迴圈的累積版本，如果失敗，或者如果迴圈展開，某些作業會更容易，則會切換回迴圈的展開版本。



| 屬性             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 展開 (x)              | 展開迴圈，直到它停止執行為止。 可以選擇性地指定迴圈要執行的最大次數。 與 **\[ 迴圈 \]** 屬性不相容。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | 產生使用流程式控制制的程式碼，以執行迴圈的每個反復專案。 與 **\[ 展開 \]** 屬性不相容。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | 減少編譯時間，但不會產生較不積極的優化。 如果您使用這個屬性，編譯器將不會展開迴圈。<br/> 這個屬性只會影響支援 [break](dx-graphics-hlsl-break.md) 指令的著色器模型目標。 此屬性適用于著色器模型 [與 \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md) （含）以後版本。 當編譯器編譯迴圈時，此功能特別適用于 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更新版本。 編譯器預設會模擬迴圈，以評估它是否可以展開它們。 如果您不想讓編譯器展開迴圈，請使用這個屬性來減少編譯時間。 <br/> |
| 允許 \_ uav \_ 條件 | 允許計算著色器迴圈終止條件以 UAV 讀取為基礎。 迴圈不能包含同步處理內建函式。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*初始 化*
</dt> <dd>

迴圈計數器的初始值。

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*
</dt> <dd>

條件 [運算式](dx-graphics-hlsl-expressions.md)。 如果條件運算式評估為 true，則會執行語句區塊。 當運算式評估為 false 時，迴圈就會結束。

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*迭 代*
</dt> <dd>

更新迴圈計數器的值。

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*
</dt> <dd>

一或多個 [HLSL 語句](dx-graphics-hlsl-statement-blocks.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 展開 \]** 和 **\[ loop \]** 屬性是互斥的，並且會在同時指定兩者時產生編譯器錯誤。

如果指定了 **\[ 展開 \]** ，就會忽略 **\[ fastopt \]** 和 **\[ allow \_ uav \_ 條件 \]** 屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[流程式控制制](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





