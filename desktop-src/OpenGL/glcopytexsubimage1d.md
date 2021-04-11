---
title: 'glCopyTexSubImage1D 函式 (Gl) '
description: GlCopyTexSubImage1D 函式會從畫面格緩衝區複製一維材質影像的子影像。
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- glCopyTexSubImage1D 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934608"
---
# <a name="glcopytexsubimage1d-function"></a><span data-ttu-id="77689-104">glCopyTexSubImage1D 函式</span><span class="sxs-lookup"><span data-stu-id="77689-104">glCopyTexSubImage1D function</span></span>

<span data-ttu-id="77689-105">**GlCopyTexSubImage1D** 函式會從畫面格緩衝區複製一維材質影像的子影像。</span><span class="sxs-lookup"><span data-stu-id="77689-105">The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="77689-106">語法</span><span class="sxs-lookup"><span data-stu-id="77689-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a><span data-ttu-id="77689-107">參數</span><span class="sxs-lookup"><span data-stu-id="77689-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77689-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="77689-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="77689-109">將變更影像資料的目標。</span><span class="sxs-lookup"><span data-stu-id="77689-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="77689-110">必須具有值 GL \_ 紋理 \_ 1d。</span><span class="sxs-lookup"><span data-stu-id="77689-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="77689-111">*level*</span><span class="sxs-lookup"><span data-stu-id="77689-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="77689-112">詳細資料層級數目。</span><span class="sxs-lookup"><span data-stu-id="77689-112">The level-of-detail number.</span></span> <span data-ttu-id="77689-113">層級0是基底映射。</span><span class="sxs-lookup"><span data-stu-id="77689-113">Level 0 is the base image.</span></span> <span data-ttu-id="77689-114">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="77689-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="77689-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="77689-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="77689-116">紋理陣列內的材質位移。</span><span class="sxs-lookup"><span data-stu-id="77689-116">The texel offset within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="77689-117">*x*</span><span class="sxs-lookup"><span data-stu-id="77689-117">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="77689-118">要複製之圖元資料列左下角的視窗 x 平面座標。</span><span class="sxs-lookup"><span data-stu-id="77689-118">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="77689-119">*y*</span><span class="sxs-lookup"><span data-stu-id="77689-119">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="77689-120">要複製之圖元資料列左下角的視窗 y 平面座標。</span><span class="sxs-lookup"><span data-stu-id="77689-120">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="77689-121">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="77689-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="77689-122">材質影像的子影像寬度。</span><span class="sxs-lookup"><span data-stu-id="77689-122">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="77689-123">指定寬度為零的材質子影像沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="77689-123">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77689-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="77689-124">Return value</span></span>

<span data-ttu-id="77689-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="77689-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77689-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="77689-126">Error codes</span></span>

<span data-ttu-id="77689-127">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="77689-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="77689-128">Name</span><span class="sxs-lookup"><span data-stu-id="77689-128">Name</span></span>                                                                                                  | <span data-ttu-id="77689-129">意義</span><span class="sxs-lookup"><span data-stu-id="77689-129">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77689-130"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="77689-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="77689-131">*目標* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="77689-131">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="77689-132"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="77689-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77689-133">*層級* 小於零，或 *層級* 大於 *log* 2 (*max*) ，其中 *max* 是 GL \_ 最大 \_ 紋理大小的傳回值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="77689-133">*level* was less than zero or *level* is greater than *log* 2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="77689-134"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="77689-134"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77689-135">*xoffset* 小於 *框線* 或 (*xoffset*  +  *寬度*) 大於  +  *框線*) 的 (，其中 *w* 是 gl \_ 紋理 \_ 寬度，而 *框線* 是 gl \_ 材質 \_ 框線。</span><span class="sxs-lookup"><span data-stu-id="77689-135">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="77689-136">請注意， *w* 包含 *框線* 寬度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="77689-136">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="77689-137"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="77689-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77689-138">*寬度* 小於 *框線* 或 *y* 小於 *框線*，其中 *框線* 是材質陣列的框線寬度。</span><span class="sxs-lookup"><span data-stu-id="77689-138">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="77689-139"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="77689-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77689-140">材質陣列未由先前的 [**glTexImage1D**](glteximage1d.md) 作業定義。</span><span class="sxs-lookup"><span data-stu-id="77689-140">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="77689-141"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="77689-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77689-142">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="77689-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                        |



## <a name="remarks"></a><span data-ttu-id="77689-143">備註</span><span class="sxs-lookup"><span data-stu-id="77689-143">Remarks</span></span>

<span data-ttu-id="77689-144">**GlCopyTexSubImage1D** 函式會使用目前畫面格緩衝區的圖元來取代一維材質影像的一部分，而不是從主儲存體（例如 [**glTexSubImage1D**](gltexsubimage1d.md)的情況下）。</span><span class="sxs-lookup"><span data-stu-id="77689-144">The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).</span></span>

