---
title: 'dcl_input_control_point_count (sm5-asm) '
description: 在 [輪廓著色器宣告] 區段中宣告輪廓著色器輸入控制點計數。
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c5414d5c660cf0bbce2b6219769cd36d4da9bbf3e59d9d130bfce0e0dceea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789878"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>dcl \_ 輸入 \_ 控制 \_ 點 \_ 計數 (sm5-asm) 

在 [輪廓著色器宣告] 區段中宣告輪廓著色器輸入控制點計數。



| dcl \_ 輸入 \_ 控制 \_ 點 \_ 計數 {1 ... 32} |
|-------------------------------------------|



 



| 項目                                                   | 描述                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N-1*<br/> | \[在 \] 輸入控制點計數中。<br/> |



 

## <a name="remarks"></a>備註

至少需要1個輸入控制點;如果不需要，它可以是空的。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

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

 

 





