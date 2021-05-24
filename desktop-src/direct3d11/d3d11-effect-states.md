---
title: '效果狀態群組 (Direct3D 11) '
description: 效果狀態是運算式形式的名稱值配對。
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- '效果、狀態群組 (Direct3D 11) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335332"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="2032d-104">效果狀態群組 (Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="2032d-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="2032d-105">效果狀態是運算式形式的名稱值配對。</span><span class="sxs-lookup"><span data-stu-id="2032d-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="2032d-106">Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="2032d-107">深度和樣板狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="2032d-108">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="2032d-109">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="2032d-110">效果物件狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="2032d-111">定義和使用狀態物件</span><span class="sxs-lookup"><span data-stu-id="2032d-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="2032d-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2032d-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="2032d-113">混色狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-113">Blend State</span></span>



| <span data-ttu-id="2032d-114">效果狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-114">Effect state</span></span>                                                                                                                      | <span data-ttu-id="2032d-115">Group</span><span class="sxs-lookup"><span data-stu-id="2032d-115">Group</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2032d-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="2032d-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="2032d-117">[ **D3D11 \_ BLEND \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="2032d-117">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="2032d-118">深度和樣板狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-118">Depth and Stencil State</span></span>



|  <span data-ttu-id="2032d-119">效果狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-119">Effect state</span></span>                                                                                                                                                              | <span data-ttu-id="2032d-120">Group</span><span class="sxs-lookup"><span data-stu-id="2032d-120">Group</span></span>                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2032d-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="2032d-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="2032d-122">[ **D3D11 深度樣板 \_ \_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="2032d-122">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="2032d-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="2032d-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="2032d-124">[ **D3D11 \_ 深度 \_ STENCILOP \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="2032d-124">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="2032d-125">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-125">Rasterizer State</span></span>



| <span data-ttu-id="2032d-126">效果狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-126">Effect state</span></span>                                                                                                                                | <span data-ttu-id="2032d-127">Group</span><span class="sxs-lookup"><span data-stu-id="2032d-127">Group</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2032d-128">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="2032d-128">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="2032d-129">**D3D11 \_ 填滿 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="2032d-129">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="2032d-130">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="2032d-130">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="2032d-131">**D3D11 的 \_ 挑選 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="2032d-131">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="2032d-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="2032d-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="2032d-133">D3D11 轉譯器 [ **\_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="2032d-133">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="2032d-134">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-134">Sampler State</span></span>



| <span data-ttu-id="2032d-135">效果狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-135">Effect state</span></span>                                                                                                    | <span data-ttu-id="2032d-136">Group</span><span class="sxs-lookup"><span data-stu-id="2032d-136">Group</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2032d-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc 邊框 MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="2032d-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="2032d-138">[ **D3D11 取樣器 \_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="2032d-138">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="2032d-139">如需範例，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) 。</span><span class="sxs-lookup"><span data-stu-id="2032d-139">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="2032d-140">效果物件狀態</span><span class="sxs-lookup"><span data-stu-id="2032d-140">Effect Object State</span></span>



| <span data-ttu-id="2032d-141">此效果物件</span><span class="sxs-lookup"><span data-stu-id="2032d-141">This Effect Object</span></span>                          | <span data-ttu-id="2032d-142">對應至</span><span class="sxs-lookup"><span data-stu-id="2032d-142">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2032d-143">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="2032d-143">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="2032d-144">轉譯器 [狀態](#rasterizer-state) 狀態物件。</span><span class="sxs-lookup"><span data-stu-id="2032d-144">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="2032d-145">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="2032d-145">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="2032d-146">[深度和樣板狀態](#depth-and-stencil-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="2032d-146">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="2032d-147">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="2032d-147">BLENDSTATE</span></span>                                  | <span data-ttu-id="2032d-148">[Blend 狀態](#blend-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="2032d-148">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="2032d-149">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="2032d-149">VERTEXSHADER</span></span>                                | <span data-ttu-id="2032d-150">已編譯的頂點著色器物件。</span><span class="sxs-lookup"><span data-stu-id="2032d-150">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="2032d-151">無效</span><span class="sxs-lookup"><span data-stu-id="2032d-151">PIXELSHADER</span></span>                                 | <span data-ttu-id="2032d-152">編譯的圖元著色器物件。</span><span class="sxs-lookup"><span data-stu-id="2032d-152">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="2032d-153">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="2032d-153">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="2032d-154">已編譯的幾何著色器物件。</span><span class="sxs-lookup"><span data-stu-id="2032d-154">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="2032d-155">DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="2032d-155">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="2032d-156">[**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="2032d-156">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="2032d-157">定義和使用狀態物件</span><span class="sxs-lookup"><span data-stu-id="2032d-157">Defining and using state objects</span></span>

<span data-ttu-id="2032d-158">系統會以下列格式在 FX 檔案中宣告狀態物件。</span><span class="sxs-lookup"><span data-stu-id="2032d-158">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="2032d-159">StateObjectType 是上面所列的其中一個狀態，而成員名稱則是任何將具有非預設值的成員名稱。</span><span class="sxs-lookup"><span data-stu-id="2032d-159">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="2032d-160">例如，若要設定 AlphaToCoverageEnable，並將 BlendEnable \[ 0 \] 設為 **FALSE** 的 blend 狀態物件，則會使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="2032d-160">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="2032d-161">使用 [ (Direct3D 11) 的效果技巧語法 ](d3d11-effect-technique-syntax.md)中所述的其中一個 SetStateGroup 函式，將狀態物件套用至技術傳遞。</span><span class="sxs-lookup"><span data-stu-id="2032d-161">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="2032d-162">例如，若要套用上面所述的 BlendState 物件，則會使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="2032d-162">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="2032d-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="2032d-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2032d-164">效果技巧語法</span><span class="sxs-lookup"><span data-stu-id="2032d-164">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="2032d-165"> (Direct3D 11) 的效果格式 </span><span class="sxs-lookup"><span data-stu-id="2032d-165">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 