---
title: 'ishr (sm4-asm) '
description: '算術右移 (sign 擴充) 。 |ishr (sm4-asm) '
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2ec191320561b05ba736b7da5630fb50a610e739d0e74f9def3eaa10bb4e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511133"
---
# <a name="ishr-sm4---asm"></a>ishr (sm4-asm) 

算術右移 (sign 擴充) 。



| ishr dest \[ . mask \] ，src0 \[ . swizzle \] ，src1. select \_ component |
|--------------------------------------------------------------|



 



| 項目                                                            | 描述                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[中的 \] 包含運算的結果。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] 包含要移位的值。<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] 包含移位量。<br/>            |



 

## <a name="remarks"></a>備註

此指令會在 *src0* 中執行每個32位值的元件的算術移位，由 LSB 5 位所提供的不帶正負號整數位移， (0-31 範圍) 在 *src1 中。選取 [ \_ 元件*]，複寫位31的值。 每個元件的32位結果都會放置在 *dest* 中。 計數是套用至所有元件的純量值。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





