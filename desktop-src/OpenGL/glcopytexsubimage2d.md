---
title: 'glCopyTexSubImage2D 函式 (Gl) '
description: GlCopyTexSubImage2D 函式會從畫面格緩衝區複製二維紋理影像的子影像。
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384818"
---
# <a name="glcopytexsubimage2d-function"></a><span data-ttu-id="9f61a-104">glCopyTexSubImage2D 函式</span><span class="sxs-lookup"><span data-stu-id="9f61a-104">glCopyTexSubImage2D function</span></span>

<span data-ttu-id="9f61a-105">**GlCopyTexSubImage2D** 函式會從畫面格緩衝區複製二維紋理影像的子影像。</span><span class="sxs-lookup"><span data-stu-id="9f61a-105">The **glCopyTexSubImage2D** function copies a sub-image of a two-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f61a-106">語法</span><span class="sxs-lookup"><span data-stu-id="9f61a-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="9f61a-107">參數</span><span class="sxs-lookup"><span data-stu-id="9f61a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f61a-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="9f61a-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-109">將變更影像資料的目標。</span><span class="sxs-lookup"><span data-stu-id="9f61a-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="9f61a-110">必須具有值 GL \_ 紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="9f61a-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="9f61a-111">*level*</span><span class="sxs-lookup"><span data-stu-id="9f61a-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-112">詳細資料層級數目。</span><span class="sxs-lookup"><span data-stu-id="9f61a-112">The level-of-detail number.</span></span> <span data-ttu-id="9f61a-113">層級0是基底映射。</span><span class="sxs-lookup"><span data-stu-id="9f61a-113">Level 0 is the base image.</span></span> <span data-ttu-id="9f61a-114">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="9f61a-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="9f61a-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="9f61a-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-116">紋理陣列內 *x* 方向的材質位移。</span><span class="sxs-lookup"><span data-stu-id="9f61a-116">The texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="9f61a-117">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="9f61a-117">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-118">紋理陣列中 *y* 方向的材質位移。</span><span class="sxs-lookup"><span data-stu-id="9f61a-118">The texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="9f61a-119">*x*</span><span class="sxs-lookup"><span data-stu-id="9f61a-119">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-120">要複製之圖元資料列左下角的視窗 x 平面座標。</span><span class="sxs-lookup"><span data-stu-id="9f61a-120">The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="9f61a-121">*y*</span><span class="sxs-lookup"><span data-stu-id="9f61a-121">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-122">要複製之圖元資料列左下角的視窗 y 平面座標。</span><span class="sxs-lookup"><span data-stu-id="9f61a-122">The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="9f61a-123">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="9f61a-123">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-124">材質影像的子影像寬度。</span><span class="sxs-lookup"><span data-stu-id="9f61a-124">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="9f61a-125">指定寬度為零的材質子影像沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9f61a-125">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="9f61a-126">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="9f61a-126">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="9f61a-127">材質影像子影像的高度。</span><span class="sxs-lookup"><span data-stu-id="9f61a-127">The height of the sub-image of the texture image.</span></span> <span data-ttu-id="9f61a-128">指定寬度為零的材質子影像沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9f61a-128">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f61a-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f61a-129">Return value</span></span>

<span data-ttu-id="9f61a-130">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9f61a-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9f61a-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9f61a-131">Error codes</span></span>

<span data-ttu-id="9f61a-132">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9f61a-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9f61a-133">Name</span><span class="sxs-lookup"><span data-stu-id="9f61a-133">Name</span></span>                                                                                                  | <span data-ttu-id="9f61a-134">意義</span><span class="sxs-lookup"><span data-stu-id="9f61a-134">Meaning</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f61a-135"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9f61a-136">*目標* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="9f61a-136">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="9f61a-137"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9f61a-138">*層級* 小於零或大於 *log* 2 (*max*) ，其中 *max* 是 GL \_ 最大 \_ 紋理大小的傳回值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9f61a-138">*level* was less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="9f61a-139"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-139"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9f61a-140">*xoffset* 小於 *框線* 或 (*xoffset*  +  *寬度*)  (大於框線  +  ) 、 *yoffset* 小於 *框線*，或 (*yoffset*  +  *高度*) 大於 (*h*  +  *框線*) ，其中 *w* 是 gl \_ 紋理 \_ 寬度和 *框線* 是 gl \_ 材質 \_ 框線。</span><span class="sxs-lookup"><span data-stu-id="9f61a-140">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), *yoffset* was less than *border*, or (*yoffset* + *height*) was greater than (*h* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="9f61a-141">請注意， *w* 包含 *框線* 寬度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="9f61a-141">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="9f61a-142"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-142"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9f61a-143">*寬度* 小於 *框線* 或 *y* 小於 *框線*，其中 *框線* 是材質陣列的框線寬度。</span><span class="sxs-lookup"><span data-stu-id="9f61a-143">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                           |
| <dl> <span data-ttu-id="9f61a-144"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-144"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9f61a-145">材質陣列未由先前的 [**glTexImage1D**](glteximage1d.md) 作業定義。</span><span class="sxs-lookup"><span data-stu-id="9f61a-145">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="9f61a-146"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-146"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9f61a-147">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="9f61a-147">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="9f61a-148">備註</span><span class="sxs-lookup"><span data-stu-id="9f61a-148">Remarks</span></span>

