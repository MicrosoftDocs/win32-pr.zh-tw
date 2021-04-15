---
title: 'ishl (sm4-asm) '
description: '左移。 |ishl (sm4-asm) '
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992014"
---
# <a name="ishl-sm4---asm"></a>ishl (sm4-asm) 

左移。



| 目的地 \[ . mask \] 、src0 \[ . swizzle \] 、src1. select \_ component |
|---------------------------------------------------------|



 



| 項目                                                            | 描述                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] 包含要移位的值。<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] 包含移位量。<br/>                  |



 

## <a name="remarks"></a>備註

此指令會在 src0 中，以 LSB 5) 0-31 (位所提供的不帶正負號的整數位元數目（在 *src1. select \_ 元件* 中，插入0），在中執行每個32位值的元件轉移。 每個元件的32位結果都會放置在 *dest* 中。 計數是套用至所有元件的純量值。

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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





