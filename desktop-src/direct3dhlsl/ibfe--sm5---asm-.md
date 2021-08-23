---
title: 'ibfe (sm5-asm) '
description: 指定某個數位的位範圍時，請將這些位移至 LSB，並將其符號延伸至範圍的 MSB。
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b04bfcaea154a8a63e9b118da12a8994398357b7c6a022a4589353c6c06eb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949618"
---
# <a name="ibfe-sm5---asm"></a>ibfe (sm5-asm) 

指定某個數位的位範圍時，請將這些位移至 LSB，並將其符號延伸至範圍的 MSB。



| ibfe dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 [位位寬度] 中 \] 。<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在欄位 \] 位移中。<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[在 \] [要移位的值] 中。<br/>                          |



 

## <a name="remarks"></a>備註

LSB 5 位的 src0 會提供位寬度 (0-31) 。

LSB 5 位的 src1 會提供位 (0-31) 的位位移。

下列範例示範如何使用此指令。

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

使用此指令來將帶正負號的整數或旗標解壓縮。

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

 

 





