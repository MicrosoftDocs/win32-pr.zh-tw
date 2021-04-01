---
title: 'gather4 (sm5-asm) '
description: '收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。 |gather4 (sm5-asm) '
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195950"
---
# <a name="gather4-sm5---asm"></a>gather4 (sm5-asm) 

收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。 此指示只適用于2D 或立方體貼圖材質，包括陣列。 只會使用取樣器的定址模式，並使用任何 mip 金字塔的最上層。



| gather4 \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler \[ . select \_ component\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 一組材質座標中。<br/>                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] 。<br/>                          |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[在 \] 取樣器註冊中。<br/>                          |



 

## <a name="remarks"></a>備註

此指令的行為就像 [**範例**](sample--sm4---asm-.md) 指令，但不會產生已篩選的範例。 這四個會造成篩選的範例會以順時針順序的方式放入 xyzw 中，從取樣到查詢位置的左下方開始。 這與 (u、v) 材質座標差異于下列位置的點取樣相同： (-、+) 、 (+、+) 、 (+、-) 、 (-,-) ，其中差異的大小一律為材質。

針對立方體貼圖材質，當雙線性使用量橫跨邊緣時，就會使用來自相鄰臉部的材質。 角落使用與 [**範例**](sample--sm4---asm-.md) 指令相同的規則;也就是說，未知的邊角會被視為三個 impinging 臉部角落的平均值。

有適用于 **gather4** 的材質格式限制（以格式清單表示）。

*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。

[ \_ *SrcSampler* 上的元件] 會選擇來源材質的哪個元件 (r/g/b/a) 讀取4個材質。

針對具有 float32 元件的格式，如果要提取的值是正規化、反正規化、+-0 或 +-INF，則會傳回未改變的著色器。 NaN 會以 NaN 傳回，但是 NaN 的精確位標記法可能會變更。 針對 TextureCubes，遺漏的第四個材質的部分合成必須在角落進行，因此不會套用合成材質未變更的位，而且可以清除 denorms。

針對硬體的執行，以傳統雙線性篩選進行優化，可直接在材質上偵測樣本，並略過讀取可能具有權數0的材質。 *gather4* 一律會傳回所有要求的材質。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





