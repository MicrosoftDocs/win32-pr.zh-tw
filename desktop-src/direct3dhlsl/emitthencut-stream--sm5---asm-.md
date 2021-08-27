---
title: 'emitThenCut_stream (sm5-asm) '
description: '相當於發出命令，後面接著剪下命令。 |emitThenCut_stream (sm5-asm) '
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d2be28ae1d63617b8ba775f8f8839c270668aeeded8a4944ef9ae7554d598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067958"
---
# <a name="emitthencut_stream-sm5---asm"></a>emitThenCut \_ stream (sm5-asm) 

相當於 [發出](emit--sm4---asm-.md) 命令，後面接著 [剪](cut--sm4---asm-.md) 下命令。



| emitThenCut \_ 資料流程 streamIndex |
|---------------------------------|



 



| 項目                                                                                                               | 描述                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[在 \] 資料流程索引中。<br/> |



 

## <a name="remarks"></a>備註

當故意輸出拓撲中的最後一個頂點時，此作業會很有用。

如果尚未宣告資料流程，您必須使用 [emitThenCut](emitthencut--sm4---asm-.md) ，而不是 **emitThenCut \_ 資料流程**。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 否        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





