---
title: 'ishr (sm5-asm) '
description: '算術右移 (sign 擴充) 。 |ishr (sm5-asm) '
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992091"
---
# <a name="ishr-sm5---asm"></a>ishr (sm5-asm) 

算術右移 (sign 擴充) 。



| ishl dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|--------------------------------------------------------|



 



| 項目                                                            | 描述                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[中的 \] 包含 shift 的結果。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]要移位的位數。<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要移位的32位值中。<br/>        |



 

## <a name="remarks"></a>備註

此指令會在 *src0* 中執行每個32位值的元件的算術移位，由 LSB 5 位所提供的不帶正負號的整數位計數 (0-31 範圍) 在 *src1* 中，複寫位31的值。 每個元件的32位結果都會放置在 *dest* 中。

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

 

 





