---
title: '效果狀態群組 (Direct3D 11) '
description: 效果狀態是運算式形式的名稱值配對。
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- '效果、狀態群組 (Direct3D 11) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933266"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="73fe4-104">效果狀態群組 (Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="73fe4-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="73fe4-105">效果狀態是運算式形式的名稱值配對。</span><span class="sxs-lookup"><span data-stu-id="73fe4-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="73fe4-106">Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="73fe4-107">深度和樣板狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="73fe4-108">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="73fe4-109">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="73fe4-110">效果物件狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="73fe4-111">定義和使用狀態物件</span><span class="sxs-lookup"><span data-stu-id="73fe4-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="73fe4-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="73fe4-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="73fe4-113">混色狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-113">Blend State</span></span>



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="73fe4-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="73fe4-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="73fe4-115">[ **D3D11 \_ BLEND \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="73fe4-115">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="73fe4-116">深度和樣板狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-116">Depth and Stencil State</span></span>



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="73fe4-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="73fe4-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="73fe4-118">[ **D3D11 深度樣板 \_ \_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="73fe4-118">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="73fe4-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="73fe4-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="73fe4-120">[ **D3D11 \_ 深度 \_ STENCILOP \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="73fe4-120">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="73fe4-121">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-121">Rasterizer State</span></span>



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="73fe4-122">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="73fe4-122">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="73fe4-123">**D3D11 \_ 填滿 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="73fe4-123">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="73fe4-124">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="73fe4-124">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="73fe4-125">**D3D11 的 \_ 挑選 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="73fe4-125">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="73fe4-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="73fe4-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="73fe4-127">D3D11 轉譯器 [ **\_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="73fe4-127">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="73fe4-128">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-128">Sampler State</span></span>



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="73fe4-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc 邊框 MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="73fe4-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="73fe4-130">[ **D3D11 取樣器 \_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="73fe4-130">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="73fe4-131">如需範例，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) 。</span><span class="sxs-lookup"><span data-stu-id="73fe4-131">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="73fe4-132">效果物件狀態</span><span class="sxs-lookup"><span data-stu-id="73fe4-132">Effect Object State</span></span>



| <span data-ttu-id="73fe4-133">此效果物件</span><span class="sxs-lookup"><span data-stu-id="73fe4-133">This Effect Object</span></span>                          | <span data-ttu-id="73fe4-134">對應至</span><span class="sxs-lookup"><span data-stu-id="73fe4-134">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="73fe4-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="73fe4-135">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="73fe4-136">轉譯器 [狀態](#rasterizer-state) 狀態物件。</span><span class="sxs-lookup"><span data-stu-id="73fe4-136">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="73fe4-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="73fe4-137">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="73fe4-138">[深度和樣板狀態](#depth-and-stencil-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="73fe4-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="73fe4-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="73fe4-139">BLENDSTATE</span></span>                                  | <span data-ttu-id="73fe4-140">[Blend 狀態](#blend-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="73fe4-140">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="73fe4-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="73fe4-141">VERTEXSHADER</span></span>                                | <span data-ttu-id="73fe4-142">已編譯的頂點著色器物件。</span><span class="sxs-lookup"><span data-stu-id="73fe4-142">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="73fe4-143">無效</span><span class="sxs-lookup"><span data-stu-id="73fe4-143">PIXELSHADER</span></span>                                 | <span data-ttu-id="73fe4-144">編譯的圖元著色器物件。</span><span class="sxs-lookup"><span data-stu-id="73fe4-144">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="73fe4-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="73fe4-145">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="73fe4-146">已編譯的幾何著色器物件。</span><span class="sxs-lookup"><span data-stu-id="73fe4-146">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="73fe4-147">DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="73fe4-147">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="73fe4-148">[**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="73fe4-148">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="73fe4-149">定義和使用狀態物件</span><span class="sxs-lookup"><span data-stu-id="73fe4-149">Defining and using state objects</span></span>

<span data-ttu-id="73fe4-150">系統會以下列格式在 FX 檔案中宣告狀態物件。</span><span class="sxs-lookup"><span data-stu-id="73fe4-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="73fe4-151">StateObjectType 是上面所列的其中一個狀態，而成員名稱則是任何將具有非預設值的成員名稱。</span><span class="sxs-lookup"><span data-stu-id="73fe4-151">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="73fe4-152">例如，若要設定 AlphaToCoverageEnable，並將 BlendEnable \[ 0 \] 設為 **FALSE** 的 blend 狀態物件，則會使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="73fe4-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="73fe4-153">使用 [ (Direct3D 11) 的效果技巧語法 ](d3d11-effect-technique-syntax.md)中所述的其中一個 SetStateGroup 函式，將狀態物件套用至技術傳遞。</span><span class="sxs-lookup"><span data-stu-id="73fe4-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="73fe4-154">例如，若要套用上面所述的 BlendState 物件，則會使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="73fe4-154">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="73fe4-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="73fe4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73fe4-156">效果技巧語法</span><span class="sxs-lookup"><span data-stu-id="73fe4-156">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="73fe4-157"> (Direct3D 11) 的效果格式 </span><span class="sxs-lookup"><span data-stu-id="73fe4-157">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 