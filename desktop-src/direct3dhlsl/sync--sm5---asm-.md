---
title: '同步 (sm5-asm) '
description: 執行緒群組同步或記憶體屏障。
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990855"
---
# <a name="sync-sm5---asm"></a><span data-ttu-id="f819f-103">同步 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="f819f-103">sync (sm5 - asm)</span></span>

<span data-ttu-id="f819f-104">執行緒群組同步或記憶體屏障。</span><span class="sxs-lookup"><span data-stu-id="f819f-104">Thread group sync or memory barrier.</span></span>



| <span data-ttu-id="f819f-105">同步處理 \[ \_ uglobal </span><span class="sxs-lookup"><span data-stu-id="f819f-105">sync\[\_uglobal</span></span>\|<span data-ttu-id="f819f-106">\_ugroup \] \[ \_ g \] \[ \_ t\]</span><span class="sxs-lookup"><span data-stu-id="f819f-106">\_ugroup\]\[\_g\]\[\_t\]</span></span> |
|-------------------------------------------|



 

## <a name="remarks"></a><span data-ttu-id="f819f-107">備註</span><span class="sxs-lookup"><span data-stu-id="f819f-107">Remarks</span></span>

<span data-ttu-id="f819f-108">**Sync** 有選項 \_ uglobal、 \_ ugroup、 \_ g 和 \_ t。</span><span class="sxs-lookup"><span data-stu-id="f819f-108">**Sync** has options \_uglobal, \_ugroup, \_g and \_t.</span></span>

<span data-ttu-id="f819f-109">在圖元著色器中，只允許 **同步處理 \_ uglobal** 。</span><span class="sxs-lookup"><span data-stu-id="f819f-109">In the pixel shader, only **sync\_uglobal** is allowed.</span></span>

<span data-ttu-id="f819f-110">在計算著色器中， \_ 必須指定 (uglobal 或 \_ ugroup \*) 和/或 \_ g。</span><span class="sxs-lookup"><span data-stu-id="f819f-110">In the compute shader, (\_uglobal or \_ugroup\*) and/or \_g must be specified.</span></span> <span data-ttu-id="f819f-111">\_此外，t 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f819f-111">\_t is optional in addition.</span></span>

### <a name="_uglobal"></a><span data-ttu-id="f819f-112">\_uglobal</span><span class="sxs-lookup"><span data-stu-id="f819f-112">\_uglobal</span></span>

<span data-ttu-id="f819f-113">Global u \# (UAV) 記憶體隔離。</span><span class="sxs-lookup"><span data-stu-id="f819f-113">Global u\# (UAV) memory fence.</span></span>

<span data-ttu-id="f819f-114">此執行緒 \# 在程式順序中的所有先前 u 記憶體讀取/寫入，在此執行緒的任何後續 u 記憶體存取之前，都會顯示在整個 GPU 上的所有線程 \# 。</span><span class="sxs-lookup"><span data-stu-id="f819f-114">All prior u\# memory reads/writes by this thread in program order are made visible to all threads on the entire GPU before any subsequent u\# memory accesses by this thread.</span></span> <span data-ttu-id="f819f-115">在一種情況下，定義的整個 GPU 部分會以小於全域範圍取代，如下所述。</span><span class="sxs-lookup"><span data-stu-id="f819f-115">The entire GPU part of the definition is replaced by a less-than-global scope in one case, described below.</span></span>

<span data-ttu-id="f819f-116">這適用于目前的著色器階段所系結的所有 UAV 記憶體。</span><span class="sxs-lookup"><span data-stu-id="f819f-116">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="f819f-117">\_uglobal 可在計算著色器或圖元著色器中取得。</span><span class="sxs-lookup"><span data-stu-id="f819f-117">\_uglobal is available in the compute shader or pixel shader.</span></span>