<span data-ttu-id="9f61a-149">**GlCopyTexSubImage2D** 函式會將二維材質影像的矩形部分取代為目前畫面格緩衝區的圖元，而不是從主儲存體（例如 [**glTexSubImage2D**](gltexsubimage2d.md)的情況下）。</span><span class="sxs-lookup"><span data-stu-id="9f61a-149">The **glCopyTexSubImage2D** function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage2D**](gltexsubimage2d.md).</span></span>

<span data-ttu-id="9f61a-150">以 *x* 和 *y* 視窗座標為開頭的圖元矩形，其維度 *寬度* 和 *高度* 會以 *xoffset* 至 *xoffset* + (*寬度* -1) 的索引來取代材質陣列的部分， *而索引則* 是透過 *yoffset* + (*寬度* -1) 在 *層級* 所指定的 mipmap 層級進行。</span><span class="sxs-lookup"><span data-stu-id="9f61a-150">A rectangle of pixels beginning with the *x* and *y* window coordinates and with the dimensions *width* and *height* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1), with the indexes *yoffset* through *yoffset* + (*width* - 1) at the mipmap level specified by *level*.</span></span> <span data-ttu-id="9f61a-151">紋理陣列中的目的地矩形不能包含原始指定之材質陣列以外的任何材質。</span><span class="sxs-lookup"><span data-stu-id="9f61a-151">The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="9f61a-152">**GlCopyTexSubImage2D** 函式會使用與 [**glCopyPixels**](glcopypixels.md)相同的方式來處理資料列中的圖元，但在圖元的最後轉換之前，所有圖元元件值都會壓制至範圍 \[ 0、1， \] 並轉換為紋理陣列中儲存的材質內部格式。</span><span class="sxs-lookup"><span data-stu-id="9f61a-152">The **glCopyTexSubImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="9f61a-153">圖元順序是以對應于較低材質座標的較低 *x* 座標來決定。</span><span class="sxs-lookup"><span data-stu-id="9f61a-153">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="9f61a-154">如果目前畫面格緩衝區中指定資料列內的任何圖元都在與目前轉譯內容相關聯的視窗之外，則其值為未定義。</span><span class="sxs-lookup"><span data-stu-id="9f61a-154">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="9f61a-155">如果目前畫面格緩衝區之指定矩形內的任何圖元都在與目前轉譯內容相關聯的讀取視窗之外，則為這些圖元取得的值未定義。</span><span class="sxs-lookup"><span data-stu-id="9f61a-155">If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined.</span></span> <span data-ttu-id="9f61a-156">不會變更指定之材質陣列的 *internalFormat*、 *width*、 *height* 或 *border* 參數，也不會材質指定之材質子影像以外的值。</span><span class="sxs-lookup"><span data-stu-id="9f61a-156">No change is made to the *internalFormat*, *width*, *height*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="9f61a-157">您不能在顯示清單中包含 **glCopyTexSubImage2D** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9f61a-157">You cannot include calls to **glCopyTexSubImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="9f61a-158">**GlCopyTexSubImage2D** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9f61a-158">The **glCopyTexSubImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="9f61a-159">紋理在色彩索引模式中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9f61a-159">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="9f61a-160">[**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)函式會以實際的方式影響材質影像，其影響使用 [**glDrawPixels**](gldrawpixels.md)繪製圖元的方式。</span><span class="sxs-lookup"><span data-stu-id="9f61a-160">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="9f61a-161">下列函式會取出與 **glCopyTexSubImage2D** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="9f61a-161">The following functions retrieve information related to **glCopyTexSubImage2D**:</span></span>

[<span data-ttu-id="9f61a-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="9f61a-162">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="9f61a-163">[](glisenabled.md)具有引數 GL \_ 材質 \_ 2d 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="9f61a-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="9f61a-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f61a-164">Requirements</span></span>



| <span data-ttu-id="9f61a-165">需求</span><span class="sxs-lookup"><span data-stu-id="9f61a-165">Requirement</span></span> | <span data-ttu-id="9f61a-166">值</span><span class="sxs-lookup"><span data-stu-id="9f61a-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f61a-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f61a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="9f61a-168">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f61a-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9f61a-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f61a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="9f61a-170">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f61a-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f61a-171">標頭</span><span class="sxs-lookup"><span data-stu-id="9f61a-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f61a-172"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9f61a-173">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f61a-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f61a-174"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f61a-175">DLL</span><span class="sxs-lookup"><span data-stu-id="9f61a-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f61a-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f61a-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f61a-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f61a-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f61a-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9f61a-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9f61a-179">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="9f61a-179">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="9f61a-180">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="9f61a-180">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="9f61a-181">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="9f61a-181">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="9f61a-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9f61a-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9f61a-183">**glFog**</span><span class="sxs-lookup"><span data-stu-id="9f61a-183">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="9f61a-184">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="9f61a-184">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="9f61a-185">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="9f61a-185">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="9f61a-186">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="9f61a-186">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="9f61a-187">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="9f61a-187">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="9f61a-188">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="9f61a-188">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="9f61a-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="9f61a-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="9f61a-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="9f61a-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





