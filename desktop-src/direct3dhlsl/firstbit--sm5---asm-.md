---
title: 'firstbit (sm5-asm) '
description: 從 LSB 或 MSB 尋找數位中設定的第一個位。
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ea47c8e0674db5dc0349e5d6a8a041fa7d3623e6578eee542edeb1749577d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511942"
---
# <a name="firstbit-sm5---asm"></a>firstbit (sm5-asm) 

從 LSB 或 MSB 尋找數位中設定的第一個位。



| firstbit { \_ 嗨|\_高低|\_shi} dest \[ \] 、src0 \[ . swizzle\] |
|-------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] *src0* 中第一個位集合的整數位置，從 LSB for FIRSTBIT \_ lo 或 MSB for firstbit hi 開始 \_ 。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 輸入整數中。<br/>                                                                                                  |



 

## <a name="remarks"></a>備註

這項作業會傳回32位輸入中第一位設定的整數位置，從 LSB for firstbit \_ lo 或 MSB for firstbit hi 開始 \_ 。 例如， \_ 在0x00000001 上的 firstbit lo 會傳回0。 \_0x10000000 上的 firstbit hi 會傳回3。

\_如果數位為負數，則 firstbit 已簽署) 的 shi (s 會傳回 MSB 中的第一個 0; 否則會傳回 MSB 中的前1個。

如果找不到相符項，則指令的所有變體會在32位暫存器中傳回 ~ 0 (0xffffffff) 。

您可以使用此指令快速列舉位中的設定位，或找出數位中最大的2乘冪。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>最低著色器模型

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

 

 





