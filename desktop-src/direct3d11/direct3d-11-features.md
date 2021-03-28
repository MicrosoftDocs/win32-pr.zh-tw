---
title: Direct3D 11 功能
description: 程式設計指南包含如何使用 Direct3D 11 可程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024303"
---
# <a name="direct3d-11-features"></a><span data-ttu-id="f8f10-103">Direct3D 11 功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-103">Direct3D 11 Features</span></span>

<span data-ttu-id="f8f10-104">程式設計指南包含如何使用 Direct3D 11 可程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f8f10-104">The programming guide contains information about how to use the Direct3D 11 programmable pipeline to create realtime 3D graphics for games, and for scientific and desktop applications.</span></span>

-   [<span data-ttu-id="f8f10-105">計算著色器</span><span class="sxs-lookup"><span data-stu-id="f8f10-105">Compute Shader</span></span>](#compute-shader)
-   [<span data-ttu-id="f8f10-106">動態著色器連結</span><span class="sxs-lookup"><span data-stu-id="f8f10-106">Dynamic Shader Linking</span></span>](#dynamic-shader-linking)
-   [<span data-ttu-id="f8f10-107">多執行緒</span><span class="sxs-lookup"><span data-stu-id="f8f10-107">Multithreading</span></span>](#multithreading)
-   [<span data-ttu-id="f8f10-108">鑲嵌式</span><span class="sxs-lookup"><span data-stu-id="f8f10-108">Tessellation</span></span>](#tessellation)
-   [<span data-ttu-id="f8f10-109">完整的功能清單</span><span class="sxs-lookup"><span data-stu-id="f8f10-109">Full Listing of Features</span></span>](#full-listing-of-features)
-   [<span data-ttu-id="f8f10-110">先前版本中新增的功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-110">Features Added in Previous Releases</span></span>](#features-added-in-previous-releases)
-   [<span data-ttu-id="f8f10-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8f10-111">Related topics</span></span>](#related-topics)

## <a name="compute-shader"></a><span data-ttu-id="f8f10-112">計算著色器</span><span class="sxs-lookup"><span data-stu-id="f8f10-112">Compute Shader</span></span>

<span data-ttu-id="f8f10-113">計算著色器是專為一般用途的資料平行處理而設計的可程式化著色器。</span><span class="sxs-lookup"><span data-stu-id="f8f10-113">A compute shader is a programmable shader designed for general-purpose data-parallel processing.</span></span> <span data-ttu-id="f8f10-114">換句話說，計算著色器允許使用 GPU 作為一般用途的平行處理器。</span><span class="sxs-lookup"><span data-stu-id="f8f10-114">In other words, compute shaders allow a GPU to be used as a general-purpose parallel processor.</span></span> <span data-ttu-id="f8f10-115">計算著色器類似于其他可程式化管線著色器 (例如頂點、圖元、幾何在存取輸入和輸出的方式) 。</span><span class="sxs-lookup"><span data-stu-id="f8f10-115">The compute shader is similar to the other programmable pipeline shaders (such as vertex, pixel, geometry) in the way that it accesses inputs and outputs.</span></span> <span data-ttu-id="f8f10-116">計算著色器技術也稱為 DirectCompute 技術。</span><span class="sxs-lookup"><span data-stu-id="f8f10-116">The compute shader technology is also known as the DirectCompute technology.</span></span> <span data-ttu-id="f8f10-117">計算著色器已整合至 Direct3D，可透過 Direct3D 裝置存取。</span><span class="sxs-lookup"><span data-stu-id="f8f10-117">A compute shader is integrated into Direct3D and is accessible through a Direct3D device.</span></span> <span data-ttu-id="f8f10-118">它可以使用 Direct3D 裝置，直接與圖形著色器共用記憶體資源。</span><span class="sxs-lookup"><span data-stu-id="f8f10-118">It can directly share memory resources with graphics shaders by using the Direct3D device.</span></span> <span data-ttu-id="f8f10-119">但是，它不會直接連接到其他著色器階段。</span><span class="sxs-lookup"><span data-stu-id="f8f10-119">However, it is not directly connected to other shader stages.</span></span>

<span data-ttu-id="f8f10-120">計算著色器是針對以互動費率執行計算的大量市場應用程式所設計，當 API (與其相關聯的軟體) 堆疊之間的轉換成本時，以及 CPU 可能會耗用太多額外負荷。</span><span class="sxs-lookup"><span data-stu-id="f8f10-120">A compute shader is designed for mass-market applications that perform computations at interactive rates, when the cost of transitioning between the API (and its associated software stack) and a CPU would consume too much overhead.</span></span>

<span data-ttu-id="f8f10-121">計算著色器有自己的一組狀態。</span><span class="sxs-lookup"><span data-stu-id="f8f10-121">A compute shader has its own set of states.</span></span> <span data-ttu-id="f8f10-122">計算著色器不一定會有強制的1-1 對應到輸入記錄 (例如頂點著色器會) 或輸出記錄 (例如圖元著色器) 。</span><span class="sxs-lookup"><span data-stu-id="f8f10-122">A compute shader does not necessarily have a forced 1-1 mapping to either input records (like a vertex shader does) or output records (like the pixel shader does).</span></span> <span data-ttu-id="f8f10-123">支援圖形著色器的某些功能，但已移除其他功能，因此可以新增計算著色器特定功能。</span><span class="sxs-lookup"><span data-stu-id="f8f10-123">Some features of the graphics shader are supported, but others have been removed so that new compute shader-specific features could be added.</span></span>

<span data-ttu-id="f8f10-124">為了支援計算著色器特有的功能，現在已有數種新的資源類型可供使用，例如讀取/寫入緩衝區、紋理和結構化緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f8f10-124">To support the compute shader-specific features, several new resource types are now available, such as read/write buffers, textures, and structured buffers.</span></span>

<span data-ttu-id="f8f10-125">如需其他資訊，請參閱 [計算著色器總覽](direct3d-11-advanced-stages-compute-shader.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8f10-125">See [Compute Shader Overview](direct3d-11-advanced-stages-compute-shader.md) for additional information.</span></span>

## <a name="dynamic-shader-linking"></a><span data-ttu-id="f8f10-126">動態著色器連結</span><span class="sxs-lookup"><span data-stu-id="f8f10-126">Dynamic Shader Linking</span></span>

<span data-ttu-id="f8f10-127">轉譯系統在管理著色器時必須處理大量的複雜性，同時提供優化著色器程式碼的機會。</span><span class="sxs-lookup"><span data-stu-id="f8f10-127">Rendering systems must deal with significant complexity when they manage shaders, while providing the opportunity to optimize shader code.</span></span> <span data-ttu-id="f8f10-128">這會成為更大的挑戰，因為著色器必須在不同硬體設定之間的轉譯場景中支援各種不同的材質。</span><span class="sxs-lookup"><span data-stu-id="f8f10-128">This becomes an even greater challenge because shaders must support a variety of different materials in a rendered scene across various hardware configurations.</span></span> <span data-ttu-id="f8f10-129">為了解決這項挑戰，著色器開發人員經常會被帶到兩種一般方法的其中一種。</span><span class="sxs-lookup"><span data-stu-id="f8f10-129">To address this challenge, shader developers have often resorted to one of two general approaches.</span></span> <span data-ttu-id="f8f10-130">他們建立了功能完整的大型、一般用途的著色器，可供各種不同的場景專案使用，以針對彈性來權衡某些效能，或針對每個幾何資料流程、材質類型或所需的光源類型組合建立個別的著色器。</span><span class="sxs-lookup"><span data-stu-id="f8f10-130">They have either created fully featured large, general-purpose shaders that can be used by a wide variety of scene items, which trade off some performance for flexibility, or created individual shaders for each geometry stream, material type, or light type combination needed.</span></span>

<span data-ttu-id="f8f10-131">這些大型的一般用途著色器會藉由使用不同的預處理器定義來重新編譯相同的著色器來處理這項挑戰，而後者的方法則是使用暴力密碼開發人員能力來達成相同的結果。</span><span class="sxs-lookup"><span data-stu-id="f8f10-131">These large, general-purpose shaders handle this challenge by recompiling the same shader with different preprocessor definitions, and the latter method uses brute-force developer power to achieve the same result.</span></span> <span data-ttu-id="f8f10-132">如果開發人員現在必須在其遊戲和資產管線中管理數千種不同的著色器排列，著色器排列爆炸通常會造成問題。</span><span class="sxs-lookup"><span data-stu-id="f8f10-132">The shader permutation explosion has often been a problem for developers who must now manage thousands of different shader permutations within their game and asset pipeline.</span></span>

<span data-ttu-id="f8f10-133">Direct3D 11 和著色器模型5引進了物件導向的語言結構，並提供著色器連結的執行時間支援，以協助開發人員程式著色器。</span><span class="sxs-lookup"><span data-stu-id="f8f10-133">Direct3D 11 and shader model 5 introduce object-oriented language constructs and provide runtime support of shader linking to help developers program shaders.</span></span>

<span data-ttu-id="f8f10-134">如需其他資訊，請參閱 [動態連結](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) 。</span><span class="sxs-lookup"><span data-stu-id="f8f10-134">See [Dynamic Linking](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) for additional information.</span></span>

## <a name="multithreading"></a><span data-ttu-id="f8f10-135">多執行緒</span><span class="sxs-lookup"><span data-stu-id="f8f10-135">Multithreading</span></span>

<span data-ttu-id="f8f10-136">許多圖形應用程式都有 CPU 系結，因為這類的活動很高，例如場景圖形遍歷、物件排序和物理模擬。</span><span class="sxs-lookup"><span data-stu-id="f8f10-136">Many graphics applications are CPU-bound because of costly activities such as scene graph traversal, object sorting, and physics simulations.</span></span> <span data-ttu-id="f8f10-137">由於多核心系統逐漸推出，因此 Direct3D 11 已改善其多執行緒支援，以在多個 CPU 執行緒和 D3D11 圖形 Api 之間啟用有效率的互動。</span><span class="sxs-lookup"><span data-stu-id="f8f10-137">Because multicore systems are becoming increasingly available, Direct3D 11 has improved its multithreading support to enable efficient interaction between multiple CPU threads and the D3D11 graphics APIs.</span></span>

<span data-ttu-id="f8f10-138">Direct3D 11 啟用下列功能以支援多執行緒處理：</span><span class="sxs-lookup"><span data-stu-id="f8f10-138">Direct3D 11 enables the following functionality to support multithreading:</span></span>

-   <span data-ttu-id="f8f10-139">並行物件現在是在不同的執行緒中建立的，讓可自由執行緒建立物件的進入點函數可讓許多執行緒同時建立物件。</span><span class="sxs-lookup"><span data-stu-id="f8f10-139">Concurrent objects are now created in separate threads — Making entry-point functions that create objects free-threaded makes it possible for many threads to create objects simultaneously.</span></span> <span data-ttu-id="f8f10-140">例如，應用程式現在可以編譯著色器，或在另一個執行緒上載入材質。</span><span class="sxs-lookup"><span data-stu-id="f8f10-140">For example, an application can now compile a shader or load a texture on one thread while rendering on another.</span></span>
-   <span data-ttu-id="f8f10-141">您可以在多個執行緒上建立命令清單，命令清單是已錄製的圖形命令序列。</span><span class="sxs-lookup"><span data-stu-id="f8f10-141">Command lists can be created on multiple threads — A command list is a recorded sequence of graphics commands.</span></span> <span data-ttu-id="f8f10-142">使用 Direct3D 11 時，您可以在多個 CPU 執行緒上建立命令清單，以平行方式在多個執行緒上進行場景資料庫或物理處理。</span><span class="sxs-lookup"><span data-stu-id="f8f10-142">With Direct3D 11, you can create command lists on multiple CPU threads, which enables parallel traversal of the scene database or physics processing on multiple threads.</span></span> <span data-ttu-id="f8f10-143">這會釋放主要轉譯執行緒，以將命令緩衝區分派至硬體。</span><span class="sxs-lookup"><span data-stu-id="f8f10-143">This frees the main rendering thread to dispatch command buffers to the hardware.</span></span>

<span data-ttu-id="f8f10-144">如需其他資訊，請參閱 [多執行緒](overviews-direct3d-11-render-multi-thread.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8f10-144">See [MultiThreading](overviews-direct3d-11-render-multi-thread.md) for additional information.</span></span>

## <a name="tessellation"></a><span data-ttu-id="f8f10-145">鑲嵌</span><span class="sxs-lookup"><span data-stu-id="f8f10-145">Tessellation</span></span>

<span data-ttu-id="f8f10-146">鑲嵌可以用來呈現具有不同詳細資料層級的單一模型。</span><span class="sxs-lookup"><span data-stu-id="f8f10-146">Tessellation can be used to render a single model with varying levels of detail.</span></span> <span data-ttu-id="f8f10-147">這種方法會產生更具幾何的精確模型，取決於場景所需的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="f8f10-147">This approach generates a more geometrically accurate model that depends on the level of detail required for a scene.</span></span> <span data-ttu-id="f8f10-148">在詳細資料層級允許較低幾何模型的場景中使用鑲嵌，可減少轉譯期間耗用的記憶體頻寬需求。</span><span class="sxs-lookup"><span data-stu-id="f8f10-148">Use tessellation in a scene where the level of detail allows a lower geometry model, which reduces the demand on memory bandwidth consumed during rendering.</span></span>

<span data-ttu-id="f8f10-149">在 Direct3D 中，會在 GPU 上執行鑲嵌，以從粗略 (較不詳細的) 輸入修補程式來計算更平滑的曲線表面。</span><span class="sxs-lookup"><span data-stu-id="f8f10-149">In Direct3D, tessellation is implemented on the GPU to calculate a smoother curved surface from a coarse (less detailed) input patch.</span></span> <span data-ttu-id="f8f10-150">每個 (四或三角形) patch 臉部都會細分成較小的三角形臉部，以更接近您想要的表面。</span><span class="sxs-lookup"><span data-stu-id="f8f10-150">Each (quad or triangle) patch face is subdivided into smaller triangular faces that better approximate the surface that you want.</span></span>

<span data-ttu-id="f8f10-151">如需在圖形管線中執行鑲嵌的詳細資訊，請參閱 [鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="f8f10-151">For information about implementing tessellation in the graphics pipeline, see [Tessellation Overview](direct3d-11-advanced-stages-tessellation.md).</span></span>

## <a name="full-listing-of-features"></a><span data-ttu-id="f8f10-152">完整的功能清單</span><span class="sxs-lookup"><span data-stu-id="f8f10-152">Full Listing of Features</span></span>

<span data-ttu-id="f8f10-153">這是 Direct3D 11 中功能的完整清單。</span><span class="sxs-lookup"><span data-stu-id="f8f10-153">This is a complete list of the features in Direct3D 11.</span></span>

-   <span data-ttu-id="f8f10-154">您可以在建立裝置時 specifing[功能等級](overviews-direct3d-11-devices-downlevel-intro.md)，在舊版[硬體](overviews-direct3d-11-devices-downlevel.md)上執行 Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="f8f10-154">You can run Direct3D 11 on [downlevel hardware](overviews-direct3d-11-devices-downlevel.md) by specifing a [feature level](overviews-direct3d-11-devices-downlevel-intro.md) when you create a device.</span></span>
-   <span data-ttu-id="f8f10-155">您可以使用下列著色器類型來執行鑲嵌式 (參閱 [鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)) ：</span><span class="sxs-lookup"><span data-stu-id="f8f10-155">You can perform tessellation (see [Tessellation Overview](direct3d-11-advanced-stages-tessellation.md)) by using the following shader types:</span></span>

    -   <span data-ttu-id="f8f10-156">輪廓著色器</span><span class="sxs-lookup"><span data-stu-id="f8f10-156">Hull Shader</span></span>
    -   <span data-ttu-id="f8f10-157">網域著色器</span><span class="sxs-lookup"><span data-stu-id="f8f10-157">Domain Shader</span></span>

-   <span data-ttu-id="f8f10-158">Direct3D 11 支援多執行緒 (查看 [多執行緒](overviews-direct3d-11-render-multi-thread.md)) </span><span class="sxs-lookup"><span data-stu-id="f8f10-158">Direct3D 11 supports multithreading (see [MultiThreading](overviews-direct3d-11-render-multi-thread.md))</span></span>

    -   <span data-ttu-id="f8f10-159">多執行緒資源/著色器/物件建立</span><span class="sxs-lookup"><span data-stu-id="f8f10-159">Multithread resource/shader/object creation</span></span>
    -   <span data-ttu-id="f8f10-160">多執行緒顯示清單建立</span><span class="sxs-lookup"><span data-stu-id="f8f10-160">Multithreaded Display list creation</span></span>

-   <span data-ttu-id="f8f10-161">Direct3D 11 使用下列功能來擴充著色器 (參閱 [著色器模型 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) </span><span class="sxs-lookup"><span data-stu-id="f8f10-161">Direct3D 11 expands shaders with the following features (see [Shader Model 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl))</span></span>

    -   <span data-ttu-id="f8f10-162">可定址的資源-紋理、常數緩衝區和取樣器</span><span class="sxs-lookup"><span data-stu-id="f8f10-162">Addressable resources - textures, constant buffers, and samplers</span></span>
    -   <span data-ttu-id="f8f10-163">其他資源類型（例如讀取/寫入緩衝區和紋理） (查看 [新的資源類型](direct3d-11-advanced-stages-cs-resources.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f8f10-163">Additional resource types, such as read/write buffers and textures (see [New Resource Types](direct3d-11-advanced-stages-cs-resources.md)).</span></span>
    -   <span data-ttu-id="f8f10-164">子 例 程</span><span class="sxs-lookup"><span data-stu-id="f8f10-164">Subroutines</span></span>
    -   <span data-ttu-id="f8f10-165">計算著色器 (查看 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器的總覽) -著色器可在數個軟體執行緒或執行緒群組之間劃分問題空間，以加速計算，並在著色器暫存器之間共用資料，以大幅減少輸入著色器所需的資料量。</span><span class="sxs-lookup"><span data-stu-id="f8f10-165">Compute shader (see [Compute Shader Overview](direct3d-11-advanced-stages-compute-shader.md)) - A shader that speeds up computations by dividing the problem space between several software threads or groups of threads, and sharing data among shader registers to significantly reduce the amount of data required to input into a shader.</span></span> <span data-ttu-id="f8f10-166">計算著色器可大幅改善的演算法包括 post 處理、動畫、物理及人工智慧。</span><span class="sxs-lookup"><span data-stu-id="f8f10-166">Algorithms that the compute shader can significantly improve include post processing, animation, physics, and artificial intelligence.</span></span>
    -   <span data-ttu-id="f8f10-167">幾何著色器 (請參閱 [幾何著色器功能](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features)) </span><span class="sxs-lookup"><span data-stu-id="f8f10-167">Geometry shader (see [Geometry Shader Features](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features))</span></span>

        -   <span data-ttu-id="f8f10-168">實例-可讓幾何著色器輸出最多1024個頂點，或實例和頂點的任意組合，最多 1024 (最多每) 32 頂點的32實例。</span><span class="sxs-lookup"><span data-stu-id="f8f10-168">Instancing - Allows the geometry shader to output a maximum of 1024 vertices, or any combination of instances and vertices up to 1024 (maximum of 32 instances of 32 vertices each).</span></span>

    -   <span data-ttu-id="f8f10-169">像素著色器</span><span class="sxs-lookup"><span data-stu-id="f8f10-169">Pixel shader</span></span>

        -   <span data-ttu-id="f8f10-170">作為 PS 輸入的涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="f8f10-170">Coverage as PS Input</span></span>
        -   <span data-ttu-id="f8f10-171">可程式化輸入的內插補點-圖元著色器可以評估圖元內的屬性，在 [取樣] 方格上的任何位置</span><span class="sxs-lookup"><span data-stu-id="f8f10-171">Programmable Interpolation of Inputs - The pixel shader can evaluate attributes within the pixel, anywhere on the multisample grid</span></span>
        -   <span data-ttu-id="f8f10-172">屬性的距心取樣必須遵守下列規則：</span><span class="sxs-lookup"><span data-stu-id="f8f10-172">Centroid sampling of attributes must obey the following rules:</span></span>

            -   <span data-ttu-id="f8f10-173">如果涵蓋了基本型別中的所有樣本，則不論範例模式是否在圖元中心都有範例位置，屬性都會在圖元中心進行評估。</span><span class="sxs-lookup"><span data-stu-id="f8f10-173">If all samples in the primitive are covered, the attribute is evaluated at the pixel center regardless of whether the sample pattern has a sample location at the pixel center.</span></span>
            -   <span data-ttu-id="f8f10-174">否則，會在第一個涵蓋的範例中評估屬性，也就是在所有範例索引之間具有最低索引的範例。</span><span class="sxs-lookup"><span data-stu-id="f8f10-174">Otherwise, the attribute is evaluated at the first covered sample, that is, the sample with the lowest index among all sample indexes.</span></span> <span data-ttu-id="f8f10-175">在此情況下，會在將邏輯 AND 運算套用至涵蓋範圍和樣本遮罩轉譯器狀態之後，判斷範例涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="f8f10-175">In this situation, sample coverage is determined after applying the logical AND operation to the coverage and the sample-mask rasterizer state.</span></span>
            -   <span data-ttu-id="f8f10-176">如果未涵蓋任何樣本 (例如，在協助程式圖元上執行，以填滿2x2 圖元戳記) 的協助程式圖元，則會以下列其中一種方式評估屬性：</span><span class="sxs-lookup"><span data-stu-id="f8f10-176">If no samples are covered (such as on helper pixels that are executed off the bounds of a primitive to fill out 2x2 pixel stamps), the attribute is evaluated in one of the following ways:</span></span>

                -   <span data-ttu-id="f8f10-177">如果範例遮罩轉譯器的狀態是圖元中樣本的子集，則範例遮罩轉譯器狀態所涵蓋的第一個範例就是評估點。</span><span class="sxs-lookup"><span data-stu-id="f8f10-177">If the sample-mask rasterizer state is a subset of the samples in the pixel, the first sample that is covered by the sample-mask rasterizer state is the evaluation point.</span></span>
                -   <span data-ttu-id="f8f10-178">否則，在完整的範例遮罩條件中，圖元中心就是評估點。</span><span class="sxs-lookup"><span data-stu-id="f8f10-178">Otherwise, in the full sample-mask condition, the pixel center is the evaluation point.</span></span>

-   <span data-ttu-id="f8f10-179">Direct3D 11 展開材質 (請參閱 [材質總覽](overviews-direct3d-11-resources-textures.md)) ，其中包含下列功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-179">Direct3D 11 expands textures (see [Textures Overview](overviews-direct3d-11-resources-textures.md)) with the following features</span></span>

    -   <span data-ttu-id="f8f10-180">Gather4</span><span class="sxs-lookup"><span data-stu-id="f8f10-180">Gather4</span></span>

        -   <span data-ttu-id="f8f10-181">支援多元件紋理-指定要載入的通道</span><span class="sxs-lookup"><span data-stu-id="f8f10-181">Support for multi-component textures - specify a channel to load from</span></span>
        -   <span data-ttu-id="f8f10-182">支援可程式化位移</span><span class="sxs-lookup"><span data-stu-id="f8f10-182">Support for programmable offsets</span></span>

    -   <span data-ttu-id="f8f10-183">串流</span><span class="sxs-lookup"><span data-stu-id="f8f10-183">Streaming</span></span>

        -   <span data-ttu-id="f8f10-184">用來限制 WDDM 預先載入的材質個</span><span class="sxs-lookup"><span data-stu-id="f8f10-184">Texture clamps to limit WDDM preload</span></span>

    -   <span data-ttu-id="f8f10-185">16K 材質限制</span><span class="sxs-lookup"><span data-stu-id="f8f10-185">16K texture limits</span></span>
    -   <span data-ttu-id="f8f10-186">紋理篩選需要8位的 subtexel 和子 mip 精確度</span><span class="sxs-lookup"><span data-stu-id="f8f10-186">Require 8-bits of subtexel and sub-mip precision on texture filtering</span></span>
    -   <span data-ttu-id="f8f10-187">新的材質壓縮格式 (1 個新的 LDR 格式和1個新的 HDR 格式) </span><span class="sxs-lookup"><span data-stu-id="f8f10-187">New texture compression formats (1 new LDR format and 1 new HDR format)</span></span>

-   <span data-ttu-id="f8f10-188">Direct3D 11 支援保守 oDepth-此演算法可讓圖元著色器比較圖元著色器的每圖元深度值與轉譯器中的圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="f8f10-188">Direct3D 11 supports conservative oDepth - This algorithm allows a pixel shader to compare the per-pixel depth value of the pixel shader with that in the rasterizer.</span></span> <span data-ttu-id="f8f10-189">結果可進行早期的剔除作業，同時維持從圖元著色器輸出 oDepth 的能力。</span><span class="sxs-lookup"><span data-stu-id="f8f10-189">The result enables early depth culling operations while maintaining the ability to output oDepth from a pixel shader.</span></span>
-   <span data-ttu-id="f8f10-190">Direct3D 11 支援大型記憶體</span><span class="sxs-lookup"><span data-stu-id="f8f10-190">Direct3D 11 supports large memory</span></span>

    -   <span data-ttu-id="f8f10-191">允許資源 > 4GB</span><span class="sxs-lookup"><span data-stu-id="f8f10-191">Allow for resources > 4GB</span></span>
    -   <span data-ttu-id="f8f10-192">將資源的索引保持在32位，但資源較大</span><span class="sxs-lookup"><span data-stu-id="f8f10-192">Keep indices of resources 32bit, but resource larger</span></span>

-   <span data-ttu-id="f8f10-193">Direct3D 11 支援資料流程輸出改進</span><span class="sxs-lookup"><span data-stu-id="f8f10-193">Direct3D 11 supports stream output improvements</span></span>

    -   <span data-ttu-id="f8f10-194">可定址的資料流程輸出</span><span class="sxs-lookup"><span data-stu-id="f8f10-194">Addressable Stream output</span></span>
    -   <span data-ttu-id="f8f10-195">將資料流程輸出計數增加至4</span><span class="sxs-lookup"><span data-stu-id="f8f10-195">Increase Stream output count to 4</span></span>
    -   <span data-ttu-id="f8f10-196">將所有資料流程輸出緩衝區變更為多元素</span><span class="sxs-lookup"><span data-stu-id="f8f10-196">Change all stream output buffers to be multi-element</span></span>

-   <span data-ttu-id="f8f10-197">Direct3D 11 支援著色器模型 5 (請參閱 [著色器模型 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)) </span><span class="sxs-lookup"><span data-stu-id="f8f10-197">Direct3D 11 supports Shader Model 5 (see [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5))</span></span>

    -   <span data-ttu-id="f8f10-198">使用 denorms 的雙精度浮點數</span><span class="sxs-lookup"><span data-stu-id="f8f10-198">Doubles with denorms</span></span>
    -   <span data-ttu-id="f8f10-199">Count 位 set 指令</span><span class="sxs-lookup"><span data-stu-id="f8f10-199">Count bits set instruction</span></span>
    -   <span data-ttu-id="f8f10-200">尋找第一個位設定指令</span><span class="sxs-lookup"><span data-stu-id="f8f10-200">Find first bit set instruction</span></span>
    -   <span data-ttu-id="f8f10-201">執行/溢位處理</span><span class="sxs-lookup"><span data-stu-id="f8f10-201">Carry/Overflow handling</span></span>
    -   <span data-ttu-id="f8f10-202">FFTs 的位反轉指示</span><span class="sxs-lookup"><span data-stu-id="f8f10-202">Bit reversal instructions for FFTs</span></span>
    -   <span data-ttu-id="f8f10-203">條件式交換內建函式</span><span class="sxs-lookup"><span data-stu-id="f8f10-203">Conditional Swap intrinsic</span></span>
    -   <span data-ttu-id="f8f10-204">緩衝區上的 Resinfo</span><span class="sxs-lookup"><span data-stu-id="f8f10-204">Resinfo on buffers</span></span>
    -   <span data-ttu-id="f8f10-205">降低精確度的倒數</span><span class="sxs-lookup"><span data-stu-id="f8f10-205">Reduced-precision reciprocal</span></span>
    -   <span data-ttu-id="f8f10-206">著色器轉換指示-fp16 至 fp32，反之亦然</span><span class="sxs-lookup"><span data-stu-id="f8f10-206">Shader conversion instructions - fp16 to fp32 and vice versa</span></span>
    -   <span data-ttu-id="f8f10-207">結構化緩衝區，這是包含結構化元素的新緩衝區類型。</span><span class="sxs-lookup"><span data-stu-id="f8f10-207">Structured buffer, which is a new type of buffer containing structured elements.</span></span>

-   <span data-ttu-id="f8f10-208">Direct3D 11 支援唯讀深度或樣板視圖</span><span class="sxs-lookup"><span data-stu-id="f8f10-208">Direct3D 11 supports read-only depth or stencil views</span></span>

    -   <span data-ttu-id="f8f10-209">停用唯讀元件的寫入，並允許使用材質作為輸入和深度剔除</span><span class="sxs-lookup"><span data-stu-id="f8f10-209">Disables writes to the part that is read-only, allows for using texture as input and for depth-culling</span></span>

-   <span data-ttu-id="f8f10-210">Direct3D 11 支援繪製間接 Direct3D 10 實 DrawAuto，它會取得 GPU) 所產生的內容 (，並將其呈現 (在 GPU) 上。</span><span class="sxs-lookup"><span data-stu-id="f8f10-210">Direct3D 11 supports draw indirect - Direct3D 10 implements DrawAuto, which takes content (generated by the GPU) and renders it (on the GPU).</span></span> <span data-ttu-id="f8f10-211">Direct3D 11 一般化 DrawAuto，使其可由使用 DrawInstanced 和 DrawIndexedInstanced 的計算著色器來呼叫。</span><span class="sxs-lookup"><span data-stu-id="f8f10-211">Direct3D 11 generalizes DrawAuto so that it can be called by a Compute Shader using DrawInstanced and DrawIndexedInstanced.</span></span>
-   <span data-ttu-id="f8f10-212">Direct3D 11 支援其他功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-212">Direct3D 11 supports miscellaneous features</span></span>

    -   <span data-ttu-id="f8f10-213">浮點數區</span><span class="sxs-lookup"><span data-stu-id="f8f10-213">Floating-point viewports</span></span>
    -   <span data-ttu-id="f8f10-214">每一資源 mipmap 固定</span><span class="sxs-lookup"><span data-stu-id="f8f10-214">Per-resource mipmap clamping</span></span>
    -   <span data-ttu-id="f8f10-215">深度偏差-此演算法會使用轉譯器狀態來更新深度偏差的行為。</span><span class="sxs-lookup"><span data-stu-id="f8f10-215">Depth Bias - This algorithm updates the behavior of depth bias, by using rasterizer state.</span></span> <span data-ttu-id="f8f10-216">結果會排除計算偏差可能是 NaN 的案例。</span><span class="sxs-lookup"><span data-stu-id="f8f10-216">The result eliminates the scenarios where the calculated bias could be NaN.</span></span>
    -   <span data-ttu-id="f8f10-217">資源限制-資源索引仍然需要 <= 32 位，但資源可能大於 4 GB。</span><span class="sxs-lookup"><span data-stu-id="f8f10-217">Resource limits - Resource indices are still required to be <= 32 bits, but resources can be larger than 4 GB.</span></span>
    -   <span data-ttu-id="f8f10-218">轉譯器精確度</span><span class="sxs-lookup"><span data-stu-id="f8f10-218">Rasterizer Precision</span></span>
    -   <span data-ttu-id="f8f10-219">MSAA 需求</span><span class="sxs-lookup"><span data-stu-id="f8f10-219">MSAA Requirements</span></span>
    -   <span data-ttu-id="f8f10-220">計數器減少</span><span class="sxs-lookup"><span data-stu-id="f8f10-220">Counters Reduced</span></span>
    -   <span data-ttu-id="f8f10-221">已移除1位格式和文字篩選</span><span class="sxs-lookup"><span data-stu-id="f8f10-221">1-Bit Format and Text Filter Removed</span></span>

## <a name="features-added-in-previous-releases"></a><span data-ttu-id="f8f10-222">先前版本中新增的功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-222">Features Added in Previous Releases</span></span>

<span data-ttu-id="f8f10-223">如需先前版本中新增的功能清單，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="f8f10-223">For the list of the features added in previous releases, see the following topics:</span></span>

-   [<span data-ttu-id="f8f10-224">2009年8月 Windows 7/Direct3D 11 SDK 的新功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-224">What's New in the August 2009 Windows 7/Direct3D 11 SDK</span></span>](dx11-whats-new.md)
-   [<span data-ttu-id="f8f10-225">2008年11月版 Direct3D 11 Technical Preview 的新功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-225">What's New in the November 2008 Direct3D 11 Technical Preview</span></span>](dx11-08nov-whats-new.md)

## <a name="related-topics"></a><span data-ttu-id="f8f10-226">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8f10-226">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8f10-227">Direct3D 11 的新功能</span><span class="sxs-lookup"><span data-stu-id="f8f10-227">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 