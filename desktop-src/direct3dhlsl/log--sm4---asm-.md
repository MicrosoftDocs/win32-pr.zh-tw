---
title: '記錄 (sm4-asm) '
description: 以元件為基礎的記錄基底2。
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998315"
---
# <a name="log-sm4---asm"></a>記錄 (sm4-asm) 

以元件為基礎的記錄基底2。



| 記錄 \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle |
|----------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> dest = log2 (src0) <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在作業 \] 的值中。<br/>                                             |



 

## <a name="remarks"></a>備註

### <a name="restrictions"></a>限制

-   遵循限制理論。
-   容錯：如果 *src0* 為 \[ 0.5，則 \] absolue 錯誤必須不超過2-21。 如果 *src0* 是 (0. 0.5) 或 (2. + INF，則 \] 相對錯誤不能超過2-21。

下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。 F 表示有限實數。



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F** | **+ inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **目標** | NaN      | NaN    | -inf        | -inf   | -inf   | -inf        | F      | +inf     | NaN     |



 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