<span data-ttu-id="f819f-118">若為任何系結器未以全域一致方式宣告的系結 UAV， \_ uglobal u \# 記憶體範圍只會顯示該 UAV 目前的計算著色器執行緒群組，就像是 \_ ugroup 而非 \_ uglobal 一樣。</span><span class="sxs-lookup"><span data-stu-id="f819f-118">For any bound UAV that has not been declared by the shader as Globally Coherent, the \_uglobal u\# memory fence only has visibility within the current compute shader thread-group for that UAV, as if it is \_ugroup instead of \_uglobal.</span></span> <span data-ttu-id="f819f-119">此問題僅適用于計算著色器，因為圖元著色器必須將所有 UAVs 宣告為全域一致。</span><span class="sxs-lookup"><span data-stu-id="f819f-119">This issue only applies to the compute shader, since the pixel shader must declare all UAVs as Globally Coherent.</span></span>

### <a name="_ugroup"></a><span data-ttu-id="f819f-120">\_ugroup</span><span class="sxs-lookup"><span data-stu-id="f819f-120">\_ugroup</span></span>

<span data-ttu-id="f819f-121">執行緒群組範圍 u \# (UAV) 記憶體隔離。</span><span class="sxs-lookup"><span data-stu-id="f819f-121">Thread group scope u\# (UAV) memory fence.</span></span>

<span data-ttu-id="f819f-122">在此執行緒的 \# 任何後續 u 記憶體存取之前，執行緒群組中的所有線程都可以看見執行緒群組中的所有先前 u 記憶體讀取或寫入 \# 。</span><span class="sxs-lookup"><span data-stu-id="f819f-122">All prior u\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent u\# memory accesses by this thread.</span></span>

<span data-ttu-id="f819f-123">這適用于目前的著色器階段所系結的所有 UAV 記憶體。</span><span class="sxs-lookup"><span data-stu-id="f819f-123">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="f819f-124">\_ugroup 僅適用于計算著色器。</span><span class="sxs-lookup"><span data-stu-id="f819f-124">\_ugroup is available in the compute shader only.</span></span>

<span data-ttu-id="f819f-125">如果 \_ ugroup 已公開，則適用于某些實作為。</span><span class="sxs-lookup"><span data-stu-id="f819f-125">If \_ugroup is exposed, for some implementations.</span></span> <span data-ttu-id="f819f-126">指定 \_ ugroup 而非 uglobal 的優點 \_ 是， **同步** 處理作業可以更快速完成。</span><span class="sxs-lookup"><span data-stu-id="f819f-126">The advantage of specifying \_ugroup instead of \_uglobal is that the **sync** operation can complete more quickly.</span></span>

<span data-ttu-id="f819f-127">其他的執行方式並不區分 \_ ugroup 與 \_ uglobal，因此這兩個作業都相等，而且行為類似 \_ uglobal。</span><span class="sxs-lookup"><span data-stu-id="f819f-127">Other implementations do not distinguish \_ugroup from \_uglobal, so both operations are equivalent and behave like \_uglobal.</span></span> <span data-ttu-id="f819f-128">應用程式可以要求最少的 **同步** 處理範圍來指定其意圖。</span><span class="sxs-lookup"><span data-stu-id="f819f-128">Applications can specify their intent by requesting the narrowest scope of **sync** necessary.</span></span>

<span data-ttu-id="f819f-129">即使特定 UAV 宣告為全域一致， \_ 如果不需要全域關卡，ugroup **同步** 作業在該 UAV 上的運作方式會更有效率。</span><span class="sxs-lookup"><span data-stu-id="f819f-129">Even if a particular UAV is declared as Globally Coherent, a \_ugroup **sync** operation will function more efficiently on that UAV if a global barrier is not required.</span></span>

### <a name="_g"></a><span data-ttu-id="f819f-130">\_G</span><span class="sxs-lookup"><span data-stu-id="f819f-130">\_g</span></span>

<span data-ttu-id="f819f-131">g \# (執行緒群組共用記憶體) 範圍。</span><span class="sxs-lookup"><span data-stu-id="f819f-131">g\# (thread group shared memory) fence.</span></span>

<span data-ttu-id="f819f-132">在這個執行緒的 \# 任何後續 g 記憶體存取之前，執行緒群組中的所有線程都可以看見執行緒群組中的所有先前 g 記憶體讀取或寫入 \# 。</span><span class="sxs-lookup"><span data-stu-id="f819f-132">All prior g\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent g\# memory accesses by this thread.</span></span>

