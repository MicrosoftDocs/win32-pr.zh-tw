---
title: 'sample_c (sm4-asm) '
description: 執行比較篩選。
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2656f70a95487ce98aadc30a028fccaed00cb1c8d6324d64bb22c9672543d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067728"
---
# <a name="sample_c-sm4---asm"></a>範例 \_ c (sm4-asm) 

執行比較篩選。



| 範例 \_ c \[ \_ aoffimmi (u，v，w) \] dest \[ \] ，srcAddress \[ . swizzle \] ，srcResource. r，//必須是。 r swizzle srcSampler，srcReferenceValue//選取單一元件 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                                       | 描述                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                                            | \[在 \] 操作結果的位址中。<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[在 \] 一組材質座標中。 如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[在材質暫存器中 \] 。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[在 \] 取樣器註冊中。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[在 \] 已選取單一元件的註冊中，用於比較。<br/>                            |



 

## <a name="remarks"></a>備註

此指示的主要目的是提供 Percentage-Closer 深度篩選的建立區塊。 **範例 \_ c** 中的 "c" 代表比較。

**範例 \_ c** 的運算元與 [範例](sample--sm4---asm-.md)指令相同，不同之處在于有一個額外的 float32 來源運算元 *srcReferenceValue*，它必須是已選取單一元件的暫存器，或純量常值。

SrcResource 參數的參數必須是. r (red) swizzle。 **範例 \_ c** 專門針對 red 元件運作，並傳回單一值。 *SrcResource* 上的 r swizzle 表示純量結果會複寫到所有元件。

當深度緩衝區設定為輸入材質時，[深度] 值會顯示在紅色的元件中。

如果這個指令與非 Texture1D/2D/2DArray/Cube/CubeArray 的資源搭配使用，它會產生未定義的結果。

當執行此指令時，取樣硬體會使用目前取樣器的 ComparisonFunction，針對每個篩選「點」位置上來源資源的紅色元件值進行比較 *srcReferenceValue* ， (材質) 目前設定的材質篩選器會根據 *srcAddress* 中提供的座標來涵蓋。

在 *srcReferenceValue* 已量化至材質格式的有效位數之後，會進行比較，與在輸出合併可見度測試的深度比較之前，z 的量化為深度緩衝區精確度的方式完全相同。 這包括格式範圍的夾具 (例如 \[ 0 ..1 \] 表示 UNORM 格式) 。

來源材質的紅色元件會與量化 *srcReferenceValue* 進行比較。 若為落在資源的材質，則會藉由套用位址模式 (和 BorderColorR （如果是以框線模式從取樣器) ）來判斷紅色元件值。 這項比較會接受所有的 D3D11 浮點數比較規則，在此情況下，材質格式為浮點數。

每次傳遞的比較都會傳回 1.0 f 做為材質的紅色元件值，而失敗的每個比較都會傳回 0.0 f 作為紋理的紅色值。 然後篩選會完全依照取樣器狀態所指定、只在 Red 元件中運作，並將單一純量篩選結果傳回給著色器，並複寫到所有遮罩的 *目的地* 元件。

**範例 \_ c** 的使用會與其他所有一般用途篩選控制項相互交。 **範例 \_ c** 可與其他一般用途篩選模式緊密搭配運作。 **範例 \_ c** 會變更一般用途篩選器的行為，使篩選的值全都會因為比較結果而變成 1.0 f 或 0.0 f。

從未系結任何專案的輸入位置提取，會針對所有元件傳回0。

如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





