---
title: 'imad (sm4-asm) '
description: 帶正負號的整數乘以並加入。
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990715"
---
# <a name="imad-sm4---asm"></a>imad (sm4-asm) 

帶正負號的整數乘以並加入。



| imad dest \[ . mask \] 、 \[ - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle \] 、 \[ - \] src2 收取 \[ . swizzle |
|---------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]要乘以 *src1* 的值。<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[\]要乘以 *src0* 的值。<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[\]要加入 *src0* 和 *src1* 產品的值。<br/> |



 

## <a name="remarks"></a>備註

32位運算元的元件取向 [imul](imul--sm4---asm-.md) *src0* 和 *src1* (簽署的) 、保留低32位 (每個元件) 結果，接著 [iadd](iadd--sm4---asm-.md) *src2 收取*，產生每個元件的正確低32位 () 結果。 32位的結果會放在 *dest* 中。

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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





