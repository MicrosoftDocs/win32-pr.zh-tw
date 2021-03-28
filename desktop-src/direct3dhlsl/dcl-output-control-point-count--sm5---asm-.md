---
title: 'dcl_output_control_point_count (sm5-asm) '
description: 宣告輪廓著色器輸出控制點計數。
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022858"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>dcl \_ 輸出 \_ 控制 \_ 點 \_ 計數 (sm5-asm) 

宣告輪廓著色器輸出控制點計數。



| dcl \_ 輸出 \_ 控制 \_ 點 \_ 計數 N |
|--------------------------------------|



 



| 項目                                                   | 描述                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N-1*<br/> | \[\]從0到32的整數值，指定輸出控制點計數。<br/> |



 

## <a name="remarks"></a>備註

如果不需要，輪廓著色器可以輸出0個控制點。

此指示適用于下列著色器階段：



| 頂點 | 船體                 | 網域 | 幾何 | 像素 | 計算 |
|--------|----------------------|--------|----------|-------|---------|
|        | 宣告區段 |        |          |       |         |



 

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

 

 





