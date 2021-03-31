---
title: 'emit_stream (sm5-asm) '
description: 將頂點發出至指定的資料流程。
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373770"
---
# <a name="emit_stream-sm5---asm"></a>發出 \_ stream (sm5-asm) 

將頂點發出至指定的資料流程。



| 發出 \_ 資料流程 streamIndex |
|--------------------------|



 



| 項目                                                                                                               | 描述                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[在 \] 資料流程索引中。<br/> |



 

## <a name="remarks"></a>備註

這個指令會讓指定資料流程的所有宣告的 o 緩存 \# 器從幾何著色器中讀出，以產生頂點。 Afer 發出，所有資料流程所有輸出暫存器中的所有資料都會變成未初始化，而不只是發出至的資料流程。

*streamIndex* 必須是宣告資料流程的立即值 \[ 0. 3。 \]

發出多個 **發出的 \_ 資料流程** 呼叫時，會產生基本專案。

### <a name="restrictions"></a>限制

-   **發出 \_ 資料流程** 可能會在幾何著色器中出現任何次數，包括 flow 控制項。
-   如果尚未宣告資料流程，您必須使用 [發出](emit--sm4---asm-.md) ，而不是 **發出 \_ 資料流程**。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





