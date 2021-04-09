---
title: 'glBitmap 函式 (Gl) '
description: GlBitmap 函式會繪製點陣圖。
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glBitmap 函式 OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025202"
---
# <a name="glbitmap-function"></a><span data-ttu-id="8faf4-104">glBitmap 函式</span><span class="sxs-lookup"><span data-stu-id="8faf4-104">glBitmap function</span></span>

<span data-ttu-id="8faf4-105">**GlBitmap** 函式會繪製點陣圖。</span><span class="sxs-lookup"><span data-stu-id="8faf4-105">The **glBitmap** function draws a bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="8faf4-106">語法</span><span class="sxs-lookup"><span data-stu-id="8faf4-106">Syntax</span></span>


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a><span data-ttu-id="8faf4-107">參數</span><span class="sxs-lookup"><span data-stu-id="8faf4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8faf4-108">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="8faf4-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="8faf4-109">點陣圖影像的圖元寬度。</span><span class="sxs-lookup"><span data-stu-id="8faf4-109">The pixel width of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="8faf4-110">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="8faf4-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="8faf4-111">點陣圖影像的圖元高度。</span><span class="sxs-lookup"><span data-stu-id="8faf4-111">The pixel height of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="8faf4-112">*xorig*</span><span class="sxs-lookup"><span data-stu-id="8faf4-112">*xorig*</span></span> 
</dt> <dd>

<span data-ttu-id="8faf4-113">點陣圖影像中原點的 *x* 位置。</span><span class="sxs-lookup"><span data-stu-id="8faf4-113">The *x* location of the origin in the bitmap image.</span></span> <span data-ttu-id="8faf4-114">來源是以點陣圖左下角來測量，而右邊和向上方向則是正軸。</span><span class="sxs-lookup"><span data-stu-id="8faf4-114">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="8faf4-115">*yorig*</span><span class="sxs-lookup"><span data-stu-id="8faf4-115">*yorig*</span></span> 
</dt> <dd>

<span data-ttu-id="8faf4-116">點陣圖影像中原點的 *y* 位置。</span><span class="sxs-lookup"><span data-stu-id="8faf4-116">The *y* location of the origin in the bitmap image.</span></span> <span data-ttu-id="8faf4-117">來源是以點陣圖左下角來測量，而右邊和向上方向則是正軸。</span><span class="sxs-lookup"><span data-stu-id="8faf4-117">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="8faf4-118">*xmove*</span><span class="sxs-lookup"><span data-stu-id="8faf4-118">*xmove*</span></span> 
</dt> <dd>

<span data-ttu-id="8faf4-119">繪製點陣圖之後要加入目前點陣位置的 *x* 位移。</span><span class="sxs-lookup"><span data-stu-id="8faf4-119">The *x* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="8faf4-120">*ymove*</span><span class="sxs-lookup"><span data-stu-id="8faf4-120">*ymove*</span></span> 
</dt> <dd>

<span data-ttu-id="8faf4-121">繪製點陣圖之後要加入目前點陣位置的 *y* 位移。</span><span class="sxs-lookup"><span data-stu-id="8faf4-121">The *y* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="8faf4-122">*點陣圖*</span><span class="sxs-lookup"><span data-stu-id="8faf4-122">*bitmap*</span></span> 
</dt> <dd>

<span data-ttu-id="8faf4-123">點陣圖影像的位址。</span><span class="sxs-lookup"><span data-stu-id="8faf4-123">The address of the bitmap image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8faf4-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="8faf4-124">Return value</span></span>

<span data-ttu-id="8faf4-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8faf4-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8faf4-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8faf4-126">Error codes</span></span>

<span data-ttu-id="8faf4-127">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8faf4-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8faf4-128">Name</span><span class="sxs-lookup"><span data-stu-id="8faf4-128">Name</span></span>                                                                                                  | <span data-ttu-id="8faf4-129">意義</span><span class="sxs-lookup"><span data-stu-id="8faf4-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8faf4-130"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="8faf4-130"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8faf4-131">*寬度* 或 *高度* 為負數。</span><span class="sxs-lookup"><span data-stu-id="8faf4-131">*width* or *height* is negative.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="8faf4-132"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="8faf4-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8faf4-133">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="8faf4-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8faf4-134">備註</span><span class="sxs-lookup"><span data-stu-id="8faf4-134">Remarks</span></span>

