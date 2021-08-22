---
title: 'imm_atomic_consume (sm5-asm) '
description: 以不可部分完成的方式遞減以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回新的值。
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0244b885d9d2c46b734994d5e101f79147839d0cf76e2bab5669e52700cf59e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119312"
---
# <a name="imm_atomic_consume-sm5---asm"></a>imm 不可部分完成 \_ \_ 的使用 (sm5-asm) 

以不可部分完成的方式遞減以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回新的值。



| imm 不可部分完成的 \_ \_ 使用 dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] ，dstUAV |
|---------------------------------------------------------------|



 



| 項目                                                                                           | 描述                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[中 \] 的包含傳回的原始計數器值。<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[在 \] 具有 Count 或 Append 旗標的結構化緩衝區 UAV 中。 <br/> |



 

## <a name="remarks"></a>備註

請參閱「imm 不可部分完成」配置，以瞭解傳回的計數值是否有效，取決於 UAV 是 Count 或 Append。 [ \_ \_ ](imm-atomic-alloc--sm5---asm-.md) 這同樣適用于 imm 不可部分完成的 **\_ \_ 使用**。

imm 不可部分完成的 **\_ \_ 使用** 會執行計數器值的不可部分完成遞減，並將新值傳回給 *dst0*。

沒有計數的固定，所以它會在下溢處進行換行。

相同的著色器無法在相同的 UAV 上 **嘗試 \_ \_ 使用** imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_** 此外，GPU 無法允許多個著色器調用在相同的 UAV 上混合使用 imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_** **\_ \_**

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



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





