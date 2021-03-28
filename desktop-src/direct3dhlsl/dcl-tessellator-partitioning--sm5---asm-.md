---
title: 'dcl_tessellator_partitioning (sm5-asm) '
description: 在 [輪廓著色器宣告] 區段中宣告鑲嵌資料分割。
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373899"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>dcl \_ 鑲嵌 \_ 分割 (sm5-asm) 

在 [輪廓著色器宣告] 區段中宣告鑲嵌資料分割。



| dcl \_ 鑲嵌 \_ 分割 {資料分割 \_ 整數 \| 資料分割 \_ pow2 \|分割 \_ 小數 \_ 奇數| 分割 \_ 小數 \_ 偶數} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 描述                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*分割 \_ 整數資料 \| 分割 \_ pow2 \| 分割小數的 \_ \_ 奇數分割小數 \| \_ \_ 偶數*<br/> | \[在 \] 鑲嵌資料分割中。<br/> |



 

## <a name="remarks"></a>備註

從硬體觀點來看， \_ pow2 的行為就像 \_ 整數一樣。 HLSL 著色器作者及/或 compilercode 將 TessFactors 四捨五入為2的乘冪。

此指示適用于下列著色器階段：



| 頂點 | 船體                 | 網域 | 幾何 | 像素 | 計算 |
|--------|----------------------|--------|----------|-------|---------|
|        | 宣告區段 |        |          |       |         |



 

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

 

 





