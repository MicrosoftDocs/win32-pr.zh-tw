---
title: 'gather4 (sm 4.1-asm) '
description: '收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。 |gather4 (sm 4.1-asm) '
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb39918bdb421123cb3e2bfe41931740e271f85a27cf36b8994d493656d91c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457578"
---
# <a name="gather4-sm41---asm"></a>gather4 (sm 4.1-asm) 

收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。



| gather4 \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] srcSampler. r |
|--------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | 描述                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[中 \] 的包含材質座標。 <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在資源暫存器中 \] 。 <br/> Swizzle 可讓傳回的值在寫入至 *目的地* 之前，任意地 swizzled。 <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[在 \] 取樣器註冊中。<br/> 此參數的 (red) swizzle，表示 R 通道的值已複製到 *目的地*。 <br/> |



 

## <a name="remarks"></a>備註

此作業僅適用于單一通道2D 或立方體貼圖材質。 若是2D 紋理，則會使用取樣器的定址模式，並使用任何 mip 金字塔的最上層。

此指令的行為就像 [範例](sample--sm4---asm-.md) 指令，但不會產生已篩選的範例。 這四個會造成篩選的範例會以順時針順序的方式放入 xyzw 中，從取樣到查詢位置的左下方開始。 這與 (u、v) 材質座標差異于下列位置的點取樣相同： (-、+) 、 (+、+) 、 (+、-) 、 (-,-) ，其中差異的大小一律為材質。

當雙線性使用量橫跨鄰近臉部的邊緣材質時，適用于立方體貼圖紋理。 角落使用與 **範例** 指令相同的規則;這是未知的邊角會被視為三個 impinging 臉部角落的平均值。

適用于 **範例** 指令的材質格式限制也適用于 **gather4** 指令。

針對硬體的執行，在傳統雙線性篩選中進行優化，可直接在材質上偵測樣本，並略過讀取具有權數0的材質無法與 **gather4** 搭配使用。 **gather4** 一律會傳回所有要求的材質。

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
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





