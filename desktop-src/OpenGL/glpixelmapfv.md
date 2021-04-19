---
title: 'glPixelMapfv 函式 (Gl) '
description: GlPixelMapfv 函式會設定圖元傳輸對應。
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- glPixelMapfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97124eeca8051ec23d9a4fea03a98468d320af8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968388"
---
# <a name="glpixelmapfv-function"></a><span data-ttu-id="b3461-104">glPixelMapfv 函式</span><span class="sxs-lookup"><span data-stu-id="b3461-104">glPixelMapfv function</span></span>

<span data-ttu-id="b3461-105">**GlPixelMapfv** 函式會設定圖元傳輸對應。</span><span class="sxs-lookup"><span data-stu-id="b3461-105">The **glPixelMapfv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3461-106">語法</span><span class="sxs-lookup"><span data-stu-id="b3461-106">Syntax</span></span>


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a><span data-ttu-id="b3461-107">參數</span><span class="sxs-lookup"><span data-stu-id="b3461-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3461-108">*map*</span><span class="sxs-lookup"><span data-stu-id="b3461-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="b3461-109">符號對應名稱。</span><span class="sxs-lookup"><span data-stu-id="b3461-109">A symbolic map name.</span></span> <span data-ttu-id="b3461-110">十個地圖如下所示。</span><span class="sxs-lookup"><span data-stu-id="b3461-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="b3461-111">值</span><span class="sxs-lookup"><span data-stu-id="b3461-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="b3461-112">意義</span><span class="sxs-lookup"><span data-stu-id="b3461-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="b3461-113"><dt>**GL \_ 圖元 \_ 對應 \_ I \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="b3461-114">將色彩索引對應至色彩索引。</span><span class="sxs-lookup"><span data-stu-id="b3461-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="b3461-115"><dt>**GL \_ 圖元 \_ 地圖 \_ S \_ 到 \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="b3461-116">將樣板索引對應至樣板索引。</span><span class="sxs-lookup"><span data-stu-id="b3461-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="b3461-117"><dt>**GL \_ 圖元 \_ 對應 \_ I \_ 到 \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="b3461-118">將色彩索引對應至紅色元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="b3461-119"><dt>**GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="b3461-120">將色彩索引對應至綠色元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="b3461-121"><dt>**GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="b3461-122">將色彩索引對應至藍色元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="b3461-123"><dt>**GL \_ 圖元 \_ 對應 \_ I \_ 到 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="b3461-124">將色彩索引對應至 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="b3461-125"><dt>**GL \_ 圖元 \_ 地圖 \_ R \_ 至 \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="b3461-126">將紅色元件對應至紅色元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="b3461-127"><dt>**GL \_ 圖元 \_ 地圖 \_ G \_ 至 \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="b3461-128">將綠色元件對應至綠色元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="b3461-129"><dt>**GL \_ 圖元 \_ 地圖 \_ B \_ 到 \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="b3461-130">將藍色元件對應至藍色元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="b3461-131"><dt>**GL \_ 圖元 \_ 將 \_ A 對應 \_ 至 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="b3461-132">將 Alpha 元件對應至 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="b3461-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b3461-133">*mapsize*</span><span class="sxs-lookup"><span data-stu-id="b3461-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="b3461-134">要定義之對應的大小。</span><span class="sxs-lookup"><span data-stu-id="b3461-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="b3461-135">*值*</span><span class="sxs-lookup"><span data-stu-id="b3461-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="b3461-136">*Mapsize* 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="b3461-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3461-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3461-137">Return value</span></span>

<span data-ttu-id="b3461-138">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b3461-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3461-139">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b3461-139">Error codes</span></span>

<span data-ttu-id="b3461-140">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3461-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b3461-141">Name</span><span class="sxs-lookup"><span data-stu-id="b3461-141">Name</span></span>                                                                                                  | <span data-ttu-id="b3461-142">意義</span><span class="sxs-lookup"><span data-stu-id="b3461-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3461-143"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3461-144">*地圖* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="b3461-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="b3461-145"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b3461-146">*mapsize* 是負數或大於 GL \_ 圖元 \_ 地圖 \_ 資料表。</span><span class="sxs-lookup"><span data-stu-id="b3461-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="b3461-147"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b3461-148">*map* was GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i、GL \_ 圖元 \_ map \_ s \_ 到 \_ s、gl \_ 圖元 \_ map \_ i \_ 到 \_ R、gl \_ 圖元 \_ map \_ i \_ 到 \_ G、gl 圖元 map i 到 B、gl 圖元 map i 至 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ a、 *mapsize* 不是2的乘冪。</span><span class="sxs-lookup"><span data-stu-id="b3461-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="b3461-149"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b3461-150">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="b3461-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="b3461-151">備註</span><span class="sxs-lookup"><span data-stu-id="b3461-151">Remarks</span></span>

