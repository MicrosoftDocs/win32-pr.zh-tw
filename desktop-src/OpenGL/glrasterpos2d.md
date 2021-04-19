---
title: 'glRasterPos2d 函式 (Gl) '
description: '指定圖元作業的點陣位置。 |glRasterPos2d 函式 (Gl) '
ms.assetid: 3aad4085-8957-433c-8822-765df6278af8
keywords:
- glRasterPos2d 函式 OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0567843e157f869bc6caf5fa0932e238e54bcf61
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991961"
---
# <a name="glrasterpos2d-function"></a><span data-ttu-id="6e924-105">glRasterPos2d 函式</span><span class="sxs-lookup"><span data-stu-id="6e924-105">glRasterPos2d function</span></span>

<span data-ttu-id="6e924-106">指定圖元作業的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="6e924-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e924-107">語法</span><span class="sxs-lookup"><span data-stu-id="6e924-107">Syntax</span></span>


```C++
void WINAPI glRasterPos2d(
   GLdouble x,
   GLdouble y
);
```



## <a name="parameters"></a><span data-ttu-id="6e924-108">參數</span><span class="sxs-lookup"><span data-stu-id="6e924-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e924-109">*x*</span><span class="sxs-lookup"><span data-stu-id="6e924-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6e924-110">指定目前點陣位置的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="6e924-110">Specifies the x-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="6e924-111">*y*</span><span class="sxs-lookup"><span data-stu-id="6e924-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6e924-112">指定目前點陣位置的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="6e924-112">Specifies the y-coordinate for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e924-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e924-113">Return value</span></span>

<span data-ttu-id="6e924-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6e924-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e924-115">備註</span><span class="sxs-lookup"><span data-stu-id="6e924-115">Remarks</span></span>

