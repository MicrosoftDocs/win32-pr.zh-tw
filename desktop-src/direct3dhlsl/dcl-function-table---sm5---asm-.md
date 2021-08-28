---
title: 'dcl_function_table (sm5-asm) '
description: 宣告函數資料表。
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549653ee7316a664b628d5cdc692c091bdf042ad24e89b983c0fd3aac8a67ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490888"
---
# <a name="dcl_function_table-sm5---asm"></a>dcl \_ 函數 \_ 表 (sm5-asm) 

宣告函數資料表。



| dcl \_ 函數 \_ 表格 ft \# = {fb \# ，fb \# ，...} |
|-----------------------------------------------|



 



| 項目                                                      | 描述                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*英尺*<br/> | \[在 \] 函數資料表專案中。<br/> |



 

## <a name="remarks"></a>備註

此函式會將函式資料表宣告為一組稍早宣告的函式主體。

這就像是 c + + vtable，但介面的每個呼叫位置都有一個專案，而不是每個方法的專案。

函數資料表中可列出的函式主體數目沒有限制。

在一或多個函式資料表中，將指定的函式主體 \# 視為不常被參考，作為共用通用程式碼的一種方式，這是有效的。

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

 

 





