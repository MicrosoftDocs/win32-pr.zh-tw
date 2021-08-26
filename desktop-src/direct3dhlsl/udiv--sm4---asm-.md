---
title: 'udiv (sm4-asm) '
description: 不帶正負號的整數除。
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b1320d0518034129efe2222a42aa2694df0422db524da0714377cb43a2b9a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948978"
---
# <a name="udiv-sm4---asm"></a>udiv (sm4-asm) 

不帶正負號的整數除。



| udiv destQUOT \[ mask \] 、destREM \[ mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|------------------------------------------------------------------------------|



 



| 項目                                                                                                   | 描述                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[在 \] 產生的商位址中。<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[在 \] 結果餘數的位址中。<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[在 \] 要除以 *src1* 的元件中。<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[在 \] [我們元件] 中，以分割 *src0*。<br/> |



 

## <a name="remarks"></a>備註

此指令會執行由32位運算元 *src1* 所 *src0* 之32位運算元的元件的不帶正負號分隔。 相除的結果是放置在 *destQUOT* 中的32位商數，而32位餘數放置於 *destREM* 中。

「零除」會針對商和餘數傳回0xffffffff。

如果不需要商或餘數，您可以將 *destQUOT* 或 *DESTREM* 指定為 Null，而不是指定註冊。

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

 

 





