---
title: 'iadd (sm4-asm) '
description: 整數加法。
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373867"
---
# <a name="iadd-sm4---asm"></a>iadd (sm4-asm) 

整數加法。



| iadd dest \[ . mask \] 、 \[ - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle\] |
|------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要加入至 *src1* 的數位中。<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要加入至 *src0* 的數位中。<br/>           |



 

## <a name="remarks"></a>備註

32位運算元的元件 *src0* 和 *src1*，將正確的32位結果放置在 *dest* 中。 不會對每個元件的32位值執行任何運算或借用，因此此指令對其運算元的正負號性質而言並不敏感。

在執行作業之前，來源運算元上的選擇性否定修飾詞會採用2的補數。

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

 

 