<span data-ttu-id="8faf4-135">點陣圖是二進位影像。</span><span class="sxs-lookup"><span data-stu-id="8faf4-135">A bitmap is a binary image.</span></span> <span data-ttu-id="8faf4-136">繪製時，點陣圖的位置相對於目前的點陣位置，而點陣圖中對應至1s 的畫面格緩衝區圖元則是使用目前的點陣色彩或索引來撰寫。</span><span class="sxs-lookup"><span data-stu-id="8faf4-136">When drawn, the bitmap is positioned relative to the current raster position, and framebuffer pixels corresponding to 1s in the bitmap are written using the current raster color or index.</span></span> <span data-ttu-id="8faf4-137">不會修改對應至點陣圖中零的框架緩衝區圖元。</span><span class="sxs-lookup"><span data-stu-id="8faf4-137">Frame-buffer pixels corresponding to zeros in the bitmap are not modified.</span></span>

<span data-ttu-id="8faf4-138">點陣圖影像的解讀方式就像是 [**glDrawPixels**](gldrawpixels.md) 函式的影像資料，其 *寬度* 和 *高度* 對應于該函式的寬度和高度引數，以及將 *type* 設定為 GL \_ 點陣圖，並將 *格式* 設定為 gl \_ 色彩 \_ 索引。</span><span class="sxs-lookup"><span data-stu-id="8faf4-138">The bitmap image is interpreted like image data for the [**glDrawPixels**](gldrawpixels.md) function, with *width* and *height* corresponding to the width and height arguments of that function, and with *type* set to GL\_BITMAP and *format* set to GL\_COLOR\_INDEX.</span></span> <span data-ttu-id="8faf4-139">使用 [**glPixelStore**](glpixelstore-functions.md) 指定的模式會影響點陣圖影像資料的解讀;使用 [**glPixelTransfer**](glpixeltransfer.md) 指定的模式則否。</span><span class="sxs-lookup"><span data-stu-id="8faf4-139">Modes you specify using [**glPixelStore**](glpixelstore-functions.md) affect the interpretation of bitmap image data; modes you specify using [**glPixelTransfer**](glpixeltransfer.md) do not.</span></span>

<span data-ttu-id="8faf4-140">如果目前的點陣位置無效，則會忽略 **glBitmap** 。</span><span class="sxs-lookup"><span data-stu-id="8faf4-140">If the current raster position is invalid, **glBitmap** is ignored.</span></span> <span data-ttu-id="8faf4-141">否則，點陣圖影像的左下角會位於下列視窗座標：</span><span class="sxs-lookup"><span data-stu-id="8faf4-141">Otherwise, the lower-left corner of the bitmap image is positioned at the following window coordinates:</span></span>

<span data-ttu-id="8faf4-142">*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*？</span><span class="sxs-lookup"><span data-stu-id="8faf4-142">*x*<sub>w</sub> = *x*<sub>r</sub> *x*?</span></span>

<span data-ttu-id="8faf4-143">*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*？</span><span class="sxs-lookup"><span data-stu-id="8faf4-143">*y*<sub>w</sub> = *y*<sub>r</sub> *y*?</span></span>

