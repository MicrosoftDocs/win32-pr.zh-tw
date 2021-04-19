---
title: 'glPixelTransferi 函式 (Gl) '
description: 'GlPixelTransferf 和 glPixelTransferi 函數會設定圖元傳輸模式。 |glPixelTransferi 函式 (Gl) '
ms.assetid: 351a872d-2cce-4fb1-b736-72201baf4157
keywords:
- glPixelTransferi 函式 OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67415a8e105dc95f3e21e6968042496b9db52038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992258"
---
# <a name="glpixeltransferi-function"></a><span data-ttu-id="57815-105">glPixelTransferi 函式</span><span class="sxs-lookup"><span data-stu-id="57815-105">glPixelTransferi function</span></span>

<span data-ttu-id="57815-106">[**GlPixelTransferf**](glpixeltransferf.md)和 **glPixelTransferi** 函數會設定圖元傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="57815-106">The [**glPixelTransferf**](glpixeltransferf.md) and **glPixelTransferi** functions set pixel transfer modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="57815-107">語法</span><span class="sxs-lookup"><span data-stu-id="57815-107">Syntax</span></span>


```C++
void WINAPI glPixelTransferi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="57815-108">參數</span><span class="sxs-lookup"><span data-stu-id="57815-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57815-109">*pname*</span><span class="sxs-lookup"><span data-stu-id="57815-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="57815-110">要設定之圖元傳輸參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="57815-110">The symbolic name of the pixel transfer parameter to be set.</span></span> <span data-ttu-id="57815-111">下表提供每個以 **glPixelTransfer** 設定之圖元傳輸參數的類型、初始值和有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="57815-111">The following table gives the type, initial value, and range of valid values for each of the pixel transfer parameters that are set with **glPixelTransfer**.</span></span>



| <span data-ttu-id="57815-112">Pname</span><span class="sxs-lookup"><span data-stu-id="57815-112">Pname</span></span>             | <span data-ttu-id="57815-113">類型</span><span class="sxs-lookup"><span data-stu-id="57815-113">Type</span></span>    | <span data-ttu-id="57815-114">初始值</span><span class="sxs-lookup"><span data-stu-id="57815-114">Initial Value</span></span>  | <span data-ttu-id="57815-115">有效範圍</span><span class="sxs-lookup"><span data-stu-id="57815-115">Valid Range</span></span>  |
|-------------------|---------|----------------|--------------|
| <span data-ttu-id="57815-116">GL \_ 地圖 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="57815-116">GL\_MAP\_COLOR</span></span>    | <span data-ttu-id="57815-117">Boolean</span><span class="sxs-lookup"><span data-stu-id="57815-117">Boolean</span></span> | <span data-ttu-id="57815-118">false</span><span class="sxs-lookup"><span data-stu-id="57815-118">false</span></span>          | <span data-ttu-id="57815-119">true/false</span><span class="sxs-lookup"><span data-stu-id="57815-119">true/false</span></span>   |
| <span data-ttu-id="57815-120">GL \_ 地圖 \_ 範本</span><span class="sxs-lookup"><span data-stu-id="57815-120">GL\_MAP\_STENCIL</span></span>  | <span data-ttu-id="57815-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="57815-121">Boolean</span></span> | <span data-ttu-id="57815-122">false</span><span class="sxs-lookup"><span data-stu-id="57815-122">false</span></span>          | <span data-ttu-id="57815-123">true/false</span><span class="sxs-lookup"><span data-stu-id="57815-123">true/false</span></span>   |
| <span data-ttu-id="57815-124">GL \_ 索引 \_ 移位</span><span class="sxs-lookup"><span data-stu-id="57815-124">GL\_INDEX\_SHIFT</span></span>  | <span data-ttu-id="57815-125">整數</span><span class="sxs-lookup"><span data-stu-id="57815-125">integer</span></span> | <span data-ttu-id="57815-126">0</span><span class="sxs-lookup"><span data-stu-id="57815-126">0</span></span>              | <span data-ttu-id="57815-127"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-127">(8,8)</span></span>        |
| <span data-ttu-id="57815-128">GL \_ 索引 \_ 位移</span><span class="sxs-lookup"><span data-stu-id="57815-128">GL\_INDEX\_OFFSET</span></span> | <span data-ttu-id="57815-129">整數</span><span class="sxs-lookup"><span data-stu-id="57815-129">integer</span></span> | <span data-ttu-id="57815-130">0</span><span class="sxs-lookup"><span data-stu-id="57815-130">0</span></span>              | <span data-ttu-id="57815-131"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-131">(8,8)</span></span>        |
| <span data-ttu-id="57815-132">GL \_ RED \_ SCALE</span><span class="sxs-lookup"><span data-stu-id="57815-132">GL\_RED\_SCALE</span></span>    | <span data-ttu-id="57815-133">整數</span><span class="sxs-lookup"><span data-stu-id="57815-133">integer</span></span> | <span data-ttu-id="57815-134">1.0</span><span class="sxs-lookup"><span data-stu-id="57815-134">1.0</span></span>            | <span data-ttu-id="57815-135"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-135">(8,8)</span></span>        |
| <span data-ttu-id="57815-136">GL \_ 綠 \_ 級</span><span class="sxs-lookup"><span data-stu-id="57815-136">GL\_GREEN\_SCALE</span></span>  | <span data-ttu-id="57815-137">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-137">float</span></span>   | <span data-ttu-id="57815-138">1.0</span><span class="sxs-lookup"><span data-stu-id="57815-138">1.0</span></span>            | <span data-ttu-id="57815-139"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-139">(8,8)</span></span>        |
| <span data-ttu-id="57815-140">GL \_ 藍色 \_ 調整</span><span class="sxs-lookup"><span data-stu-id="57815-140">GL\_BLUE\_SCALE</span></span>   | <span data-ttu-id="57815-141">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-141">float</span></span>   | <span data-ttu-id="57815-142">1.0</span><span class="sxs-lookup"><span data-stu-id="57815-142">1.0</span></span>            | <span data-ttu-id="57815-143"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-143">(8,8)</span></span>        |
| <span data-ttu-id="57815-144">GL \_ ALPHA \_ 刻度</span><span class="sxs-lookup"><span data-stu-id="57815-144">GL\_ALPHA\_SCALE</span></span>  | <span data-ttu-id="57815-145">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-145">float</span></span>   | <span data-ttu-id="57815-146">1.0</span><span class="sxs-lookup"><span data-stu-id="57815-146">1.0</span></span>            | <span data-ttu-id="57815-147"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-147">(8,8)</span></span>        |
| <span data-ttu-id="57815-148">GL \_ 深度 \_ 調整</span><span class="sxs-lookup"><span data-stu-id="57815-148">GL\_DEPTH\_SCALE</span></span>  | <span data-ttu-id="57815-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-149">float</span></span>   | <span data-ttu-id="57815-150">1.0</span><span class="sxs-lookup"><span data-stu-id="57815-150">1.0</span></span>            | <span data-ttu-id="57815-151"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-151">(8,8)</span></span>        |
| <span data-ttu-id="57815-152">GL \_ 紅色 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-152">GL\_RED\_BIAS</span></span>     | <span data-ttu-id="57815-153">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-153">float</span></span>   | <span data-ttu-id="57815-154">0.0</span><span class="sxs-lookup"><span data-stu-id="57815-154">0.0</span></span>            | <span data-ttu-id="57815-155"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-155">(8,8)</span></span>        |
| <span data-ttu-id="57815-156">GL \_ 綠色 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-156">GL\_GREEN\_BIAS</span></span>   | <span data-ttu-id="57815-157">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-157">float</span></span>   | <span data-ttu-id="57815-158">0.0</span><span class="sxs-lookup"><span data-stu-id="57815-158">0.0</span></span>            | <span data-ttu-id="57815-159"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-159">(8,8)</span></span>        |
| <span data-ttu-id="57815-160">GL \_ 藍色 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-160">GL\_BLUE\_BIAS</span></span>    | <span data-ttu-id="57815-161">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-161">float</span></span>   | <span data-ttu-id="57815-162">0.0</span><span class="sxs-lookup"><span data-stu-id="57815-162">0.0</span></span>            | <span data-ttu-id="57815-163"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-163">(8,8)</span></span>        |
| <span data-ttu-id="57815-164">GL \_ ALPHA \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-164">GL\_ALPHA\_BIAS</span></span>   | <span data-ttu-id="57815-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-165">float</span></span>   | <span data-ttu-id="57815-166">0.0</span><span class="sxs-lookup"><span data-stu-id="57815-166">0.0</span></span>            | <span data-ttu-id="57815-167"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-167">(8,8)</span></span>        |
| <span data-ttu-id="57815-168">GL \_ 深度 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-168">GL\_DEPTH\_BIAS</span></span>   | <span data-ttu-id="57815-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="57815-169">float</span></span>   | <span data-ttu-id="57815-170">0.0</span><span class="sxs-lookup"><span data-stu-id="57815-170">0.0</span></span>            | <span data-ttu-id="57815-171"> (8、8) </span><span class="sxs-lookup"><span data-stu-id="57815-171">(8,8)</span></span>        |



 

</dd> <dt>

<span data-ttu-id="57815-172">*param*</span><span class="sxs-lookup"><span data-stu-id="57815-172">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="57815-173">*Pname* 設定為的值。</span><span class="sxs-lookup"><span data-stu-id="57815-173">The value that *pname* is set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57815-174">傳回值</span><span class="sxs-lookup"><span data-stu-id="57815-174">Return value</span></span>

<span data-ttu-id="57815-175">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="57815-175">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57815-176">備註</span><span class="sxs-lookup"><span data-stu-id="57815-176">Remarks</span></span>

<span data-ttu-id="57815-177">**GlPixelTransfer** 函式會設定圖元傳輸模式，其會影響後續 [**glCopyPixels**](glcopypixels.md)、 [**glCopyTexImage1D**](glcopyteximage1d.md)、 [**glCopyTexImage2D**](glcopyteximage2d.md)、 [**glCopyTexSubImage1D**](glcopytexsubimage1d.md)、 [**glCopyTexSubImage2D**](glcopytexsubimage2d.md)、 [**glDrawPixels**](gldrawpixels.md)、 [**glReadPixels**](glreadpixels.md)、 [**glTexImage1D**](glteximage1d.md)、 [**glTexImage2D**](glteximage2d.md)、 [**glTexSubImage1D**](gltexsubimage1d.md)和 [**glTexSubImage2D**](gltexsubimage2d.md)命令的操作。</span><span class="sxs-lookup"><span data-stu-id="57815-177">The **glPixelTransfer** function sets pixel transfer modes that affect the operation of subsequent [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md) commands.</span></span> <span data-ttu-id="57815-178">圖元傳輸模式所指定的演算法在從畫面格緩衝區讀取之後，會以圖元為單位運作， (**glReadPixels** 和 **glCopyPixels**) 或從用戶端記憶體 (**glDrawPixels**、 **glTexImage1D** 和 **glTexImage2D**) 解壓縮。</span><span class="sxs-lookup"><span data-stu-id="57815-178">The algorithms that are specified by pixel transfer modes operate on pixels after they are read from the framebuffer (**glReadPixels** and **glCopyPixels**) or unpacked from client memory (**glDrawPixels**, **glTexImage1D**, and **glTexImage2D**).</span></span> <span data-ttu-id="57815-179">圖元傳送作業會以相同的順序進行，並以相同的方式執行，而不論造成圖元運算的命令為何。</span><span class="sxs-lookup"><span data-stu-id="57815-179">Pixel transfer operations happen in the same order, and in the same manner, regardless of the command that resulted in the pixel operation.</span></span> <span data-ttu-id="57815-180">圖元儲存模式 ([**glPixelStore**](glpixelstore-functions.md)) 控制要從用戶端記憶體中讀取的圖元，以及將圖元包裝回用戶端記憶體的方式。</span><span class="sxs-lookup"><span data-stu-id="57815-180">Pixel storage modes ([**glPixelStore**](glpixelstore-functions.md)) control the unpacking of pixels being read from client memory, and the packing of pixels being written back into client memory.</span></span>

<span data-ttu-id="57815-181">圖元傳輸作業會處理四個基本圖元類型： *色彩*、 *色彩索引*、 *深度* 和 *樣板。* 色彩圖元是由四個具有未指定尾數和指數大小的浮點值所組成，其縮放比例為0.0 表示零濃度，1.0 代表完整濃度。</span><span class="sxs-lookup"><span data-stu-id="57815-181">Pixel transfer operations handle four fundamental pixel types: *color*, *color index*, *depth*, and *stencil*.Color pixels are made up of four floating-point values with unspecified mantissa and exponent sizes, scaled such that 0.0 represents zero intensity and 1.0 represents full intensity.</span></span> <span data-ttu-id="57815-182">色彩索引是由單一固定點值組成，而且在二進位點右邊沒有未指定的精確度。</span><span class="sxs-lookup"><span data-stu-id="57815-182">Color indexes comprise a single fixed-point value, with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="57815-183">深度圖元組成單一浮點值，具有未指定的尾數和指數大小，可進行調整以使0.0 表示最小深度緩衝區值，1.0 則代表最大深度緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="57815-183">Depth pixels comprise a single floating-point value, with unspecified mantissa and exponent sizes, scaled such that 0.0 represents the minimum depth buffer value, and 1.0 represents the maximum depth buffer value.</span></span> <span data-ttu-id="57815-184">最後，樣板圖元是由單一固定點值組成，而且在二進位點右邊沒有未指定的精確度。</span><span class="sxs-lookup"><span data-stu-id="57815-184">Finally, stencil pixels comprise a single fixed-point value, with unspecified precision to the right of the binary point.</span></span>

<span data-ttu-id="57815-185">在四個基本圖元類型上執行的圖元傳送作業如下所示：</span><span class="sxs-lookup"><span data-stu-id="57815-185">The pixel transfer operations performed on the four basic pixel types are as follows:</span></span>



| <span data-ttu-id="57815-186">圖元類型</span><span class="sxs-lookup"><span data-stu-id="57815-186">Pixel type</span></span>  | <span data-ttu-id="57815-187">圖元傳送作業</span><span class="sxs-lookup"><span data-stu-id="57815-187">Pixel transfer operation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57815-188">Color</span><span class="sxs-lookup"><span data-stu-id="57815-188">Color</span></span>       | <span data-ttu-id="57815-189">四個色彩元件的每一個都乘以一個縮放因數，然後再加上偏差因數。</span><span class="sxs-lookup"><span data-stu-id="57815-189">Each of the four color components is multiplied by a scale factor, and then added to a bias factor.</span></span> <span data-ttu-id="57815-190">也就是說，紅色的元件會乘以 GL \_ red \_ scale，然後新增至 gl \_ 紅色 \_ 偏差; 綠色的元件會乘以 gl \_ 綠 \_ 級，然後新增至 gl \_ 綠色 \_ 偏差; 藍色元件會乘以 GL \_ 藍色 \_ 比例，然後再新增至 gl \_ blue \_ 偏差; Alpha 元件會乘以 gl \_ Alpha 小數位數，然後 \_ 再新增至 gl \_ Alpha \_ 偏差。</span><span class="sxs-lookup"><span data-stu-id="57815-190">That is, the red component is multiplied by GL\_RED\_SCALE, and then added to GL\_RED\_BIAS; the green component is multiplied by GL\_GREEN\_SCALE, and then added to GL\_GREEN\_BIAS; the blue component is multiplied by GL\_BLUE\_SCALE, and then added to GL\_BLUE\_BIAS; and the alpha component is multiplied by GL\_ALPHA\_SCALE, and then added to GL\_ALPHA\_BIAS.</span></span> <span data-ttu-id="57815-191">當四個色彩元件都經過縮放和偏誤之後，每個都壓制至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="57815-191">After all four color components are scaled and biased, each is clamped to the range \[0,1\].</span></span> <span data-ttu-id="57815-192">所有色階和偏差值都是使用 **glPixelTransfer** 來指定。</span><span class="sxs-lookup"><span data-stu-id="57815-192">All color scale and bias values are specified with **glPixelTransfer**.</span></span> <br/> <span data-ttu-id="57815-193">如果 GL \_ 地圖 \_ 色彩為 true，每個色彩元件都會依對應的色彩對應色彩來調整，然後由已調整的元件所索引的地圖內容取代。</span><span class="sxs-lookup"><span data-stu-id="57815-193">If GL\_MAP\_COLOR is true, each color component is scaled by the size of the corresponding color-to-color map, and then replaced by the contents of that map indexed by the scaled component.</span></span> <span data-ttu-id="57815-194">也就是說，紅色的元件會依照 GL \_ 圖元 \_ 地圖 \_ r 大小調整 \_ \_ \_ ，然後 \_ 以 gl 圖元地圖 r 的內容取代 \_ \_ \_ 為 \_ 其本身的索引。</span><span class="sxs-lookup"><span data-stu-id="57815-194">That is, the red component is scaled by GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE, and then replaced by the contents of GL\_PIXEL\_MAP\_R\_TO\_R indexed by itself.</span></span> <span data-ttu-id="57815-195">綠色的元件會依 GL \_ 圖元 \_ 地圖 \_ g 大小調整 \_ \_ \_ ，然後以 gl 圖元地圖 g 的內容取代 \_ \_ \_ \_ 為 \_ 其本身的索引。</span><span class="sxs-lookup"><span data-stu-id="57815-195">The green component is scaled by GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE, and then replaced by the contents of GL\_PIXEL\_MAP\_G\_TO\_G indexed by itself.</span></span> <span data-ttu-id="57815-196">藍色元件會依照 GL \_ 圖元 \_ 地圖 b 的 \_ \_ 大小調整為 \_ b \_ ，然後 \_ 以 gl 圖元地圖 b 的內容取代 \_ \_ \_ 為 b 的 \_ 索引。</span><span class="sxs-lookup"><span data-stu-id="57815-196">The blue component is scaled by GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE, and then replaced by the contents of GL\_PIXEL\_MAP\_B\_TO\_B indexed by itself.</span></span> <span data-ttu-id="57815-197">Alpha 元件會依照 GL \_ 圖元 \_ 地圖 a 調整 \_ \_ 為 \_ \_ 大小，然後以 gl 圖元地圖的內容取代為 \_ \_ \_ \_ \_ 索引。</span><span class="sxs-lookup"><span data-stu-id="57815-197">The alpha component is scaled by GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE, and then replaced by the contents of GL\_PIXEL\_MAP\_A\_TO\_A indexed by itself.</span></span> <span data-ttu-id="57815-198">從對應取得的所有元件都會壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="57815-198">All components taken from the maps are then clamped to the range \[0,1\].</span></span> <span data-ttu-id="57815-199">GL \_ 地圖 \_ 色彩是以 **glPixelTransfer** 指定的。</span><span class="sxs-lookup"><span data-stu-id="57815-199">GL\_MAP\_COLOR is specified with **glPixelTransfer**.</span></span> <span data-ttu-id="57815-200">不同對應的內容是以 **glPixelMap** 指定的。</span><span class="sxs-lookup"><span data-stu-id="57815-200">The contents of the various maps are specified with **glPixelMap**.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="57815-201">色彩索引</span><span class="sxs-lookup"><span data-stu-id="57815-201">Color index</span></span> | <span data-ttu-id="57815-202">每個色彩索引都會由 GL \_ 索引 \_ 移位位左移，填滿由固定點索引所送出之分數位數目以外的零。</span><span class="sxs-lookup"><span data-stu-id="57815-202">Each color index is shifted left by GL\_INDEX\_SHIFT bits, filling with zeros any bits beyond the number of fraction bits carried by the fixed-point index.</span></span> <span data-ttu-id="57815-203">如果 GL \_ 索引 \_ 移位是負數，則右移會再次填滿零。</span><span class="sxs-lookup"><span data-stu-id="57815-203">If GL\_INDEX\_SHIFT is negative, the shift is to the right, again zero filled.</span></span> <span data-ttu-id="57815-204">然後，會將 GL \_ 索引 \_ 位移新增至索引。</span><span class="sxs-lookup"><span data-stu-id="57815-204">GL\_INDEX\_OFFSET is then added to the index.</span></span> <span data-ttu-id="57815-205">GL \_ 索引 \_ 移位和 gl \_ 索引 \_ 位移會以 **glPixelTransfer** 指定。</span><span class="sxs-lookup"><span data-stu-id="57815-205">GL\_INDEX\_SHIFT and GL\_INDEX\_OFFSET are specified with **glPixelTransfer**.</span></span><br/> <span data-ttu-id="57815-206">從此時開始，作業分歧取決於所產生之圖元的必要格式。</span><span class="sxs-lookup"><span data-stu-id="57815-206">From this point, operation diverges depending on the required format of the resulting pixels.</span></span> <span data-ttu-id="57815-207">如果產生的圖元要寫入至色彩索引緩衝區，或將它們讀回 GL 色彩索引格式的用戶端記憶體 \_ \_ ，則會繼續將圖元視為索引。</span><span class="sxs-lookup"><span data-stu-id="57815-207">If the resulting pixels are to be written to a color-index buffer, or if they are being read back to client memory in GL\_COLOR\_INDEX format, the pixels continue to be treated as indexes.</span></span> <span data-ttu-id="57815-208">如果 GL \_ 對應 \_ 色彩為 true，則每個索引都會遮罩 2 ^ *n* 1，其中 *n* 是 gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i 的 \_ 大小，然後以 gl 圖元地圖的內容取代，並 \_ \_ \_ \_ 以 \_ 遮罩的值進行索引。</span><span class="sxs-lookup"><span data-stu-id="57815-208">If GL\_MAP\_COLOR is true, then each index is masked by 2 ^ *n* 1, where *n* is GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE, and then replaced by the contents of GL\_PIXEL\_MAP\_I\_TO\_I indexed by the masked value.</span></span> <span data-ttu-id="57815-209">GL \_ 地圖 \_ 色彩是以 **glPixelTransfer** 指定的。</span><span class="sxs-lookup"><span data-stu-id="57815-209">GL\_MAP\_COLOR is specified with **glPixelTransfer**.</span></span> <span data-ttu-id="57815-210">索引對應的內容是以 **glPixelMap** 指定的。</span><span class="sxs-lookup"><span data-stu-id="57815-210">The contents of the index map are specified with **glPixelMap**.</span></span><br/> <span data-ttu-id="57815-211">如果產生的圖元要寫入 RGBA 色彩緩衝區，或將其以 GL 色彩索引以外的格式讀回用戶端記憶體 \_ \_ ，則會參考四個 maps GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ R、GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ G、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ B，以及將 \_ i 圖元地圖移 \_ \_ \_ 至 \_ a，以從索引轉換為色彩。</span><span class="sxs-lookup"><span data-stu-id="57815-211">If the resulting pixels are to be written to an RGBA color buffer, or if they are being read back to client memory in a format other than GL\_COLOR\_INDEX, the pixels are converted from indexes to colors by referencing the four maps GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A.</span></span> <span data-ttu-id="57815-212">在進行取值之前，索引會由2個 n 1 遮罩，其中 n 是 GL \_ 圖元 \_ 對應 \_ i \_ 到 \_ 紅色地圖的 R \_ 大小、gl \_ 圖元地圖 i 至綠色地圖的大小、gl 圖元地圖 i 到 \_ B 的 \_ \_ \_ \_ \_ 藍色地圖大小， \_ \_ \_ \_ \_ 以及 gl \_ 圖元 \_ 地圖 \_ i \_ 至 \_ \_ Alpha 地圖的大小。</span><span class="sxs-lookup"><span data-stu-id="57815-212">Before being dereferenced, the index is masked by 2 n 1, where n is GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE for the red map, GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE for the green map, GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE for the blue map, and GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE for the alpha map.</span></span> <span data-ttu-id="57815-213">從對應取得的所有元件都會壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="57815-213">All components taken from the maps are then clamped to the range \[0,1\].</span></span> <span data-ttu-id="57815-214">四個對應的內容是以 **glPixelMap** 指定的。</span><span class="sxs-lookup"><span data-stu-id="57815-214">The contents of the four maps are specified with **glPixelMap**.</span></span><br/> |
| <span data-ttu-id="57815-215">深度</span><span class="sxs-lookup"><span data-stu-id="57815-215">Depth</span></span>       | <span data-ttu-id="57815-216">每個深度值乘以 GL \_ 深度 \_ 比例、新增至 GL \_ 深度 \_ 偏差，然後壓制至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="57815-216">Each depth value is multiplied by GL\_DEPTH\_SCALE, added to GL\_DEPTH\_BIAS, and then clamped to the range \[0,1\].</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="57815-217">樣板</span><span class="sxs-lookup"><span data-stu-id="57815-217">Stencil</span></span>     | <span data-ttu-id="57815-218">每個索引都會改 \_ 為將 GL 索引 \_ 移位位移位，如同色彩索引為，然後新增至 GL \_ 索引 \_ 位移。</span><span class="sxs-lookup"><span data-stu-id="57815-218">Each index is shifted GL\_INDEX\_SHIFT bits just as a color index is, and then added to GL\_INDEX\_OFFSET.</span></span> <span data-ttu-id="57815-219">如果 GL \_ 對應樣板 \_ 為 true，則每個索引都會由 2n 1 遮罩，其中 *n* 是 gl \_ 圖元 \_ 地圖 \_ s \_ 到 \_ s \_ 大小，然後 \_ \_ \_ \_ 以 \_ 由遮罩值所編制索引之 gl 圖元地圖的內容取代。</span><span class="sxs-lookup"><span data-stu-id="57815-219">If GL\_MAP\_STENCIL is true, each index is masked by 2n 1, where *n* is GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE, then replaced by the contents of GL\_PIXEL\_MAP\_S\_TO\_S indexed by the masked value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="57815-220">[**GlPixelTransferf**](glpixeltransfer.md)函式可以用來設定任何圖元傳輸參數。</span><span class="sxs-lookup"><span data-stu-id="57815-220">The [**glPixelTransferf**](glpixeltransfer.md) function can be used to set any pixel transfer parameter.</span></span> <span data-ttu-id="57815-221">如果參數類型為布林值，0.0 表示 false，而任何其他值則表示 true。</span><span class="sxs-lookup"><span data-stu-id="57815-221">If the parameter type is Boolean, 0.0 implies false and any other value implies true.</span></span> <span data-ttu-id="57815-222">如果 *pname* 是整數參數，則會將 *param* 四捨五入至最接近的整數。</span><span class="sxs-lookup"><span data-stu-id="57815-222">If *pname* is an integer parameter, *param* is rounded to the nearest integer.</span></span>

<span data-ttu-id="57815-223">同樣地， **glPixelTransferi** 也可以用來設定任何圖元傳輸參數。</span><span class="sxs-lookup"><span data-stu-id="57815-223">Likewise, **glPixelTransferi** can also be used to set any of the pixel transfer parameters.</span></span> <span data-ttu-id="57815-224">如果 *param* 為0，則布林參數設定為 false，否則為 true。</span><span class="sxs-lookup"><span data-stu-id="57815-224">Boolean parameters are set to false if *param* is 0 and true otherwise.</span></span> <span data-ttu-id="57815-225">*Param* 參數在指派給實值參數之前，會先轉換成浮點數。</span><span class="sxs-lookup"><span data-stu-id="57815-225">The *param* parameter is converted to floating point before being assigned to real-valued parameters.</span></span>

<span data-ttu-id="57815-226">如果 [ [**glDrawPixels**](gldrawpixels.md)]、[ [**glReadPixels**](glreadpixels.md)]、[ [**glCopyPixels**](glcopypixels.md)]、[ [**glTexImage1D**](glteximage1d.md)] 或 [ [**glTexImage2D**](glteximage2d.md) ] 命令都放在顯示清單中 (請參閱 [**glNewList**](glnewlist.md) 和 [**glCallList**](glcalllist.md)) ， *執行* 顯示清單時生效的圖元傳輸模式設定就是所使用的值。</span><span class="sxs-lookup"><span data-stu-id="57815-226">If a [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md), or [**glTexImage2D**](glteximage2d.md) command is placed in a display list (see [**glNewList**](glnewlist.md) and [**glCallList**](glcalllist.md)), the pixel transfer mode settings in effect when the display list is *executed* are the ones that are used.</span></span> <span data-ttu-id="57815-227">當命令編譯到顯示清單中時，它們可能會與設定不同。</span><span class="sxs-lookup"><span data-stu-id="57815-227">They may be different from the settings when the command was compiled into the display list.</span></span>

<span data-ttu-id="57815-228">下列函式會取出與 **glPixelTransfer** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="57815-228">The following functions retrieve information related to **glPixelTransfer**:</span></span>

<span data-ttu-id="57815-229">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 對應 \_ 色彩的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-229">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP\_COLOR</span></span>

<span data-ttu-id="57815-230">具有引數 GL 對應樣板的 **glGet** \_ \_</span><span class="sxs-lookup"><span data-stu-id="57815-230">**glGet** with argument GL\_MAP\_STENCIL</span></span>

<span data-ttu-id="57815-231">具有引數 GL \_ 索引 \_ 移位的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-231">**glGet** with argument GL\_INDEX\_SHIFT</span></span>

<span data-ttu-id="57815-232">具有引數 GL \_ 索引 \_ 位移的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-232">**glGet** with argument GL\_INDEX\_OFFSET</span></span>

<span data-ttu-id="57815-233">具有引數 GL \_ RED \_ SCALE 的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-233">**glGet** with argument GL\_RED\_SCALE</span></span>

<span data-ttu-id="57815-234">具有引數 GL \_ 紅色 \_ 偏差的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-234">**glGet** with argument GL\_RED\_BIAS</span></span>

<span data-ttu-id="57815-235">具有引數 GL \_ 綠 \_ 級的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-235">**glGet** with argument GL\_GREEN\_SCALE</span></span>

<span data-ttu-id="57815-236">**glGet** 與引數 GL \_ 綠色 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-236">**glGet** with argument GL\_GREEN\_BIAS</span></span>

<span data-ttu-id="57815-237">具有引數 GL \_ BLUE \_ SCALE 的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-237">**glGet** with argument GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="57815-238">**glGet** 與引數 GL \_ 藍色 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-238">**glGet** with argument GL\_BLUE\_BIAS</span></span>

<span data-ttu-id="57815-239">具有引數 GL \_ ALPHA \_ 刻度的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-239">**glGet** with argument GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="57815-240">**glGet** 與引數 GL \_ ALPHA \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="57815-240">**glGet** with argument GL\_ALPHA\_BIAS</span></span>

<span data-ttu-id="57815-241">具有引數 GL \_ 深度 \_ 比例的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-241">**glGet** with argument GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="57815-242">具有引數 GL \_ 深度 \_ 偏差的 glGet</span><span class="sxs-lookup"><span data-stu-id="57815-242">**glGet** with argument GL\_DEPTH\_BIAS</span></span>

## <a name="requirements"></a><span data-ttu-id="57815-243">規格需求</span><span class="sxs-lookup"><span data-stu-id="57815-243">Requirements</span></span>



| <span data-ttu-id="57815-244">需求</span><span class="sxs-lookup"><span data-stu-id="57815-244">Requirement</span></span> | <span data-ttu-id="57815-245">值</span><span class="sxs-lookup"><span data-stu-id="57815-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57815-246">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57815-246">Minimum supported client</span></span><br/> | <span data-ttu-id="57815-247">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57815-247">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="57815-248">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57815-248">Minimum supported server</span></span><br/> | <span data-ttu-id="57815-249">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57815-249">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57815-250">標頭</span><span class="sxs-lookup"><span data-stu-id="57815-250">Header</span></span><br/>                   | <dl> <span data-ttu-id="57815-251"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="57815-251"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="57815-252">程式庫</span><span class="sxs-lookup"><span data-stu-id="57815-252">Library</span></span><br/>                  | <dl> <span data-ttu-id="57815-253"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="57815-253"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="57815-254">DLL</span><span class="sxs-lookup"><span data-stu-id="57815-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57815-255"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57815-255"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57815-256">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57815-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57815-257">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="57815-257">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="57815-258">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="57815-258">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="57815-259">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="57815-259">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="57815-260">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="57815-260">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="57815-261">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="57815-261">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="57815-262">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="57815-262">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="57815-263">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="57815-263">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="57815-264">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="57815-264">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="57815-265">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="57815-265">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="57815-266">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="57815-266">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="57815-267">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="57815-267">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="57815-268">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="57815-268">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





