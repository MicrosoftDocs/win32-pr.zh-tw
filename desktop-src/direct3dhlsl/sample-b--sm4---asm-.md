---
title: 'sample_b (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |sample_b (sm4-asm) '
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196067"
---
# <a name="sample_b-sm4---asm"></a>範例 \_ b (sm4-asm) 

使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。



| 範例 \_ b \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler、srcLODBias. 選取 \_ 元件 |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 一組材質座標中。 如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] 。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[在 \] 取樣器註冊中。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[\]如需此參數的詳細資訊，請參閱「**備註**」一節。<br/>                                        |



 

## <a name="remarks"></a>備註

來源資料可能來自于緩衝區以外的任何資源類型。 額外的偏差會套用至在指令執行過程中計算的詳細資料層級。

此指令的行為就像是 [範例](sample--sm4---asm-.md) 指令，其中新增了將指定的 *srcLODBias* 值套用至在選取 mip map (s) 之前，在指示執行過程中計算的詳細資料值層級。 *SrcLODBias* 值會以每圖元為單位新增至計算的」 lod，以及在要 MinLOD 和 MaxLOD 的夾具之前的取樣器 MipLODBias 值。

### <a name="restrictions"></a>限制

-   **範例 \_ b** 會繼承與 [範例](sample--sm4---asm-.md) 指令相同的限制，再加上其他參數的其他限制。
-   *SrcLODBias* 範圍是 (-16.0 f 到 15.99 f) ;此範圍外的值會產生未定義的結果。
-   如果 *srcLODBias* 不是純量立即的，則必須使用單一元件選取器。

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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





