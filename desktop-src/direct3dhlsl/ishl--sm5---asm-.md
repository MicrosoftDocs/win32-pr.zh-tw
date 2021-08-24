---
title: ishl (sm5 - asm)
description: '左移。 |ishl (sm5-asm) '
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6908d12824c5aa84e04db38fb2462031bb2ae4a198700f98938456ecbd8619a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854208"
---
# <a name="ishl-sm5---asm"></a>ishl (sm5 - asm)

左移。



| ishl dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|--------------------------------------------------------|



 



| 項目                                                            | 描述                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[中的 \] 包含 shift 的結果。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要移位的32位值中。<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[\]要移位的位數。<br/>        |



 

## <a name="remarks"></a>備註

此指令會在 *src0* 中以 LSB 5) 0-31 (位所提供的不帶正負號整數位計數，在 *src1* 中插入0時，執行以元件為依據的每個32位值的位移。 每個元件的32位結果都會放置在 *dest* 中。

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

 

 





