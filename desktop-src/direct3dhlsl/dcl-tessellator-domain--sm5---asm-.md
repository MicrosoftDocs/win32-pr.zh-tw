---
title: 'dcl_tessellator_domain (sm5-asm) '
description: 在 [輪廓著色器宣告] 區段和網域著色器中宣告鑲嵌網域。
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a027e9fab091cf31e8577266015e974ec78033fe19a9542f0aa3c6ca4651db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986708"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>dcl \_ 鑲嵌 \_ 網域 (sm5-asm) 

在 [輪廓著色器宣告] 區段和網域著色器中宣告鑲嵌網域。



| dcl \_ 鑲嵌 \_ 網域 {網域 \_ 等值線 \| 網域 \_ 三| 網域 \_ 四個 |
|---------------------------------------------------------------------------|



 



| 項目                                                                                                                                                                                | 描述                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*網域 \_ 等值線 \| 網域 \_ 三個 \| 網域 \_ 四個*<br/> | \[在 \] 網域中。<br/> |



 

## <a name="remarks"></a>備註

如果輪廓著色器和網域著色器提供不相符的網域或任何其他衝突的 decalarations，則行為是未定義的。

此指示適用于下列著色器階段：



| 頂點 | 船體                 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|----------------------|--------|----------|-------|---------|
|        | 宣告區段 | X      |          |       |         |



 

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

 

 





