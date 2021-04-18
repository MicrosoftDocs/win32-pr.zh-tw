---
title: 'glGetTexImage 函式 (Gl) '
description: GlGetTexImage 函式會傳回材質影像。
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glGetTexImage 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968793"
---
# <a name="glgetteximage-function"></a><span data-ttu-id="85811-104">glGetTexImage 函式</span><span class="sxs-lookup"><span data-stu-id="85811-104">glGetTexImage function</span></span>

<span data-ttu-id="85811-105">**GlGetTexImage** 函式會傳回材質影像。</span><span class="sxs-lookup"><span data-stu-id="85811-105">The **glGetTexImage** function returns a texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="85811-106">語法</span><span class="sxs-lookup"><span data-stu-id="85811-106">Syntax</span></span>


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="85811-107">參數</span><span class="sxs-lookup"><span data-stu-id="85811-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85811-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="85811-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="85811-109">指定要取得的材質。</span><span class="sxs-lookup"><span data-stu-id="85811-109">Specifies which texture is to be obtained.</span></span> <span data-ttu-id="85811-110">\_ \_ 已接受 gl 材質1D 和 gl \_ 材質 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="85811-110">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="85811-111">*level*</span><span class="sxs-lookup"><span data-stu-id="85811-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="85811-112">所需影像的詳細層級編號。</span><span class="sxs-lookup"><span data-stu-id="85811-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="85811-113">層級0是基底映射層級。</span><span class="sxs-lookup"><span data-stu-id="85811-113">Level 0 is the base image level.</span></span> <span data-ttu-id="85811-114">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="85811-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="85811-115">*format*</span><span class="sxs-lookup"><span data-stu-id="85811-115">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="85811-116">傳回資料的像素格式。</span><span class="sxs-lookup"><span data-stu-id="85811-116">A pixel format for the returned data.</span></span> <span data-ttu-id="85811-117">支援的格式為 GL \_ RED、gl \_ 綠、gl \_ BLUE、GL \_ ALPHA、gl \_ RGB、gl \_ RGBA、gl \_ 亮度、gl \_ BGR \_ EXT、gl \_ BGRA \_ ext 和 gl \_ 亮度 \_ ALPHA。</span><span class="sxs-lookup"><span data-stu-id="85811-117">The supported formats are GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_LUMINANCE, GL\_BGR\_EXT, GL\_BGRA\_EXT, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="85811-118">*type*</span><span class="sxs-lookup"><span data-stu-id="85811-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="85811-119">傳回資料的圖元型別。</span><span class="sxs-lookup"><span data-stu-id="85811-119">A pixel type for the returned data.</span></span> <span data-ttu-id="85811-120">支援的類型為 GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、gl 不 \_ 帶正負號的 \_ SHORT、gl \_ short、gl 不 \_ 帶正負號 \_ int、gl \_ int 和 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="85811-120">The supported types are GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="85811-121">*圖元*</span><span class="sxs-lookup"><span data-stu-id="85811-121">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="85811-122">傳回材質影像。</span><span class="sxs-lookup"><span data-stu-id="85811-122">Returns the texture image.</span></span> <span data-ttu-id="85811-123">應為 *類型* 所指定之類型陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="85811-123">Should be a pointer to an array of the type specified by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85811-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="85811-124">Return value</span></span>

<span data-ttu-id="85811-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="85811-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="85811-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="85811-126">Error codes</span></span>

<span data-ttu-id="85811-127">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="85811-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="85811-128">Name</span><span class="sxs-lookup"><span data-stu-id="85811-128">Name</span></span>                                                                                                  | <span data-ttu-id="85811-129">意義</span><span class="sxs-lookup"><span data-stu-id="85811-129">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85811-130"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="85811-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="85811-131">*目標*、 *格式* 或 *類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="85811-131">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="85811-132"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="85811-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="85811-133">*層級* 小於零或大於 *log* 2 (*max*) ，其中 *max* 是 GL \_ 最大 \_ 紋理大小的傳回值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="85811-133">*level* is less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="85811-134"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="85811-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="85811-135">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md) 呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="85811-135">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) .</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="85811-136">備註</span><span class="sxs-lookup"><span data-stu-id="85811-136">Remarks</span></span>

