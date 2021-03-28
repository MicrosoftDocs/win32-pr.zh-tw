---
description: 此區段會列出 GetROP2 和 SetROP2 函式所使用的二元點陣作業程式碼。 點陣作業碼定義 GDI 如何將所選畫筆的位與目的地點陣圖中的位結合。
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: 二元點陣運算
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114740"
---
# <a name="binary-raster-operations"></a><span data-ttu-id="e257d-104">二元點陣運算</span><span class="sxs-lookup"><span data-stu-id="e257d-104">Binary Raster Operations</span></span>

<span data-ttu-id="e257d-105">此區段會列出 [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) 和 [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) 函式所使用的二元點陣作業程式碼。</span><span class="sxs-lookup"><span data-stu-id="e257d-105">This section lists the binary raster-operation codes used by the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) and [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) functions.</span></span> <span data-ttu-id="e257d-106">點陣作業碼定義 GDI 如何將所選畫筆的位與目的地點陣圖中的位結合。</span><span class="sxs-lookup"><span data-stu-id="e257d-106">Raster-operation codes define how GDI combines the bits from the selected pen with the bits in the destination bitmap.</span></span>

<span data-ttu-id="e257d-107">每個點陣作業程式碼都代表一個布耳運算，其中所選畫筆和目的點陣圖中的圖元值會合並。</span><span class="sxs-lookup"><span data-stu-id="e257d-107">Each raster-operation code represents a Boolean operation in which the values of the pixels in the selected pen and the destination bitmap are combined.</span></span> <span data-ttu-id="e257d-108">以下是這些作業中使用的兩個運算元。</span><span class="sxs-lookup"><span data-stu-id="e257d-108">The following are the two operands used in these operations.</span></span>



| <span data-ttu-id="e257d-109">運算元</span><span class="sxs-lookup"><span data-stu-id="e257d-109">Operand</span></span> | <span data-ttu-id="e257d-110">意義</span><span class="sxs-lookup"><span data-stu-id="e257d-110">Meaning</span></span>            |
|---------|--------------------|
| <span data-ttu-id="e257d-111">P</span><span class="sxs-lookup"><span data-stu-id="e257d-111">P</span></span>       | <span data-ttu-id="e257d-112">選取的畫筆</span><span class="sxs-lookup"><span data-stu-id="e257d-112">Selected pen</span></span>       |
| <span data-ttu-id="e257d-113">D</span><span class="sxs-lookup"><span data-stu-id="e257d-113">D</span></span>       | <span data-ttu-id="e257d-114">目的地點陣圖</span><span class="sxs-lookup"><span data-stu-id="e257d-114">Destination bitmap</span></span> |



 

<span data-ttu-id="e257d-115">這些作業中使用的布林運算子如下所示。</span><span class="sxs-lookup"><span data-stu-id="e257d-115">The Boolean operators used in these operations follow.</span></span>



| <span data-ttu-id="e257d-116">運算子</span><span class="sxs-lookup"><span data-stu-id="e257d-116">Operator</span></span> | <span data-ttu-id="e257d-117">意義</span><span class="sxs-lookup"><span data-stu-id="e257d-117">Meaning</span></span>                    |
|----------|----------------------------|
| <span data-ttu-id="e257d-118">a</span><span class="sxs-lookup"><span data-stu-id="e257d-118">a</span></span>        | <span data-ttu-id="e257d-119">位元 AND</span><span class="sxs-lookup"><span data-stu-id="e257d-119">Bitwise AND</span></span>                |
| <span data-ttu-id="e257d-120">n</span><span class="sxs-lookup"><span data-stu-id="e257d-120">n</span></span>        | <span data-ttu-id="e257d-121">位 NOT (反向) </span><span class="sxs-lookup"><span data-stu-id="e257d-121">Bitwise NOT (inverse)</span></span>      |
| <span data-ttu-id="e257d-122">o</span><span class="sxs-lookup"><span data-stu-id="e257d-122">o</span></span>        | <span data-ttu-id="e257d-123">位元 OR</span><span class="sxs-lookup"><span data-stu-id="e257d-123">Bitwise OR</span></span>                 |
| <span data-ttu-id="e257d-124">x</span><span class="sxs-lookup"><span data-stu-id="e257d-124">x</span></span>        | <span data-ttu-id="e257d-125">位互斥 OR (XOR) </span><span class="sxs-lookup"><span data-stu-id="e257d-125">Bitwise exclusive OR (XOR)</span></span> |



 

