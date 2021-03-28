---
title: 'store_uav_typed (sm5-asm) '
description: 隨機存取將專案寫入至具類型的未排序存取視圖 (UAV) 。
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022808"
---
# <a name="store_uav_typed-sm5---asm"></a>儲存 \_ uav \_ 類型 (sm5-asm) 

隨機存取將專案寫入至具類型的未排序存取視圖 (UAV) 。



| store \_ uav 具 \_ 類型的 dstUAV. Xyzw、dstAddress \[ . swizzle \] 、src0 \[ . swizzle\] |
|-------------------------------------------------------------------------|



 



| 項目                                                                                                           | 描述                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[中的 \] 包含運算的結果。<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[在 \] 要寫入的位址中。<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[在 \] 要寫入的元件中。<br/>              |



 

## <a name="remarks"></a>備註

此指令會在 \* *dstAddress* 的位址執行從 *src0* 寫入至 *dstUAV* 的4個元件32位元素。 *dstUAV* 是具類型的 UAV (u \#) 。

UAV 的格式會決定格式轉換。

從位址取得的32位不帶正負號整陣列件的數目，取決於在 *dstUAV* 中宣告之資源的維度。 此位址是在元素中。

超出範圍定址表示不會將任何內容寫入記憶體。

*dstUAV* 一律有 xyzw 寫入遮罩。 必須撰寫所有的元件。

它無效且未定義，無法在未宣告為具類型的 UAV 上使用這個指令。 也就是說，在結構化或無類型的 UAV 上執行這項操作將會無效。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。



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

 

 





