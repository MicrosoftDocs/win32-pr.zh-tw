---
description: 下列章節說明 Direct3D 如何處理資料類型之間的轉換。
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: 資料轉換規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61abdc58811af9155c67d7b32bcd47e9d4b71ea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688811"
---
# <a name="data-conversion-rules"></a><span data-ttu-id="245d6-103">資料轉換規則</span><span class="sxs-lookup"><span data-stu-id="245d6-103">Data Conversion Rules</span></span>

<span data-ttu-id="245d6-104">下列章節說明 Direct3D 如何處理資料類型之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="245d6-104">The following sections describe how Direct3D handles conversions between data types.</span></span>

-   [<span data-ttu-id="245d6-105">資料類型術語</span><span class="sxs-lookup"><span data-stu-id="245d6-105">Data Type Terminology</span></span>](#data-type-terminology)
-   [<span data-ttu-id="245d6-106">浮點數轉換</span><span class="sxs-lookup"><span data-stu-id="245d6-106">Floating Point Conversion</span></span>](#floating-point-conversion)
    -   [<span data-ttu-id="245d6-107">從較高的範圍標記法 Conververting 至較低範圍的標記法</span><span class="sxs-lookup"><span data-stu-id="245d6-107">Conververting from a higher range representation to a lower range representation</span></span>](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [<span data-ttu-id="245d6-108">從較低範圍表示轉換為較高範圍的標記法</span><span class="sxs-lookup"><span data-stu-id="245d6-108">Converting from a lower range representation to a higher range representation</span></span>](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [<span data-ttu-id="245d6-109">整數轉換</span><span class="sxs-lookup"><span data-stu-id="245d6-109">Integer Conversion</span></span>](#integer-conversion)
-   [<span data-ttu-id="245d6-110">固定點整數轉換</span><span class="sxs-lookup"><span data-stu-id="245d6-110">Fixed Point Integer Conversion</span></span>](#fixed-point-integer-conversion)
-   [<span data-ttu-id="245d6-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="245d6-111">Related topics</span></span>](#related-topics)

## <a name="data-type-terminology"></a><span data-ttu-id="245d6-112">資料類型詞彙</span><span class="sxs-lookup"><span data-stu-id="245d6-112">Data Type Terminology</span></span>

<span data-ttu-id="245d6-113">下列詞彙組後續將用來描述各種不同的格式轉換。</span><span class="sxs-lookup"><span data-stu-id="245d6-113">The following set of terms are subsequently used to characterize various format conversions.</span></span>



| <span data-ttu-id="245d6-114">詞彙</span><span class="sxs-lookup"><span data-stu-id="245d6-114">Term</span></span>  | <span data-ttu-id="245d6-115">定義</span><span class="sxs-lookup"><span data-stu-id="245d6-115">Definition</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="245d6-116">SNORM</span><span class="sxs-lookup"><span data-stu-id="245d6-116">SNORM</span></span> | <span data-ttu-id="245d6-117">帶正負號的標準化整數，表示 n-位元 2 的補數，最大值是指 1.0f (例如 5-位元值 01111 對應至 1.0f)，最小值是指 -1.0f (例如 5-位元值 10000 對應至 -1.0f)。</span><span class="sxs-lookup"><span data-stu-id="245d6-117">Signed normalized integer, meaning that for an n-bit 2's complement number, the maximum value means 1.0f (e.g. the 5-bit value 01111 maps to 1.0f), and the minimum value means -1.0f (e.g. the 5-bit value 10000 maps to -1.0f).</span></span> <span data-ttu-id="245d6-118">此外，第二小的數字對應至 -1.0f (例如 5-位元值 10001 對應至 -1.0f)。</span><span class="sxs-lookup"><span data-stu-id="245d6-118">In addition, the second-minimum number maps to -1.0f (e.g. the 5-bit value 10001 maps to -1.0f).</span></span> <span data-ttu-id="245d6-119">因此，-1.0f 有兩種整數表示法。</span><span class="sxs-lookup"><span data-stu-id="245d6-119">There are thus two integer representations for -1.0f.</span></span> <span data-ttu-id="245d6-120">0.0f 只有一種表示法，1.0f 也只有一種表示法。</span><span class="sxs-lookup"><span data-stu-id="245d6-120">There is a single representation for 0.0f, and a single representation for 1.0f.</span></span> <span data-ttu-id="245d6-121">這會對範圍 (-1.0f...0.0f) 中間隔平均的浮點值產生一組整數表示法，另外，範圍 (0.0f...1.0f) 中數字的補數也會有一組表示法</span><span class="sxs-lookup"><span data-stu-id="245d6-121">This results in a set of integer representations for evenly spaced floating point values in the range (-1.0f...0.0f), and also a complementary set of representations for numbers in the range (0.0f...1.0f)</span></span> |
| <span data-ttu-id="245d6-122">UNORM</span><span class="sxs-lookup"><span data-stu-id="245d6-122">UNORM</span></span> | <span data-ttu-id="245d6-123">不帶正負號的標準化整數，表示對於 n 位元數字，所有 0 都表示 0.0f，所有 1 都表示 1.0f。</span><span class="sxs-lookup"><span data-stu-id="245d6-123">Unsigned normalized integer, meaning that for an n-bit number, all 0's means 0.0f, and all 1's means 1.0f.</span></span> <span data-ttu-id="245d6-124">表示從 0.0f 到 1.0f 間隔平均的浮點值序列。</span><span class="sxs-lookup"><span data-stu-id="245d6-124">A sequence of evenly spaced floating point values from 0.0f to 1.0f are represented.</span></span> <span data-ttu-id="245d6-125">例如 2-位元 UNORM 代表 0.0f、1/3、2/3 及 1.0f。</span><span class="sxs-lookup"><span data-stu-id="245d6-125">e.g. a 2-bit UNORM represents 0.0f, 1/3, 2/3, and 1.0f.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="245d6-126">SINT</span><span class="sxs-lookup"><span data-stu-id="245d6-126">SINT</span></span>  | <span data-ttu-id="245d6-127">帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-127">Signed integer.</span></span> <span data-ttu-id="245d6-128">2 的整數補數。</span><span class="sxs-lookup"><span data-stu-id="245d6-128">2's complement integer.</span></span> <span data-ttu-id="245d6-129">例如 3-位元 SINT 代表整數值 -4、-3、-2、-1、0、1、2、3。</span><span class="sxs-lookup"><span data-stu-id="245d6-129">e.g. an 3-bit SINT represents the integral values -4, -3, -2, -1, 0, 1, 2, 3.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="245d6-130">UINT</span><span class="sxs-lookup"><span data-stu-id="245d6-130">UINT</span></span>  | <span data-ttu-id="245d6-131">不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-131">Unsigned integer.</span></span> <span data-ttu-id="245d6-132">例如 3-位元 UINT 代表整數值 0、1、2、3、4、5、6、7。</span><span class="sxs-lookup"><span data-stu-id="245d6-132">e.g. a 3-bit UINT represents the integral values 0, 1, 2, 3, 4, 5, 6, 7.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="245d6-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-133">FLOAT</span></span> | <span data-ttu-id="245d6-134">Direct3D 定義的任何表示法中的浮點值。</span><span class="sxs-lookup"><span data-stu-id="245d6-134">A floating-point value in any of the representations defined by Direct3D.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="245d6-135">SRGB</span><span class="sxs-lookup"><span data-stu-id="245d6-135">SRGB</span></span>  | <span data-ttu-id="245d6-136">類似 UNORM，對於 n-位元數字，所有 0 都表示 0.0f，所有 1 都表示 1.0f。</span><span class="sxs-lookup"><span data-stu-id="245d6-136">Similar to UNORM, in that for an n-bit number, all 0's means 0.0f and all 1's means 1.0f.</span></span> <span data-ttu-id="245d6-137">不過，與 UNORM 不同的是，若是 SRGB，介於所有 0 到所有 1 之間不帶正負號的整數編碼序列代表數字 (介於 0.0f 到 1.0f) 的浮點轉譯中的非線性數列。</span><span class="sxs-lookup"><span data-stu-id="245d6-137">However unlike UNORM, with SRGB the sequence of unsigned integer encodings between all 0's to all 1's represent a nonlinear progression in the floating point interpretation of the numbers, between 0.0f to 1.0f.</span></span> <span data-ttu-id="245d6-138">大致來說，如果這個非線性數列 SRGB 顯示為色彩序列，則會顯示為相對於「平均」觀察值的線性亮度等級坡形，在「平均」檢視條件下「平均」顯示。</span><span class="sxs-lookup"><span data-stu-id="245d6-138">Roughly, if this nonlinear progression, SRGB, is displayed as a sequence of colors, it would appear as a linear ramp of luminosity levels to an "average" observer, under "average" viewing conditions, on an "average" display.</span></span> <span data-ttu-id="245d6-139">如需完整的詳細資訊，請參考 IEC (國際電子電機委員會) 的 SRGB 色彩標準 IEC 61996-2-1。</span><span class="sxs-lookup"><span data-stu-id="245d6-139">For complete detail, refer to the SRGB color standard, IEC 61996-2-1, at IEC (International Electrotechnical Commission).</span></span>                |



 

## <a name="floating-point-conversion"></a><span data-ttu-id="245d6-140">浮點轉換</span><span class="sxs-lookup"><span data-stu-id="245d6-140">Floating Point Conversion</span></span>

<span data-ttu-id="245d6-141">只要不同的表示法之間發生浮點轉換，包括非浮點表示法之間來回轉換，就適用下列規則。</span><span class="sxs-lookup"><span data-stu-id="245d6-141">Whenever a floating point conversion between different representations occurs, including to or from non-floating point representations, the following rules apply.</span></span>

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a><span data-ttu-id="245d6-142">從較高範圍表示法轉換成較低範圍表示法</span><span class="sxs-lookup"><span data-stu-id="245d6-142">Conververting from a higher range representation to a lower range representation</span></span>

-   <span data-ttu-id="245d6-143">轉換成另一種浮點數格式時會使用 Round-to-zero (四捨五入至零)。</span><span class="sxs-lookup"><span data-stu-id="245d6-143">Round-to-zero is used during conversion to another float format.</span></span> <span data-ttu-id="245d6-144">如果目標是整數或固定點格式，則會使用 round-to-nearest-even (四捨五入至最接近的偶數)，除非轉換明確記載為使用另一種四捨五入行為，例如 FLOAT 轉換成 SNORM、FLOAT 轉換成 UNORM 或 FLOAT 轉換成 SRGB 使用的 round-to-nearest (四捨五入至最接近數字)。</span><span class="sxs-lookup"><span data-stu-id="245d6-144">If the target is an integer or fixed point format, round-to-nearest-even is used, unless the conversion is explicitly documented as using another rounding behavior, such as round-to-nearest for FLOAT to SNORM, FLOAT to UNORM or FLOAT to SRGB.</span></span> <span data-ttu-id="245d6-145">其他例外狀況為 ftoi 和 ftou shader 指令，會使用 round-to-zero (四捨五入至零)。</span><span class="sxs-lookup"><span data-stu-id="245d6-145">Other exceptions are the ftoi and ftou shader instructions, which use round-to-zero.</span></span> <span data-ttu-id="245d6-146">最後，紋理取樣工具和點陣化使用的 float-to-fixed 轉換有指定的容錯，以來自無限精確概念的 Unit-Last-Place 計算。</span><span class="sxs-lookup"><span data-stu-id="245d6-146">Finally, the float-to-fixed conversions used by the texture sampler and rasterizer have a specified tolerance measured in Unit-Last-Place from an infinitely precise ideal.</span></span>
-   <span data-ttu-id="245d6-147">若來源值大於較低範圍目標格式的動態範圍 (例如</span><span class="sxs-lookup"><span data-stu-id="245d6-147">For source values greater than the dynamic range of a lower range target format (eg.</span></span> <span data-ttu-id="245d6-148">大型 32 位元浮點值寫入 16 位元浮點值 RenderTarget)，則會得出最大可表示 (帶適當正負號) 值，「不」包括帶正負號的無限大 (因為上述的四捨五入至零)。</span><span class="sxs-lookup"><span data-stu-id="245d6-148">a large 32-bit float value is written into a 16-bit float RenderTarget), the maximum representable (appropriately signed) value results, NOT including signed infinity (due to the round to zero described above).</span></span>
-   <span data-ttu-id="245d6-149">採用較高範圍格式的 NaN 將轉換成採用較低範圍格式的 NaN 表示法，如果 NaN 表示法存在較低範圍格式中。</span><span class="sxs-lookup"><span data-stu-id="245d6-149">NaN in a higher range format will be converted to NaN representation in the lower range format if the NaN representation exists in the lower range format.</span></span> <span data-ttu-id="245d6-150">如果較低格式沒有 NaN 表示法，則結果會是 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-150">If the lower format does not have a NaN representation, the result will be 0.</span></span>
-   <span data-ttu-id="245d6-151">採用較高範圍格式的 INF 將會轉換成採用較低範圍格式的 INF (如有的話)。</span><span class="sxs-lookup"><span data-stu-id="245d6-151">INF in a higher range format will be converted to INF in the lower range format if available.</span></span> <span data-ttu-id="245d6-152">如果較低格式沒有 INF 表示法，它將會轉換成可表示的最大值。</span><span class="sxs-lookup"><span data-stu-id="245d6-152">If the lower format does not have an INF representation, it will be converted to the maximum value representable.</span></span> <span data-ttu-id="245d6-153">正負號將保留，如果目標格式中提供。</span><span class="sxs-lookup"><span data-stu-id="245d6-153">The sign will be preserved if available in the target format.</span></span>
-   <span data-ttu-id="245d6-154">採用較高範圍格式的 Denorm 將會轉換成採用較低範圍格式的 Denorm 表示法 (如較低範圍格式中有提供且可轉換)，否則結果會是 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-154">Denorm in a higher range format will be converted to the Denorm representation in the lower range format if available in the lower range format and the conversion is possible, otherwise the result is 0.</span></span> <span data-ttu-id="245d6-155">正負號位元將保留，如果目標格式中提供。</span><span class="sxs-lookup"><span data-stu-id="245d6-155">The sign bit will be preserved if available in the target format.</span></span>

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a><span data-ttu-id="245d6-156">從較低範圍表示法轉換成較高範圍表示法</span><span class="sxs-lookup"><span data-stu-id="245d6-156">Converting from a lower range representation to a higher range representation</span></span>

-   <span data-ttu-id="245d6-157">採用較低範圍格式的 NaN 將轉換成採用較高範圍格式的 NaN 表示法 (如果較高範圍格式中有提供)。</span><span class="sxs-lookup"><span data-stu-id="245d6-157">NaN in a lower range format will be converted to the NaN representation in the higher range format if available in the higher range format.</span></span> <span data-ttu-id="245d6-158">如果較高範圍格式沒有 NaN 表示法，它將會轉換成 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-158">If the higher range format does not have a NaN representation, it will be converted to 0.</span></span>
-   <span data-ttu-id="245d6-159">採用較低範圍格式的 INF 將轉換成採用較高範圍格式的 INF 表示法 (如果較高範圍格式中有提供)。</span><span class="sxs-lookup"><span data-stu-id="245d6-159">INF in a lower range format will be converted to the INF representation in the higher range format if available in the higher range format.</span></span> <span data-ttu-id="245d6-160">如果較高的格式沒有 INF 標記法，則會將它轉換成該格式)  (最大浮點數的最大值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="245d6-160">If the higher format does not have an INF representation, it will be converted to the maximum value representable (MAX\_FLOAT in that format).</span></span> <span data-ttu-id="245d6-161">正負號將保留，如果目標格式中提供。</span><span class="sxs-lookup"><span data-stu-id="245d6-161">The sign will be preserved if available in the target format.</span></span>
-   <span data-ttu-id="245d6-162">採用較低範圍格式的 Denorm 將轉換成採用較高範圍格式的標準化表示法 (如有可能)，或是轉換成採用較高範圍格式的 Denorm 表示法 (如果 Denorm 表示法存在)。</span><span class="sxs-lookup"><span data-stu-id="245d6-162">Denorm in a lower range format will be converted to a normalized representation in the higher range format if possible, or else to a Denorm representation in the higher range format if the Denorm representation exists.</span></span> <span data-ttu-id="245d6-163">若較高範圍格式沒有 Denorm 表示法，則這些都會失敗，且它將會轉換成 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-163">Failing those, if the higher range format does not have a Denorm representation, it will be converted to 0.</span></span> <span data-ttu-id="245d6-164">正負號將保留，如果目標格式中提供。</span><span class="sxs-lookup"><span data-stu-id="245d6-164">The sign will be preserved if available in the target format.</span></span> <span data-ttu-id="245d6-165">請注意，32 位元浮點數計算格式時不會採用 Denorm 表示法 (因為 32 位元浮點數運算中，Denorm 會清除為保留正負號的 0)。</span><span class="sxs-lookup"><span data-stu-id="245d6-165">Note that 32-bit float numbers count as a format without a Denorm representation (because Denorms in operations on 32-bit floats flush to sign preserved 0).</span></span>

## <a name="integer-conversion"></a><span data-ttu-id="245d6-166">整數轉換</span><span class="sxs-lookup"><span data-stu-id="245d6-166">Integer Conversion</span></span>

<span data-ttu-id="245d6-167">下表描述從上述各種不同的表示法轉換成其他表示法。</span><span class="sxs-lookup"><span data-stu-id="245d6-167">The following table describes conversions from various representations described above to other representations.</span></span> <span data-ttu-id="245d6-168">只會顯示實際在 Direct3D 中發生的轉換。</span><span class="sxs-lookup"><span data-stu-id="245d6-168">Only conversions that actually occur in Direct3D are shown.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="245d6-169">來源資料類型</span><span class="sxs-lookup"><span data-stu-id="245d6-169">Source Data Type</span></span></th>
<th><span data-ttu-id="245d6-170">目的地資料類型</span><span class="sxs-lookup"><span data-stu-id="245d6-170">Destination Data Type</span></span></th>
<th><span data-ttu-id="245d6-171">轉換規則</span><span class="sxs-lookup"><span data-stu-id="245d6-171">Conversion Rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="245d6-172">SNORM</span><span class="sxs-lookup"><span data-stu-id="245d6-172">SNORM</span></span></td>
<td><span data-ttu-id="245d6-173">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-173">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-174">假設有一個 n-位元整數值，代表帶正負號的範圍 [-1.0f 至 1.0f]，轉換成浮點數的方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="245d6-174">Given an n-bit integer value representing the signed range [-1.0f to 1.0f], conversion to floating-point is as follows.</span></span><br/>
<ul>
<li><span data-ttu-id="245d6-175">最大負值對應至 -1.0f。</span><span class="sxs-lookup"><span data-stu-id="245d6-175">The most-negative value maps to -1.0f.</span></span> <span data-ttu-id="245d6-176">例如 5-位元值 10000 對應至 -1.0f。</span><span class="sxs-lookup"><span data-stu-id="245d6-176">e.g. the 5-bit value 10000 maps to -1.0f.</span></span></li>
<li><span data-ttu-id="245d6-177">其他每一個值都會轉換成浮點數 (稱為 c)，然後結果 = c \* (1.0f / (2⁽ⁿ⁻¹⁾-1))。</span><span class="sxs-lookup"><span data-stu-id="245d6-177">Every other value is converted to a float (call it c), and then result = c \* (1.0f / (2⁽ⁿ⁻¹⁾-1)).</span></span> <span data-ttu-id="245d6-178">例如，5 位元值 10001 轉換成 -15.0f，然後除以 15.0f，得出 -1.0f。</span><span class="sxs-lookup"><span data-stu-id="245d6-178">For example the 5-bit value 10001 is converted to -15.0f, and then divided by 15.0f, yielding -1.0f.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245d6-179">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-179">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-180">SNORM</span><span class="sxs-lookup"><span data-stu-id="245d6-180">SNORM</span></span></td>
<td><span data-ttu-id="245d6-181">假設有一個浮點數，轉換成代表帶正負號的範圍 [-1.0f 至 1.0f] 的 n-位元整數值的方式如下所述。</span><span class="sxs-lookup"><span data-stu-id="245d6-181">Given a floating-point number, conversion to an n-bit integer value representing the signed range [-1.0f to 1.0f] is as follows.</span></span><br/>
<ul>
<li><span data-ttu-id="245d6-182">讓 c 代表開始值。</span><span class="sxs-lookup"><span data-stu-id="245d6-182">Let c represent the starting value.</span></span></li>
<li><span data-ttu-id="245d6-183">如果 c 是 NaN，則結果是 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-183">If c is NaN, the result is 0.</span></span></li>
<li><span data-ttu-id="245d6-184">如果 c > 1.0 f，包括 INF，則會壓制到 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="245d6-184">If c > 1.0f, including INF, it is clamped to 1.0f.</span></span></li>
<li><span data-ttu-id="245d6-185">如果 c <-1.0 f （包括-INF）壓制為-1.0 f。</span><span class="sxs-lookup"><span data-stu-id="245d6-185">If c < -1.0f, including -INF, it is clamped to -1.0f.</span></span></li>
<li><span data-ttu-id="245d6-186">從浮點數進位法轉換成整數進位法：c = c \* (2ⁿ⁻¹-1)。</span><span class="sxs-lookup"><span data-stu-id="245d6-186">Convert from float scale to integer scale: c = c \* (2ⁿ⁻¹-1).</span></span></li>
<li><span data-ttu-id="245d6-187">如下所述轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-187">Convert to an integer as follows.</span></span>
<ul>
<li><span data-ttu-id="245d6-188">如果 c >= 0，則 c = c + 0.5 f，否則 c = c-0.5 f。</span><span class="sxs-lookup"><span data-stu-id="245d6-188">If c >= 0 then c = c + 0.5f, otherwise, c = c - 0.5f.</span></span></li>
<li><span data-ttu-id="245d6-189">去除小數，剩餘的浮點 (整數) 值就會直接轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-189">Drop the decimal fraction, and the remaining floating point (integral) value is converted directly to an integer.</span></span></li>
</ul></li>
</ul>
<span data-ttu-id="245d6-190">此轉換容許的容錯為 D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place Unit-Last-Place (整數端)。</span><span class="sxs-lookup"><span data-stu-id="245d6-190">This conversion is permitted a tolerance of D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place Unit-Last-Place (on the integer side).</span></span> <span data-ttu-id="245d6-191">這表示，從浮點數轉換成整數進位法之後，可表示的目標格式值的 D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place 內的任何值都可對應至該值。</span><span class="sxs-lookup"><span data-stu-id="245d6-191">This means that after converting from float to integer scale, any value within D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place of a representable target format value is permitted to map to that value.</span></span> <span data-ttu-id="245d6-192">額外的資料可逆性需求可確保轉換在整個範圍內不減少，而且所有輸出值都可實現。</span><span class="sxs-lookup"><span data-stu-id="245d6-192">The additional Data Invertability requirement ensures that the conversion is nondecreasing across the range and all output values are attainable.</span></span> <span data-ttu-id="245d6-193">(在此處顯示的常數中，<em>xx</em> 應取代為 Direct3D 版本，例如 10、11 或 12)</span><span class="sxs-lookup"><span data-stu-id="245d6-193">(In the constants shown here, <em>xx</em> should be replaced with the Direct3D version, for example 10, 11, or 12.)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="245d6-194">UNORM</span><span class="sxs-lookup"><span data-stu-id="245d6-194">UNORM</span></span></td>
<td><span data-ttu-id="245d6-195">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-195">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-196">開始的 n 位元值會轉換成浮點數 (0.0f、1.0f、2.0f 等)，然後除以 (2ⁿ-1)。</span><span class="sxs-lookup"><span data-stu-id="245d6-196">The starting n-bit value is converted to float (0.0f, 1.0f, 2.0f, etc.) and then divided by (2ⁿ-1).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245d6-197">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-197">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-198">UNORM</span><span class="sxs-lookup"><span data-stu-id="245d6-198">UNORM</span></span></td>
<td><span data-ttu-id="245d6-199">讓 c 代表開始值。</span><span class="sxs-lookup"><span data-stu-id="245d6-199">Let c represent the starting value.</span></span><br/>
<ul>
<li><span data-ttu-id="245d6-200">如果 c 是 NaN，則結果是 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-200">If c is NaN, the result is 0.</span></span></li>
<li><span data-ttu-id="245d6-201">如果 c > 1.0 f，包括 INF，則會壓制到 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="245d6-201">If c > 1.0f, including INF, it is clamped to 1.0f.</span></span></li>
<li><span data-ttu-id="245d6-202">如果 c < 0.0 f （包括-INF）壓制為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="245d6-202">If c < 0.0f, including -INF, it is clamped to 0.0f.</span></span></li>
<li><span data-ttu-id="245d6-203">從浮點數進位法轉換成整數進位法：c = c \* (2ⁿ-1)。</span><span class="sxs-lookup"><span data-stu-id="245d6-203">Convert from float scale to integer scale: c = c \* (2ⁿ-1).</span></span></li>
<li><span data-ttu-id="245d6-204">轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-204">Convert to integer.</span></span>
<ul>
<li><span data-ttu-id="245d6-205">c = c + 0.5f。</span><span class="sxs-lookup"><span data-stu-id="245d6-205">c = c + 0.5f.</span></span></li>
<li><span data-ttu-id="245d6-206">小數會去除，剩餘的浮點 (整數) 值就會直接轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-206">The decimal fraction is dropped, and the remaining floating point (integral) value is converted directly to an integer.</span></span></li>
</ul></li>
</ul>
<span data-ttu-id="245d6-207">此轉換容許的容錯為 D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (整數端)。</span><span class="sxs-lookup"><span data-stu-id="245d6-207">This conversion is permitted a tolerance of D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (on the integer side).</span></span> <span data-ttu-id="245d6-208">這表示，從浮點數轉換成整數進位法之後，可表示的目標格式值的 D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place 內的任何值都可對應至該值。</span><span class="sxs-lookup"><span data-stu-id="245d6-208">This means that after converting from float to integer scale, any value within D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place of a representable target format value is permitted to map to that value.</span></span> <span data-ttu-id="245d6-209">額外的資料可逆性需求可確保轉換在整個範圍內不減少，而且所有輸出值都可實現。</span><span class="sxs-lookup"><span data-stu-id="245d6-209">The additional Data Invertability requirement ensures that the conversion is nondecreasing across the range and all output values are attainable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="245d6-210">SRGB</span><span class="sxs-lookup"><span data-stu-id="245d6-210">SRGB</span></span></td>
<td><span data-ttu-id="245d6-211">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-211">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-212">以下是理想的 SRGB 至 FLOAT 轉換。</span><span class="sxs-lookup"><span data-stu-id="245d6-212">The following is the ideal SRGB to FLOAT conversion.</span></span><br/>
<ul>
<li><span data-ttu-id="245d6-213">取一個開始的 n 位元值，將它轉換成浮點數 (0.0f、1.0f、2.0f 等)；將此稱為 c。</span><span class="sxs-lookup"><span data-stu-id="245d6-213">Take the starting n-bit value, convert it a float (0.0f, 1.0f, 2.0f, etc.); call this c.</span></span></li>
<li><span data-ttu-id="245d6-214">c = c \* (1.0f / (2ⁿ-1))</span><span class="sxs-lookup"><span data-stu-id="245d6-214">c = c \* (1.0f / (2ⁿ-1))</span></span></li>
<li><span data-ttu-id="245d6-215">如果 (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD) then： result = c/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_1，否則： result = ( (c + d3d<em>xx</em>_SRGB_TO_FLOAT_OFFSET) /D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_2) D3D<em>xx</em>_SRGB_TO_FLOAT_EXPONENT</span><span class="sxs-lookup"><span data-stu-id="245d6-215">If (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD) then: result = c / D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_1, else: result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_2)D3D<em>xx</em>_SRGB_TO_FLOAT_EXPONENT</span></span></li>
</ul>
<span data-ttu-id="245d6-216">此轉換容許的容錯為 D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP Unit-Last-Place (SRGB 端)。</span><span class="sxs-lookup"><span data-stu-id="245d6-216">This conversion is permitted a tolerance of D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP Unit-Last-Place (on the SRGB side).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245d6-217">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-217">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-218">SRGB</span><span class="sxs-lookup"><span data-stu-id="245d6-218">SRGB</span></span></td>
<td><span data-ttu-id="245d6-219">以下是理想的 FLOAT > SRGB 轉換。</span><span class="sxs-lookup"><span data-stu-id="245d6-219">The following is the ideal FLOAT -> SRGB conversion.</span></span><br/> <span data-ttu-id="245d6-220">假設目標 SRGB 色彩元件有 n 個位元：</span><span class="sxs-lookup"><span data-stu-id="245d6-220">Assuming the target SRGB color component has n bits:</span></span><br/>
<ul>
<li><span data-ttu-id="245d6-221">假設開始值是 c。</span><span class="sxs-lookup"><span data-stu-id="245d6-221">Suppose the starting value is c.</span></span></li>
<li><span data-ttu-id="245d6-222">如果 c 是 NaN，則結果是 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-222">If c is NaN, the result is 0.</span></span></li>
<li><span data-ttu-id="245d6-223">如果 c > 1.0 f （包括 INF）壓制至 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="245d6-223">If c > 1.0f, including INF, is clamped to 1.0f.</span></span></li>
<li><span data-ttu-id="245d6-224">如果 c < 0.0 f （包括-INF）壓制為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="245d6-224">If c < 0.0f, including -INF, it is clamped to 0.0f.</span></span></li>
<li><span data-ttu-id="245d6-225">如果 (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD) then： c = d3d<em>xx</em>_FLOAT_TO_SRGB_SCALE_1 \* c，否則： c = d3d<em>XX</em>_FLOAT_TO_SRGB_SCALE_2 \* c (D3D<em>XX</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/d3d<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR) -D3D<em>xx</em>_FLOAT_TO_SRGB_OFFSET</span><span class="sxs-lookup"><span data-stu-id="245d6-225">If (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD) then: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_1 \* c, else: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_2 \* c(D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR) - D3D<em>xx</em>_FLOAT_TO_SRGB_OFFSET</span></span></li>
<li><span data-ttu-id="245d6-226">從浮點數進位法轉換成整數進位法：c = c \* (2ⁿ-1)。</span><span class="sxs-lookup"><span data-stu-id="245d6-226">Convert from float scale to integer scale: c = c \* (2ⁿ-1).</span></span></li>
<li><span data-ttu-id="245d6-227">轉換成整數：</span><span class="sxs-lookup"><span data-stu-id="245d6-227">Convert to integer:</span></span>
<ul>
<li><span data-ttu-id="245d6-228">c = c + 0.5f。</span><span class="sxs-lookup"><span data-stu-id="245d6-228">c = c + 0.5f.</span></span></li>
<li><span data-ttu-id="245d6-229">小數會去除，剩餘的浮點 (整數) 值就會直接轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-229">The decimal fraction is dropped, and the remaining floating point (integral) value is converted directly to an integer.</span></span></li>
</ul></li>
</ul>
<span data-ttu-id="245d6-230">此轉換容許的容錯為 D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (整數端)。</span><span class="sxs-lookup"><span data-stu-id="245d6-230">This conversion is permitted a tolerance of D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (on the integer side).</span></span> <span data-ttu-id="245d6-231">這表示，從浮點數轉換成整數進位法之後，可表示的目標格式值的 D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place 內的任何值都可對應至該值。</span><span class="sxs-lookup"><span data-stu-id="245d6-231">This means that after converting from float to integer scale, any value within D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place of a representable target format value is permitted to map to that value.</span></span> <span data-ttu-id="245d6-232">額外的資料可逆性需求可確保轉換在整個範圍內不減少，而且所有輸出值都可實現。</span><span class="sxs-lookup"><span data-stu-id="245d6-232">The additional Data Invertability requirement ensures that the conversion is nondecreasing across the range and all output values are attainable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="245d6-233">SINT</span><span class="sxs-lookup"><span data-stu-id="245d6-233">SINT</span></span></td>
<td><span data-ttu-id="245d6-234">SINT 與更多位元</span><span class="sxs-lookup"><span data-stu-id="245d6-234">SINT With More Bits</span></span></td>
<td><span data-ttu-id="245d6-235">若要從 SINT 轉換成 SINT 與更多位元，開始數字的最高有效位元 (MSB) 會是 &quot;正負號延伸&quot; 至目標格式中提供的其他位元。</span><span class="sxs-lookup"><span data-stu-id="245d6-235">To convert from SINT to an SINT with more bits, the most significant bit (MSB) of the starting number is &quot;sign-extended&quot; to the additional bits available in the target format.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245d6-236">UINT</span><span class="sxs-lookup"><span data-stu-id="245d6-236">UINT</span></span></td>
<td><span data-ttu-id="245d6-237">SINT 與更多位元</span><span class="sxs-lookup"><span data-stu-id="245d6-237">SINT With More Bits</span></span></td>
<td><span data-ttu-id="245d6-238">若要從 UINT 轉換成 SINT 與更多位元，數字會複製到目標格式的最低有效位元 (LSB)，且其他 MSB 會以 0 填入。</span><span class="sxs-lookup"><span data-stu-id="245d6-238">To convert from UINT to an SINT with more bits, the number is copied to the target format's least significant bits (LSBs) and additional MSBs are padded with 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="245d6-239">SINT</span><span class="sxs-lookup"><span data-stu-id="245d6-239">SINT</span></span></td>
<td><span data-ttu-id="245d6-240">UINT 與更多位元</span><span class="sxs-lookup"><span data-stu-id="245d6-240">UINT With More Bits</span></span></td>
<td><span data-ttu-id="245d6-241">若要從 SINT 轉換成 UINT 與更多位元：如果是負數，值會限制為 0。</span><span class="sxs-lookup"><span data-stu-id="245d6-241">To convert from SINT to UINT with more bits: If negative, the value is clamped to 0.</span></span> <span data-ttu-id="245d6-242">否則數字會複製到目標格式的 LSB，且其他 MSB 會以 0 填入。</span><span class="sxs-lookup"><span data-stu-id="245d6-242">Otherwise the number is copied to the target format's LSBs and additional MSB's are padded with 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245d6-243">UINT</span><span class="sxs-lookup"><span data-stu-id="245d6-243">UINT</span></span></td>
<td><span data-ttu-id="245d6-244">UINT 與更多位元</span><span class="sxs-lookup"><span data-stu-id="245d6-244">UINT With More Bits</span></span></td>
<td><span data-ttu-id="245d6-245">若要從 UINT 轉換成 UINT 與更多位元，數字會複製到目標格式的 LSB，且其他 MSB 會以 0 填入。</span><span class="sxs-lookup"><span data-stu-id="245d6-245">To convert from UINT to UINT with more bits the number is copied to the target format's LSBs and additional MSB's are padded with 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="245d6-246">SINT 或 UINT</span><span class="sxs-lookup"><span data-stu-id="245d6-246">SINT or UINT</span></span></td>
<td><span data-ttu-id="245d6-247">SINT 或 UINT 與更少或等於位元</span><span class="sxs-lookup"><span data-stu-id="245d6-247">SINT or UINT With Fewer or Equal Bits</span></span></td>
<td><span data-ttu-id="245d6-248">若要從 SINT 或 UINT 轉換成 SINT 或 UINT 與更少或等於位元 (和/或正負號變更)，只會將開始值限制為目標格式的範圍。</span><span class="sxs-lookup"><span data-stu-id="245d6-248">To convert from a SINT or UINT to SINT or UINT with fewer or equal bits (and/or change in signedness), the starting value is simply clamped to the range of the target format.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a><span data-ttu-id="245d6-249">固定點整數轉換</span><span class="sxs-lookup"><span data-stu-id="245d6-249">Fixed Point Integer Conversion</span></span>

<span data-ttu-id="245d6-250">固定點整數單純是某個位元大小的整數，其中某個固定位置有隱含的小數點。</span><span class="sxs-lookup"><span data-stu-id="245d6-250">Fixed point integers are simply integers of some bit size that have an implicit decimal point at a fixed location.</span></span>

<span data-ttu-id="245d6-251">普遍的「整數」資料類型是固定點整數的特殊案例，小數點位於數字結尾。</span><span class="sxs-lookup"><span data-stu-id="245d6-251">The ubiquitous "integer" data type is a special case of a fixed point integer with the decimal at the end of the number.</span></span>

<span data-ttu-id="245d6-252">固定點數字表示法描述如下：i.f，其中 i 是整數位元數，f 是分數位元數。</span><span class="sxs-lookup"><span data-stu-id="245d6-252">Fixed point number representations are characterized as: i.f, where i is the number of integer bits and f is the number of fractional bits.</span></span> <span data-ttu-id="245d6-253">例如 16.8 表示 16 位元整數，後面接著 8 位元分數。</span><span class="sxs-lookup"><span data-stu-id="245d6-253">e.g. 16.8 means 16 bits integer followed by 8 bits of fraction.</span></span> <span data-ttu-id="245d6-254">整數部分是以 2 的補數儲存，至少如此處鎖定一 (雖然它同樣可以對不帶正負號的整數定義)。</span><span class="sxs-lookup"><span data-stu-id="245d6-254">The integer part is stored in 2's complement, at least as defined here (though it can be defined equally for unsigned integers as well).</span></span> <span data-ttu-id="245d6-255">分數部分是以不帶正負號的形式儲存。</span><span class="sxs-lookup"><span data-stu-id="245d6-255">The fractional part is stored in unsigned form.</span></span> <span data-ttu-id="245d6-256">分數部分一律代表正分數，介於最接近的兩個整數值之間，從最大負數開始。</span><span class="sxs-lookup"><span data-stu-id="245d6-256">The fractional part always represents the positive fraction between the two nearest integral values, starting from the most negative.</span></span>

<span data-ttu-id="245d6-257">固定點數字的加減運算是單純使用標準整數算術執行，不考慮隱含的小數點位置。</span><span class="sxs-lookup"><span data-stu-id="245d6-257">Addition and subtraction operations on fixed point numbers are performed simply using standard integer arithmetic, without any consideration for where the implied decimal lies.</span></span> <span data-ttu-id="245d6-258">將 16.8 固定點數字加 1，僅表示加上 256，因為小數點在數字最低有效結尾起算的第 8 位。</span><span class="sxs-lookup"><span data-stu-id="245d6-258">Adding 1 to a 16.8 fixed point number just means adding 256, since the decimal is 8 places in from the least significant end of the number.</span></span> <span data-ttu-id="245d6-259">其他運算像是乘法，同樣可以單純使用整數算術執行，假設考慮對固定小數點的效果。</span><span class="sxs-lookup"><span data-stu-id="245d6-259">Other operations such as multiplication, can be performed as well simply using integer arithmetic, provided the effect on the fixed decimal is accounted for.</span></span> <span data-ttu-id="245d6-260">例如，使用整數乘法將兩個 16.8 整數相乘，會得到 32.16 的結果。</span><span class="sxs-lookup"><span data-stu-id="245d6-260">For example, multiplying two 16.8 integers using an integer multiply produces a 32.16 result.</span></span>

<span data-ttu-id="245d6-261">固定點整數表示法在 Direct3D 中使用的方式有兩種。</span><span class="sxs-lookup"><span data-stu-id="245d6-261">Fixed point integer representations are used in two ways in Direct3D.</span></span>

-   <span data-ttu-id="245d6-262">點陣化中後續剪裁的頂點位置會貼齊固定點，以便跨 RenderTarget 區域統一分配精確度。</span><span class="sxs-lookup"><span data-stu-id="245d6-262">Post-clipped vertex positions in the rasterizer are snapped to fixed point, to uniformly distribute precision across the RenderTarget area.</span></span> <span data-ttu-id="245d6-263">許多點陣化運算 (例如面消除) 是在固定點貼齊位置上發生，其他運算 (像是屬性 Interpolator 設定) 則使用已從固定點貼齊位置轉換回浮點數的位置。</span><span class="sxs-lookup"><span data-stu-id="245d6-263">Many rasterizer operations, including face culling as one example, occur on fixed point snapped positions, while other operations, such as attribute interpolator setup, use positions that have been converted back to floating point from the fixed point snapped positions.</span></span>
-   <span data-ttu-id="245d6-264">取樣作業的紋理座標會貼齊固定點 (經過紋理大小縮放後)，以跨紋理空間統一分配精確度，以便選擇篩選點選位置/權重。</span><span class="sxs-lookup"><span data-stu-id="245d6-264">Texture coordinates for sampling operations are snapped to fixed point (after being scaled by texture size), to uniformly distribute precision across texture space, in choosing filter tap locations/weights.</span></span> <span data-ttu-id="245d6-265">權重值會在進行實際篩選算術之前轉換回浮點數。</span><span class="sxs-lookup"><span data-stu-id="245d6-265">Weight values are converted back to floating point before actual filtering arithmetic is performed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="245d6-266">來源資料類型</span><span class="sxs-lookup"><span data-stu-id="245d6-266">Source Data Type</span></span></th>
<th><span data-ttu-id="245d6-267">目的地資料類型</span><span class="sxs-lookup"><span data-stu-id="245d6-267">Destination Data Type</span></span></th>
<th><span data-ttu-id="245d6-268">轉換規則</span><span class="sxs-lookup"><span data-stu-id="245d6-268">Conversion Rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="245d6-269">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-269">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-270">固定點整數</span><span class="sxs-lookup"><span data-stu-id="245d6-270">Fixed Point Integer</span></span></td>
<td><span data-ttu-id="245d6-271">以下是將浮點數 n 轉換成固定點整數 i.f 的一般程序，其中 i 是 (帶正負號的) 整數位元數，f 是分數位元數。</span><span class="sxs-lookup"><span data-stu-id="245d6-271">The following is the general procedure for converting a floating point number n to a fixed point integer i.f, where i is the number of (signed) integer bits and f is the number of fractional bits.</span></span><br/>
<ul>
<li><span data-ttu-id="245d6-272">計算 FixedMin = -2⁽ⁱ⁻¹⁾</span><span class="sxs-lookup"><span data-stu-id="245d6-272">Compute FixedMin = -2⁽ⁱ⁻¹⁾</span></span></li>
<li><span data-ttu-id="245d6-273">Compute FixedMax = 2 ⁽ⁱ⁻¹⁾-2<sup> (-f) </sup></span><span class="sxs-lookup"><span data-stu-id="245d6-273">Compute FixedMax = 2⁽ⁱ⁻¹⁾ - 2<sup>(-f)</sup></span></span></li>
<li><span data-ttu-id="245d6-274">如果 n 是 NaN，則結果 = 0;如果 n 是 + Inf，result = FixedMax \* 2<sup>f</sup>;如果 n 是-Inf，result = FixedMin \* 2<sup>f</sup></span><span class="sxs-lookup"><span data-stu-id="245d6-274">If n is a NaN, result = 0; if n is +Inf, result = FixedMax*2<sup>f</sup>; if n is -Inf, result = FixedMin*2<sup>f</sup></span></span></li>
<li><span data-ttu-id="245d6-275">如果 n >= FixedMax，result = Fixedmax \* 2<sup>f</sup>;如果 n <= FixedMin，result = FixedMin \* 2 <sup> f</span><span class="sxs-lookup"><span data-stu-id="245d6-275">If n >= FixedMax, result = Fixedmax*2<sup>f</sup>; if n <= FixedMin, result = FixedMin*2<sup>f</span></span></sup></li>
<li><span data-ttu-id="245d6-276">否則計算 n\*2<sup>f</sup> 並轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="245d6-276">Else compute n\*2<sup>f</sup> and convert to integer.</span></span></li>
</ul>
<span data-ttu-id="245d6-277">實作在整數結果中容許 D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place 容錯，而非上方最後一個步驟之後的無限精確值 n\*2<sup>f</sup>。</span><span class="sxs-lookup"><span data-stu-id="245d6-277">Implementations are permitted D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place tolerance in the integer result, instead of the infinitely precise value n\*2<sup>f</sup> after the last step above.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="245d6-278">固定點整數</span><span class="sxs-lookup"><span data-stu-id="245d6-278">Fixed Point Integer</span></span></td>
<td><span data-ttu-id="245d6-279">FLOAT</span><span class="sxs-lookup"><span data-stu-id="245d6-279">FLOAT</span></span></td>
<td><span data-ttu-id="245d6-280">假設要轉換成浮點數的特定固定點表示法未包含總計超過 24 個位元的資訊，則分數元件中不會超過其中的 23 個位元。</span><span class="sxs-lookup"><span data-stu-id="245d6-280">Assume that the specific fixed point representation being converted to float does not contain more than a total of 24 bits of information, no more than 23 bits of which is in the fractional component.</span></span> <span data-ttu-id="245d6-281">假設某個固定點數字 fxp 採用 i.f 形式 (i 位元整數，f 位元分數)。</span><span class="sxs-lookup"><span data-stu-id="245d6-281">Suppose a given fixed point number, fxp, is in i.f form (i bits integer, f bits fraction).</span></span> <span data-ttu-id="245d6-282">轉換成浮點數類似下列虛擬程式碼。</span><span class="sxs-lookup"><span data-stu-id="245d6-282">The conversion to float is akin to the following pseudocode.</span></span><br/> <span data-ttu-id="245d6-283">float result = (float)  (fxp >> f) +//解壓縮整數</span><span class="sxs-lookup"><span data-stu-id="245d6-283">float result = (float)(fxp >> f) + // extract integer</span></span><br/> <dl> <span data-ttu-id="245d6-284"> ( (float)  (fxp & (2<sup>f</sup> - 1) ) / (2<sup>f</sup>) ) ;//解壓縮分數</span><span class="sxs-lookup"><span data-stu-id="245d6-284">((float)(fxp & (2<sup>f</sup> - 1)) / (2<sup>f</sup>)); // extract fraction</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="245d6-285">相關主題</span><span class="sxs-lookup"><span data-stu-id="245d6-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="245d6-286"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="245d6-286">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




