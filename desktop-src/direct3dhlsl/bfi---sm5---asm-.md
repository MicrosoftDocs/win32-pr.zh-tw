---
title: 'bfi (sm5-asm) '
description: 從數位的 LSB 中指定位範圍，並將該位數的數位放在其他數位的任何位移。
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022832"
---
# <a name="bfi-sm5---asm"></a>bfi (sm5-asm) 

從數位的 LSB 中指定位範圍，並將該位數的數位放在其他數位的任何位移。



| bfi dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle \] 、src3 \[ . swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 結果的位址中。<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]要從 *src2 收取* 取得的位位寬度。<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[用 \] 來取代 *src3* 中之位的位位位移。<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[\]從取得位數的數位。 <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[， \] 包含要取代的位數。<br/>              |



 

## <a name="remarks"></a>備註

LSB 5 位的 *src0* 會提供位寬度 (0-31) 要從 *src2 收取* 中取得。

*Src1* 的 LSB 5 位會提供位位移 (0-31) 來開始取代從 *src3* 讀取的位數。

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

此指令用於封裝整數或旗標。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





