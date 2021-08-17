---
title: 'dcl_function_body (sm5-asm) '
description: 宣告函數主體。
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339e7f5d7edb91f4f3405b328286a9ae32a8108efdaafaba1f212870be7ff8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727232"
---
# <a name="dcl_function_body-sm5---asm"></a>\_ \_ (的 dcl 函數主體) sm5-asm

宣告函數主體。



| dcl \_ 函數 \_ 主體 fb\# |
|--------------------------|



 



| 項目                                                          | 描述                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*Fb\#*<br/> | \[在將出現函式 \] 之位置的標籤中。<br/> |



 

## <a name="remarks"></a>備註

此指令宣告了唯一的函式主體，其程式碼稍後會在標籤為 fb 的程式中顯示 \# 。

函數主體用於函數表聲明中。 如需詳細資訊，請參閱 [dcl \_ 函數 \_ 表](dcl-function-table---sm5---asm-.md)。

在輪廓著色器和網域著色器中，其中有多個階段 (控制點階段、分支階段和聯結階段) ，所有的函式主體 (標籤 fb \#) 會出現在所有階段之後，而不是依階段分組。

有多少個函數主體可以存在。

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

 

 