<span data-ttu-id="f819f-133">這會套用至目前線程群組的 g \# 共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f819f-133">This applies to all of the current thread group's g\# shared memory.</span></span>

<span data-ttu-id="f819f-134">\_g 僅適用于計算著色器。</span><span class="sxs-lookup"><span data-stu-id="f819f-134">\_g is available in the compute shader only.</span></span>

### <a name="_t"></a><span data-ttu-id="f819f-135">\_t</span><span class="sxs-lookup"><span data-stu-id="f819f-135">\_t</span></span>

<span data-ttu-id="f819f-136">執行緒群組同步處理。單一線程群組內的所有線程 (可以共用共用暫存器空間集之存取權的執行緒) 將會執行到任何執行緒可以繼續的位置，直到到達此指令為止。</span><span class="sxs-lookup"><span data-stu-id="f819f-136">Thread group sync. All threads within a single thread group (those that can share access to a common set of shared register space) will be executed up to the point where they reach this instruction before any thread can continue.</span></span>

<span data-ttu-id="f819f-137">\_t 不能放在動態流程式控制制中， (可能會線上程群組) 內改變的分支，但是可以存在於統一的流量控制中，而群組中的所有線程都挑選相同的路徑。</span><span class="sxs-lookup"><span data-stu-id="f819f-137">\_t cannot be placed in dynamic flow control, (branches which could vary within a thread group), but can be present in uniform flow control, where all threads in the group pick the same path.</span></span>

<span data-ttu-id="f819f-138">\_t 僅適用于計算著色器。</span><span class="sxs-lookup"><span data-stu-id="f819f-138">\_t is available in the compute shader only.</span></span>

<span data-ttu-id="f819f-139">以下是計算著色器 ' sync ' 變異的清單。</span><span class="sxs-lookup"><span data-stu-id="f819f-139">The following is a listing of compute shader ‘sync’ variants.</span></span>

-   <span data-ttu-id="f819f-140">同步 \_ g</span><span class="sxs-lookup"><span data-stu-id="f819f-140">sync\_g</span></span>
-   <span data-ttu-id="f819f-141">同步 \_ ugroup\*</span><span class="sxs-lookup"><span data-stu-id="f819f-141">sync\_ugroup\*</span></span>
-   <span data-ttu-id="f819f-142">同步 \_ uglobal</span><span class="sxs-lookup"><span data-stu-id="f819f-142">sync\_uglobal</span></span>
-   <span data-ttu-id="f819f-143">同步 \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="f819f-143">sync\_g\_t</span></span>
-   <span data-ttu-id="f819f-144">同步 \_ ugroup \_ t\*</span><span class="sxs-lookup"><span data-stu-id="f819f-144">sync\_ugroup\_t\*</span></span>
-   <span data-ttu-id="f819f-145">同步 \_ uglobal \_ t</span><span class="sxs-lookup"><span data-stu-id="f819f-145">sync\_uglobal\_t</span></span>
-   <span data-ttu-id="f819f-146">同步 \_ ugroup \_ g\*</span><span class="sxs-lookup"><span data-stu-id="f819f-146">sync\_ugroup\_g\*</span></span>
-   <span data-ttu-id="f819f-147">同步 \_ uglobal \_ g</span><span class="sxs-lookup"><span data-stu-id="f819f-147">sync\_uglobal\_g</span></span>
-   <span data-ttu-id="f819f-148">同步 \_ ugroup \_ g \_ t\*</span><span class="sxs-lookup"><span data-stu-id="f819f-148">sync\_ugroup\_g\_t\*</span></span>
-   <span data-ttu-id="f819f-149">同步 \_ uglobal \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="f819f-149">sync\_uglobal\_g\_t</span></span>

<span data-ttu-id="f819f-150">\*\_HLSL 編譯器可能不會根據 \_ 上述 ugroup 一節中的先前討論，將具有 ugroup 的變體設為目標。</span><span class="sxs-lookup"><span data-stu-id="f819f-150">\*Variants with \_ugroup may not be targeted by the HLSL compiler, per the earlier discussion in the \_ugroup section above.</span></span>

