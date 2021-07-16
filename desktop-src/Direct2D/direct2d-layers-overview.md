---
title: 圖層總覽
description: 描述 Direct2D 圖層的基本概念。
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D，圖層
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 027be097c5c21929f3ccdbaa169a1f3dac55b394
ms.sourcegitcommit: 698ce2d9ba2fa650f2875225d99623995fac246a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/15/2021
ms.locfileid: "114231605"
---
# <a name="layers-overview"></a><span data-ttu-id="d71c3-104">圖層總覽</span><span class="sxs-lookup"><span data-stu-id="d71c3-104">Layers Overview</span></span>

<span data-ttu-id="d71c3-105">本總覽說明使用 Direct2D 層的基本概念。</span><span class="sxs-lookup"><span data-stu-id="d71c3-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="d71c3-106">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="d71c3-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="d71c3-107">什麼是圖層？</span><span class="sxs-lookup"><span data-stu-id="d71c3-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="d71c3-108">Windows 8 和更新版本中的圖層</span><span class="sxs-lookup"><span data-stu-id="d71c3-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="d71c3-109">ID2D1DeviceCoNtext 和 PushLayer</span><span class="sxs-lookup"><span data-stu-id="d71c3-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="d71c3-110">D2D1 \_ 圖層 \_ PARAMETERS1 和 D2D1 \_ 圖層 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="d71c3-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="d71c3-111">混合模式</span><span class="sxs-lookup"><span data-stu-id="d71c3-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="d71c3-112">相互</span><span class="sxs-lookup"><span data-stu-id="d71c3-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="d71c3-113">建立圖層</span><span class="sxs-lookup"><span data-stu-id="d71c3-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="d71c3-114">內容界限</span><span class="sxs-lookup"><span data-stu-id="d71c3-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="d71c3-115">幾何遮罩</span><span class="sxs-lookup"><span data-stu-id="d71c3-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="d71c3-116">不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="d71c3-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="d71c3-117">圖層的替代專案</span><span class="sxs-lookup"><span data-stu-id="d71c3-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="d71c3-118">裁剪任意圖形</span><span class="sxs-lookup"><span data-stu-id="d71c3-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="d71c3-119">軸對齊的剪輯</span><span class="sxs-lookup"><span data-stu-id="d71c3-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="d71c3-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="d71c3-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="d71c3-121">什麼是圖層？</span><span class="sxs-lookup"><span data-stu-id="d71c3-121">What Are Layers?</span></span>

