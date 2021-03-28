---
title: 'dcl_thread_group (sm5-asm) '
description: 宣告執行緒群組大小。
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022846"
---
# <a name="dcl_thread_group-sm5---asm"></a>dcl \_ 執行緒 \_ 群組 (sm5-asm) 

宣告執行緒群組大小。



| dcl \_ 執行緒 \_ 群組 x、y、z |
|----------------------------|



 



| 項目                                                   | 描述                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] usigned 32 位整數中。 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[在 \] usigned 32 位整數中。 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*Z*<br/> | \[在 \] usigned 32 位整數中。 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>備註

x \* y \* z <= 1024

此執行緒群組宣告必須在計算著色器中出現一次。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