<span data-ttu-id="f819f-151">圖元著色器同步變異清單僅包含 sync \_ uglobal。</span><span class="sxs-lookup"><span data-stu-id="f819f-151">Listing of pixel shader sync variants include sync\_uglobal only.</span></span>

<span data-ttu-id="f819f-152">記憶體不足會防止受影響的指令在整個範圍內由編譯器或硬體重新排序。</span><span class="sxs-lookup"><span data-stu-id="f819f-152">Memory fences prevent affected instructions from being reordered by compilers or hardware across the fence.</span></span>

<span data-ttu-id="f819f-153">從相同位址讀取的多個資料，不會被記憶體阻礙或寫入位址的多個資料，也可以一起折迭。</span><span class="sxs-lookup"><span data-stu-id="f819f-153">Multiple reads from the same address by a shader invocation that are not separated by memory barriers or writes to the address can be collapsed together.</span></span> <span data-ttu-id="f819f-154">這同樣適用於寫入。</span><span class="sxs-lookup"><span data-stu-id="f819f-154">The same applies to writes.</span></span> <span data-ttu-id="f819f-155">以關卡分隔的存取權無法在關卡之間合併或移動。</span><span class="sxs-lookup"><span data-stu-id="f819f-155">Accesses separated by a barrier cannot be merged or moved across the barrier.</span></span>

<span data-ttu-id="f819f-156">由不同執行緒正常運作的指定位址不可部分完成的作業，不需要記憶體不足的情況。</span><span class="sxs-lookup"><span data-stu-id="f819f-156">Memory fences are not necessary for atomic operations to a given address by different threads to function correctly.</span></span> <span data-ttu-id="f819f-157">當 atomics 和（或）載入/存放區作業從其他執行緒的觀點來看，在個別的執行緒中出現時，就需要使用此功能。</span><span class="sxs-lookup"><span data-stu-id="f819f-157">Fences are needed when atomics and/or load/store operations need to be synchronized with respect to each other as they appear in individual threads from the point of view of other threads.</span></span>

<span data-ttu-id="f819f-158">在圖元著色器中， [捨棄](discard--sm4---asm-.md) 指示表示同步 \_ uglobal 範圍，在此指示中，無法在 **捨棄** 期間重新排序。</span><span class="sxs-lookup"><span data-stu-id="f819f-158">In the pixel shader, [discard](discard--sm4---asm-.md) instructions imply a sync\_uglobal fence, in that instructions cannot be reordered across the **discard**.</span></span> <span data-ttu-id="f819f-159">在協助程式 \_ 圖元 (同步處理 uglobal，此功能僅執行來支援衍生) 或捨棄的圖元可能不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="f819f-159">sync\_uglobal in helper pixels (which run only to support derivatives) or discarded pixels may or may not have any affect.</span></span> <span data-ttu-id="f819f-160">系統不允許協助程式或捨棄的圖元寫入至 UAVs （如果捨棄的話），寫入會在捨棄之後發出。</span><span class="sxs-lookup"><span data-stu-id="f819f-160">It is not allowed for helper or discarded pixels to write to UAVs if, in the case of discard, the writes are issued after the discard.</span></span> <span data-ttu-id="f819f-161">從 UAVs 傳回的值不能參與衍生計算。</span><span class="sxs-lookup"><span data-stu-id="f819f-161">Returned values from UAVs are not allowed to contribute to derivative calculations.</span></span> <span data-ttu-id="f819f-162">因此，不論是否接受同步處理 \_ u，helper 圖元或捨棄之後發出的想法。</span><span class="sxs-lookup"><span data-stu-id="f819f-162">Therefore whether or not sync\_u is honored for helper pixels or when issued after a discard is moot.</span></span>

