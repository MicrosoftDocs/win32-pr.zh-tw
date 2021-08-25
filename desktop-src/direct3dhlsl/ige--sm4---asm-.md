---
title: 'ige (sm4-asm) '
description: 以元件為依據的向量整數大於或等於比較。
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15de044678d61adea52607166c622e6fb5dc20211499de4c11066e6688216910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982418"
---
# <a name="ige-sm4---asm"></a>ige (sm4-asm) 

以元件為依據的向量整數大於或等於比較。



| ige dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|-------------------------------------------------------|



 



| 項目                                                            | 描述                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要與 *src1* 比較的元件中。<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要與 *src0* 比較的元件中。<br/> |



 

## <a name="remarks"></a>備註

針對每個元件執行整數比較 (*src0*  >=  *src1*) ，然後將結果寫入至 *目的地*。

如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。 否則會傳回0x0000000。

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

 

 





