---
title: VML Eqn 屬性
description: VML Eqn 屬性
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da00084a825147c6f8a05f503e5ee2679f40e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316414"
---
# <a name="vml-eqn-attribute"></a><span data-ttu-id="d8d31-103">VML Eqn 屬性</span><span class="sxs-lookup"><span data-stu-id="d8d31-103">VML Eqn Attribute</span></span>

<span data-ttu-id="d8d31-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="d8d31-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d8d31-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="d8d31-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d8d31-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="d8d31-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d8d31-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="d8d31-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d8d31-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="d8d31-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d8d31-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="d8d31-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d8d31-110">定義公式所使用的方程式。</span><span class="sxs-lookup"><span data-stu-id="d8d31-110">Defines the equation used by a formula.</span></span> <span data-ttu-id="d8d31-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d8d31-111">Read/write.</span></span> <span data-ttu-id="d8d31-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="d8d31-112">**String**.</span></span>

<span data-ttu-id="d8d31-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="d8d31-113">**Applies To**</span></span>

<span data-ttu-id="d8d31-114">[公式](msdn-online-vml-formulas-element.md)) 的[F](msdn-online-vml-f-element.md) (子項目</span><span class="sxs-lookup"><span data-stu-id="d8d31-114">[F](msdn-online-vml-f-element.md) (subelement of [Formulas](msdn-online-vml-formulas-element.md))</span></span>

<span data-ttu-id="d8d31-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="d8d31-115">**Tag Syntax**</span></span>

<span data-ttu-id="d8d31-116"><v： *element* eqn = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d8d31-116"><v: *element* eqn=" *expression* "></span></span>

<span data-ttu-id="d8d31-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="d8d31-117">**Script Syntax**</span></span>

<span data-ttu-id="d8d31-118"> eqn = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d8d31-118">*element* .eqn="*expression*"</span></span>

<span data-ttu-id="d8d31-119">*運算式* =\*\* eqn</span><span class="sxs-lookup"><span data-stu-id="d8d31-119">*expression*=*element*.eqn</span></span>

<span data-ttu-id="d8d31-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="d8d31-120">**Remarks**</span></span>

<span data-ttu-id="d8d31-121">方程式是藉由評估具有運算一般形式的文字運算式來定義，並在後面加上最多三個引數。</span><span class="sxs-lookup"><span data-stu-id="d8d31-121">Equations are defined by the evaluation of a text expression that has the general form of an operation followed by up to three arguments.</span></span> <span data-ttu-id="d8d31-122">每個引數都可以是下列類型：</span><span class="sxs-lookup"><span data-stu-id="d8d31-122">Each argument may be of the following types:</span></span>

-   <span data-ttu-id="d8d31-123">調整 (例如， \# 2) </span><span class="sxs-lookup"><span data-stu-id="d8d31-123">adjustment (for example, \#2)</span></span>
-   <span data-ttu-id="d8d31-124">另一個公式 (例如， @2) </span><span class="sxs-lookup"><span data-stu-id="d8d31-124">another formula (for example, @2)</span></span>
-   <span data-ttu-id="d8d31-125">固定數位 (例如，2) </span><span class="sxs-lookup"><span data-stu-id="d8d31-125">fixed numbers (for example, 2)</span></span>
-   <span data-ttu-id="d8d31-126">預先定義的值</span><span class="sxs-lookup"><span data-stu-id="d8d31-126">predefined values</span></span>

<span data-ttu-id="d8d31-127">下表定義可搭配選擇性引數使用的公式，指定名稱為 *v*、 *p1* 和 *p2*。公式模式為：</span><span class="sxs-lookup"><span data-stu-id="d8d31-127">The table below defines the formulas that can be used withthe optional arguments given the names *v*, *p1*, and *p2*.The formula pattern is:</span></span>

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| <span data-ttu-id="d8d31-128">作業</span><span class="sxs-lookup"><span data-stu-id="d8d31-128">Operation</span></span> | <span data-ttu-id="d8d31-129">Params</span><span class="sxs-lookup"><span data-stu-id="d8d31-129">Params</span></span> | <span data-ttu-id="d8d31-130">精確</span><span class="sxs-lookup"><span data-stu-id="d8d31-130">Exact</span></span>  | <span data-ttu-id="d8d31-131">結果</span><span class="sxs-lookup"><span data-stu-id="d8d31-131">Result</span></span>                    | <span data-ttu-id="d8d31-132">描述</span><span class="sxs-lookup"><span data-stu-id="d8d31-132">Description</span></span>                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d8d31-133">瓦爾</span><span class="sxs-lookup"><span data-stu-id="d8d31-133">val</span></span>       | <span data-ttu-id="d8d31-134">1</span><span class="sxs-lookup"><span data-stu-id="d8d31-134">1</span></span>      | <span data-ttu-id="d8d31-135">是</span><span class="sxs-lookup"><span data-stu-id="d8d31-135">yes</span></span>    | <span data-ttu-id="d8d31-136">v</span><span class="sxs-lookup"><span data-stu-id="d8d31-136">v</span></span>                         | <span data-ttu-id="d8d31-137">定義其他值的輔助線值。</span><span class="sxs-lookup"><span data-stu-id="d8d31-137">Defines a guide value from some other value.</span></span>                                   |
| <span data-ttu-id="d8d31-138">Sum</span><span class="sxs-lookup"><span data-stu-id="d8d31-138">sum</span></span>       | <span data-ttu-id="d8d31-139">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-139">3</span></span>      | <span data-ttu-id="d8d31-140">是</span><span class="sxs-lookup"><span data-stu-id="d8d31-140">yes</span></span>    | <span data-ttu-id="d8d31-141">v + p1-p2</span><span class="sxs-lookup"><span data-stu-id="d8d31-141">v + p1 - p2</span></span>               | <span data-ttu-id="d8d31-142">用於加法和減法。</span><span class="sxs-lookup"><span data-stu-id="d8d31-142">Used for addition and subtraction.</span></span>                                             |
| <span data-ttu-id="d8d31-143">product</span><span class="sxs-lookup"><span data-stu-id="d8d31-143">product</span></span>   | <span data-ttu-id="d8d31-144">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-144">3</span></span>      | <span data-ttu-id="d8d31-145">輪</span><span class="sxs-lookup"><span data-stu-id="d8d31-145">rounds</span></span> | <span data-ttu-id="d8d31-146">v \* p1/p2</span><span class="sxs-lookup"><span data-stu-id="d8d31-146">v \* p1 / p2</span></span>              | <span data-ttu-id="d8d31-147">用於乘法和除法。</span><span class="sxs-lookup"><span data-stu-id="d8d31-147">Used for multiplication and division.</span></span>                                          |
| <span data-ttu-id="d8d31-148">mid</span><span class="sxs-lookup"><span data-stu-id="d8d31-148">mid</span></span>       | <span data-ttu-id="d8d31-149">2</span><span class="sxs-lookup"><span data-stu-id="d8d31-149">2</span></span>      | <span data-ttu-id="d8d31-150"> (c) </span><span class="sxs-lookup"><span data-stu-id="d8d31-150">(c)</span></span>    | <span data-ttu-id="d8d31-151"> (v + p1) /2</span><span class="sxs-lookup"><span data-stu-id="d8d31-151">(v + p1)/ 2</span></span>               | <span data-ttu-id="d8d31-152">平均。</span><span class="sxs-lookup"><span data-stu-id="d8d31-152">Average.</span></span>                                                                       |
| <span data-ttu-id="d8d31-153">abs</span><span class="sxs-lookup"><span data-stu-id="d8d31-153">abs</span></span>       | <span data-ttu-id="d8d31-154">1</span><span class="sxs-lookup"><span data-stu-id="d8d31-154">1</span></span>      | <span data-ttu-id="d8d31-155">是</span><span class="sxs-lookup"><span data-stu-id="d8d31-155">yes</span></span>    | <span data-ttu-id="d8d31-156">abs (v) </span><span class="sxs-lookup"><span data-stu-id="d8d31-156">abs(v)</span></span>                    | <span data-ttu-id="d8d31-157">絕對值。</span><span class="sxs-lookup"><span data-stu-id="d8d31-157">Absolute value.</span></span>                                                                |
| <span data-ttu-id="d8d31-158">分鐘</span><span class="sxs-lookup"><span data-stu-id="d8d31-158">min</span></span>       | <span data-ttu-id="d8d31-159">2</span><span class="sxs-lookup"><span data-stu-id="d8d31-159">2</span></span>      | <span data-ttu-id="d8d31-160">是</span><span class="sxs-lookup"><span data-stu-id="d8d31-160">yes</span></span>    | <span data-ttu-id="d8d31-161">min (v，p1) </span><span class="sxs-lookup"><span data-stu-id="d8d31-161">min(v,p1)</span></span>                 | <span data-ttu-id="d8d31-162">V 和 p1 的較小值。</span><span class="sxs-lookup"><span data-stu-id="d8d31-162">The lesser value of v and p1.</span></span>                                                  |
| <span data-ttu-id="d8d31-163">max</span><span class="sxs-lookup"><span data-stu-id="d8d31-163">max</span></span>       | <span data-ttu-id="d8d31-164">2</span><span class="sxs-lookup"><span data-stu-id="d8d31-164">2</span></span>      | <span data-ttu-id="d8d31-165">是</span><span class="sxs-lookup"><span data-stu-id="d8d31-165">yes</span></span>    | <span data-ttu-id="d8d31-166">max (v，p1) </span><span class="sxs-lookup"><span data-stu-id="d8d31-166">max(v,p1)</span></span>                 | <span data-ttu-id="d8d31-167">V 和 p1 的值愈大。</span><span class="sxs-lookup"><span data-stu-id="d8d31-167">The greater value of v and p1.</span></span>                                                 |
| <span data-ttu-id="d8d31-168">if</span><span class="sxs-lookup"><span data-stu-id="d8d31-168">if</span></span>        | <span data-ttu-id="d8d31-169">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-169">3</span></span>      | <span data-ttu-id="d8d31-170">是</span><span class="sxs-lookup"><span data-stu-id="d8d31-170">yes</span></span>    | <span data-ttu-id="d8d31-171">v > 0？</span><span class="sxs-lookup"><span data-stu-id="d8d31-171">v > 0 ?</span></span> <span data-ttu-id="d8d31-172">p1： p2</span><span class="sxs-lookup"><span data-stu-id="d8d31-172">p1 : p2</span></span>        | <span data-ttu-id="d8d31-173">條件式測試。</span><span class="sxs-lookup"><span data-stu-id="d8d31-173">Conditional testing.</span></span>                                                           |
| <span data-ttu-id="d8d31-174">mod</span><span class="sxs-lookup"><span data-stu-id="d8d31-174">mod</span></span>       | <span data-ttu-id="d8d31-175">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-175">3</span></span>      | <span data-ttu-id="d8d31-176">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-176">no</span></span>     | <span data-ttu-id="d8d31-177">sqrt (v ^ 2 + p1 ^ 2 + p2 ^ 2) </span><span class="sxs-lookup"><span data-stu-id="d8d31-177">sqrt(v^2 + p1^2 + p2^2)</span></span>   | <span data-ttu-id="d8d31-178">模數值。</span><span class="sxs-lookup"><span data-stu-id="d8d31-178">Modulus value.</span></span>                                                                 |
| <span data-ttu-id="d8d31-179">atan2</span><span class="sxs-lookup"><span data-stu-id="d8d31-179">atan2</span></span>     | <span data-ttu-id="d8d31-180">2</span><span class="sxs-lookup"><span data-stu-id="d8d31-180">2</span></span>      | <span data-ttu-id="d8d31-181">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-181">no</span></span>     | <span data-ttu-id="d8d31-182">atan2 (p1，v) </span><span class="sxs-lookup"><span data-stu-id="d8d31-182">atan2(p1,v)</span></span>               | <span data-ttu-id="d8d31-183">以度為單位 \* 2 ^ 16 (fd 單位) 的極值。</span><span class="sxs-lookup"><span data-stu-id="d8d31-183">Polar value in degrees \* 2^16 (fd units).</span></span>                                     |
| <span data-ttu-id="d8d31-184">sin</span><span class="sxs-lookup"><span data-stu-id="d8d31-184">sin</span></span>       | <span data-ttu-id="d8d31-185">2</span><span class="sxs-lookup"><span data-stu-id="d8d31-185">2</span></span>      | <span data-ttu-id="d8d31-186">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-186">no</span></span>     | <span data-ttu-id="d8d31-187">v \* sin (p1) </span><span class="sxs-lookup"><span data-stu-id="d8d31-187">v \* sin(p1)</span></span>              | <span data-ttu-id="d8d31-188">Sin，以度數 \* 2 ^ 16 (fd [單位](msdn-online-vml-units.md) ) 的引數。</span><span class="sxs-lookup"><span data-stu-id="d8d31-188">Sin, argument in degrees \* 2^16 (fd [units](msdn-online-vml-units.md) ).</span></span>     |
| <span data-ttu-id="d8d31-189">cos</span><span class="sxs-lookup"><span data-stu-id="d8d31-189">cos</span></span>       | <span data-ttu-id="d8d31-190">2</span><span class="sxs-lookup"><span data-stu-id="d8d31-190">2</span></span>      | <span data-ttu-id="d8d31-191">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-191">no</span></span>     | <span data-ttu-id="d8d31-192">v \* cos (p1) </span><span class="sxs-lookup"><span data-stu-id="d8d31-192">v \* cos(p1)</span></span>              | <span data-ttu-id="d8d31-193">Cos，以度數 \* 2 ^ 16 (fd [單位](msdn-online-vml-units.md) ) 的引數。</span><span class="sxs-lookup"><span data-stu-id="d8d31-193">Cos, argument in degrees \* 2^16 (fd [units](msdn-online-vml-units.md) ).</span></span>     |
| <span data-ttu-id="d8d31-194">cosatan2</span><span class="sxs-lookup"><span data-stu-id="d8d31-194">cosatan2</span></span>  | <span data-ttu-id="d8d31-195">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-195">3</span></span>      | <span data-ttu-id="d8d31-196">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-196">no</span></span>     | <span data-ttu-id="d8d31-197">v \* cos (atan2 (p2，p1) ) </span><span class="sxs-lookup"><span data-stu-id="d8d31-197">v \* cos(atan2(p2,p1))</span></span>    | <span data-ttu-id="d8d31-198">在中繼計算中保留完整的精確度。</span><span class="sxs-lookup"><span data-stu-id="d8d31-198">Preserves full accuracy in intermediate calculation.</span></span>                           |
| <span data-ttu-id="d8d31-199">sinatan2</span><span class="sxs-lookup"><span data-stu-id="d8d31-199">sinatan2</span></span>  | <span data-ttu-id="d8d31-200">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-200">3</span></span>      | <span data-ttu-id="d8d31-201">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-201">no</span></span>     | <span data-ttu-id="d8d31-202">v \* sin (atan2 (p2，p1) ) </span><span class="sxs-lookup"><span data-stu-id="d8d31-202">v \* sin(atan2(p2,p1))</span></span>    | <span data-ttu-id="d8d31-203">在中繼計算中保留完整的精確度。</span><span class="sxs-lookup"><span data-stu-id="d8d31-203">Preserves full accuracy in intermediate calculation.</span></span>                           |
| <span data-ttu-id="d8d31-204">sqrt</span><span class="sxs-lookup"><span data-stu-id="d8d31-204">sqrt</span></span>      | <span data-ttu-id="d8d31-205">1</span><span class="sxs-lookup"><span data-stu-id="d8d31-205">1</span></span>      | <span data-ttu-id="d8d31-206">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-206">no</span></span>     | <span data-ttu-id="d8d31-207">sqrt (v) </span><span class="sxs-lookup"><span data-stu-id="d8d31-207">sqrt(v)</span></span>                   | <span data-ttu-id="d8d31-208">結果為正向下四捨五入。</span><span class="sxs-lookup"><span data-stu-id="d8d31-208">Result is positive and rounds down.</span></span>                                            |
| <span data-ttu-id="d8d31-209">sumangle</span><span class="sxs-lookup"><span data-stu-id="d8d31-209">sumangle</span></span>  | <span data-ttu-id="d8d31-210">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-210">3</span></span>      | <span data-ttu-id="d8d31-211">是</span><span class="sxs-lookup"><span data-stu-id="d8d31-211">yes</span></span>    | <span data-ttu-id="d8d31-212">v + p1 \* 2 ^ 16 + p2 \* 2 ^ 16</span><span class="sxs-lookup"><span data-stu-id="d8d31-212">v + p1 \* 2^16 + p2\*2^16</span></span> | <span data-ttu-id="d8d31-213">依 2 ^ 16 比例的 vp1 和 p2 是度。</span><span class="sxs-lookup"><span data-stu-id="d8d31-213">v scaled by 2^16; p1 and p2 are degrees.</span></span><br/>                            |
| <span data-ttu-id="d8d31-214">ellipse</span><span class="sxs-lookup"><span data-stu-id="d8d31-214">ellipse</span></span>   | <span data-ttu-id="d8d31-215">3</span><span class="sxs-lookup"><span data-stu-id="d8d31-215">3</span></span>      | <span data-ttu-id="d8d31-216">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-216">no</span></span>     | <span data-ttu-id="d8d31-217">p2 \* sqrt (1- (v/p1) ^ 2) </span><span class="sxs-lookup"><span data-stu-id="d8d31-217">p2 \* sqrt(1-(v/p1)^2)</span></span>    | <span data-ttu-id="d8d31-218">橢圓。</span><span class="sxs-lookup"><span data-stu-id="d8d31-218">Ellipse.</span></span>                                                                       |
| <span data-ttu-id="d8d31-219">tan</span><span class="sxs-lookup"><span data-stu-id="d8d31-219">tan</span></span>       | <span data-ttu-id="d8d31-220">2</span><span class="sxs-lookup"><span data-stu-id="d8d31-220">2</span></span>      | <span data-ttu-id="d8d31-221">不可以</span><span class="sxs-lookup"><span data-stu-id="d8d31-221">no</span></span>     | <span data-ttu-id="d8d31-222">v \* tan (p1) </span><span class="sxs-lookup"><span data-stu-id="d8d31-222">v \* tan(p1)</span></span>              | <span data-ttu-id="d8d31-223">正切函數，以度數 \* 2 ^ 16 (fd [單位](msdn-online-vml-units.md) ) 的引數。</span><span class="sxs-lookup"><span data-stu-id="d8d31-223">Tangent, argument in degrees \* 2^16 (fd [units](msdn-online-vml-units.md) ).</span></span> |



 

<span data-ttu-id="d8d31-224">請注意，方程式只包含作業和數位;會省略數學符號。</span><span class="sxs-lookup"><span data-stu-id="d8d31-224">Note that the equation only consists of operations and numbers; mathematical symbols are omitted.</span></span> <span data-ttu-id="d8d31-225">例如，方程式</span><span class="sxs-lookup"><span data-stu-id="d8d31-225">For example, the equation</span></span>

<span data-ttu-id="d8d31-226">eqn = "sum 5 9 3"</span><span class="sxs-lookup"><span data-stu-id="d8d31-226">eqn="sum 5 9 3"</span></span>

<span data-ttu-id="d8d31-227">會產生對等的</span><span class="sxs-lookup"><span data-stu-id="d8d31-227">would yield the equivalent of</span></span>

<span data-ttu-id="d8d31-228">5 + 9-3</span><span class="sxs-lookup"><span data-stu-id="d8d31-228">5 + 9 - 3</span></span>

<span data-ttu-id="d8d31-229">傳回的值為11。</span><span class="sxs-lookup"><span data-stu-id="d8d31-229">for the returned value of 11.</span></span> <span data-ttu-id="d8d31-230">如果遺漏了運算元，就不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="d8d31-230">If operands are missing, the value is not used.</span></span> <span data-ttu-id="d8d31-231">例如，</span><span class="sxs-lookup"><span data-stu-id="d8d31-231">For example,</span></span>

<span data-ttu-id="d8d31-232">eqn = "sum 5 9"</span><span class="sxs-lookup"><span data-stu-id="d8d31-232">eqn="sum 5 9"</span></span>

<span data-ttu-id="d8d31-233">會產生對等的</span><span class="sxs-lookup"><span data-stu-id="d8d31-233">would yield the equivalent of</span></span>

<span data-ttu-id="d8d31-234">5 + 9</span><span class="sxs-lookup"><span data-stu-id="d8d31-234">5 + 9</span></span>

<span data-ttu-id="d8d31-235">而且會忽略遺漏的運算元。</span><span class="sxs-lookup"><span data-stu-id="d8d31-235">and would ignore the missing operand.</span></span>

<span data-ttu-id="d8d31-236">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="d8d31-236">*VML Standard Attribute*</span></span>

<span data-ttu-id="d8d31-237">**範例**</span><span class="sxs-lookup"><span data-stu-id="d8d31-237">**Example**</span></span>

<span data-ttu-id="d8d31-238">下列公式產生的結果為 6 (兩個數字的總和除以 2) ，如果這是第一個公式，則可以使用符號 "" 來抓取 @0 。</span><span class="sxs-lookup"><span data-stu-id="d8d31-238">The following formula would yield a result of 6 (the sum of both numbers divided by 2), which, if this were the first formula, could be retrieved by the symbol "@0".</span></span>


```HTML
    <v:f eqn="mid 5 7"/>
```



 