<span data-ttu-id="e257d-126">所有布林值作業都會以反轉波蘭文標記法呈現。</span><span class="sxs-lookup"><span data-stu-id="e257d-126">All Boolean operations are presented in reverse Polish notation.</span></span> <span data-ttu-id="e257d-127">例如，下列作業會以畫筆的圖元值與所選筆刷的組合來取代目的地點陣圖中的圖元值：</span><span class="sxs-lookup"><span data-stu-id="e257d-127">For example, the following operation replaces the values of the pixels in the destination bitmap with a combination of the pixel values of the pen and the selected brush:</span></span>


```C++
DPo 
```



<span data-ttu-id="e257d-128">每個點陣作業程式碼都是一個32位的整數，其高序位單字是布耳運算索引，而其低序位字是作業程式碼。</span><span class="sxs-lookup"><span data-stu-id="e257d-128">Each raster-operation code is a 32-bit integer whose high-order word is a Boolean operation index and whose low-order word is the operation code.</span></span> <span data-ttu-id="e257d-129">16位作業索引是零擴充的8位值，表示在兩個參數上的布耳運算所產生的所有可能結果 (在此案例中，) 的畫筆和目的地值。</span><span class="sxs-lookup"><span data-stu-id="e257d-129">The 16-bit operation index is a zero-extended 8-bit value that represents all possible outcomes resulting from the Boolean operation on two parameters (in this case, the pen and destination values).</span></span> <span data-ttu-id="e257d-130">例如，下列清單會顯示 DPo 和 DPan 作業的作業索引。</span><span class="sxs-lookup"><span data-stu-id="e257d-130">For example, the operation indexes for the DPo and DPan operations are shown in the following list.</span></span>



| <span data-ttu-id="e257d-131">P</span><span class="sxs-lookup"><span data-stu-id="e257d-131">P</span></span>   | <span data-ttu-id="e257d-132">D</span><span class="sxs-lookup"><span data-stu-id="e257d-132">D</span></span>   | <span data-ttu-id="e257d-133">DPo</span><span class="sxs-lookup"><span data-stu-id="e257d-133">DPo</span></span> | <span data-ttu-id="e257d-134">Dpan</span><span class="sxs-lookup"><span data-stu-id="e257d-134">Dpan</span></span> |
|-----|-----|-----|------|
| <span data-ttu-id="e257d-135">0</span><span class="sxs-lookup"><span data-stu-id="e257d-135">0</span></span>   | <span data-ttu-id="e257d-136">0</span><span class="sxs-lookup"><span data-stu-id="e257d-136">0</span></span>   | <span data-ttu-id="e257d-137">0</span><span class="sxs-lookup"><span data-stu-id="e257d-137">0</span></span>   | <span data-ttu-id="e257d-138">1</span><span class="sxs-lookup"><span data-stu-id="e257d-138">1</span></span>    |
| <span data-ttu-id="e257d-139">0</span><span class="sxs-lookup"><span data-stu-id="e257d-139">0</span></span>   | <span data-ttu-id="e257d-140">1</span><span class="sxs-lookup"><span data-stu-id="e257d-140">1</span></span>   | <span data-ttu-id="e257d-141">1</span><span class="sxs-lookup"><span data-stu-id="e257d-141">1</span></span>   | <span data-ttu-id="e257d-142">1</span><span class="sxs-lookup"><span data-stu-id="e257d-142">1</span></span>    |
| <span data-ttu-id="e257d-143">1</span><span class="sxs-lookup"><span data-stu-id="e257d-143">1</span></span>   | <span data-ttu-id="e257d-144">0</span><span class="sxs-lookup"><span data-stu-id="e257d-144">0</span></span>   | <span data-ttu-id="e257d-145">1</span><span class="sxs-lookup"><span data-stu-id="e257d-145">1</span></span>   | <span data-ttu-id="e257d-146">1</span><span class="sxs-lookup"><span data-stu-id="e257d-146">1</span></span>    |
| <span data-ttu-id="e257d-147">1</span><span class="sxs-lookup"><span data-stu-id="e257d-147">1</span></span>   | <span data-ttu-id="e257d-148">1</span><span class="sxs-lookup"><span data-stu-id="e257d-148">1</span></span>   | <span data-ttu-id="e257d-149">1</span><span class="sxs-lookup"><span data-stu-id="e257d-149">1</span></span>   | <span data-ttu-id="e257d-150">0</span><span class="sxs-lookup"><span data-stu-id="e257d-150">0</span></span>    |



 

