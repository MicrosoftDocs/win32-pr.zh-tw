---
title: 'glPointSize 函式 (Gl) '
description: GlPointSize 函式會指定柵格點的直徑。
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize 函式 OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969788"
---
# <a name="glpointsize-function"></a><span data-ttu-id="91101-104">glPointSize 函式</span><span class="sxs-lookup"><span data-stu-id="91101-104">glPointSize function</span></span>

<span data-ttu-id="91101-105">**GlPointSize** 函式會指定柵格點的直徑。</span><span class="sxs-lookup"><span data-stu-id="91101-105">The **glPointSize** function specifies the diameter of rasterized points.</span></span>

## <a name="syntax"></a><span data-ttu-id="91101-106">語法</span><span class="sxs-lookup"><span data-stu-id="91101-106">Syntax</span></span>


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a><span data-ttu-id="91101-107">參數</span><span class="sxs-lookup"><span data-stu-id="91101-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91101-108">*size*</span><span class="sxs-lookup"><span data-stu-id="91101-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="91101-109">柵格化點的直徑。</span><span class="sxs-lookup"><span data-stu-id="91101-109">The diameter of rasterized points.</span></span> <span data-ttu-id="91101-110">預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="91101-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91101-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="91101-111">Return value</span></span>

<span data-ttu-id="91101-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="91101-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="91101-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="91101-113">Error codes</span></span>

<span data-ttu-id="91101-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="91101-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="91101-115">Name</span><span class="sxs-lookup"><span data-stu-id="91101-115">Name</span></span>                                                                                                  | <span data-ttu-id="91101-116">意義</span><span class="sxs-lookup"><span data-stu-id="91101-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91101-117"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="91101-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="91101-118">*大小* 小於或等於零。</span><span class="sxs-lookup"><span data-stu-id="91101-118">*size* was less than or equal to zero.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="91101-119"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="91101-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="91101-120">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="91101-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91101-121">備註</span><span class="sxs-lookup"><span data-stu-id="91101-121">Remarks</span></span>

<span data-ttu-id="91101-122">**GlPointSize** 函式會指定鋸齒和反鋸齒點的柵格化直徑。</span><span class="sxs-lookup"><span data-stu-id="91101-122">The **glPointSize** function specifies the rasterized diameter of both aliased and antialiased points.</span></span> <span data-ttu-id="91101-123">使用1.0 以外的點大小有不同的效果，取決於是否已啟用點消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="91101-123">Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled.</span></span> <span data-ttu-id="91101-124">點消除鋸齒是藉由呼叫 [**glEnable**](glenable.md) 和 **glDisable** 和引數 GL \_ 點平滑來控制 \_ 。</span><span class="sxs-lookup"><span data-stu-id="91101-124">Point antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_POINT\_SMOOTH.</span></span>

