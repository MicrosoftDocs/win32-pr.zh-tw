---
title: " (Direct3D 11) 的浮點規則"
description: Direct3D 11 支援數個浮點數標記法。 所有浮點數計算運作都在 IEEE 754 32 位元單精確度浮點數規則的定義子集下運作。
ms.assetid: 33F21BD0-FDF8-4D35-95C0-0A3920814CB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83c87db0daa69c0393d0399ece5bdb6cf01d519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375541"
---
# <a name="floating-point-rules-direct3d-11"></a><span data-ttu-id="e5dcd-104"> (Direct3D 11) 的浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-104">Floating-point rules (Direct3D 11)</span></span>

<span data-ttu-id="e5dcd-105">Direct3D 11 支援數個浮點數標記法。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-105">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="e5dcd-106">所有浮點數計算運作都在 IEEE 754 32 位元單精確度浮點數規則的定義子集下運作。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-106">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span>

-   [<span data-ttu-id="e5dcd-107">32位浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-107">32-bit floating-point rules</span></span>](#32-bit-floating-point-rules)
    -   [<span data-ttu-id="e5dcd-108">接受 IEEE-754 規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-108">Honored IEEE-754 rules</span></span>](#honored-ieee-754-rules)
    -   [<span data-ttu-id="e5dcd-109">IEEE-754 規則的偏差或其他需求</span><span class="sxs-lookup"><span data-stu-id="e5dcd-109">Deviations or additional requirements from IEEE-754 rules</span></span>](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [<span data-ttu-id="e5dcd-110">64位 (雙精確度) 浮點數規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-110">64-bit (double precision) floating point rules</span></span>](#64-bit-double-precision-floating-point-rules)
-   [<span data-ttu-id="e5dcd-111">16位浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-111">16-bit floating-point rules</span></span>](#16-bit-floating-point-rules)
-   [<span data-ttu-id="e5dcd-112">11位和10位浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-112">11-bit and 10-bit floating-point rules</span></span>](#11-bit-and-10-bit-floating-point-rules)
-   [<span data-ttu-id="e5dcd-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5dcd-113">Related topics</span></span>](#related-topics)

## <a name="32-bit-floating-point-rules"></a><span data-ttu-id="e5dcd-114">32 位元浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-114">32-bit floating-point rules</span></span>

<span data-ttu-id="e5dcd-115">有兩組規則：符合 IEEE-754 的規則，以及偏離標準的規則。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-115">There are two sets of rules: those that conform to IEEE-754, and those that deviate from the standard.</span></span>

### <a name="honored-ieee-754-rules"></a><span data-ttu-id="e5dcd-116">遵循 IEEE-754 規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-116">Honored IEEE-754 rules</span></span>

<span data-ttu-id="e5dcd-117">有些規則是單一選項，由 IEEE-754 提供選擇。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-117">Some of these rules are a single option where IEEE-754 offers choices.</span></span>

-   <span data-ttu-id="e5dcd-118">除以 0 會產生 +/- INF，除了 0/0 得到 NaN 的結果。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-118">Divide by 0 produces +/- INF, except 0/0 which results in NaN.</span></span>
-   <span data-ttu-id="e5dcd-119">(+/-) 0 的對數會產生 -INF。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-119">log of (+/-) 0 produces -INF.</span></span> <span data-ttu-id="e5dcd-120">負值 (-0 除外) 的對數會產生 NaN。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-120">log of a negative value (other than -0) produces NaN.</span></span>
-   <span data-ttu-id="e5dcd-121">負數的反平方根 (rsq) 或平方根 (sqrt) 會產生 NaN。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-121">Reciprocal square root (rsq) or square root (sqrt) of a negative number produces NaN.</span></span> <span data-ttu-id="e5dcd-122">例外是 -0；sqrt(-0) 會產生 -0，而 rsq(-0) 會產生 -INF。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-122">The exception is -0; sqrt(-0) produces -0, and rsq(-0) produces -INF.</span></span>
-   <span data-ttu-id="e5dcd-123">INF - INF = NaN</span><span class="sxs-lookup"><span data-stu-id="e5dcd-123">INF - INF = NaN</span></span>
-   <span data-ttu-id="e5dcd-124">(+/-)INF / (+/-)INF = NaN</span><span class="sxs-lookup"><span data-stu-id="e5dcd-124">(+/-)INF / (+/-)INF = NaN</span></span>
-   <span data-ttu-id="e5dcd-125"> (+/-) INF \* 0 = NaN</span><span class="sxs-lookup"><span data-stu-id="e5dcd-125">(+/-)INF \* 0 = NaN</span></span>
-   <span data-ttu-id="e5dcd-126">NaN (任意 OP) 任意值 = NaN</span><span class="sxs-lookup"><span data-stu-id="e5dcd-126">NaN (any OP) any-value = NaN</span></span>
-   <span data-ttu-id="e5dcd-127">比較 EQ、GT、GE、LT 和 LE，若任一個或兩個運算元皆為 NaN，則傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-127">The comparisons EQ, GT, GE, LT, and LE, when either or both operands is NaN returns **FALSE**.</span></span>
-   <span data-ttu-id="e5dcd-128">比較會忽略 0 的正負號 (因此 +0 等於 -0)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-128">Comparisons ignore the sign of 0 (so +0 equals -0).</span></span>
-   <span data-ttu-id="e5dcd-129">比較 NE，若任一個或兩個運算元皆為 NaN，則傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-129">The comparison NE, when either or both operands is NaN returns **TRUE**.</span></span>
-   <span data-ttu-id="e5dcd-130">任何非 NaN 值與 +/- INF 比較會傳回正確的結果。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-130">Comparisons of any non-NaN value against +/- INF return the correct result.</span></span>

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a><span data-ttu-id="e5dcd-131">IEEE-754 規則的差異或其他需求</span><span class="sxs-lookup"><span data-stu-id="e5dcd-131">Deviations or additional requirements from IEEE-754 rules</span></span>

-   <span data-ttu-id="e5dcd-132">IEEE-754 需要浮點運算產生結果，此結果為最接近無限精確結果的可表示值，也稱為 round-to-nearest-even。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-132">IEEE-754 requires floating-point operations to produce a result that is the nearest representable value to an infinitely-precise result, known as round-to-nearest-even.</span></span> <span data-ttu-id="e5dcd-133">Direct3D 11 定義相同的需求：32位浮點運算產生的結果是在0.5 單位-最後 (ULP) 的最精確結果。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-133">Direct3D 11 defines the same requirement: 32-bit floating-point operations produce a result that is within 0.5 unit-last-place (ULP) of the infinitely-precise result.</span></span> <span data-ttu-id="e5dcd-134">這表示，例如，硬體允許將結果截斷為32位，而不是執行四捨五入到最接近的結果，因為這會導致最多 0.5 ULP 的錯誤。此規則只適用于加法、減法和乘法。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-134">This means that, for example, hardware is allowed to truncate results to 32-bit rather than perform round-to-nearest-even, as that would result in error of at most 0.5 ULP.This rule applies only to addition, subtraction, and multiplication.</span></span>
-   <span data-ttu-id="e5dcd-135">不支援浮點例外、狀態位元或設陷。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-135">There is no support for floating-point exceptions, status bits or traps.</span></span>
-   <span data-ttu-id="e5dcd-136">Denorm 會在任何浮點數學運算的輸入和輸出上，排清至保留正負號的零。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-136">Denorms are flushed to sign-preserved zero on input and output of any floating-point mathematical operation.</span></span> <span data-ttu-id="e5dcd-137">例外是針對不操作資料的任何 I/O 或資料移動作業。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-137">Exceptions are made for any I/O or data movement operation that doesn't manipulate the data.</span></span>
-   <span data-ttu-id="e5dcd-138">包含浮點值的狀態（例如，MinDepth/MaxDepth 等）可以提供為 denorm 值，而且不一定會在硬體使用這些值之前進行清除。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-138">States that contain floating-point values, such as Viewport MinDepth/MaxDepth, BorderColor values, may be provided as denorm values and may or may not be flushed before the hardware uses them.</span></span>
-   <span data-ttu-id="e5dcd-139">最小值或最大值作業會針對比較排清 denorm，但結果不一定會是排清 denorm。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-139">Min or max operations flush denorms for comparison, but the result may or may not be denorm flushed.</span></span>
-   <span data-ttu-id="e5dcd-140">運算的 NaN 輸入一律會在輸出產生 NaN。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-140">NaN input to an operation always produces NaN on output.</span></span> <span data-ttu-id="e5dcd-141">但 NaN 的精確位元模式不必保持不變 (除非運算操作是原始移動指示 - 不會修改資料)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-141">But the exact bit pattern of the NaN is not required to stay the same (unless the operation is a raw move instruction - which doesn't alter data.)</span></span>
-   <span data-ttu-id="e5dcd-142">只有一個運算元是 NaN 的最小值或最大值運算，會傳回其他運算元做為結果 (與我們前面所說的比較規則相反)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-142">Min or max operations for which only one operand is NaN return the other operand as the result (contrary to comparison rules we looked at earlier).</span></span> <span data-ttu-id="e5dcd-143">這是 IEEE 754R 規則。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-143">This is a IEEE 754R rule.</span></span>

    <span data-ttu-id="e5dcd-144">浮點最小值和最大值運算的 IEEE-754R 規格指出，如果其中一個最小值或最大值的輸入是 quiet QNaN 值，運算結果就是另一個參數。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-144">The IEEE-754R specification for floating point min and max operations states that if one of the inputs to min or max is a quiet QNaN value, the result of the operation is the other parameter.</span></span> <span data-ttu-id="e5dcd-145">例如：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-145">For example:</span></span>

    ```C++
    min(x,QNaN) == min(QNaN,x) == x (same for max)
    ```

    

    <span data-ttu-id="e5dcd-146">IEEE-754R 規格的修訂對最小值和最大值採用了不同的行為，當一個輸入為 "signaling" SNaN 值與 QNaN 值比較：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-146">A revision of the IEEE-754R specification adopted a different behavior for min and max when one input is a "signaling" SNaN value versus a QNaN value:</span></span>

    ```C++
    min(x,SNaN) == min(SNaN,x) == QNaN (same for max)
     
    ```

    

    <span data-ttu-id="e5dcd-147">一般而言，Direct3D 遵循算術標準︰IEEE-754 和 IEEE-754R。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-147">Generally, Direct3D follows the standards for arithmetic: IEEE-754 and IEEE-754R.</span></span> <span data-ttu-id="e5dcd-148">但在此案例中有誤差。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-148">But in this case, we have a deviation.</span></span>

    <span data-ttu-id="e5dcd-149">Direct3D 10 及更新版本中的算術規則不會在 quiet 和 signaling NaN 值 (QNaN 與 SNaN 比較) 之間做出區別。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-149">The arithmetic rules in Direct3D 10 and later don't make any distinctions between quiet and signaling NaN values (QNaN versus SNaN).</span></span> <span data-ttu-id="e5dcd-150">所有 NaN 值都以相同方式處理。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-150">All NaN values are handled the same way.</span></span> <span data-ttu-id="e5dcd-151">若是最小值和最大值，任何 NaN 的 Direct3D 行為就像是 QNaN 在 IEEE-754R 定義中的處理方式。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-151">In the case of min and max, the Direct3D behavior for any NaN value is like how QNaN is handled in the IEEE-754R definition.</span></span> <span data-ttu-id="e5dcd-152">(為了完整性，如果兩個輸入都是 NaN，則會傳回任一個 NaN 值)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-152">(For completeness - if both inputs are NaN, any NaN value is returned.)</span></span>

-   <span data-ttu-id="e5dcd-153">另一項 IEEE 754R 規則是 min(-0,+0) == min(+0,-0) == -0 和 max(-0,+0) == max(+0,-0) == +0，其採用正負號，與帶正負號的零的比較規則相反 (如前面所見)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-153">Another IEEE 754R rule is that min(-0,+0) == min(+0,-0) == -0, and max(-0,+0) == max(+0,-0) == +0, which honors the sign, in contrast to the comparison rules for signed zero (as we saw earlier).</span></span> <span data-ttu-id="e5dcd-154">Direct3D 在此建議 IEEE 754R 行為，但不會強制執行；它允許比較零的結果取決於參數順序，使用忽略正負號的比較。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-154">Direct3D recommends the IEEE 754R behavior here, but doesn't enforce it; it is permissible for the result of comparing zeros to be dependent on the order of parameters, using a comparison that ignores the signs.</span></span>
-   <span data-ttu-id="e5dcd-155">\*除了 denorm 排清) 之外，x 1.0 f 一律會產生 x (。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-155">x\*1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="e5dcd-156">x/1.0f 一律產生 x (除了會排清 denorm)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-156">x/1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="e5dcd-157">x +/- 0.0f 一律產生 x (除了會排清 denorm)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-157">x +/- 0.0f always results in x (except denorm flushed).</span></span> <span data-ttu-id="e5dcd-158">但是 -0 + 0 = +0。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-158">But -0 + 0 = +0.</span></span>
-   <span data-ttu-id="e5dcd-159">合併運算 (例如 mad、dp3) 產生的結果肯定比非合併擴展運算可能最差的序列評估順序精確。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-159">Fused operations (such as mad, dp3) produce results that are no less accurate than the worst possible serial ordering of evaluation of the unfused expansion of the operation.</span></span> <span data-ttu-id="e5dcd-160">可能最差順序的定義 (基於誤差目的) 對於特定合併運算來說並非固定的定義；它取決於特殊的輸入值。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-160">The definition of the worst possible ordering, for the purpose of tolerance, is not a fixed definition for a given fused operation; it depends on the particular values of the inputs.</span></span> <span data-ttu-id="e5dcd-161">對於非合併擴展的個別步驟，每一個允許 1 ULP 誤差 (或對於 Direct3D 呼叫的任何指令，若 lax 誤差多於 1 ULP，則允許越大 lax 誤差)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-161">The individual steps in the unfused expansion are each allowed 1 ULP tolerance (or for any instructions Direct3D calls out with a more lax tolerance than 1 ULP, the more lax tolerance is allowed).</span></span>
-   <span data-ttu-id="e5dcd-162">合併運算遵循與非合併運算相同的 NaN 規則。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-162">Fused operations adhere to the same NaN rules as non-fused operations.</span></span>
-   <span data-ttu-id="e5dcd-163">sqrt 和 rcp 有 1 ULP 誤差。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-163">sqrt and rcp have 1 ULP tolerance.</span></span> <span data-ttu-id="e5dcd-164">著色器倒數和倒數平方根指令 [**rcp**](/previous-versions/windows/desktop/legacy/hh447205(v=vs.85)) 和 [**rsq**](/windows/desktop/direct3dhlsl/rsq--sm4---asm-) 各有自己較寬鬆的精確需求。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-164">The shader reciprocal and reciprocal square-root instructions, [**rcp**](/previous-versions/windows/desktop/legacy/hh447205(v=vs.85)) and [**rsq**](/windows/desktop/direct3dhlsl/rsq--sm4---asm-), have their own separate relaxed precision requirement.</span></span>
-   <span data-ttu-id="e5dcd-165">乘和除各在 32 位元浮點精準度運算 (乘積的精準度為 0.5 ULP，倒數的精準度為 1.0 ULP)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-165">Multiply and divide each operate at the 32-bit floating-point precision level (accuracy to 0.5 ULP for multiply, 1.0 ULP for reciprocal).</span></span> <span data-ttu-id="e5dcd-166">如果直接實作 x/y，結果必須大於或等於比兩步驟方法的精準度。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-166">If x/y is implemented directly, results must be of greater or equal accuracy than a two-step method.</span></span>

## <a name="64-bit-double-precision-floating-point-rules"></a><span data-ttu-id="e5dcd-167">64 位元 (雙精確度)浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-167">64-bit (double precision) floating point rules</span></span>

<span data-ttu-id="e5dcd-168">硬體和顯示器驅動程式選擇性支援雙精確度浮點。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-168">Hardware and display drivers optionally support double-precision floating-point.</span></span> <span data-ttu-id="e5dcd-169">為了指出支援，當您使用 [**D3D11 \_ 功能 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)時，驅動程式會將 [**D3D11 \_ 功能 \_ 資料 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)的 **DoublePrecisionFloatShaderOps** 設定為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-169">To indicate support, when you call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_DOUBLES**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature), the driver sets **DoublePrecisionFloatShaderOps** of [**D3D11\_FEATURE\_DATA\_DOUBLES**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) to TRUE.</span></span> <span data-ttu-id="e5dcd-170">驅動程式和硬體必須支援所有雙精確度浮點指令。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-170">The driver and hardware must then support all double-precision floating-point instructions.</span></span>

<span data-ttu-id="e5dcd-171">雙精確度指令遵循 IEEE 754R 行為需求。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-171">Double-precision instructions follow IEEE 754R behavior requirements.</span></span>

<span data-ttu-id="e5dcd-172">產生去標準化值的支援為雙精確度資料所必要 (不允許 flush-to-zero 行為)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-172">Support for generation of denormalized values is required for double-precision data (no flush-to-zero behavior).</span></span> <span data-ttu-id="e5dcd-173">同樣地，指令不會將去標準化資料讀做帶正負號的零，它們會採用 denorm 值。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-173">Likewise, instructions don't read denormalized data as a signed zero, they honor the denorm value.</span></span>

## <a name="16-bit-floating-point-rules"></a><span data-ttu-id="e5dcd-174">16 位元浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-174">16-bit floating-point rules</span></span>

<span data-ttu-id="e5dcd-175">Direct3D 11 也支援以16位表示的浮點數。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-175">Direct3D 11 also supports 16-bit representations of floating-point numbers.</span></span>

<span data-ttu-id="e5dcd-176">格式：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-176">Format:</span></span>

-   <span data-ttu-id="e5dcd-177">在 MSB 位元位置 1 帶正負號位元 (s)</span><span class="sxs-lookup"><span data-stu-id="e5dcd-177">1 sign bit (s)in the MSB bit position</span></span>
-   <span data-ttu-id="e5dcd-178">5 位元偏置指数 (e)</span><span class="sxs-lookup"><span data-stu-id="e5dcd-178">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="e5dcd-179">10 位元分數 (f)，含一個額外的隱藏位元</span><span class="sxs-lookup"><span data-stu-id="e5dcd-179">10 bits of fraction (f), with an additional hidden bit</span></span>

<span data-ttu-id="e5dcd-180">float16 值 (v) 遵循下列規則：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-180">A float16 value (v) follows these rules:</span></span>

-   <span data-ttu-id="e5dcd-181">若 e == 31 且 f != 0，則 v 為 NaN，不考慮 s</span><span class="sxs-lookup"><span data-stu-id="e5dcd-181">if e == 31 and f != 0, then v is NaN regardless of s</span></span>
-   <span data-ttu-id="e5dcd-182">如果 e = = 31 且 f = = 0，則 v = (-1) \* 無限大 (帶正負號的無限大) </span><span class="sxs-lookup"><span data-stu-id="e5dcd-182">if e == 31 and f == 0, then v = (-1)s\*infinity (signed infinity)</span></span>
-   <span data-ttu-id="e5dcd-183">如果 e 介於0和31之間，則 v = (-1) s \* 2 (e-15) \* (1. f) </span><span class="sxs-lookup"><span data-stu-id="e5dcd-183">if e is between 0 and 31, then v = (-1)s\*2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="e5dcd-184">如果 e = = 0 和 f！ = 0，則 v = (-1) s \* 2 (e-14) \* (0 f)  (反正規化數位) </span><span class="sxs-lookup"><span data-stu-id="e5dcd-184">if e == 0 and f != 0, then v = (-1)s\*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="e5dcd-185">如果 e = = 0 且 f = = 0，則 v = (-1) s \* 0 (帶正負號的零) </span><span class="sxs-lookup"><span data-stu-id="e5dcd-185">if e == 0 and f == 0, then v = (-1)s\*0 (signed zero)</span></span>

<span data-ttu-id="e5dcd-186">32 位元浮點規則也會針對 16 位元浮點數保留，並針對前面所述的位元配置調整。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-186">32-bit floating-point rules also hold for 16-bit floating-point numbers, adjusted for the bit layout described earlier.</span></span> <span data-ttu-id="e5dcd-187">例外狀況包括：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-187">Exceptions to this include:</span></span>

-   <span data-ttu-id="e5dcd-188">精確度︰16 位元浮點數的未合併運算產生的結果為最接近無限精確結果的可表示值 (進位置最接近偶數，依照 IEEE-754，適用於 16 位元值)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-188">Precision: Unfused operations on 16-bit floating-point numbers produce a result that is the nearest representable value to an infinitely-precise result (round to nearest even, per IEEE-754, applied to 16-bit values).</span></span> <span data-ttu-id="e5dcd-189">32 位元浮點規則遵循 1 ULP 誤差，16 位元浮點規則針對非合併運算遵循 0.5 ULP，合併運算則為 0.6 ULP。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-189">32-bit floating-point rules adhere to 1 ULP tolerance, 16-bit floating-point rules adhere to 0.5 ULP for unfused operations, and 0.6 ULP for fused operations.</span></span>
-   <span data-ttu-id="e5dcd-190">16 位元浮點數保留 denorm。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-190">16-bit floating-point numbers preserve denorms.</span></span>

## <a name="11-bit-and-10-bit-floating-point-rules"></a><span data-ttu-id="e5dcd-191">11 位元與 10 位元浮點規則</span><span class="sxs-lookup"><span data-stu-id="e5dcd-191">11-bit and 10-bit floating-point rules</span></span>

<span data-ttu-id="e5dcd-192">Direct3D 11 也支援11位和10位浮點數格式。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-192">Direct3D 11 also supports 11-bit and 10-bit floating-point formats.</span></span>

<span data-ttu-id="e5dcd-193">格式：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-193">Format:</span></span>

-   <span data-ttu-id="e5dcd-194">不帶正負號的位元</span><span class="sxs-lookup"><span data-stu-id="e5dcd-194">No sign bit</span></span>
-   <span data-ttu-id="e5dcd-195">5 位元偏置指数 (e)</span><span class="sxs-lookup"><span data-stu-id="e5dcd-195">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="e5dcd-196">11 位元格式為 6 位元分數 (f)，10 位元格式為 5 位元分數 (f)，兩者皆有一個額外的隱藏位元。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-196">6 bits of fraction (f) for an 11-bit format, 5 bits of fraction (f) for a 10-bit format, with an additional hidden bit in either case.</span></span>

<span data-ttu-id="e5dcd-197">float11/float10 值 (v) 遵循下列規則：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-197">A float11/float10 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="e5dcd-198">若 e == 31 且 f != 0，則 v 為 NaN</span><span class="sxs-lookup"><span data-stu-id="e5dcd-198">if e == 31 and f != 0, then v is NaN</span></span>
-   <span data-ttu-id="e5dcd-199">若 e == 31 且 f == 0，則 v = +infinity</span><span class="sxs-lookup"><span data-stu-id="e5dcd-199">if e == 31 and f == 0, then v = +infinity</span></span>
-   <span data-ttu-id="e5dcd-200">如果 e 介於0和31之間，則 v = 2 (e-15) \* (1. f) </span><span class="sxs-lookup"><span data-stu-id="e5dcd-200">if e is between 0 and 31, then v = 2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="e5dcd-201">如果 e = = 0 和 f！ = 0，則 v = \* 2 (e-14) \* (0. f)  (反正規化數位) </span><span class="sxs-lookup"><span data-stu-id="e5dcd-201">if e == 0 and f != 0, then v = \*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="e5dcd-202">若 e == 0 且 f == 0，則 v = 0 (零)</span><span class="sxs-lookup"><span data-stu-id="e5dcd-202">if e == 0 and f == 0, then v = 0 (zero)</span></span>

<span data-ttu-id="e5dcd-203">32 位元浮點規則也會針對 11 位元和 10 位元浮點數保留，並針對前面所述的位元配置調整。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-203">32-bit floating-point rules also hold for 11-bit and 10-bit floating-point numbers, adjusted for the bit layout described earlier.</span></span> <span data-ttu-id="e5dcd-204">例外狀況包括：</span><span class="sxs-lookup"><span data-stu-id="e5dcd-204">Exceptions include:</span></span>

-   <span data-ttu-id="e5dcd-205">精確度︰32 位元浮點規則遵循 0.5 ULP。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-205">Precision: 32-bit floating-point rules adhere to 0.5 ULP.</span></span>
-   <span data-ttu-id="e5dcd-206">10/11 位元浮點數保留 denorm。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-206">10/11-bit floating-point numbers preserve denorms.</span></span>
-   <span data-ttu-id="e5dcd-207">任何結果為小於零的運算都會限制為零。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-207">Any operation that would result in a number less than zero is clamped to zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5dcd-208">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5dcd-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5dcd-209">資源</span><span class="sxs-lookup"><span data-stu-id="e5dcd-209">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> <dt>

[<span data-ttu-id="e5dcd-210">紋理</span><span class="sxs-lookup"><span data-stu-id="e5dcd-210">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 