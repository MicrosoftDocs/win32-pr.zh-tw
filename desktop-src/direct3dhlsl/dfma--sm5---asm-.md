---
title: 'dfma (sm5-asm) '
description: 執行融合乘積的新增。
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84952ed594ba8541223df072fa59550aded581e5517dee3d6f4168b7661a87aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068388"
---
# <a name="dfma-sm5---asm"></a>dfma (sm5-asm) 

執行融合乘積的新增。



| dfma \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src2 收取 \[ \_ abs \] \[ . swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。 結果值必須正確到 0.5 ULP。<br/> *目的地*  = *src0* \**src1*  + *src2 收取*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要與 *src1* 相乘的元件中。<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要與 *src0* 相乘的元件中。<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[在 \] 要新增至 *src0* \* *src1* 的元件中。<br/>                                                                                               |



 

## <a name="remarks"></a>備註

使用此指令的著色器會標記為著色器旗標，除非符合下列所有條件，否則會導致無法系結。

-   系統支援 DirectX 11.1。
-   系統包含 WDDM 1.2 驅動程式。
-   驅動程式會透過 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項，向此指令報告支援。ExtendedDoublesShaderInstructions** 設定為 **TRUE**。

此指示適用于下列著色器階段：



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

 

 





