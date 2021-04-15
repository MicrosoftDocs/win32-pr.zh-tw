---
description: 建立使用3D 圖形之即時應用程式的每位開發人員都關心效能優化。 本節提供從程式碼取得最佳效能的指導方針。
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: " (Direct3D 9) 的效能優化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d42be994522f0d83e36387b1a5866b3eee10df3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467434"
---
# <a name="performance-optimizations-direct3d-9"></a><span data-ttu-id="ae124-104"> (Direct3D 9) 的效能優化</span><span class="sxs-lookup"><span data-stu-id="ae124-104">Performance Optimizations (Direct3D 9)</span></span>

<span data-ttu-id="ae124-105">建立使用3D 圖形之即時應用程式的每位開發人員都關心效能優化。</span><span class="sxs-lookup"><span data-stu-id="ae124-105">Every developer who creates real-time applications that use 3D graphics is concerned about performance optimization.</span></span> <span data-ttu-id="ae124-106">本節提供從程式碼取得最佳效能的指導方針。</span><span class="sxs-lookup"><span data-stu-id="ae124-106">This section provides guidelines for getting the best performance from your code.</span></span>

-   [<span data-ttu-id="ae124-107">一般效能秘訣</span><span class="sxs-lookup"><span data-stu-id="ae124-107">General Performance Tips</span></span>](#general-performance-tips)
-   [<span data-ttu-id="ae124-108">資料庫和剔除</span><span class="sxs-lookup"><span data-stu-id="ae124-108">Databases and Culling</span></span>](#databases-and-culling)
-   [<span data-ttu-id="ae124-109">批次處理基本專案</span><span class="sxs-lookup"><span data-stu-id="ae124-109">Batching Primitives</span></span>](#batching-primitives)
-   [<span data-ttu-id="ae124-110">光源提示</span><span class="sxs-lookup"><span data-stu-id="ae124-110">Lighting Tips</span></span>](#lighting-tips)
-   [<span data-ttu-id="ae124-111">材質大小</span><span class="sxs-lookup"><span data-stu-id="ae124-111">Texture Size</span></span>](#texture-size)
-   [<span data-ttu-id="ae124-112">矩陣轉換</span><span class="sxs-lookup"><span data-stu-id="ae124-112">Matrix Transforms</span></span>](#matrix-transforms)
-   [<span data-ttu-id="ae124-113">使用動態紋理</span><span class="sxs-lookup"><span data-stu-id="ae124-113">Using Dynamic Textures</span></span>](#using-dynamic-textures)
-   [<span data-ttu-id="ae124-114">使用動態頂點和索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ae124-114">Using Dynamic Vertex and Index Buffers</span></span>](#using-dynamic-vertex-and-index-buffers)
-   [<span data-ttu-id="ae124-115">使用網格</span><span class="sxs-lookup"><span data-stu-id="ae124-115">Using Meshes</span></span>](#using-meshes)
-   [<span data-ttu-id="ae124-116">Z 緩衝區效能</span><span class="sxs-lookup"><span data-stu-id="ae124-116">Z-Buffer Performance</span></span>](#z-buffer-performance)

## <a name="general-performance-tips"></a><span data-ttu-id="ae124-117">一般效能秘訣</span><span class="sxs-lookup"><span data-stu-id="ae124-117">General Performance Tips</span></span>

-   <span data-ttu-id="ae124-118">只有在您必須時才清除。</span><span class="sxs-lookup"><span data-stu-id="ae124-118">Clear only when you must.</span></span>
-   <span data-ttu-id="ae124-119">將狀態變更降至最低，並將剩餘的狀態變更為群組。</span><span class="sxs-lookup"><span data-stu-id="ae124-119">Minimize state changes and group the remaining state changes.</span></span>
-   <span data-ttu-id="ae124-120">如果您可以，請使用較小的紋理。</span><span class="sxs-lookup"><span data-stu-id="ae124-120">Use smaller textures, if you can do so.</span></span>
-   <span data-ttu-id="ae124-121">從前方到上一頁繪製場景中的物件。</span><span class="sxs-lookup"><span data-stu-id="ae124-121">Draw objects in your scene from front to back.</span></span>
-   <span data-ttu-id="ae124-122">使用三角形的停車線，而不是清單和風扇。</span><span class="sxs-lookup"><span data-stu-id="ae124-122">Use triangle strips instead of lists and fans.</span></span> <span data-ttu-id="ae124-123">為了獲得最佳的頂點快取效能，請將帶狀排列成更快重複使用三角形頂點，而不是稍後使用。</span><span class="sxs-lookup"><span data-stu-id="ae124-123">For optimal vertex cache performance, arrange strips to reuse triangle vertices sooner, rather than later.</span></span>
-   <span data-ttu-id="ae124-124">正常降低需要不相稱的系統資源分享的特殊效果。</span><span class="sxs-lookup"><span data-stu-id="ae124-124">Gracefully degrade special effects that require a disproportionate share of system resources.</span></span>
-   <span data-ttu-id="ae124-125">持續測試您的應用程式效能。</span><span class="sxs-lookup"><span data-stu-id="ae124-125">Constantly test your application's performance.</span></span>
-   <span data-ttu-id="ae124-126">最小化頂點緩衝區參數。</span><span class="sxs-lookup"><span data-stu-id="ae124-126">Minimize vertex buffer switches.</span></span>
-   <span data-ttu-id="ae124-127">盡可能使用靜態頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ae124-127">Use static vertex buffers where possible.</span></span>
-   <span data-ttu-id="ae124-128">針對靜態物件，每個 FVF 使用一個大型靜態頂點緩衝區，而不是每個物件一個。</span><span class="sxs-lookup"><span data-stu-id="ae124-128">Use one large static vertex buffer per FVF for static objects, rather than one per object.</span></span>
-   <span data-ttu-id="ae124-129">如果您的應用程式需要隨機存取 AGP 記憶體中的頂點緩衝區，請選擇屬於32個位元組倍數的頂點格式大小。</span><span class="sxs-lookup"><span data-stu-id="ae124-129">If your application needs random access into the vertex buffer in AGP memory, choose a vertex format size that is a multiple of 32 bytes.</span></span> <span data-ttu-id="ae124-130">否則，請選取最小的適當格式。</span><span class="sxs-lookup"><span data-stu-id="ae124-130">Otherwise, select the smallest appropriate format.</span></span>
-   <span data-ttu-id="ae124-131">使用索引基本專案繪製。</span><span class="sxs-lookup"><span data-stu-id="ae124-131">Draw using indexed primitives.</span></span> <span data-ttu-id="ae124-132">這可讓您在硬體內有更有效率的頂點快取。</span><span class="sxs-lookup"><span data-stu-id="ae124-132">This can allow for more efficient vertex caching within hardware.</span></span>
-   <span data-ttu-id="ae124-133">如果深度緩衝區格式包含樣板通道，請一律同時清除深度和樣板通道。</span><span class="sxs-lookup"><span data-stu-id="ae124-133">If the depth buffer format contains a stencil channel, always clear the depth and stencil channels at the same time.</span></span>
-   <span data-ttu-id="ae124-134">盡可能結合著色器指令和資料輸出。</span><span class="sxs-lookup"><span data-stu-id="ae124-134">Combine the shader instruction and the data output where possible.</span></span> <span data-ttu-id="ae124-135">例如：</span><span class="sxs-lookup"><span data-stu-id="ae124-135">For example:</span></span>
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a><span data-ttu-id="ae124-136">資料庫和剔除</span><span class="sxs-lookup"><span data-stu-id="ae124-136">Databases and Culling</span></span>

<span data-ttu-id="ae124-137">在您的世界中建立可靠的物件資料庫，是 Direct3D 中絕佳效能的關鍵。</span><span class="sxs-lookup"><span data-stu-id="ae124-137">Building a reliable database of the objects in your world is key to excellent performance in Direct3D.</span></span> <span data-ttu-id="ae124-138">它比對柵格化或硬體的改進更為重要。</span><span class="sxs-lookup"><span data-stu-id="ae124-138">It is more important than improvements to rasterization or hardware.</span></span>

<span data-ttu-id="ae124-139">您應維持可能管理的最小多邊形計數。</span><span class="sxs-lookup"><span data-stu-id="ae124-139">You should maintain the lowest polygon count you can possibly manage.</span></span> <span data-ttu-id="ae124-140">從頭開始建立低多邊形模型，以設計較低的多邊形計數。</span><span class="sxs-lookup"><span data-stu-id="ae124-140">Design for a low polygon count by building low-polygon models from the start.</span></span> <span data-ttu-id="ae124-141">如果您這樣做，請新增多邊形，而不會在開發過程中犧牲效能。</span><span class="sxs-lookup"><span data-stu-id="ae124-141">Add polygons if you can do so without sacrificing performance later in the development process.</span></span> <span data-ttu-id="ae124-142">請記住，最快的多邊形是您未繪製的多邊形。</span><span class="sxs-lookup"><span data-stu-id="ae124-142">Remember, the fastest polygons are the ones you don't draw.</span></span>

## <a name="batching-primitives"></a><span data-ttu-id="ae124-143">批次處理基本專案</span><span class="sxs-lookup"><span data-stu-id="ae124-143">Batching Primitives</span></span>

<span data-ttu-id="ae124-144">若要在執行期間取得最佳轉譯效能，請嘗試以批次方式處理基本專案，並盡可能減少轉譯狀態變更的數目。</span><span class="sxs-lookup"><span data-stu-id="ae124-144">To get the best rendering performance during execution, try to work with primitives in batches and keep the number of render-state changes as low as possible.</span></span> <span data-ttu-id="ae124-145">例如，如果您有一個具有兩個材質的物件，請將使用第一個材質的三角形分組，並依照所需的轉譯狀態來變更材質。</span><span class="sxs-lookup"><span data-stu-id="ae124-145">For example, if you have an object with two textures, group the triangles that use the first texture and follow them with the necessary render state to change the texture.</span></span> <span data-ttu-id="ae124-146">然後，將使用第二個材質的所有三角形分組。</span><span class="sxs-lookup"><span data-stu-id="ae124-146">Then group all the triangles that use the second texture.</span></span> <span data-ttu-id="ae124-147">最簡單的 Direct3D 硬體支援是透過硬體抽象層（ (HAL) ），以批次呈現狀態和基本專案的批次來呼叫。</span><span class="sxs-lookup"><span data-stu-id="ae124-147">The simplest hardware support for Direct3D is called with batches of render states and batches of primitives through the hardware abstraction layer (HAL).</span></span> <span data-ttu-id="ae124-148">更有效地批處理指示，執行期間會執行較少的 HAL 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ae124-148">The more effectively the instructions are batched, the fewer HAL calls are performed during execution.</span></span>

## <a name="lighting-tips"></a><span data-ttu-id="ae124-149">光源提示</span><span class="sxs-lookup"><span data-stu-id="ae124-149">Lighting Tips</span></span>

<span data-ttu-id="ae124-150">由於燈光會將每個頂點的成本加入至每個呈現的框架，因此您可以在應用程式中使用它們，以大幅改善效能。</span><span class="sxs-lookup"><span data-stu-id="ae124-150">Because lights add a per-vertex cost to each rendered frame, you can improve performance significantly by being careful about how you use them in your application.</span></span> <span data-ttu-id="ae124-151">下列大部分的秘訣都是衍生自背道而馳「最快的程式碼是永遠不會呼叫的程式碼」。</span><span class="sxs-lookup"><span data-stu-id="ae124-151">Most of the following tips derive from the maxim, "the fastest code is code that is never called."</span></span>

-   <span data-ttu-id="ae124-152">盡可能使用較少的輕量來源。</span><span class="sxs-lookup"><span data-stu-id="ae124-152">Use as few light sources as possible.</span></span> <span data-ttu-id="ae124-153">例如，若要提高整體光源層級，請使用環境光源，而不是加入新的燈光來源。</span><span class="sxs-lookup"><span data-stu-id="ae124-153">To increase the overall lighting level, for example, use the ambient light instead of adding a new light source.</span></span>
-   <span data-ttu-id="ae124-154">方向光線比點燈或聚光燈更有效率。</span><span class="sxs-lookup"><span data-stu-id="ae124-154">Directional lights are more efficient than point lights or spotlights.</span></span> <span data-ttu-id="ae124-155">針對方向光源，光的方向是固定的，而且不需要以每個頂點為基礎來計算。</span><span class="sxs-lookup"><span data-stu-id="ae124-155">For directional lights, the direction to the light is fixed and doesn't need to be calculated on a per-vertex basis.</span></span>
-   <span data-ttu-id="ae124-156">聚光燈的結果可能比點燈更有效率，因為光線的範圍外的區域會快速計算。</span><span class="sxs-lookup"><span data-stu-id="ae124-156">Spotlights can be more efficient than point lights, because the area outside the cone of light is calculated quickly.</span></span> <span data-ttu-id="ae124-157">聚光燈是否更有效率，而不會取決於焦點在您的場景中的程度。</span><span class="sxs-lookup"><span data-stu-id="ae124-157">Whether spotlights are more efficient or not depends on how much of your scene is lit by the spotlight.</span></span>
-   <span data-ttu-id="ae124-158">您可以使用 range 參數，將您的燈光限制為只有您需要照亮的場景部分。</span><span class="sxs-lookup"><span data-stu-id="ae124-158">Use the range parameter to limit your lights to only the parts of the scene you need to illuminate.</span></span> <span data-ttu-id="ae124-159">所有的光線類型在超出範圍時，就會相當早結束。</span><span class="sxs-lookup"><span data-stu-id="ae124-159">All the light types exit fairly early when they are out of range.</span></span>
-   <span data-ttu-id="ae124-160">反光幾乎會醒目顯示光線成本的兩倍。</span><span class="sxs-lookup"><span data-stu-id="ae124-160">Specular highlights almost double the cost of a light.</span></span> <span data-ttu-id="ae124-161">只有在您必須時才使用它們。</span><span class="sxs-lookup"><span data-stu-id="ae124-161">Use them only when you must.</span></span> <span data-ttu-id="ae124-162">盡可能將 D3DRS \_ SPECULARENABLE 轉譯狀態設定為0（預設值）。</span><span class="sxs-lookup"><span data-stu-id="ae124-162">Set the D3DRS\_SPECULARENABLE render state to 0, the default value, whenever possible.</span></span> <span data-ttu-id="ae124-163">定義材質時，您必須將反射功率值設定為零，以關閉該材質的高光。只是將反射色彩設定為0、0、0就夠了。</span><span class="sxs-lookup"><span data-stu-id="ae124-163">When defining materials, you must set the specular power value to zero to turn off specular highlights for that material; just setting the specular color to 0,0,0 is not enough.</span></span>

## <a name="texture-size"></a><span data-ttu-id="ae124-164">材質大小</span><span class="sxs-lookup"><span data-stu-id="ae124-164">Texture Size</span></span>

<span data-ttu-id="ae124-165">紋理對應效能與記憶體的速度非常相關。</span><span class="sxs-lookup"><span data-stu-id="ae124-165">Texture-mapping performance is heavily dependent on the speed of memory.</span></span> <span data-ttu-id="ae124-166">有數種方式可將應用程式材質的快取效能最大化。</span><span class="sxs-lookup"><span data-stu-id="ae124-166">There are a number of ways to maximize the cache performance of your application's textures.</span></span>

-   <span data-ttu-id="ae124-167">讓紋理保持小。</span><span class="sxs-lookup"><span data-stu-id="ae124-167">Keep the textures small.</span></span> <span data-ttu-id="ae124-168">紋理越小，就可以在主要 CPU 的次要快取中維護更好的機會。</span><span class="sxs-lookup"><span data-stu-id="ae124-168">The smaller the textures are, the better chance they have of being maintained in the main CPU's secondary cache.</span></span>
-   <span data-ttu-id="ae124-169">請勿變更每個基本的材質。</span><span class="sxs-lookup"><span data-stu-id="ae124-169">Do not change the textures on a per-primitive basis.</span></span> <span data-ttu-id="ae124-170">請嘗試將多邊形依其使用的紋理順序分組。</span><span class="sxs-lookup"><span data-stu-id="ae124-170">Try to keep polygons grouped in order of the textures they use.</span></span>
-   <span data-ttu-id="ae124-171">盡可能使用正方形紋理。</span><span class="sxs-lookup"><span data-stu-id="ae124-171">Use square textures whenever possible.</span></span> <span data-ttu-id="ae124-172">其維度為256x256 的紋理最快。</span><span class="sxs-lookup"><span data-stu-id="ae124-172">Textures whose dimensions are 256x256 are the fastest.</span></span> <span data-ttu-id="ae124-173">例如，如果您的應用程式使用四個128x128 材質，請試著確定它們使用相同的調色板，並將它們全部放在一個256x256 材質中。</span><span class="sxs-lookup"><span data-stu-id="ae124-173">If your application uses four 128x128 textures, for example, try to ensure that they use the same palette and place them all into one 256x256 texture.</span></span> <span data-ttu-id="ae124-174">這項技術也可減少材質交換的量。</span><span class="sxs-lookup"><span data-stu-id="ae124-174">This technique also reduces the amount of texture swapping.</span></span> <span data-ttu-id="ae124-175">當然，除非您的應用程式需要太多紋理，否則除非您的應用程式需要太多紋理，否則您不應該使用256x256 紋理。</span><span class="sxs-lookup"><span data-stu-id="ae124-175">Of course, you should not use 256x256 textures unless your application requires that much texturing because, as mentioned, textures should be kept as small as possible.</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="ae124-176">矩陣轉換</span><span class="sxs-lookup"><span data-stu-id="ae124-176">Matrix Transforms</span></span>

<span data-ttu-id="ae124-177">Direct3D 使用世界和檢視矩陣，讓您設定數個內部資料結構。</span><span class="sxs-lookup"><span data-stu-id="ae124-177">Direct3D uses the world and view matrices that you set to configure several internal data structures.</span></span> <span data-ttu-id="ae124-178">每當您設定世界或檢視矩陣，系統會重新計算相關內部結構。</span><span class="sxs-lookup"><span data-stu-id="ae124-178">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="ae124-179">頻繁地設定這些矩陣（例如，每個框架上千次）都是計算時間耗用量。</span><span class="sxs-lookup"><span data-stu-id="ae124-179">Setting these matrices frequently - for example, thousands of times per frame - is computationally time-consuming.</span></span> <span data-ttu-id="ae124-180">您可以串連世界和檢視矩陣成為世界檢視矩陣 (您將其設為世界矩陣)，然後將檢視矩陣設為單位矩陣，將所需的計算次數最小化。</span><span class="sxs-lookup"><span data-stu-id="ae124-180">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="ae124-181">保留個別世界和檢視矩陣的快取複本，讓您可以視需要修改、串連並重設世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="ae124-181">Keep cached copies of individual world and view matrices so that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="ae124-182">為了清楚起見，在本檔中，Direct3D 範例很少使用這項優化。</span><span class="sxs-lookup"><span data-stu-id="ae124-182">For clarity in this documentation, Direct3D samples rarely employ this optimization.</span></span>

## <a name="using-dynamic-textures"></a><span data-ttu-id="ae124-183">使用動態紋理</span><span class="sxs-lookup"><span data-stu-id="ae124-183">Using Dynamic Textures</span></span>

<span data-ttu-id="ae124-184">若要查明驅動程式是否支援動態材質，請檢查 \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 D3DCAPS2 DYNAMICTEXTURES 旗標。</span><span class="sxs-lookup"><span data-stu-id="ae124-184">To find out if the driver supports dynamic textures, check the D3DCAPS2\_DYNAMICTEXTURES flag of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

<span data-ttu-id="ae124-185">使用動態紋理時，請記住下列事項。</span><span class="sxs-lookup"><span data-stu-id="ae124-185">Keep the following things in mind when working with dynamic textures.</span></span>

-   <span data-ttu-id="ae124-186">無法進行管理。</span><span class="sxs-lookup"><span data-stu-id="ae124-186">They cannot be managed.</span></span> <span data-ttu-id="ae124-187">例如，其集區無法 D3DPOOL \_ 管理。</span><span class="sxs-lookup"><span data-stu-id="ae124-187">For example, their pool cannot be D3DPOOL\_MANAGED.</span></span>
-   <span data-ttu-id="ae124-188">動態紋理可以鎖定，即使它們是在 D3DPOOL 預設中建立的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ae124-188">Dynamic textures can be locked, even if they are created in D3DPOOL\_DEFAULT.</span></span>
-   <span data-ttu-id="ae124-189">D3DLOCK \_ 捨棄是動態紋理的有效鎖定旗標。</span><span class="sxs-lookup"><span data-stu-id="ae124-189">D3DLOCK\_DISCARD is a valid lock flag for dynamic textures.</span></span>

<span data-ttu-id="ae124-190">最好只針對每一種格式建立一個動態材質，而且可能會依大小來建立。</span><span class="sxs-lookup"><span data-stu-id="ae124-190">It is a good idea to create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="ae124-191">由於鎖定每個層級的額外負荷，因此不建議使用動態 mipmap、cube 和磁片區。</span><span class="sxs-lookup"><span data-stu-id="ae124-191">Dynamic mipmaps, cubes, and volumes are not recommended because of the additional overhead in locking every level.</span></span> <span data-ttu-id="ae124-192">若為 mipmap， \_ 則只允許在最上層使用 D3DLOCK 捨棄。</span><span class="sxs-lookup"><span data-stu-id="ae124-192">For mipmaps, D3DLOCK\_DISCARD is allowed only on the top level.</span></span> <span data-ttu-id="ae124-193">只要鎖定最上層，就會捨棄所有層級。</span><span class="sxs-lookup"><span data-stu-id="ae124-193">All levels are discarded by locking just the top level.</span></span> <span data-ttu-id="ae124-194">此行為對於磁片區和 cube 而言是相同的。</span><span class="sxs-lookup"><span data-stu-id="ae124-194">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="ae124-195">針對 cube，最上層和臉部0會被鎖定。</span><span class="sxs-lookup"><span data-stu-id="ae124-195">For cubes, the top level and face 0 are locked.</span></span>

<span data-ttu-id="ae124-196">下列虛擬程式碼顯示使用動態材質的範例。</span><span class="sxs-lookup"><span data-stu-id="ae124-196">The following pseudocode shows an example of using a dynamic texture.</span></span>


```
DrawProceduralTexture(pTex)
{
    // pTex should not be very small because overhead of 
    //   calling driver every D3DLOCK_DISCARD will not 
    //   justify the performance gain. Experimentation is encouraged.
    pTex->Lock(D3DLOCK_DISCARD);
    <Overwrite *entire* texture>
    pTex->Unlock();
    pDev->SetTexture();
    pDev->DrawPrimitive();
}
```



## <a name="using-dynamic-vertex-and-index-buffers"></a><span data-ttu-id="ae124-197">使用動態頂點和索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ae124-197">Using Dynamic Vertex and Index Buffers</span></span>

<span data-ttu-id="ae124-198">當圖形處理器使用緩衝區時，鎖定靜態頂點緩衝區可能會對效能造成顯著的影響。</span><span class="sxs-lookup"><span data-stu-id="ae124-198">Locking a static vertex buffer while the graphics processor is using the buffer can have a significant performance penalty.</span></span> <span data-ttu-id="ae124-199">鎖定呼叫必須等到圖形處理器從緩衝區讀取頂點或索引資料之後，才可以傳回給呼叫的應用程式，這會造成嚴重的延遲。</span><span class="sxs-lookup"><span data-stu-id="ae124-199">The lock call must wait until the graphics processor is finished reading vertex or index data from the buffer before it can return to the calling application, a significant delay.</span></span> <span data-ttu-id="ae124-200">針對每個畫面格的靜態緩衝區進行鎖定，然後再進行轉譯，也可防止圖形處理器緩衝轉譯命令，因為它必須在傳回鎖定指標之前完成命令。</span><span class="sxs-lookup"><span data-stu-id="ae124-200">Locking and then rendering from a static buffer several times per frame also prevents the graphics processor from buffering rendering commands, since it must finish commands before returning the lock pointer.</span></span> <span data-ttu-id="ae124-201">如果沒有緩衝的命令，圖形處理器會維持閒置，直到應用程式完成填滿頂點緩衝區或索引緩衝區併發出轉譯命令為止。</span><span class="sxs-lookup"><span data-stu-id="ae124-201">Without buffered commands, the graphics processor remains idle until after the application is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="ae124-202">在理想的情況下，頂點或索引資料永遠不會變更，不過這不一定是可行的。</span><span class="sxs-lookup"><span data-stu-id="ae124-202">Ideally the vertex or index data would never change, however this is not always possible.</span></span> <span data-ttu-id="ae124-203">在許多情況下，應用程式需要在每個框架中變更頂點或索引資料，甚至是每個框架的次數。</span><span class="sxs-lookup"><span data-stu-id="ae124-203">There are many situations where the application needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="ae124-204">在這些情況下，應該使用 D3DUSAGE 動態來建立頂點或索引緩衝區 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ae124-204">For these situations, the vertex or index buffer should be created with D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ae124-205">此使用旗標會導致 Direct3D 針對頻繁的鎖定作業進行優化。</span><span class="sxs-lookup"><span data-stu-id="ae124-205">This usage flag causes Direct3D to optimize for frequent lock operations.</span></span> <span data-ttu-id="ae124-206">D3DUSAGE \_ DYNAMIC 只適用于經常鎖定緩衝區的情況; 保持不變的資料應放置在靜態頂點或索引緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="ae124-206">D3DUSAGE\_DYNAMIC is only useful when the buffer is locked frequently; data that remains constant should be placed in a static vertex or index buffer.</span></span>

<span data-ttu-id="ae124-207">若要在使用動態頂點緩衝區時獲得效能改進，應用程式必須使用適當的旗標來呼叫 [**IDirect3DVertexBuffer9：： lock**](/windows/desktop/api) 或 [**IDirect3DIndexBuffer9：： lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) 。</span><span class="sxs-lookup"><span data-stu-id="ae124-207">To receive a performance improvement when using dynamic vertex buffers, the application must call [**IDirect3DVertexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DIndexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) with the appropriate flags.</span></span> <span data-ttu-id="ae124-208">D3DLOCK \_ 捨棄表示應用程式不需要將舊的頂點或索引資料保留在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="ae124-208">D3DLOCK\_DISCARD indicates that the application does not need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="ae124-209">如果使用 D3DLOCK 捨棄呼叫鎖定時，圖形處理器仍在使用緩衝區 \_ ，則會傳回新記憶體區域的指標，而不是舊的緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="ae124-209">If the graphics processor is still using the buffer when lock is called with D3DLOCK\_DISCARD, a pointer to a new region of memory is returned instead of the old buffer data.</span></span> <span data-ttu-id="ae124-210">這可讓圖形處理器在應用程式將資料放在新的緩衝區時，繼續使用舊的資料。</span><span class="sxs-lookup"><span data-stu-id="ae124-210">This allows the graphics processor to continue using the old data while the application places data in the new buffer.</span></span> <span data-ttu-id="ae124-211">應用程式不需要額外的記憶體管理;當圖形處理器已完成時，舊的緩衝區會自動重複使用或損毀。</span><span class="sxs-lookup"><span data-stu-id="ae124-211">No additional memory management is required in the application; the old buffer is reused or destroyed automatically when the graphics processor is finished with it.</span></span> <span data-ttu-id="ae124-212">請注意，使用 D3DLOCK 捨棄來鎖定緩衝區 \_ 一律會捨棄整個緩衝區，指定非零位移或受限大小欄位不會在緩衝區的已解除鎖定區域中保留資訊。</span><span class="sxs-lookup"><span data-stu-id="ae124-212">Note that locking a buffer with D3DLOCK\_DISCARD always discards the entire buffer, specifying a nonzero offset or limited size field does not preserve information in unlocked areas of the buffer.</span></span>

<span data-ttu-id="ae124-213">在某些情況下，應用程式每個鎖定所需儲存的資料量很小，例如新增四個頂點來轉譯 sprite。</span><span class="sxs-lookup"><span data-stu-id="ae124-213">There are cases where the amount of data the application needs to store per lock is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="ae124-214">D3DLOCK \_ NOOVERWRITE 表示應用程式不會覆寫動態緩衝區中已在使用中的資料。</span><span class="sxs-lookup"><span data-stu-id="ae124-214">D3DLOCK\_NOOVERWRITE indicates that the application will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="ae124-215">鎖定呼叫會傳回舊資料的指標，讓應用程式在頂點或索引緩衝區未使用的區域中加入新的資料。</span><span class="sxs-lookup"><span data-stu-id="ae124-215">The lock call will return a pointer to the old data, allowing the application to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="ae124-216">應用程式不應該修改繪製作業中使用的頂點或索引，因為它們可能仍由圖形處理器使用中。</span><span class="sxs-lookup"><span data-stu-id="ae124-216">The application should not modify vertices or indices used in a draw operation as they might still be in use by the graphics processor.</span></span> <span data-ttu-id="ae124-217">然後，應用程式應該在 \_ 動態緩衝區已滿時使用 D3DLOCK 捨棄，以接收新的記憶體區域，然後在圖形處理器完成後捨棄舊的頂點或索引資料。</span><span class="sxs-lookup"><span data-stu-id="ae124-217">The application should then use D3DLOCK\_DISCARD after the dynamic buffer is full to receive a new region of memory, discarding the old vertex or index data after the graphics processor is finished.</span></span>

<span data-ttu-id="ae124-218">非同步查詢機制很適合用來判斷圖形處理器是否仍在使用頂點。</span><span class="sxs-lookup"><span data-stu-id="ae124-218">The asynchronous query mechanism is useful to determine if vertices are still in use by the graphics processor.</span></span> <span data-ttu-id="ae124-219">\_在最後一個使用頂點的 DrawPrimitive 呼叫之後發出類型 D3DQUERYTYPE 事件的查詢。</span><span class="sxs-lookup"><span data-stu-id="ae124-219">Issue a query of type D3DQUERYTYPE\_EVENT after the last DrawPrimitive call that uses the vertices.</span></span> <span data-ttu-id="ae124-220">當 [**IDirect3DQuery9：：：：：：**](/windows/desktop/api) 時，不會再使用頂點 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ae124-220">The vertices are no longer in use when [**IDirect3DQuery9::GetData**](/windows/desktop/api) returns S\_OK.</span></span> <span data-ttu-id="ae124-221">使用 D3DLOCK \_ 捨棄或沒有旗標來鎖定緩衝區，一律保證頂點會與圖形處理器正確地同步處理，不過，使用沒有旗標的鎖定將會產生稍早所述的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="ae124-221">Locking a buffer with D3DLOCK\_DISCARD or no flags will always guarantee the vertices are synchronized properly with the graphics processor, however using lock without flags will incur the performance penalty described earlier.</span></span> <span data-ttu-id="ae124-222">其他 API 呼叫（例如 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api)、 [**IDirect3DDevice9：： EndScene**](/windows/desktop/api)和 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送）不保證圖形處理器已使用頂點完成。</span><span class="sxs-lookup"><span data-stu-id="ae124-222">Other API calls such as [**IDirect3DDevice9::BeginScene**](/windows/desktop/api), [**IDirect3DDevice9::EndScene**](/windows/desktop/api), and [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) do not guarantee the graphics processor is finished using vertices.</span></span>

<span data-ttu-id="ae124-223">以下是使用動態緩衝區和適當鎖定旗標的方式。</span><span class="sxs-lookup"><span data-stu-id="ae124-223">Below are ways to use dynamic buffers and the proper lock flags.</span></span>


```
    // USAGE STYLE 1
    // Discard the entire vertex buffer and refill with thousands of vertices.
    // Might contain multiple objects and/or require multiple DrawPrimitive 
    //   calls separated by state changes, etc.
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // Discard and refill the used portion of the vertex buffer.
    CONST DWORD dwLockFlags = D3DLOCK_DISCARD;
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( 0, 0, &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, nNumberOfVertices/3)
```




```
    // USAGE STYLE 2
    // Reusing one vertex buffer for multiple objects
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // No overwrite will be used if the vertices can fit into 
    //   the space remaining in the vertex buffer.
    DWORD dwLockFlags = D3DLOCK_NOOVERWRITE;
    
    // Check to see if the entire vertex buffer has been used up yet.
    if( m_nNextVertexData > m_nSizeOfVB - nSizeOfData )
    {
        // No space remains. Start over from the beginning 
        //   of the vertex buffer.
        dwLockFlags = D3DLOCK_DISCARD;
        m_nNextVertexData = 0;
    }
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( (UINT)m_nNextVertexData, nSizeOfData, 
               &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 
               m_nNextVertexData/m_nVertexStride, nNumberOfVertices/3)
 
    // Advance to the next position in the vertex buffer.
    m_nNextVertexData += nSizeOfData;
```



## <a name="using-meshes"></a><span data-ttu-id="ae124-224">使用網格</span><span class="sxs-lookup"><span data-stu-id="ae124-224">Using Meshes</span></span>

<span data-ttu-id="ae124-225">您可以使用 Direct3D 索引三角形來優化網格，而不是使用索引的三角形。</span><span class="sxs-lookup"><span data-stu-id="ae124-225">You can optimize meshes by using Direct3D indexed triangles instead of indexed triangle strips.</span></span> <span data-ttu-id="ae124-226">硬體會發現連續三角形的95% 其實形成條紋並據以調整。</span><span class="sxs-lookup"><span data-stu-id="ae124-226">The hardware will discover that 95 percent of successive triangles actually form strips and adjust accordingly.</span></span> <span data-ttu-id="ae124-227">許多驅動程式也適用于較舊的硬體。</span><span class="sxs-lookup"><span data-stu-id="ae124-227">Many drivers do this for older hardware also.</span></span>

<span data-ttu-id="ae124-228">D3DX 網格物件可以有標記有 DWORD 的每個三角形（或臉部），稱為該臉部的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae124-228">D3DX mesh objects can have each triangle, or face, tagged with a DWORD, called the attribute of that face.</span></span> <span data-ttu-id="ae124-229">DWORD 的語法是使用者定義的。</span><span class="sxs-lookup"><span data-stu-id="ae124-229">The semantics of the DWORD are user-defined.</span></span> <span data-ttu-id="ae124-230">D3DX 會使用它們來將網格分類為子集。</span><span class="sxs-lookup"><span data-stu-id="ae124-230">They are used by D3DX to classify the mesh into subsets.</span></span> <span data-ttu-id="ae124-231">應用程式會使用 [**ID3DXMesh：： LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) 呼叫來設定每一臉部屬性。</span><span class="sxs-lookup"><span data-stu-id="ae124-231">The application sets per-face attributes using the [**ID3DXMesh::LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) call.</span></span> <span data-ttu-id="ae124-232">[**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md)方法有一個選項，可使用 D3DXMESHOPT ATTRSORT 選項，將網格頂點和屬性的臉部群組在一起 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ae124-232">The [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method has an option to group the mesh vertices and faces on attributes using the D3DXMESHOPT\_ATTRSORT option.</span></span> <span data-ttu-id="ae124-233">完成此動作時，網格物件會計算可透過呼叫 [**ID3DXBaseMesh：： GetAttributeTable**](id3dxbasemesh--getattributetable.md)來取得應用程式的屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="ae124-233">When this is done, the mesh object calculates an attribute table that can be obtained by the application by calling [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md).</span></span> <span data-ttu-id="ae124-234">如果網格未依屬性排序，此呼叫會傳回0。</span><span class="sxs-lookup"><span data-stu-id="ae124-234">This call returns 0 if the mesh is not sorted by attributes.</span></span> <span data-ttu-id="ae124-235">應用程式無法設定屬性資料表，因為它是由 **ID3DXMesh：： Optimize** 方法所產生。</span><span class="sxs-lookup"><span data-stu-id="ae124-235">There is no way for an application to set an attribute table because it is generated by the **ID3DXMesh::Optimize** method.</span></span> <span data-ttu-id="ae124-236">屬性排序會區分資料，因此，如果應用程式知道網格的屬性已排序，它仍然需要呼叫 **ID3DXMesh：： Optimize** 來產生屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="ae124-236">The attribute sort is data sensitive, so if the application knows that a mesh is attribute sorted, it still needs to call **ID3DXMesh::Optimize** to generate the attribute table.</span></span>

<span data-ttu-id="ae124-237">下列主題描述網格的不同屬性。</span><span class="sxs-lookup"><span data-stu-id="ae124-237">The following topics describe the different attributes of a mesh.</span></span>

### <a name="attribute-id"></a><span data-ttu-id="ae124-238">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="ae124-238">Attribute ID</span></span>

<span data-ttu-id="ae124-239">屬性識別碼是一個值，可將臉部群組與屬性群組產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ae124-239">An attribute id is a value that associates a group of faces with an attribute group.</span></span> <span data-ttu-id="ae124-240">此識別碼描述 ID3DXBaseMesh 應繪製哪些臉部子集 [**：:D rawsubset**](id3dxbasemesh--drawsubset.md) 。</span><span class="sxs-lookup"><span data-stu-id="ae124-240">This id describes which subset of faces [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) should draw.</span></span> <span data-ttu-id="ae124-241">屬性緩衝區中的臉部會指定屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae124-241">Attribute ids are specified for the faces in the attribute buffer.</span></span> <span data-ttu-id="ae124-242">屬性識別碼的實際值可以是任何符合32位的元素，但通常會使用0到 n，其中 n 是屬性的數目。</span><span class="sxs-lookup"><span data-stu-id="ae124-242">The actual values of the attribute ids can be anything that fits in 32 bits, but it is common to use 0 to n where n is the number of attributes.</span></span>

### <a name="attribute-buffer"></a><span data-ttu-id="ae124-243">屬性緩衝區</span><span class="sxs-lookup"><span data-stu-id="ae124-243">Attribute Buffer</span></span>

<span data-ttu-id="ae124-244">屬性緩衝區是一個 Dword 陣列 (每個臉部) 一個，指定每個臉部所屬的屬性群組。</span><span class="sxs-lookup"><span data-stu-id="ae124-244">The attribute buffer is an array of DWORDs (one per face) that specifies which attribute group each face belongs in.</span></span> <span data-ttu-id="ae124-245">在建立網格時，此緩衝區會初始化為零，但會由載入常式填滿，如果需要多個識別符為0的屬性，則必須由使用者填入。</span><span class="sxs-lookup"><span data-stu-id="ae124-245">This buffer is initialized to zero on creation of a mesh, but is either filled by the load routines or must be filled by the user if more than one attribute with id 0 is desired.</span></span> <span data-ttu-id="ae124-246">此緩衝區包含用來根據 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md)中的屬性來排序網格的資訊。</span><span class="sxs-lookup"><span data-stu-id="ae124-246">This buffer contains the information that is used to sort the mesh based on attributes in [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md).</span></span> <span data-ttu-id="ae124-247">如果沒有屬性工作表存在， [**ID3DXBaseMesh：:D rawsubset**](id3dxbasemesh--drawsubset.md) 會掃描這個緩衝區，以選取要繪製之指定屬性的臉部。</span><span class="sxs-lookup"><span data-stu-id="ae124-247">If no attribute table is present, [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) scans this buffer to select the faces of the given attribute to draw.</span></span>

### <a name="attribute-table"></a><span data-ttu-id="ae124-248">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="ae124-248">Attribute Table</span></span>

<span data-ttu-id="ae124-249">屬性工作表是網格所擁有及維護的結構。</span><span class="sxs-lookup"><span data-stu-id="ae124-249">The attribute table is a structure owned and maintained by the mesh.</span></span> <span data-ttu-id="ae124-250">唯一要產生的方法，是藉由呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) with 屬性排序或增強的優化功能。</span><span class="sxs-lookup"><span data-stu-id="ae124-250">The only way for one to be generated is by calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with attribute sorting or stronger optimization enabled.</span></span> <span data-ttu-id="ae124-251">屬性工作表用來快速起始對 [**ID3DXBaseMesh：:D rawsubset**](id3dxbasemesh--drawsubset.md)的單一繪製基本呼叫。</span><span class="sxs-lookup"><span data-stu-id="ae124-251">The attribute table is used to quickly initiate a single draw primitive call to [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md).</span></span> <span data-ttu-id="ae124-252">唯一的用法是，執行中的網格也會維持此結構，因此您可以在目前的詳細資料層級查看有哪些臉部和頂點處於作用中。</span><span class="sxs-lookup"><span data-stu-id="ae124-252">The only other use is that progressing meshes also maintain this structure, so it is possible to see what faces and vertices are active at the current level of detail.</span></span>

## <a name="z-buffer-performance"></a><span data-ttu-id="ae124-253">Z 緩衝區效能</span><span class="sxs-lookup"><span data-stu-id="ae124-253">Z-Buffer Performance</span></span>

<span data-ttu-id="ae124-254">使用 z 緩衝和紋理處理時，應用程式可提高效能，藉由確保場景從前到後轉譯。</span><span class="sxs-lookup"><span data-stu-id="ae124-254">Applications can increase performance when using z-buffering and texturing by ensuring that scenes are rendered from front to back.</span></span> <span data-ttu-id="ae124-255">有紋理的 z 緩衝基本類型會針對 z 緩衝區預先測試，以掃描列為基礎。</span><span class="sxs-lookup"><span data-stu-id="ae124-255">Textured z-buffered primitives are pretested against the z-buffer on a scan line basis.</span></span> <span data-ttu-id="ae124-256">如果掃描列被掀錢轉譯的多邊形隱藏，系統會快速且有效率地拒絕它。</span><span class="sxs-lookup"><span data-stu-id="ae124-256">If a scan line is hidden by a previously rendered polygon, the system rejects it quickly and efficiently.</span></span> <span data-ttu-id="ae124-257">Z 緩衝可以提升效能，但此技術在場景多次繪製相同像素時最實用。</span><span class="sxs-lookup"><span data-stu-id="ae124-257">Z-buffering can improve performance, but the technique is most useful when a scene draws the same pixels more than once.</span></span> <span data-ttu-id="ae124-258">這很難精確計算，但是您通常可以算出近似值。</span><span class="sxs-lookup"><span data-stu-id="ae124-258">This is difficult to calculate exactly, but you can often make a close approximation.</span></span> <span data-ttu-id="ae124-259">如果相同像素繪製少於兩次，將 z 緩衝關閉並從後到前轉譯場景，將可達到最佳效能。</span><span class="sxs-lookup"><span data-stu-id="ae124-259">If the same pixels are drawn less than twice, you can achieve the best performance by turning z-buffering off and rendering the scene from back to front.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae124-260">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae124-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae124-261">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="ae124-261">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
