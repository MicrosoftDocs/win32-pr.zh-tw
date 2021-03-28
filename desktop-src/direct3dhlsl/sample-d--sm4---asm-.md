---
title: 'sample_d (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |sample_d (sm4-asm) '
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992042"
---
# <a name="sample_d-sm4---asm"></a>範例 \_ d (sm4-asm) 

使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。



| ssample \_ d \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource、swizzle、 \[ \] srcSampler、srcXDerivatives \[ . swizzle \] 、srcYDerivatives \[ . swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                               | 描述                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                                    | \[在 \] 操作結果的位址中。<br/>                                                                  |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                     | \[在 \] 一組材質座標中。 如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。<br/>      |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                 | \[在材質暫存器中 \] 。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                      |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                     | \[在 \] 取樣器註冊中。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                      |
| <span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*<br/> | \[以 \] x 方向的來源位址衍生。 如需詳細資訊，請參閱「 **備註** 」一節。<br/> |
| <span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*<br/> | \[以 \] y 方向的來源位址衍生。 如需詳細資訊，請參閱「 **備註** 」一節。<br/> |



 

## <a name="remarks"></a>備註

此指示的行為就像 [範例](sample--sm4---asm-.md) 指令，不同之處在于 x 方向和 y 方向的來源位址衍生是由額外的參數（ *srcXDerivatives* 和 *srcYDerivatives*）所提供。 這些衍生的是標準化的材質座標空間。

*SrcXDerivatives* 的 r、g 和 b 元件 (POS swizzle) 提供 du/dx、dv/dx 和 dw/dx。 會忽略 ' a ' 元件 (POS swizzle) 。

*SrcYDerivatives* 的 r、g 和 b 元件 (POS-swizzle) 提供 du/dy、dv/dy 和 dw/dy。 會忽略 ' a ' 元件 (POS swizzle) 。

與範例指令不同，這是允許跨2x2 戳記共用單一」 LOD 計算的 **範例** 指令，因此，在圖元著色器中使用時， **範例 \_ d** 必須完全獨立地計算」 lod。

如果 **範例 \_ d** 的衍生輸入來自圖元著色器中的衍生計算指示，且值包含 INF/NaN，則 **範例 \_ d** 的行為可能與 **範例** 指令不相符，這會隱含地計算衍生。 INF/NaN 值可能會以不同的方式影響」 LOD 計算。

從未系結任何專案的輸入位置提取，會針對所有元件傳回0。

### <a name="restrictions"></a>限制

-   **範例 \_ d** 會繼承與 **範例** 指令相同的限制，再加上下列額外參數的限制。
-   *srcXDerivatives* 和 *srcYDerivatives* 必須是 temp (r \# /x \#) 、constantBuffer (cb \#) 、輸入 (v \#) 註冊或立即值 (s) 。

此指示適用于下列著色器階段：



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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





