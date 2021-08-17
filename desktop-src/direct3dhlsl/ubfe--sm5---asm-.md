---
title: 'ubfe (sm5-asm) '
description: 指定某個數位的位範圍時，請將這些位移至 LSB，並將其餘的位設定為0。
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3149173bf495957bb38800234e4d853d0e32797254eecfdb3e5b77faf4498ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722159"
---
# <a name="ubfe-sm5---asm"></a>ubfe (sm5-asm) 

指定某個數位的位範圍時，請將這些位移至 LSB，並將其餘的位設定為0。



| ubfe dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[中的 \] 包含指令的結果。<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] LSB 5 位中， (0-31) 提供位寬。<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] *SRC1* 的 LSB 5 位中，提供位 (0-31) 的位位移。<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[在 \] 要移位的數位中。<br/>                                         |



 

## <a name="remarks"></a>備註

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

使用此指令來解除封裝不帶正負號的整數或旗標。

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

 

 





