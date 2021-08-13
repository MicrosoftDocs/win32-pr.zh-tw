---
title: " (Direct3D 11) 的效果函數語法"
description: 效果函式是以 HLSL 撰寫，並使用本節所述的語法來宣告。
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945f7104d44947f37af71ce664dd99ff64362062b1d42af62af2054538bacb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046616"
---
# <a name="effect-function-syntax-direct3d-11"></a> (Direct3D 11) 的效果函數語法

效果函式是以 HLSL 撰寫，並使用本節所述的語法來宣告。

## <a name="syntax"></a>Syntax

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] ) 

{

<dl> \[ *陳述式* \]
</dl>

};



| 名稱         | 描述                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | 任何 [HLSL 類型](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | 能唯一識別著色器函式名稱的 ASCII 字串。                                                                                                                                                                                            |
| ArgumentList | 以逗號分隔的一或多個引數 (請參閱 [ (DIRECTX HLSL) ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)) 的函式引數。                                                                                                                             |
| 陳述式   | 一或多個語句 (查看組成函式主體 [ (DIRECTX HLSL) ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) 的語句。 如果定義的函式沒有主體，則會被視為原型;和必須在使用之前以主體重新定義。 |



 

效果函式可能是著色器，也可能只是著色器所呼叫的函式。 函式是由其名稱、其參數的類型和目標平臺來唯一識別;因此，可以多載函式。 任何有效的 HLSL 函式都應該符合此格式;如需 HLSL 函式的語法詳細清單，請參閱) 的函式 [ (DIRECTX HLSL ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions)。

## <a name="example"></a>範例

以下是圖元著色器函式的範例。


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](d3d11-effect-format.md)
</dt> </dl>

 

 