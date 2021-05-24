---
description: 在 Direct3D 10 中，裝置狀態會分組為狀態物件，以大幅降低狀態變更的成本。
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: " (Direct3D 10) 的狀態物件"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335422"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="4786f-103"> (Direct3D 10) 的狀態物件</span><span class="sxs-lookup"><span data-stu-id="4786f-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="4786f-104">在 Direct3D 10 中，裝置狀態會分組為狀態物件，以大幅降低狀態變更的成本。</span><span class="sxs-lookup"><span data-stu-id="4786f-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="4786f-105">有幾個狀態物件，每個設計成針對特定管線階段初始化一組狀態。</span><span class="sxs-lookup"><span data-stu-id="4786f-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="4786f-106">您最多可以為每種類型的狀態物件建立4096。</span><span class="sxs-lookup"><span data-stu-id="4786f-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="4786f-107">輸入-版面配置狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="4786f-108">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="4786f-109">深度樣板狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="4786f-110">Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="4786f-111">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="4786f-112">效能考量</span><span class="sxs-lookup"><span data-stu-id="4786f-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="4786f-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="4786f-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="4786f-114">輸入配置狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-114">Input-Layout State</span></span>

<span data-ttu-id="4786f-115">這一組狀態 (請參閱 [**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) 指定輸入組合語言 [階段](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) 如何從輸入緩衝區讀取資料，並將它組合供端點著色器使用。</span><span class="sxs-lookup"><span data-stu-id="4786f-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="4786f-116">這包括狀態，例如輸入緩衝區中的元素數目和輸入資料簽章。</span><span class="sxs-lookup"><span data-stu-id="4786f-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="4786f-117">輸入組譯工具階段是管線中的新階段，其工作是將記憶體中的基本串流串流至管線。</span><span class="sxs-lookup"><span data-stu-id="4786f-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="4786f-118">若要建立輸入版面配置狀態物件，請參閱 [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)。</span><span class="sxs-lookup"><span data-stu-id="4786f-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="4786f-119">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-119">Rasterizer State</span></span>

<span data-ttu-id="4786f-120">此狀態群組 (查看 D3D10 轉譯器 [**\_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) 初始化轉譯器 [階段](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md)。</span><span class="sxs-lookup"><span data-stu-id="4786f-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="4786f-121">此物件包含填滿或揀選 (Cull) 模式、啟用剪式矩形裁剪和設定多重樣本參數等狀態。</span><span class="sxs-lookup"><span data-stu-id="4786f-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="4786f-122">這個階段會將基本類型點陣化成像素，執行像是裁剪及對應基本類型到檢視區等作業。</span><span class="sxs-lookup"><span data-stu-id="4786f-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="4786f-123">若要建立轉譯器狀態物件，請參閱 [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)。</span><span class="sxs-lookup"><span data-stu-id="4786f-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="4786f-124">深度樣板狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-124">Depth-Stencil State</span></span>

<span data-ttu-id="4786f-125">此狀態群組 (查看 [**D3D10 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) 初始化 [輸出合併階段](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)的深度樣板部分。</span><span class="sxs-lookup"><span data-stu-id="4786f-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="4786f-126">更具體而言，這個物件初始化深度和樣板測試。</span><span class="sxs-lookup"><span data-stu-id="4786f-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="4786f-127">若要建立深度範本狀態物件，請參閱 [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)。</span><span class="sxs-lookup"><span data-stu-id="4786f-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="4786f-128">混色狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-128">Blend State</span></span>

<span data-ttu-id="4786f-129">這一組狀態 (請參閱 [**D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) 初始化 [輸出合併階段](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)的混合部分。</span><span class="sxs-lookup"><span data-stu-id="4786f-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="4786f-130">若要建立 blend 狀態物件，請參閱 [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate)。</span><span class="sxs-lookup"><span data-stu-id="4786f-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="4786f-131">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="4786f-131">Sampler State</span></span>

<span data-ttu-id="4786f-132">這一組狀態 (請參閱 [**D3D10 \_ 取樣器 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) 初始化取樣器物件。</span><span class="sxs-lookup"><span data-stu-id="4786f-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="4786f-133">著色器階段使用取樣器物件，以篩選記憶體中的紋理。</span><span class="sxs-lookup"><span data-stu-id="4786f-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



<span data-ttu-id="4786f-134">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="4786f-134">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="4786f-135">在 Direct3D 10 中，取樣器物件不再系結至特定材質，它只會說明如何針對任何附加的資源進行篩選。</span><span class="sxs-lookup"><span data-stu-id="4786f-135">In Direct3D 10, the sampler object is no longer bound to a specific texture, it just describes how to do filtering given any attached resource.</span></span>



 

<span data-ttu-id="4786f-136">若要建立取樣器狀態物件，請參閱 [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)。</span><span class="sxs-lookup"><span data-stu-id="4786f-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="4786f-137">效能考量</span><span class="sxs-lookup"><span data-stu-id="4786f-137">Performance Considerations</span></span>

<span data-ttu-id="4786f-138">設計 API 以使用狀態物件，會建立許多效能優點。</span><span class="sxs-lookup"><span data-stu-id="4786f-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="4786f-139">其中包括在物件建立時驗證狀態，在硬體啟用狀態物件快取，並大幅降低狀態設定 API 呼叫期間傳遞的狀態數量（傳遞狀態物件的控制代碼，而不是狀態）。</span><span class="sxs-lookup"><span data-stu-id="4786f-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="4786f-140">若要達成這些效能改進，您應該在應用程式啟動時，在轉譯迴圈之前，建立狀態物件。</span><span class="sxs-lookup"><span data-stu-id="4786f-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="4786f-141">狀態物件是不變，也就是狀態物件建立之後便無法變更。</span><span class="sxs-lookup"><span data-stu-id="4786f-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="4786f-142">相反地，您必須終結並重新建立它們。</span><span class="sxs-lookup"><span data-stu-id="4786f-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="4786f-143">若要解決這項限制，您最多可以為每種類型的狀態物件建立4096。</span><span class="sxs-lookup"><span data-stu-id="4786f-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="4786f-144">例如，您可以使用各種取樣器狀態組合來建立數個取樣器物件。</span><span class="sxs-lookup"><span data-stu-id="4786f-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="4786f-145">然後，藉由呼叫適當的 Set API （將控制碼傳遞給物件 (而不是取樣器狀態) ）來變更取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="4786f-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="4786f-146">這大幅降低變更狀態的每個轉譯畫面期間的額外負荷數量，因為呼叫數目和資料量已大幅降低。</span><span class="sxs-lookup"><span data-stu-id="4786f-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="4786f-147">或者，您可以選擇使用效果系統，為您的應用程式自動管理狀態物件的有效建立和解構。</span><span class="sxs-lookup"><span data-stu-id="4786f-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4786f-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="4786f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4786f-149"> (Direct3D 10) 的 API 功能 </span><span class="sxs-lookup"><span data-stu-id="4786f-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