<span data-ttu-id="e257d-151">下列清單概述繪圖模式以及它們所代表的布耳運算。</span><span class="sxs-lookup"><span data-stu-id="e257d-151">The following list outlines the drawing modes and the Boolean operations that they represent.</span></span>



| <span data-ttu-id="e257d-152">點陣運算</span><span class="sxs-lookup"><span data-stu-id="e257d-152">Raster operation</span></span> | <span data-ttu-id="e257d-153">布耳運算</span><span class="sxs-lookup"><span data-stu-id="e257d-153">Boolean operation</span></span> |
|------------------|-------------------|
| <span data-ttu-id="e257d-154">R2 \_ 黑色</span><span class="sxs-lookup"><span data-stu-id="e257d-154">R2\_BLACK</span></span>        | <span data-ttu-id="e257d-155">0</span><span class="sxs-lookup"><span data-stu-id="e257d-155">0</span></span>                 |
| <span data-ttu-id="e257d-156">R2 \_ COPYPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-156">R2\_COPYPEN</span></span>      | <span data-ttu-id="e257d-157">P</span><span class="sxs-lookup"><span data-stu-id="e257d-157">P</span></span>                 |
| <span data-ttu-id="e257d-158">R2 \_ MASKNOTPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-158">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="e257d-159">DPna</span><span class="sxs-lookup"><span data-stu-id="e257d-159">DPna</span></span>              |
| <span data-ttu-id="e257d-160">R2 \_ MASKPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-160">R2\_MASKPEN</span></span>      | <span data-ttu-id="e257d-161">Dpa</span><span class="sxs-lookup"><span data-stu-id="e257d-161">DPa</span></span>               |
| <span data-ttu-id="e257d-162">R2 \_ MASKPENNOT</span><span class="sxs-lookup"><span data-stu-id="e257d-162">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="e257d-163">PDna</span><span class="sxs-lookup"><span data-stu-id="e257d-163">PDna</span></span>              |
| <span data-ttu-id="e257d-164">R2 \_ MERGENOTPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-164">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="e257d-165">DPno</span><span class="sxs-lookup"><span data-stu-id="e257d-165">DPno</span></span>              |
| <span data-ttu-id="e257d-166">R2 \_ MERGEPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-166">R2\_MERGEPEN</span></span>     | <span data-ttu-id="e257d-167">DPo</span><span class="sxs-lookup"><span data-stu-id="e257d-167">DPo</span></span>               |
| <span data-ttu-id="e257d-168">R2 \_ MERGEPENNOT</span><span class="sxs-lookup"><span data-stu-id="e257d-168">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="e257d-169">PDno</span><span class="sxs-lookup"><span data-stu-id="e257d-169">PDno</span></span>              |
| <span data-ttu-id="e257d-170">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="e257d-170">R2\_NOP</span></span>          | <span data-ttu-id="e257d-171">D</span><span class="sxs-lookup"><span data-stu-id="e257d-171">D</span></span>                 |
| <span data-ttu-id="e257d-172">R2 \_ 未</span><span class="sxs-lookup"><span data-stu-id="e257d-172">R2\_NOT</span></span>          | <span data-ttu-id="e257d-173">DN</span><span class="sxs-lookup"><span data-stu-id="e257d-173">Dn</span></span>                |
| <span data-ttu-id="e257d-174">R2 \_ NOTCOPYPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-174">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="e257d-175">Pn</span><span class="sxs-lookup"><span data-stu-id="e257d-175">Pn</span></span>                |
| <span data-ttu-id="e257d-176">R2 \_ NOTMASKPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-176">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="e257d-177">DPan</span><span class="sxs-lookup"><span data-stu-id="e257d-177">DPan</span></span>              |
| <span data-ttu-id="e257d-178">R2 \_ NOTMERGEPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-178">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="e257d-179">DPon</span><span class="sxs-lookup"><span data-stu-id="e257d-179">DPon</span></span>              |
| <span data-ttu-id="e257d-180">R2 \_ NOTXORPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-180">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="e257d-181">DPxn</span><span class="sxs-lookup"><span data-stu-id="e257d-181">DPxn</span></span>              |
| <span data-ttu-id="e257d-182">R2 \_ 白色</span><span class="sxs-lookup"><span data-stu-id="e257d-182">R2\_WHITE</span></span>        | <span data-ttu-id="e257d-183">1</span><span class="sxs-lookup"><span data-stu-id="e257d-183">1</span></span>                 |
| <span data-ttu-id="e257d-184">R2 \_ XORPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-184">R2\_XORPEN</span></span>       | <span data-ttu-id="e257d-185">DPx</span><span class="sxs-lookup"><span data-stu-id="e257d-185">DPx</span></span>               |



 

