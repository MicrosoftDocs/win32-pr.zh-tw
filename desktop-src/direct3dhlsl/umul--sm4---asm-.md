---
title: 'umul (sm4-asm) '
description: 不帶正負號的整數相乘。
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec63b3a95ffbdf1f71142c9fc508e21e718b44d988b725dad5d73775746871c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721832"
---
# <a name="umul-sm4---asm"></a>umul (sm4-asm) 

不帶正負號的整數相乘。



| umul destHI \[ mask \] 、destLO \[ mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|---------------------------------------------------------------------------|



 



| 項目                                                                                           | 描述                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[在 \] 結果的高32位中，每個元件。<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[在 \] 結果的低32位中，每個元件。<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[用 \] 來乘以 *src1* 的元件。<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[用 \] 來乘以 *src0* 的元件。<br/>    |



 

## <a name="remarks"></a>備註

此指令會針對未簽署的32位運算元 *src0* 和 *src1* 執行元件的乘積，並為每個元件產生正確的完整64位結果。 每個元件的低32位都放在 *destLO* 中。 每個元件的高32位都放在 *destHI* 中。

您可以指定 *destHI* 或 *DESTLO* 做為 Null，而不是在不需要64位結果的高或低32位時指定暫存器。

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

 

 