<span data-ttu-id="6e924-116">OpenGL 會在視窗座標中維持立體的位置。</span><span class="sxs-lookup"><span data-stu-id="6e924-116">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="6e924-117">這個位置（稱為點陣定位）會以子圖元精確度來維持。</span><span class="sxs-lookup"><span data-stu-id="6e924-117">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="6e924-118">它是用來放置圖元和點陣圖寫入作業。</span><span class="sxs-lookup"><span data-stu-id="6e924-118">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="6e924-119">請參閱 [**glBitmap**](glbitmap.md)、 [**glDrawPixels**](gldrawpixels.md)和 [**glCopyPixels**](glcopypixels.md)。</span><span class="sxs-lookup"><span data-stu-id="6e924-119">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="6e924-120">目前的點陣位置包含三個視窗座標 (*x、y、z*) 、剪輯座標（ *w* 值）、眼睛座標距離、有效位，以及相關聯的色彩資料和材質座標。</span><span class="sxs-lookup"><span data-stu-id="6e924-120">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="6e924-121">*W* 座標是剪輯座標，因為 *w* 不會投影至視窗座標。</span><span class="sxs-lookup"><span data-stu-id="6e924-121">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="6e924-122">[GlRasterPos4](glrasterpos-functions.md)函式會明確指定物件座標 *x、y、z* 和 *w* 。</span><span class="sxs-lookup"><span data-stu-id="6e924-122">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="6e924-123">GlRasterPos3 函式會明確指定物件座標 *x、y* 和 *z* ，而 *w* 會隱含地設定為一。</span><span class="sxs-lookup"><span data-stu-id="6e924-123">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="6e924-124">GlRasterPos2 函式會使用 *x* 和 *y* 的引數值，同時將 *z* 和 *w* 隱含設定為零和1。</span><span class="sxs-lookup"><span data-stu-id="6e924-124">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="6e924-125">[GlRasterPos](glrasterpos-functions.md)所呈現的物件座標就如同[glVertex](glvertex-functions.md)命令的座標一樣。</span><span class="sxs-lookup"><span data-stu-id="6e924-125">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="6e924-126">它們是由目前的模型和投射矩陣進行轉換，並且傳遞至剪切階段。</span><span class="sxs-lookup"><span data-stu-id="6e924-126">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="6e924-127">如果頂點未挑選，則會進行投影並調整為視窗座標（這會成為新的目前點陣位置），並設定 GL \_ 目前的 \_ 點陣 \_ 定位 \_ 有效旗標。</span><span class="sxs-lookup"><span data-stu-id="6e924-127">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="6e924-128">如果頂點是挑選，則會清除有效位，而且不會定義目前的點陣位置和相關聯的色彩和材質座標。</span><span class="sxs-lookup"><span data-stu-id="6e924-128">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="6e924-129">目前的點陣位置也包含一些相關聯的色彩資料和材質座標。</span><span class="sxs-lookup"><span data-stu-id="6e924-129">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="6e924-130">如果已啟用光源，則在 \_ \_ \_ RGBA 模式中使用 gl 目前的點陣色彩，或 \_ 在 [ \_ 色彩索引模式] 中將 [gl 目前的點陣 \_ 索引] 設定為 [光線計算] 所產生的色彩 (請參閱 [glLight](gllight-functions.md)、 [glLightModel](gllightmodel-functions.md)和 [**glShadeModel**](glshademodel.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6e924-130">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="6e924-131">如果停用光源，目前的色彩 (在 RGBA 模式下，狀態變數 GL \_ 目前 \_ 色彩) 或色彩索引 (處於色彩索引模式時，狀態變數 gl \_ 目前 \_ 索引) 會用來更新目前的點陣色彩。</span><span class="sxs-lookup"><span data-stu-id="6e924-131">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="6e924-132">同樣地， \_ \_ \_ \_ 根據紋理矩陣和材質產生函式，會將 gl 目前的點陣材質 coords 更新為 gl \_ 目前材質 coords 的函式 \_ \_ (查看 [glTexGen](gltexgen-functions.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6e924-132">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="6e924-133">最後，從眼睛座標系統的原點到頂點的距離（僅由模型矩陣轉換）會取代 GL \_ 目前的 \_ 點陣 \_ 距離。</span><span class="sxs-lookup"><span data-stu-id="6e924-133">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="6e924-134">一開始，目前的點陣位置是 (0、0、0、1) 、目前的點陣距離為0、已設定有效位、相關聯的 RGBA 色彩 (1、1、1、1) 、相關聯的色彩索引為1，且相關聯的材質座標為 (0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="6e924-134">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="6e924-135">在 RGBA 模式中， \_ GL \_ 目前 \_ 的點陣索引一律為 1; 在色彩索引模式中，目前的點陣 RGBA 色彩一律會維持其初始值。</span><span class="sxs-lookup"><span data-stu-id="6e924-135">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="6e924-136">[GlRasterPos](glrasterpos-functions.md)和 by [**glBitmap**](glbitmap.md)都會修改點陣位置。</span><span class="sxs-lookup"><span data-stu-id="6e924-136">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="6e924-137">當點陣位置座標無效時，會忽略以點陣位置為基礎的繪製命令 (也就是不會導致 OpenGL 狀態) 的變更。</span><span class="sxs-lookup"><span data-stu-id="6e924-137">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="6e924-138">下列函式會取出與 [glRasterPos](glrasterpos-functions.md)相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="6e924-138">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="6e924-139">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet</span><span class="sxs-lookup"><span data-stu-id="6e924-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="6e924-140">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet</span><span class="sxs-lookup"><span data-stu-id="6e924-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="6e924-141">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 距離的 glGet</span><span class="sxs-lookup"><span data-stu-id="6e924-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="6e924-142">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 色彩的 glGet</span><span class="sxs-lookup"><span data-stu-id="6e924-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="6e924-143">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 索引的 glGet</span><span class="sxs-lookup"><span data-stu-id="6e924-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="6e924-144">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 材質紋理 \_ 的 glGet</span><span class="sxs-lookup"><span data-stu-id="6e924-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="6e924-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e924-145">Requirements</span></span>



| <span data-ttu-id="6e924-146">需求</span><span class="sxs-lookup"><span data-stu-id="6e924-146">Requirement</span></span> | <span data-ttu-id="6e924-147">值</span><span class="sxs-lookup"><span data-stu-id="6e924-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e924-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e924-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6e924-149">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e924-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6e924-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e924-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6e924-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e924-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e924-152">標頭</span><span class="sxs-lookup"><span data-stu-id="6e924-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e924-153"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="6e924-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6e924-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e924-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e924-155"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e924-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e924-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6e924-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e924-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e924-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e924-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e924-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e924-159">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6e924-159">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6e924-160">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="6e924-160">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="6e924-161">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="6e924-161">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="6e924-162">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="6e924-162">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="6e924-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6e924-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6e924-164">glLight</span><span class="sxs-lookup"><span data-stu-id="6e924-164">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="6e924-165">glLightModel</span><span class="sxs-lookup"><span data-stu-id="6e924-165">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="6e924-166">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="6e924-166">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="6e924-167">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="6e924-167">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="6e924-168">glTexGen</span><span class="sxs-lookup"><span data-stu-id="6e924-168">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="6e924-169">glVertex</span><span class="sxs-lookup"><span data-stu-id="6e924-169">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





