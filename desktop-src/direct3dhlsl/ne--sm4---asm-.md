---
title: 'ne (sm4-asm) '
description: 元件的向量浮點數不相等比較。
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116f6197c33ef3c040d6c02b7aa561e03cdcc694a2878b6f16554c053a8862db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457338"
---
# <a name="ne-sm4---asm"></a>ne (sm4-asm) 

元件的向量浮點數不相等比較。



| ne dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\] |
|----------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] [要與 *src1* 比較的元件] 中。<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] [要與 *src0* 比較的元件] 中。<br/> |



 

## <a name="remarks"></a>備註

此指令會針對每個元件執行 float 比較 (*src0* ！ = *src1*) ，並將結果寫入至 *目的地*。

如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。 否則會傳回0x0000000。

Denorms 會在與原始來源登錄沒有改變之前排清。

+ 0 等於-0。

與 NaN 的比較會傳回 true。

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

 

 





