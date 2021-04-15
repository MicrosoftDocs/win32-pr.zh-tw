---
description: 效果函式是以 HLSL 撰寫，並且使用下列語法來宣告。
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: " (Direct3D 10) 的效果函數語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468185"
---
# <a name="effect-function-syntax-direct3d-10"></a> (Direct3D 10) 的效果函數語法

效果函式是以 HLSL 撰寫，並且使用下列語法來宣告。

## <a name="syntax"></a>Syntax

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] ) 

{

<dl> \[ *陳述式* \]
</dl>

};



| Name         | 描述                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | 任何 [HLSL 類型](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | 能唯一識別著色器函式名稱的 ASCII 字串。                                                                                                                                                                                            |
| ArgumentList | 以逗號分隔的一或多個引數 (請參閱 [ (DIRECTX HLSL) ](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)) 的函式引數。                                                                                                                             |
| 陳述式   | 一或多個語句 (查看組成函式主體 [ (DIRECTX HLSL) ](../direct3dhlsl/dx-graphics-hlsl-statements.md)) 的語句。 如果定義的函式沒有主體，則會被視為原型;和必須在使用之前以主體重新定義。 |



 

效果函式可能是著色器，也可能只是著色器所呼叫的函式。 函式是由其名稱、其參數的類型和目標平臺來唯一識別;因此，可以多載函式。 任何有效的 HLSL 函式都應該符合此格式;如需 HLSL 函式的語法詳細清單，請參閱) 的函式 [ (DIRECTX HLSL ](../direct3dhlsl/dx-graphics-hlsl-functions.md)。

## <a name="example"></a>範例

[BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)會使用圖元著色器和頂點著色器。 圖元著色器函式稱為 RenderScenePS，如下所示。


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

[效果格式](d3d10-effect-format.md)
</dt> </dl>

 

 