<span data-ttu-id="b3461-152">**GlPixelMap** 函數會設定 [**glCopyPixels**](glcopypixels.md)、 [**glCopyTexImage1D**](glcopyteximage1d.md)、 [**glCopyTexImage2D**](glcopyteximage2d.md)、 [**glCopyTexSubImage1D**](glcopytexsubimage1d.md)、 [**glCopyTexSubImage2D、glDrawPixels**](glcopytexsubimage2d.md) [**、**](gldrawpixels.md) [**glReadPixels**](glreadpixels.md) [**、glTexImage1D、**](glteximage1d.md) [**glTexImage2D**](glteximage2d.md)、glTexSubImage1D 和 [**glTexSubImage2D**](gltexsubimage2d.md)所使用的轉譯資料表或 [](gltexsubimage1d.md)*對應*。</span><span class="sxs-lookup"><span data-stu-id="b3461-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="b3461-153">這些對應的使用會在 [**glPixelTransfer**](glpixeltransfer.md) 主題中完整描述，部分位於圖元和材質影像命令的主題中。</span><span class="sxs-lookup"><span data-stu-id="b3461-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="b3461-154">本主題只會說明對應的規格。</span><span class="sxs-lookup"><span data-stu-id="b3461-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="b3461-155">*Map* 參數是符號對應名稱，表示要設定的十個地圖中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="b3461-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="b3461-156">*Mapsize* 參數會指定地圖中的專案數，而 *值* 則是 *mapsize* 對應值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="b3461-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="b3461-157">地圖中的專案可以指定為單精確度浮點數、不帶正負號的短整數或不帶正負號的長整數。</span><span class="sxs-lookup"><span data-stu-id="b3461-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="b3461-158">將色彩元件值儲存 (所有的對應，但 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i 和 gl 圖元的對應 \_ \_ \_ s \_ \_) 以浮點數格式保留其值，並具有未指定的尾數和指數大小。</span><span class="sxs-lookup"><span data-stu-id="b3461-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="b3461-159">[**GlPixelMapfv**](glpixelmap.md)所指定的浮點值會直接轉換成這些對應的內部浮點格式，然後壓制至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="b3461-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="b3461-160">**GlPixelMapusv** 和 **glPixelMapuiv** 指定的不帶正負號的整數值會以線性方式轉換，使可代表的最大整數對應到1.0，而零對應到0.0。</span><span class="sxs-lookup"><span data-stu-id="b3461-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="b3461-161">儲存索引、GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i 和 GL 圖元圖元地圖的地圖會以 \_ \_ \_ \_ \_ 固定點格式保留其值，並在二進位點右邊指定不指定的位數。</span><span class="sxs-lookup"><span data-stu-id="b3461-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="b3461-162">[**GlPixelMapfv**](glpixelmap.md)所指定的浮點值會直接轉換成這些對應的內部固定點格式。</span><span class="sxs-lookup"><span data-stu-id="b3461-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="b3461-163">**GlPixelMapusv** 和 **glPixelMapuiv** 指定的不帶正負號的整數值會指定整數值，並在二進位點的右邊加上零。</span><span class="sxs-lookup"><span data-stu-id="b3461-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="b3461-164">下表顯示每個對應的初始大小和值。</span><span class="sxs-lookup"><span data-stu-id="b3461-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="b3461-165">以色彩或樣板索引編制索引的地圖必須有 *mapsize* = 2 ^ *n* ，部分 *n* 或結果未定義。</span><span class="sxs-lookup"><span data-stu-id="b3461-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="b3461-166">每個對應的允許大小上限取決於執行，而且可以藉由呼叫 **glGet** 與引數 GL \_ 最大 \_ 圖元 \_ 地圖 \_ 表格來判斷。</span><span class="sxs-lookup"><span data-stu-id="b3461-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="b3461-167">單一最大值適用于所有對應，且至少為32。</span><span class="sxs-lookup"><span data-stu-id="b3461-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="b3461-168">對應</span><span class="sxs-lookup"><span data-stu-id="b3461-168">Map</span></span>                      | <span data-ttu-id="b3461-169">查閱索引</span><span class="sxs-lookup"><span data-stu-id="b3461-169">Lookup Index</span></span>  | <span data-ttu-id="b3461-170">查閱值</span><span class="sxs-lookup"><span data-stu-id="b3461-170">Lookup Value</span></span>  | <span data-ttu-id="b3461-171">初始大小</span><span class="sxs-lookup"><span data-stu-id="b3461-171">Initial Size</span></span> | <span data-ttu-id="b3461-172">初始值</span><span class="sxs-lookup"><span data-stu-id="b3461-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="b3461-173">GL \_ 圖元 \_ 對應 \_ I \_ \_</span><span class="sxs-lookup"><span data-stu-id="b3461-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="b3461-174">色彩索引</span><span class="sxs-lookup"><span data-stu-id="b3461-174">color index</span></span>   | <span data-ttu-id="b3461-175">色彩索引</span><span class="sxs-lookup"><span data-stu-id="b3461-175">color index</span></span>   | <span data-ttu-id="b3461-176">1</span><span class="sxs-lookup"><span data-stu-id="b3461-176">1</span></span>            | <span data-ttu-id="b3461-177">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-177">0.0</span></span>           |
| <span data-ttu-id="b3461-178">GL \_ 圖元 \_ 地圖 \_ S \_ 到 \_ S</span><span class="sxs-lookup"><span data-stu-id="b3461-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="b3461-179">樣板索引</span><span class="sxs-lookup"><span data-stu-id="b3461-179">stencil index</span></span> | <span data-ttu-id="b3461-180">樣板索引</span><span class="sxs-lookup"><span data-stu-id="b3461-180">stencil index</span></span> | <span data-ttu-id="b3461-181">1</span><span class="sxs-lookup"><span data-stu-id="b3461-181">1</span></span>            | <span data-ttu-id="b3461-182">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-182">0.0</span></span>           |
| <span data-ttu-id="b3461-183">GL \_ 圖元 \_ 對應 \_ I \_ 到 \_ R</span><span class="sxs-lookup"><span data-stu-id="b3461-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="b3461-184">色彩索引</span><span class="sxs-lookup"><span data-stu-id="b3461-184">color index</span></span>   | <span data-ttu-id="b3461-185">R</span><span class="sxs-lookup"><span data-stu-id="b3461-185">R</span></span>             | <span data-ttu-id="b3461-186">1</span><span class="sxs-lookup"><span data-stu-id="b3461-186">1</span></span>            | <span data-ttu-id="b3461-187">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-187">0.0</span></span>           |
| <span data-ttu-id="b3461-188">GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G</span><span class="sxs-lookup"><span data-stu-id="b3461-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="b3461-189">色彩索引</span><span class="sxs-lookup"><span data-stu-id="b3461-189">color index</span></span>   | <span data-ttu-id="b3461-190">G</span><span class="sxs-lookup"><span data-stu-id="b3461-190">G</span></span>             | <span data-ttu-id="b3461-191">1</span><span class="sxs-lookup"><span data-stu-id="b3461-191">1</span></span>            | <span data-ttu-id="b3461-192">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-192">0.0</span></span>           |
| <span data-ttu-id="b3461-193">GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ B</span><span class="sxs-lookup"><span data-stu-id="b3461-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="b3461-194">色彩索引</span><span class="sxs-lookup"><span data-stu-id="b3461-194">color index</span></span>   | <span data-ttu-id="b3461-195">B</span><span class="sxs-lookup"><span data-stu-id="b3461-195">B</span></span>             | <span data-ttu-id="b3461-196">1</span><span class="sxs-lookup"><span data-stu-id="b3461-196">1</span></span>            | <span data-ttu-id="b3461-197">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-197">0.0</span></span>           |
| <span data-ttu-id="b3461-198">GL \_ 圖元 \_ 對應 \_ I \_ 到 \_</span><span class="sxs-lookup"><span data-stu-id="b3461-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="b3461-199">色彩索引</span><span class="sxs-lookup"><span data-stu-id="b3461-199">color index</span></span>   | <span data-ttu-id="b3461-200">A</span><span class="sxs-lookup"><span data-stu-id="b3461-200">A</span></span>             | <span data-ttu-id="b3461-201">1</span><span class="sxs-lookup"><span data-stu-id="b3461-201">1</span></span>            | <span data-ttu-id="b3461-202">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-202">0.0</span></span>           |
| <span data-ttu-id="b3461-203">GL \_ 圖元 \_ 地圖 \_ R \_ 至 \_ R</span><span class="sxs-lookup"><span data-stu-id="b3461-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="b3461-204">R</span><span class="sxs-lookup"><span data-stu-id="b3461-204">R</span></span>             | <span data-ttu-id="b3461-205">R</span><span class="sxs-lookup"><span data-stu-id="b3461-205">R</span></span>             | <span data-ttu-id="b3461-206">1</span><span class="sxs-lookup"><span data-stu-id="b3461-206">1</span></span>            | <span data-ttu-id="b3461-207">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-207">0.0</span></span>           |
| <span data-ttu-id="b3461-208">GL \_ 圖元 \_ 地圖 \_ G \_ 至 \_ G</span><span class="sxs-lookup"><span data-stu-id="b3461-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="b3461-209">G</span><span class="sxs-lookup"><span data-stu-id="b3461-209">G</span></span>             | <span data-ttu-id="b3461-210">G</span><span class="sxs-lookup"><span data-stu-id="b3461-210">G</span></span>             | <span data-ttu-id="b3461-211">1</span><span class="sxs-lookup"><span data-stu-id="b3461-211">1</span></span>            | <span data-ttu-id="b3461-212">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-212">0.0</span></span>           |
| <span data-ttu-id="b3461-213">GL \_ 圖元 \_ 地圖 \_ B \_ 到 \_ B</span><span class="sxs-lookup"><span data-stu-id="b3461-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="b3461-214">B</span><span class="sxs-lookup"><span data-stu-id="b3461-214">B</span></span>             | <span data-ttu-id="b3461-215">B</span><span class="sxs-lookup"><span data-stu-id="b3461-215">B</span></span>             | <span data-ttu-id="b3461-216">1</span><span class="sxs-lookup"><span data-stu-id="b3461-216">1</span></span>            | <span data-ttu-id="b3461-217">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-217">0.0</span></span>           |
| <span data-ttu-id="b3461-218">GL \_ 圖元 \_ 將 \_ A 對應 \_ 至 \_</span><span class="sxs-lookup"><span data-stu-id="b3461-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="b3461-219">A</span><span class="sxs-lookup"><span data-stu-id="b3461-219">A</span></span>             | <span data-ttu-id="b3461-220">A</span><span class="sxs-lookup"><span data-stu-id="b3461-220">A</span></span>             | <span data-ttu-id="b3461-221">1</span><span class="sxs-lookup"><span data-stu-id="b3461-221">1</span></span>            | <span data-ttu-id="b3461-222">0.0</span><span class="sxs-lookup"><span data-stu-id="b3461-222">0.0</span></span>           |



 

