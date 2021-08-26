---
title: 'imm_atomic_or (sm5-asm) '
description: 立即不可部分完成的位 OR 至記憶體。 傳回在或之前的記憶體中的值。
ms.assetid: 0ACE977D-5D0E-4E9C-A49F-B81D789B0D43
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4188e8b79cdf4d782ebc926645a4279d08c9682fd0ae254c2ce37c5fbcf46a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982098"
---
# <a name="imm_atomic_or-sm5---asm"></a>imm 不可部分完成 \_ \_ 或 (sm5-asm) 

立即不可部分完成的位 OR 至記憶體。 傳回在或之前的記憶體中的值。



| imm \_ 不可 \_ 部分完成或 dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] 、dst1、dstAddress \[ swizzle \] 、src0 \[ 。選取 \_ 元件\] |
|------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                           | 描述                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] 包含在或之前的 *dst1* 值。<br/>                                                                   |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[在 \] 未排序的存取視圖中 (UAV)  (u \#) 。 在計算著色器中，這也可以是執行緒群組的共用記憶體 (g \#) 。 <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[在 \] 記憶體位址中。<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | *Dst1* 的值。<br/>                                                                                           |



 

## <a name="remarks"></a>備註

此指令會在每個元件位址 *dstAddress* 的32位上執行單一元件32位位 or of 運算元 *src0* with *dst1* 。

如果 *dst1* 是 u \# ，則可能已宣告為 raw、具型別或結構化。 如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。

如果 *dst1* 為 g \# ，則必須將它宣告為 raw 或結構化。

在或之前 *dst1* 記憶體中的值會傳回至 *dst0*。

整個作業會以不可部分完成的方式執行。

從位址取得的元件數目取決於在 *dst1* 中宣告之資源的維度。

如果著色器調用處于非使用中狀態，例如，如果圖元先前在其執行過程中已捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令完全不會改變 *dst1* 記憶體，且傳回的值為未定義。

除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。

U 或 g 的超出範圍定址 \# \# 會導致未定義的結果傳回 *dst0* 中的著色器。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
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

 

 





