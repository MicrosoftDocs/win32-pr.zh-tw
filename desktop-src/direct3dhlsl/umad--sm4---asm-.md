---
title: 'umad (sm4-asm) '
description: 不帶正負號的整數相乘和 add。
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6a6c649a61c78eebee249b9fec5c032a07a8a0761a3d23d6e45da573be122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405988"
---
# <a name="umad-sm4---asm"></a>umad (sm4-asm) 

不帶正負號的整數相乘和 add。



| umad dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要乘以 *src1* 的值中。<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要乘以 *src1* 的值中。<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[在 \] 要加入至 *src0* 和 *src1* 產品的值中。<br/> |



 

## <a name="remarks"></a>備註

32位運算元的元件取向 [umul](umul--sm4---asm-.md) *src0* 和 *src1* 未簽署，並保留結果的低32位（每個元件）。 此指令接著會執行 *src2 收取* 的 [iadd](iadd--sm4---asm-.md) ，) 結果產生每個元件的正確低32位 (。 32位的結果會放在 *dest* 中。

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

 

 