<span data-ttu-id="b3461-223">下列函式會取出與 **glPixelMap** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="b3461-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="b3461-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 圖元 \_ 對應 \_ 我 \_ 的 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b3461-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="b3461-225">將引數 GL \_ 圖元 \_ 對應 \_ \_ 到 \_ s \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="b3461-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="b3461-226">使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ R \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="b3461-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="b3461-227">使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="b3461-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="b3461-228">**glGet** 與引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 B 的 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b3461-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="b3461-229">**glGet** 與引數 GL \_ 圖元 \_ 對應 \_ I \_ 至 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b3461-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="b3461-230">使用引數 GL \_ 圖元 \_ 地圖 \_ r \_ 至 \_ r \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="b3461-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="b3461-231">具有引數 GL \_ 圖元 \_ 地圖 \_ g \_ 至 \_ g \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="b3461-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="b3461-232">具有引數 GL \_ 圖元 \_ 地圖 \_ b \_ 到 \_ b \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="b3461-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="b3461-233">具有引數 GL \_ 圖元 \_ 的 glGet 對應 \_ \_ 至 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b3461-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="b3461-234">具有引數 GL \_ 最大 \_ 圖元 \_ 地圖 \_ 資料表的 glGet</span><span class="sxs-lookup"><span data-stu-id="b3461-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="b3461-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3461-235">Requirements</span></span>



| <span data-ttu-id="b3461-236">需求</span><span class="sxs-lookup"><span data-stu-id="b3461-236">Requirement</span></span> | <span data-ttu-id="b3461-237">值</span><span class="sxs-lookup"><span data-stu-id="b3461-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3461-238">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3461-238">Minimum supported client</span></span><br/> | <span data-ttu-id="b3461-239">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3461-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3461-240">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3461-240">Minimum supported server</span></span><br/> | <span data-ttu-id="b3461-241">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3461-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3461-242">標頭</span><span class="sxs-lookup"><span data-stu-id="b3461-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3461-243"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3461-244">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3461-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3461-245"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3461-246">DLL</span><span class="sxs-lookup"><span data-stu-id="b3461-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3461-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3461-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3461-248">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3461-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3461-249">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b3461-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b3461-250">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="b3461-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="b3461-251">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="b3461-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b3461-252">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b3461-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b3461-253">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="b3461-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="b3461-254">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="b3461-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="b3461-255">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="b3461-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="b3461-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b3461-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b3461-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3461-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