<span data-ttu-id="e257d-186">若為單色裝置，GDI 會將零值對應至黑色，並將值1對應至白色。</span><span class="sxs-lookup"><span data-stu-id="e257d-186">For a monochrome device, GDI maps the value zero to black and the value 1 to white.</span></span> <span data-ttu-id="e257d-187">如果應用程式嘗試使用可用的二進位點陣運算在白色目的地上繪製黑色畫筆，則會發生下列結果。</span><span class="sxs-lookup"><span data-stu-id="e257d-187">If an application attempts to draw with a black pen on a white destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="e257d-188">點陣運算</span><span class="sxs-lookup"><span data-stu-id="e257d-188">Raster operation</span></span> | <span data-ttu-id="e257d-189">結果</span><span class="sxs-lookup"><span data-stu-id="e257d-189">Result</span></span>             |
|------------------|--------------------|
| <span data-ttu-id="e257d-190">R2 \_ 黑色</span><span class="sxs-lookup"><span data-stu-id="e257d-190">R2\_BLACK</span></span>        | <span data-ttu-id="e257d-191">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-191">Visible black line</span></span> |
| <span data-ttu-id="e257d-192">R2 \_ COPYPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-192">R2\_COPYPEN</span></span>      | <span data-ttu-id="e257d-193">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-193">Visible black line</span></span> |
| <span data-ttu-id="e257d-194">R2 \_ MASKNOTPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-194">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="e257d-195">沒有可見的行</span><span class="sxs-lookup"><span data-stu-id="e257d-195">No visible line</span></span>    |
| <span data-ttu-id="e257d-196">R2 \_ MASKPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-196">R2\_MASKPEN</span></span>      | <span data-ttu-id="e257d-197">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-197">Visible black line</span></span> |
| <span data-ttu-id="e257d-198">R2 \_ MASKPENNOT</span><span class="sxs-lookup"><span data-stu-id="e257d-198">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="e257d-199">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-199">Visible black line</span></span> |
| <span data-ttu-id="e257d-200">R2 \_ MERGENOTPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-200">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="e257d-201">沒有可見的行</span><span class="sxs-lookup"><span data-stu-id="e257d-201">No visible line</span></span>    |
| <span data-ttu-id="e257d-202">R2 \_ MERGEPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-202">R2\_MERGEPEN</span></span>     | <span data-ttu-id="e257d-203">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-203">Visible black line</span></span> |
| <span data-ttu-id="e257d-204">R2 \_ MERGEPENNOT</span><span class="sxs-lookup"><span data-stu-id="e257d-204">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="e257d-205">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-205">Visible black line</span></span> |
| <span data-ttu-id="e257d-206">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="e257d-206">R2\_NOP</span></span>          | <span data-ttu-id="e257d-207">沒有可見的行</span><span class="sxs-lookup"><span data-stu-id="e257d-207">No visible line</span></span>    |
| <span data-ttu-id="e257d-208">R2 \_ 未</span><span class="sxs-lookup"><span data-stu-id="e257d-208">R2\_NOT</span></span>          | <span data-ttu-id="e257d-209">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-209">Visible black line</span></span> |
| <span data-ttu-id="e257d-210">R2 \_ NOTCOPYPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-210">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="e257d-211">沒有可見的行</span><span class="sxs-lookup"><span data-stu-id="e257d-211">No visible line</span></span>    |
| <span data-ttu-id="e257d-212">R2 \_ NOTMASKPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-212">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="e257d-213">沒有可見的行</span><span class="sxs-lookup"><span data-stu-id="e257d-213">No visible line</span></span>    |
| <span data-ttu-id="e257d-214">R2 \_ NOTMERGEPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-214">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="e257d-215">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-215">Visible black line</span></span> |
| <span data-ttu-id="e257d-216">R2 \_ NOTXORPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-216">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="e257d-217">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-217">Visible black line</span></span> |
| <span data-ttu-id="e257d-218">R2 \_ 白色</span><span class="sxs-lookup"><span data-stu-id="e257d-218">R2\_WHITE</span></span>        | <span data-ttu-id="e257d-219">沒有可見的行</span><span class="sxs-lookup"><span data-stu-id="e257d-219">No visible line</span></span>    |
| <span data-ttu-id="e257d-220">R2 \_ XORPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-220">R2\_XORPEN</span></span>       | <span data-ttu-id="e257d-221">沒有可見的行</span><span class="sxs-lookup"><span data-stu-id="e257d-221">No visible line</span></span>    |



 

