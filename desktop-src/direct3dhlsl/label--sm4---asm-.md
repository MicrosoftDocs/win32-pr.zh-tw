---
title: '標籤 (sm4-asm) '
description: 指出副程式的開頭。
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679144"
---
# <a name="label-sm4---asm"></a>標籤 (sm4-asm) 

指出副程式的開頭。



| 標籤 l\# |
|-----------|



 



| 項目                                                       | 描述                         |
|------------------------------------------------------------|-------------------------------------|
| <span id="l_"></span><span id="L_"></span>*我\#*<br/> | \[在 \] 標籤編號中。<br/> |



 

## <a name="remarks"></a>備註

**標籤** 只能出現在未在任何流程式控制制語句中嵌套之 [**ret**](ret--sm4---asm-.md)指令的正上方。

程式中第一個 **標籤** 前面的程式碼是主要程式。 所有副程式都會出現在程式的結尾，並以 **label** 語句表示。

下列範例示範如何使用此指令。

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

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

 

 





