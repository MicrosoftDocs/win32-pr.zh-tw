---
title: 'dmov (sm5-asm) '
description: '元件取向的移動。 |dmov (sm5-asm) '
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103946022"
---
# <a name="dmov-sm5---asm"></a>dmov (sm5-asm) 

元件取向的移動。



| dmov \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|-------------------------------------------------------------|



 



| 項目                                                            | 描述                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 移動目的地。 *目的地*  = *src0*。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要移動的元件中。<br/>            |



 

## <a name="remarks"></a>備註

Swizzle 以外的修飾詞會假設資料是浮點。 缺少修飾詞會移動資料，而不會改變位。

來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。 以下是 swizzle 後的 *src* 對應：

-   *src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。
-   *src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





