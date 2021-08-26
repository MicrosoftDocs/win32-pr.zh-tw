---
title: '視窗 (sm4-asm) '
description: 元件的向量整數不等於比較。
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0170dd8b5cfd6284356699bc065e5581a601f8868bfd6c0db99a6a53f9bcfd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023848"
---
# <a name="ine-sm4---asm"></a>視窗 (sm4-asm) 

元件的向量整數不等於比較。



| 視窗 dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|-------------------------------------------------------|



 



| 項目                                                            | 描述                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] 包含要與 *src1* 比較的值。<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] 包含要與 *src0* 比較的值。<br/>    |



 

## <a name="remarks"></a>備註

針對每個元件執行整數比較 (*src0* ！ = *src1*) ，並將結果寫入至 *目的地*。

如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。 否則會傳回0x0000000

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

 

 





