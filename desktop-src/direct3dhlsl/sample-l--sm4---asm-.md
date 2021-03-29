---
title: 'sample_l (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |sample_l (sm4-asm) '
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322320"
---
# <a name="sample_l-sm4---asm"></a>範例 \_ l (sm4-asm) 

使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。



| 範例 \_ l \[ \_ aoffimmi (u，v，w) \] dest \[ \] ，srcAddress \[ . swizzle \] ，srcResource \[ . swizzle \] ，srcSampler，srcLOD. select \_ component |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 一組材質座標中。 如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] 。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[在 \] 取樣器註冊中。 如需詳細資訊，請參閱 **範例** 指令。<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[在 \] 」 lod 中。<br/>                                                                                                 |



 

## <a name="remarks"></a>備註

此指示與 [範例](sample--sm4---asm-.md)相同，不同之處在于」 lod 是由應用程式直接提供為純量值，表示沒有 anisotropy。 此指示適用于所有 progammable 著色器階段。

**範例 \_ l** ：使用 *srcLOD* 作為」 lod 的材質範例。 如果」 LOD 值為 <= 0，則會選擇 zero'th (最大的地圖) ，並根據篩選模式) 套用放大篩選 (如果適用的話。 因為 *srcLOD* 是浮點值，所以如果縮短篩選準則為線性或使用非等向篩選，則會使用小數值在兩個 mip 層級之間插補。

**範例 \_ l** 會忽略位址衍生，因此篩選行為純粹是 isotropic。 因為衍生的會被忽略，所以會以 isotropic 篩選的形式來運作。

會接受取樣器狀態 MIPLODBIAS 和 MAX/MINMIPLEVEL。

在圖元著色器中使用時， **範例 \_ l** 表示選擇的」 lod 是每個圖元，而不會影響連續的圖元，例如在相同的2x2 戳記中。

從未系結任何專案的輸入位置提取，會針對所有元件傳回0。

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

 

 





