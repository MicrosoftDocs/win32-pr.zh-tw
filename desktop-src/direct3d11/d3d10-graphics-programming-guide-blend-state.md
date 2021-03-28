---
title: 設定混合功能
description: 在輸出值寫入轉譯目標之前，會對每個圖元著色器輸出 (RGBA 值) 執行混合作業。 如果啟用取樣，則會在每個執行程式上進行混合;否則，會在每個圖元上執行混色。
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990919"
---
# <a name="configuring-blending-functionality"></a><span data-ttu-id="325ff-104">設定混合功能</span><span class="sxs-lookup"><span data-stu-id="325ff-104">Configuring Blending Functionality</span></span>

<span data-ttu-id="325ff-105">在輸出值寫入轉譯目標之前，會對每個圖元著色器輸出 (RGBA 值) 執行混合作業。</span><span class="sxs-lookup"><span data-stu-id="325ff-105">Blending operations are performed on every pixel shader output (RGBA value) before the output value is written to a render target.</span></span> <span data-ttu-id="325ff-106">如果啟用取樣，則會在每個執行程式上進行混合;否則，會在每個圖元上執行混色。</span><span class="sxs-lookup"><span data-stu-id="325ff-106">If multisampling is enabled, blending is done on each multisample; otherwise, blending is performed on each pixel.</span></span>

