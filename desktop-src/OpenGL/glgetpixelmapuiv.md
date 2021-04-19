---
title: 'glGetPixelMapuiv 函式 (Gl) '
description: 'GlGetPixelMapfv、glGetPixelMapuiv 和 glGetPixelMapusv 函數會傳回指定的圖元對應。 |glGetPixelMapuiv 函式 (Gl) '
ms.assetid: a49f5fd2-c350-4acc-8f61-ecb92b0164cc
keywords:
- glGetPixelMapuiv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c017e7601e074c588aa534b6ea90aef79325ed4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992677"
---
# <a name="glgetpixelmapuiv-function"></a><span data-ttu-id="664d2-105">glGetPixelMapuiv 函式</span><span class="sxs-lookup"><span data-stu-id="664d2-105">glGetPixelMapuiv function</span></span>

<span data-ttu-id="664d2-106">[**GlGetPixelMapfv**](glgetpixelmapfv.md)、 **glGetPixelMapuiv** 和 [**glGetPixelMapusv**](glgetpixelmapusv.md)函數會傳回指定的圖元對應。</span><span class="sxs-lookup"><span data-stu-id="664d2-106">The [**glGetPixelMapfv**](glgetpixelmapfv.md), **glGetPixelMapuiv**, and [**glGetPixelMapusv**](glgetpixelmapusv.md) functions return the specified pixel map.</span></span>

## <a name="syntax"></a><span data-ttu-id="664d2-107">語法</span><span class="sxs-lookup"><span data-stu-id="664d2-107">Syntax</span></span>


```C++
void WINAPI glGetPixelMapuiv(
   GLenum map,
   GLuint *values
);
```



## <a name="parameters"></a><span data-ttu-id="664d2-108">參數</span><span class="sxs-lookup"><span data-stu-id="664d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="664d2-109">*map*</span><span class="sxs-lookup"><span data-stu-id="664d2-109">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="664d2-110">要傳回的圖元對應名稱。</span><span class="sxs-lookup"><span data-stu-id="664d2-110">The name of the pixel map to return.</span></span> <span data-ttu-id="664d2-111">接受的值為 GL \_ 圖元 \_ 地圖 \_ i \_ 至 \_ i、gl \_ 圖元 \_ 地圖 \_ s \_ 、到 s、 \_ gl \_ 圖元 \_ 對應 \_ i \_ 到 \_ R、gl \_ 圖元 \_ 地圖 i 到 \_ \_ \_ G、gl 圖元對應 i \_ \_ \_ \_ 到 \_ b、gl 圖元對應 i 到 \_ \_ \_ \_ \_ a、gl 圖元地圖 \_ \_ \_ r \_ 至 R、 \_ gl 圖元地圖 \_ \_ \_ G \_ 至 \_ G、gl 圖元地圖 \_ \_ \_ b \_ 到 \_ b，而 gl 圖元會將 \_ \_ A 對應 \_ \_ 至 \_ 。</span><span class="sxs-lookup"><span data-stu-id="664d2-111">Accepted values are GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, GL\_PIXEL\_MAP\_I\_TO\_A, GL\_PIXEL\_MAP\_R\_TO\_R, GL\_PIXEL\_MAP\_G\_TO\_G, GL\_PIXEL\_MAP\_B\_TO\_B, and GL\_PIXEL\_MAP\_A\_TO\_A.</span></span>

</dd> <dt>

<span data-ttu-id="664d2-112">*值*</span><span class="sxs-lookup"><span data-stu-id="664d2-112">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="664d2-113">傳回圖元地圖內容。</span><span class="sxs-lookup"><span data-stu-id="664d2-113">Returns the pixel map contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="664d2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="664d2-114">Return value</span></span>

<span data-ttu-id="664d2-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="664d2-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="664d2-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="664d2-116">Error codes</span></span>

<span data-ttu-id="664d2-117">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="664d2-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="664d2-118">Name</span><span class="sxs-lookup"><span data-stu-id="664d2-118">Name</span></span>                                                                                                  | <span data-ttu-id="664d2-119">意義</span><span class="sxs-lookup"><span data-stu-id="664d2-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="664d2-120"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="664d2-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="664d2-121">*地圖* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="664d2-121">*map* was not an accepted value.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="664d2-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="664d2-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="664d2-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="664d2-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="664d2-124">備註</span><span class="sxs-lookup"><span data-stu-id="664d2-124">Remarks</span></span>