<span data-ttu-id="f819f-163">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此指令。</span><span class="sxs-lookup"><span data-stu-id="f819f-163">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="f819f-164">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f819f-164">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f819f-165">頂點</span><span class="sxs-lookup"><span data-stu-id="f819f-165">Vertex</span></span> | <span data-ttu-id="f819f-166">船體</span><span class="sxs-lookup"><span data-stu-id="f819f-166">Hull</span></span> | <span data-ttu-id="f819f-167">網域</span><span class="sxs-lookup"><span data-stu-id="f819f-167">Domain</span></span> | <span data-ttu-id="f819f-168">幾何</span><span class="sxs-lookup"><span data-stu-id="f819f-168">Geometry</span></span> | <span data-ttu-id="f819f-169">像素</span><span class="sxs-lookup"><span data-stu-id="f819f-169">Pixel</span></span> | <span data-ttu-id="f819f-170">計算</span><span class="sxs-lookup"><span data-stu-id="f819f-170">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f819f-171">X</span><span class="sxs-lookup"><span data-stu-id="f819f-171">X</span></span>     | <span data-ttu-id="f819f-172">X</span><span class="sxs-lookup"><span data-stu-id="f819f-172">X</span></span>       |



 

<span data-ttu-id="f819f-173">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指令的 **同步 \_ uglobal** 變體適用于 direct3d 11.1 執行時間的所有著色器階段（從 Windows 8 開始提供）。</span><span class="sxs-lookup"><span data-stu-id="f819f-173">Because UAVs are available at all shader stages for Direct3D 11.1, the **sync\_uglobal** variant of this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f819f-174">頂點</span><span class="sxs-lookup"><span data-stu-id="f819f-174">Vertex</span></span> | <span data-ttu-id="f819f-175">船體</span><span class="sxs-lookup"><span data-stu-id="f819f-175">Hull</span></span> | <span data-ttu-id="f819f-176">網域</span><span class="sxs-lookup"><span data-stu-id="f819f-176">Domain</span></span> | <span data-ttu-id="f819f-177">幾何</span><span class="sxs-lookup"><span data-stu-id="f819f-177">Geometry</span></span> | <span data-ttu-id="f819f-178">像素</span><span class="sxs-lookup"><span data-stu-id="f819f-178">Pixel</span></span> | <span data-ttu-id="f819f-179">計算</span><span class="sxs-lookup"><span data-stu-id="f819f-179">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f819f-180">X</span><span class="sxs-lookup"><span data-stu-id="f819f-180">X</span></span>      | <span data-ttu-id="f819f-181">X</span><span class="sxs-lookup"><span data-stu-id="f819f-181">X</span></span>    | <span data-ttu-id="f819f-182">X</span><span class="sxs-lookup"><span data-stu-id="f819f-182">X</span></span>      | <span data-ttu-id="f819f-183">X</span><span class="sxs-lookup"><span data-stu-id="f819f-183">X</span></span>        | <span data-ttu-id="f819f-184">X</span><span class="sxs-lookup"><span data-stu-id="f819f-184">X</span></span>     | <span data-ttu-id="f819f-185">X</span><span class="sxs-lookup"><span data-stu-id="f819f-185">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f819f-186">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f819f-186">Minimum Shader Model</span></span>

<span data-ttu-id="f819f-187">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="f819f-187">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f819f-188">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f819f-188">Shader Model</span></span>                                              | <span data-ttu-id="f819f-189">支援</span><span class="sxs-lookup"><span data-stu-id="f819f-189">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f819f-190">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f819f-190">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f819f-191">是</span><span class="sxs-lookup"><span data-stu-id="f819f-191">yes</span></span>       |
| [<span data-ttu-id="f819f-192">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f819f-192">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f819f-193">不可以</span><span class="sxs-lookup"><span data-stu-id="f819f-193">no</span></span>        |
| [<span data-ttu-id="f819f-194">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f819f-194">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f819f-195">不可以</span><span class="sxs-lookup"><span data-stu-id="f819f-195">no</span></span>        |
| [<span data-ttu-id="f819f-196">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f819f-196">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f819f-197">不可以</span><span class="sxs-lookup"><span data-stu-id="f819f-197">no</span></span>        |
| [<span data-ttu-id="f819f-198">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f819f-198">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f819f-199">不可以</span><span class="sxs-lookup"><span data-stu-id="f819f-199">no</span></span>        |
| [<span data-ttu-id="f819f-200">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f819f-200">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f819f-201">不可以</span><span class="sxs-lookup"><span data-stu-id="f819f-201">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f819f-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="f819f-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f819f-203">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f819f-203">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




