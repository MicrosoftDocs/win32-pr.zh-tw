---
title: 'xor (sm4-asm) '
description: 位 xor。
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a4dae86a4c6ade427b749c2bb72974564b8a4b7a6baae6821edb3c0d63b2164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892408"
---
# <a name="xor-sm4---asm"></a>xor (sm4-asm) 

位 xor。



| xor dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|-------------------------------------------------------|



 



| 項目                                                            | 描述                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 與 *src1* XOR 的元件中。<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 與 *src0* XOR 的元件中。<br/> |



 

## <a name="remarks"></a>備註

此指令會針對 *src0* 和 *src1* 中的每一對32位值，執行每一組的元件的邏輯 XOR。 32位結果會放在 *dest* 中。

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

 

 





