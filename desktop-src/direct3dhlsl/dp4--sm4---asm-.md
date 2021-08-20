---
title: 'dp4 (sm4-asm) '
description: 4維向量點-元件 rgba、POS swizzle 的乘積。
ms.assetid: A41EC054-0060-49CA-90FB-A096E63DD27D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 742bf3c736d6769a70bf9dd792e453cc5977e9eb494206b5c110d10b01b60350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726668"
---
# <a name="dp4-sm4---asm"></a>dp4 (sm4-asm) 

4維向量點-元件 rgba、POS swizzle 的乘積。



| dp4 \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle \] ， |
|---------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。 <br/> *目的地*  = *src0. r* \* *src1. r*  +  *src0.* g \* *src1. g*  +  *src0* \*  +   \*  . b src1. a src0. a src1. a<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 作業的元件中。<br/>                                                                                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 作業的元件中。<br/>                                                                                                          |



 

## <a name="remarks"></a>備註

純量結果已複寫至寫入遮罩中的元件。

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

 

 





