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
# <a name="shader-type"></a><span data-ttu-id="96347-104">著色器類型</span><span class="sxs-lookup"><span data-stu-id="96347-104">Shader Type</span></span>

<span data-ttu-id="96347-105">將效果中的著色器變數宣告為從 Direct3D 9 變更為 Direct3D 10 的語法。</span><span class="sxs-lookup"><span data-stu-id="96347-105">The syntax for declaring a shader variable in an effect changed from Direct3D 9 to Direct3D 10.</span></span>

## <a name="shader-type-for-direct3d-10"></a><span data-ttu-id="96347-106">Direct3D 10 的著色器類型</span><span class="sxs-lookup"><span data-stu-id="96347-106">Shader Type for Direct3D 10</span></span>

<span data-ttu-id="96347-107">使用著色器類型語法，在 Direct3D 10) 的效果通過 (中宣告著色器變數：</span><span class="sxs-lookup"><span data-stu-id="96347-107">Declare a shader variable within an effect pass (in Direct3D 10) using the shader type syntax:</span></span>



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96347-108">**SetPixelShader** Compile ( **ShaderTarget、ShaderFunction** ) ; **SetGeometryShader** Compile ( **ShaderTarget、ShaderFunction** ) ; **SetVertexShader** Compile ( **ShaderTarget、ShaderFunction** ) ;</span><span class="sxs-lookup"><span data-stu-id="96347-108">**SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** );</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="96347-109">參數</span><span class="sxs-lookup"><span data-stu-id="96347-109">Parameters</span></span>



| <span data-ttu-id="96347-110">項目</span><span class="sxs-lookup"><span data-stu-id="96347-110">Item</span></span>                                                                                                                             | <span data-ttu-id="96347-111">描述</span><span class="sxs-lookup"><span data-stu-id="96347-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96347-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span><span class="sxs-lookup"><span data-stu-id="96347-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span></span><br/>         | <span data-ttu-id="96347-113">用來建立著色器物件的 Direct3D API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="96347-113">The Direct3D API call that creates the shader object.</span></span> <span data-ttu-id="96347-114">可以是： **SetPixelShader** 、 **SetGeometryShader** 或 **SetVertexShader**。</span><span class="sxs-lookup"><span data-stu-id="96347-114">Can be either: **SetPixelShader** or **SetGeometryShader** or **SetVertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="96347-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="96347-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>         | <span data-ttu-id="96347-116">要針對編譯的著色器模型。</span><span class="sxs-lookup"><span data-stu-id="96347-116">The shader model to compile against.</span></span> <span data-ttu-id="96347-117">這適用于任何目標，包括所有 Direct3D 9 目標以及 [著色器模型 4](dx-graphics-hlsl-sm4.md) 目標： vs \_ 4 \_ 0、gs \_ 4 \_ 0 和 ps \_ 4 \_ 0。</span><span class="sxs-lookup"><span data-stu-id="96347-117">This is valid for any target including all Direct3D 9 targets plus the [shader model 4](dx-graphics-hlsl-sm4.md) targets: vs\_4\_0, gs\_4\_0, and ps\_4\_0.</span></span><br/>                                                                                                                                                                                                                                          |
| <span data-ttu-id="96347-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="96347-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span></span><br/> | <span data-ttu-id="96347-119">包含著色器進入點函數名稱的 ASCII 字串;這是叫用著色器時開始執行的函式。</span><span class="sxs-lookup"><span data-stu-id="96347-119">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="96347-120"> ( ... ) 表示著色器引數;這些是傳遞給著色器建立 API 的相同引數： [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) 或 [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) 或 [**pssetshade**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader)。</span><span class="sxs-lookup"><span data-stu-id="96347-120">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) or [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) or [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="96347-121">範例</span><span class="sxs-lookup"><span data-stu-id="96347-121">Example</span></span>

<span data-ttu-id="96347-122">以下範例會建立針對特定著色器模型編譯的頂點著色器和圖元著色器物件。</span><span class="sxs-lookup"><span data-stu-id="96347-122">Here is an example that creates a vertex shader and pixel shader object, compiled for a particular shader model.</span></span> <span data-ttu-id="96347-123">在 Direct3D 10 範例中，沒有幾何著色器，因此指標會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="96347-123">In the Direct3D 10 example, there is no geometry shader, so the pointer is set to **NULL**.</span></span>


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



## <a name="shader-type-for-direct3d-9"></a><span data-ttu-id="96347-124">Direct3D 9 的著色器類型</span><span class="sxs-lookup"><span data-stu-id="96347-124">Shader Type for Direct3D 9</span></span>

<span data-ttu-id="96347-125">使用著色器類型語法，在 Direct3D 9) 的效果通過 (中宣告著色器變數：</span><span class="sxs-lookup"><span data-stu-id="96347-125">Declare a shader variable within an effect pass (for Direct3D 9) using the shader type syntax:</span></span>



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96347-126">**無效** = Compile **ShaderTarget ShaderFunction ( ... ) ;VertexShader** = Compile **ShaderTarget ShaderFunction ( ... ) ;**</span><span class="sxs-lookup"><span data-stu-id="96347-126">**PixelShader** = compile **ShaderTarget ShaderFunction(...);VertexShader** = compile **ShaderTarget ShaderFunction(...);**</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="96347-127">參數</span><span class="sxs-lookup"><span data-stu-id="96347-127">Parameters</span></span>



| <span data-ttu-id="96347-128">項目</span><span class="sxs-lookup"><span data-stu-id="96347-128">Item</span></span>                                                                                                                                                 | <span data-ttu-id="96347-129">描述</span><span class="sxs-lookup"><span data-stu-id="96347-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96347-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span><span class="sxs-lookup"><span data-stu-id="96347-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span></span><br/>                                         | <span data-ttu-id="96347-131">著色器變數，代表已編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="96347-131">A shader variable, which represents the compiled shader.</span></span> <span data-ttu-id="96347-132">可以是： **無效** 或 **VertexShader**。</span><span class="sxs-lookup"><span data-stu-id="96347-132">Can be either: **PixelShader** or **VertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="96347-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="96347-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>                             | <span data-ttu-id="96347-134">要針對編譯的 [著色器模型](dx-graphics-hlsl-models.md) ;取決於著色器變數的類型。</span><span class="sxs-lookup"><span data-stu-id="96347-134">The [shader model](dx-graphics-hlsl-models.md) to compile against; depends on the type of shader variable.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="96347-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction ( ... )**</span><span class="sxs-lookup"><span data-stu-id="96347-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span></span><br/> | <span data-ttu-id="96347-136">包含著色器進入點函數名稱的 ASCII 字串;這是叫用著色器時開始執行的函式。</span><span class="sxs-lookup"><span data-stu-id="96347-136">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="96347-137"> ( ... ) 表示著色器引數;這些是傳遞給著色器建立 API 的相同引數： [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) 或 [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)。</span><span class="sxs-lookup"><span data-stu-id="96347-137">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) or [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="96347-138">範例</span><span class="sxs-lookup"><span data-stu-id="96347-138">Example</span></span>

<span data-ttu-id="96347-139">以下是針對特定著色器模型編譯之頂點著色器和圖元著色器物件的範例。</span><span class="sxs-lookup"><span data-stu-id="96347-139">Here is an example of a vertex shader and pixel shader object, compiled for a particular shader model.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="96347-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96347-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96347-141"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="96347-141">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

