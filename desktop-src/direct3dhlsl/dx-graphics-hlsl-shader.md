---
title: 著色器類型
description: 將效果中的著色器變數宣告為從 Direct3D 9 變更為 Direct3D 10 的語法。
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- 著色器類型 HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971768"
---
# <a name="shader-type"></a>著色器類型

將效果中的著色器變數宣告為從 Direct3D 9 變更為 Direct3D 10 的語法。

## <a name="shader-type-for-direct3d-10"></a>Direct3D 10 的著色器類型

使用著色器類型語法，在 Direct3D 10) 的效果通過 (中宣告著色器變數：



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SetPixelShader** Compile ( **ShaderTarget、ShaderFunction** ) ; **SetGeometryShader** Compile ( **ShaderTarget、ShaderFunction** ) ; **SetVertexShader** Compile ( **ShaderTarget、ShaderFunction** ) ; |



 

### <a name="parameters"></a>參數



| 項目                                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**<br/>         | 用來建立著色器物件的 Direct3D API 呼叫。 可以是： **SetPixelShader** 、 **SetGeometryShader** 或 **SetVertexShader**。<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>         | 要針對編譯的著色器模型。 這適用于任何目標，包括所有 Direct3D 9 目標以及 [著色器模型 4](dx-graphics-hlsl-sm4.md) 目標： vs \_ 4 \_ 0、gs \_ 4 \_ 0 和 ps \_ 4 \_ 0。<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**<br/> | 包含著色器進入點函數名稱的 ASCII 字串;這是叫用著色器時開始執行的函式。  ( ... ) 表示著色器引數;這些是傳遞給著色器建立 API 的相同引數： [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) 或 [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) 或 [**pssetshade**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader)。<br/> |



 

### <a name="example"></a>範例

以下範例會建立針對特定著色器模型編譯的頂點著色器和圖元著色器物件。 在 Direct3D 10 範例中，沒有幾何著色器，因此指標會設定為 **Null**。


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a>Direct3D 9 的著色器類型

使用著色器類型語法，在 Direct3D 9) 的效果通過 (中宣告著色器變數：



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **無效** = Compile **ShaderTarget ShaderFunction ( ... ) ;VertexShader** = Compile **ShaderTarget ShaderFunction ( ... ) ;** |



 

### <a name="parameters"></a>參數



| 項目                                                                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**<br/>                                         | 著色器變數，代表已編譯的著色器。 可以是： **無效** 或 **VertexShader**。<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>                             | 要針對編譯的 [著色器模型](dx-graphics-hlsl-models.md) ;取決於著色器變數的類型。<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction ( ... )**<br/> | 包含著色器進入點函數名稱的 ASCII 字串;這是叫用著色器時開始執行的函式。  ( ... ) 表示著色器引數;這些是傳遞給著色器建立 API 的相同引數： [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) 或 [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)。<br/> |



 

### <a name="example"></a>範例

以下是針對特定著色器模型編譯之頂點著色器和圖元著色器物件的範例。


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

