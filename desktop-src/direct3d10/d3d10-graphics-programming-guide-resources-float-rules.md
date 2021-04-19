---
description: Direct3D 10 支援數個不同的浮點數標記法。 所有浮點數運算都是在定義的 IEEE 754 32 位單一精確度浮點數行為的子集下運作。
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: " (Direct3D 10) 的 FFloating 點規則"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966634"
---
# <a name="floating-point-rules-direct3d-10"></a><span data-ttu-id="3f89d-104"> (Direct3D 10) 的浮點規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-104">Floating-point rules (Direct3D 10)</span></span>

<span data-ttu-id="3f89d-105">Direct3D 10 支援數個不同的浮點數標記法。</span><span class="sxs-lookup"><span data-stu-id="3f89d-105">Direct3D 10 supports several different floating-point representations.</span></span> <span data-ttu-id="3f89d-106">所有浮點數運算都是在定義的 IEEE 754 32 位單一精確度浮點數行為的子集下運作。</span><span class="sxs-lookup"><span data-stu-id="3f89d-106">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point behavior.</span></span>

-   [<span data-ttu-id="3f89d-107">32位 Floating-Point 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-107">32-bit Floating-Point Rules</span></span>](#32-bit-floating-point-rules)
    -   [<span data-ttu-id="3f89d-108">接受 IEEE-754 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-108">Honored IEEE-754 Rules</span></span>](#honored-ieee-754-rules)
    -   [<span data-ttu-id="3f89d-109">IEEE-754 規則的偏差或其他需求</span><span class="sxs-lookup"><span data-stu-id="3f89d-109">Deviations or Additional Requirements from IEEE-754 Rules</span></span>](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [<span data-ttu-id="3f89d-110">16位 Floating-Point 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-110">16-bit Floating-Point Rules</span></span>](#16-bit-floating-point-rules)
-   [<span data-ttu-id="3f89d-111">11位和10位 Floating-Point 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-111">11-bit and 10-bit Floating-Point Rules</span></span>](#11-bit-and-10-bit-floating-point-rules)
-   [<span data-ttu-id="3f89d-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f89d-112">Related topics</span></span>](#related-topics)

## <a name="32-bit-floating-point-rules"></a><span data-ttu-id="3f89d-113">32位 Floating-Point 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-113">32-bit Floating-Point Rules</span></span>

<span data-ttu-id="3f89d-114">有兩組規則：符合 IEEE-754 的規則，以及偏離標準的規則。</span><span class="sxs-lookup"><span data-stu-id="3f89d-114">There are two sets of rules: those that conform to IEEE-754, and those that deviate from the standard.</span></span>

### <a name="honored-ieee-754-rules"></a><span data-ttu-id="3f89d-115">接受 IEEE-754 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-115">Honored IEEE-754 Rules</span></span>

<span data-ttu-id="3f89d-116">有些規則是單一選項，由 IEEE-754 提供選擇。</span><span class="sxs-lookup"><span data-stu-id="3f89d-116">Some of these rules are a single option where IEEE-754 offers choices.</span></span>

-   <span data-ttu-id="3f89d-117">除以 0 會產生 +/- INF，除了 0/0 得到 NaN 的結果。</span><span class="sxs-lookup"><span data-stu-id="3f89d-117">Divide by 0 produces +/- INF, except 0/0 which results in NaN.</span></span>
-   <span data-ttu-id="3f89d-118">(+/-) 0 的對數會產生 -INF。</span><span class="sxs-lookup"><span data-stu-id="3f89d-118">log of (+/-) 0 produces -INF.</span></span> <span data-ttu-id="3f89d-119">負值 (-0 除外) 的對數會產生 NaN。</span><span class="sxs-lookup"><span data-stu-id="3f89d-119">log of a negative value (other than -0) produces NaN.</span></span>
-   <span data-ttu-id="3f89d-120">負數的反平方根 (rsq) 或平方根 (sqrt) 會產生 NaN。</span><span class="sxs-lookup"><span data-stu-id="3f89d-120">Reciprocal square root (rsq) or square root (sqrt) of a negative number produces NaN.</span></span> <span data-ttu-id="3f89d-121">例外是 -0；sqrt(-0) 會產生 -0，而 rsq(-0) 會產生 -INF。</span><span class="sxs-lookup"><span data-stu-id="3f89d-121">The exception is -0; sqrt(-0) produces -0, and rsq(-0) produces -INF.</span></span>
-   <span data-ttu-id="3f89d-122">INF - INF = NaN</span><span class="sxs-lookup"><span data-stu-id="3f89d-122">INF - INF = NaN</span></span>
-   <span data-ttu-id="3f89d-123">(+/-)INF / (+/-)INF = NaN</span><span class="sxs-lookup"><span data-stu-id="3f89d-123">(+/-)INF / (+/-)INF = NaN</span></span>
-   <span data-ttu-id="3f89d-124"> (+/-) INF \* 0 = NaN</span><span class="sxs-lookup"><span data-stu-id="3f89d-124">(+/-)INF \* 0 = NaN</span></span>
-   <span data-ttu-id="3f89d-125">NaN (任意 OP) 任意值 = NaN</span><span class="sxs-lookup"><span data-stu-id="3f89d-125">NaN (any OP) any-value = NaN</span></span>
-   <span data-ttu-id="3f89d-126">比較 EQ、GT、GE、LT 和 LE，若任一個或兩個運算元皆為 NaN，則傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3f89d-126">The comparisons EQ, GT, GE, LT, and LE, when either or both operands is NaN returns **FALSE**.</span></span>
-   <span data-ttu-id="3f89d-127">比較會忽略 0 的正負號 (因此 +0 等於 -0)。</span><span class="sxs-lookup"><span data-stu-id="3f89d-127">Comparisons ignore the sign of 0 (so +0 equals -0).</span></span>
-   <span data-ttu-id="3f89d-128">比較 NE，若任一個或兩個運算元皆為 NaN，則傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3f89d-128">The comparison NE, when either or both operands is NaN returns **TRUE**.</span></span>
-   <span data-ttu-id="3f89d-129">任何非 NaN 值與 +/- INF 比較會傳回正確的結果。</span><span class="sxs-lookup"><span data-stu-id="3f89d-129">Comparisons of any non-NaN value against +/- INF return the correct result.</span></span>

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a><span data-ttu-id="3f89d-130">IEEE-754 規則的偏差或其他需求</span><span class="sxs-lookup"><span data-stu-id="3f89d-130">Deviations or Additional Requirements from IEEE-754 Rules</span></span>

-   <span data-ttu-id="3f89d-131">IEEE-754 需要浮點運算產生結果，此結果為最接近無限精確結果的可表示值，也稱為 round-to-nearest-even。</span><span class="sxs-lookup"><span data-stu-id="3f89d-131">IEEE-754 requires floating-point operations to produce a result that is the nearest representable value to an infinitely-precise result, known as round-to-nearest-even.</span></span> <span data-ttu-id="3f89d-132">但是，Direct3D 10 定義了較鬆散需求：32位的浮點運算會產生一個單位-最後一個單元中的結果， (1 ULP) 的無限精確度結果。</span><span class="sxs-lookup"><span data-stu-id="3f89d-132">Direct3D 10, however, defines a looser requirement: 32-bit floating-point operations produce a result that is within one unit-last-place (1 ULP) of the infinitely-precise result.</span></span> <span data-ttu-id="3f89d-133">這表示，例如硬體允許截斷結果至 32 位元，而不是執行 round-to-nearest-even，因為這樣會讓最多一個 ULP 產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3f89d-133">This means that, for example, hardware is allowed to truncate results to 32-bit rather than perform round-to-nearest-even, as that would result in error of at most one ULP.</span></span>
-   <span data-ttu-id="3f89d-134">不支援浮點例外、狀態位元或設陷。</span><span class="sxs-lookup"><span data-stu-id="3f89d-134">There is no support for floating-point exceptions, status bits or traps.</span></span>
-   <span data-ttu-id="3f89d-135">Denorm 會在任何浮點數學運算的輸入和輸出上，排清至保留正負號的零。</span><span class="sxs-lookup"><span data-stu-id="3f89d-135">Denorms are flushed to sign-preserved zero on input and output of any floating-point mathematical operation.</span></span> <span data-ttu-id="3f89d-136">不會運算元據的任何 i/o 或資料移動作業都會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="3f89d-136">Exceptions are made for any I/O or data movement operation that does not manipulate the data.</span></span>
-   <span data-ttu-id="3f89d-137">包含浮點值的狀態（例如，MinDepth/MaxDepth、邊框型值等）可提供為 denorm 值，而且可能會在硬體使用之前或可能不會被清除。</span><span class="sxs-lookup"><span data-stu-id="3f89d-137">States that contain floating-point values, such as Viewport MinDepth/MaxDepth, BorderColor values etc., may be provided as denorm values and may or may not be flushed before use by the hardware.</span></span>
-   <span data-ttu-id="3f89d-138">最小值或最大值作業會針對比較排清 denorm，但結果不一定會是排清 denorm。</span><span class="sxs-lookup"><span data-stu-id="3f89d-138">Min or max operations flush denorms for comparison, but the result may or may not be denorm flushed.</span></span>
-   <span data-ttu-id="3f89d-139">對作業的 NaN 輸入一律會在輸出上產生 NaN，不過，不需要 NaN 的確切位模式來維持相同的 (除非作業是原始的移動指令，而這完全不會改變數據。 ) </span><span class="sxs-lookup"><span data-stu-id="3f89d-139">NaN input to an operation always produces NaN on output, however the exact bit pattern of the NaN is not required to stay the same (unless the operation is a raw move instruction - which does not alter data at all.)</span></span>
-   <span data-ttu-id="3f89d-140">只有一個運算元為 NaN 的最小或最大作業會傳回另一個運算元作為結果， (與上述) 的比較規則相反。</span><span class="sxs-lookup"><span data-stu-id="3f89d-140">Min or max operations for which only one operand is NaN return the other operand as the result (contrary to comparison rules above).</span></span> <span data-ttu-id="3f89d-141">這是在 Direct3D 10 中所需 (IEEE 754R) 的新 IEEE 規則。</span><span class="sxs-lookup"><span data-stu-id="3f89d-141">This is a new IEEE rule (IEEE 754R), required in Direct3D 10.</span></span>
-   <span data-ttu-id="3f89d-142">另一個新的 IEEE 754R 規則是 min (-0、+ 0) = = min (+ 0、-0) = =-0 和 max (-0、+ 0) = = max (+ 0、-0) = = + 0 （相較于上述 (所述的帶正負號零) 的比較規則）。</span><span class="sxs-lookup"><span data-stu-id="3f89d-142">Another new IEEE 754R rule is that min(-0,+0) == min(+0,-0) == -0, and max(-0,+0) == max(+0,-0) == +0, which honor the sign, in contrast to the comparison rules for signed zero (stated above).</span></span> <span data-ttu-id="3f89d-143">Direct3D 10 在此建議 IEEE 754R 行為，但不會強制執行;您可以使用忽略符號的比較，讓比較零的結果相依于參數的順序。</span><span class="sxs-lookup"><span data-stu-id="3f89d-143">Direct3D 10 recommends the IEEE 754R behavior here, but it will not be enforced; it is permissible for the result of comparing zeros to be dependent on the order of parameters, using a comparison that ignores the signs.</span></span>
-   <span data-ttu-id="3f89d-144">\*除了 denorm 排清) 之外，x 1.0 f 一律會產生 x (。</span><span class="sxs-lookup"><span data-stu-id="3f89d-144">x\*1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="3f89d-145">x/1.0f 一律產生 x (除了會排清 denorm)。</span><span class="sxs-lookup"><span data-stu-id="3f89d-145">x/1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="3f89d-146">x +/- 0.0f 一律產生 x (除了會排清 denorm)。</span><span class="sxs-lookup"><span data-stu-id="3f89d-146">x +/- 0.0f always results in x (except denorm flushed).</span></span> <span data-ttu-id="3f89d-147">但是 -0 + 0 = +0。</span><span class="sxs-lookup"><span data-stu-id="3f89d-147">But -0 + 0 = +0.</span></span>
-   <span data-ttu-id="3f89d-148">合併運算 (例如 mad、dp3) 產生的結果肯定比非合併擴展運算可能最差的序列評估順序精確。</span><span class="sxs-lookup"><span data-stu-id="3f89d-148">Fused operations (such as mad, dp3) produce results that are no less accurate than the worst possible serial ordering of evaluation of the unfused expansion of the operation.</span></span> <span data-ttu-id="3f89d-149">請注意，最差可能順序的定義（基於容錯目的）不是指定之融合作業的固定定義;這取決於輸入的特定值。</span><span class="sxs-lookup"><span data-stu-id="3f89d-149">Note that the definition of the worst possible ordering, for the purpose of tolerance, is not a fixed definition for a given fused operation; it depends on the particular values of the inputs.</span></span> <span data-ttu-id="3f89d-150">Unfused 擴充中的個別步驟分別允許1個 ULP 容忍 (或針對任何 Direct3D 10 呼叫的指示，其中具有比 1 ULP 更寬鬆的容錯能力，) 允許較寬鬆的容錯。</span><span class="sxs-lookup"><span data-stu-id="3f89d-150">The individual steps in the unfused expansion are each allowed 1 ULP tolerance (or for any instructions Direct3D 10 calls out with a more lax tolerance than 1 ULP, the more lax tolerance is allowed).</span></span>
-   <span data-ttu-id="3f89d-151">合併運算遵循與非合併運算相同的 NaN 規則。</span><span class="sxs-lookup"><span data-stu-id="3f89d-151">Fused operations adhere to the same NaN rules as non-fused operations.</span></span>
-   <span data-ttu-id="3f89d-152">將每個在32位浮點精確度層級的作業相乘和相除 (精確度為 1 ULP) 。</span><span class="sxs-lookup"><span data-stu-id="3f89d-152">Multiply and divide each operate at the 32-bit floating-point precision level (accuracy to 1 ULP).</span></span>

## <a name="16-bit-floating-point-rules"></a><span data-ttu-id="3f89d-153">16位 Floating-Point 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-153">16-bit Floating-Point Rules</span></span>

<span data-ttu-id="3f89d-154">Direct3D 10 也支援以16位表示的浮點數。</span><span class="sxs-lookup"><span data-stu-id="3f89d-154">Direct3D 10 also supports 16-bit representations of floating-point numbers.</span></span>

<span data-ttu-id="3f89d-155">格式：</span><span class="sxs-lookup"><span data-stu-id="3f89d-155">Format:</span></span>

-   <span data-ttu-id="3f89d-156">在 MSB 位元位置 1 帶正負號位元 (s)</span><span class="sxs-lookup"><span data-stu-id="3f89d-156">1 sign bit (s)in the MSB bit position</span></span>
-   <span data-ttu-id="3f89d-157">5 位元偏置指数 (e)</span><span class="sxs-lookup"><span data-stu-id="3f89d-157">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="3f89d-158">10 位元分數 (f)，含一個額外的隱藏位元</span><span class="sxs-lookup"><span data-stu-id="3f89d-158">10 bits of fraction (f), with an additional hidden bit</span></span>

<span data-ttu-id="3f89d-159"> (v) 的 float16 值會遵循下列規則：</span><span class="sxs-lookup"><span data-stu-id="3f89d-159">A float16 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="3f89d-160">若 e == 31 且 f != 0，則 v 為 NaN，不考慮 s</span><span class="sxs-lookup"><span data-stu-id="3f89d-160">if e == 31 and f != 0, then v is NaN regardless of s</span></span>
-   <span data-ttu-id="3f89d-161">如果 e = = 31 且 f = = 0，則 v = (-1) \* 無限大 (帶正負號的無限大) </span><span class="sxs-lookup"><span data-stu-id="3f89d-161">if e == 31 and f == 0, then v = (-1)s\*infinity (signed infinity)</span></span>
-   <span data-ttu-id="3f89d-162">如果 e 介於0和31之間，則 v = (-1) s \* 2 (e-15) \* (1. f) </span><span class="sxs-lookup"><span data-stu-id="3f89d-162">if e is between 0 and 31, then v = (-1)s\*2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="3f89d-163">如果 e = = 0 和 f！ = 0，則 v = (-1) s \* 2 (e-14) \* (0 f)  (反正規化數位) </span><span class="sxs-lookup"><span data-stu-id="3f89d-163">if e == 0 and f != 0, then v = (-1)s\*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="3f89d-164">如果 e = = 0 且 f = = 0，則 v = (-1) s \* 0 (帶正負號的零) </span><span class="sxs-lookup"><span data-stu-id="3f89d-164">if e == 0 and f == 0, then v = (-1)s\*0 (signed zero)</span></span>

<span data-ttu-id="3f89d-165">32位浮點規則也會保存16位浮點數，並針對上面所述的位配置進行調整。</span><span class="sxs-lookup"><span data-stu-id="3f89d-165">32-bit floating-point rules also hold for 16-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="3f89d-166">例外狀況包括：</span><span class="sxs-lookup"><span data-stu-id="3f89d-166">Exceptions to this include:</span></span>

-   <span data-ttu-id="3f89d-167">精確度︰16 位元浮點數的未合併運算產生的結果為最接近無限精確結果的可表示值 (進位置最接近偶數，依照 IEEE-754，適用於 16 位元值)。</span><span class="sxs-lookup"><span data-stu-id="3f89d-167">Precision: Unfused operations on 16-bit floating-point numbers produce a result that is the nearest representable value to an infinitely-precise result (round to nearest even, per IEEE-754, applied to 16-bit values).</span></span> <span data-ttu-id="3f89d-168">32 位元浮點規則遵循 1 ULP 誤差，16 位元浮點規則針對非合併運算遵循 0.5 ULP，合併運算則為 0.6 ULP。</span><span class="sxs-lookup"><span data-stu-id="3f89d-168">32-bit floating-point rules adhere to 1 ULP tolerance, 16-bit floating-point rules adhere to 0.5 ULP for unfused operations, and 0.6 ULP for fused operations.</span></span>
-   <span data-ttu-id="3f89d-169">16 位元浮點數保留 denorm。</span><span class="sxs-lookup"><span data-stu-id="3f89d-169">16-bit floating-point numbers preserve denorms.</span></span>

## <a name="11-bit-and-10-bit-floating-point-rules"></a><span data-ttu-id="3f89d-170">11位和10位 Floating-Point 規則</span><span class="sxs-lookup"><span data-stu-id="3f89d-170">11-bit and 10-bit Floating-Point Rules</span></span>

<span data-ttu-id="3f89d-171">Direct3D 10 也支援11位和10位浮點數格式。</span><span class="sxs-lookup"><span data-stu-id="3f89d-171">Direct3D 10 also supports 11-bit and 10-bit floating-point formats.</span></span>

<span data-ttu-id="3f89d-172">格式：</span><span class="sxs-lookup"><span data-stu-id="3f89d-172">Format:</span></span>

-   <span data-ttu-id="3f89d-173">不帶正負號的位元</span><span class="sxs-lookup"><span data-stu-id="3f89d-173">No sign bit</span></span>
-   <span data-ttu-id="3f89d-174">5 位元偏置指数 (e)</span><span class="sxs-lookup"><span data-stu-id="3f89d-174">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="3f89d-175">11 位元格式為 6 位元分數 (f)，10 位元格式為 5 位元分數 (f)，兩者皆有一個額外的隱藏位元。</span><span class="sxs-lookup"><span data-stu-id="3f89d-175">6 bits of fraction (f) for an 11-bit format, 5 bits of fraction (f) for a 10-bit format, with an additional hidden bit in either case.</span></span>

<span data-ttu-id="3f89d-176">float11/float10 值 (v) 遵循下列規則：</span><span class="sxs-lookup"><span data-stu-id="3f89d-176">A float11/float10 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="3f89d-177">若 e == 31 且 f != 0，則 v 為 NaN</span><span class="sxs-lookup"><span data-stu-id="3f89d-177">if e == 31 and f != 0, then v is NaN</span></span>
-   <span data-ttu-id="3f89d-178">若 e == 31 且 f == 0，則 v = +infinity</span><span class="sxs-lookup"><span data-stu-id="3f89d-178">if e == 31 and f == 0, then v = +infinity</span></span>
-   <span data-ttu-id="3f89d-179">如果 e 介於0和31之間，則 v = 2 (e-15) \* (1. f) </span><span class="sxs-lookup"><span data-stu-id="3f89d-179">if e is between 0 and 31, then v = 2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="3f89d-180">如果 e = = 0 和 f！ = 0，則 v = \* 2 (e-14) \* (0. f)  (反正規化數位) </span><span class="sxs-lookup"><span data-stu-id="3f89d-180">if e == 0 and f != 0, then v = \*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="3f89d-181">若 e == 0 且 f == 0，則 v = 0 (零)</span><span class="sxs-lookup"><span data-stu-id="3f89d-181">if e == 0 and f == 0, then v = 0 (zero)</span></span>

<span data-ttu-id="3f89d-182">32位浮點規則也會保留11位和10位浮點數，並針對上面所述的位配置進行調整。</span><span class="sxs-lookup"><span data-stu-id="3f89d-182">32-bit floating-point rules also hold for 11-bit and 10-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="3f89d-183">例外狀況包括：</span><span class="sxs-lookup"><span data-stu-id="3f89d-183">Exceptions include:</span></span>

-   <span data-ttu-id="3f89d-184">精確度︰32 位元浮點規則遵循 0.5 ULP。</span><span class="sxs-lookup"><span data-stu-id="3f89d-184">Precision: 32-bit floating-point rules adhere to 0.5 ULP.</span></span>
-   <span data-ttu-id="3f89d-185">10/11 位元浮點數保留 denorm。</span><span class="sxs-lookup"><span data-stu-id="3f89d-185">10/11-bit floating-point numbers preserve denorms.</span></span>
-   <span data-ttu-id="3f89d-186">任何會產生小於零之數位的作業都會壓制為零。</span><span class="sxs-lookup"><span data-stu-id="3f89d-186">Any operation that would result in a number less than zero, is clamped to zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f89d-187">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f89d-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f89d-188"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="3f89d-188">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



