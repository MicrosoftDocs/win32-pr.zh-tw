---
title: 'imul (sm4-asm) '
description: 帶正負號的整數相乘。
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87eabcc07dc5c6a662494c71a26c5f60e5fa1053265e3740ad3605ed685771a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986488"
---
# <a name="imul-sm4---asm"></a>imul (sm4-asm) 

帶正負號的整數相乘。



| imul destHI \[ mask \] 、destLO \[ mask \] 、 \[ - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle\] |
|-------------------------------------------------------------------------------------|



 



| 項目                                                                                           | 描述                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[在 \] 結果的高32位位址中。<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[在 \] 結果的低32位位址中。<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[在 \] 要乘以 *src1* 的值中。<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[在 \] 要乘以 *src0* 的值中。<br/>             |



 

## <a name="remarks"></a>備註

32位運算元的元件取向乘以 *src0* 和 *src1* (兩者皆已簽署) ，會產生每個元件的正確完整64位 () 結果。 每個元件) 的低32位 (放在 *destLO* 中。 每個元件) 的高32位 (放在 *destHI* 中。

如果不需要64位結果的高或低32位，則可以將 *destHI* 或 *DESTLO* 指定為 Null，而不是指定暫存器。

在執行算數運算之前，來源運算元上的選擇性否定修飾詞會採用2的補數。

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

 

 