<span data-ttu-id="e257d-222">針對色彩裝置，GDI 會使用 RGB 值來表示畫筆和目的地的色彩。</span><span class="sxs-lookup"><span data-stu-id="e257d-222">For a color device, GDI uses RGB values to represent the colors of the pen and the destination.</span></span> <span data-ttu-id="e257d-223">RGB 色彩值是包含紅色、綠色和藍色色彩欄位的長整數，每個都指定指定色彩的濃度。</span><span class="sxs-lookup"><span data-stu-id="e257d-223">An RGB color value is a long integer that contains a red, a green, and a blue color field, each specifying the intensity of the specified color.</span></span> <span data-ttu-id="e257d-224">濃度的範圍是從0到255。</span><span class="sxs-lookup"><span data-stu-id="e257d-224">Intensities range from 0 through 255.</span></span> <span data-ttu-id="e257d-225">這些值會以長整數的三個低序位位元組封裝。</span><span class="sxs-lookup"><span data-stu-id="e257d-225">The values are packed in the three low-order bytes of the long integer.</span></span> <span data-ttu-id="e257d-226">畫筆的色彩一律是純色，但目的地的色彩可能是任何二或三種色彩的混合。</span><span class="sxs-lookup"><span data-stu-id="e257d-226">The color of a pen is always a solid color, but the color of the destination may be a mixture of any two or three colors.</span></span> <span data-ttu-id="e257d-227">如果應用程式嘗試使用可用的二進位點陣運算，在藍色目的地繪製白色畫筆，則會發生下列結果。</span><span class="sxs-lookup"><span data-stu-id="e257d-227">If an application attempts to draw with a white pen on a blue destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="e257d-228">點陣運算</span><span class="sxs-lookup"><span data-stu-id="e257d-228">Raster operation</span></span> | <span data-ttu-id="e257d-229">結果</span><span class="sxs-lookup"><span data-stu-id="e257d-229">Result</span></span>                 |
|------------------|------------------------|
| <span data-ttu-id="e257d-230">R2 \_ 黑色</span><span class="sxs-lookup"><span data-stu-id="e257d-230">R2\_BLACK</span></span>        | <span data-ttu-id="e257d-231">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-231">Visible black line</span></span>     |
| <span data-ttu-id="e257d-232">R2 \_ COPYPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-232">R2\_COPYPEN</span></span>      | <span data-ttu-id="e257d-233">可見的白色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-233">Visible white line</span></span>     |
| <span data-ttu-id="e257d-234">R2 \_ MASKNOTPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-234">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="e257d-235">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-235">Visible black line</span></span>     |
| <span data-ttu-id="e257d-236">R2 \_ MASKPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-236">R2\_MASKPEN</span></span>      | <span data-ttu-id="e257d-237">不可見的藍線</span><span class="sxs-lookup"><span data-stu-id="e257d-237">Invisible blue line</span></span>    |
| <span data-ttu-id="e257d-238">R2 \_ MASKPENNOT</span><span class="sxs-lookup"><span data-stu-id="e257d-238">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="e257d-239">可見的紅色/綠線</span><span class="sxs-lookup"><span data-stu-id="e257d-239">Visible red/green line</span></span> |
| <span data-ttu-id="e257d-240">R2 \_ MERGENOTPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-240">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="e257d-241">不可見的藍線</span><span class="sxs-lookup"><span data-stu-id="e257d-241">Invisible blue line</span></span>    |
| <span data-ttu-id="e257d-242">R2 \_ MERGEPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-242">R2\_MERGEPEN</span></span>     | <span data-ttu-id="e257d-243">可見的白色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-243">Visible white line</span></span>     |
| <span data-ttu-id="e257d-244">R2 \_ MERGEPENNOT</span><span class="sxs-lookup"><span data-stu-id="e257d-244">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="e257d-245">可見的白色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-245">Visible white line</span></span>     |
| <span data-ttu-id="e257d-246">R2 \_ NOP</span><span class="sxs-lookup"><span data-stu-id="e257d-246">R2\_NOP</span></span>          | <span data-ttu-id="e257d-247">不可見的藍線</span><span class="sxs-lookup"><span data-stu-id="e257d-247">Invisible blue line</span></span>    |
| <span data-ttu-id="e257d-248">R2 \_ 未</span><span class="sxs-lookup"><span data-stu-id="e257d-248">R2\_NOT</span></span>          | <span data-ttu-id="e257d-249">可見的紅色/綠線</span><span class="sxs-lookup"><span data-stu-id="e257d-249">Visible red/green line</span></span> |
| <span data-ttu-id="e257d-250">R2 \_ NOTCOPYPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-250">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="e257d-251">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-251">Visible black line</span></span>     |
| <span data-ttu-id="e257d-252">R2 \_ NOTMASKPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-252">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="e257d-253">可見的紅色/綠線</span><span class="sxs-lookup"><span data-stu-id="e257d-253">Visible red/green line</span></span> |
| <span data-ttu-id="e257d-254">R2 \_ NOTMERGEPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-254">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="e257d-255">可見的黑色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-255">Visible black line</span></span>     |
| <span data-ttu-id="e257d-256">R2 \_ NOTXORPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-256">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="e257d-257">不可見的藍線</span><span class="sxs-lookup"><span data-stu-id="e257d-257">Invisible blue line</span></span>    |
| <span data-ttu-id="e257d-258">R2 \_ 白色</span><span class="sxs-lookup"><span data-stu-id="e257d-258">R2\_WHITE</span></span>        | <span data-ttu-id="e257d-259">可見的白色線條</span><span class="sxs-lookup"><span data-stu-id="e257d-259">Visible white line</span></span>     |
| <span data-ttu-id="e257d-260">R2 \_ XORPEN</span><span class="sxs-lookup"><span data-stu-id="e257d-260">R2\_XORPEN</span></span>       | <span data-ttu-id="e257d-261">可見的紅色/綠線</span><span class="sxs-lookup"><span data-stu-id="e257d-261">Visible red/green line</span></span> |



 

 

 



