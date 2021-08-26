---
title: 'dcl_uav_typed (sm5-asm) '
description: '宣告未排序的存取視圖 (UAV) 供著色器使用。 |dcl_uav_typed (sm5-asm) '
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec321389f8c8296bda8ccd1eba947b5ba38adc80c94b3c8c0685b069fcdafbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950578"
---
# <a name="dcl_uav_typed-sm5---asm"></a>\_uav 具 \_ 類型的 sm5-asm)  (

宣告未排序的存取視圖 (UAV) 供著色器使用。



| dcl \_ uav 具 \_ 類型 \[ \_ \] 的 glc dstUAV、dimension、type |
|--------------------------------------------------|



 



| 項目                                                                                           | 描述                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[在 \] UAV 中。<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*維 度*<br/>                 | \[中的 \] 會指定存取 UAV 的指示所提供的維度數目。<br/> |
| <span id="type"></span><span id="TYPE"></span>*類型*<br/>                                | \[在 \] UAV 的類型中。<br/>                                                            |



 

## <a name="remarks"></a>備註

*dstUAV* 是宣告 \# 為 UnorderedAccessView 的參考，而該必須系結至 API 的 UAV \# 位置。

維度必須是 buffer、Texture1D、Texture1DArray、Texture2D、Texture2DArray 或 Texture3D。 這表示有多少維度可存取 UAV 的任何指示提供： 1 (Texture1D、Buffer) 、2 (Texture1DArray、Texture2D) 或 3 (Texture2DArray、Texture3D) 。

類型為 {UNORM，SNORM，UINT，聖，FLOAT}。 使用宣告 u 完成的作業 \# 必須與此處宣告的型別相容，而且系結至位置的 UAV \# 也必須具有相同的類型。

\_Glc 旗標代表「全域一致」。 缺少 \_ glc 表示 UAV 在計算著色器中宣告為「群組一致」，或在單一圖元著色器調用中宣告為「本機一致」。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> 計算著色器4.x 不支援此指令。

 

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

 

 