-   [<span data-ttu-id="325ff-107">建立 Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="325ff-107">Create the Blend State</span></span>](#create-the-blend-state)
-   [<span data-ttu-id="325ff-108">系結 Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="325ff-108">Bind the Blend State</span></span>](#bind-the-blend-state)
-   [<span data-ttu-id="325ff-109">Advanced 混色主題</span><span class="sxs-lookup"><span data-stu-id="325ff-109">Advanced Blending Topics</span></span>](#advanced-blending-topics)
    -   [<span data-ttu-id="325ff-110">Alpha 到涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="325ff-110">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
    -   [<span data-ttu-id="325ff-111">混合圖元著色器輸出</span><span class="sxs-lookup"><span data-stu-id="325ff-111">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)
-   [<span data-ttu-id="325ff-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="325ff-112">Related topics</span></span>](#related-topics)

## <a name="create-the-blend-state"></a><span data-ttu-id="325ff-113">建立 Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="325ff-113">Create the Blend State</span></span>

<span data-ttu-id="325ff-114">Blend 狀態是用來控制混合的狀態集合。</span><span class="sxs-lookup"><span data-stu-id="325ff-114">The blend state is a collection of states used to control blending.</span></span> <span data-ttu-id="325ff-115">這些狀態 (定義于 [**D3D11 \_ blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) 用來藉由呼叫 [**ID3D11Device1：： CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1)來建立 BLEND 狀態物件。</span><span class="sxs-lookup"><span data-stu-id="325ff-115">These states (defined in [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) are used to create the blend state object by calling [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span></span>

<span data-ttu-id="325ff-116">例如，以下是一個非常簡單的 blend 狀態建立範例，可停用 Alpha 混合，而不會使用每個元件的圖元遮罩。</span><span class="sxs-lookup"><span data-stu-id="325ff-116">For instance, here is a very simple example of blend-state creation that disables alpha blending and uses no per-component pixel masking.</span></span>


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



<span data-ttu-id="325ff-117">此範例類似于 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="325ff-117">This example is similar to the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="bind-the-blend-state"></a><span data-ttu-id="325ff-118">系結 Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="325ff-118">Bind the Blend State</span></span>

<span data-ttu-id="325ff-119">建立 blend 狀態物件之後，請呼叫 [**>id3d11devicecoNtext：： OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate)，將 blend 狀態物件系結至輸出合併階段。</span><span class="sxs-lookup"><span data-stu-id="325ff-119">After you create the blend-state object, bind the blend-state object to the output-merger stage by calling [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span></span>


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



<span data-ttu-id="325ff-120">此 API 採用三個參數： blend 物件、四個元件的 blend 因數，以及一個範例遮罩。</span><span class="sxs-lookup"><span data-stu-id="325ff-120">This API takes three parameters: the blend-state object, a four-component blend factor, and a sample mask.</span></span> <span data-ttu-id="325ff-121">您可以針對 blend 狀態物件傳遞 **Null** ，以指定預設的 blend 狀態或傳入 blend 物件。</span><span class="sxs-lookup"><span data-stu-id="325ff-121">You can pass in **NULL** for the blend-state object to specify the default blend state or pass in a blend-state object.</span></span> <span data-ttu-id="325ff-122">如果您使用 [**D3D11 \_ blend \_ Blend \_ 因數**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) 或 [**D3D11 blend 的 blend \_ \_ \_ \_ 因數**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend)來建立 blend 物件，您可以將 blend 因數傳遞給圖元著色器、轉譯目標或兩者的 lambert 值。</span><span class="sxs-lookup"><span data-stu-id="325ff-122">If you created the blend-state object with [**D3D11\_BLEND\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) or [**D3D11\_BLEND\_INV\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), you can pass a blend factor to modulate values for the pixel shader, render target, or both.</span></span> <span data-ttu-id="325ff-123">如果您未使用 **D3D11 \_ blend \_ Blend \_ 因數** 或 **D3D11 blend 的 blend \_ \_ \_ \_ 因數** 來建立 blend 物件，您仍然可以傳遞非 Null 的 blend 因數，但是混合階段不會使用 blend 因數; 執行時間會儲存 blend 因數，您稍後可以呼叫 [**>id3d11devicecoNtext：： OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) 來取得 blend 係數。</span><span class="sxs-lookup"><span data-stu-id="325ff-123">If you didn't create the blend-state object with **D3D11\_BLEND\_BLEND\_FACTOR** or **D3D11\_BLEND\_INV\_BLEND\_FACTOR**, you can still pass a non-NULL blend factor, but the blending stage does not use the blend factor; the runtime stores the blend factor, and you can later call [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) to retrieve the blend factor.</span></span> <span data-ttu-id="325ff-124">如果您傳遞 **Null**，則執行時間會使用或儲存相當於 {1，1，1，1} 的 blend 係數。</span><span class="sxs-lookup"><span data-stu-id="325ff-124">If you pass **NULL**, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.</span></span> <span data-ttu-id="325ff-125">範例遮罩是使用者定義的遮罩，可決定如何在更新現有的轉譯目標之前對其進行取樣。</span><span class="sxs-lookup"><span data-stu-id="325ff-125">The sample mask is a user-defined mask that determines how to sample the existing render target before updating it.</span></span> <span data-ttu-id="325ff-126">預設的取樣遮罩是指定點取樣的0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="325ff-126">The default sampling mask is 0xffffffff which designates point sampling.</span></span>

<span data-ttu-id="325ff-127">在最深度的緩衝配置中，最接近相機的圖元是繪製的圖元。</span><span class="sxs-lookup"><span data-stu-id="325ff-127">In most depth buffering schemes, the pixel closest to the camera is the one that gets drawn.</span></span> <span data-ttu-id="325ff-128">[設定深度樣板狀態](d3d10-graphics-programming-guide-depth-stencil.md)時， [**D3D11 深度樣板 \_ \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)的 **DepthFunc** 成員可以是任何 [**D3D11 的 \_ 比較 \_ FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func)。</span><span class="sxs-lookup"><span data-stu-id="325ff-128">When [setting up the depth stencil state](d3d10-graphics-programming-guide-depth-stencil.md), the **DepthFunc** member of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) can be any [**D3D11\_COMPARISON\_FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span></span> <span data-ttu-id="325ff-129">一般來說，您會想要讓 **DepthFunc** 的 **D3D11 \_ 比較比較 \_ 少**，因此最接近相機的圖元會覆寫其後的圖元。</span><span class="sxs-lookup"><span data-stu-id="325ff-129">Normally, you would want **DepthFunc** to be **D3D11\_COMPARISON\_LESS**, so that the pixels closest to the camera will overwrite the pixels behind them.</span></span> <span data-ttu-id="325ff-130">不過，視您的應用程式需求而定，您可以使用任何其他的比較函數來進行深度測試。</span><span class="sxs-lookup"><span data-stu-id="325ff-130">However, depending on the needs of your application, any of the other comparison functions may be used to do the depth test.</span></span>

## <a name="advanced-blending-topics"></a><span data-ttu-id="325ff-131">Advanced 混色主題</span><span class="sxs-lookup"><span data-stu-id="325ff-131">Advanced Blending Topics</span></span>

-   [<span data-ttu-id="325ff-132">Alpha 到涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="325ff-132">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
-   [<span data-ttu-id="325ff-133">混合圖元著色器輸出</span><span class="sxs-lookup"><span data-stu-id="325ff-133">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a><span data-ttu-id="325ff-134">Alpha 到涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="325ff-134">Alpha-To-Coverage</span></span>

<span data-ttu-id="325ff-135">「Alpha 到涵蓋範圍」是一種對等情況最有用的多層式技術，例如密集 foliage，其中有數個重迭的多邊形會使用 Alpha 透明度來定義介面內的邊緣。</span><span class="sxs-lookup"><span data-stu-id="325ff-135">Alpha-to-coverage is a multisampling technique that is most useful for situations such as dense foliage where there are several overlapping polygons that use alpha transparency to define edges within the surface.</span></span>

<span data-ttu-id="325ff-136">您可以使用 [**D3D11 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)或 [**D3D11 \_ blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)的 **AlphaToCoverageEnable** 成員，來切換執行時間是否會將輸出暫存器 (Alpha) 的元件，[從 \_](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)圖元著色器轉換成 n 步驟涵蓋範圍遮罩 (提供了 n 個範例 **RenderTarget**) 。</span><span class="sxs-lookup"><span data-stu-id="325ff-136">You can use the **AlphaToCoverageEnable** member of [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) or [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) to toggle whether the runtime converts the .a component (alpha) of output register [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 from the pixel shader to an n-step coverage mask (given an n-sample **RenderTarget**).</span></span> <span data-ttu-id="325ff-137">執行時間除了範例遮罩之外，也會使用基本 (中圖元的一般樣本涵蓋範圍來執行 **和作業，**) 判斷要在所有使用中的 **RenderTarget** 中更新的範例。</span><span class="sxs-lookup"><span data-stu-id="325ff-137">The runtime performs an **AND** operation of this mask with the typical sample coverage for the pixel in the primitive (in addition to the sample mask) to determine which samples to update in all the active **RenderTarget** s.</span></span>

<span data-ttu-id="325ff-138">如果圖元著色器輸出 [SV \_ 涵蓋範圍](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)，則執行時間會停用 Alpha 至涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="325ff-138">If the pixel shader outputs [SV\_Coverage](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), the runtime disables alpha-to-coverage.</span></span>

> [!Note]  
> <span data-ttu-id="325ff-139">在取樣中，執行時間只會共用所有 **RenderTarget** 的一個涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="325ff-139">In multisampling, the runtime shares only one coverage for all **RenderTarget** s.</span></span> <span data-ttu-id="325ff-140">執行時間讀取和轉換的事實。當 **AlphaToCoverageEnable** 為 TRUE 時，從輸出 [SV \_ 目標](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 到涵蓋範圍的事實不會變更。如果 **RenderTarget** 發生在) 中，則會在 **RenderTarget** 0 時移至 blender 的值 (。</span><span class="sxs-lookup"><span data-stu-id="325ff-140">The fact that the runtime reads and converts .a from output [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 to coverage when **AlphaToCoverageEnable** is TRUE does not change the .a value that goes to the blender at **RenderTarget** 0 (if a **RenderTarget** happens to be set there).</span></span> <span data-ttu-id="325ff-141">一般情況下，如果您啟用 Alpha 至涵蓋範圍，就不會影響圖元著色器的所有色彩輸出如何透過 [輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md)與 **RenderTarget** 互動，不同之處在于執行時間會使用 Alpha 對涵蓋範圍遮罩來執行涵蓋範圍遮罩的 **和** 作業。</span><span class="sxs-lookup"><span data-stu-id="325ff-141">In general, if you enable alpha-to-coverage, you don't affect how all color outputs from pixel shaders interact with **RenderTarget** s through the [output-merger stage](d3d10-graphics-programming-guide-output-merger-stage.md) except that the runtime performs an **AND** operation of the coverage mask with the alpha-to-coverage mask.</span></span> <span data-ttu-id="325ff-142">Alpha 到涵蓋範圍適用于執行時間是否可以 blend **RenderTarget** 或您是否在 **RenderTarget** 上使用 blend。</span><span class="sxs-lookup"><span data-stu-id="325ff-142">Alpha-to-coverage works independently to whether the runtime can blend **RenderTarget** or whether you use blending on **RenderTarget**.</span></span>

 

<span data-ttu-id="325ff-143">圖形硬體無法精確地指定其轉換圖元著色器 [SV \_ 目標](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 的方式。 (Alpha) 至涵蓋範圍遮罩，但 0 (或較少的) 必須對應至不 (的涵蓋範圍，且小於 1) 或更高的必須對應到完整的涵蓋範圍， (在執行時間使用實際的基本涵蓋範圍) 來執行 **和** 作業之前，必須先</span><span class="sxs-lookup"><span data-stu-id="325ff-143">Graphics hardware doesn't precisely specify exactly how it converts pixel shader [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alpha) to a coverage mask, except that alpha of 0 (or less) must map to no coverage and alpha of 1 (or greater) must map to full coverage (before the runtime performs an **AND** operation with actual primitive coverage).</span></span> <span data-ttu-id="325ff-144">當 Alpha 從0變成1時，產生的涵蓋範圍通常會以單純的方式增加。</span><span class="sxs-lookup"><span data-stu-id="325ff-144">As alpha goes from 0 to 1, the resulting coverage should generally increase monotonically.</span></span> <span data-ttu-id="325ff-145">不過，硬體可能會執列區域遞色，以提供更好的 Alpha 值量化，代價是空間解析度和雜訊的成本。</span><span class="sxs-lookup"><span data-stu-id="325ff-145">However, hardware might perform area dithering to provide some better quantization of alpha values at the cost of spatial resolution and noise.</span></span> <span data-ttu-id="325ff-146">NaN 的 Alpha 值 (不是數位) 會導致 (零) mask 沒有涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="325ff-146">An alpha value of NaN (Not a Number) results in a no coverage (zero) mask.</span></span>

<span data-ttu-id="325ff-147">Alpha 到涵蓋範圍也是傳統上用來進行螢幕畫面的透明度或定義詳細的 silhouettes，否則不透明的 sprite。</span><span class="sxs-lookup"><span data-stu-id="325ff-147">Alpha-to-coverage is also traditionally used for screen-door transparency or defining detailed silhouettes for otherwise opaque sprites.</span></span>

### <a name="blending-pixel-shader-outputs"></a><span data-ttu-id="325ff-148">混合圖元著色器輸出</span><span class="sxs-lookup"><span data-stu-id="325ff-148">Blending Pixel Shader Outputs</span></span>

<span data-ttu-id="325ff-149">這項功能可讓輸出合併同時使用圖元著色器輸出，做為混合作業的輸入來源與位置0的單一轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="325ff-149">This feature enables the output merger to use both the pixel shader outputs simultaneously as input sources to a blending operation with the single render target at slot 0.</span></span>

<span data-ttu-id="325ff-150">這個範例會採用兩個結果，並將它們結合在單一行程中，然後將一個乘到目的地，並使用另一個來加上：</span><span class="sxs-lookup"><span data-stu-id="325ff-150">This example takes two results and combines them in a single pass, blending one into the destination with a multiply and the other with an add:</span></span>


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



<span data-ttu-id="325ff-151">這個範例會將第一個圖元著色器輸出設定為來源色彩，並將第二個輸出設定為每個色彩元件 blend 係數。</span><span class="sxs-lookup"><span data-stu-id="325ff-151">This example configures the first pixel shader output as the source color and the second output as a per-color component blend factor.</span></span>


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



<span data-ttu-id="325ff-152">此範例說明 blend 因數必須與著色器 swizzles 相符的方式：</span><span class="sxs-lookup"><span data-stu-id="325ff-152">This example illustrates how the blend factors must match the shader swizzles:</span></span>


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



<span data-ttu-id="325ff-153">Blend 因數和著色器程式碼會一起表示需要圖元著色器，才可輸出至少 o0 r 和 o1. a。</span><span class="sxs-lookup"><span data-stu-id="325ff-153">Together, the blend factors and the shader code imply that the pixel shader is required to output at least o0.r and o1.a.</span></span> <span data-ttu-id="325ff-154">著色器可以輸出額外的輸出元件，但會忽略，而較少的元件會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="325ff-154">Extra output components can be output by the shader but would be ignored, fewer components would produce undefined results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="325ff-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="325ff-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="325ff-156">輸出合併階段</span><span class="sxs-lookup"><span data-stu-id="325ff-156">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="325ff-157"> (Direct3D 10) 的管線階段 </span><span class="sxs-lookup"><span data-stu-id="325ff-157">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 