---
title: 基本的 VML 類型
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 將依賴 VML 的網頁和應用程式遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Vector Markup Language (VML) 、基本類型
- VML (Vector Markup Language) ，基本類型
- 向量圖形，基本的 VML 類型
- Vector Markup Language (VML) ，類型
- VML (Vector Markup Language) 、類型
- 向量圖形、VML 類型
- 基本的 VML 類型
- 布林類型
- 分數類型
- 縱座標類型
- 長度類型
- 量數值型別
- 角度類型
- 色彩類型
- 字型類型
- 點陣圖類型
- 向量類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104563761"
---
# <a name="basic-vml-types"></a><span data-ttu-id="533c3-121">基本的 VML 類型</span><span class="sxs-lookup"><span data-stu-id="533c3-121">Basic VML Types</span></span>

<span data-ttu-id="533c3-122">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="533c3-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="533c3-123">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="533c3-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="533c3-124">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="533c3-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="533c3-125">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="533c3-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="533c3-126">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="533c3-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="533c3-127">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="533c3-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="533c3-128">**Contents**</span><span class="sxs-lookup"><span data-stu-id="533c3-128">**Contents**</span></span>

-   [<span data-ttu-id="533c3-129">簡介</span><span class="sxs-lookup"><span data-stu-id="533c3-129">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="533c3-130">boolean</span><span class="sxs-lookup"><span data-stu-id="533c3-130">boolean</span></span>](#boolean)
-   [<span data-ttu-id="533c3-131">分數</span><span class="sxs-lookup"><span data-stu-id="533c3-131">fraction</span></span>](#fraction)
-   [<span data-ttu-id="533c3-132">座標</span><span class="sxs-lookup"><span data-stu-id="533c3-132">ordinate</span></span>](#ordinate)
-   <span data-ttu-id="533c3-133">[length](#length) (長度)</span><span class="sxs-lookup"><span data-stu-id="533c3-133">[length](#length)</span></span>
    -   [<span data-ttu-id="533c3-134">替代標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-134">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="533c3-135">措施</span><span class="sxs-lookup"><span data-stu-id="533c3-135">measure</span></span>](#measure)
    -   [<span data-ttu-id="533c3-136">替代標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-136">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="533c3-137">角度</span><span class="sxs-lookup"><span data-stu-id="533c3-137">angle</span></span>](#angle)
    -   [<span data-ttu-id="533c3-138">替代標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-138">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="533c3-139">color</span><span class="sxs-lookup"><span data-stu-id="533c3-139">color</span></span>](#color)
    -   [<span data-ttu-id="533c3-140">色彩單位</span><span class="sxs-lookup"><span data-stu-id="533c3-140">Color units</span></span>](#color-units)
    -   [<span data-ttu-id="533c3-141">HTML 色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-141">HTML colors</span></span>](#html-colors)
    -   [<span data-ttu-id="533c3-142">配置色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-142">Scheme colors</span></span>](#scheme-colors)
    -   [<span data-ttu-id="533c3-143">系統色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-143">System colors</span></span>](#system-colors)
    -   [<span data-ttu-id="533c3-144">純虛擬色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-144">Pure colors</span></span>](#pure-colors)
    -   [<span data-ttu-id="533c3-145">色彩調整</span><span class="sxs-lookup"><span data-stu-id="533c3-145">Color adjustments</span></span>](#color-adjustments)
-   [<span data-ttu-id="533c3-146">字體</span><span class="sxs-lookup"><span data-stu-id="533c3-146">font</span></span>](#font)
-   [<span data-ttu-id="533c3-147">點陣圖</span><span class="sxs-lookup"><span data-stu-id="533c3-147">bitmap</span></span>](#bitmap)
    -   [<span data-ttu-id="533c3-148">圖片檔案格式</span><span class="sxs-lookup"><span data-stu-id="533c3-148">Picture file formats</span></span>](#picture-file-formats)
-   [<span data-ttu-id="533c3-149">向量</span><span class="sxs-lookup"><span data-stu-id="533c3-149">vector</span></span>](#vector)

## <a name="introduction"></a><span data-ttu-id="533c3-150">簡介</span><span class="sxs-lookup"><span data-stu-id="533c3-150">Introduction</span></span>

<span data-ttu-id="533c3-151">這份提案使用下表所列的少數基本類型。</span><span class="sxs-lookup"><span data-stu-id="533c3-151">This proposal uses a small number of basic types, listed in the table below.</span></span>



| <span data-ttu-id="533c3-152">類型</span><span class="sxs-lookup"><span data-stu-id="533c3-152">Type</span></span>                  | <span data-ttu-id="533c3-153">元素</span><span class="sxs-lookup"><span data-stu-id="533c3-153">Element</span></span>           | <span data-ttu-id="533c3-154">基本標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-154">Fundamental Representation</span></span> | <span data-ttu-id="533c3-155">Description</span><span class="sxs-lookup"><span data-stu-id="533c3-155">Description</span></span>                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="533c3-156">boolean</span><span class="sxs-lookup"><span data-stu-id="533c3-156">boolean</span></span>](#boolean)   |                   | <span data-ttu-id="533c3-157">1位</span><span class="sxs-lookup"><span data-stu-id="533c3-157">1 bit</span></span>                      | <span data-ttu-id="533c3-158">布林值： true 或 false。</span><span class="sxs-lookup"><span data-stu-id="533c3-158">A boolean value: true or false.</span></span>                                                                      |
| [<span data-ttu-id="533c3-159">分數</span><span class="sxs-lookup"><span data-stu-id="533c3-159">fraction</span></span>](#fraction) |                   | <span data-ttu-id="533c3-160">數位 2 6</span><span class="sxs-lookup"><span data-stu-id="533c3-160">number 2 6</span></span>                 | <span data-ttu-id="533c3-161">數值，以 2 6 () 65536 進行調整，並儲存為帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="533c3-161">A numeric value, scaled by 2 6 (65536) and stored as a signed integer.</span></span>                               |
| [<span data-ttu-id="533c3-162">座標</span><span class="sxs-lookup"><span data-stu-id="533c3-162">ordinate</span></span>](#ordinate) |                   | <span data-ttu-id="533c3-163">30位整數加正負號</span><span class="sxs-lookup"><span data-stu-id="533c3-163">30-bit integer plus sign</span></span>   | <span data-ttu-id="533c3-164">座標的一部分 (例如，在 ) 的路徑中，是由 coord 所定義的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-164">Part of a coordinate (e.g., in a path ), the values defined by coord.</span></span>                                |
| <span data-ttu-id="533c3-165">[length](#length) (長度)</span><span class="sxs-lookup"><span data-stu-id="533c3-165">[length](#length)</span></span>     |                   | [<span data-ttu-id="533c3-166">動 車組</span><span class="sxs-lookup"><span data-stu-id="533c3-166">EMU</span></span>](#length)             | <span data-ttu-id="533c3-167">實體長度，例如線條的寬度或字型的大小。</span><span class="sxs-lookup"><span data-stu-id="533c3-167">A physical length, such as the width of a line or the size of a font.</span></span>                                |
| [<span data-ttu-id="533c3-168">措施</span><span class="sxs-lookup"><span data-stu-id="533c3-168">measure</span></span>](#measure)   |                   | <span data-ttu-id="533c3-169">EMU 或數位 2 6</span><span class="sxs-lookup"><span data-stu-id="533c3-169">EMU or number 2 6</span></span>          | <span data-ttu-id="533c3-170">實體長度，包括數個裝置圖元或部分其他數量的部分。</span><span class="sxs-lookup"><span data-stu-id="533c3-170">Either a physical length, including a number of device pixels, or a fraction of some other quantity.</span></span> |
| [<span data-ttu-id="533c3-171">角度</span><span class="sxs-lookup"><span data-stu-id="533c3-171">angle</span></span>](#angle)       |                   | <span data-ttu-id="533c3-172">度數 2 6</span><span class="sxs-lookup"><span data-stu-id="533c3-172">degrees 2 6</span></span>                | <span data-ttu-id="533c3-173">角度;正面是順時針。</span><span class="sxs-lookup"><span data-stu-id="533c3-173">An angle; positive is clockwise.</span></span>                                                                     |
| [<span data-ttu-id="533c3-174">color</span><span class="sxs-lookup"><span data-stu-id="533c3-174">color</span></span>](#color)       | [<span data-ttu-id="533c3-175">c</span><span class="sxs-lookup"><span data-stu-id="533c3-175">c</span></span>](#color)       | <span data-ttu-id="533c3-176">複雜</span><span class="sxs-lookup"><span data-stu-id="533c3-176">complex</span></span>                    | <span data-ttu-id="533c3-177">允許衍生色彩的元素。</span><span class="sxs-lookup"><span data-stu-id="533c3-177">An element that allows a color to be derived.</span></span>                                                        |
| [<span data-ttu-id="533c3-178">字體</span><span class="sxs-lookup"><span data-stu-id="533c3-178">font</span></span>](#font)         | [<span data-ttu-id="533c3-179">字體</span><span class="sxs-lookup"><span data-stu-id="533c3-179">font</span></span>](#font)     | <span data-ttu-id="533c3-180">複雜</span><span class="sxs-lookup"><span data-stu-id="533c3-180">complex</span></span>                    | <span data-ttu-id="533c3-181">字型的描述。</span><span class="sxs-lookup"><span data-stu-id="533c3-181">A description of a font.</span></span>                                                                             |
| [<span data-ttu-id="533c3-182">點陣圖</span><span class="sxs-lookup"><span data-stu-id="533c3-182">bitmap</span></span>](#bitmap)     | [<span data-ttu-id="533c3-183">點陣圖</span><span class="sxs-lookup"><span data-stu-id="533c3-183">bitmap</span></span>](#bitmap) | <span data-ttu-id="533c3-184">href</span><span class="sxs-lookup"><span data-stu-id="533c3-184">href</span></span>                       | <span data-ttu-id="533c3-185">外部圖片檔案的參考。</span><span class="sxs-lookup"><span data-stu-id="533c3-185">A reference to an external picture file.</span></span>                                                             |
| [<span data-ttu-id="533c3-186">向量</span><span class="sxs-lookup"><span data-stu-id="533c3-186">vector</span></span>](#vector)     | [<span data-ttu-id="533c3-187">V</span><span class="sxs-lookup"><span data-stu-id="533c3-187">v</span></span>](#vector)      | <span data-ttu-id="533c3-188">複雜</span><span class="sxs-lookup"><span data-stu-id="533c3-188">complex</span></span>                    | <span data-ttu-id="533c3-189">向量路徑的描述</span><span class="sxs-lookup"><span data-stu-id="533c3-189">A description of a vector path</span></span>                                                                       |



 

<span data-ttu-id="533c3-190">「基本標記法」是最高精確度的標記法，此表示提案需要符合規範的實施才能維持;如果執行不能將資料表示為所需的精確度，資料將會遺失。</span><span class="sxs-lookup"><span data-stu-id="533c3-190">The "fundamental representation" is the highest precision representation that the proposal requires a conforming implementation to maintain; data will be lost if the implementation is not able to represent the data to the precision required.</span></span> <span data-ttu-id="533c3-191">色彩、字型和向量類型會對應至本身具有結構的專案，而不是基本類型;不過，將這些專案視為此提案內的方式很方便。</span><span class="sxs-lookup"><span data-stu-id="533c3-191">The color, font, and vector types correspond to elements which themselves have structure -- in a sense, they are not basic types; however, it is convenient to treat them as such within this proposal.</span></span>

<span data-ttu-id="533c3-192">每個非複雜的基本類型都有相同名稱的相關聯元素。</span><span class="sxs-lookup"><span data-stu-id="533c3-192">Each non-complex basic type has an associated element of the same name.</span></span> <span data-ttu-id="533c3-193">這些專案名稱會保留，而且可能無法用於延伸模組中的任何其他用途，即使在 onview = "skip" 擴充專案中使用也是如此。</span><span class="sxs-lookup"><span data-stu-id="533c3-193">These element names are reserved and may not be used for any other purpose within extensions, even if the use is within an onview="skip" extension element.</span></span> <span data-ttu-id="533c3-194">基於這個原因，您可能會遇到未知 XML 的執行，以提供未知 XML 的有效內部儲存，只要這些值是以 "type" 元素括住。</span><span class="sxs-lookup"><span data-stu-id="533c3-194">Because of this, it is possible for an implementation that encounters unknown XML to provide efficient internal storage of the unknown XML as long as the values are enclosed in the "type" elements.</span></span>


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



<span data-ttu-id="533c3-195">在上述的第一個範例中，字串 "1.578" 必須儲存為字元序列 (而不知道它是否為字串或數位) ;在第二個範例中，分數元素表示內容為數字，因此可以轉換成高精確度分數標記法。</span><span class="sxs-lookup"><span data-stu-id="533c3-195">In the first example above, the string "1.578" must be stored as a sequence of characters (the implementation does not know whether it is a string or a number); in the second example, the fraction element indicates that the content is a number, thus it may be converted to the high precision fraction representation.</span></span>

<span data-ttu-id="533c3-196">複雜類型 (包括點陣圖) 有相關聯的專案名稱，可用來分隔值。</span><span class="sxs-lookup"><span data-stu-id="533c3-196">Complex types (including bitmap) have associated element names that are used to delimit the value.</span></span> <span data-ttu-id="533c3-197">這會藉由確保更複雜的剖析工作與唯一的專案標記建立關聯，以簡化剖析。</span><span class="sxs-lookup"><span data-stu-id="533c3-197">This simplifies parsing by ensuring that the more complex parsing tasks are associated with unique element tags.</span></span>

<span data-ttu-id="533c3-198">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-198">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="boolean"></a><span data-ttu-id="533c3-199">boolean</span><span class="sxs-lookup"><span data-stu-id="533c3-199">boolean</span></span>


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="533c3-200">布林值會表示為指出旗標狀態的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="533c3-200">A boolean value is represented as a keyword indicating the state of the flag.</span></span> <span data-ttu-id="533c3-201">已定義下列關鍵字。</span><span class="sxs-lookup"><span data-stu-id="533c3-201">The following keywords are defined.</span></span>



| <span data-ttu-id="533c3-202">True 的值</span><span class="sxs-lookup"><span data-stu-id="533c3-202">Value for true</span></span> | <span data-ttu-id="533c3-203">False 的值</span><span class="sxs-lookup"><span data-stu-id="533c3-203">Value for false</span></span> |
|----------------|-----------------|
| <span data-ttu-id="533c3-204">true</span><span class="sxs-lookup"><span data-stu-id="533c3-204">true</span></span>           | <span data-ttu-id="533c3-205">false</span><span class="sxs-lookup"><span data-stu-id="533c3-205">false</span></span>           |
| <span data-ttu-id="533c3-206">是</span><span class="sxs-lookup"><span data-stu-id="533c3-206">yes</span></span>            | <span data-ttu-id="533c3-207">不可以</span><span class="sxs-lookup"><span data-stu-id="533c3-207">no</span></span>              |
| <span data-ttu-id="533c3-208">on</span><span class="sxs-lookup"><span data-stu-id="533c3-208">on</span></span>             | <span data-ttu-id="533c3-209">關</span><span class="sxs-lookup"><span data-stu-id="533c3-209">off</span></span>             |
| <span data-ttu-id="533c3-210">t</span><span class="sxs-lookup"><span data-stu-id="533c3-210">t</span></span>              | <span data-ttu-id="533c3-211">f</span><span class="sxs-lookup"><span data-stu-id="533c3-211">f</span></span>               |
| <span data-ttu-id="533c3-212">1</span><span class="sxs-lookup"><span data-stu-id="533c3-212">1</span></span>              | <span data-ttu-id="533c3-213">0</span><span class="sxs-lookup"><span data-stu-id="533c3-213">0</span></span>               |



 

<span data-ttu-id="533c3-214">執行可能會寫入任何值，而且必須辨識所有的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-214">An implementation may write any value and must recognize all values.</span></span> <span data-ttu-id="533c3-215">可以自由地將值從一個表示變更為另一個標記法。</span><span class="sxs-lookup"><span data-stu-id="533c3-215">An implementation is free to change values from one representation to another.</span></span>

<span data-ttu-id="533c3-216">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-216">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="fraction"></a><span data-ttu-id="533c3-217">分數</span><span class="sxs-lookup"><span data-stu-id="533c3-217">fraction</span></span>


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="533c3-218">所有數值 (也就是，在此提案中) 的量值量值，可以藉由 2 6 (65536) 進行調整來儲存為整數。</span><span class="sxs-lookup"><span data-stu-id="533c3-218">All numeric values (i.e., values of dimensionless quantities) within this proposal can be stored as integers by scaling them by 2  6 (65536).</span></span> <span data-ttu-id="533c3-219">您可以使用此格式來指定數位，尾碼為 f 或不含尾碼的十進位數。</span><span class="sxs-lookup"><span data-stu-id="533c3-219">A number may be given either in this form, with the suffix f or as a decimal number with no suffix.</span></span> <span data-ttu-id="533c3-220">因此，下列假設元素代表相同的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-220">Thus, the following hypothetical elements represent the same value.</span></span>


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



<span data-ttu-id="533c3-221">具有 f 尾碼的數量必須是整數;不允許使用小數數位。</span><span class="sxs-lookup"><span data-stu-id="533c3-221">A quantity with the f suffix must be a whole number; fractional numbers are not permitted.</span></span> <span data-ttu-id="533c3-222">結果整數必須可表示為32位的補數帶正負號的數位;因此，表示的有效範圍是 32768 (事實上，小於32768且大於或等於-32768。 ) </span><span class="sxs-lookup"><span data-stu-id="533c3-222">The resultant integer must be representable as a 32-bit 2's complement signed number; thus, the effective range of the representation is  32768 (in fact, less than 32768 and greater than or equal to -32768.)</span></span>

<span data-ttu-id="533c3-223">需要符合規範的實值，才能保留以 f 值表示的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-223">A conforming implementation is required to preserve values that are expressed as f values.</span></span> <span data-ttu-id="533c3-224">以十進位數表示的值可能會轉換成 f 值，並以該方式儲存。</span><span class="sxs-lookup"><span data-stu-id="533c3-224">Values represented as decimal numbers may be converted to an f value and stored that way.</span></span> <span data-ttu-id="533c3-225">允許應用程式在任何適當的單位中記錄內部產生的值;不過，從現有檔中讀取的值必須維持為完整原始有效位數，或必須轉換為 f 值。</span><span class="sxs-lookup"><span data-stu-id="533c3-225">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an f value.</span></span>

<span data-ttu-id="533c3-226">如果執行無法這麼做，就必須警告使用者資料可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="533c3-226">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="533c3-227"> (在第一次遇到外部產生的資料時，可以接受發出這類警告一次的情況。 ) </span><span class="sxs-lookup"><span data-stu-id="533c3-227">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="533c3-228">當 decimal 值轉換為 f 格式時，實值可能會使用任何算術舍入模式;不過，整數必須完全轉換成 f 格式。</span><span class="sxs-lookup"><span data-stu-id="533c3-228">When a decimal value is converted into f format, the implementation may use any arithmetic rounding mode; however, a whole number must be converted to the f format exactly.</span></span> <span data-ttu-id="533c3-229">建議將實作為轉換成減號無限大，且轉換一律是精確的。</span><span class="sxs-lookup"><span data-stu-id="533c3-229">It is recommended that implementations convert by rounding to minus infinity and that the convertion always be exact.</span></span>

<span data-ttu-id="533c3-230">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-230">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="ordinate"></a><span data-ttu-id="533c3-231">座標</span><span class="sxs-lookup"><span data-stu-id="533c3-231">ordinate</span></span>


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="533c3-232">Coord 所建立的座標系統單位是某些名義型別，稱為「縱座標」。</span><span class="sxs-lookup"><span data-stu-id="533c3-232">The units of the coordinate system established by coord are of some nominal type, which is referred to as ordinate.</span></span> <span data-ttu-id="533c3-233">這是長度的量值，但只會與 coord 所建立的矩形相對應。</span><span class="sxs-lookup"><span data-stu-id="533c3-233">This is a measure of length, but it is only used in relation to the rectangle that coord establishes.</span></span> <span data-ttu-id="533c3-234">任何類型為縱座標的值都會以 coord 的 *w* 和 *h* 值，以及用來在輸出裝置上建立實際度量的結果比例進行縮放。</span><span class="sxs-lookup"><span data-stu-id="533c3-234">Any value of type ordinate will be scaled by the *w* and *h* values of the coord and the resulting ratio used to establish a real measurement on the output device.</span></span>

<span data-ttu-id="533c3-235">符合規範的執行必須能夠處理最多30個位的座標值，以及正負號 (例如31位帶正負號的整數，而不是32位帶正負號的整數) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-235">A conforming implementation must be able to handle ordinate values of up to 30 bits plus sign (i.e., a 31-bit signed integer, not a 32-bit signed integer).</span></span> <span data-ttu-id="533c3-236">不過，建議您嘗試針對具有大約16位精確度的路徑和類似元素產生座標。</span><span class="sxs-lookup"><span data-stu-id="533c3-236">It is recommended, however, that implementations attempt to produce coordinates for path and similar elements that have about 16 bits of precision.</span></span> <span data-ttu-id="533c3-237">這可將不符合規範的實作為下溢或溢位的機率降到最低。</span><span class="sxs-lookup"><span data-stu-id="533c3-237">This will minimize the chance of either underflow or overflow in a non-conforming implementation.</span></span>

<span data-ttu-id="533c3-238">座標值一律為整數。</span><span class="sxs-lookup"><span data-stu-id="533c3-238">ordinate values are always integral.</span></span> <span data-ttu-id="533c3-239">小點可能不會出現在類型座標的值中。</span><span class="sxs-lookup"><span data-stu-id="533c3-239">A decimal point may not appear in a value of type ordinate.</span></span> <span data-ttu-id="533c3-240">不可以將任何單位規範附加至縱座標類型的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-240">No unit specifiers may be appended to values of type ordinate.</span></span>

<span data-ttu-id="533c3-241">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-241">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="length"></a><span data-ttu-id="533c3-242">長度</span><span class="sxs-lookup"><span data-stu-id="533c3-242">length</span></span>


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="533c3-243">長度是真實世界的測量，有時也是裝置圖元的度量。</span><span class="sxs-lookup"><span data-stu-id="533c3-243">A length is a real-world measurement or, sometimes, a measurement in device pixels.</span></span> <span data-ttu-id="533c3-244">建議您避免使用裝置圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-244">It is recommended that implementations avoid the use of device pixels (px).</span></span>

<span data-ttu-id="533c3-245">所有標準 [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) 單位限定詞的長度都是允許的。</span><span class="sxs-lookup"><span data-stu-id="533c3-245">All the standard [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) unit qualifiers are permitted on a length.</span></span> <span data-ttu-id="533c3-246">此外，也可以使用限定詞的 emu。</span><span class="sxs-lookup"><span data-stu-id="533c3-246">In addition, the qualifier emu may be used.</span></span> <span data-ttu-id="533c3-247">此辨識符號指的是單位（EMU (英文計量單位) --這是在電腦圖形中廣泛使用之測量數量的常見分母。</span><span class="sxs-lookup"><span data-stu-id="533c3-247">This qualifier refers to a unit -- the EMU (English Metric Unit) -- which is a common denominator of the measurement quantities in widespread use in computer graphics.</span></span> <span data-ttu-id="533c3-248">EMU 為 <sup>英寸</sup> /914400，也就是每英寸有914400個 EMU。</span><span class="sxs-lookup"><span data-stu-id="533c3-248">The EMU is <sup>inch</sup> / 914400, i.e., there are 914400 EMU per inch.</span></span> <span data-ttu-id="533c3-249">下表列出少數常見單位中的 EMUs 數目。</span><span class="sxs-lookup"><span data-stu-id="533c3-249">The following table lists the number of EMUs in a small number of commonly encountered units.</span></span>



| <span data-ttu-id="533c3-250">EMUs 數目</span><span class="sxs-lookup"><span data-stu-id="533c3-250">Number of EMUs</span></span> | <span data-ttu-id="533c3-251">每英寸的數目</span><span class="sxs-lookup"><span data-stu-id="533c3-251">Number per Inch</span></span> | <span data-ttu-id="533c3-252">每個毫米的數位</span><span class="sxs-lookup"><span data-stu-id="533c3-252">Number per Millimeter</span></span> | <span data-ttu-id="533c3-253">Description</span><span class="sxs-lookup"><span data-stu-id="533c3-253">Description</span></span>             |
|----------------|-----------------|-----------------------|-------------------------|
| <span data-ttu-id="533c3-254">360</span><span class="sxs-lookup"><span data-stu-id="533c3-254">360</span></span>            |                 | <span data-ttu-id="533c3-255">0.01</span><span class="sxs-lookup"><span data-stu-id="533c3-255">0.01</span></span>                  | <span data-ttu-id="533c3-256">Win32 HIMETRIC</span><span class="sxs-lookup"><span data-stu-id="533c3-256">Win32 HIMETRIC</span></span>          |
| <span data-ttu-id="533c3-257">12700</span><span class="sxs-lookup"><span data-stu-id="533c3-257">12700</span></span>          | <span data-ttu-id="533c3-258">72</span><span class="sxs-lookup"><span data-stu-id="533c3-258">72</span></span>              |                       | <span data-ttu-id="533c3-259">時候</span><span class="sxs-lookup"><span data-stu-id="533c3-259">"point"</span></span>                 |
| <span data-ttu-id="533c3-260">635</span><span class="sxs-lookup"><span data-stu-id="533c3-260">635</span></span>            | <span data-ttu-id="533c3-261">1440</span><span class="sxs-lookup"><span data-stu-id="533c3-261">1440</span></span>            |                       | <span data-ttu-id="533c3-262">Win32 TWIP</span><span class="sxs-lookup"><span data-stu-id="533c3-262">Win32 TWIP</span></span>              |
| <span data-ttu-id="533c3-263">762</span><span class="sxs-lookup"><span data-stu-id="533c3-263">762</span></span>            | <span data-ttu-id="533c3-264">1200</span><span class="sxs-lookup"><span data-stu-id="533c3-264">1200</span></span>            |                       | <span data-ttu-id="533c3-265">高解析度印表機</span><span class="sxs-lookup"><span data-stu-id="533c3-265">High-resolution printer</span></span> |



 

<span data-ttu-id="533c3-266">不允許 EMUs 的小數數位。</span><span class="sxs-lookup"><span data-stu-id="533c3-266">Fractional numbers of EMUs are not permitted.</span></span> <span data-ttu-id="533c3-267">任何量測都必須以32位帶正負號的整數 EMUs 形式來表示，這會將量測的大小限制為2348英寸--大約59計量或65碼。</span><span class="sxs-lookup"><span data-stu-id="533c3-267">Any measurement must be representable as a 32-bit signed integral number of EMUs -- this limits the magnitude of a measurement to 2348 inches -- about 59 meters or 65 yards.</span></span> <span data-ttu-id="533c3-268">因為量測一律會參考名義上螢幕或頁面大小輸出裝置上的轉譯大小，它們一律會在此範圍內。</span><span class="sxs-lookup"><span data-stu-id="533c3-268">Because the measurements always refer to the size of a rendering on a nominally screen- or page-sized output device, they will always be within this range.</span></span>

<span data-ttu-id="533c3-269">不過，請注意，此標記法不適合實際的度量，而且會記錄在 (例如記錄路徑的真實世界大小) 必須使用其他標記法。</span><span class="sxs-lookup"><span data-stu-id="533c3-269">Notice, however, that the representation is inappropriate for real-world measurements and that where these are recorded (for example, to record the real-world size of a path) some other representation must be used.</span></span>

<span data-ttu-id="533c3-270">需要符合規範的實值，才能保留精確 EMUs 數目的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-270">A conforming implementation is required to preserve values that are exact numbers of EMUs.</span></span> <span data-ttu-id="533c3-271">以任何其他方式表示的值可能會轉換成 EMU 值，並以該方式儲存。</span><span class="sxs-lookup"><span data-stu-id="533c3-271">Values represented in any other way may be converted to an EMU value and stored that way.</span></span> <span data-ttu-id="533c3-272">允許應用程式在任何適當的單位中記錄內部產生的值;不過，從現有檔中讀取的值必須維持為完整原始有效位數，或必須轉換成 EMU 值。</span><span class="sxs-lookup"><span data-stu-id="533c3-272">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an EMU value.</span></span>

<span data-ttu-id="533c3-273">如果執行無法這麼做，就必須警告使用者資料可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="533c3-273">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="533c3-274"> (在第一次遇到外部產生的資料時，可以接受發出這類警告一次的情況。 ) </span><span class="sxs-lookup"><span data-stu-id="533c3-274">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="533c3-275">實際上，在此提案中，實體長度是用於相對較少的度量。</span><span class="sxs-lookup"><span data-stu-id="533c3-275">In practice, physical lengths are used for relatively few measurements in this proposal.</span></span> <span data-ttu-id="533c3-276">通常最重要的資料是路徑資料，而這會以個別圖形為基礎，以 coord 的方式在定義的座標系統中編碼。</span><span class="sxs-lookup"><span data-stu-id="533c3-276">The data which is normally most important is the path data and this is encoded in the coordinate system defined, on a per-shape basis, by coord.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="533c3-277">替代標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-277">Alternative representations</span></span>

<span data-ttu-id="533c3-278">HTML 的標準長度表示是由 [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) 所定義。</span><span class="sxs-lookup"><span data-stu-id="533c3-278">The standard length representations of HTML are defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span></span> <span data-ttu-id="533c3-279">相對單位（圖元除外）在此提案中使用長度的內容中沒有意義，而且不得使用。</span><span class="sxs-lookup"><span data-stu-id="533c3-279">Relative units, with the exception of the pixel, are not meaningful in the context within which lengths are used in this proposal and must not be used.</span></span> <span data-ttu-id="533c3-280">如果檔記錄了預期的 (目標) 圖元大小，這會將圖元的轉譯定義為 EMU;否則，應該使用 [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) 所定義的 90 DPI 預設值。</span><span class="sxs-lookup"><span data-stu-id="533c3-280">If the document records the intended (target) pixel size, this defines the translation of pixels into EMU; otherwise, the default of 90 dpi defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) should be used.</span></span>

<span data-ttu-id="533c3-281">除了 emu 以外，任何值都可以指定為小數小數。</span><span class="sxs-lookup"><span data-stu-id="533c3-281">With the exception of emu, any value may be given as a decimal fraction.</span></span> <span data-ttu-id="533c3-282">當 decimal 值轉換成 EMU 時，實值可能會使用任何算術舍入模式。</span><span class="sxs-lookup"><span data-stu-id="533c3-282">When a decimal value is converted to EMU, the implementation may use any arithmetic rounding mode.</span></span> <span data-ttu-id="533c3-283"> (製作應用程式保證特定結果的唯一方式，就是以 emu 來指定。 ) </span><span class="sxs-lookup"><span data-stu-id="533c3-283">(The only way for an authoring application to guarantee a particular result is to specify it in emu.)</span></span>

<span data-ttu-id="533c3-284">如果長度值未指定任何單位規範，則實作為必須假設為 emu。</span><span class="sxs-lookup"><span data-stu-id="533c3-284">If no unit specifier is given in a length value, the implementation must assume emu.</span></span>

<span data-ttu-id="533c3-285">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-285">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="measure"></a><span data-ttu-id="533c3-286">measure</span><span class="sxs-lookup"><span data-stu-id="533c3-286">measure</span></span>


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="533c3-287">量值是可能是 [長度](#length) 或 [分數](#fraction)的數量。</span><span class="sxs-lookup"><span data-stu-id="533c3-287">A measure is a quantity that may be either a [length](#length) or a [fraction](#fraction).</span></span> <span data-ttu-id="533c3-288">這與 HTML 和 CSS 長度的測量非常類似，在許多情況下，可能是實體量測或某些其他數量的百分比。</span><span class="sxs-lookup"><span data-stu-id="533c3-288">This closely resembles the HTML and CSS length measurements, which can, in many cases, either be physical measurements or percentages of some other quantity.</span></span> <span data-ttu-id="533c3-289">如果未指定任何單位規範，則值必須假設為小數小數 (因此，此行為會從分數繼承，而不是從長度繼承。 ) </span><span class="sxs-lookup"><span data-stu-id="533c3-289">If no unit specifier is given, the value must be assumed to be a decimal fraction (thus, this behavior is inherited from fraction, not from length.)</span></span>

<span data-ttu-id="533c3-290">不同于長度，圖元值具有內容定義的意義，因此轉換成 emu 通常是不正確的。</span><span class="sxs-lookup"><span data-stu-id="533c3-290">Unlike length, a pixel value has a context-defined meaning, so conversion to emu is normally inappropriate.</span></span> <span data-ttu-id="533c3-291">有三種可能的基本標記法必須維持 (，也就是其中一個標記法無法轉換成另一個，而不會遺失任何資訊) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-291">There are three possible fundamental representations that the implementation must maintain (i.e., one representation cannot be converted into another without loss of information).</span></span>

1.  <span data-ttu-id="533c3-292">小數值應以 [小數](#fraction) 格式進行維護， ("f" 值) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-292">A fractional value should be maintained in the [fraction](#fraction) format (an " f " value).</span></span>
2.  <span data-ttu-id="533c3-293">實體長度應以 EMU 維護。</span><span class="sxs-lookup"><span data-stu-id="533c3-293">A physical length should be maintained in EMU.</span></span>
3.  <span data-ttu-id="533c3-294">圖元值應該維持為整數的圖元數。</span><span class="sxs-lookup"><span data-stu-id="533c3-294">A pixel value should be maintained as a whole number of pixels.</span></span>

<span data-ttu-id="533c3-295">不允許小數的圖元數。</span><span class="sxs-lookup"><span data-stu-id="533c3-295">Fractional numbers of pixels are not permitted.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="533c3-296">替代標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-296">Alternative representations</span></span>

<span data-ttu-id="533c3-297">允許 [小數](#fraction) 和 [長度](#length) 的所有替代標記法。</span><span class="sxs-lookup"><span data-stu-id="533c3-297">All the alternate representations of both [fraction](#fraction) and [length](#length) are permitted.</span></span>

<span data-ttu-id="533c3-298">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-298">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="angle"></a><span data-ttu-id="533c3-299">角度</span><span class="sxs-lookup"><span data-stu-id="533c3-299">angle</span></span>


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="533c3-300">角度的基本標記法是由 2 6 (65536) 所乘以的程度，並儲存為整數。</span><span class="sxs-lookup"><span data-stu-id="533c3-300">The fundamental representation of an angle is a number of degrees multipled by 2 6 (65536) and stored as an integer.</span></span> <span data-ttu-id="533c3-301">因為座標空間會反轉 (正 y 軸會) 關閉，所以順時針角度是正面的。</span><span class="sxs-lookup"><span data-stu-id="533c3-301">Because the coordinate space is inverted (positive y axis is down), a clockwise angle is positive.</span></span> <span data-ttu-id="533c3-302">需要符合規範的實，才能保留這類值的完整精確度。</span><span class="sxs-lookup"><span data-stu-id="533c3-302">A conforming implementation is required to preserve the full precision of such a value.</span></span>

<span data-ttu-id="533c3-303">您可以使用任何角度的範圍，並允許 normalise 角度 (例如-180 到 + 180 或0至 360 ) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-303">An implementation is permitted to use any range for angles and is permitted to normalise an angle (for example to -180  to +180  or 0 to 360 ).</span></span> <span data-ttu-id="533c3-304">執行不需要一致;不過，角度的整數標記法不能超過32位帶正負號整數的範圍。</span><span class="sxs-lookup"><span data-stu-id="533c3-304">Implementations are not required to be consistent; however, the integral representation of an angle must not exceed the range of a 32-bit signed integer.</span></span>

<span data-ttu-id="533c3-305">尾碼 fd 會用來識別此標記法的角度 (分數) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-305">The suffix fd is used to identify this representation of an angle (fractional degree).</span></span> <span data-ttu-id="533c3-306">請注意，這會從 f 尾碼分辨成維度分數，雖然可以使用相同的算術來支援它。</span><span class="sxs-lookup"><span data-stu-id="533c3-306">Notice that this is distinguished from the f suffix for a dimensionless fraction although identical arithmetic can be used to support it.</span></span> <span data-ttu-id="533c3-307">角度值的預設值為簡單度，也就是無比例的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-307">The default for an angular value is simple degrees, i.e., an unscaled value.</span></span> <span data-ttu-id="533c3-308">這也可能會使用後置字元 "" (角度符號) ;不過，使用這項功能取決於是否有適當的檔編碼--因此，後置字元度數也會定義為平均度數。</span><span class="sxs-lookup"><span data-stu-id="533c3-308">This may also be signalled with the suffix " " (the degree symbol); however, use of this depends on having a suitable document encoding -- consequently, the suffix deg is also defined to mean degrees.</span></span> <span data-ttu-id="533c3-309">一組完整的可能尾碼，如下所示。</span><span class="sxs-lookup"><span data-stu-id="533c3-309">The full set of possible suffices are as follows.</span></span>



| <span data-ttu-id="533c3-310">後置詞</span><span class="sxs-lookup"><span data-stu-id="533c3-310">Suffix</span></span>       | <span data-ttu-id="533c3-311">轉換因數</span><span class="sxs-lookup"><span data-stu-id="533c3-311">Conversion Factor</span></span> | <span data-ttu-id="533c3-312">註解</span><span class="sxs-lookup"><span data-stu-id="533c3-312">Comments</span></span>                               |
|--------------|-------------------|----------------------------------------|
| <span data-ttu-id="533c3-313">Fd</span><span class="sxs-lookup"><span data-stu-id="533c3-313">fd</span></span>           | <span data-ttu-id="533c3-314">1</span><span class="sxs-lookup"><span data-stu-id="533c3-314">1</span></span>                 | <span data-ttu-id="533c3-315">高精確度內部標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-315">High-precision internal representation</span></span> |
| <span data-ttu-id="533c3-316">無、度、</span><span class="sxs-lookup"><span data-stu-id="533c3-316">none, deg,</span></span>   | <span data-ttu-id="533c3-317">65536</span><span class="sxs-lookup"><span data-stu-id="533c3-317">65536</span></span>             | <span data-ttu-id="533c3-318">Degrees</span><span class="sxs-lookup"><span data-stu-id="533c3-318">Degrees</span></span>                                |
| <span data-ttu-id="533c3-319">rad</span><span class="sxs-lookup"><span data-stu-id="533c3-319">rad</span></span>          | <span data-ttu-id="533c3-320">65536pi/180</span><span class="sxs-lookup"><span data-stu-id="533c3-320">65536pi/180</span></span>       | <span data-ttu-id="533c3-321">Radians</span><span class="sxs-lookup"><span data-stu-id="533c3-321">Radians</span></span>                                |



 

### <a name="alternative-representations"></a><span data-ttu-id="533c3-322">替代標記法</span><span class="sxs-lookup"><span data-stu-id="533c3-322">Alternative representations</span></span>

<span data-ttu-id="533c3-323">縮放轉換的不連續是45的奇數倍數。</span><span class="sxs-lookup"><span data-stu-id="533c3-323">The scaling transformation has discontinuities at odd multiples of 45 .</span></span> <span data-ttu-id="533c3-324">因此，將任何不精確的數量轉換成妥善定義非常重要。</span><span class="sxs-lookup"><span data-stu-id="533c3-324">It is, therefore, extremely important for the conversion of any inexact quantity to be well defined.</span></span> <span data-ttu-id="533c3-325">基於這個理由，轉換的算術定義為舍入減去無限大。</span><span class="sxs-lookup"><span data-stu-id="533c3-325">For this reason, the arithmetic of conversion is defined to round towards minus infinity.</span></span>

<span data-ttu-id="533c3-326">因為這在某些實作為中可能很困難或無法保證，所以使用下列內容會定義為層級3功能：</span><span class="sxs-lookup"><span data-stu-id="533c3-326">Because this may be difficult or impossible to guarantee in some implementations, the use of the following is defined to be a level 3 feature:</span></span>

1.  <span data-ttu-id="533c3-327">任何小數度值。</span><span class="sxs-lookup"><span data-stu-id="533c3-327">Any fractional degree value.</span></span>
2.  <span data-ttu-id="533c3-328">任何弧度值</span><span class="sxs-lookup"><span data-stu-id="533c3-328">Any radian value</span></span>

<span data-ttu-id="533c3-329">因此，值限定的 fd 和不合格的整數值或整數值的限定度，必須完全由符合層級0的實作為處理;其他值則不需要。</span><span class="sxs-lookup"><span data-stu-id="533c3-329">Thus, values qualified fd and unqualified integral values, or integral values qualified deg or   must be handled exactly by a conforming level 0 implementation; other values need not.</span></span> <span data-ttu-id="533c3-330">強烈建議任何實值都能處理從小數度值到已縮放 (fd) 度值的轉換。</span><span class="sxs-lookup"><span data-stu-id="533c3-330">It is strongly recommended that any implementation handle the conversion from a fractional degree value to a scaled (fd) degree value exactly.</span></span> <span data-ttu-id="533c3-331">這可以在沒有浮點支援的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="533c3-331">This can be done without floating point support.</span></span>

<span data-ttu-id="533c3-332">更嚴格的轉換需求區分 fd 與 f。</span><span class="sxs-lookup"><span data-stu-id="533c3-332">The more exacting requirements for conversion distinguish fd from f.</span></span>

<span data-ttu-id="533c3-333">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-333">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="color"></a><span data-ttu-id="533c3-334">color</span><span class="sxs-lookup"><span data-stu-id="533c3-334">color</span></span>


```HTML
c
<!element c  %color;>
```



<span data-ttu-id="533c3-335">色彩是新式電腦圖形中不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="533c3-335">Colors are an essential part of modern computer graphics.</span></span> <span data-ttu-id="533c3-336">提案會使用已建立的方法來指定固定色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-336">The proposal uses the established methods of specifying fixed colors.</span></span> <span data-ttu-id="533c3-337">不過，圖表中的色彩很少是簡單的靜態色彩;它們通常衍生自圖表中的其他元素。</span><span class="sxs-lookup"><span data-stu-id="533c3-337">However, colors in diagrams are rarely simple static colors; they are often derived from other elements in the diagram.</span></span> <span data-ttu-id="533c3-338">大部分的資訊都是應用程式特定的，因此，這個提案提供兩種非常基本的機制來指定這類行為：</span><span class="sxs-lookup"><span data-stu-id="533c3-338">Much of this information is very application-specific, so this proposal provides two very basic mechanisms to specify such behavior:</span></span>

1.  <span data-ttu-id="533c3-339">色彩可能會衍生自相同形狀中的另一種色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-339">A color may be derived from another color in the same shape.</span></span>
2.  <span data-ttu-id="533c3-340">定義少量的算數運算來衍生或修改色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-340">A small number of arithmetic operations are defined for deriving, or modifying, a color.</span></span>

<span data-ttu-id="533c3-341">原型圖形機制會藉由允許從可繼承的色彩來定義原型來補充此項。</span><span class="sxs-lookup"><span data-stu-id="533c3-341">The prototype shape mechanism supplements this by allow prototypes to be defined from which colors can be inherited.</span></span>


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



<span data-ttu-id="533c3-342">色彩值是 [CSS1 色彩定義](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) 的超集合。</span><span class="sxs-lookup"><span data-stu-id="533c3-342">A color value is a superset of the [CSS1 color definition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span> <span data-ttu-id="533c3-343">擴充功能可讓您從圖形內的其他色彩，或從使用 CSS1 所定義的整體色彩配置來判斷 RGB 色彩值。</span><span class="sxs-lookup"><span data-stu-id="533c3-343">The extensions allow the RGB color value to be determined from other colors within the shape or from an overall color scheme defined using CSS1.</span></span>

<span data-ttu-id="533c3-344">如果元素的值定義為色彩，則元素的 *內容* 會透過對應 RGB 色彩上的算數運算選擇性地修改的單一色彩標記，來定義色彩值。</span><span class="sxs-lookup"><span data-stu-id="533c3-344">If the value of an element is defined to be a color, the *content* of an element defines the color value by means of a single color token optionally modified by an arithmetic operation on the corresponding RGB color.</span></span>

<span data-ttu-id="533c3-345">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-345">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-units"></a><span data-ttu-id="533c3-346">色彩單位</span><span class="sxs-lookup"><span data-stu-id="533c3-346">Color units</span></span>

<span data-ttu-id="533c3-347">一組完整的色彩標記來自各種來源： HTML、CSS1 和此提案。</span><span class="sxs-lookup"><span data-stu-id="533c3-347">The full set of color tokens come from a variety of sources: HTML, CSS1, and this proposal.</span></span> <span data-ttu-id="533c3-348">它們定義如下：使用 [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) 中的標記法或針對 XML 連結所定義的 XPointer 標記法。</span><span class="sxs-lookup"><span data-stu-id="533c3-348">They are defined as follows using notation from [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) or the XPointer notation defined for XML linking.</span></span>

<span data-ttu-id="533c3-349">在 XPointer 定義中，位置來源是包含色彩值的元素，而運算式則是指圖形的整個元素集，就像任何基底原型元素已經與圖形合併一樣。</span><span class="sxs-lookup"><span data-stu-id="533c3-349">In the XPointer definitions, the location source is the element containing the color value, and the expression refers to the whole element set of the shape as though any base prototype elements had been merged with the shape.</span></span> <span data-ttu-id="533c3-350">當對應的專案不存在時，就會使用該元素的預設值。</span><span class="sxs-lookup"><span data-stu-id="533c3-350">When the corresponding element does not exist, the default value for that element is used in its place.</span></span>



| <span data-ttu-id="533c3-351">Color</span><span class="sxs-lookup"><span data-stu-id="533c3-351">Color</span></span>            | <span data-ttu-id="533c3-352">定義</span><span class="sxs-lookup"><span data-stu-id="533c3-352">Definition</span></span>                                                                                                  | <span data-ttu-id="533c3-353">層級</span><span class="sxs-lookup"><span data-stu-id="533c3-353">Level</span></span> | <span data-ttu-id="533c3-354">描述</span><span class="sxs-lookup"><span data-stu-id="533c3-354">Description</span></span>                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533c3-355">NAME</span><span class="sxs-lookup"><span data-stu-id="533c3-355">name</span></span>             | <span data-ttu-id="533c3-356">請參閱下方</span><span class="sxs-lookup"><span data-stu-id="533c3-356">See below</span></span>                                                                                                   | <span data-ttu-id="533c3-357">0</span><span class="sxs-lookup"><span data-stu-id="533c3-357">0</span></span>     | <span data-ttu-id="533c3-358">HTML 色彩名稱，如下表所列。</span><span class="sxs-lookup"><span data-stu-id="533c3-358">HTML color name, as listed in the table below.</span></span>                                                                                                                            |
| <span data-ttu-id="533c3-359">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="533c3-359">\#rr'gg'bb'</span></span>      | <span data-ttu-id="533c3-360">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="533c3-360">\#rr'gg'bb'</span></span>                                                                                                 | <span data-ttu-id="533c3-361">0</span><span class="sxs-lookup"><span data-stu-id="533c3-361">0</span></span>     | <span data-ttu-id="533c3-362">標準 CSS1/sRGB 色彩表示使用範圍0到255中的值，每個都使用2個十六進位數位表示。</span><span class="sxs-lookup"><span data-stu-id="533c3-362">Standard CSS1/sRGB color representation using values in the range 0..255 represented using 2 hexadecimal digits each.</span></span>                                                     |
| <span data-ttu-id="533c3-363">\#Rgb</span><span class="sxs-lookup"><span data-stu-id="533c3-363">\#rgb</span></span>            | <span data-ttu-id="533c3-364">\#rrggbb</span><span class="sxs-lookup"><span data-stu-id="533c3-364">\#rrggbb</span></span>                                                                                                    | <span data-ttu-id="533c3-365">1</span><span class="sxs-lookup"><span data-stu-id="533c3-365">1</span></span>     | <span data-ttu-id="533c3-366">縮短 CSS1 表單只包含三個十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="533c3-366">Shortened CSS1 form with only three hexadecimal digits.</span></span>                                                                                                                   |
| <span data-ttu-id="533c3-367">rgb (r、g、b) </span><span class="sxs-lookup"><span data-stu-id="533c3-367">rgb(r,g,b)</span></span>       | <span data-ttu-id="533c3-368">\# (r)  (g)  (b) </span><span class="sxs-lookup"><span data-stu-id="533c3-368">\#(r)(g)(b)</span></span>                                                                                                 | <span data-ttu-id="533c3-369">1</span><span class="sxs-lookup"><span data-stu-id="533c3-369">1</span></span>     | <span data-ttu-id="533c3-370">CSS1 rgb 表單;rgb 值的元素會依照 [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) 中的定義進行轉換。</span><span class="sxs-lookup"><span data-stu-id="533c3-370">CSS1 rgb form; the elements of the rgb value are converted as defined in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span>                                      |
| <span data-ttu-id="533c3-371">fill</span><span class="sxs-lookup"><span data-stu-id="533c3-371">fill</span></span>             | <span data-ttu-id="533c3-372">上階 (1，圖形) </span><span class="sxs-lookup"><span data-stu-id="533c3-372">ancestor(1,shape)</span></span><br/> <span data-ttu-id="533c3-373">子 (1，填滿) </span><span class="sxs-lookup"><span data-stu-id="533c3-373">child(1, fill)</span></span><br/> <span data-ttu-id="533c3-374">子 (1、色彩) </span><span class="sxs-lookup"><span data-stu-id="533c3-374">child(1, color)</span></span><br/>                           | <span data-ttu-id="533c3-375">1</span><span class="sxs-lookup"><span data-stu-id="533c3-375">1</span></span>     | <span data-ttu-id="533c3-376">圖形的前景填滿色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-376">The foreground fill color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="533c3-377">fillBack</span><span class="sxs-lookup"><span data-stu-id="533c3-377">fillBack</span></span>         | <span data-ttu-id="533c3-378">上階 (1，圖形) </span><span class="sxs-lookup"><span data-stu-id="533c3-378">ancestor(1,shape)</span></span><br/> <span data-ttu-id="533c3-379">子 (1，填滿) </span><span class="sxs-lookup"><span data-stu-id="533c3-379">child(1, fill)</span></span><br/> <span data-ttu-id="533c3-380">子 (1，back) </span><span class="sxs-lookup"><span data-stu-id="533c3-380">child(1, back)</span></span><br/> <span data-ttu-id="533c3-381">子 (1、色彩) </span><span class="sxs-lookup"><span data-stu-id="533c3-381">child(1, color)</span></span><br/> | <span data-ttu-id="533c3-382">1</span><span class="sxs-lookup"><span data-stu-id="533c3-382">1</span></span>     | <span data-ttu-id="533c3-383">圖形填滿的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-383">The background color of the shape fill.</span></span>                                                                                                                                   |
| <span data-ttu-id="533c3-384">line</span><span class="sxs-lookup"><span data-stu-id="533c3-384">line</span></span>             | <span data-ttu-id="533c3-385">上階 (1，圖形) </span><span class="sxs-lookup"><span data-stu-id="533c3-385">ancestor(1,shape)</span></span><br/> <span data-ttu-id="533c3-386">子 (1，行) </span><span class="sxs-lookup"><span data-stu-id="533c3-386">child(1, line)</span></span><br/> <span data-ttu-id="533c3-387">子 (1、色彩) </span><span class="sxs-lookup"><span data-stu-id="533c3-387">child(1, color)</span></span><br/>                           | <span data-ttu-id="533c3-388">1</span><span class="sxs-lookup"><span data-stu-id="533c3-388">1</span></span>     | <span data-ttu-id="533c3-389">圖形的前景線條色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-389">The foreground line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="533c3-390">lineBack</span><span class="sxs-lookup"><span data-stu-id="533c3-390">lineBack</span></span>         | <span data-ttu-id="533c3-391">上階 (1，圖形) </span><span class="sxs-lookup"><span data-stu-id="533c3-391">ancestor(1,shape)</span></span><br/> <span data-ttu-id="533c3-392">子 (1，行) </span><span class="sxs-lookup"><span data-stu-id="533c3-392">child(1, line)</span></span><br/> <span data-ttu-id="533c3-393">子 (1，back) </span><span class="sxs-lookup"><span data-stu-id="533c3-393">child(1,back)</span></span> <br/> <span data-ttu-id="533c3-394">子 (1、色彩) </span><span class="sxs-lookup"><span data-stu-id="533c3-394">child(1, color)</span></span><br/> | <span data-ttu-id="533c3-395">1</span><span class="sxs-lookup"><span data-stu-id="533c3-395">1</span></span>     | <span data-ttu-id="533c3-396">圖形的背景線條色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-396">The background line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="533c3-397">lineOrFill</span><span class="sxs-lookup"><span data-stu-id="533c3-397">lineOrFill</span></span>       | <span data-ttu-id="533c3-398">行，填滿</span><span class="sxs-lookup"><span data-stu-id="533c3-398">line, fill</span></span>                                                                                                  | <span data-ttu-id="533c3-399">1</span><span class="sxs-lookup"><span data-stu-id="533c3-399">1</span></span>     | <span data-ttu-id="533c3-400">如果沒有預設值，則為行值，否則為填滿值。</span><span class="sxs-lookup"><span data-stu-id="533c3-400">The line value if not defaulted, otherwise the fill value.</span></span> <span data-ttu-id="533c3-401">這會有效地傳回圖形邊緣的色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-401">This effectively returns the color that is at the edge of the shape.</span></span>                                           |
| <span data-ttu-id="533c3-402">fillThenLine</span><span class="sxs-lookup"><span data-stu-id="533c3-402">fillThenLine</span></span>     | <span data-ttu-id="533c3-403">填滿、行</span><span class="sxs-lookup"><span data-stu-id="533c3-403">fill, line</span></span>                                                                                                  | <span data-ttu-id="533c3-404">1</span><span class="sxs-lookup"><span data-stu-id="533c3-404">1</span></span>     | <span data-ttu-id="533c3-405">如果沒有預設值，則為填滿值，否則為行值。</span><span class="sxs-lookup"><span data-stu-id="533c3-405">The fill value if not defaulted, otherwise the line value.</span></span> <span data-ttu-id="533c3-406">這會有效地傳回主要形狀色彩 (如果圖形未填滿，則結果將會是線條色彩) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-406">This effectively returns the main shape color (if the shape is unfilled, the result will be the line color).</span></span>   |
| <span data-ttu-id="533c3-407">shadow</span><span class="sxs-lookup"><span data-stu-id="533c3-407">shadow</span></span>           | <span data-ttu-id="533c3-408">上階 (1，圖形) </span><span class="sxs-lookup"><span data-stu-id="533c3-408">ancestor(1,shape)</span></span><br/> <span data-ttu-id="533c3-409">子 (1、陰影) </span><span class="sxs-lookup"><span data-stu-id="533c3-409">child(1, shadow)</span></span><br/> <span data-ttu-id="533c3-410">子 (1、色彩) </span><span class="sxs-lookup"><span data-stu-id="533c3-410">child(1, color)</span></span><br/>                         | <span data-ttu-id="533c3-411">2</span><span class="sxs-lookup"><span data-stu-id="533c3-411">2</span></span>     | <span data-ttu-id="533c3-412">陰影的色彩 (這是) 的層級2功能。</span><span class="sxs-lookup"><span data-stu-id="533c3-412">The color of the shadow (this is a level 2 feature).</span></span>                                                                                                                      |
| <span data-ttu-id="533c3-413">scheme</span><span class="sxs-lookup"><span data-stu-id="533c3-413">scheme</span></span>           | <span data-ttu-id="533c3-414">請參閱下方</span><span class="sxs-lookup"><span data-stu-id="533c3-414">See below</span></span>                                                                                                   | <span data-ttu-id="533c3-415">1</span><span class="sxs-lookup"><span data-stu-id="533c3-415">1</span></span>     | <span data-ttu-id="533c3-416">從為檔定義的配置中的配置色彩;請參閱下文。</span><span class="sxs-lookup"><span data-stu-id="533c3-416">A scheme color from the scheme defined for the document; see below.</span></span>                                                                                                       |
| <span data-ttu-id="533c3-417">配置 (*索引*) </span><span class="sxs-lookup"><span data-stu-id="533c3-417">scheme(*index*)</span></span>  | <span data-ttu-id="533c3-418">請參閱下方</span><span class="sxs-lookup"><span data-stu-id="533c3-418">See below</span></span>                                                                                                   | <span data-ttu-id="533c3-419">1</span><span class="sxs-lookup"><span data-stu-id="533c3-419">1</span></span>     | <span data-ttu-id="533c3-420">配置色彩 *索引*，從0開始;請參閱下文。</span><span class="sxs-lookup"><span data-stu-id="533c3-420">Scheme color *index*, starting from 0; see below.</span></span>                                                                                                                         |
| <span data-ttu-id="533c3-421">this</span><span class="sxs-lookup"><span data-stu-id="533c3-421">this</span></span>             | <span data-ttu-id="533c3-422">暗示</span><span class="sxs-lookup"><span data-stu-id="533c3-422">Implied</span></span>                                                                                                     | <span data-ttu-id="533c3-423">2</span><span class="sxs-lookup"><span data-stu-id="533c3-423">2</span></span>     | <span data-ttu-id="533c3-424"> (填滿路徑或繪製) 的作業會以其他方式定義 (例如，做為點陣圖) ，而色彩則會指定對色彩的「修改」。</span><span class="sxs-lookup"><span data-stu-id="533c3-424">The operation (filling a path, or drawing it) is defined in some other way (for example, as a bitmap), and the color specifies a "modification" to the colors so implied.</span></span> |
| <span data-ttu-id="533c3-425"> (*索引*) 的調色板</span><span class="sxs-lookup"><span data-stu-id="533c3-425">palette(*index*)</span></span> | <span data-ttu-id="533c3-426">暗示</span><span class="sxs-lookup"><span data-stu-id="533c3-426">Implied</span></span>                                                                                                     | <span data-ttu-id="533c3-427">3</span><span class="sxs-lookup"><span data-stu-id="533c3-427">3</span></span>     | <span data-ttu-id="533c3-428">的行為方式與此相同，不同之處在于點陣圖色彩表中只會識別出一個專案。</span><span class="sxs-lookup"><span data-stu-id="533c3-428">Behaves in the same way as this, except that exactly one entry in a bitmap color table is identified.</span></span> <span data-ttu-id="533c3-429">只允許明確陳述的位置。</span><span class="sxs-lookup"><span data-stu-id="533c3-429">Permitted only where explicitly stated.</span></span>                             |
| <span data-ttu-id="533c3-430">無</span><span class="sxs-lookup"><span data-stu-id="533c3-430">none</span></span>             | \-                                                                                                          | <span data-ttu-id="533c3-431">2</span><span class="sxs-lookup"><span data-stu-id="533c3-431">2</span></span>     | <span data-ttu-id="533c3-432">指出沒有色彩;可以用來取消使用色彩的繪圖操作。</span><span class="sxs-lookup"><span data-stu-id="533c3-432">Indicates the absence of a color; may be used to cancel a drawing operation that uses the color.</span></span>                                                                          |
| <span data-ttu-id="533c3-433">系統</span><span class="sxs-lookup"><span data-stu-id="533c3-433">system</span></span>           | <span data-ttu-id="533c3-434">請參閱下方</span><span class="sxs-lookup"><span data-stu-id="533c3-434">See below</span></span>                                                                                                   | <span data-ttu-id="533c3-435">3</span><span class="sxs-lookup"><span data-stu-id="533c3-435">3</span></span>     | <span data-ttu-id="533c3-436">系統使用者介面所定義的色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-436">A color defined by the system user interface.</span></span>                                                                                                                             |



 

<span data-ttu-id="533c3-437">此色彩可讓色彩值指定以其他方式衍生之色彩的修改;尤其是，可以為點陣圖中的所有色彩指定單一作業。</span><span class="sxs-lookup"><span data-stu-id="533c3-437">The this color allows a color value to specify a modification to a color which is derived in some other way; in particular, a single operation may be specified for all the colors in a bitmap.</span></span> <span data-ttu-id="533c3-438">調色板 (*索引*) 色彩會識別調色板對應點陣圖中的特定專案。</span><span class="sxs-lookup"><span data-stu-id="533c3-438">The palette(*index*) color identifies a particular entry in a palette-mapped bitmap.</span></span> <span data-ttu-id="533c3-439">只有在記錄這類點陣圖中應視為透明的色彩資料表專案時，才會定義使用此專案。</span><span class="sxs-lookup"><span data-stu-id="533c3-439">Use of this is only defined for recording a color table entry that should be regarded as transparent in such a bitmap.</span></span>

<span data-ttu-id="533c3-440">色彩值的定義不能直接或間接參考本身。</span><span class="sxs-lookup"><span data-stu-id="533c3-440">The definition of a color value must not refer to itself, either directly or indirectly.</span></span> <span data-ttu-id="533c3-441">如果遇到這類定義，建議您將未定義的值視為黑色，而不是必要的。</span><span class="sxs-lookup"><span data-stu-id="533c3-441">If such a definition is encountered, it is recommended, but not required, that the implementation treat the undefined value as black.</span></span>

<span data-ttu-id="533c3-442">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-442">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="html-colors"></a><span data-ttu-id="533c3-443">HTML 色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-443">HTML colors</span></span>

<span data-ttu-id="533c3-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) 會定義下列十六個色彩名稱：</span><span class="sxs-lookup"><span data-stu-id="533c3-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) defines the following sixteen color names:</span></span>



<span data-ttu-id="533c3-445">色彩名稱和 sRGB 值</span><span class="sxs-lookup"><span data-stu-id="533c3-445">Color names and sRGB values</span></span>

![黑色色彩的範例。](images/black.gif)

<span data-ttu-id="533c3-447">黑色 = " \# 000000"</span><span class="sxs-lookup"><span data-stu-id="533c3-447">Black = "\#000000"</span></span>

![綠色色彩的範例。](images/green.gif)

<span data-ttu-id="533c3-449">綠 = " \# 008000"</span><span class="sxs-lookup"><span data-stu-id="533c3-449">Green = "\#008000"</span></span>

![銀級色彩範例。](images/silver.gif)

<span data-ttu-id="533c3-451">銀 = " \# C0C0C0"</span><span class="sxs-lookup"><span data-stu-id="533c3-451">Silver = "\#C0C0C0"</span></span>

![橙色色彩的範例。](images/lime.gif)

<span data-ttu-id="533c3-453">橙色 = " \# 00FF00"</span><span class="sxs-lookup"><span data-stu-id="533c3-453">Lime = "\#00FF00"</span></span>

![灰色色彩的範例。](images/gray.gif)

<span data-ttu-id="533c3-455">灰色 = " \# 808080"</span><span class="sxs-lookup"><span data-stu-id="533c3-455">Gray = "\#808080"</span></span>

![橄欖色的範例。](images/olive.gif)

<span data-ttu-id="533c3-457">橄欖色 = " \# 808000"</span><span class="sxs-lookup"><span data-stu-id="533c3-457">Olive = "\#808000"</span></span>

![白色色彩的範例。](images/white.gif)

<span data-ttu-id="533c3-459">白色 = " \# FFFFFF"</span><span class="sxs-lookup"><span data-stu-id="533c3-459">White = "\#FFFFFF"</span></span>

![Ywllow 色彩的範例。](images/yellow.gif)

<span data-ttu-id="533c3-461">黃色 = " \# ffff00 代表色彩"</span><span class="sxs-lookup"><span data-stu-id="533c3-461">Yellow = "\#FFFF00"</span></span>

![暗紫紅色色彩的範例。](images/maroon.gif)

<span data-ttu-id="533c3-463">暗紫紅色 = " \# 800000"</span><span class="sxs-lookup"><span data-stu-id="533c3-463">Maroon = "\#800000"</span></span>

![Navy 色彩的範例。](images/navy.gif)

<span data-ttu-id="533c3-465">Navy = " \# 000080"</span><span class="sxs-lookup"><span data-stu-id="533c3-465">Navy = "\#000080"</span></span>

![紅色色彩的範例。](images/red.gif)

<span data-ttu-id="533c3-467">Red = " \# FF0000"</span><span class="sxs-lookup"><span data-stu-id="533c3-467">Red = "\#FF0000"</span></span>

![藍色的範例。](images/blue.gif)

<span data-ttu-id="533c3-469">Blue = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="533c3-469">Blue = "\#0000FF"</span></span>

![紫色色彩的範例。](images/purple.gif)

<span data-ttu-id="533c3-471">紫色 = " \# 800080"</span><span class="sxs-lookup"><span data-stu-id="533c3-471">Purple = "\#800080"</span></span>

![藍綠色色彩的範例。](images/teal.gif)

<span data-ttu-id="533c3-473">青色 = " \# 008080"</span><span class="sxs-lookup"><span data-stu-id="533c3-473">Teal = "\#008080"</span></span>

![Fuchsia 色彩的範例。](images/fuchsia.gif)

<span data-ttu-id="533c3-475">Fuchsia = " \# FF00FF"</span><span class="sxs-lookup"><span data-stu-id="533c3-475">Fuchsia = "\#FF00FF"</span></span>

![綠色色彩的範例。](images/aqua.gif)

<span data-ttu-id="533c3-477">綠色 = " \# 00FFFF"</span><span class="sxs-lookup"><span data-stu-id="533c3-477">Aqua = "\#00FFFF"</span></span>



 

<span data-ttu-id="533c3-478">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-478">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="scheme-colors"></a><span data-ttu-id="533c3-479">配置色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-479">Scheme colors</span></span>

<span data-ttu-id="533c3-480">配置所參考的配置色彩是在檔層級定義，並使用名稱屬性為「主題色彩配置」的中繼標記。</span><span class="sxs-lookup"><span data-stu-id="533c3-480">The scheme colors referenced by scheme are defined at the document level using the meta tag with a name attribute of "Theme Color Scheme".</span></span>


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



<span data-ttu-id="533c3-481">此標記最多可定義八種配置色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-481">This tag allows up to eight scheme colors to be defined.</span></span> <span data-ttu-id="533c3-482">未定義的色彩應該預設為黑色。</span><span class="sxs-lookup"><span data-stu-id="533c3-482">Undefined colors should default to black.</span></span> <span data-ttu-id="533c3-483">配置色彩可讓您只需變更主題色彩配置內容，就能變更整個檔所用的色彩配置。</span><span class="sxs-lookup"><span data-stu-id="533c3-483">The scheme colors allow the color scheme used for a complete document to be changed just by altering the Theme Color Scheme contents.</span></span> <span data-ttu-id="533c3-484">為了確保從不同撰寫應用程式匯入的圖形會一致地使用配置色彩，會定義下列解釋。</span><span class="sxs-lookup"><span data-stu-id="533c3-484">To ensure that graphics imported from different authoring applications make consistent use of the scheme colors, the following interpretations are defined.</span></span> <span data-ttu-id="533c3-485">「使用方式」是目的的簡短描述，而「描述」資料行會提供其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="533c3-485">The "usage" is a short description of the purpose, and the "description" column provides additional details.</span></span>



| <span data-ttu-id="533c3-486">索引</span><span class="sxs-lookup"><span data-stu-id="533c3-486">Index</span></span> | <span data-ttu-id="533c3-487">名稱</span><span class="sxs-lookup"><span data-stu-id="533c3-487">Name</span></span>              | <span data-ttu-id="533c3-488">使用量</span><span class="sxs-lookup"><span data-stu-id="533c3-488">Usage</span></span>                         | <span data-ttu-id="533c3-489">描述</span><span class="sxs-lookup"><span data-stu-id="533c3-489">Description</span></span>                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533c3-490">0</span><span class="sxs-lookup"><span data-stu-id="533c3-490">0</span></span>     | <span data-ttu-id="533c3-491">配置。背景</span><span class="sxs-lookup"><span data-stu-id="533c3-491">scheme.background</span></span> | <span data-ttu-id="533c3-492">背景</span><span class="sxs-lookup"><span data-stu-id="533c3-492">Background</span></span>                    | <span data-ttu-id="533c3-493">用於圖形背景的色彩 (，通常是整個頁面) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-493">The color used for the background of a graphic (and, frequently, for the whole page).</span></span>                                    |
| <span data-ttu-id="533c3-494">1</span><span class="sxs-lookup"><span data-stu-id="533c3-494">1</span></span>     | <span data-ttu-id="533c3-495">配置。文字</span><span class="sxs-lookup"><span data-stu-id="533c3-495">scheme.text</span></span>       | <span data-ttu-id="533c3-496">文字和線條</span><span class="sxs-lookup"><span data-stu-id="533c3-496">Text and lines</span></span>                | <span data-ttu-id="533c3-497">附加至圖形和標準線條色彩的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-497">The color for text attached to a shape and the standard line color.</span></span>                                                      |
| <span data-ttu-id="533c3-498">2</span><span class="sxs-lookup"><span data-stu-id="533c3-498">2</span></span>     | <span data-ttu-id="533c3-499">配置：陰影</span><span class="sxs-lookup"><span data-stu-id="533c3-499">scheme.shadow</span></span>     | <span data-ttu-id="533c3-500">陰影</span><span class="sxs-lookup"><span data-stu-id="533c3-500">Shadows</span></span>                       | <span data-ttu-id="533c3-501">標準陰影色彩：通常用於圖形陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-501">Standard shadow color -- the color typically used for shape shadows.</span></span>                                                     |
| <span data-ttu-id="533c3-502">3</span><span class="sxs-lookup"><span data-stu-id="533c3-502">3</span></span>     | <span data-ttu-id="533c3-503">配置. 標題</span><span class="sxs-lookup"><span data-stu-id="533c3-503">scheme.title</span></span>      | <span data-ttu-id="533c3-504">標題文字</span><span class="sxs-lookup"><span data-stu-id="533c3-504">Title text</span></span>                    | <span data-ttu-id="533c3-505">用於標題或標題文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-505">The color to use for heading or title text.</span></span>                                                                              |
| <span data-ttu-id="533c3-506">4</span><span class="sxs-lookup"><span data-stu-id="533c3-506">4</span></span>     | <span data-ttu-id="533c3-507">配置：填滿</span><span class="sxs-lookup"><span data-stu-id="533c3-507">scheme.fill</span></span>       | <span data-ttu-id="533c3-508">充滿</span><span class="sxs-lookup"><span data-stu-id="533c3-508">Fills</span></span>                         | <span data-ttu-id="533c3-509">標準填滿色彩：通常用來填滿圖形的色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-509">Standard fill color -- the color typically used to fill shapes.</span></span>                                                          |
| <span data-ttu-id="533c3-510">5</span><span class="sxs-lookup"><span data-stu-id="533c3-510">5</span></span>     | <span data-ttu-id="533c3-511">配置：輔色</span><span class="sxs-lookup"><span data-stu-id="533c3-511">scheme.accent</span></span>     | <span data-ttu-id="533c3-512">口音</span><span class="sxs-lookup"><span data-stu-id="533c3-512">Accent</span></span>                        | <span data-ttu-id="533c3-513">一般「反白顯示」色彩，用來強調圖形的重要元素。</span><span class="sxs-lookup"><span data-stu-id="533c3-513">Normal "highlight" color used to emphasis an important element of a graphic.</span></span>                                             |
| <span data-ttu-id="533c3-514">6</span><span class="sxs-lookup"><span data-stu-id="533c3-514">6</span></span>     | <span data-ttu-id="533c3-515">配置：超連結</span><span class="sxs-lookup"><span data-stu-id="533c3-515">scheme.hyperlink</span></span>  | <span data-ttu-id="533c3-516">輔色和超連結</span><span class="sxs-lookup"><span data-stu-id="533c3-516">Accent and hyperlink</span></span>          | <span data-ttu-id="533c3-517">反白顯示用於超連結的色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-517">Highlight color used for hyperlinks.</span></span> <span data-ttu-id="533c3-518">可用於其他用途，其中的色彩代表其他資訊的連結。</span><span class="sxs-lookup"><span data-stu-id="533c3-518">May be used for other purposes where the color denotes a link to other information.</span></span> |
| <span data-ttu-id="533c3-519">7</span><span class="sxs-lookup"><span data-stu-id="533c3-519">7</span></span>     | <span data-ttu-id="533c3-520">配置。遵循</span><span class="sxs-lookup"><span data-stu-id="533c3-520">scheme.followed</span></span>   | <span data-ttu-id="533c3-521">輔色和後續的超連結</span><span class="sxs-lookup"><span data-stu-id="533c3-521">Accent and followed hyperlink</span></span> | <span data-ttu-id="533c3-522">醒目提示已跟隨超連結的色彩;也適用于「回溯」連結。</span><span class="sxs-lookup"><span data-stu-id="533c3-522">Highlight color for followed hyperlinks; also appropriate for "backwards" links.</span></span>                                         |



 

<span data-ttu-id="533c3-523">配置色彩可依名稱或索引來參考，因此配置. 填滿和配置 (4) 的色彩相同。</span><span class="sxs-lookup"><span data-stu-id="533c3-523">A scheme color may be referred to either by name or by index, thus scheme.fill and scheme(4) are the same color.</span></span>

<span data-ttu-id="533c3-524">如果未指定色彩，配置色彩不會參與預設配置。</span><span class="sxs-lookup"><span data-stu-id="533c3-524">Scheme colors do not participate in the defaulting scheme if a color is not specified.</span></span> <span data-ttu-id="533c3-525">無論配置色彩4的色彩為何，未指定的填滿色彩都必須被視為白色。</span><span class="sxs-lookup"><span data-stu-id="533c3-525">An unspecified fill color must always be interpreted as white, regardless of the color of scheme color 4.</span></span> <span data-ttu-id="533c3-526">"輔色" 色彩應該與背景 (0) 和填滿 (4) 色彩相同，且文字和標題文字色彩應該具有相同的屬性。</span><span class="sxs-lookup"><span data-stu-id="533c3-526">The "accent" colors should contrast with both the background (0) and the fill (4) colors, and text and title text colors should have the same property.</span></span> <span data-ttu-id="533c3-527">其中一個標準技巧是讓強調色彩和標準文字 uncolored (通常是黑色或白色) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-527">One standard technique is to make the accents colored and the standard text uncolored (typically black or white).</span></span>

<span data-ttu-id="533c3-528">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-528">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="system-colors"></a><span data-ttu-id="533c3-529">系統色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-529">System colors</span></span>

<span data-ttu-id="533c3-530">應用程式有時會根據圖形內的作業系統設定來記錄色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-530">Applications sometimes record colors based on operating system settings within graphics.</span></span> <span data-ttu-id="533c3-531">一般來說，這些都是暫時性的，不需要寫出;thesystemcolor 定義只是為了支援這個而存在。</span><span class="sxs-lookup"><span data-stu-id="533c3-531">Normally these are transient and need not be written out; thesystemcolor definitions exist solely to support this.</span></span> <span data-ttu-id="533c3-532">藉由在新的命名空間中定義適當的標籤，並在元素內容中插入適當的資訊來引入系統色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-532">A system color is introduced by defining an appropriate tag in a new namespace and inserting the appropriate information in the element content.</span></span>

<span data-ttu-id="533c3-533">本提案定義了這類標記，以便編碼 winuser .h 標頭檔中定義的 Windows 使用者介面色彩。</span><span class="sxs-lookup"><span data-stu-id="533c3-533">This proposal defines such a tag to encode the Windows user interface colors defined in the winuser.h header file.</span></span>


```HTML
win.color
<!element win.color #pcdata>
```



<span data-ttu-id="533c3-534">元素的內容是單一的整數，其中包含 winuser 中相關色彩定義的值。 \_</span><span class="sxs-lookup"><span data-stu-id="533c3-534">The content of the element is a single integer which contains the value of the relevant COLOR\_ define from winuser.h.</span></span> <span data-ttu-id="533c3-535">您可以針對任何系統或應用程式特定的色彩規格採用類似的技術。</span><span class="sxs-lookup"><span data-stu-id="533c3-535">A similar technique can be adopted for any system- or application-specific color specification.</span></span> <span data-ttu-id="533c3-536">強烈建議您只針對回溯相容性使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="533c3-536">It is strongly recommended that this feature be used only for backward compatibility.</span></span>

<span data-ttu-id="533c3-537">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-537">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="pure-colors"></a><span data-ttu-id="533c3-538">純虛擬色彩</span><span class="sxs-lookup"><span data-stu-id="533c3-538">Pure colors</span></span>


```HTML
pure
<!elementpure empty>
```



<span data-ttu-id="533c3-539">如果專案 <pure/> 出現在色彩值中，則會提示色彩不應由遞色模式近似。</span><span class="sxs-lookup"><span data-stu-id="533c3-539">If the element <pure/> appears in a color value, it is a hint that the color should not be approximated by a dither pattern.</span></span> <span data-ttu-id="533c3-540">這是層級1的功能，且符合規範的執行不需要接受。</span><span class="sxs-lookup"><span data-stu-id="533c3-540">This is a level 1 feature, and a conforming implementation need not honor it.</span></span> <span data-ttu-id="533c3-541">對於顯示在中型解析度裝置上的圖形（例如影片顯示器）來說，指定是很重要的，因為這類小型功能 (例如線條) 可能會導致色彩失真的錯誤別名。</span><span class="sxs-lookup"><span data-stu-id="533c3-541">The designation is important for graphics displayed on medium-resolution devices, such as video displays, where small features (such as lines) may cause bad aliasing with dithered colors.</span></span> <span data-ttu-id="533c3-542">在印表機（例如印表機）上，通常會將一些完全飽和的色彩，但通常會有足夠的色彩來避免此問題。</span><span class="sxs-lookup"><span data-stu-id="533c3-542">On devices such as printers, which normally dither all colors except for the few fully saturated colors, the dithering is normally sufficiently fine to avoid this problem.</span></span>

<span data-ttu-id="533c3-543">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-543">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-adjustments"></a><span data-ttu-id="533c3-544">色彩調整</span><span class="sxs-lookup"><span data-stu-id="533c3-544">Color adjustments</span></span>

<span data-ttu-id="533c3-545">基底色彩可透過 RGB 值上的算數運算來調整。</span><span class="sxs-lookup"><span data-stu-id="533c3-545">The base color may be adjusted by arithmetic operations on the RGB value.</span></span> <span data-ttu-id="533c3-546">這些作業會使用色彩值內的其他元素來定義。</span><span class="sxs-lookup"><span data-stu-id="533c3-546">These operations are defined using additional elements within the color value.</span></span> <span data-ttu-id="533c3-547">這類調整只有在套用至衍生自其他元素的色彩時才有用。</span><span class="sxs-lookup"><span data-stu-id="533c3-547">Such adjustments are useful only when applied to colors derived from other elements.</span></span> <span data-ttu-id="533c3-548">對固定色彩值指定這類調整是有效的;不過，您可以將此實值縮減為對應的 RGB 值，並儲存該值，而不是使用原始值。</span><span class="sxs-lookup"><span data-stu-id="533c3-548">It is valid to specify such an adjustment on a fixed color value; however, an implementation is permitted to reduce this to the corresponding RGB value and store that instead of the original.</span></span>

<span data-ttu-id="533c3-549">本節所述的所有色彩調整功能都是層級1的功能。</span><span class="sxs-lookup"><span data-stu-id="533c3-549">All the color adjustment features described in this section are level 1 features.</span></span>


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



<span data-ttu-id="533c3-550">前六個作業的參數是範圍0到255的單一整數數值。</span><span class="sxs-lookup"><span data-stu-id="533c3-550">The parameter of the first six operations is a single integral numeric value in the range 0 to 255.</span></span> <span data-ttu-id="533c3-551">調整會在 3x8bit RGB 值上執行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="533c3-551">The adjustment is performed on the 3x8bit RGB value as follows:</span></span>

1.  <span data-ttu-id="533c3-552">如果 <gray/> 指定了，則 RGB 值會由 yyy 取代，其中 y 是從709下的 sRGB 值計算而來的亮度 (y ' ) 值。</span><span class="sxs-lookup"><span data-stu-id="533c3-552">If <gray/> is specified, the RGB value is replaced by yyy, where y is the luminance (y') value calculated from the sRGB value in following the ITU-r BT.709.</span></span> <span data-ttu-id="533c3-553">這項計算如下：</span><span class="sxs-lookup"><span data-stu-id="533c3-553">This calculation is:</span></span>
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  <span data-ttu-id="533c3-554">如果指定了色彩，則會根據下表分別調整每個元件。</span><span class="sxs-lookup"><span data-stu-id="533c3-554">If a color.op modification is given, each component is separately adjusted according to the table below.</span></span> <span data-ttu-id="533c3-555">c 是元件值，而 p 是 color. 參數值。</span><span class="sxs-lookup"><span data-stu-id="533c3-555">c is the component value, and p is the color.parameter value.</span></span>

    | <span data-ttu-id="533c3-556">作業</span><span class="sxs-lookup"><span data-stu-id="533c3-556">Operation</span></span>       | <span data-ttu-id="533c3-557">Formula</span><span class="sxs-lookup"><span data-stu-id="533c3-557">Formula</span></span>                            |
    |-----------------|------------------------------------|
    | <span data-ttu-id="533c3-558">變 暗</span><span class="sxs-lookup"><span data-stu-id="533c3-558">darken</span></span>          | <span data-ttu-id="533c3-559">c： = cxp/255</span><span class="sxs-lookup"><span data-stu-id="533c3-559">c := cxp/255</span></span>                       |
    | <span data-ttu-id="533c3-560">減輕</span><span class="sxs-lookup"><span data-stu-id="533c3-560">lighten</span></span>         | <span data-ttu-id="533c3-561">c： = 255- (255-c) xp/255</span><span class="sxs-lookup"><span data-stu-id="533c3-561">c := 255 - (255-c)xp/255</span></span>           |
    | <span data-ttu-id="533c3-562">add</span><span class="sxs-lookup"><span data-stu-id="533c3-562">add</span></span>             | <span data-ttu-id="533c3-563">c： = c + p</span><span class="sxs-lookup"><span data-stu-id="533c3-563">c := c + p</span></span>                         |
    | <span data-ttu-id="533c3-564">減</span><span class="sxs-lookup"><span data-stu-id="533c3-564">subtract</span></span>        | <span data-ttu-id="533c3-565">c： = c-p</span><span class="sxs-lookup"><span data-stu-id="533c3-565">c := c - p</span></span>                         |
    | <span data-ttu-id="533c3-566">reversesubtract</span><span class="sxs-lookup"><span data-stu-id="533c3-566">reversesubtract</span></span> | <span data-ttu-id="533c3-567">c： = p-c</span><span class="sxs-lookup"><span data-stu-id="533c3-567">c := p - c</span></span>                         |
    | <span data-ttu-id="533c3-568">blackwhite</span><span class="sxs-lookup"><span data-stu-id="533c3-568">blackwhite</span></span>      | <span data-ttu-id="533c3-569">if c < p thenc： = 0elsec： = 255</span><span class="sxs-lookup"><span data-stu-id="533c3-569">if c < p thenc := 0elsec := 255</span></span> |

    

     

    <span data-ttu-id="533c3-570">在每個案例中，如果計算的元件值 c 超過255，則會使用255，如果小於0，則會使用0。</span><span class="sxs-lookup"><span data-stu-id="533c3-570">In each case, if the calculated component value, c, exceeds 255, then 255 is used, and if it is less than 0, then 0 is used.</span></span>

3.  <span data-ttu-id="533c3-571">如果 <INVERT128/> 指定了，則會根據元件是否小於128，將值128減去或加入至每個元件。</span><span class="sxs-lookup"><span data-stu-id="533c3-571">If <INVERT128/> is given, the value 128 is subtracted or added to each component according to whether the component is less than 128 or not.</span></span>
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  <span data-ttu-id="533c3-572">如果 <invert/> 指定了，則會將每個元件取代為255減去元件的值。</span><span class="sxs-lookup"><span data-stu-id="533c3-572">If <invert/> is given, each component is replaced by 255 minus the value of the component.</span></span>
    ```HTML
    c := 255-c
    ```

    

<span data-ttu-id="533c3-573">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-573">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="font"></a><span data-ttu-id="533c3-574">字型</span><span class="sxs-lookup"><span data-stu-id="533c3-574">font</span></span>


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



<span data-ttu-id="533c3-575">您可以使用 [CSS1 區段 5.2 (字型屬性) ](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) 中所定義的樣式屬性來識別字型。</span><span class="sxs-lookup"><span data-stu-id="533c3-575">A font is identified using a style attribute as defined in [CSS1 section 5.2 (font properties)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span></span> <span data-ttu-id="533c3-576">字型元素的主體目前是未定義的，但未來可能會用來編碼標準字型資訊。</span><span class="sxs-lookup"><span data-stu-id="533c3-576">The body of the font element is, at present, undefined but may be used in the future to encode standard font information.</span></span> <span data-ttu-id="533c3-577">本提案的初始實施應該會保留但不會解讀資訊。</span><span class="sxs-lookup"><span data-stu-id="533c3-577">Initial implementations of this proposal should preserve but not interpret the information.</span></span>

<span data-ttu-id="533c3-578">未來，將會為您的換行字型資訊 (可下載的字型，或) 的共用字型資源，未來會新增支援。</span><span class="sxs-lookup"><span data-stu-id="533c3-578">It is conceivable that support will be added in the future for out-of-line font information (downloadable fonts, or shared font resources).</span></span> <span data-ttu-id="533c3-579">這會透過字型元素內容中的 XML 連結元素來完成，以確保具有初始執行的回溯 compatbility。</span><span class="sxs-lookup"><span data-stu-id="533c3-579">This will be done by an XML-link element within the content of the font element, ensuring backward compatbility with initial implementations.</span></span>

<span data-ttu-id="533c3-580">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-580">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="bitmap"></a><span data-ttu-id="533c3-581">點陣圖</span><span class="sxs-lookup"><span data-stu-id="533c3-581">bitmap</span></span>


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



<span data-ttu-id="533c3-582">點陣圖元素可讓您參考非線上圖片資源 (通常是要包含在圖形中的點陣圖) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-582">The bitmap element allows a reference to an out-of-line picture resource (normally a bitmap) to be included in a graphic.</span></span>

<span data-ttu-id="533c3-583">點陣圖是層級1的功能。</span><span class="sxs-lookup"><span data-stu-id="533c3-583">bitmap is a level 1 feature.</span></span>

<span data-ttu-id="533c3-584">行為屬性可用來指出點陣圖應該如何由編輯應用程式處理。</span><span class="sxs-lookup"><span data-stu-id="533c3-584">The behavior attribute may be used to indicate how the bitmap should be handled by an editing application.</span></span> <span data-ttu-id="533c3-585">值可以是下列其中一個或兩個標記。</span><span class="sxs-lookup"><span data-stu-id="533c3-585">The value may be one or both of the following tokens.</span></span>



| <span data-ttu-id="533c3-586">Token</span><span class="sxs-lookup"><span data-stu-id="533c3-586">Token</span></span>    | <span data-ttu-id="533c3-587">描述</span><span class="sxs-lookup"><span data-stu-id="533c3-587">Description</span></span>                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533c3-588">分離</span><span class="sxs-lookup"><span data-stu-id="533c3-588">separate</span></span> | <span data-ttu-id="533c3-589">將點陣圖標記為個別的實體，不應視為檔的整數部分。</span><span class="sxs-lookup"><span data-stu-id="533c3-589">Marks the bitmap as a separate entity, which should not be regarded as an integral part of the document.</span></span> <span data-ttu-id="533c3-590">點陣圖不應與檔一起保存。</span><span class="sxs-lookup"><span data-stu-id="533c3-590">The bitmap should not be kept with the document.</span></span> <span data-ttu-id="533c3-591">如果複製檔，則不應複製點陣圖;如果移動檔，則不應移動點陣圖。</span><span class="sxs-lookup"><span data-stu-id="533c3-591">If the document is copied, the bitmap should not be copied; if the document is moved, the bitmap should not be moved with it.</span></span> |
| <span data-ttu-id="533c3-592">原始</span><span class="sxs-lookup"><span data-stu-id="533c3-592">original</span></span> | <span data-ttu-id="533c3-593">Title 屬性會將點陣圖的原始位置識別為 URL;否則，就不會指定 title 的意義。</span><span class="sxs-lookup"><span data-stu-id="533c3-593">The title attribute identifies the original location of the bitmap as a URL; otherwise, the meaning of title is not specified.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="533c3-594">這些值都是預期行為的提示。</span><span class="sxs-lookup"><span data-stu-id="533c3-594">These values are both hints as to the expected behavior.</span></span> <span data-ttu-id="533c3-595">個別的選項是指 href 所參考資料的行為。</span><span class="sxs-lookup"><span data-stu-id="533c3-595">The separate option refers to the behavior of the data referred to by href.</span></span> <span data-ttu-id="533c3-596">如果同時指定了個別和原始的，應用程式應該會忽略 href URI，並從原始資料重新產生點陣圖。</span><span class="sxs-lookup"><span data-stu-id="533c3-596">If both separate and original are given, the application is expected to disregard the href URI and regenerate the bitmap from the original data.</span></span> <span data-ttu-id="533c3-597">如果只指定原始的，應用程式應該使用 href URI 來尋找點陣圖，但是可讓使用者選擇重新產生它。</span><span class="sxs-lookup"><span data-stu-id="533c3-597">If only original is given, the application is expected to use the href URI to find the bitmap but may give the user the option of regenerating it.</span></span>

<span data-ttu-id="533c3-598">將 href URI 和 title 屬性設為相同的 (詞法) 值是有效的，這適用于參考的點陣圖未「儲存于」檔時。</span><span class="sxs-lookup"><span data-stu-id="533c3-598">It is valid to make the href URI and the title attribute the same (lexical) value -- this is appropriate if the referenced bitmap is not "stored with" the document.</span></span> <span data-ttu-id="533c3-599">它的目的是要 (但不是) 必要的，因為 href 用於檔本身的點陣圖複本，如果刪除參考圖形，則可能會遭到刪除，而且該標題會用來表示共用副本。</span><span class="sxs-lookup"><span data-stu-id="533c3-599">It is intended (though not required) that href be used for the document's own copy of the bitmap -- which may be deleted if the referencing shapes are deleted -- and that title be used to indicate a shared copy.</span></span> <span data-ttu-id="533c3-600">因此，如果兩者都包含相同的值，就不會有檔特定的複本。</span><span class="sxs-lookup"><span data-stu-id="533c3-600">Thus, if both contain the same value there is no document-specific copy.</span></span>

<span data-ttu-id="533c3-601">如果應用程式不符合 XML 資料的實際儲存模型，則可能會忽略該提示。</span><span class="sxs-lookup"><span data-stu-id="533c3-601">Applications may disregard the hint if it does not fit in with the actual storage model of the XML data.</span></span>

<span data-ttu-id="533c3-602">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-602">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="picture-file-formats"></a><span data-ttu-id="533c3-603">圖片檔案格式</span><span class="sxs-lookup"><span data-stu-id="533c3-603">Picture file formats</span></span>

<span data-ttu-id="533c3-604">在此提案的內容中，外部資料一定是用來產生點陣圖的點陣圖或檔案。</span><span class="sxs-lookup"><span data-stu-id="533c3-604">Within the context of this proposal, external data is invariably either a bitmap or a file which is used to produce a bitmap.</span></span> <span data-ttu-id="533c3-605">在轉譯層級0，不需要支援外部點陣圖格式，只會以純色填滿路徑。</span><span class="sxs-lookup"><span data-stu-id="533c3-605">At render level 0, no external bitmap format need be supported -- paths may only be filled with solid colors.</span></span> <span data-ttu-id="533c3-606">若要轉譯一組完整的轉譯層級1填滿，必須支援點陣圖。</span><span class="sxs-lookup"><span data-stu-id="533c3-606">To render the full set of render level 1 fills, bitmaps need to be supported.</span></span> <span data-ttu-id="533c3-607">轉譯層級1包含 (僅) 下列格式：</span><span class="sxs-lookup"><span data-stu-id="533c3-607">Render level 1 includes (only) the following formats:</span></span>

1.  <span data-ttu-id="533c3-608">JFIF，也就是在具有 JFIF 標頭的檔案中內嵌的 ISO/IEC 10918 格式資料， (可以在 SOI maker) 之後被視為特定 APP0 標記，並包括 (只) IJG v6 程式碼所支援的 JPEG 格式範圍。</span><span class="sxs-lookup"><span data-stu-id="533c3-608">JFIF, i.e. ISO/IEC 10918 format data embedded within a file with the JFIF header (which may be regarded as a particular APP0 marker after the SOI maker) and including (only) the range of JPEG formats supported by the IJG v6 code.</span></span>
2.  <span data-ttu-id="533c3-609">.Png （如 PNG 版本1.0 規格所定義）。</span><span class="sxs-lookup"><span data-stu-id="533c3-609">PNG, as defined by the PNG version 1.0 specification.</span></span>

<span data-ttu-id="533c3-610">轉譯層級2也包含下列支援：</span><span class="sxs-lookup"><span data-stu-id="533c3-610">Render level 2 also includes support for the following:</span></span>

-   <span data-ttu-id="533c3-611">GIF，如1987中 CompuServ 所發佈的 GIF 規格所定義 (通常稱為 "GIF87a" ) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-611">GIF, as defined by the GIF specification published by CompuServ in 1987 (normally referred to as "GIF87a").</span></span> <span data-ttu-id="533c3-612">此層級也必須支援 GIF89a，受限於資料不能包含任何需要解讀的延伸區塊，以顯示圖形控制項 extensionswithouta 在使用者輸入或延遲時間的需求以外的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="533c3-612">GIF89a must also be supported at this level, subject to the restriction that the data must not contain any extension blocks that need interpretation to display the bitmap other than graphics control extensionswithouta requirement for user input or a delay time.</span></span> <span data-ttu-id="533c3-613">這可包含批註，而不是純文字延伸。</span><span class="sxs-lookup"><span data-stu-id="533c3-613">This allows comments to be included, but not the plain text extension.</span></span> <span data-ttu-id="533c3-614">應用程式可能會將應用程式插入 (0x21、0xFF) 擴充功能，但使用此提案的術語時，這些必須只包含編輯而非轉譯的資料。</span><span class="sxs-lookup"><span data-stu-id="533c3-614">An application may insert application (0x21, 0xFF) extensions but, using the terminology of this proposal, these must contain only editing, not rendering, data.</span></span>

<span data-ttu-id="533c3-615">圖形中使用的任何其他資料格式都會強制圖形至少為編輯層級3，而且可能會轉譯層級 3 (如果需要資料才能轉譯圖形) 。</span><span class="sxs-lookup"><span data-stu-id="533c3-615">Any other data format used in the graphic forces that graphic to be at least editing level 3 and possibly rendering level 3 (if the data is necessary to render the graphic).</span></span> <span data-ttu-id="533c3-616">建議應用程式發佈其所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="533c3-616">An application is encouraged to publish the formats which it supports.</span></span> <span data-ttu-id="533c3-617">例如，Microsoft Office 原本就支援下列其他格式，因此可能會以下列格式寫入編輯資料：</span><span class="sxs-lookup"><span data-stu-id="533c3-617">For example, Microsoft Office supports the following additional formats natively and may therefore write editing data in this form:</span></span>

1.  <span data-ttu-id="533c3-618">WMF--Windows 中繼檔 (Win 3.1 格式) </span><span class="sxs-lookup"><span data-stu-id="533c3-618">WMF -- Windows metafile (Win 3.1 format)</span></span>
2.  <span data-ttu-id="533c3-619">EMF--Windows "增強" 中繼檔 (Win32 格式) </span><span class="sxs-lookup"><span data-stu-id="533c3-619">EMF -- Windows "enhanced" metafile (Win32 format)</span></span>
3.  <span data-ttu-id="533c3-620">PICT--Mac OS QuickDraw PICT 檔案 (所有版本，但不含 QuickTime 記錄或其他延伸模組) </span><span class="sxs-lookup"><span data-stu-id="533c3-620">PICT -- Mac OS QuickDraw PICT file (all versions but with no QuickTime records or other extensions)</span></span>
4.  <span data-ttu-id="533c3-621">BMP--Windows 點陣圖檔案格式、"os/2" (BITMAPCORE) 、BITMAPINFO、BITMAPV4 和 BITMAPV5 格式</span><span class="sxs-lookup"><span data-stu-id="533c3-621">BMP -- Windows bitmap file format, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4, and BITMAPV5 formats</span></span>

<span data-ttu-id="533c3-622">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="533c3-622">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vector"></a><span data-ttu-id="533c3-623">向量</span><span class="sxs-lookup"><span data-stu-id="533c3-623">vector</span></span>


```HTML
v
<!element v "( #pcdata | p )*">
```



<span data-ttu-id="533c3-624">向量圖形路徑會編碼為 pcdata。</span><span class="sxs-lookup"><span data-stu-id="533c3-624">A vector graphic path is encoded as pcdata.</span></span> <span data-ttu-id="533c3-625">V 元素的內容是混合的，包含以 p 元素選擇性參數化的向量路徑描述。</span><span class="sxs-lookup"><span data-stu-id="533c3-625">The content of the v element is mixed, containing a vector path description optionally parameterized with p elements.</span></span>

[<span data-ttu-id="533c3-626">返回 VML 總覽</span><span class="sxs-lookup"><span data-stu-id="533c3-626">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

