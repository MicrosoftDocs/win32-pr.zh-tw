---
title: 'gather4_po_c (sm5-asm) '
description: 的行為與 gather4 \_ po 相同，但在材質上執行比較，類似于範例 \_ c。
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83342aed97663c027b0915f612b13b288192d937d29d364257004cfc8966aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743868"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (sm5-asm) 

的行為與 [**gather4 \_ po**](gather4-po--sm5---asm-.md)相同，但在材質上執行比較，類似于 [**範例 \_ c**](sample-c--sm4---asm-.md)。



| gather4 \_ po \_ c dest \[ . mask \] 、srcAddress \[ . swizzle \] 、srcOffset \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler \[ 。R \] 、srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                                       | 描述                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                                            | \[在 \] 操作結果的位址中。<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[在 \] 一組材質座標中。<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[在 \] 位移中。<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[在材質暫存器中 \] 。<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[在 \] 取樣器註冊中。<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[在 \] 選取的單一元件中。<br/>                  |



 

## <a name="remarks"></a>備註

如需有關如何將 *srcReferenceValue* 與每個提取的材質進行比較的詳細資訊，請參閱 [**範例 \_ c**](sample-c--sm4---asm-.md) 。 不同于 **範例 \_ c**， *gather4 \_ po \_ c* 會傳回每個比較結果，而不是篩選結果。

此指令（例如 **gather4 \_ po**）僅適用于2d 材質。 這與 [**gather4 \_ c**](gather4-c--sm5---asm-.md)不同，它也可以搭配 TextureCubes 使用。

針對具有 float32 元件的格式，如果要提取的值是正規化的或 +-INF，比較作業就會使用此值。 在比較作業中使用 NaN 做為 NaN，但 NaN 的精確位標記法可能會變更。 Denorms 會排清到零進行比較。 針對 TextureCubes，遺漏的第四個材質的部分合成必須在角落進行，因此未變更合成材質的未變更的概念。

支援的 **gather4 \_ po \_ c** 格式與 **範例 \_ c** 所支援的格式相同。 這些都是單一元件格式，因此。SrcSampler 上的 R，而非任意 swizzle。

未系結資源上的 **gather4 \_ po \_ c** 會傳回0。

使用這個方法來進行陰影對應篩選。

此指示適用于下列著色器階段：



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

 

 





