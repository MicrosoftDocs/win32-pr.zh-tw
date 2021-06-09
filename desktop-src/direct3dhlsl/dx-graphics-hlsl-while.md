---
title: while 陳述式
description: 在條件運算式失敗之前執行語句區塊。
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while 語句 HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826671"
---
# <a name="while-statement"></a>while 陳述式

在條件運算式失敗之前執行語句區塊。

\[*屬性* \]while (*條件* 式 ) {*語句區塊*;}



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*
</dt> <dd>

可控制如何編譯語句的選擇性參數。



| 屬性             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 展開 (x)              | 展開迴圈，直到它停止執行為止。 您可以選擇性地指定迴圈可執行檔最大次數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | 在編譯的著色器中使用流程式控制制語句;請勿展開迴圈。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | 減少編譯時間，但不會產生較不積極的優化。 如果您使用這個屬性，編譯器將不會展開迴圈。<br/> 這個屬性只會影響支援 [break](dx-graphics-hlsl-break.md) 指令的著色器模型目標。 此屬性適用于著色器模型 [與 \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md) （含）以後版本。 當編譯器編譯迴圈時，此功能特別適用于 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更新版本。 編譯器預設會模擬迴圈，以評估它是否可以展開它們。 如果您不想讓編譯器展開迴圈，請使用這個屬性來減少編譯時間。<br/> |
| 允許 \_ uav \_ 條件 | 允許計算著色器迴圈終止條件以 UAV 讀取為基礎。 迴圈不能包含同步處理內建函式。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*
</dt> <dd>

條件 [運算式](dx-graphics-hlsl-expressions.md)。 如果運算式評估為 true，則會執行語句區塊。 當運算式評估為 false 時，迴圈就會結束。

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*
</dt> <dd>

一或多個 [語句](dx-graphics-hlsl-statement-blocks.md)。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[流程式控制制](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





