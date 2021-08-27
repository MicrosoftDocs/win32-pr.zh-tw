---
title: 'mul (sm4-asm) '
description: 元件的乘積。
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0185f0d11807ddc8cfc7b057cf9a8af1bc49e199d187c01bf16029e0ce54d018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118348"
---
# <a name="mul-sm4---asm"></a>mul (sm4-asm) 

元件的乘積。



| mul \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                        |
|-----------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。 dest = src0 \* src1<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 被乘數中。<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 乘數中。<br/>                                  |



 

## <a name="remarks"></a>備註

下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。

F 表示有限實數。



| **src0 src1->** | **-inf** | **-F** | **-1。0** | **-denorm** | **-0** | **+0** | **denorm** | **+ 1。0** | **+ F** | **+ inf** | **NaN** |
|---------------------|----------|--------|----------|-------------|--------|--------|------------|----------|--------|----------|---------|
| **-inf**            | +inf     | +inf   | +inf     | NaN         | NaN    | NaN    | NaN        | -inf     | -inf   | -inf     | NaN     |
| **-F**              | +inf     | +F     | -src0    | +0          | +0     | -0     | -0         | src0     | -F     | -inf     | NaN     |
| **-1**              | +inf     | -src1  | + 1。0     | +0          | +0     | -0     | -0         | -1.0     | -src1  | -inf     | NaN     |
| **-denorm**         | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **-0**              | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **+0**              | 電子     | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+ denorm**         | NaN      | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+ 1。0**            | -inf     | src1   | -1.0     | -0          | -0     | +0     | +0         | + 1。0     | src1   | +inf     | NaN     |
| **+ F**              | -inf     | -F     | -src0    | -0          | -0     | +0     | +0         | src0     | +F     | +inf     | NaN     |
| **+ inf**            | -inf     | -inf   | -inf     | NaN         | NaN    | NaN    | NaN        | +inf     | +inf   | +inf     | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN         | NaN    | NaN    | NaN        | NaN      | NaN    | NaN      | NaN     |



 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

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

 

 





