---
title: 'dmul (sm5-asm) '
description: 元件的雙精確度乘積。
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999085"
---
# <a name="dmul-sm5---asm"></a>dmul (sm5-asm) 

元件的雙精確度乘積。



| dmul \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> *目的地*  = *src0* \**src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要與 *src1* 相乘的元件中。<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要與 *src0* 相乘的元件中。<br/>                                          |



 

## <a name="remarks"></a>備註

來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。 有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。 以下是 swizzle 後的 *src* 對應：

-   *dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。
-   *src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。
-   *src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。

下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。

F 表示有限實數。



| **src0 src1->** | **-inf** | **-F** | **-1。0** | **-0** | **+0** | **+ 1。0** | **+ F** | **+ inf** | **NaN** |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-inf**           | +inf     | +inf   | +inf     | NaN    | NaN    | -inf     | -inf   | -inf     | NaN     |
| **-F**             | +inf     | +F     | -src0    | +0     | -0     | src0     | -F     | -inf     | NaN     |
| **-1.0 f**          | +inf     | -src1  | + 1。0     | +0     | -0     | -1.0     | -src1  | -inf     | NaN     |
| **-0**             | NaN      | +0     | +0       | +0     | -0     | -0       | -0     | NaN      | NaN     |
| **+0**             | NaN      | -0     | -0       | -0     | +0     | +0       | +0     | NaN      | NaN     |
| **+ 1。0**           | -inf     | src1   | -1.0     | -0     | +0     | +1       | src1   | +inf     | NaN     |
| **+ F**             | -inf     | -F     | -src0    | -0     | +0     | src0     | +F     | +inf     | NaN     |
| **+ inf**           | -inf     | -inf   | -inf     | NaN    | NaN    | +inf     | +inf   | +inf     | NaN     |
| **NaN**            | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





