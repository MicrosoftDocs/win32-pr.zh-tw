---
title: 'sample_c_lz (sm4-asm) '
description: 執行比較篩選。 此指令的行為類似範例 \_ c，但」 lod 為0，而衍生項則會被忽略。
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b2866bdfddf91f9bd6ab1bbccbc9d76de071065b3cf28c1093cb1fdb041f3db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981498"
---
# <a name="sample_c_lz-sm4---asm"></a>範例 \_ c \_ lz (sm4-asm) 

執行比較篩選。 此指令的行為類似 [範例 \_ c](sample-c--sm4---asm-.md)，但」 lod 為0，而衍生項則會被忽略。



| 範例 \_ c \_ lz \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource. r、//必須是. r swizzle srcSampler、srcReferenceValue//選取單一元件 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                                       | 描述                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                                            | \[在 \] 操作結果的位址中。<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[在 \] 一組材質座標中。 如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[在材質暫存器中 \] 。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[在 \] 取樣器註冊中。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[在 \] 已選取單一元件的註冊中，用於比較。<br/>                            |



 

## <a name="remarks"></a>備註

"Lz" 代表層級0。 因為會忽略衍生項，所以在圖元著色器以外的著色器中可使用此指令。

如果此指令搭配 mipmapped 材質使用，則會取樣」 LOD 0，除非取樣器有」 LOD 的夾具，這會將」 LOD 放在其他位置，或如果有」 LOD 偏差，這就是從0開始的偏差。 因為衍生的會被忽略，所以會以 isotropic 篩選的形式來運作。

在圖元著色器中，當材質座標衍生於著色器中時，此指令可在不同的流量控制內使用，與 **範例 \_ c** 不同。

從未系結任何專案的輸入位置提取，會針對所有元件傳回0。

此指示適用于所有著色器，而不只是圖元著色器，以保持一致性。



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

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

 

 





