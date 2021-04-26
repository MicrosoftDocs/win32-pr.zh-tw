---
title: 'rcp (sm5-asm) '
description: 元件的相互比較。
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998245"
---
# <a name="rcp-sm5---asm"></a>rcp (sm5-asm) 

元件的相互比較。



| rcp \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 結果的位址中<br/> *目的地*  = **1.0 f**  / *src0*。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]要採用的數位。<br/>                             |



 

## <a name="remarks"></a>備註

請使用此指令來取得較低的精確度，而不受限於除的嚴格需求。

相對錯誤的最大值是2-21。  (容錯功能只符合 rsq) 

下表顯示使用各種不同的數位類別來執行指令時所取得的結果。



| *src*  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F** | **+ inf** | **NaN** |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| *目標* | -0       | -F     | -inf        | -inf   | +inf   | +inf        | +F     | +0       | NaN     |



 

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





