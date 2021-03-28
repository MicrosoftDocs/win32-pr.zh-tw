---
title: 使用轉譯器階段開始使用
description: 本節說明如何設定視口、剪刀矩形、轉譯器狀態和多取樣。
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- '取樣器、轉譯器狀態 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315214"
---
# <a name="getting-started-with-the-rasterizer-stage"></a><span data-ttu-id="d9106-104">使用轉譯器階段開始使用</span><span class="sxs-lookup"><span data-stu-id="d9106-104">Getting Started with the Rasterizer Stage</span></span>

<span data-ttu-id="d9106-105">本節說明如何設定視口、剪刀矩形、轉譯器狀態和多取樣。</span><span class="sxs-lookup"><span data-stu-id="d9106-105">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span>

## <a name="set-the-viewport"></a><span data-ttu-id="d9106-106">設定區</span><span class="sxs-lookup"><span data-stu-id="d9106-106">Set the Viewport</span></span>

<span data-ttu-id="d9106-107">視口會將剪輯) 空間中 (的頂點位置對應到轉譯目標位置。</span><span class="sxs-lookup"><span data-stu-id="d9106-107">A viewport maps vertex positions (in clip space) into render target positions.</span></span> <span data-ttu-id="d9106-108">此步驟會將3D 位置調整成2D 空間。</span><span class="sxs-lookup"><span data-stu-id="d9106-108">This step scales the 3D positions into 2D space.</span></span> <span data-ttu-id="d9106-109">轉譯目標的方向是指向下 Y 軸;這需要在視口縮放期間翻轉 Y 座標。</span><span class="sxs-lookup"><span data-stu-id="d9106-109">A render target is oriented with the Y axes pointing down; this requires that the Y coordinates get flipped during the viewport scale.</span></span> <span data-ttu-id="d9106-110">此外，x 和 y 值的 x 和 y 範圍 (範圍的 x 和 y) 值會根據下列公式進行調整，以符合各區大小：</span><span class="sxs-lookup"><span data-stu-id="d9106-110">In addition, the x and y extents (range of the x and y values) are scaled to fit the viewport size according to the following formulas:</span></span>


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



<span data-ttu-id="d9106-111">教學課程1使用 [**D3D11 的 \_ 視口**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) 和呼叫 [**>id3d11devicecoNtext：： RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)來建立640×480的區。</span><span class="sxs-lookup"><span data-stu-id="d9106-111">Tutorial 1 creates a 640 × 480 viewport using [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) and by calling [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span></span>


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



<span data-ttu-id="d9106-112">[區描述] 會指定區的大小、使用 *MinDepth* 和 *MaxDepth*) 的地圖深度至 (的範圍，以及區左上角的位置。</span><span class="sxs-lookup"><span data-stu-id="d9106-112">The viewport description specifies the size of the viewport, the range to map depth to (using *MinDepth* and *MaxDepth*), and the placement of the top left of the viewport.</span></span> <span data-ttu-id="d9106-113">*MinDepth* 必須小於或等於 *MaxDepth*; *MinDepth* 和 *MaxDepth* 的範圍介於0.0 到1.0 （含）之間。</span><span class="sxs-lookup"><span data-stu-id="d9106-113">*MinDepth* must be less than or equal to *MaxDepth*; the range for both *MinDepth* and *MaxDepth* is between 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="d9106-114">區通常會對應至轉譯目標，但不是必要的;此外，此區的大小或位置不一定要與轉譯目標相同。</span><span class="sxs-lookup"><span data-stu-id="d9106-114">It is common for the viewport to map to a render target but it is not necessary; additionally, the viewport does not have to have the same size or position as the render target.</span></span>

<span data-ttu-id="d9106-115">您可以建立一個範圍的陣列，但只能將一個可套用至幾何著色器的基本輸出。</span><span class="sxs-lookup"><span data-stu-id="d9106-115">You can create an array of viewports, but only one can be applied to a primitive output from the geometry shader.</span></span> <span data-ttu-id="d9106-116">一次只能設定一個使用中的區。</span><span class="sxs-lookup"><span data-stu-id="d9106-116">Only one viewport can be set active at a time.</span></span> <span data-ttu-id="d9106-117">管線會使用預設的區域 (和剪式矩形，下一節會在點陣化期間) 討論。</span><span class="sxs-lookup"><span data-stu-id="d9106-117">The pipeline uses a default viewport (and scissor rectangle, discussed in the next section) during rasterization.</span></span> <span data-ttu-id="d9106-118">預設值一律是陣列中 (或剪下矩形) 的第一個視口。</span><span class="sxs-lookup"><span data-stu-id="d9106-118">The default is always the first viewport (or scissor rectangle) in the array.</span></span> <span data-ttu-id="d9106-119">若要在幾何著色器中執行每個基本的區選，請在 GS 輸出簽章宣告中的適當 GS 輸出元件上，指定 ViewportArrayIndex 語義。</span><span class="sxs-lookup"><span data-stu-id="d9106-119">To perform a per-primitive selection of the viewport in the geometry shader, specify the ViewportArrayIndex semantic on the appropriate GS output component in the GS output signature declaration.</span></span>

<span data-ttu-id="d9106-120">可在任何時間系結至轉譯器階段的最大視口 (和剪式矩形) 數目是 16 (由 **D3D11 \_ 區 \_ 和 \_ \_ \_ \_ 每個 \_ 管線) 的 SCISSORRECT 物件計數** 所指定。</span><span class="sxs-lookup"><span data-stu-id="d9106-120">The maximum number of viewports (and scissor rectangles) that can be bound to the rasterizer stage at any one time is 16 (specified by **D3D11\_VIEWPORT\_AND\_SCISSORRECT\_OBJECT\_COUNT\_PER\_PIPELINE**).</span></span>

## <a name="set-the-scissor-rectangle"></a><span data-ttu-id="d9106-121">設定剪式矩形</span><span class="sxs-lookup"><span data-stu-id="d9106-121">Set the Scissor Rectangle</span></span>

<span data-ttu-id="d9106-122">剪式矩形讓您有機會減少將傳送至輸出合併階段的圖元數目。</span><span class="sxs-lookup"><span data-stu-id="d9106-122">A scissor rectangle gives you another opportunity to reduce the number of pixels that will be sent to the output merger stage.</span></span> <span data-ttu-id="d9106-123">剪式矩形外的圖元會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="d9106-123">Pixels outside of the scissor rectangle are discarded.</span></span> <span data-ttu-id="d9106-124">剪式矩形的大小是以整數指定。</span><span class="sxs-lookup"><span data-stu-id="d9106-124">The size of the scissor rectangle is specified in integers.</span></span> <span data-ttu-id="d9106-125">根據 [系統值語義](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)中的 *ViewportArrayIndex* ，只有一個剪式矩形 () 可以在點陣期間套用至三角形。</span><span class="sxs-lookup"><span data-stu-id="d9106-125">Only one scissor rectangle (based on *ViewportArrayIndex* in [system value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) can be applied to a triangle during rasterization.</span></span>

<span data-ttu-id="d9106-126">若要啟用剪式矩形，請使用 D3D11 轉譯器 [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)中的 *ScissorEnable* 成員 () 。</span><span class="sxs-lookup"><span data-stu-id="d9106-126">To enable the scissor rectangle, use the *ScissorEnable* member (in [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span> <span data-ttu-id="d9106-127">預設的剪式矩形是空的矩形;也就是說，所有 rect 值都是0。</span><span class="sxs-lookup"><span data-stu-id="d9106-127">The default scissor rectangle is an empty rectangle; that is, all rect values are 0.</span></span> <span data-ttu-id="d9106-128">換句話說，如果您未設定剪式矩形，且已啟用剪下，則不會將任何圖元傳送到輸出合併階段。</span><span class="sxs-lookup"><span data-stu-id="d9106-128">In other words, if you do not set up the scissor rectangle and scissor is enabled, you will not send any pixels to the output-merger stage.</span></span> <span data-ttu-id="d9106-129">最常見的設定是將剪式矩形初始化為視口的大小。</span><span class="sxs-lookup"><span data-stu-id="d9106-129">The most common setup is to initialize the scissor rectangle to the size of the viewport.</span></span>

<span data-ttu-id="d9106-130">若要將剪式矩形的陣列設定至裝置，請使用 [**D3D11 \_ RECT**](d3d11-rect.md)呼叫 [**>id3d11devicecoNtext：： RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) 。</span><span class="sxs-lookup"><span data-stu-id="d9106-130">To set an array of scissor rectangles to the device, call [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) with [**D3D11\_RECT**](d3d11-rect.md).</span></span>


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



<span data-ttu-id="d9106-131">這個方法會採用兩個參數： (1) 陣列中的矩形數目， (2) 矩形的陣列。</span><span class="sxs-lookup"><span data-stu-id="d9106-131">This method takes two parameters: (1) the number of rectangles in the array and (2) an array of rectangles.</span></span>

<span data-ttu-id="d9106-132">管線會在點陣 (使用預設的剪式矩形索引，預設值為零大小的矩形，並已停用剪切) 。</span><span class="sxs-lookup"><span data-stu-id="d9106-132">The pipeline uses a default scissor rectangle index during rasterization (the default is a zero-size rectangle with clipping disabled).</span></span> <span data-ttu-id="d9106-133">若要覆寫此項，請 \_ 在 gs 輸出簽章宣告中指定 gs 輸出元件的 SV ViewportArrayIndex 語義。</span><span class="sxs-lookup"><span data-stu-id="d9106-133">To override this, specify the SV\_ViewportArrayIndex semantic to a GS output component in the GS output signature declaration.</span></span> <span data-ttu-id="d9106-134">這會造成 GS 階段將此 GS 輸出元件標示為系統產生的元件，並具備此語義。</span><span class="sxs-lookup"><span data-stu-id="d9106-134">This will cause the GS stage to mark this GS output component as a system-generated component with this semantic.</span></span> <span data-ttu-id="d9106-135">轉譯器階段會辨識此語義，並使用它附加的參數做為剪式矩形索引，以存取剪式矩形的陣列。</span><span class="sxs-lookup"><span data-stu-id="d9106-135">The rasterizer stage recognizes this semantic and will use the parameter it is attached to as the scissor rectangle index to access the array of scissor rectangles.</span></span> <span data-ttu-id="d9106-136">別忘了，您可以在建立轉譯器物件之前，先啟用 [轉譯器描述] 中的 [ *ScissorEnable* ] 值，讓轉譯器階段使用您定義的剪矩形。</span><span class="sxs-lookup"><span data-stu-id="d9106-136">Don't forget to tell the rasterizer stage to use the scissor rectangle that you define by enabling the *ScissorEnable* value in the rasterizer description before creating the rasterizer object.</span></span>

## <a name="set-rasterizer-state"></a><span data-ttu-id="d9106-137">設定轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="d9106-137">Set Rasterizer State</span></span>

<span data-ttu-id="d9106-138">從 Direct3D 10 開始，轉譯器的狀態會封裝在轉譯器的狀態物件中。</span><span class="sxs-lookup"><span data-stu-id="d9106-138">Beginning with Direct3D 10, rasterizer state is encapsulated in a rasterizer state object.</span></span> <span data-ttu-id="d9106-139">您最多可以建立4096個轉譯器狀態物件，然後藉由將控制碼傳遞給狀態物件，將其設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="d9106-139">You may create up to 4096 rasterizer state objects which can then be set to the device by passing a handle to the state object.</span></span>

<span data-ttu-id="d9106-140">使用 [**ID3D11Device1：： CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) 從轉譯器描述建立轉譯器狀態物件 (參閱 D3D11 轉譯器 [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) 。</span><span class="sxs-lookup"><span data-stu-id="d9106-140">Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) to create a rasterizer state object from a rasterizer description (see [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span>


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



<span data-ttu-id="d9106-141">這一組範例狀態的完成可能是最基本的轉譯器設定：</span><span class="sxs-lookup"><span data-stu-id="d9106-141">This example set of state accomplishes perhaps the most basic rasterizer setup:</span></span>

-   <span data-ttu-id="d9106-142">純色填滿模式</span><span class="sxs-lookup"><span data-stu-id="d9106-142">Solid fill mode</span></span>
-   <span data-ttu-id="d9106-143">挑選出或移除臉部;假設基本物件的逆時針繞組順序</span><span class="sxs-lookup"><span data-stu-id="d9106-143">Cull out or remove back faces; assume counter-clockwise winding order for primitives</span></span>
-   <span data-ttu-id="d9106-144">關閉深度偏差但啟用深度緩衝，並啟用剪式矩形</span><span class="sxs-lookup"><span data-stu-id="d9106-144">Turn off depth bias but enable depth buffering and enable the scissor rectangle</span></span>
-   <span data-ttu-id="d9106-145">關閉取樣和線條消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="d9106-145">Turn off multisampling and line anti-aliasing</span></span>

<span data-ttu-id="d9106-146">此外，基本的轉譯器作業一律包含下列各項：將 (剪切至視圖的錐分割) 、透視圖和圖區尺規。</span><span class="sxs-lookup"><span data-stu-id="d9106-146">In addition, basic rasterizer operations, always include the following: clipping (to the view frustum), perspective divide, and the viewport scale.</span></span> <span data-ttu-id="d9106-147">成功建立轉譯器狀態物件之後，請將它設定為裝置，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d9106-147">After successfully creating the rasterizer state object, set it to the device like this:</span></span>


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a><span data-ttu-id="d9106-148">多重採樣</span><span class="sxs-lookup"><span data-stu-id="d9106-148">Multisampling</span></span>

<span data-ttu-id="d9106-149">多級取樣會以較高的解析度來取樣影像的部分或所有元件， (接著將解析度縮小至原始解析度) ，以減少繪製多邊形邊緣所造成的最明顯鋸齒形式。</span><span class="sxs-lookup"><span data-stu-id="d9106-149">Multisampling samples some or all of the components of an image at a higher resolution (followed by downsampling to the original resolution) to reduce the most visible form of aliasing caused by drawing polygon edges.</span></span> <span data-ttu-id="d9106-150">雖然取樣器需要子圖元範例，但新式 GPU 會執行多重取樣，以便每個圖元執行一次圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="d9106-150">Even though multisampling requires sub-pixel samples, modern GPU's implement multisampling so that a pixel shader runs once per pixel.</span></span> <span data-ttu-id="d9106-151">這可在效能 (特別是在 GPU 系結應用程式) 和消除最終影像的消除鋸齒之間提供可接受的取捨。</span><span class="sxs-lookup"><span data-stu-id="d9106-151">This provides an acceptable tradeoff between performance (especially in a GPU bound application) and anti-aliasing the final image.</span></span>

<span data-ttu-id="d9106-152">若要使用取樣，請在 [點陣化 [**描述**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)] 中設定 [啟用] 欄位、建立多重取樣轉譯目標，然後使用著色器讀取轉譯目標，將範例解析成單一圖元色彩，或呼叫 [**>id3d11devicecoNtext：： ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) ，以使用視訊卡來解析範例。</span><span class="sxs-lookup"><span data-stu-id="d9106-152">To use multisampling, set the enable field in the [**rasterization description**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), create a multisampled render target, and either read the render target with a shader to resolve the samples into a single pixel color or call [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) to resolve the samples using the video card.</span></span> <span data-ttu-id="d9106-153">最常見的案例是繪製至一個或多個多重取樣轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="d9106-153">The most common scenario is to draw to one or more multisampled render targets.</span></span>

<span data-ttu-id="d9106-154">交叉取樣與使用範例遮罩無關、已啟用 [Alpha 至涵蓋範圍](d3d10-graphics-programming-guide-blend-state.md) ，還是每個樣本) 一律執行的樣板作業 (。</span><span class="sxs-lookup"><span data-stu-id="d9106-154">Multisampling is independent of whether or not a sample mask is used, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) is enabled, or stencil operations (which are always performed per-sample).</span></span>

<span data-ttu-id="d9106-155">深度測試會受到取樣的影響：</span><span class="sxs-lookup"><span data-stu-id="d9106-155">Depth testing is affected by multisampling:</span></span>

-   <span data-ttu-id="d9106-156">啟用取樣時，深度會依樣本插入，且深度/樣板測試會依樣本進行：所有傳遞範例的圖元著色器輸出色彩都是重複的。</span><span class="sxs-lookup"><span data-stu-id="d9106-156">When multisampling is enabled, depth is interpolated per sample and the depth/stencil test is done per sample; the pixel shader output color is duplicated for all passing samples.</span></span> <span data-ttu-id="d9106-157">如果圖元著色器輸出深度，則所有樣本的深度值都會重複 (雖然此案例失去了取樣) 的優點。</span><span class="sxs-lookup"><span data-stu-id="d9106-157">If the pixel shader outputs depth, the depth value is duplicated for all samples (although this scenario loses the benefit of multisampling).</span></span>
-   <span data-ttu-id="d9106-158">當您停用取樣時，深度/樣板測試仍會依樣本進行，但深度不會依樣本插補。</span><span class="sxs-lookup"><span data-stu-id="d9106-158">When multisampling is disabled, depth/stencil testing is still done per-sample, but depth is not interpolated per-sample.</span></span>

<span data-ttu-id="d9106-159">在單一轉譯目標內混用多重取樣和非多重取樣轉譯沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="d9106-159">There are no restrictions for mixing multisampled and non-multisampled rendering within a single render target.</span></span> <span data-ttu-id="d9106-160">如果您啟用取樣器並繪製至非多重取樣轉譯目標，則會產生與未啟用取樣器相同的結果;取樣的完成方式為每圖元一個樣本。</span><span class="sxs-lookup"><span data-stu-id="d9106-160">If you enable multisampling and draw to a non-multisampled render target, you produce the same result as if multisampling were not enabled; sampling is done with a single sample per-pixel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9106-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9106-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9106-162">轉譯器階段</span><span class="sxs-lookup"><span data-stu-id="d9106-162">Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 