<span data-ttu-id="d71c3-122">以 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 物件表示的圖層，可讓應用程式操作一組繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="d71c3-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="d71c3-123">您可以使用圖層，將它「推送」到轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="d71c3-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="d71c3-124">轉譯目標的後續繪圖作業會導向至圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="d71c3-125">當您完成圖層之後，您會從呈現目標「快顯」圖層，將圖層的內容合成回轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="d71c3-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="d71c3-126">和筆刷一樣，圖層是由呈現目標所建立的裝置相依資源。</span><span class="sxs-lookup"><span data-stu-id="d71c3-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="d71c3-127">您可以在包含建立它之轉譯目標所在的相同資源網域中的任何轉譯目標上使用圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="d71c3-128">不過，一次只能有一個呈現目標使用的圖層資源。</span><span class="sxs-lookup"><span data-stu-id="d71c3-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="d71c3-129">如需資源的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。</span><span class="sxs-lookup"><span data-stu-id="d71c3-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="d71c3-130">雖然圖層提供了功能強大的轉譯技術來產生有趣的效果，但應用程式中的圖層數量過多可能會對其效能造成負面影響，因為與管理圖層和分層資源相關聯的成本各有不同。</span><span class="sxs-lookup"><span data-stu-id="d71c3-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="d71c3-131">例如，填滿或清除圖層，然後再將它混合回來（尤其是在高階硬體上）的成本。</span><span class="sxs-lookup"><span data-stu-id="d71c3-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="d71c3-132">然後，會有管理層資源的成本。</span><span class="sxs-lookup"><span data-stu-id="d71c3-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="d71c3-133">如果您經常重新配置這些，產生的 GPU 將會是最重要的問題。</span><span class="sxs-lookup"><span data-stu-id="d71c3-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="d71c3-134">當您設計您的應用程式時，請嘗試最大化重複使用圖層資源。</span><span class="sxs-lookup"><span data-stu-id="d71c3-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="d71c3-135">Windows 8 和更新版本中的圖層</span><span class="sxs-lookup"><span data-stu-id="d71c3-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="d71c3-136">Windows 8 引進了新的分層相關 api，可簡化、改善的效能，並將功能新增至圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="d71c3-137">ID2D1DeviceCoNtext 和 PushLayer</span><span class="sxs-lookup"><span data-stu-id="d71c3-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="d71c3-138">[**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面衍生自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)介面，也是在 Windows 8 中顯示 Direct2D 內容的關鍵。如需此介面的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md)內容。</span><span class="sxs-lookup"><span data-stu-id="d71c3-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="d71c3-139">您可以使用裝置內容介面略過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 方法，然後將 Null 傳遞至 [**ID2D1DeviceCoNtext：:P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 方法。</span><span class="sxs-lookup"><span data-stu-id="d71c3-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="d71c3-140">Direct2D 會自動管理圖層資源，並可在圖層和效果圖形之間共用資源。</span><span class="sxs-lookup"><span data-stu-id="d71c3-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="d71c3-141">D2D1 \_ 圖層 \_ PARAMETERS1 和 D2D1 \_ 圖層 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="d71c3-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="d71c3-142">[**D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1)結構與 [**D2D1 圖層 \_ \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)相同，不同之處在于結構的最後一個成員現在是 [**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)列舉。</span><span class="sxs-lookup"><span data-stu-id="d71c3-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="d71c3-143">[**D2D1 \_圖層 \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) 沒有 ClearType 選項，有兩個不同的選項可讓您用來改善效能：</span><span class="sxs-lookup"><span data-stu-id="d71c3-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="d71c3-144">[**D2D1 \_圖 \_ 層 \_ OPTIONS1 \_ 從 \_ 背景初始化**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)： Direct2D 會將基本專案轉譯為圖層，而不會以透明黑色將其清除。</span><span class="sxs-lookup"><span data-stu-id="d71c3-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="d71c3-145">這並不是預設值，但在大部分情況下，會產生較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="d71c3-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="d71c3-146">[**D2D1 \_圖層 \_ OPTIONS1 \_ 忽略 \_ Alpha**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)：如果基礎介面設定為 [**D2D1 \_ ALPHA \_ 模式 \_ 忽略**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)，此選項可讓 Direct2D 避免修改圖層的 ALPHA 色板。</span><span class="sxs-lookup"><span data-stu-id="d71c3-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="d71c3-147">在其他情況下請勿使用此功能。</span><span class="sxs-lookup"><span data-stu-id="d71c3-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="d71c3-148">混合模式</span><span class="sxs-lookup"><span data-stu-id="d71c3-148">Blend Modes</span></span>

<span data-ttu-id="d71c3-149">從 Windows 8 開始，裝置內容具有 [**基本 blend 模式**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)，可決定每個基本類型如何與目標介面混合。</span><span class="sxs-lookup"><span data-stu-id="d71c3-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="d71c3-150">當您呼叫 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 方法時，這個模式也適用于圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="d71c3-151">例如，如果您使用圖層來裁剪具有透明度的基本專案，請在裝置內容上設定 [**D2D1 \_ 基本 \_ BLEND \_ 複製**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) 模式，以取得適當的結果。</span><span class="sxs-lookup"><span data-stu-id="d71c3-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="d71c3-152">複製模式會根據圖層的幾何遮罩，讓裝置內容線性將所有4色通道（包括 Alpha 色板）插補，其中每個圖元都有目標介面的內容。</span><span class="sxs-lookup"><span data-stu-id="d71c3-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="d71c3-153">互通</span><span class="sxs-lookup"><span data-stu-id="d71c3-153">Interoperation</span></span>

<span data-ttu-id="d71c3-154">從 Windows 8 開始，Direct2D 支援在推送圖層或剪輯時，與 Direct3D 和 GDI 交互操作。</span><span class="sxs-lookup"><span data-stu-id="d71c3-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="d71c3-155">您可以呼叫 [**ID2D1GdiInteropRenderTarget：： GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) ，同時將圖層推送至與 GDI 相交互操作。</span><span class="sxs-lookup"><span data-stu-id="d71c3-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="d71c3-156">您可以呼叫 [**ID2D1DeviceCoNtext：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) ，然後轉譯至基礎介面，以與 Direct3D 交互操作。</span><span class="sxs-lookup"><span data-stu-id="d71c3-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="d71c3-157">使用 Direct3D 或 GDI 在圖層或剪輯內轉譯是您的責任。</span><span class="sxs-lookup"><span data-stu-id="d71c3-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="d71c3-158">如果您嘗試在圖層或剪輯之外轉譯，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="d71c3-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="d71c3-159">建立圖層</span><span class="sxs-lookup"><span data-stu-id="d71c3-159">Creating Layers</span></span>

<span data-ttu-id="d71c3-160">使用圖層需要熟悉 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))、 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 方法，以及 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) 結構，其中包含一組可定義如何使用圖層的參數化資料。</span><span class="sxs-lookup"><span data-stu-id="d71c3-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="d71c3-161">下列清單描述方法和結構。</span><span class="sxs-lookup"><span data-stu-id="d71c3-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="d71c3-162">呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 方法來建立圖層資源。</span><span class="sxs-lookup"><span data-stu-id="d71c3-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="d71c3-163">從 Windows 8 開始，您可以略過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))方法，然後在 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面上將 Null 傳遞至 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))方法。</span><span class="sxs-lookup"><span data-stu-id="d71c3-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="d71c3-164">這比較簡單，而且可讓 Direct2D 自動管理圖層資源，以及在圖層和效果圖形之間共用資源。</span><span class="sxs-lookup"><span data-stu-id="d71c3-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="d71c3-165">當轉譯目標在呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法之後，開始繪製 () 之後，您就可以使用 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 方法。</span><span class="sxs-lookup"><span data-stu-id="d71c3-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="d71c3-166">**PushLayer** 方法會將指定的圖層加入至轉譯目標，讓目標接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)為止。</span><span class="sxs-lookup"><span data-stu-id="d71c3-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="d71c3-167">這個方法會透過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))和 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構中的 *layerParameters* ，來取得傳回的 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)物件。</span><span class="sxs-lookup"><span data-stu-id="d71c3-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="d71c3-168">下表描述結構的欄位。</span><span class="sxs-lookup"><span data-stu-id="d71c3-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="d71c3-169">欄位</span><span class="sxs-lookup"><span data-stu-id="d71c3-169">Field</span></span>                 | <span data-ttu-id="d71c3-170">描述</span><span class="sxs-lookup"><span data-stu-id="d71c3-170">Description</span></span>|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d71c3-171">**contentBounds**</span><span class="sxs-lookup"><span data-stu-id="d71c3-171">**contentBounds**</span></span>     | <span data-ttu-id="d71c3-172">圖層的內容界限。</span><span class="sxs-lookup"><span data-stu-id="d71c3-172">The content bounds of the layer.</span></span> <span data-ttu-id="d71c3-173">內容不會在這些界限之外轉譯。</span><span class="sxs-lookup"><span data-stu-id="d71c3-173">Content won't render outside these bounds.</span></span> <span data-ttu-id="d71c3-174">此參數的預設值為 [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)。</span><span class="sxs-lookup"><span data-stu-id="d71c3-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="d71c3-175">使用預設值時，內容界限實際上會被視為呈現目標的界限。</span><span class="sxs-lookup"><span data-stu-id="d71c3-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |
    | <span data-ttu-id="d71c3-176">**geometricMask**</span><span class="sxs-lookup"><span data-stu-id="d71c3-176">**geometricMask**</span></span>     | <span data-ttu-id="d71c3-177"> (選擇性的) 區域（由 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)定義），應將該圖層裁剪至該區域。</span><span class="sxs-lookup"><span data-stu-id="d71c3-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="d71c3-178">如果不應該將圖層裁剪成幾何，請設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d71c3-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span> |
    | <span data-ttu-id="d71c3-179">**maskAntialiasMode**</span><span class="sxs-lookup"><span data-stu-id="d71c3-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="d71c3-180">值，指定 **geometricMask** 欄位所指定之幾何遮罩的消除鋸齒模式。</span><span class="sxs-lookup"><span data-stu-id="d71c3-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span> |
    | <span data-ttu-id="d71c3-181">**maskTransform**</span><span class="sxs-lookup"><span data-stu-id="d71c3-181">**maskTransform**</span></span>     | <span data-ttu-id="d71c3-182">值，指定在組合圖層時，套用至幾何遮罩的轉換。</span><span class="sxs-lookup"><span data-stu-id="d71c3-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="d71c3-183">這是與世界轉換相關的。</span><span class="sxs-lookup"><span data-stu-id="d71c3-183">This is relative to the world transform.</span></span>  |
    | <span data-ttu-id="d71c3-184">**透明度**</span><span class="sxs-lookup"><span data-stu-id="d71c3-184">**opacity**</span></span>           | <span data-ttu-id="d71c3-185">圖層的不透明度值。</span><span class="sxs-lookup"><span data-stu-id="d71c3-185">The opacity value of the layer.</span></span> <span data-ttu-id="d71c3-186">當對目標進行組合時，圖層中每個資源的不透明度會乘以此值。</span><span class="sxs-lookup"><span data-stu-id="d71c3-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>  |
    | <span data-ttu-id="d71c3-187">**opacityBrush**</span><span class="sxs-lookup"><span data-stu-id="d71c3-187">**opacityBrush**</span></span>      | <span data-ttu-id="d71c3-188"> (選擇性) 用來修改圖層不透明度的筆刷。</span><span class="sxs-lookup"><span data-stu-id="d71c3-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="d71c3-189">筆刷會對應到圖層，而每個對應筆刷圖元的 Alpha 色板會乘以對應的圖層圖元。</span><span class="sxs-lookup"><span data-stu-id="d71c3-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="d71c3-190">如果圖層不應有不透明度遮罩，則設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d71c3-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>   |
    | <span data-ttu-id="d71c3-191">**layerOptions**</span><span class="sxs-lookup"><span data-stu-id="d71c3-191">**layerOptions**</span></span>      | <span data-ttu-id="d71c3-192">值，指定圖層是否打算以 ClearType 消除鋸齒來呈現文字。</span><span class="sxs-lookup"><span data-stu-id="d71c3-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="d71c3-193">此參數預設為 off。</span><span class="sxs-lookup"><span data-stu-id="d71c3-193">This parameter defaults to off.</span></span> <span data-ttu-id="d71c3-194">開啟它可讓 ClearType 正常運作，但會產生稍微慢的轉譯速度。</span><span class="sxs-lookup"><span data-stu-id="d71c3-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>    |

    

     

    > [!Note]  
    > <span data-ttu-id="d71c3-195">從 Windows 8 開始，您無法在圖層中以 ClearType 轉譯，因此 **layerOptions** 參數應一律設定為 [**D2D1 \_ 圖層 \_ 選項 \_ NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span><span class="sxs-lookup"><span data-stu-id="d71c3-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="d71c3-196">為了方便起見，Direct2D 提供 [**D2D1：： LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) 方法，以協助您建立 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) 結構。</span><span class="sxs-lookup"><span data-stu-id="d71c3-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="d71c3-197">若要將圖層的內容複合到轉譯目標中，請呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 方法。</span><span class="sxs-lookup"><span data-stu-id="d71c3-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="d71c3-198">在呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)方法之前，您必須先呼叫 **PopLayer** 方法。</span><span class="sxs-lookup"><span data-stu-id="d71c3-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="d71c3-199">下列範例顯示如何使用 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))、 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)。</span><span class="sxs-lookup"><span data-stu-id="d71c3-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="d71c3-200">[**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構中的所有欄位都會設定為其預設值，但 **opacityBrush** 會設定為 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)。</span><span class="sxs-lookup"><span data-stu-id="d71c3-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



