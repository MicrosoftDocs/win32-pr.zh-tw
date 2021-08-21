---
title: 'dmovc (sm5-asm) '
description: '以元件為條件的移動。 |dmovc (sm5-asm) '
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0ed15d81a91d8a93ce99eda3fa17b91900e0045301f1c5b5d1f56e4448954a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792379"
---
# <a name="dmovc-sm5---asm"></a>dmovc (sm5-asm) 

以元件為條件的移動。



| dmovc \[ \_ sat \] dest \[ . mask \] 、src0 \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src2 收取 \[ \_ abs \] \[ . swizzle \] 、 |
|-----------------------------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 移動目的地。<br/> 如果是 *src0*，則 *dest*  =  *src1* else *dest*  =  *src2 收取*。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[用 \] 來測試條件的元件。<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 條件為 true 時要移動的元件中。<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[\]如果條件為 false，則在要移動的元件中。<br/>                                      |



 

## <a name="remarks"></a>備註

下列範例示範如何使用此指令。

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

適用于 dest 的有效遮罩是 xy、. zw、. xyzw。

適用于 *src0* 的有效 swizzles 為任何。 Swizzle 後的前兩個元件會用來識別 2 32 位的條件值。

包含雙精度浮點數的 *src1* 和 *src2 收取* 的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。 是 xy、. zw 和. xyzw。

下列 *src* 對應為 swizzle 後：

-   *dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。
-   *src0* 是跨 x 和 y 的32位/元件 vec2 (zw 忽略) 。
-   *src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。
-   *src2 收取* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。

*Src1* 和 *src2 收取* 上的修飾詞（除了 swizzle 以外）會假設資料是雙精度浮點數。 缺少修飾詞會移動資料，而不會改變位。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 否        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