<span data-ttu-id="664d2-125">如需 *map* 參數可接受值的描述，請參閱 [**glPixelMap**](glpixelmap.md) 。</span><span class="sxs-lookup"><span data-stu-id="664d2-125">See [**glPixelMap**](glpixelmap.md) for a description of the acceptable values for the *map* parameter.</span></span> <span data-ttu-id="664d2-126">**GlGetPixelMap** 函式會傳回 *map* 中所指定圖元地圖內容的 *值*。</span><span class="sxs-lookup"><span data-stu-id="664d2-126">The **glGetPixelMap** function returns in *values* the contents of the pixel map specified in *map*.</span></span> <span data-ttu-id="664d2-127">在執行 [**glReadPixels**](glreadpixels.md)、 [**glDrawPixels**](gldrawpixels.md)、 [**glCopyPixels**](glcopypixels.md)、 [**glTexImage1D**](glteximage1d.md)和 [**glTexImage2D**](glteximage2d.md) 期間使用圖元地圖，以將色彩索引、樣板索引、色彩元件和深度元件對應至其他值。</span><span class="sxs-lookup"><span data-stu-id="664d2-127">Use pixel maps during the execution of [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md), and [**glTexImage2D**](glteximage2d.md) to map color indexes, stencil indexes, color components, and depth components to other values.</span></span>

<span data-ttu-id="664d2-128">不帶正負號的整數值（如有要求）會以線性方式從內部固定或浮點表示對應，使1.0 對應到最大的可表示整數值，0.0 則對應至零。</span><span class="sxs-lookup"><span data-stu-id="664d2-128">Unsigned integer values, if requested, are linearly mapped from the internal fixed or floating-point representation such that 1.0 maps to the largest representable integer value, and 0.0 maps to zero.</span></span> <span data-ttu-id="664d2-129">如果對應值不在0到1的範圍內，則不會定義傳回不帶正負號的整數值 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="664d2-129">Return unsigned integer values are undefined if the map value was not in the range \[0,1\].</span></span>

<span data-ttu-id="664d2-130">若要判斷所需的 *地圖* 大小，請使用適當的符號常數來呼叫 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 。</span><span class="sxs-lookup"><span data-stu-id="664d2-130">To determine the required size of *map*, call [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with the appropriate symbolic constant.</span></span>

<span data-ttu-id="664d2-131">如果產生錯誤，則不會對 *值* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="664d2-131">If an error is generated, no change is made to the contents of *values*.</span></span>

<span data-ttu-id="664d2-132">下列函式會取出與 **glGetPixelMap** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="664d2-132">The following functions retrieve information related to **glGetPixelMap**:</span></span>

<span data-ttu-id="664d2-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 圖元 \_ 對應 \_ 我 \_ 的 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="664d2-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="664d2-134">將引數 GL \_ 圖元 \_ 對應 \_ \_ 到 \_ s \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="664d2-134">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="664d2-135">使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ R \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="664d2-135">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="664d2-136">使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="664d2-136">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="664d2-137">**glGet** 與引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 B 的 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="664d2-137">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="664d2-138">**glGet** 與引數 GL \_ 圖元 \_ 對應 \_ I \_ 至 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="664d2-138">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="664d2-139">使用引數 GL \_ 圖元 \_ 地圖 \_ r \_ 至 \_ r \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="664d2-139">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="664d2-140">具有引數 GL \_ 圖元 \_ 地圖 \_ g \_ 至 \_ g \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="664d2-140">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="664d2-141">具有引數 GL \_ 圖元 \_ 地圖 \_ b \_ 到 \_ b \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="664d2-141">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="664d2-142">具有引數 GL \_ 圖元 \_ 的 glGet 對應 \_ \_ 至 \_ \_ 大小</span><span class="sxs-lookup"><span data-stu-id="664d2-142">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="664d2-143">具有引數 GL \_ 最大 \_ 圖元 \_ 地圖 \_ 資料表的 glGet</span><span class="sxs-lookup"><span data-stu-id="664d2-143">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="664d2-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="664d2-144">Requirements</span></span>



| <span data-ttu-id="664d2-145">需求</span><span class="sxs-lookup"><span data-stu-id="664d2-145">Requirement</span></span> | <span data-ttu-id="664d2-146">值</span><span class="sxs-lookup"><span data-stu-id="664d2-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="664d2-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="664d2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="664d2-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="664d2-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="664d2-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="664d2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="664d2-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="664d2-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="664d2-151">標頭</span><span class="sxs-lookup"><span data-stu-id="664d2-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="664d2-152"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="664d2-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="664d2-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="664d2-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="664d2-154"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="664d2-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="664d2-155">DLL</span><span class="sxs-lookup"><span data-stu-id="664d2-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="664d2-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="664d2-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="664d2-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="664d2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664d2-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="664d2-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="664d2-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="664d2-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="664d2-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="664d2-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="664d2-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="664d2-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="664d2-162">**glGet**</span><span class="sxs-lookup"><span data-stu-id="664d2-162">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="664d2-163">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="664d2-163">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="664d2-164">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="664d2-164">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="664d2-165">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="664d2-165">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="664d2-166">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="664d2-166">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="664d2-167">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="664d2-167">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