<span data-ttu-id="d71c3-201">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="d71c3-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="d71c3-202">請注意，當您呼叫 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)時，請確定每個 **PushLayer** 都有相符的 **PopLayer** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d71c3-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="d71c3-203">如果有比 **PushLayer** 呼叫更多的 **PopLayer** 呼叫，轉譯目標會置於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="d71c3-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="d71c3-204">如果在所有未處理的層上取出之前呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) ，轉譯目標會進入錯誤狀態，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d71c3-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="d71c3-205">若要清除錯誤狀態，請使用 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)。</span><span class="sxs-lookup"><span data-stu-id="d71c3-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="d71c3-206">內容界限</span><span class="sxs-lookup"><span data-stu-id="d71c3-206">Content Bounds</span></span>

<span data-ttu-id="d71c3-207">**ContentBounds** 會設定要繪製至圖層的限制。</span><span class="sxs-lookup"><span data-stu-id="d71c3-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="d71c3-208">只有內容界限內的專案會呈現回轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="d71c3-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="d71c3-209">接下來的範例會示範如何指定 **contentBounds** ，以便將原始影像裁剪至左上角的內容界限， (10，108) ，而右下角 (121，177) 。</span><span class="sxs-lookup"><span data-stu-id="d71c3-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="d71c3-210">下圖顯示將影像裁剪至內容界限的原始影像和結果。</span><span class="sxs-lookup"><span data-stu-id="d71c3-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![原始圖片上的內容界限圖例和產生的裁剪圖片](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="d71c3-212">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="d71c3-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="d71c3-213">如果您指定 **geometricMask**，則會進一步影響產生的裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="d71c3-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="d71c3-214">如需詳細資訊，請參閱「 [幾何遮罩](#geometric-masks) 」一節。</span><span class="sxs-lookup"><span data-stu-id="d71c3-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="d71c3-215">幾何遮罩</span><span class="sxs-lookup"><span data-stu-id="d71c3-215">Geometric Masks</span></span>

<span data-ttu-id="d71c3-216">幾何遮罩是由 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件所定義的剪輯或裁剪，可在呈現目標繪製圖層時遮罩圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="d71c3-217">您可以使用 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構的 **geometricMask** 欄位，將結果遮罩到幾何。</span><span class="sxs-lookup"><span data-stu-id="d71c3-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="d71c3-218">例如，如果您想要顯示由區塊字母 "A" 遮罩的影像，您可以先建立代表封鎖字母 "A" 的幾何，然後使用該幾何作為圖層的幾何遮罩。</span><span class="sxs-lookup"><span data-stu-id="d71c3-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="d71c3-219">然後，在推送圖層之後，您就可以繪製影像。</span><span class="sxs-lookup"><span data-stu-id="d71c3-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="d71c3-220">快顯圖層會導致影像裁剪成封鎖字母「A」圖形。</span><span class="sxs-lookup"><span data-stu-id="d71c3-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="d71c3-221">接下來的範例顯示如何建立包含山區圖形的 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) ，然後將路徑幾何傳遞給 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))。</span><span class="sxs-lookup"><span data-stu-id="d71c3-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="d71c3-222">然後繪製點陣圖和方塊。</span><span class="sxs-lookup"><span data-stu-id="d71c3-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="d71c3-223">如果要轉譯的圖層中只有一個點陣圖，請使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 搭配壓制點陣圖筆刷來提高效率。</span><span class="sxs-lookup"><span data-stu-id="d71c3-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="d71c3-224">下圖顯示範例的輸出。</span><span class="sxs-lookup"><span data-stu-id="d71c3-224">The following illustration shows the output from the example.</span></span>

