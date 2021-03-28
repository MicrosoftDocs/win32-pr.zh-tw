---
title: 指定編譯器目標
description: 在這裡，我們會列出 D3DCompile \ 函式和 HLSL 編譯器支援之各種設定檔的目標。
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382734"
---
# <a name="specifying-compiler-targets"></a><span data-ttu-id="a0fbf-103">指定編譯器目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-103">Specifying Compiler Targets</span></span>

<span data-ttu-id="a0fbf-104">當您呼叫 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)、 [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)或 [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) 函式時，您需要指定著色器目標（著色器的組合）來進行編譯。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-104">You need to specify the shader target — set of shader features — to compile against when you call the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2), or [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function.</span></span> <span data-ttu-id="a0fbf-105">在這裡，我們會列出 **D3DCompile \*** 函式和 HLSL 編譯器支援之各種設定檔的目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-105">Here we list the targets for various profiles that the **D3DCompile\*** functions and the HLSL compiler support.</span></span>

-   [<span data-ttu-id="a0fbf-106">Direct3D 11.0 和11.1 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-106">Direct3D 11.0 and 11.1 feature levels</span></span>](#direct3d-110-and-111-feature-levels)
-   [<span data-ttu-id="a0fbf-107">Direct3D 10.1 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-107">Direct3D 10.1 feature level</span></span>](#direct3d-101-feature-level)
-   [<span data-ttu-id="a0fbf-108">Direct3D 10.0 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-108">Direct3D 10.0 feature level</span></span>](#direct3d-100-feature-level)
-   [<span data-ttu-id="a0fbf-109">Direct3D 9.1、9.2 和9.3 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-109">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>](#direct3d-91-92-and-93-feature-levels)
-   [<span data-ttu-id="a0fbf-110">舊版 Direct3D 9 著色器模型3。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-110">Legacy Direct3D 9 Shader Model 3.0</span></span>](#legacy-direct3d-9-shader-model-30)
-   [<span data-ttu-id="a0fbf-111">舊版 Direct3D 9 著色器模型2。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-111">Legacy Direct3D 9 Shader Model 2.0</span></span>](#legacy-direct3d-9-shader-model-20)
-   [<span data-ttu-id="a0fbf-112">舊版 Direct3D 9 著色器模型1。x</span><span class="sxs-lookup"><span data-stu-id="a0fbf-112">Legacy Direct3D 9 Shader Model 1.x</span></span>](#legacy-direct3d-9-shader-model-1x)
-   [<span data-ttu-id="a0fbf-113">舊版效果</span><span class="sxs-lookup"><span data-stu-id="a0fbf-113">Legacy Effects</span></span>](#legacy-effects)
-   [<span data-ttu-id="a0fbf-114">注意事項</span><span class="sxs-lookup"><span data-stu-id="a0fbf-114">Notes</span></span>](#notes)
-   [<span data-ttu-id="a0fbf-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0fbf-115">Related topics</span></span>](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a><span data-ttu-id="a0fbf-116">Direct3D 11.0 和11.1 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-116">Direct3D 11.0 and 11.1 feature levels</span></span>

<span data-ttu-id="a0fbf-117">以下是 Direct3D 11.0 和 11.1 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-117">Here are the shader targets that Direct3D 11.0 and 11.1 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>



| <span data-ttu-id="a0fbf-118">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-118">Target</span></span>   | <span data-ttu-id="a0fbf-119">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-119">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fbf-120">cs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-120">cs\_5\_0</span></span> | <span data-ttu-id="a0fbf-121">DirectCompute 5.0 ([計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-121">DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span></span>                              |
| <span data-ttu-id="a0fbf-122">ds \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-122">ds\_5\_0</span></span> | [<span data-ttu-id="a0fbf-123">網域著色器</span><span class="sxs-lookup"><span data-stu-id="a0fbf-123">Domain shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| <span data-ttu-id="a0fbf-124">gs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-124">gs\_5\_0</span></span> | <span data-ttu-id="a0fbf-125">[幾何著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-125">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="a0fbf-126">hs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-126">hs\_5\_0</span></span> | [<span data-ttu-id="a0fbf-127">輪廓著色器</span><span class="sxs-lookup"><span data-stu-id="a0fbf-127">Hull shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| <span data-ttu-id="a0fbf-128">ps \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-128">ps\_5\_0</span></span> | <span data-ttu-id="a0fbf-129">[像素著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="a0fbf-130">vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-130">vs\_5\_0</span></span> | <span data-ttu-id="a0fbf-131">[頂點著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-101-feature-level"></a><span data-ttu-id="a0fbf-132">Direct3D 10.1 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-132">Direct3D 10.1 feature level</span></span>

<span data-ttu-id="a0fbf-133">以下是 Direct3D 10.1 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-133">Here are the shader targets that the Direct3D 10.1 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="a0fbf-134">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-134">Target</span></span>   | <span data-ttu-id="a0fbf-135">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-135">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fbf-136">cs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-136">cs\_4\_1</span></span> | <span data-ttu-id="a0fbf-137">DirectCompute 4.1 ([計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="a0fbf-137">DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="a0fbf-138">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-138">gs\_4\_1</span></span> | <span data-ttu-id="a0fbf-139">[幾何著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-139">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="a0fbf-140">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-140">ps\_4\_1</span></span> | <span data-ttu-id="a0fbf-141">[像素著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="a0fbf-142">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-142">vs\_4\_1</span></span> | <span data-ttu-id="a0fbf-143">[頂點著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-100-feature-level"></a><span data-ttu-id="a0fbf-144">Direct3D 10.0 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-144">Direct3D 10.0 feature level</span></span>

<span data-ttu-id="a0fbf-145">以下是 Direct3D 10.0 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-145">Here are the shader targets that the Direct3D 10.0 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="a0fbf-146">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-146">Target</span></span>   | <span data-ttu-id="a0fbf-147">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-147">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fbf-148">cs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-148">cs\_4\_0</span></span> | <span data-ttu-id="a0fbf-149">DirectCompute 4.0 ([計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="a0fbf-149">DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="a0fbf-150">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-150">gs\_4\_0</span></span> | <span data-ttu-id="a0fbf-151">[幾何著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-151">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="a0fbf-152">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-152">ps\_4\_0</span></span> | <span data-ttu-id="a0fbf-153">[像素著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="a0fbf-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-154">vs\_4\_0</span></span> | <span data-ttu-id="a0fbf-155">[頂點著色器](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0fbf-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a><span data-ttu-id="a0fbf-156">Direct3D 9.1、9.2 和9.3 功能等級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-156">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>

<span data-ttu-id="a0fbf-157">以下是 Direct3D 9.1、9.2 和 9.3 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-157">Here are the shader targets that Direct3D 9.1, 9.2 and 9.3 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>

> [!Note]  
> <span data-ttu-id="a0fbf-158">當您使用 \* \_ 4 個 \_ \_ 層級 \_ 9 \_ x HLSL 著色器設定檔時，會隱含地使用[著色器模型](dx-graphics-hlsl-sm2.md)2.x 設定檔來支援具有 Direct3D 9 功能的硬體。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-158">When you use the \*\_4\_0\_level\_9\_x HLSL shader profiles, you implicitly use of the [Shader Model 2.x](dx-graphics-hlsl-sm2.md) profiles to support Direct3D 9 capable hardware.</span></span> <span data-ttu-id="a0fbf-159">著色器模型2.x 設定檔支援的流程式控制制行為比 [著色器模型](dx-graphics-hlsl-sm4.md) 4.x 和更新版本設定檔更受限。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-159">Shader Model 2.x profiles support more limited flow control behavior than the [Shader Model 4.x](dx-graphics-hlsl-sm4.md) and later profiles.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0fbf-160">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-160">Target</span></span></th>
<th><span data-ttu-id="a0fbf-161">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0fbf-162">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-162">ps_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="a0fbf-163">9.1 和9.2 的[圖元著色器](/previous-versions//bb205146(v=vs.85)) (ps_2_0) 的類似限制</span><span class="sxs-lookup"><span data-stu-id="a0fbf-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) for 9.1 and 9.2 (similar limits to ps_2_0)</span></span>
<ul>
<li><span data-ttu-id="a0fbf-164">64算術和32材質指示</span><span class="sxs-lookup"><span data-stu-id="a0fbf-164">64 arithmetic and 32 texture instructions</span></span></li>
<li><span data-ttu-id="a0fbf-165">12個臨時暫存器</span><span class="sxs-lookup"><span data-stu-id="a0fbf-165">12 temporary registers</span></span></li>
<li><span data-ttu-id="a0fbf-166">4個相依讀取層級</span><span class="sxs-lookup"><span data-stu-id="a0fbf-166">4 levels of dependent reads</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0fbf-167">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="a0fbf-167">ps_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="a0fbf-168">9.3 的<a href="/previous-versions//bb205146(v=vs.85)">圖元著色器</a> (ps_2_x ²與額外著色器功能的類似限制) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> for 9.3 (similar limits to ps_2_x² with additional shader features)</span></span>
<ul>
<li><span data-ttu-id="a0fbf-169">512指示</span><span class="sxs-lookup"><span data-stu-id="a0fbf-169">512 instructions</span></span></li>
<li><span data-ttu-id="a0fbf-170">32臨時暫存器</span><span class="sxs-lookup"><span data-stu-id="a0fbf-170">32 temporary registers</span></span></li>
<li><span data-ttu-id="a0fbf-171">靜態流量控制 (最大深度 4) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-171">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="a0fbf-172">動態流量控制 (最大深度 24) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-172">Dynamic flow control (max depth of 24)</span></span></li>
<li><span data-ttu-id="a0fbf-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="a0fbf-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span></span></li>
<li><span data-ttu-id="a0fbf-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="a0fbf-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span></span></li>
<li><span data-ttu-id="a0fbf-175">D3DPS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="a0fbf-175">D3DPS20CAPS_PREDICATION</span></span></li>
<li><span data-ttu-id="a0fbf-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="a0fbf-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span></span></li>
<li><span data-ttu-id="a0fbf-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="a0fbf-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0fbf-178">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-178">vs_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="a0fbf-179">9.1 和 9.2 (的<a href="/previous-versions//bb205146(v=vs.85)">頂點著色器</a>類似于 vs_2_0) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.1 and 9.2 (similar to vs_2_0)</span></span>
<ul>
<li><span data-ttu-id="a0fbf-180">256指示</span><span class="sxs-lookup"><span data-stu-id="a0fbf-180">256 instructions</span></span></li>
<li><span data-ttu-id="a0fbf-181">12個臨時暫存器</span><span class="sxs-lookup"><span data-stu-id="a0fbf-181">12 temporary registers</span></span></li>
<li><span data-ttu-id="a0fbf-182">靜態流量控制 (最大深度為 1) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-182">Static flow control (max depth of 1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0fbf-183">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="a0fbf-183">vs_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="a0fbf-184">9.3 (的<a href="/previous-versions//bb205146(v=vs.85)">頂點著色器</a>類似于 vs_2_a ²與其他著色器功能和實例) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.3 (similar to vs_2_a² with additional shader features and instancing)</span></span>
<ul>
<li><span data-ttu-id="a0fbf-185">256指示</span><span class="sxs-lookup"><span data-stu-id="a0fbf-185">256 instructions</span></span></li>
<li><span data-ttu-id="a0fbf-186">32臨時暫存器</span><span class="sxs-lookup"><span data-stu-id="a0fbf-186">32 temporary registers</span></span></li>
<li><span data-ttu-id="a0fbf-187">靜態流量控制 (最大深度 4) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-187">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="a0fbf-188">D3DVS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="a0fbf-188">D3DVS20CAPS_PREDICATION</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a><span data-ttu-id="a0fbf-189">舊版 Direct3D 9 著色器模型3。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-189">Legacy Direct3D 9 Shader Model 3.0</span></span>

<span data-ttu-id="a0fbf-190">以下是舊版 Direct3D 9 著色器模型3.0 ³的著色器目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-190">Here are the shader targets for legacy Direct3D 9 shader model 3.0³.</span></span>



| <span data-ttu-id="a0fbf-191">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-191">Target</span></span>    | <span data-ttu-id="a0fbf-192">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-192">Description</span></span>                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fbf-193">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-193">ps\_3\_0</span></span>  | <span data-ttu-id="a0fbf-194">[圖元著色器](/previous-versions//bb205146(v=vs.85)) 3。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>               |
| <span data-ttu-id="a0fbf-195">ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a0fbf-195">ps\_3\_sw</span></span> | <span data-ttu-id="a0fbf-196">[圖元著色器](/previous-versions//bb205146(v=vs.85)) 3.0 (軟體) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span>    |
| <span data-ttu-id="a0fbf-197">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-197">vs\_3\_0</span></span>  | <span data-ttu-id="a0fbf-198">[頂點著色器](/previous-versions//bb205146(v=vs.85)) 3。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>            |
| <span data-ttu-id="a0fbf-199">vs \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a0fbf-199">vs\_3\_sw</span></span> | <span data-ttu-id="a0fbf-200">[頂點著色器](/previous-versions//bb205146(v=vs.85)) 3.0 (軟體) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-20"></a><span data-ttu-id="a0fbf-201">舊版 Direct3D 9 著色器模型2。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-201">Legacy Direct3D 9 Shader Model 2.0</span></span>

<span data-ttu-id="a0fbf-202">以下是舊版 Direct3D 9 著色器模型2.0 ³的著色器目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-202">Here are the shader targets for legacy Direct3D 9 shader model 2.0³.</span></span>



| <span data-ttu-id="a0fbf-203">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-203">Target</span></span>    | <span data-ttu-id="a0fbf-204">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-204">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fbf-205">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-205">ps\_2\_0</span></span>  | <span data-ttu-id="a0fbf-206">[圖元著色器](/previous-versions//bb205146(v=vs.85)) 2。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>             |
| <span data-ttu-id="a0fbf-207">ps \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="a0fbf-207">ps\_2\_a</span></span>  | <span data-ttu-id="a0fbf-208">[圖元著色器](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="a0fbf-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>              |
| <span data-ttu-id="a0fbf-209">ps \_ 2 \_ b</span><span class="sxs-lookup"><span data-stu-id="a0fbf-209">ps\_2\_b</span></span>  | <span data-ttu-id="a0fbf-210">[圖元著色器](/previous-versions//bb205146(v=vs.85)) 2b</span><span class="sxs-lookup"><span data-stu-id="a0fbf-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b</span></span>              |
| <span data-ttu-id="a0fbf-211">ps \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a0fbf-211">ps\_2\_sw</span></span> | <span data-ttu-id="a0fbf-212">[圖元著色器](/previous-versions//bb205146(v=vs.85)) 2.0 軟體</span><span class="sxs-lookup"><span data-stu-id="a0fbf-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span>    |
| <span data-ttu-id="a0fbf-213">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-213">vs\_2\_0</span></span>  | <span data-ttu-id="a0fbf-214">[頂點著色器](/previous-versions//bb205146(v=vs.85)) 2。0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>          |
| <span data-ttu-id="a0fbf-215">vs \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="a0fbf-215">vs\_2\_a</span></span>  | <span data-ttu-id="a0fbf-216">[頂點著色器](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="a0fbf-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>           |
| <span data-ttu-id="a0fbf-217">vs \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a0fbf-217">vs\_2\_sw</span></span> | <span data-ttu-id="a0fbf-218">[頂點著色器](/previous-versions//bb205146(v=vs.85)) 2.0 軟體</span><span class="sxs-lookup"><span data-stu-id="a0fbf-218">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a><span data-ttu-id="a0fbf-219">舊版 Direct3D 9 著色器模型1。x</span><span class="sxs-lookup"><span data-stu-id="a0fbf-219">Legacy Direct3D 9 Shader Model 1.x</span></span>

<span data-ttu-id="a0fbf-220">以下是舊版 Direct3D 9 著色器模型1.x ⁴的著色器目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-220">Here are the shader targets for legacy Direct3D 9 shader model 1.x⁴.</span></span>



| <span data-ttu-id="a0fbf-221">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-221">Target</span></span>   | <span data-ttu-id="a0fbf-222">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-222">Description</span></span>                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fbf-223">德克薩斯州 \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-223">tx\_1\_0</span></span> | <span data-ttu-id="a0fbf-224">舊版 D3DX9 ⁵函式 [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) 和 [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) 使用的材質著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="a0fbf-224">Texture shader profile that legacy D3DX9⁵ functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) and [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span></span> |
| <span data-ttu-id="a0fbf-225">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-225">vs\_1\_1</span></span> | <span data-ttu-id="a0fbf-226">[頂點著色器](/previous-versions//bb205146(v=vs.85)) 1。1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1</span></span>                                                            |



 

## <a name="legacy-effects"></a><span data-ttu-id="a0fbf-227">舊版效果</span><span class="sxs-lookup"><span data-stu-id="a0fbf-227">Legacy Effects</span></span>

<span data-ttu-id="a0fbf-228">以下是舊版效果的效果目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-228">Here are the effect targets for legacy effects.</span></span>



| <span data-ttu-id="a0fbf-229">目標</span><span class="sxs-lookup"><span data-stu-id="a0fbf-229">Target</span></span>   | <span data-ttu-id="a0fbf-230">Description</span><span class="sxs-lookup"><span data-stu-id="a0fbf-230">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="a0fbf-231">fx \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-231">fx\_2\_0</span></span> | <span data-ttu-id="a0fbf-232">在 D3DX9 ⁵中，Direct3D 9 的 (FX) 效果</span><span class="sxs-lookup"><span data-stu-id="a0fbf-232">Effects (FX) for Direct3D 9 in D3DX9⁵</span></span>     |
| <span data-ttu-id="a0fbf-233">fx \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-233">fx\_4\_0</span></span> | <span data-ttu-id="a0fbf-234">D3DX10 ⁵中 Direct3D 10.0 的效果 (FX) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-234">Effects (FX) for Direct3D 10.0 in D3DX10⁵</span></span> |
| <span data-ttu-id="a0fbf-235">fx \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a0fbf-235">fx\_4\_1</span></span> | <span data-ttu-id="a0fbf-236">D3DX10 ⁵中 Direct3D 10.1 的效果 (FX) </span><span class="sxs-lookup"><span data-stu-id="a0fbf-236">Effects (FX) for Direct3D 10.1 in D3DX10⁵</span></span> |
| <span data-ttu-id="a0fbf-237">fx \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0fbf-237">fx\_5\_0</span></span> | <span data-ttu-id="a0fbf-238">適用于 Direct3D 11 ⁵的 (FX) 效果</span><span class="sxs-lookup"><span data-stu-id="a0fbf-238">Effects (FX) for Direct3D 11⁵</span></span>             |



 

## <a name="notes"></a><span data-ttu-id="a0fbf-239">備註</span><span class="sxs-lookup"><span data-stu-id="a0fbf-239">Notes</span></span>

<span data-ttu-id="a0fbf-240">以下是上述各節所指的一些注意事項：</span><span class="sxs-lookup"><span data-stu-id="a0fbf-240">Here are some notes that the preceding sections refer to:</span></span>

1.  <span data-ttu-id="a0fbf-241">[功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 和10.1 裝置可選擇性地支援 DirectCompute。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-241">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 and 10.1 devices can optionally support DirectCompute.</span></span> <span data-ttu-id="a0fbf-242">若要驗證支援，請使用 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) 搭配 [**D3D11 \_ 功能 \_ D3D10 \_ X \_ 硬體 \_ 選項**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature)。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-242">To verify support, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span></span>
2.  <span data-ttu-id="a0fbf-243">[功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 實際上需要符合 [舊版 Direct3D 9 著色器模型 3.0](#legacy-direct3d-9-shader-model-30)需求的硬體，但此功能層級不會使用 vs \_ 3 \_ 0 或 ps \_ 3 \_ 0 目標。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-243">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 effectively requires hardware that complies with the requirements for [legacy Direct3D 9 shader model 3.0](#legacy-direct3d-9-shader-model-30), but this feature level does not make use of vs\_3\_0 or ps\_3\_0 targets.</span></span>
3.  <span data-ttu-id="a0fbf-244">只搭配 Direct3D 9 API 使用舊版 Direct3D 9 著色器模型。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-244">Only use legacy Direct3D 9 shader models with the Direct3D 9 API.</span></span> <span data-ttu-id="a0fbf-245">相反地，請將2.x 設定檔與 Direct3D 2.x 和 11. x API 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-245">Instead, use the 9.x profiles with the Direct3D 10.x and 11.x API.</span></span>
4.  <span data-ttu-id="a0fbf-246">目前的 HLSL 著色 **器 \* D3DCompile** 函數不支援舊版1.x 圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-246">The current HLSL shader **D3DCompile\*** functions don't support legacy 1.x pixel shaders.</span></span> <span data-ttu-id="a0fbf-247">HLSL 支援這些目標的最新版本已于2006年10月版本的 DirectX SDK 中 D3DX9。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-247">The last version of HLSL to support these targets was D3DX9 in the October 2006 release of the DirectX SDK.</span></span>
5.  <span data-ttu-id="a0fbf-248">所有版本的 D3DX 和 DirectX SDK 均已淘汰。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-248">All versions of D3DX and the DirectX SDK are deprecated.</span></span> <span data-ttu-id="a0fbf-249">如需詳細資訊，請參閱 [什麼是 DIRECTX SDK？](/windows/desktop/directx-sdk--august-2009-)。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-249">For more info, see [Where is the DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0fbf-250">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0fbf-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0fbf-251">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="a0fbf-251">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 