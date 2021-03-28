---
title: 'cut_stream (sm5-asm) '
description: 幾何著色器指令，會在指定的資料流程上完成目前的基本拓撲，如果已發出任何頂點，並啟動該資料流程上幾何著色器所宣告類型的新拓撲。
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373735"
---
# <a name="cut_stream-sm5---asm"></a>剪下 \_ 資料流程 (sm5-asm) 

幾何著色器指令，會在指定的資料流程上完成目前的基本拓撲，如果已發出任何頂點，並啟動該資料流程上幾何著色器所宣告類型的新拓撲。



| 剪下 \_ 資料流程 streamIndex |
|-------------------------|



 



| 項目                                                                                                               | 描述                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[在 \] 資料流程索引中。<br/> |



 

## <a name="remarks"></a>備註

當執行此指令時，會完成任何先前由幾何著色器調用發出的拓撲。 如果未針對先前的基本拓撲發出足夠的頂點，則會捨棄這些頂點。 因為幾何著色器的唯一可用輸出拓撲是 pointlist、linestrip 和 trianglestrip，所以永遠不會有任何剩餘的頂點。

*streamIndex* 必須是宣告資料流程的立即值 \[ 0. 3。 \]

在先前的拓撲（如果有的話）完成之後，此指示會使用宣告為幾何著色器輸出的拓撲來開始新的拓撲。

### <a name="restrictions"></a>限制

-   此指令僅適用于幾何著色器。
-   **剪下 \_ 資料流程** 可能會在幾何著色器中出現任何次數，包括在流程式控制制內。
-   如果幾何著色器結束且頂點已發出，則會完成其所建立的拓撲，如同剪下 **\_ 資料流程** 指令做為最後一個指令執行一樣。
-   如果尚未宣告資料流程，您必須使用 [剪](cut--sm4---asm-.md) 下，而不是 **剪下 \_ 資料流程**。

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

 

 





