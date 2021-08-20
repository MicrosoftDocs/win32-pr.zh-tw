---
title: 'itof (sm4-asm) '
description: 帶正負號的整數轉換浮點數。
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f473b5cc9664ee1c9acab88381bc9de6a5b4897fac3899923c6bb20c22bba7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986478"
---
# <a name="itof-sm4---asm"></a>itof (sm4-asm) 

帶正負號的整數轉換浮點數。



| itof dest \[ . mask \] ， \[ - \] src0 \[ . swizzle\] |
|-------------------------------------------|



 



| 項目                                                            | 描述                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[中的 \] 包含運算的結果。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] 包含要轉換的值。<br/>        |



 

## <a name="remarks"></a>備註

此帶正負號的整數到浮點數轉換指令會假設 *src0* 包含帶正負號的32位整數4元組。 在執行指令之後， *dest* 將包含浮點數4元組。

每個元件都會執行轉換。

當整數輸入值的大小太大而無法以浮點數格式表示時，強烈建議您四捨五入到最接近的偶數模式，但並非必要。

在執行算數運算之前，來源運算元的選擇性否定修飾詞會採用2的補數。

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

 

 





