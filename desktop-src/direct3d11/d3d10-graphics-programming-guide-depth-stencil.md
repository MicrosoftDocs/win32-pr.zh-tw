---
title: 設定 Depth-Stencil 功能
description: 本章節涵蓋的步驟，內容為設定深度樣板緩衝區及輸出合併階段的深度樣板狀態。
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682718"
---
# <a name="configuring-depth-stencil-functionality"></a><span data-ttu-id="72fe2-103">設定 Depth-Stencil 功能</span><span class="sxs-lookup"><span data-stu-id="72fe2-103">Configuring Depth-Stencil Functionality</span></span>

<span data-ttu-id="72fe2-104">本章節涵蓋的步驟，內容為設定深度樣板緩衝區及輸出合併階段的深度樣板狀態。</span><span class="sxs-lookup"><span data-stu-id="72fe2-104">This section covers the steps for setting up the depth-stencil buffer, and depth-stencil state for the output-merger stage.</span></span>

-   [<span data-ttu-id="72fe2-105">建立 Depth-Stencil 資源</span><span class="sxs-lookup"><span data-stu-id="72fe2-105">Create a Depth-Stencil Resource</span></span>](#create-a-depth-stencil-resource)
-   [<span data-ttu-id="72fe2-106">建立 Depth-Stencil 狀態</span><span class="sxs-lookup"><span data-stu-id="72fe2-106">Create Depth-Stencil State</span></span>](#create-depth-stencil-state)
-   [<span data-ttu-id="72fe2-107">將 Depth-Stencil 資料系結至 OM 階段</span><span class="sxs-lookup"><span data-stu-id="72fe2-107">Bind Depth-Stencil Data to the OM Stage</span></span>](#bind-depth-stencil-data-to-the-om-stage)

<span data-ttu-id="72fe2-108">待您了解如何使用深度樣板緩衝區及其對應的深度樣板狀態之後，請參閱[進階樣板技術](#advanced-stencil-techniques)。</span><span class="sxs-lookup"><span data-stu-id="72fe2-108">Once you know how to use the depth-stencil buffer and the corresponding depth-stencil state, refer to [advanced-stencil techniques](#advanced-stencil-techniques).</span></span>

## <a name="create-a-depth-stencil-resource"></a><span data-ttu-id="72fe2-109">建立 Depth-Stencil 資源</span><span class="sxs-lookup"><span data-stu-id="72fe2-109">Create a Depth-Stencil Resource</span></span>

<span data-ttu-id="72fe2-110">使用材質資源建立深度樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="72fe2-110">Create the depth-stencil buffer using a texture resource.</span></span>


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a><span data-ttu-id="72fe2-111">建立深度樣板狀態</span><span class="sxs-lookup"><span data-stu-id="72fe2-111">Create Depth-Stencil State</span></span>

<span data-ttu-id="72fe2-112">深度樣板狀態會告訴輸出合併階段如何執行[深度樣板測試](d3d10-graphics-programming-guide-output-merger-stage.md)。</span><span class="sxs-lookup"><span data-stu-id="72fe2-112">The depth-stencil state tells the output-merger stage how to perform the [depth-stencil test](d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="72fe2-113">深度樣板測試決定是否要繪製給定的像素。</span><span class="sxs-lookup"><span data-stu-id="72fe2-113">The depth-stencil test determines whether or not a given pixel should be drawn.</span></span>


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



<span data-ttu-id="72fe2-114">DepthEnable 和 StencilEnable 可啟用 (並停用) 深度和樣板測試。</span><span class="sxs-lookup"><span data-stu-id="72fe2-114">DepthEnable and StencilEnable enable (and disable) depth and stencil testing.</span></span> <span data-ttu-id="72fe2-115">將 DepthEnable 設定為 **FALSE** 以停用深度測試，並防止寫入深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="72fe2-115">Set DepthEnable to **FALSE** to disable depth testing and prevent writing to the depth buffer.</span></span> <span data-ttu-id="72fe2-116">將 StencilEnable 設定為 **false** 以停用樣板測試，並防止寫入至樣板緩衝區 (當 DepthEnable 為 **FALSE** 且 StencilEnable 為 **TRUE** 時，深度測試一律會在樣板作業) 中傳遞。</span><span class="sxs-lookup"><span data-stu-id="72fe2-116">Set StencilEnable to **FALSE** to disable stencil testing and prevent writing to the stencil buffer (when DepthEnable is **FALSE** and StencilEnable is **TRUE**, the depth test always passes in the stencil operation).</span></span>

<span data-ttu-id="72fe2-117">DepthEnable 只會影響輸出合併階段-在資料輸入至圖元著色器之前，不會影響剪切、深度偏差或值的固定。</span><span class="sxs-lookup"><span data-stu-id="72fe2-117">DepthEnable only affects the output-merger stage - it does not affect clipping, depth bias, or clamping of values before the data is input to a pixel shader.</span></span>

## <a name="bind-depth-stencil-data-to-the-om-stage"></a><span data-ttu-id="72fe2-118">將深度樣板資料繫結至輸出合併階段</span><span class="sxs-lookup"><span data-stu-id="72fe2-118">Bind Depth-Stencil Data to the OM Stage</span></span>

<span data-ttu-id="72fe2-119">繫結深度樣板狀態。</span><span class="sxs-lookup"><span data-stu-id="72fe2-119">Bind the depth-stencil state.</span></span>


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



<span data-ttu-id="72fe2-120">使用檢視繫結深度樣板資源。</span><span class="sxs-lookup"><span data-stu-id="72fe2-120">Bind the depth-stencil resource using a view.</span></span>


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



<span data-ttu-id="72fe2-121">轉譯目標視圖的陣列可傳遞至 [**>id3d11devicecoNtext：： OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)，不過所有的呈現目標視圖都將對應至單一深度樣板視圖。</span><span class="sxs-lookup"><span data-stu-id="72fe2-121">An array of render-target views may be passed into [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), however all of those render-target views will correspond to a single depth stencil view.</span></span> <span data-ttu-id="72fe2-122">Direct3D 11 中的轉譯目標陣列是一項功能，可讓應用程式在基本層級同時轉譯成多個呈現目標。</span><span class="sxs-lookup"><span data-stu-id="72fe2-122">The render target array in Direct3D 11 is a feature that enables an application to render onto multiple render targets simultaneously at the primitive level.</span></span> <span data-ttu-id="72fe2-123">轉譯目標陣列可讓您以多個 **>id3d11devicecoNtext：： OMSetRenderTargets** 呼叫來個別設定轉譯目標，以提供更高的效能， (基本上是 Direct3D 9) 中所採用的方法。</span><span class="sxs-lookup"><span data-stu-id="72fe2-123">Render target arrays offer increased performance over individually setting render targets with multiple calls to **ID3D11DeviceContext::OMSetRenderTargets** (essentially the method employed in Direct3D 9).</span></span>

<span data-ttu-id="72fe2-124">轉譯目標必須全部都是相同的資源類型。</span><span class="sxs-lookup"><span data-stu-id="72fe2-124">Render targets must all be the same type of resource.</span></span> <span data-ttu-id="72fe2-125">若要使用多重採樣消除鋸齒，所有已繫結的轉譯目標及深度緩衝區都必須要有相同的樣本數量。</span><span class="sxs-lookup"><span data-stu-id="72fe2-125">If multisample antialiasing is used, all bound render targets and depth buffers must have the same sample counts.</span></span>

<span data-ttu-id="72fe2-126">當緩衝區作為轉譯目標使用時，則不支援深度樣板測試和多重轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="72fe2-126">When a buffer is used as a render target, depth-stencil testing and multiple render targets are not supported.</span></span>

-   <span data-ttu-id="72fe2-127">最多可以同時繫結 8 個轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="72fe2-127">As many as 8 render targets can be bound simultaneously.</span></span>
-   <span data-ttu-id="72fe2-128">所有的呈現目標在所有維度中都必須具有相同的大小 (寬度和高度，以及 \*) 陣列類型的3d 或陣列大小的深度。</span><span class="sxs-lookup"><span data-stu-id="72fe2-128">All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for \*Array types).</span></span>
-   <span data-ttu-id="72fe2-129">各個轉譯目標可能會有不同的資料格式。</span><span class="sxs-lookup"><span data-stu-id="72fe2-129">Each render target may have a different data format.</span></span>
-   <span data-ttu-id="72fe2-130">寫入遮罩可用來控制將寫入轉譯目標的資料。</span><span class="sxs-lookup"><span data-stu-id="72fe2-130">Write masks control what data gets written to a render target.</span></span> <span data-ttu-id="72fe2-131">輸出寫入遮罩可根據每個轉譯目標及每個元件，控制將寫入轉譯目標的資料。</span><span class="sxs-lookup"><span data-stu-id="72fe2-131">The output write masks control on a per-render target, per-component level what data gets written to the render target(s).</span></span>

## <a name="advanced-stencil-techniques"></a><span data-ttu-id="72fe2-132">進階樣板技術</span><span class="sxs-lookup"><span data-stu-id="72fe2-132">Advanced Stencil Techniques</span></span>

<span data-ttu-id="72fe2-133">深度樣板緩衝區的樣板部分可用於建立轉譯效果，例如：合成、印花，以及外框。</span><span class="sxs-lookup"><span data-stu-id="72fe2-133">The stencil portion of the depth-stencil buffer can be used for creating rendering effects such as compositing, decaling, and outlining.</span></span>

-   [<span data-ttu-id="72fe2-134">合成</span><span class="sxs-lookup"><span data-stu-id="72fe2-134">Compositing</span></span>](#compositing)
-   [<span data-ttu-id="72fe2-135">Decaling</span><span class="sxs-lookup"><span data-stu-id="72fe2-135">Decaling</span></span>](#decaling)
-   [<span data-ttu-id="72fe2-136">大綱和 Silhouettes</span><span class="sxs-lookup"><span data-stu-id="72fe2-136">Outlines and Silhouettes</span></span>](#outlines-and-silhouettes)
-   [<span data-ttu-id="72fe2-137">雙側範本</span><span class="sxs-lookup"><span data-stu-id="72fe2-137">Two-Sided Stencil</span></span>](#two-sided-stencil)
-   [<span data-ttu-id="72fe2-138">以材質的形式讀取 Depth-Stencil 緩衝區</span><span class="sxs-lookup"><span data-stu-id="72fe2-138">Reading the Depth-Stencil Buffer as a Texture</span></span>](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a><span data-ttu-id="72fe2-139">合成</span><span class="sxs-lookup"><span data-stu-id="72fe2-139">Compositing</span></span>

<span data-ttu-id="72fe2-140">您的應用程式可利用樣板緩衝區將 2D 或 3D 影像合成為 3D 場景。</span><span class="sxs-lookup"><span data-stu-id="72fe2-140">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="72fe2-141">樣板緩衝區中的遮罩可用於遮蔽轉譯目標的部分表面區域。</span><span class="sxs-lookup"><span data-stu-id="72fe2-141">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="72fe2-142">儲存的 2D 資訊 (例如文字或點陣圖) 接著便可寫入遮蔽區域。</span><span class="sxs-lookup"><span data-stu-id="72fe2-142">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="72fe2-143">或者，您的應用程式也可將其他 3D 原始物件轉譯至轉譯目標表面的樣板遮蔽區域。</span><span class="sxs-lookup"><span data-stu-id="72fe2-143">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="72fe2-144">甚至可以轉譯整個場景。</span><span class="sxs-lookup"><span data-stu-id="72fe2-144">It can even render an entire scene.</span></span>

<span data-ttu-id="72fe2-145">通常，遊戲會將多個 3D 場景合成在一起。</span><span class="sxs-lookup"><span data-stu-id="72fe2-145">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="72fe2-146">例如：競速遊戲通常都會顯示後照鏡。</span><span class="sxs-lookup"><span data-stu-id="72fe2-146">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="72fe2-147">後照鏡便包含了駕駛後方的 3D 場景。</span><span class="sxs-lookup"><span data-stu-id="72fe2-147">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="72fe2-148">該檢視基本上就是合成於駕駛前方檢視的第二個 3D 場景。</span><span class="sxs-lookup"><span data-stu-id="72fe2-148">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

### <a name="decaling"></a><span data-ttu-id="72fe2-149">印花</span><span class="sxs-lookup"><span data-stu-id="72fe2-149">Decaling</span></span>

<span data-ttu-id="72fe2-150">Direct3D 應用程式使用印花來控制從特定原始影像繪製到轉譯目標表面上的像素。</span><span class="sxs-lookup"><span data-stu-id="72fe2-150">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="72fe2-151">應用程式將印花套用至原始物件的影像，以正確地轉譯共面多邊形。</span><span class="sxs-lookup"><span data-stu-id="72fe2-151">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="72fe2-152">例如：將輪胎標記及黃線畫上道路之後，標記應該要直接出現在道路上方。</span><span class="sxs-lookup"><span data-stu-id="72fe2-152">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="72fe2-153">但是，標記和道路的 z 值是相同的。</span><span class="sxs-lookup"><span data-stu-id="72fe2-153">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="72fe2-154">因此，深度緩衝區不一定會在這兩者之間正常分離。</span><span class="sxs-lookup"><span data-stu-id="72fe2-154">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="72fe2-155">某些後方原始物件的像素可能會轉譯至前方原始物件的上方，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="72fe2-155">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="72fe2-156">產生的影像似乎在影格間不斷閃爍。</span><span class="sxs-lookup"><span data-stu-id="72fe2-156">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="72fe2-157">此效果稱為「z 衝突」或「影格閃爍」。</span><span class="sxs-lookup"><span data-stu-id="72fe2-157">This effect is called z-fighting or flimmering.</span></span>

<span data-ttu-id="72fe2-158">若要解決這個問題，可使用樣板將後方原始物件上印花出現的區域遮蔽。</span><span class="sxs-lookup"><span data-stu-id="72fe2-158">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="72fe2-159">關閉 z 緩衝，並將前方原始物件的影像轉譯至轉譯目標表面上已被遮蔽的區域。</span><span class="sxs-lookup"><span data-stu-id="72fe2-159">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="72fe2-160">多重紋理混合可用於解決此問題。</span><span class="sxs-lookup"><span data-stu-id="72fe2-160">Multiple texture blending can be used to solve this problem.</span></span>

### <a name="outlines-and-silhouettes"></a><span data-ttu-id="72fe2-161">外框及剪影</span><span class="sxs-lookup"><span data-stu-id="72fe2-161">Outlines and Silhouettes</span></span>

<span data-ttu-id="72fe2-162">您可以利用樣板緩衝區以獲得更抽象的效果，例如：外框及剪影。</span><span class="sxs-lookup"><span data-stu-id="72fe2-162">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="72fe2-163">如果您的應用程式進行了二階段的轉譯 (第一階段產生樣板遮罩，並於第二階段在原始物件稍微變小之後，將樣板遮罩套用至影像)，產生的影像可能只會包含原始物件的外框。</span><span class="sxs-lookup"><span data-stu-id="72fe2-163">If your application does two render passes - one to generate the stencil mask and second to apply the stencil mask to the image, but with the primitives slightly smaller on the second pass - the resulting image will contain only the primitive's outline.</span></span> <span data-ttu-id="72fe2-164">應用程式可以再以單色填滿影像中被樣板遮蔽的區域，給予原始物件浮凸的外觀。</span><span class="sxs-lookup"><span data-stu-id="72fe2-164">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="72fe2-165">如果樣板遮罩的大小及形狀與您正在轉譯的原始物件相同，產出的影像將會在原先原始物件所在的位置留下一個洞。</span><span class="sxs-lookup"><span data-stu-id="72fe2-165">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="72fe2-166">您的應用程式可以再以黑色填滿該空洞，產生原始物件的剪影效果。</span><span class="sxs-lookup"><span data-stu-id="72fe2-166">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

### <a name="two-sided-stencil"></a><span data-ttu-id="72fe2-167">雙面樣板</span><span class="sxs-lookup"><span data-stu-id="72fe2-167">Two-Sided Stencil</span></span>

<span data-ttu-id="72fe2-168">利用樣板緩衝區繪製陰影時將會使用到陰影錐。</span><span class="sxs-lookup"><span data-stu-id="72fe2-168">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="72fe2-169">應用程式透過計算剪影的邊緣，將其往光源的反方向突出並形成一組 3D 體積的集合，進而計算遮蔽幾何物的陰影錐。</span><span class="sxs-lookup"><span data-stu-id="72fe2-169">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="72fe2-170">這些物體接著會在經過兩次的轉譯之後寫入樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="72fe2-170">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="72fe2-171">第一次轉譯會繪製面向前端的多邊形，並遞增樣板緩衝區的值。</span><span class="sxs-lookup"><span data-stu-id="72fe2-171">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="72fe2-172">第二次轉譯會繪製陰影錐面向後端的多邊形，並遞減樣板緩衝區的值。</span><span class="sxs-lookup"><span data-stu-id="72fe2-172">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="72fe2-173">一般而言，所有遞增及遞減的值會互相抵銷。不過，當陰影錐被轉譯時，場景已經在一般幾何導致某些像素無法通過 z 衝突測試時轉譯完成。</span><span class="sxs-lookup"><span data-stu-id="72fe2-173">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="72fe2-174">留在樣板緩衝區的值將會對應到陰影中的像素。</span><span class="sxs-lookup"><span data-stu-id="72fe2-174">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="72fe2-175">這些剩餘的樣板緩衝區內容會作為遮罩使用，以將一個包括所有內容的巨大黑色四元組 Alpha 混合至場景中。</span><span class="sxs-lookup"><span data-stu-id="72fe2-175">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="72fe2-176">藉由將樣板緩衝區作為遮罩，陰影中的像素將會進一步加深。</span><span class="sxs-lookup"><span data-stu-id="72fe2-176">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="72fe2-177">這表示針對每個光源，陰影幾何都會繪製兩次，因此對 GPU 的頂點輸送量形成了壓力。</span><span class="sxs-lookup"><span data-stu-id="72fe2-177">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="72fe2-178">雙面樣板便是為了避免這種情況而設計出來的功能。</span><span class="sxs-lookup"><span data-stu-id="72fe2-178">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="72fe2-179">在這種方法之下，會有兩組樣板狀態 (命名如下)：其中一組為針對每個面向前端的三角形設定的樣板狀態，另外一組則是針對面向後端的三角形。</span><span class="sxs-lookup"><span data-stu-id="72fe2-179">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="72fe2-180">如此一來，針對每個光源及每個陰影錐都只會進行一階段的繪製。</span><span class="sxs-lookup"><span data-stu-id="72fe2-180">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="72fe2-181">您可以在 [ShadowVolume10 範例](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)中找到兩個邊樣板執行的範例。</span><span class="sxs-lookup"><span data-stu-id="72fe2-181">An example of two-sided stencil implementation can be found in the [ShadowVolume10 Sample](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span></span>

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a><span data-ttu-id="72fe2-182">讀取深度樣板緩衝區作為紋理</span><span class="sxs-lookup"><span data-stu-id="72fe2-182">Reading the Depth-Stencil Buffer as a Texture</span></span>

<span data-ttu-id="72fe2-183">非使用中的深度樣板緩衝區可由著色器作為紋理讀取。</span><span class="sxs-lookup"><span data-stu-id="72fe2-183">An inactive depth-stencil buffer can be read by a shader as a texture.</span></span> <span data-ttu-id="72fe2-184">讀取深度樣板緩衝區作為紋理的應用程式，將會進行二階段的轉譯：在第一階段寫入深度樣板緩衝區，並於第二階段從緩衝區中讀取。</span><span class="sxs-lookup"><span data-stu-id="72fe2-184">An application that reads a depth-stencil buffer as a texture renders in two passes, the first pass writes to the depth-stencil buffer and the second pass reads from the buffer.</span></span> <span data-ttu-id="72fe2-185">這可以讓著色器將先前寫入緩衝區的深度值或樣板值，與目前轉譯中像素的值互相比較。</span><span class="sxs-lookup"><span data-stu-id="72fe2-185">This allows a shader to compare depth or stencil values previously written to the buffer against the value for the pixel currrently being rendered.</span></span> <span data-ttu-id="72fe2-186">比較的結果可用來建立效果，例如陰影貼圖或粒子系統中的軟粒子。</span><span class="sxs-lookup"><span data-stu-id="72fe2-186">The result of the comparison can be used to create effects such as shadow mapping or soft particles in a particle system.</span></span>

<span data-ttu-id="72fe2-187">若要建立可做為深度樣板資源和著色器資源的深度樣板緩衝區，必須對 [ [建立 Depth-Stencil 資源](#create-a-depth-stencil-resource) ] 區段中的範例程式碼進行一些變更。</span><span class="sxs-lookup"><span data-stu-id="72fe2-187">To create a depth-stencil buffer that can be used as both a depth-stencil resource and a shader resource a few changes need to be made to sample code in the [Create a Depth-Stencil Resource](#create-a-depth-stencil-resource) section.</span></span>

-   <span data-ttu-id="72fe2-188">深度樣板資源必須有不具格式的格式，例如 DXGI \_ 格式 R32 無型別 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="72fe2-188">The depth-stencil resource must have a typeless format such as DXGI\_FORMAT\_R32\_TYPELESS.</span></span>
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   <span data-ttu-id="72fe2-189">深度樣板資源必須同時使用 D3D10 系結 \_ 深度樣板 \_ 和 D3D10 系結 \_ \_ \_ 著色器資源系結 \_ 旗標。</span><span class="sxs-lookup"><span data-stu-id="72fe2-189">The depth-stencil resource must use both the D3D10\_BIND\_DEPTH\_STENCIL and D3D10\_BIND\_SHADER\_RESOURCE bind flags.</span></span>
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

<span data-ttu-id="72fe2-190">此外，您必須使用 [**D3D11 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) 結構和 [**ID3D11Device：： CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)，為深度緩衝區建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="72fe2-190">In addition a shader resource view needs to be created for the depth buffer using a [**D3D11\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) structure and [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span></span> <span data-ttu-id="72fe2-191">著色器資源檢視會使用具類型的格式，例如 **DXGI \_ 格式 \_ R32 \_ FLOAT** ，這相當於建立深度樣板資源時所指定的無類型格式。</span><span class="sxs-lookup"><span data-stu-id="72fe2-191">The shader resource view will use a typed format such as **DXGI\_FORMAT\_R32\_FLOAT** that is the equivalent to the typeless format specified when the depth-stencil resource was created.</span></span>

<span data-ttu-id="72fe2-192">在第一次轉譯階段中，深度緩衝區系結，如將 [Depth-Stencil 資料系結至 OM 階段](#bind-depth-stencil-data-to-the-om-stage) 一節中所述。</span><span class="sxs-lookup"><span data-stu-id="72fe2-192">In the first render pass the depth buffer is bound as described in the [Bind Depth-Stencil Data to the OM Stage](#bind-depth-stencil-data-to-the-om-stage) section.</span></span> <span data-ttu-id="72fe2-193">請注意，傳遞至 [**D3D11 \_ 深度樣板 \_ \_ 視圖 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)的格式。格式會使用具類型的格式，例如 **DXGI \_ 格式 \_ D32 \_ FLOAT**。</span><span class="sxs-lookup"><span data-stu-id="72fe2-193">Note that the format passed to [**D3D11\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc).Format will use a typed format such as **DXGI\_FORMAT\_D32\_FLOAT**.</span></span> <span data-ttu-id="72fe2-194">第一次轉譯階段之後，深度緩衝區將包含場景的深度值。</span><span class="sxs-lookup"><span data-stu-id="72fe2-194">After the first render pass the depth buffer will contain the depth values for the scene.</span></span>

<span data-ttu-id="72fe2-195">在第二個轉譯階段中， [**>id3d11devicecoNtext：： OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) 函式是用來將深度樣板視圖設定為 **Null** 或不同的深度樣板資源，而著色器資源檢視會使用 [**ID3D11EffectShaderResourceVariable：： SetResource**](id3dx11effectshaderresourcevariable-setresource.md)傳遞給著色器。</span><span class="sxs-lookup"><span data-stu-id="72fe2-195">In the second render pass the [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) function is used to set the depth-stencil view to **NULL** or a different depth-stencil resource and the shader resource view is passed to the shader using [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span></span> <span data-ttu-id="72fe2-196">這可讓著色器查詢第一次轉譯行程中計算出的深度值。</span><span class="sxs-lookup"><span data-stu-id="72fe2-196">This allows the shader to look up the depth values calculated in the first rendering pass.</span></span> <span data-ttu-id="72fe2-197">請注意，如果第一次轉譯傳遞的觀點與第二個轉譯行程不同，則必須套用轉換來取得深度值。</span><span class="sxs-lookup"><span data-stu-id="72fe2-197">Note that a transformation will need to be applied to retrieve depth values if the point of view of the first render pass is different from the second render pass.</span></span> <span data-ttu-id="72fe2-198">例如，如果使用陰影對應技術，則第一次轉譯階段會從光源的角度來看，而第二次轉譯階段則是從檢視器的觀點來看。</span><span class="sxs-lookup"><span data-stu-id="72fe2-198">For example, if a shadow mapping technique is being used the first render pass will be from the perspective of a light source while the second render pass will from the viewer's perspective.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72fe2-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="72fe2-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72fe2-200">輸出合併階段</span><span class="sxs-lookup"><span data-stu-id="72fe2-200">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="72fe2-201"> (Direct3D 10) 的管線階段 </span><span class="sxs-lookup"><span data-stu-id="72fe2-201">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 