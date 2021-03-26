---
title: 'usubb (sm5-asm) '
description: 不帶正負號的整數減去借用。
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373715"
---
# <a name="usubb-sm5---asm"></a>usubb (sm5-asm) 

不帶正負號的整數減去借用。



| usubb dest0 \[ mask \] 、dest1 \[ mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| 項目                                                               | 描述                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[中的 \] 包含指令的 LSAB 結果。<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[在 \] 指定是否產生借用的對應 *dest0* 元件中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[\]要從中減去的值。<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[\]從 *src0* 減去的數量。<br/>                                             |



 

## <a name="remarks"></a>備註

此指令會執行從 *src0* *src1* 的元件的不帶正負號減去32位運算元，將32位結果的 LSB 部分放在 *dest0* 中。

如果產生借用， *dest1* 中對應的元件會以1寫入，否則為0。

如果不需要借用， *dest1* 可以是 Null。

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

 

 





