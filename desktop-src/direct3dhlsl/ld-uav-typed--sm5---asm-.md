---
title: 'ld_uav_typed (sm5-asm) '
description: 從具類型的未排序存取視圖中隨機存取專案的讀取 (UAV) 。
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9685341f4a3a2e6b22bbbcc4b36f6ecccc153f17c67f38c390e6beeef94358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982068"
---
# <a name="ld_uav_typed-sm5---asm"></a>ld \_ uav \_ 類型 (sm5-asm) 

從具類型的未排序存取視圖中隨機存取專案的讀取 (UAV) 。



| ld \_ uav 具 \_ 類型的 dst0 \[ . mask \] 、srcAddress \[ . swizzle \] 、srcUAV \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| 項目                                                                                                           | 描述                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[在 \] 操作結果的位址中。<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[中的 \] 指定要讀取的位址。<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[\]來源中的讀取來源。 <br/>                    |



 

## <a name="remarks"></a>備註

此指令會從 *srcAddress* 中不帶正負號的整數位址，執行 *srcUAV* 讀取的4元件元素，並根據格式轉換為每個元件的32位，然後寫入著色器中的 *dst0* 。

*srcUAV* 是 UAV (u \#) 宣告為具類型。 不過，系結資源的類型必須是 R32 \_ UINT/聖/FLOAT。

從位址取得的32位不帶正負號整陣列件的數目，取決於在 *srcUAV* 中宣告之資源的維度。 定址與 [ld](ld--sm4---asm-.md) 指令相同。

超出範圍定址與 **ld** 指令相同。

此指令的行為與 **ld** 指令相同（如果呼叫的是 **ld dst0 \[ \] ，srcAddress \[ . swizzle \] ，srcUAV \[ . swizzle \]** ）。

它無效且未定義，無法在未宣告為具類型的 UAV 上使用這個指令。 在結構化或無別 UAV 上執行這項操作，是不正確。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。



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



 

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV、SRV 和 TGSM 的指令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





