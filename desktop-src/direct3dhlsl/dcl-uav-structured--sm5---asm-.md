---
title: 'dcl_uav_structured (sm5-asm) '
description: '宣告未排序的存取視圖 (UAV) 供著色器使用。 |dcl_uav_structured (sm5-asm) '
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195954"
---
# <a name="dcl_uav_structured-sm5---asm"></a>dcl \_ uav \_ 結構化 (sm5-asm) 

宣告未排序的存取視圖 (UAV) 供著色器使用。



| dcl \_ uav \_ 結構化 \[ \_ glc \] dstUAV、structByteStride |
|--------------------------------------------------------|



 



| 項目                                                                                                                                   | 描述                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[在 \] UAV 中。<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[以 \] 位元組為單位的結構大小。<br/> |



 

## <a name="remarks"></a>備註

*dstUAV* 是宣告 \# 為結構化緩衝區 UnorderedAccessView 參考的 u 暫存器，其指定的 stride 必須系結至 API 的 UAV \# 位置。

結構的內容沒有類型;在記憶體上執行的作業可能會隱含地將資料解讀為具有類型。

*structByteStride* 是要宣告的緩衝區中的結構大小（以位元組為單位）。 這個值必須大於零。 *structByteStride* 是 uint 類型，而且必須是4的倍數。

參考結構化 u 的指示 \# 會採用2d 位址，其中第一個元件挑選 \[ 結構 \] ，而第二個元件則挑選 \[ 結構內的位移（以對齊的位元組為單位） \] 。

\_Glc 旗標表示「全域一致」。 缺少 \_ glc 表示 UAV 在計算著色器中宣告為「群組一致」，或在單一圖元著色器調用中宣告為「本機一致」。

\_Opc 旗標是「訂單保留」計數器。 這表示，如果 UAV 系結至 \# (u) 的位置 \# ，則必須使用計數器旗標來建立它。 這表示，在著色器中的 imm 不可部分完成配置或 imm 不可部分完成取用作業會操作一個計數器，其值可以在著色器中當做 UAV 中位置的永久參考[ \_ \_ ](imm-atomic-alloc--sm5---asm-.md)使用。 [ \_ \_ ](imm-atomic-consume--sm5---asm-.md) 在著色器結束之後，資料無法重新排序。

缺少 \_ opc 旗標表示如果著色器使用了 imm 不可部分完成配置或 imm 不可部分完成的[ \_ \_ 使用](imm-atomic-consume--sm5---asm-.md)指示，且 UAV 系結至 (u) 的位置[ \_ \_ ](imm-atomic-alloc--sm5---asm-.md) \# ，則必須已使用 APPEND 旗標建立此旗標，此旗標提供的計數器不保證會在著色器調用之後保留順序。

如果不 \_ 存在 opc 旗標，且著色器未包含 [imm \_ \_ ](imm-atomic-alloc--sm5---asm-.md) 不可部分完成配置或 imm 不可部分完成的 [ \_ \_ 使用](imm-atomic-consume--sm5---asm-.md) 指示，則 \# 會允許使用計數器旗標來建立系結至插槽 (u) 的 UAV， (計數器將不會被此著色器) 、不 (任何旗標) ，但不會使用附加旗標。

> [!Note]  
> cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援 **\_ tgsm \_ 結構化**，但不 [支援 \_ tgsm \_ 原始](dcl-tgsm-raw--sm5---asm-.md)的 dcl。

 

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



 

> [!Note]  
> Cs \_ 4 \_ 0 和 cs \_ 4 1 支援這個指令 \_ 。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





