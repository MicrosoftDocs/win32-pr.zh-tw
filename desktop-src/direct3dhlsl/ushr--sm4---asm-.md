---
title: 'ushr (sm4-asm) '
description: '右移。 |ushr (sm4-asm) '
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55343f9c9b4db4fff4b0df7ab4e2a567f25f0eb43e93486fe9c41b89cf68454
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787818"
---
# <a name="ushr-sm4---asm"></a>ushr (sm4-asm) 

右移。



| ushr dest \[ . mask \] ，src0 \[ . swizzle \] ，src1. select \_ component |
|--------------------------------------------------------------|



 



| 項目                                                            | 描述                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要移位的元件中。<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] [要移位的數量] *src0* 中。<br/>                 |



 

## <a name="remarks"></a>備註

此指令會在 *src0* 中執行每個32位值的元件轉移，由 LSB 5 位所提供的不帶正負號整數位計數 (0-31 範圍) 在 *src1 中。選取 \_ 元件*，插入0。 每個元件的32位結果都會放置在 *dest* 中。 計數是套用至所有元件的純量值。

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

 

 





