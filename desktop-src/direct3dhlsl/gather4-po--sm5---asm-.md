---
title: 'gather4_po (sm5-asm) '
description: Gather4 的變體，但不支援立即位移--8. 7 \，此位移是指令的參數，而且也有更大範圍的-32.. 31 \。
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971585"
---
# <a name="gather4_po-sm5---asm"></a>gather4 \_ po (sm5-asm) 

[Gather4](gather4--sm5---asm-.md)的變體，但不支援立即位移 \[ -8. 7 \] ，此位移會作為指令的參數，也會有較大範圍的 \[ -32.. 31 \] 。



| gather4 \_ po dest \[ . mask \] ，srcAddress \[ . swizzle \] ，srcOffset \[ . swizzle \] ，srcResource \[ ，swizzle \] ，srcSampler \[ . select \_ component\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 一組材質座標中。<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>         | \[在 \] 位移中。<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] 。<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[在 \] 取樣器註冊中。<br/>                         |



 

## <a name="remarks"></a>備註

4向量 offset 參數的前兩個元件提供32位整數位移。 系統會忽略此參數的其他元件。

每個位移值6個最少的有效位會接受為帶正負號的值，並產生 \[ -32.. 31 的 \] 範圍。

此指示只適用于2D 材質，不同于 **gather4**，它也可搭配 TextureCubes 使用。

取樣器中唯一接受的模式是定址模式。 只會使用資源檢視中最詳細的 mip。

如果位址落在材質中心，這並不表示其他材質可以清空。

*SrcSampler* 參數包含 \[ . select \_ 元件 \] ，允許抓取紋理的任何單一元件，包括傳回遺漏元件的預設值。

針對具有 float32 元件的格式，如果要提取的值是正規化、反正規化、+-0 或 +-INF，則會傳回未改變的著色器。 NaN 會以 NaN 傳回，但是 NaN 的精確位標記法可能會變更。 針對 TextureCubes，遺漏第四個材質的部分合成必須在角落髮生，因此不會套用合成材質未變更的位的概念，而且可以清除 denorms。

使用此指令可將 **gather4** 的位移範圍延伸到更大和可程式化。 名稱上的 "po" 尾碼表示「可程式化的位移」。

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

 

 