![套用山的幾何遮罩之後，分葉圖片和產生的圖片的圖例](images/layers-bitmapmask.png)

<span data-ttu-id="d71c3-226">第一個範例會定義要當做遮罩使用的幾何。</span><span class="sxs-lookup"><span data-stu-id="d71c3-226">The first example defines the geometry to be used as a mask.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



<span data-ttu-id="d71c3-227">下一個範例會使用 geometry 做為圖層的遮罩。</span><span class="sxs-lookup"><span data-stu-id="d71c3-227">The next example uses the geometry as a mask for the layer.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="d71c3-228">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="d71c3-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="d71c3-229">一般來說，如果您指定 **geometricMask**，您可以使用 **contentBounds** 的預設值 [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)。</span><span class="sxs-lookup"><span data-stu-id="d71c3-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="d71c3-230">如果 **contentBounds** 為 null，而 **GEOMETRICMASK** 為非 null，則在套用遮罩轉換之後，內容界限實際上是幾何遮罩的範圍。</span><span class="sxs-lookup"><span data-stu-id="d71c3-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="d71c3-231">如果 **contentBounds** 為非 null，且 **GEOMETRICMASK** 為非 null，則會有效地針對內容界限裁剪已轉換的幾何遮罩，並假設內容界限是無限的。</span><span class="sxs-lookup"><span data-stu-id="d71c3-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="d71c3-232">不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="d71c3-232">Opacity Masks</span></span>

