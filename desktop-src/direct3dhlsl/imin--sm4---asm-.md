---
title: 'imin (sm4-asm) '
description: 最小元件的整數。
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373858"
---
# <a name="imin-sm4---asm"></a>imin (sm4-asm) 

最小元件的整數。



| imin dest \[ . mask \] 、 \[  - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle \] 、 |
|--------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。<br/> *目的地*  = *src0*  < *src1* 嗎？ *src0* ： *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] [要與 *src1* 比較的值] 中。<br/>                                                       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] [要與 *src0* 比較的值] 中。<br/>                                                       |



 

## <a name="remarks"></a>備註

在執行作業之前，來源運算元上的選擇性否定修飾詞會採用2的補數。

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

 

 