<span data-ttu-id="77689-145">以 *x* 和 *y* 指定的視窗座標為開頭的資料列，且其長度 *寬度* 會以 *xoffset* 至 *xoffset* + (*寬度* -1) 的索引來取代材質陣列的部分。</span><span class="sxs-lookup"><span data-stu-id="77689-145">A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1).</span></span> <span data-ttu-id="77689-146">材質陣列中的目的地無法包含原始指定之材質陣列以外的任何材質。</span><span class="sxs-lookup"><span data-stu-id="77689-146">The destination in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="77689-147">**GlCopyTexSubImage1D** 函式會使用與 [**glCopyPixels**](glcopypixels.md)相同的方式來處理資料列中的圖元，但在最後轉換圖元之前，所有圖元元件值都會壓制至範圍 \[ 0、1， \] 並轉換成紋理陣列中儲存的材質內部格式。</span><span class="sxs-lookup"><span data-stu-id="77689-147">The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="77689-148">圖元順序是以對應于較低材質座標的較低 *x* 座標來決定。</span><span class="sxs-lookup"><span data-stu-id="77689-148">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="77689-149">如果目前畫面格緩衝區中指定資料列內的任何圖元都在與目前轉譯內容相關聯的視窗之外，則其值為未定義。</span><span class="sxs-lookup"><span data-stu-id="77689-149">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="77689-150">不會變更指定之材質陣列的 *internalFormat*、 *width* 或 *border* 參數，也不會材質指定之材質子影像以外的值。</span><span class="sxs-lookup"><span data-stu-id="77689-150">No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="77689-151">您不能在顯示清單中包含 **glCopyTexSubImage1D** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="77689-151">You cannot include calls to **glCopyTexSubImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="77689-152">**GlCopyTexSubImage1D** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="77689-152">The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="77689-153">紋理在色彩索引模式中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="77689-153">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="77689-154">[**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)函式會以實際的方式影響材質影像，其影響使用 [**glDrawPixels**](gldrawpixels.md)繪製圖元的方式。</span><span class="sxs-lookup"><span data-stu-id="77689-154">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="77689-155">下列函式會取出與 **glCopyTexSubImage1D** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="77689-155">The following functions retrieve information related to **glCopyTexSubImage1D**:</span></span>

[<span data-ttu-id="77689-156">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="77689-156">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="77689-157">[](glisenabled.md)具有引數 GL \_ 材質 \_ 1d 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="77689-157">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="77689-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="77689-158">Requirements</span></span>



| <span data-ttu-id="77689-159">需求</span><span class="sxs-lookup"><span data-stu-id="77689-159">Requirement</span></span> | <span data-ttu-id="77689-160">值</span><span class="sxs-lookup"><span data-stu-id="77689-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77689-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77689-161">Minimum supported client</span></span><br/> | <span data-ttu-id="77689-162">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77689-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77689-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77689-163">Minimum supported server</span></span><br/> | <span data-ttu-id="77689-164">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77689-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77689-165">標頭</span><span class="sxs-lookup"><span data-stu-id="77689-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="77689-166"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="77689-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="77689-167">程式庫</span><span class="sxs-lookup"><span data-stu-id="77689-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="77689-168"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="77689-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="77689-169">DLL</span><span class="sxs-lookup"><span data-stu-id="77689-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77689-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77689-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77689-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77689-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77689-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="77689-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77689-173">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="77689-173">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="77689-174">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="77689-174">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="77689-175">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="77689-175">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77689-176">**glFog**</span><span class="sxs-lookup"><span data-stu-id="77689-176">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="77689-177">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="77689-177">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="77689-178">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="77689-178">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="77689-179">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="77689-179">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="77689-180">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="77689-180">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="77689-181">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="77689-181">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="77689-182">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="77689-182">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="77689-183">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="77689-183">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="77689-184">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="77689-184">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="77689-185">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="77689-185">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





