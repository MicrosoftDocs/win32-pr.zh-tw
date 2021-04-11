---
title: 'glRasterPos3fv 函式 (Gl) '
description: '指定圖元作業的點陣位置。 |glRasterPos3fv 函式 (Gl) '
ms.assetid: a6bf1823-2652-4e39-806e-ebf5b7aac9f2
keywords:
- glRasterPos3fv 函式 OpenGL
topic_type:
- apiref
api_name:
- glRasterPos3fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f6d2738ced6781c56a678af56c372352e839a9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035260"
---
# <a name="glrasterpos3fv-function"></a><span data-ttu-id="832ae-105">glRasterPos3fv 函式</span><span class="sxs-lookup"><span data-stu-id="832ae-105">glRasterPos3fv function</span></span>

<span data-ttu-id="832ae-106">指定圖元作業的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="832ae-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="832ae-107">語法</span><span class="sxs-lookup"><span data-stu-id="832ae-107">Syntax</span></span>


```C++
void WINAPI glRasterPos3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="832ae-108">參數</span><span class="sxs-lookup"><span data-stu-id="832ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="832ae-109">*V*</span><span class="sxs-lookup"><span data-stu-id="832ae-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="832ae-110">指標，指向三個元素的陣列，指定目前點陣位置的 x、y 和 z 座標。</span><span class="sxs-lookup"><span data-stu-id="832ae-110">A pointer to an array of three elements, specifying x, y, and z coordinates for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="832ae-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="832ae-111">Return value</span></span>

<span data-ttu-id="832ae-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="832ae-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="832ae-113">備註</span><span class="sxs-lookup"><span data-stu-id="832ae-113">Remarks</span></span>

<span data-ttu-id="832ae-114">OpenGL 會在視窗座標中維持立體的位置。</span><span class="sxs-lookup"><span data-stu-id="832ae-114">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="832ae-115">這個位置（稱為點陣定位）會以子圖元精確度來維持。</span><span class="sxs-lookup"><span data-stu-id="832ae-115">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="832ae-116">它是用來放置圖元和點陣圖寫入作業。</span><span class="sxs-lookup"><span data-stu-id="832ae-116">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="832ae-117">請參閱 [**glBitmap**](glbitmap.md)、 [**glDrawPixels**](gldrawpixels.md)和 [**glCopyPixels**](glcopypixels.md)。</span><span class="sxs-lookup"><span data-stu-id="832ae-117">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="832ae-118">目前的點陣位置包含三個視窗座標 (*x、y、z*) 、剪輯座標（ *w* 值）、眼睛座標距離、有效位，以及相關聯的色彩資料和材質座標。</span><span class="sxs-lookup"><span data-stu-id="832ae-118">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="832ae-119">*W* 座標是剪輯座標，因為 *w* 不會投影至視窗座標。</span><span class="sxs-lookup"><span data-stu-id="832ae-119">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="832ae-120">[GlRasterPos4](glrasterpos-functions.md)函式會明確指定物件座標 *x、y、z* 和 *w* 。</span><span class="sxs-lookup"><span data-stu-id="832ae-120">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="832ae-121">GlRasterPos3 函式會明確指定物件座標 *x、y* 和 *z* ，而 *w* 會隱含地設定為一。</span><span class="sxs-lookup"><span data-stu-id="832ae-121">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="832ae-122">GlRasterPos2 函式會使用 *x* 和 *y* 的引數值，同時將 *z* 和 *w* 隱含設定為零和1。</span><span class="sxs-lookup"><span data-stu-id="832ae-122">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="832ae-123">[GlRasterPos](glrasterpos-functions.md)所呈現的物件座標就如同[glVertex](glvertex-functions.md)命令的座標一樣。</span><span class="sxs-lookup"><span data-stu-id="832ae-123">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="832ae-124">它們是由目前的模型和投射矩陣進行轉換，並且傳遞至剪切階段。</span><span class="sxs-lookup"><span data-stu-id="832ae-124">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="832ae-125">如果頂點未挑選，則會進行投影並調整為視窗座標（這會成為新的目前點陣位置），並設定 GL \_ 目前的 \_ 點陣 \_ 定位 \_ 有效旗標。</span><span class="sxs-lookup"><span data-stu-id="832ae-125">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="832ae-126">如果頂點是挑選，則會清除有效位，而且不會定義目前的點陣位置和相關聯的色彩和材質座標。</span><span class="sxs-lookup"><span data-stu-id="832ae-126">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="832ae-127">目前的點陣位置也包含一些相關聯的色彩資料和材質座標。</span><span class="sxs-lookup"><span data-stu-id="832ae-127">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="832ae-128">如果已啟用光源，則在 \_ \_ \_ RGBA 模式中使用 gl 目前的點陣色彩，或 \_ 在 [ \_ 色彩索引模式] 中將 [gl 目前的點陣 \_ 索引] 設定為 [光線計算] 所產生的色彩 (請參閱 [glLight](gllight-functions.md)、 [glLightModel](gllightmodel-functions.md)和 [**glShadeModel**](glshademodel.md)) 。</span><span class="sxs-lookup"><span data-stu-id="832ae-128">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="832ae-129">如果停用光源，目前的色彩 (在 RGBA 模式下，狀態變數 GL \_ 目前 \_ 色彩) 或色彩索引 (處於色彩索引模式時，狀態變數 gl \_ 目前 \_ 索引) 會用來更新目前的點陣色彩。</span><span class="sxs-lookup"><span data-stu-id="832ae-129">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="832ae-130">同樣地， \_ \_ \_ \_ 根據紋理矩陣和材質產生函式，會將 gl 目前的點陣材質 coords 更新為 gl \_ 目前材質 coords 的函式 \_ \_ (查看 [glTexGen](gltexgen-functions.md)) 。</span><span class="sxs-lookup"><span data-stu-id="832ae-130">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="832ae-131">最後，從眼睛座標系統的原點到頂點的距離（僅由模型矩陣轉換）會取代 GL \_ 目前的 \_ 點陣 \_ 距離。</span><span class="sxs-lookup"><span data-stu-id="832ae-131">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="832ae-132">一開始，目前的點陣位置是 (0、0、0、1) 、目前的點陣距離為0、已設定有效位、相關聯的 RGBA 色彩 (1、1、1、1) 、相關聯的色彩索引為1，且相關聯的材質座標為 (0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="832ae-132">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="832ae-133">在 RGBA 模式中， \_ GL \_ 目前 \_ 的點陣索引一律為 1; 在色彩索引模式中，目前的點陣 RGBA 色彩一律會維持其初始值。</span><span class="sxs-lookup"><span data-stu-id="832ae-133">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="832ae-134">[GlRasterPos](glrasterpos-functions.md)和 by [**glBitmap**](glbitmap.md)都會修改點陣位置。</span><span class="sxs-lookup"><span data-stu-id="832ae-134">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="832ae-135">當點陣位置座標無效時，會忽略以點陣位置為基礎的繪製命令 (也就是不會導致 OpenGL 狀態) 的變更。</span><span class="sxs-lookup"><span data-stu-id="832ae-135">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="832ae-136">下列函式會取出與 [glRasterPos](glrasterpos-functions.md)相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="832ae-136">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="832ae-137">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet</span><span class="sxs-lookup"><span data-stu-id="832ae-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="832ae-138">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet</span><span class="sxs-lookup"><span data-stu-id="832ae-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="832ae-139">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 距離的 glGet</span><span class="sxs-lookup"><span data-stu-id="832ae-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="832ae-140">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 色彩的 glGet</span><span class="sxs-lookup"><span data-stu-id="832ae-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="832ae-141">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 索引的 glGet</span><span class="sxs-lookup"><span data-stu-id="832ae-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="832ae-142">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 材質紋理 \_ 的 glGet</span><span class="sxs-lookup"><span data-stu-id="832ae-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="832ae-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="832ae-143">Requirements</span></span>



| <span data-ttu-id="832ae-144">需求</span><span class="sxs-lookup"><span data-stu-id="832ae-144">Requirement</span></span> | <span data-ttu-id="832ae-145">值</span><span class="sxs-lookup"><span data-stu-id="832ae-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="832ae-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="832ae-146">Minimum supported client</span></span><br/> | <span data-ttu-id="832ae-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="832ae-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="832ae-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="832ae-148">Minimum supported server</span></span><br/> | <span data-ttu-id="832ae-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="832ae-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="832ae-150">標頭</span><span class="sxs-lookup"><span data-stu-id="832ae-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="832ae-151"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="832ae-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="832ae-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="832ae-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="832ae-153"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="832ae-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="832ae-154">DLL</span><span class="sxs-lookup"><span data-stu-id="832ae-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="832ae-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="832ae-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="832ae-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="832ae-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="832ae-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="832ae-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="832ae-158">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="832ae-158">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="832ae-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="832ae-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="832ae-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="832ae-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="832ae-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="832ae-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="832ae-162">glLight</span><span class="sxs-lookup"><span data-stu-id="832ae-162">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="832ae-163">glLightModel</span><span class="sxs-lookup"><span data-stu-id="832ae-163">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="832ae-164">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="832ae-164">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="832ae-165">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="832ae-165">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="832ae-166">glTexGen</span><span class="sxs-lookup"><span data-stu-id="832ae-166">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="832ae-167">glVertex</span><span class="sxs-lookup"><span data-stu-id="832ae-167">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