<span data-ttu-id="91101-125">如果停用點消除鋸齒，則會將提供的大小四捨五入至最接近的整數來決定實際大小。</span><span class="sxs-lookup"><span data-stu-id="91101-125">If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer.</span></span> <span data-ttu-id="91101-126"> (如果四捨五入結果的值為0，則會如同點大小為1。 ) 如果舍入大小為奇數，則表示該點之圖元片段的中心點 (*x*，*y*) 會計算為</span><span class="sxs-lookup"><span data-stu-id="91101-126">(If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (*x*,*y*) of the pixel fragment that represents the point is computed as</span></span>

<span data-ttu-id="91101-127"> (*x*<sub>w</sub> + .5， *y*<sub>w</sub> +. 5) </span><span class="sxs-lookup"><span data-stu-id="91101-127">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="91101-128">*w* 注標表示視窗座標。</span><span class="sxs-lookup"><span data-stu-id="91101-128">where *w* subscripts indicate window coordinates.</span></span> <span data-ttu-id="91101-129">在四捨五入大小的正方形方格內的所有圖元都位於 (*x*，*y*) 組成片段。</span><span class="sxs-lookup"><span data-stu-id="91101-129">All pixels that lie within the square grid of the rounded size centered at (*x*,*y*) make up the fragment.</span></span> <span data-ttu-id="91101-130">如果大小為偶數，則中心點為</span><span class="sxs-lookup"><span data-stu-id="91101-130">If the size is even, the center point is</span></span>

<span data-ttu-id="91101-131"> (*x*<sub>w</sub> + .5， *y*<sub>w</sub> +. 5) </span><span class="sxs-lookup"><span data-stu-id="91101-131">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="91101-132">柵格化片段的中心是在四捨五入大小的正方形內的半整數視窗座標，以 *x (x*，*y*) 為中心。</span><span class="sxs-lookup"><span data-stu-id="91101-132">and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (*x*,*y*).</span></span> <span data-ttu-id="91101-133">在將 nonantialiased 點進行柵格化時所產生的所有圖元片段都會指派相同的關聯資料;對應到點的頂點。</span><span class="sxs-lookup"><span data-stu-id="91101-133">All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.</span></span>

<span data-ttu-id="91101-134">如果已啟用消除鋸齒功能，則點柵格化會為每個圖元正方形產生一個片段，而該正方形與目前的點大小 <sub>相等，並</sub>以 *y*<sub>w</sub> )  (*x* 的點為中心。</span><span class="sxs-lookup"><span data-stu-id="91101-134">If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span></span> <span data-ttu-id="91101-135">每個片段的涵蓋範圍值都是迴圈區域與對應圖元正方形交集的視窗座標區域。</span><span class="sxs-lookup"><span data-stu-id="91101-135">The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square.</span></span> <span data-ttu-id="91101-136">此值會儲存並用於最後的點陣化步驟中。</span><span class="sxs-lookup"><span data-stu-id="91101-136">This value is saved and used in the final rasterization step.</span></span> <span data-ttu-id="91101-137">與每個片段相關聯的資料是與正在進行柵格化的點相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="91101-137">The data associated with each fragment is the data associated with the point being rasterized.</span></span>

<span data-ttu-id="91101-138">當點消除鋸齒啟用時，不支援所有的大小。</span><span class="sxs-lookup"><span data-stu-id="91101-138">Not all sizes are supported when point antialiasing is enabled.</span></span> <span data-ttu-id="91101-139">如果要求的大小不受支援，則會使用最接近的支援大小。</span><span class="sxs-lookup"><span data-stu-id="91101-139">If an unsupported size is requested, the nearest supported size is used.</span></span> <span data-ttu-id="91101-140">只保證支援大小 1.0;其他則取決於執行。</span><span class="sxs-lookup"><span data-stu-id="91101-140">Only size 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="91101-141">您可以藉由呼叫 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 點 \_ 大小 \_ 範圍和 GL \_ 點 \_ 大小 \_ 的資料細微性，來查詢範圍內支援的大小和大小差異。</span><span class="sxs-lookup"><span data-stu-id="91101-141">The range of supported sizes and the size difference between supported sizes within the range can be queried by calling [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with arguments GL\_POINT\_SIZE\_RANGE and GL\_POINT\_SIZE\_GRANULARITY.</span></span>

<span data-ttu-id="91101-142">當查詢 GL 點大小時，一律會傳回 **glPointSize** 所指定的點大小 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="91101-142">The point size specified by **glPointSize** is always returned when GL\_POINT\_SIZE is queried.</span></span> <span data-ttu-id="91101-143">別名和反鋸齒點的固定和舍入對指定的值沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="91101-143">Clamping and rounding for aliased and antialiased points have no effect on the specified value.</span></span>

<span data-ttu-id="91101-144">非反鋸齒的點大小可能會壓制為與執行相關的最大值。</span><span class="sxs-lookup"><span data-stu-id="91101-144">Non-antialiased point size may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="91101-145">雖然無法查詢這個最大值，但它必須小於反鋸齒點的最大值，舍入到最接近的整數值。</span><span class="sxs-lookup"><span data-stu-id="91101-145">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.</span></span>

<span data-ttu-id="91101-146">下列函式會取出與 **glPointSize** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="91101-146">The following functions retrieve information related to **glPointSize**:</span></span>

<span data-ttu-id="91101-147">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 點 \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="91101-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POINT\_SIZE</span></span>

<span data-ttu-id="91101-148">具有引數 GL \_ 點 \_ 大小 \_ 範圍的 glGet</span><span class="sxs-lookup"><span data-stu-id="91101-148">**glGet** with argument GL\_POINT\_SIZE\_RANGE</span></span>

<span data-ttu-id="91101-149">具有引數 GL \_ 點 \_ 大小 \_ 細微性的 glGet</span><span class="sxs-lookup"><span data-stu-id="91101-149">**glGet** with argument GL\_POINT\_SIZE\_GRANULARITY</span></span>

<span data-ttu-id="91101-150">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 點 \_ 平滑</span><span class="sxs-lookup"><span data-stu-id="91101-150">[**glIsEnabled**](glisenabled.md) with argument GL\_POINT\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="91101-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="91101-151">Requirements</span></span>



| <span data-ttu-id="91101-152">需求</span><span class="sxs-lookup"><span data-stu-id="91101-152">Requirement</span></span> | <span data-ttu-id="91101-153">值</span><span class="sxs-lookup"><span data-stu-id="91101-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91101-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91101-154">Minimum supported client</span></span><br/> | <span data-ttu-id="91101-155">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91101-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="91101-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91101-156">Minimum supported server</span></span><br/> | <span data-ttu-id="91101-157">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91101-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91101-158">標頭</span><span class="sxs-lookup"><span data-stu-id="91101-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="91101-159"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="91101-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="91101-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="91101-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="91101-161"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="91101-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="91101-162">DLL</span><span class="sxs-lookup"><span data-stu-id="91101-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91101-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91101-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91101-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91101-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91101-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="91101-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="91101-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="91101-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="91101-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="91101-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="91101-168">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="91101-168">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





