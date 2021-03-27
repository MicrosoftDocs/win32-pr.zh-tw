---
title: '」 lod (sm 4.1-asm) '
description: 傳回用於材質篩選 (」 LOD) 的詳細層級。
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679140"
---
# <a name="lod-sm41---asm"></a>」 lod (sm 4.1-asm) 

傳回用於材質篩選 (」 LOD) 的詳細層級。



| 」 lod dest \[ . mask \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler |
|--------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 結果的位址中。<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 一組材質座標中。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] 。<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[在 \] 取樣器註冊中。<br/>           |



 

## <a name="remarks"></a>備註

這種行為類似 [範例](sample--sm4---asm-.md) 指令，但不會產生已篩選的範例。 指令會計算下列向量 (ClampedLOD、NonClampedLOD、0、0) 。 NonClampedLOD 是一種計算的」 LOD 值，會忽略取樣器或材質 (的任何固定，也就是它可以傳回負值。 ) ClampedLOD 是計算的」 LOD 值，會由實際的 **範例** 指令使用。 *SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。

如果沒有任何資源系結至指定的位置，則會傳回0。

如果取樣器使用非等向性篩選，則」 LOD 應該根據橢圓磁片使用量的較小軸，對應至小數 mip 層級。

這適用于下列材質類型： Texture1D、Texture2D、Texture3D 和 TextureCube。

搭配指定點 mip 篩選的取樣器（特別是 \_ 在 mip 點結束的任何 D3D10 篩選準則列舉）使用時，不會定義」 lod 指令 \_ 。  (其中一個範例是 D3D10 \_ FILTER \_ MIN \_ MAG \_ MIP \_ POINT. ) 

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
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