<span data-ttu-id="d71c3-233">不透明度遮罩是由筆刷或點陣圖描述的遮罩，會套用到另一個物件，使該物件部分或完全透明。</span><span class="sxs-lookup"><span data-stu-id="d71c3-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="d71c3-234">它允許使用筆刷的 Alpha 色板作為內容遮罩。</span><span class="sxs-lookup"><span data-stu-id="d71c3-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="d71c3-235">例如，您可以定義不同于透明的星形漸層筆刷，以建立 vignette 效果。</span><span class="sxs-lookup"><span data-stu-id="d71c3-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="d71c3-236">接下來的範例會使用 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) 作為不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="d71c3-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="d71c3-237">然後繪製點陣圖和方塊。</span><span class="sxs-lookup"><span data-stu-id="d71c3-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="d71c3-238">如果要轉譯的圖層中只有一個點陣圖，請使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 搭配壓制點陣圖筆刷來提高效率。</span><span class="sxs-lookup"><span data-stu-id="d71c3-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="d71c3-239">下圖顯示此範例的輸出。</span><span class="sxs-lookup"><span data-stu-id="d71c3-239">The following illustration shows the output from this example.</span></span>

![套用不透明度遮罩之後的樹狀結構圖片和產生的圖片圖例](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="d71c3-241">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="d71c3-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="d71c3-242">此範例會使用圖層將不透明度遮罩套用至單一物件，讓範例盡可能簡單。</span><span class="sxs-lookup"><span data-stu-id="d71c3-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="d71c3-243">將不透明度遮罩套用至單一物件時，使用 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 或 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法（而非圖層）會更有效率。</span><span class="sxs-lookup"><span data-stu-id="d71c3-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="d71c3-244">如需如何在不使用圖層的情況下套用不透明度遮罩的指示，請參閱 [不透明度遮罩總覽](opacity-masks-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d71c3-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="d71c3-245">圖層的替代專案</span><span class="sxs-lookup"><span data-stu-id="d71c3-245">Alternatives to Layers</span></span>

<span data-ttu-id="d71c3-246">如先前所述，過多的層級可能會對應用程式的效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="d71c3-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="d71c3-247">若要改善效能，請盡可能避免使用圖層;改為使用其替代方案。</span><span class="sxs-lookup"><span data-stu-id="d71c3-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="d71c3-248">下列程式碼範例示範如何使用 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) 和 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) 來裁剪區域，以替代使用具有內容界限的圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="d71c3-249">同樣地，使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 搭配壓制點陣圖筆刷，作為在圖層中只有一個要轉譯的內容時，使用具有不透明度遮罩的圖層的替代方式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="d71c3-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="d71c3-250">除了使用具有幾何遮罩的圖層之外，請考慮使用點陣圖遮罩來裁剪區域，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="d71c3-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="d71c3-251">最後，如果您想要將不透明度套用至單一基本型別，則應該將不透明度乘以至筆刷色彩，然後轉譯基本類型。</span><span class="sxs-lookup"><span data-stu-id="d71c3-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="d71c3-252">您不需要圖層或不透明度遮罩點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d71c3-252">You do not need a layer or an opacity mask bitmap.</span></span>


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="d71c3-253">裁剪任意圖形</span><span class="sxs-lookup"><span data-stu-id="d71c3-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="d71c3-254">這裡的圖顯示將剪輯套用至影像的結果。</span><span class="sxs-lookup"><span data-stu-id="d71c3-254">The figure here shows the result of applying a clip to an image.</span></span>

