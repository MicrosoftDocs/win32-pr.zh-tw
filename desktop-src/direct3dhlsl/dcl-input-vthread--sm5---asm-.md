---
title: 'dcl_input vThread (sm5-asm) '
description: 宣告計算著色器輸入識別碼。
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c7eef8fe85ae39fb61d9e34b600805d38f7b92d5dbceb7dc2218b1515b6d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286196"
---
# <a name="dcl_input-vthread-sm5---asm"></a>dcl \_ 輸入 vThread (sm5-asm) 

宣告計算著色器輸入識別碼。



| dcl \_ 輸入 {vThreadID.xyz \|vThreadGroupID.xyz \| vThreadIDInGroup.xyz \|vThreadIDInGroupFlattened} |
|--------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                                                                                                                                                                                                                                                          | 描述                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*<br/> | \[在 \] 3 個元件的 [不帶正負號 32-位整數識別碼] 值。<br/> |



 

在其他著色器階段中， **dcl \_ 輸入** 是現有的宣告。 它是在計算著色器中用來宣告不同于計算著色器的3個元件不帶正負號32位整數識別碼值。 這些包括：

-   vThreadID.xyz
-   vGroupID.xyz
-   vThreadIDInGroup.xyz
-   vThreadIDInGroupFlattened (單一元件) 

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