<span data-ttu-id="85811-137">**GlGetTexImage** 函式會將材質影像傳回到 *圖元*。</span><span class="sxs-lookup"><span data-stu-id="85811-137">The **glGetTexImage** function returns a texture image into *pixels*.</span></span> <span data-ttu-id="85811-138">*目標* 參數會指定所需的材質影像是由 [**glTexImage1D**](glteximage1d.md) **(** GL \_ 材質 \_ 1d **)** 或 [**glTexImage2D**](glteximage2d.md) **(** GL \_ 材質 \_ 2d **)** 所指定。</span><span class="sxs-lookup"><span data-stu-id="85811-138">The *target* parameter specifies whether the desired texture image is one specified by [**glTexImage1D**](glteximage1d.md)**(** GL\_TEXTURE\_1D **)** or by [**glTexImage2D**](glteximage2d.md)**(** GL\_TEXTURE\_2D **)**.</span></span> <span data-ttu-id="85811-139">*Level* 參數會指定所需影像的詳細層級數目。</span><span class="sxs-lookup"><span data-stu-id="85811-139">The *level* parameter specifies the level-of-detail number of the desired image.</span></span> <span data-ttu-id="85811-140">*Format* 和 *type* 參數會指定所需影像陣列的格式和類型。</span><span class="sxs-lookup"><span data-stu-id="85811-140">The *format* and *type* parameters specify the format and type of the desired image array.</span></span> <span data-ttu-id="85811-141">如需適用于 *格式* 和 *類型* 參數的可接受值的描述，請參閱 **glTexImage1D** 和 [**glDrawPixels**](gldrawpixels.md)。</span><span class="sxs-lookup"><span data-stu-id="85811-141">For a description of the acceptable values for the *format* and *type* parameters, respectively, see **glTexImage1D** and [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="85811-142">將選取的內部四元件紋理影像視為映射大小的 RGBA 色彩緩衝區，可充分瞭解 **glGetTexImage** 的作業。</span><span class="sxs-lookup"><span data-stu-id="85811-142">Operation of **glGetTexImage** is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image.</span></span> <span data-ttu-id="85811-143">然後， **glGetTexImage** 的語義會與使用相同 *格式* 和 *類型* 呼叫的 [**glReadPixels**](glreadpixels.md)相同。如果 *x* 和 *y* 設定為零，則寬度設定為材質影像的寬度 (包括框線（如果有指定的話）) ，以及將 *寬度* 設定為 1-d 影像 *的高度，* 或是材質影像的高度（如果指定了2d 影像) ，則會包含框線）。 (</span><span class="sxs-lookup"><span data-stu-id="85811-143">The semantics of **glGetTexImage** are then identical to those of [**glReadPixels**](glreadpixels.md) called with the same *format* and *type*, with *x* and *y* set to zero, *width* set to the width of the texture image (including border if one was specified), and *height* set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.</span></span>

<span data-ttu-id="85811-144">因為內部紋理影像是 RGBA 影像，所以不接受像素格式的 GL \_ 色彩 \_ 索引、gl 樣板 \_ \_ 索引和 gl \_ 深度 \_ 元件，而且不接受圖元類型 gl \_ 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="85811-144">Because the internal texture image is an RGBA image, pixel formats GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, and GL\_DEPTH\_COMPONENT are not accepted, and pixel type GL\_BITMAP is not accepted.</span></span>

<span data-ttu-id="85811-145">如果選取的材質影像未包含四個元件，則會套用下列對應。</span><span class="sxs-lookup"><span data-stu-id="85811-145">If the selected texture image does not contain four components, the following mappings are applied.</span></span> <span data-ttu-id="85811-146">單一元件紋理會被視為 RGBA 緩衝區，並將紅色設定為單一元件值，綠色、藍色和 Alpha 設定為零。</span><span class="sxs-lookup"><span data-stu-id="85811-146">Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.</span></span>

<span data-ttu-id="85811-147">雙元件紋理會視為 RGBA 緩衝區，並將紅色設定為元件零的值、將 Alpha 設定為元件1的值，而綠色和藍色設定為零。</span><span class="sxs-lookup"><span data-stu-id="85811-147">Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero.</span></span> <span data-ttu-id="85811-148">最後，會將三個元件的材質視為 RGBA 緩衝區，並將紅色設定為 [元件零]、綠色設定為 [元件 1]、[藍色設定為第二個]、[Alpha] 設定為零。</span><span class="sxs-lookup"><span data-stu-id="85811-148">Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.</span></span>

<span data-ttu-id="85811-149">若要判斷所需的 *圖元* 大小，請使用 [**glGetTexLevelParameter**](glgettexlevelparameter.md) 來確定內部紋理影像的維度，然後根據 *格式* 和 *類型*，根據每個圖元所需的儲存體來調整所需的圖元數目。</span><span class="sxs-lookup"><span data-stu-id="85811-149">To determine the required size of *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on *format* and *type*.</span></span> <span data-ttu-id="85811-150">務必將圖元儲存體參數納入考慮，特別是 GL \_ 套件 \_ 對齊。</span><span class="sxs-lookup"><span data-stu-id="85811-150">Be sure to take the pixel-storage parameters into account, especially GL\_PACK\_ALIGNMENT.</span></span>

<span data-ttu-id="85811-151">如果產生錯誤，則不會對 *圖元* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="85811-151">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="85811-152">下列函式會取出與 **glGetTexImage** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="85811-152">The following functions retrieve information related to **glGetTexImage**:</span></span>

<span data-ttu-id="85811-153">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 套件 \_ 對齊和其他專案的 glGet</span><span class="sxs-lookup"><span data-stu-id="85811-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PACK\_ALIGNMENT and others</span></span>

<span data-ttu-id="85811-154">[](glgettexlevelparameter.md)具有引數 GL \_ 材質 \_ 寬度的 glGetTexLevelParameter</span><span class="sxs-lookup"><span data-stu-id="85811-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) with argument GL\_TEXTURE\_WIDTH</span></span>

<span data-ttu-id="85811-155">具有引數 GL \_ 材質 \_ 高度的 glGetTexLevelParameter</span><span class="sxs-lookup"><span data-stu-id="85811-155">**glGetTexLevelParameter** with argument GL\_TEXTURE\_HEIGHT</span></span>

<span data-ttu-id="85811-156">具有引數 GL \_ 紋理 \_ 框線的 glGetTexLevelParameter</span><span class="sxs-lookup"><span data-stu-id="85811-156">**glGetTexLevelParameter** with argument GL\_TEXTURE\_BORDER</span></span>

<span data-ttu-id="85811-157">具有引數 GL \_ 材質 \_ 元件的 glGetTexLevelParameter</span><span class="sxs-lookup"><span data-stu-id="85811-157">**glGetTexLevelParameter** with argument GL\_TEXTURE\_COMPONENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="85811-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="85811-158">Requirements</span></span>



| <span data-ttu-id="85811-159">需求</span><span class="sxs-lookup"><span data-stu-id="85811-159">Requirement</span></span> | <span data-ttu-id="85811-160">值</span><span class="sxs-lookup"><span data-stu-id="85811-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85811-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85811-161">Minimum supported client</span></span><br/> | <span data-ttu-id="85811-162">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85811-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="85811-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85811-163">Minimum supported server</span></span><br/> | <span data-ttu-id="85811-164">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85811-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="85811-165">標頭</span><span class="sxs-lookup"><span data-stu-id="85811-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="85811-166"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="85811-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="85811-167">程式庫</span><span class="sxs-lookup"><span data-stu-id="85811-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="85811-168"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="85811-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="85811-169">DLL</span><span class="sxs-lookup"><span data-stu-id="85811-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85811-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85811-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85811-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85811-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85811-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="85811-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="85811-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="85811-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="85811-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="85811-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="85811-175">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="85811-175">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="85811-176">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="85811-176">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="85811-177">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="85811-177">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="85811-178">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="85811-178">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





