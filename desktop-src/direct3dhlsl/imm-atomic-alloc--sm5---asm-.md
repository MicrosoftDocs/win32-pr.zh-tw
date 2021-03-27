---
title: 'imm_atomic_alloc (sm5-asm) '
description: 以不可部分完成的方式遞增以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回原始值。
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679151"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>imm 不可部分完成配置 \_ \_ (sm5-asm) 

以不可部分完成的方式遞增以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回原始值。



| imm 不可部分完成配置 \_ \_ dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] ，dstUAV |
|-------------------------------------------------------------|



 



| 項目                                                                                           | 描述                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[中 \] 的包含傳回的計數器值。<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[在 \] 具有 Count 或 Append 旗標的結構化緩衝區 UAV 中。 <br/> |



 

## <a name="remarks"></a>備註

有一個隱藏的不帶正負號32位整數計數器值與每個計數或附加緩衝區視圖相關聯，此值會在 view 系結至管線時初始化，包括保留先前值的選項。

此指令會執行計數器值的不可部分完成遞增，並將原始值傳回給 *dst0*。

針對附加 UAV，傳回的值僅適用于著色器調用的持續時間。 之後，執行可能會重新排列記憶體配置。 任何以傳回值為基礎的記憶體定址都必須限制為著色器調用。

針對附加 UAV，在著色器調用中，HLSL 編譯器可以使用傳回的值做為用來存取結構化緩衝區的結構索引。 存取由呼叫 (s 所傳回的任何結構索引，) 至 imm 不可部分完成的配置或 [ \_ 使用](imm-atomic-consume--sm5---asm-.md)會產生未定義的結果，即表示正在存取 UAV 中的記憶體位置是隨機的，而且只會在著色器調用的存留期內修正。 **\_ \_**

針對計數 UAV，應用程式可以將傳回的值儲存為 UAV 內的固定位置參考，而該位置在著色器調用結束後有意義。 計數 UAV 中的任何位置，都可以永遠存取，而不受 count 值的影響。

沒有計數的固定，所以它會在溢位時換行。

相同的著色器無法在相同的 UAV 上 **嘗試 \_ \_ 使用** imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_** 此外，GPU 無法允許多個著色器調用在相同的 UAV 上混合使用 imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_** **\_ \_**

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

 

 