![顯示剪輯前後影像範例的影像。](images/clip.png)

<span data-ttu-id="d71c3-256">您可以使用具有幾何遮罩的圖層或具有不透明度筆刷的 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法來取得這個結果。</span><span class="sxs-lookup"><span data-stu-id="d71c3-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="d71c3-257">以下是使用圖層的範例：</span><span class="sxs-lookup"><span data-stu-id="d71c3-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="d71c3-258">以下是使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法的範例：</span><span class="sxs-lookup"><span data-stu-id="d71c3-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="d71c3-259">在此程式碼範例中，當您呼叫 PushLayer 方法時，不會傳入應用程式所建立的圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="d71c3-260">Direct2D 會為您建立圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="d71c3-261">Direct2D 可以管理此資源的配置和終結，而不需要應用程式的任何介入。</span><span class="sxs-lookup"><span data-stu-id="d71c3-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="d71c3-262">這可讓 Direct2D 在內部重複使用圖層，並套用資源管理優化。</span><span class="sxs-lookup"><span data-stu-id="d71c3-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="d71c3-263">在 Windows 8 已對層級使用進行許多優化，建議您盡可能嘗試使用層 api，而不是 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 。</span><span class="sxs-lookup"><span data-stu-id="d71c3-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="d71c3-264">軸對齊的剪輯</span><span class="sxs-lookup"><span data-stu-id="d71c3-264">Axis aligned clips</span></span>

<span data-ttu-id="d71c3-265">如果要裁剪的區域對齊繪圖介面的軸，而不是任意的。</span><span class="sxs-lookup"><span data-stu-id="d71c3-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="d71c3-266">此案例適用于使用剪輯矩形而非圖層。</span><span class="sxs-lookup"><span data-stu-id="d71c3-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="d71c3-267">效能提升比反鋸齒幾何的別名幾何更多。</span><span class="sxs-lookup"><span data-stu-id="d71c3-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="d71c3-268">如需軸對齊剪輯的詳細資訊，請參閱 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 主題。</span><span class="sxs-lookup"><span data-stu-id="d71c3-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d71c3-269">相關主題</span><span class="sxs-lookup"><span data-stu-id="d71c3-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d71c3-270">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="d71c3-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 