<span data-ttu-id="8faf4-144">在這些座標中， (*x*<sub>r</sub> 、 *y*<sub>r</sub> ) 是點陣位置，而 (*x*？</span><span class="sxs-lookup"><span data-stu-id="8faf4-144">In these coordinates, (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the raster position, and (*x*?</span></span> <span data-ttu-id="8faf4-145">， *y*？</span><span class="sxs-lookup"><span data-stu-id="8faf4-145">, *y*?</span></span> <span data-ttu-id="8faf4-146">) 是點陣圖原點。</span><span class="sxs-lookup"><span data-stu-id="8faf4-146">) is the bitmap origin.</span></span> <span data-ttu-id="8faf4-147">然後會為點陣圖影像中對應至1的每個圖元產生片段。</span><span class="sxs-lookup"><span data-stu-id="8faf4-147">Fragments are then generated for each pixel corresponding to a 1 in the bitmap image.</span></span> <span data-ttu-id="8faf4-148">這些片段會使用目前的點陣 *z* 座標、色彩或色彩索引，以及目前的點陣材質座標來產生。</span><span class="sxs-lookup"><span data-stu-id="8faf4-148">These fragments are generated using the current raster *z*-coordinate, color or color index, and current raster texture coordinates.</span></span> <span data-ttu-id="8faf4-149">然後，系統會將它們視為由點、線條或多邊形產生，包括紋理對應、fogging，以及 Alpha 和深度測試等所有的每個片段作業。</span><span class="sxs-lookup"><span data-stu-id="8faf4-149">They are then treated just as if they had been generated by a point, line, or polygon, including texture mapping, fogging, and all per-fragment operations such as alpha and depth testing.</span></span>

<span data-ttu-id="8faf4-150">繪製點陣圖之後，目前點陣位置的 *x* 和 *y* 座標會以 *xmove* 和 *ymove* 位移。</span><span class="sxs-lookup"><span data-stu-id="8faf4-150">After the bitmap has been drawn, the *x* and *y* coordinates of the current raster position are offset by *xmove* and *ymove*.</span></span> <span data-ttu-id="8faf4-151">目前點陣位置的 *z* 座標或目前的點陣色彩、索引或材質座標都不會進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="8faf4-151">No change is made to the *z*-coordinate of the current raster position, or to the current raster color, index, or texture coordinates.</span></span>

<span data-ttu-id="8faf4-152">下列函式會取出與 **glBitmap** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="8faf4-152">The following functions retrieve information related to the **glBitmap** function:</span></span>

<span data-ttu-id="8faf4-153">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet</span><span class="sxs-lookup"><span data-stu-id="8faf4-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

 

<span data-ttu-id="8faf4-154">具有引數 GL \_ 目前 \_ 點陣 \_ 色彩的 glGet</span><span class="sxs-lookup"><span data-stu-id="8faf4-154">**glGet** with argument GL\_CURRENT\_RASTER\_COLOR</span></span>

 

<span data-ttu-id="8faf4-155">具有引數 GL \_ 目前 \_ 點陣 \_ 索引的 glGet</span><span class="sxs-lookup"><span data-stu-id="8faf4-155">**glGet** with argument GL\_CURRENT\_RASTER\_INDEX</span></span>

 

<span data-ttu-id="8faf4-156">具有引數 GL \_ 目前 \_ 點陣 \_ 材質紋理 \_ 的 glGet</span><span class="sxs-lookup"><span data-stu-id="8faf4-156">**glGet** with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>

 

<span data-ttu-id="8faf4-157">具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet</span><span class="sxs-lookup"><span data-stu-id="8faf4-157">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="8faf4-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="8faf4-158">Requirements</span></span>



| <span data-ttu-id="8faf4-159">需求</span><span class="sxs-lookup"><span data-stu-id="8faf4-159">Requirement</span></span> | <span data-ttu-id="8faf4-160">值</span><span class="sxs-lookup"><span data-stu-id="8faf4-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8faf4-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8faf4-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8faf4-162">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8faf4-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8faf4-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8faf4-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8faf4-164">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8faf4-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8faf4-165">標頭</span><span class="sxs-lookup"><span data-stu-id="8faf4-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="8faf4-166"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="8faf4-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8faf4-167">程式庫</span><span class="sxs-lookup"><span data-stu-id="8faf4-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="8faf4-168"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8faf4-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8faf4-169">DLL</span><span class="sxs-lookup"><span data-stu-id="8faf4-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8faf4-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8faf4-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8faf4-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8faf4-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8faf4-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8faf4-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8faf4-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="8faf4-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="8faf4-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8faf4-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8faf4-175">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="8faf4-175">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="8faf4-176">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="8faf4-176">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="8faf4-177">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="8faf4-177">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> </dl>

 

 





