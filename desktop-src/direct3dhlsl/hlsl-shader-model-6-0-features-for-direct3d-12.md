---
title: HLSL 著色器模型6。0
description: 描述新增至 HLSL 著色器模型6.0 的 wave 作業內建。
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d082fc131c7cd08db9eb1861c4af39d600f40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971725"
---
# <a name="hlsl-shader-model-60"></a><span data-ttu-id="311f6-103">HLSL 著色器模型6。0</span><span class="sxs-lookup"><span data-stu-id="311f6-103">HLSL Shader Model 6.0</span></span>

<span data-ttu-id="311f6-104">描述新增至 HLSL 著色器模型6.0 的 wave 作業內建。</span><span class="sxs-lookup"><span data-stu-id="311f6-104">Describes the wave operation intrinsics added to HLSL Shader Model 6.0.</span></span>

- [<span data-ttu-id="311f6-105">著色器模型6。0</span><span class="sxs-lookup"><span data-stu-id="311f6-105">Shader model 6.0</span></span>](#shader-model-60)
- [<span data-ttu-id="311f6-106">術語</span><span class="sxs-lookup"><span data-stu-id="311f6-106">Terminology</span></span>](#terminology)
- [<span data-ttu-id="311f6-107">網底語言內建函式</span><span class="sxs-lookup"><span data-stu-id="311f6-107">Shading language intrinsics</span></span>](#shading-language-intrinsics)
    - [<span data-ttu-id="311f6-108">Wave 查詢</span><span class="sxs-lookup"><span data-stu-id="311f6-108">Wave Query</span></span>](#wave-query)
    - [<span data-ttu-id="311f6-109">Wave 投票</span><span class="sxs-lookup"><span data-stu-id="311f6-109">Wave Vote</span></span>](#wave-vote)
    - [<span data-ttu-id="311f6-110">Wave 廣播</span><span class="sxs-lookup"><span data-stu-id="311f6-110">Wave Broadcast</span></span>](#wave-broadcast)
    - [<span data-ttu-id="311f6-111">減少 Wave</span><span class="sxs-lookup"><span data-stu-id="311f6-111">Wave Reduction</span></span>](#wave-reduction)
    - [<span data-ttu-id="311f6-112">Wave 掃描和前置詞</span><span class="sxs-lookup"><span data-stu-id="311f6-112">Wave Scan and Prefix</span></span>](#wave-scan-and-prefix)
    - [<span data-ttu-id="311f6-113">四個全半隨機作業</span><span class="sxs-lookup"><span data-stu-id="311f6-113">Quad-wide Shuffle operations</span></span>](#quad-wide-shuffle-operations)
- [<span data-ttu-id="311f6-114">硬體功能</span><span class="sxs-lookup"><span data-stu-id="311f6-114">Hardware capability</span></span>](#hardware-capability)
- [<span data-ttu-id="311f6-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="311f6-115">Related topics</span></span>](#related-topics)

## <a name="shader-model-60"></a><span data-ttu-id="311f6-116">著色器模型6。0</span><span class="sxs-lookup"><span data-stu-id="311f6-116">Shader Model 6.0</span></span>

<span data-ttu-id="311f6-117">針對較早的著色器模型，HLSL 程式設計只會公開單一執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="311f6-117">For earlier shader models, HLSL programming exposes only a single thread of execution.</span></span> <span data-ttu-id="311f6-118">從模型6.0 開始提供新的 wave 層級作業，以明確利用目前 Gpu 的平行處理原則-許多執行緒可以同時在相同核心上的密集建置中執行。</span><span class="sxs-lookup"><span data-stu-id="311f6-118">New wave-level operations are provided, starting with model 6.0, to explicitly take advantage of the parallelism of current GPUs - many threads can be executing in lockstep on the same core simultaneously.</span></span> <span data-ttu-id="311f6-119">例如，當同步處理的範圍在 SIMD 處理器的寬度內，或某些其他已知為不可部分完成的執行緒時，模型6.0 內建函式可讓您排除關卡結構。</span><span class="sxs-lookup"><span data-stu-id="311f6-119">For example, the model 6.0 intrinsics enable the elimination of barrier constructs when the scope of synchronization is within the width of the SIMD processor, or some other set of threads that are known to be atomic relative to each other.</span></span>

<span data-ttu-id="311f6-120">可能的使用案例包括：資料流程壓縮、縮減、區塊變換、bitonic 排序或快速傅立葉轉換 (FFT) 、分類收納、串流消除重複和類似案例。</span><span class="sxs-lookup"><span data-stu-id="311f6-120">Potential use cases include: stream compaction, reductions, block transpose, bitonic sort or Fast Fourier Transforms (FFT), binning, stream de-duplication, and similar scenarios.</span></span>

<span data-ttu-id="311f6-121">大部分的內建函式都會出現在圖元著色器和計算著色器中，但 (針對每個函式) 注明一些例外狀況。</span><span class="sxs-lookup"><span data-stu-id="311f6-121">Most of the intrinsics appear in pixel shaders and compute shaders, though there are some exceptions (noted for each function).</span></span> <span data-ttu-id="311f6-122">這些函式已新增至在 API 層級12下的 DirectX 功能等級12.0 需求。</span><span class="sxs-lookup"><span data-stu-id="311f6-122">The functions have been added to the requirements for DirectX Feature Level 12.0, under API level 12.</span></span>

<span data-ttu-id="311f6-123">這些函式的 *<type>* 參數和傳回值意指運算式的類型，支援的型別是下列清單中 *也* 存在於您應用程式的目標著色器模型中的類型：</span><span class="sxs-lookup"><span data-stu-id="311f6-123">The *<type>* parameter and return value for these functions implies the type of the expression, the supported types are those from the following list that are *also* present in the target shader model for your app:</span></span>

- <span data-ttu-id="311f6-124">半、half2、half3、half4</span><span class="sxs-lookup"><span data-stu-id="311f6-124">half, half2, half3, half4</span></span>
- <span data-ttu-id="311f6-125">float、float2、float3、float4</span><span class="sxs-lookup"><span data-stu-id="311f6-125">float, float2, float3, float4</span></span>
- <span data-ttu-id="311f6-126">double、double2、double3、double4</span><span class="sxs-lookup"><span data-stu-id="311f6-126">double, double2, double3, double4</span></span>
- <span data-ttu-id="311f6-127">int、int2、int3、int4</span><span class="sxs-lookup"><span data-stu-id="311f6-127">int, int2, int3, int4</span></span>
- <span data-ttu-id="311f6-128">uint、uint2、uint3、uint4</span><span class="sxs-lookup"><span data-stu-id="311f6-128">uint, uint2, uint3, uint4</span></span>
- <span data-ttu-id="311f6-129">short、short2、short3、short4</span><span class="sxs-lookup"><span data-stu-id="311f6-129">short, short2, short3, short4</span></span>
- <span data-ttu-id="311f6-130">ushort、ushort2、ushort3、ushort4</span><span class="sxs-lookup"><span data-stu-id="311f6-130">ushort, ushort2, ushort3, ushort4</span></span>
- <span data-ttu-id="311f6-131">uint64 \_ t、uint64 \_ t2、uint64 \_ t3、uint64 \_ t4</span><span class="sxs-lookup"><span data-stu-id="311f6-131">uint64\_t, uint64\_t2, uint64\_t3, uint64\_t4</span></span>

<span data-ttu-id="311f6-132">某些作業 (例如位運算子) 只支援整數類型。</span><span class="sxs-lookup"><span data-stu-id="311f6-132">Some operations (such as the bitwise operators) only support the integer types.</span></span>

## <a name="terminology"></a><span data-ttu-id="311f6-133">詞彙</span><span class="sxs-lookup"><span data-stu-id="311f6-133">Terminology</span></span>

| | |
|-|-|
| <span data-ttu-id="311f6-134">**字詞**</span><span class="sxs-lookup"><span data-stu-id="311f6-134">**Term**</span></span> | <span data-ttu-id="311f6-135">**[定義]**</span><span class="sxs-lookup"><span data-stu-id="311f6-135">**Definition**</span></span> |
| <span data-ttu-id="311f6-136">車道</span><span class="sxs-lookup"><span data-stu-id="311f6-136">Lane</span></span> | <span data-ttu-id="311f6-137">單一線程執行。</span><span class="sxs-lookup"><span data-stu-id="311f6-137">A single thread of execution.</span></span> <span data-ttu-id="311f6-138">6.0 版之前的著色器模型只會在語言層級公開上述其中一種模型，讓您完全擴充至平行 SIMD 處理以執行。</span><span class="sxs-lookup"><span data-stu-id="311f6-138">The shader models before version 6.0 expose only one of these at the language level, leaving expansion to parallel SIMD processing entirely up to the implementation.</span></span> |
| <span data-ttu-id="311f6-139">Wave</span><span class="sxs-lookup"><span data-stu-id="311f6-139">Wave</span></span> | <span data-ttu-id="311f6-140">在處理器中) 同時執行的一組通道 (執行緒。</span><span class="sxs-lookup"><span data-stu-id="311f6-140">A set of lanes (threads) executed simultaneously in the processor.</span></span> <span data-ttu-id="311f6-141">不需要明確的阻礙，以確保它們會以平行方式執行。</span><span class="sxs-lookup"><span data-stu-id="311f6-141">No explicit barriers are required to guarantee that they execute in parallel.</span></span> <span data-ttu-id="311f6-142">類似的概念包括「變形」和「wavefront」。</span><span class="sxs-lookup"><span data-stu-id="311f6-142">Similar concepts include "warp" and "wavefront."</span></span> |
| <span data-ttu-id="311f6-143">非使用中航道</span><span class="sxs-lookup"><span data-stu-id="311f6-143">Inactive Lane</span></span> | <span data-ttu-id="311f6-144">未執行的通道，例如因為控制流程，或沒有足夠的工作來填滿 wave 的大小下限。</span><span class="sxs-lookup"><span data-stu-id="311f6-144">A lane which is not being executed, for example due to the flow of control, or insufficient work to fill the minimum size of the wave.</span></span> |
| <span data-ttu-id="311f6-145">使用中車道</span><span class="sxs-lookup"><span data-stu-id="311f6-145">Active Lane</span></span> | <span data-ttu-id="311f6-146">正在執行執行的通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-146">A lane for which execution is being performed.</span></span> <span data-ttu-id="311f6-147">在圖元著色器中，它可能包含任何協助程式圖元車道。</span><span class="sxs-lookup"><span data-stu-id="311f6-147">In pixel shaders, it may include any helper pixel lanes.</span></span> |
| <span data-ttu-id="311f6-148">四</span><span class="sxs-lookup"><span data-stu-id="311f6-148">Quad</span></span> | <span data-ttu-id="311f6-149">一組4個連續的通道，對應至以2x2 正方形排列的圖元。</span><span class="sxs-lookup"><span data-stu-id="311f6-149">A set of 4 adjacent lanes corresponding to pixels arranged in a 2x2 square.</span></span> <span data-ttu-id="311f6-150">它們是用來依 x 或 y 差異來預估漸層。</span><span class="sxs-lookup"><span data-stu-id="311f6-150">They are used to estimate gradients by differencing in either x or y.</span></span> <span data-ttu-id="311f6-151">Wave 可能由多個四邊形組成。</span><span class="sxs-lookup"><span data-stu-id="311f6-151">A wave may be comprised of multiple quads.</span></span> <span data-ttu-id="311f6-152">作用中的四個圖元中的所有圖元都 (執行，而且可能是「使用中通道」 ) ，但不會產生可見結果的圖元稱為「協助程式通道」。</span><span class="sxs-lookup"><span data-stu-id="311f6-152">All pixels in an active quad are executed (and may be "Active Lanes"), but those that do not produce visible results are termed "Helper Lanes".</span></span> |
| <span data-ttu-id="311f6-153">Helper 航道</span><span class="sxs-lookup"><span data-stu-id="311f6-153">Helper Lane</span></span> | <span data-ttu-id="311f6-154">僅針對圖元著色器四邊形中的漸層用途而執行的通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-154">A lane which is executed solely for the purpose of gradients in pixel shader quads.</span></span> <span data-ttu-id="311f6-155">這類通道的輸出將會被捨棄，因此不會轉譯為目的介面。</span><span class="sxs-lookup"><span data-stu-id="311f6-155">The output of such a lane will be discarded, and so not render to the destination surface.</span></span> |

## <a name="shading-language-intrinsics"></a><span data-ttu-id="311f6-156">網底語言內建函式</span><span class="sxs-lookup"><span data-stu-id="311f6-156">Shading language intrinsics</span></span>

<span data-ttu-id="311f6-157">此著色器模型的所有作業都已新增至範圍內的內建函式。</span><span class="sxs-lookup"><span data-stu-id="311f6-157">All the operations of this shader model have been added in a range of intrinsic functions.</span></span>

### <a name="wave-query"></a><span data-ttu-id="311f6-158">Wave 查詢</span><span class="sxs-lookup"><span data-stu-id="311f6-158">Wave Query</span></span>

<span data-ttu-id="311f6-159">查詢單一 wave 的內建函式。</span><span class="sxs-lookup"><span data-stu-id="311f6-159">The intrinsics for querying a single wave.</span></span>

| | | | |
|-|-|-|-|
| <span data-ttu-id="311f6-160">**內建**</span><span class="sxs-lookup"><span data-stu-id="311f6-160">**Intrinsic**</span></span> | <span data-ttu-id="311f6-161">**說明**</span><span class="sxs-lookup"><span data-stu-id="311f6-161">**Description**</span></span> | <span data-ttu-id="311f6-162">**像素著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-162">**Pixel shader**</span></span> | <span data-ttu-id="311f6-163">**計算著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-163">**Compute shader**</span></span> |
| [<span data-ttu-id="311f6-164">**WaveGetLaneCount**</span><span class="sxs-lookup"><span data-stu-id="311f6-164">**WaveGetLaneCount**</span></span>](wavegetlanecount.md) | <span data-ttu-id="311f6-165">傳回目前 wave 中的航道數目。</span><span class="sxs-lookup"><span data-stu-id="311f6-165">Returns the number of lanes in the current wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-166">**WaveGetLaneIndex**</span><span class="sxs-lookup"><span data-stu-id="311f6-166">**WaveGetLaneIndex**</span></span>](wavegetlaneindex.md) | <span data-ttu-id="311f6-167">傳回目前 wave 內目前通道的索引。</span><span class="sxs-lookup"><span data-stu-id="311f6-167">Returns the index of the current lane within the current wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-168">**WaveIsFirstLane**</span><span class="sxs-lookup"><span data-stu-id="311f6-168">**WaveIsFirstLane**</span></span>](waveisfirstlane.md) | <span data-ttu-id="311f6-169">只針對目前 wave 中具有最小索引的現用通道傳回 true</span><span class="sxs-lookup"><span data-stu-id="311f6-169">Returns true only for the active lane in the current wave with the smallest index</span></span> | \* | \* |

### <a name="wave-vote"></a><span data-ttu-id="311f6-170">Wave 投票</span><span class="sxs-lookup"><span data-stu-id="311f6-170">Wave Vote</span></span>

<span data-ttu-id="311f6-171">這一組內建函式會比較目前在目前使用中的執行緒之間的值。</span><span class="sxs-lookup"><span data-stu-id="311f6-171">This set of intrinsics compare values across threads currently active from the current wave.</span></span>

| | | | |
|-|-|-|-|
| <span data-ttu-id="311f6-172">**內建**</span><span class="sxs-lookup"><span data-stu-id="311f6-172">**Intrinsic**</span></span> | <span data-ttu-id="311f6-173">**說明**</span><span class="sxs-lookup"><span data-stu-id="311f6-173">**Description**</span></span> | <span data-ttu-id="311f6-174">**像素著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-174">**Pixel shader**</span></span> | <span data-ttu-id="311f6-175">**計算著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-175">**Compute shader**</span></span> |
| [<span data-ttu-id="311f6-176">**WaveActiveAnyTrue**</span><span class="sxs-lookup"><span data-stu-id="311f6-176">**WaveActiveAnyTrue**</span></span>](waveanytrue.md) | <span data-ttu-id="311f6-177">如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="311f6-177">Returns true if the expression is true in any active lane in the current wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-178">**WaveActiveAllTrue**</span><span class="sxs-lookup"><span data-stu-id="311f6-178">**WaveActiveAllTrue**</span></span>](wavealltrue.md) | <span data-ttu-id="311f6-179">如果目前 wave 的所有作用中通道中的運算式為 true，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="311f6-179">Returns true if the expression is true in all active lanes in the current wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-180">**WaveActiveBallot**</span><span class="sxs-lookup"><span data-stu-id="311f6-180">**WaveActiveBallot**</span></span>](waveballot.md) | <span data-ttu-id="311f6-181">針對指定 wave 中所有使用中的通道，傳回布林運算式評估的64位不帶正負號的整數位遮罩。</span><span class="sxs-lookup"><span data-stu-id="311f6-181">Returns a 64-bit unsigned integer bitmask of the evaluation of the Boolean expression for all active lanes in the specified wave.</span></span> | \* | \* |

### <a name="wave-broadcast"></a><span data-ttu-id="311f6-182">Wave 廣播</span><span class="sxs-lookup"><span data-stu-id="311f6-182">Wave Broadcast</span></span>

<span data-ttu-id="311f6-183">這些內建函式可讓目前 wave 中的所有使用中通道，從指定的通道接收值，有效地將其廣播。</span><span class="sxs-lookup"><span data-stu-id="311f6-183">These intrinsics enable all active lanes in the current wave to receive the value from the specified lane, effectively broadcasting it.</span></span> <span data-ttu-id="311f6-184">來自無效通道的傳回值未定義。</span><span class="sxs-lookup"><span data-stu-id="311f6-184">The return value from an invalid lane is undefined.</span></span>

| | | | |
|-|-|-|-|
| <span data-ttu-id="311f6-185">**內建**</span><span class="sxs-lookup"><span data-stu-id="311f6-185">**Intrinsic**</span></span> | <span data-ttu-id="311f6-186">**說明**</span><span class="sxs-lookup"><span data-stu-id="311f6-186">**Description**</span></span> | <span data-ttu-id="311f6-187">**像素著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-187">**Pixel shader**</span></span> | <span data-ttu-id="311f6-188">**計算著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-188">**Compute shader**</span></span> |
| [<span data-ttu-id="311f6-189">**WaveReadLaneAt**</span><span class="sxs-lookup"><span data-stu-id="311f6-189">**WaveReadLaneAt**</span></span>](wavereadlaneat.md) | <span data-ttu-id="311f6-190">傳回指定 wave 內給定通道索引的運算式值。</span><span class="sxs-lookup"><span data-stu-id="311f6-190">Returns the value of the expression for the given lane index within the specified wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-191">**WaveReadLaneFirst**</span><span class="sxs-lookup"><span data-stu-id="311f6-191">**WaveReadLaneFirst**</span></span>](wavereadfirstlane.md) | <span data-ttu-id="311f6-192">傳回目前 wave （具有最小索引）之使用中通道的運算式值。</span><span class="sxs-lookup"><span data-stu-id="311f6-192">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span> | \* | \* |

### <a name="wave-reduction"></a><span data-ttu-id="311f6-193">減少 Wave</span><span class="sxs-lookup"><span data-stu-id="311f6-193">Wave Reduction</span></span>

<span data-ttu-id="311f6-194">這些內建函式會在 wave 中的所有使用中通道上計算指定的作業，並將最終結果廣播到所有使用中的通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-194">These intrinsics compute the specified operation across all active lanes in the wave and broadcast the final result to all active lanes.</span></span> <span data-ttu-id="311f6-195">因此，最終的輸出保證會在 wave 之間保持一致。</span><span class="sxs-lookup"><span data-stu-id="311f6-195">Therefore, the final output is guaranteed uniform across the wave.</span></span>

| | | | |
|-|-|-|-|
| <span data-ttu-id="311f6-196">**內建**</span><span class="sxs-lookup"><span data-stu-id="311f6-196">**Intrinsic**</span></span> | <span data-ttu-id="311f6-197">**說明**</span><span class="sxs-lookup"><span data-stu-id="311f6-197">**Description**</span></span> | <span data-ttu-id="311f6-198">**像素著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-198">**Pixel shader**</span></span> | <span data-ttu-id="311f6-199">**計算著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-199">**Compute shader**</span></span> |
| [<span data-ttu-id="311f6-200">**WaveActiveAllEqual**</span><span class="sxs-lookup"><span data-stu-id="311f6-200">**WaveActiveAllEqual**</span></span>](waveactiveallequal.md) | <span data-ttu-id="311f6-201">如果目前 wave (中的每個使用中通道的運算式相同，則會傳回 true，因此) 之間保持一致。</span><span class="sxs-lookup"><span data-stu-id="311f6-201">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span> | \* | \* |
| [<span data-ttu-id="311f6-202">**WaveActiveBitAnd**</span><span class="sxs-lookup"><span data-stu-id="311f6-202">**WaveActiveBitAnd**</span></span>](waveallbitand.md) | <span data-ttu-id="311f6-203">傳回目前 wave 中所有使用中通道的所有運算式值的位 AND，然後將結果複製到 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-203">Returns the bitwise AND of all the values of the expression across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-204">**WaveActiveBitOr**</span><span class="sxs-lookup"><span data-stu-id="311f6-204">**WaveActiveBitOr**</span></span>](waveallbitor.md) | <span data-ttu-id="311f6-205">傳回目前 wave 中所有使用中通道之所有運算式值的位 OR，並且將結果複寫至 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-205">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-206">**WaveActiveBitXor**</span><span class="sxs-lookup"><span data-stu-id="311f6-206">**WaveActiveBitXor**</span></span>](waveallbitxor.md) | <span data-ttu-id="311f6-207">傳回目前 wave 中所有使用中通道的所有運算式值的位互斥 OR，並將結果複寫至 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-207">Returns the bitwise Exclusive OR of all the values of the expression across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-208">**WaveActiveCountBits**</span><span class="sxs-lookup"><span data-stu-id="311f6-208">**WaveActiveCountBits**</span></span>](waveactivecountbits.md) | <span data-ttu-id="311f6-209">計算在目前 wave 的所有作用中通道上評估為 true 的布林值變數數目，並將結果複製到 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-209">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-210">**WaveActiveMax**</span><span class="sxs-lookup"><span data-stu-id="311f6-210">**WaveActiveMax**</span></span>](waveallmax.md) | <span data-ttu-id="311f6-211">計算目前 wave 中所有使用中通道的運算式最大值，並將結果複製到 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-211">Computes the maximum value of the expression across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-212">**WaveActiveMin**</span><span class="sxs-lookup"><span data-stu-id="311f6-212">**WaveActiveMin**</span></span>](waveallmin.md) | <span data-ttu-id="311f6-213">計算目前 wave 中所有使用中通道的運算式最小值，並將結果複寫至 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-213">Computes the minimum value of the expression across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-214">**WaveActiveProduct**</span><span class="sxs-lookup"><span data-stu-id="311f6-214">**WaveActiveProduct**</span></span>](waveallproduct.md) | <span data-ttu-id="311f6-215">將運算式的值與目前 wave 中的所有使用中車道相乘，並將結果複寫至 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-215">Multiplies the values of the expression together across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-216">**WaveActiveSum**</span><span class="sxs-lookup"><span data-stu-id="311f6-216">**WaveActiveSum**</span></span>](waveallsum.md) | <span data-ttu-id="311f6-217">加總目前 wave 中所有使用中通道的運算式值，並將其複製到目前 wave 中的所有通道，並將結果複寫至 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="311f6-217">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave, and replicates the result to all lanes in the wave.</span></span> | \* | \* |

### <a name="wave-scan-and-prefix"></a><span data-ttu-id="311f6-218">Wave 掃描和前置詞</span><span class="sxs-lookup"><span data-stu-id="311f6-218">Wave Scan and Prefix</span></span>

<span data-ttu-id="311f6-219">這些內建函式會將作業套用到每個通道，並將計算的每個部分結果保留在對應的通道中。</span><span class="sxs-lookup"><span data-stu-id="311f6-219">These intrinsics apply the operation to each lane and leave each partial result of the computation in the corresponding lane.</span></span>

| | | | |
|-|-|-|-|
| <span data-ttu-id="311f6-220">**內建**</span><span class="sxs-lookup"><span data-stu-id="311f6-220">**Intrinsic**</span></span> | <span data-ttu-id="311f6-221">**說明**</span><span class="sxs-lookup"><span data-stu-id="311f6-221">**Description**</span></span> | <span data-ttu-id="311f6-222">**像素著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-222">**Pixel shader**</span></span> | <span data-ttu-id="311f6-223">**計算著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-223">**Compute shader**</span></span> |
| [<span data-ttu-id="311f6-224">**WavePrefixCountBits**</span><span class="sxs-lookup"><span data-stu-id="311f6-224">**WavePrefixCountBits**</span></span>](waveprefixcountbytes.md) | <span data-ttu-id="311f6-225">傳回所有在所有作用中的通道上，所有指定的布林值變數設定為 true 的總和，其索引小於目前的航道。</span><span class="sxs-lookup"><span data-stu-id="311f6-225">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-226">**WavePrefixSum**</span><span class="sxs-lookup"><span data-stu-id="311f6-226">**WavePrefixSum**</span></span>](waveprefixsum.md) | <span data-ttu-id="311f6-227">傳回使用中通道的所有值加上小於此值的總和。</span><span class="sxs-lookup"><span data-stu-id="311f6-227">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span> | \* | \* |
| [<span data-ttu-id="311f6-228">**WavePrefixProduct**</span><span class="sxs-lookup"><span data-stu-id="311f6-228">**WavePrefixProduct**</span></span>](waveprefixproduct.md) | <span data-ttu-id="311f6-229">傳回信道中這個指定 wave 之前的所有值的乘積。</span><span class="sxs-lookup"><span data-stu-id="311f6-229">Returns the product of all of the values in the lanes before this one of the specified wave.</span></span> | \* | \* |

### <a name="quad-wide-shuffle-operations"></a><span data-ttu-id="311f6-230">四個全半隨機作業</span><span class="sxs-lookup"><span data-stu-id="311f6-230">Quad-wide Shuffle operations</span></span>

<span data-ttu-id="311f6-231">這些內建函式會對已知包含圖元著色器四邊形的所有值執行交換作業，如這裡所定義。</span><span class="sxs-lookup"><span data-stu-id="311f6-231">These intrinsics perform swap operations on the values across a wave known to contain pixel shader quads as defined here.</span></span> <span data-ttu-id="311f6-232">四個四個圖元的索引定義于掃描行或讀取順序中，四個中的座標如下：</span><span class="sxs-lookup"><span data-stu-id="311f6-232">The indices of the pixels in the quad are defined in scan-line or reading order - where the coordinates within a quad are:</span></span>

<span data-ttu-id="311f6-233">+---------> X</span><span class="sxs-lookup"><span data-stu-id="311f6-233">+---------> X</span></span> 

<span data-ttu-id="311f6-234">|[0] [1]</span><span class="sxs-lookup"><span data-stu-id="311f6-234">| [0] [1]</span></span> 

<span data-ttu-id="311f6-235">|[2] [3]</span><span class="sxs-lookup"><span data-stu-id="311f6-235">| [2] [3]</span></span> 

<span data-ttu-id="311f6-236">v</span><span class="sxs-lookup"><span data-stu-id="311f6-236">v</span></span> 

<span data-ttu-id="311f6-237">Y</span><span class="sxs-lookup"><span data-stu-id="311f6-237">Y</span></span> 


<span data-ttu-id="311f6-238">這些常式可以在計算著色器或圖元著色器中運作。</span><span class="sxs-lookup"><span data-stu-id="311f6-238">These routines work in either compute shaders or pixel shaders.</span></span> <span data-ttu-id="311f6-239">在計算著色器中，它們在四邊形中的運作方式是在 SIMD wave 內定義為平均分配4群組。</span><span class="sxs-lookup"><span data-stu-id="311f6-239">In compute shaders they operate in quads defined as evenly divided groups of 4 within an SIMD wave.</span></span> <span data-ttu-id="311f6-240">在圖元著色器中，它們應該用於 WaveQuadLanes 所捕獲的波浪，否則結果會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="311f6-240">In pixel shaders they should be used on waves captured by WaveQuadLanes, otherwise results are undefined.</span></span>

| | | | |
|-|-|-|-|
| <span data-ttu-id="311f6-241">**內建**</span><span class="sxs-lookup"><span data-stu-id="311f6-241">**Intrinsic**</span></span> | <span data-ttu-id="311f6-242">**說明**</span><span class="sxs-lookup"><span data-stu-id="311f6-242">**Description**</span></span> | <span data-ttu-id="311f6-243">**像素著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-243">**Pixel shader**</span></span> | <span data-ttu-id="311f6-244">**計算著色器**</span><span class="sxs-lookup"><span data-stu-id="311f6-244">**Compute shader**</span></span> |
| [<span data-ttu-id="311f6-245">**QuadReadLaneAt**</span><span class="sxs-lookup"><span data-stu-id="311f6-245">**QuadReadLaneAt**</span></span>](quadreadlaneat.md) | <span data-ttu-id="311f6-246">從 quadLaneID 0 所識別的目前四顆線的通道中，傳回指定的來源值， \[ \] 其必須在四個之間保持一致。</span><span class="sxs-lookup"><span data-stu-id="311f6-246">Returns the specified source value read from the lane of the current quad identified by quadLaneID \[0..3\] which must be uniform across the quad.</span></span> | \* | |
| [<span data-ttu-id="311f6-247">**QuadReadAcrossDiagonal**</span><span class="sxs-lookup"><span data-stu-id="311f6-247">**QuadReadAcrossDiagonal**</span></span>](quadreadacrossdiagonal.md) | <span data-ttu-id="311f6-248">傳回指定的區域值，此值是從這個四個對角線中的相反通道讀取的。</span><span class="sxs-lookup"><span data-stu-id="311f6-248">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span> | \* | |
| [<span data-ttu-id="311f6-249">**QuadReadAcrossX**</span><span class="sxs-lookup"><span data-stu-id="311f6-249">**QuadReadAcrossX**</span></span>](quadswapx.md) | <span data-ttu-id="311f6-250">傳回指定的來源值，此值是從這個四的 X 方向中的另一個通道讀取的。</span><span class="sxs-lookup"><span data-stu-id="311f6-250">Returns the specified source value read from the other lane in this quad in the X direction.</span></span> | \* | |
| [<span data-ttu-id="311f6-251">**QuadReadAcrossY**</span><span class="sxs-lookup"><span data-stu-id="311f6-251">**QuadReadAcrossY**</span></span>](quadswapy.md) | <span data-ttu-id="311f6-252">傳回從這個四個 Y 方向的其他通道讀取的指定來源值。</span><span class="sxs-lookup"><span data-stu-id="311f6-252">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span> | \* | |

## <a name="hardware-capability"></a><span data-ttu-id="311f6-253">硬體功能</span><span class="sxs-lookup"><span data-stu-id="311f6-253">Hardware capability</span></span>

<span data-ttu-id="311f6-254">若要檢查是否有任何特定硬體可使用 wave 作業功能，請呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)，並記下 [**D3D12 \_ 功能 \_ 資料 \_ D3D12 \_ OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) 結構的描述與使用。</span><span class="sxs-lookup"><span data-stu-id="311f6-254">In order to check that the wave operation features are available on any specific hardware, call [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport), noting the description and use of the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="311f6-255">相關主題</span><span class="sxs-lookup"><span data-stu-id="311f6-255">Related topics</span></span>

* [<span data-ttu-id="311f6-256">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="311f6-256">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="311f6-257">著色器模型6內建函式</span><span class="sxs-lookup"><span data-stu-id="311f6-257">Shader Model 6 intrinsics</span></span>](shader-model-6-0.md)