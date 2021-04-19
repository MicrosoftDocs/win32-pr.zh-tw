---
title: 'glLineWidth 函式 (Gl) '
description: GlLineWidth 函式會指定柵格線的寬度。
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth 函式 OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967572"
---
# <a name="gllinewidth-function"></a><span data-ttu-id="49812-104">glLineWidth 函式</span><span class="sxs-lookup"><span data-stu-id="49812-104">glLineWidth function</span></span>

<span data-ttu-id="49812-105">**GlLineWidth** 函式會指定柵格線的寬度。</span><span class="sxs-lookup"><span data-stu-id="49812-105">The **glLineWidth** function specifies the width of rasterized lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="49812-106">語法</span><span class="sxs-lookup"><span data-stu-id="49812-106">Syntax</span></span>


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a><span data-ttu-id="49812-107">參數</span><span class="sxs-lookup"><span data-stu-id="49812-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49812-108">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="49812-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="49812-109">柵格線的寬度。</span><span class="sxs-lookup"><span data-stu-id="49812-109">The width of rasterized lines.</span></span> <span data-ttu-id="49812-110">預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="49812-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49812-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="49812-111">Return value</span></span>

<span data-ttu-id="49812-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="49812-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="49812-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="49812-113">Error codes</span></span>

<span data-ttu-id="49812-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49812-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="49812-115">Name</span><span class="sxs-lookup"><span data-stu-id="49812-115">Name</span></span>                                                                                                  | <span data-ttu-id="49812-116">意義</span><span class="sxs-lookup"><span data-stu-id="49812-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49812-117"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="49812-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="49812-118">*寬度* 小於或等於零。</span><span class="sxs-lookup"><span data-stu-id="49812-118">*width* was less than or equal to zero.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="49812-119"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="49812-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="49812-120">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="49812-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="49812-121">備註</span><span class="sxs-lookup"><span data-stu-id="49812-121">Remarks</span></span>

<span data-ttu-id="49812-122">**GlLineWidth** 函式會指定鋸齒和反鋸齒線條的點陣化寬度。</span><span class="sxs-lookup"><span data-stu-id="49812-122">The **glLineWidth** function specifies the rasterized width of both aliased and antialiased lines.</span></span> <span data-ttu-id="49812-123">使用1.0 以外的線條寬度有不同的效果，這取決於是否已啟用行消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="49812-123">Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled.</span></span> <span data-ttu-id="49812-124">藉由呼叫 [**glEnable**](glenable.md) 和 **glDisable** ，並將引數 GL \_ 行平滑，以控制線條消除鋸齒 \_ 。</span><span class="sxs-lookup"><span data-stu-id="49812-124">Line antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_SMOOTH.</span></span>

<span data-ttu-id="49812-125">如果停用行消除鋸齒，則會將提供的寬度四捨五入至最接近的整數，以決定實際寬度。</span><span class="sxs-lookup"><span data-stu-id="49812-125">If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer.</span></span> <span data-ttu-id="49812-126"> (如果舍入結果的值為0.0，則會像行寬度是 1.0) If \| ？</span><span class="sxs-lookup"><span data-stu-id="49812-126">(If the rounding results in the value 0.0, it is as if the line width were 1.0) If \| ?</span></span> <span data-ttu-id="49812-127">x \|  =  \| ？</span><span class="sxs-lookup"><span data-stu-id="49812-127">x \| = \| ?</span></span> <span data-ttu-id="49812-128">y \| ， *i* 圖元會填入每個柵格化的資料行，其中 *i* 是 *寬度* 的舍入值。</span><span class="sxs-lookup"><span data-stu-id="49812-128">y \|, *i* pixels are filled in each column that is rasterized, where *i* is the rounded value of *width*.</span></span> <span data-ttu-id="49812-129">否則，系統會在每個已點陣化的資料列中填入 *i* 圖元。</span><span class="sxs-lookup"><span data-stu-id="49812-129">Otherwise, *i* pixels are filled in each row that is rasterized.</span></span>

<span data-ttu-id="49812-130">如果已啟用消除鋸齒功能，則線條柵格化會針對每個圖元正方形產生一個片段，該矩形的寬度等於目前的線條寬度、長度等於線條的實際長度，並以數學線線段為中心。</span><span class="sxs-lookup"><span data-stu-id="49812-130">If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment.</span></span> <span data-ttu-id="49812-131">每個片段的涵蓋範圍值是矩形區域與對應圖元正方形交集的視窗座標區域。</span><span class="sxs-lookup"><span data-stu-id="49812-131">The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square.</span></span> <span data-ttu-id="49812-132">此值會儲存並用於最後的點陣化步驟中。</span><span class="sxs-lookup"><span data-stu-id="49812-132">This value is saved and used in the final rasterization step.</span></span>

<span data-ttu-id="49812-133">啟用線條消除鋸齒功能時，並非所有寬度都可支援。</span><span class="sxs-lookup"><span data-stu-id="49812-133">Not all widths can be supported when line antialiasing is enabled.</span></span> <span data-ttu-id="49812-134">如果要求的寬度不受支援，則會使用最接近的支援寬度。</span><span class="sxs-lookup"><span data-stu-id="49812-134">If an unsupported width is requested, the nearest supported width is used.</span></span> <span data-ttu-id="49812-135">只保證支援寬度 1.0;其他則取決於執行。</span><span class="sxs-lookup"><span data-stu-id="49812-135">Only width 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="49812-136">您可以藉由呼叫 **glGet** 與引數 GL \_ 行 \_ 寬度 \_ 範圍和 GL \_ 行 \_ 寬度 \_ 的資料細微性，來查詢範圍中支援的寬度和大小差異。</span><span class="sxs-lookup"><span data-stu-id="49812-136">The range of supported widths and the size difference between supported widths within the range can be queried by calling **glGet** with arguments GL\_LINE\_WIDTH\_RANGE and GL\_LINE\_WIDTH\_GRANULARITY.</span></span>

<span data-ttu-id="49812-137">當查詢 GL 行寬時，一律會傳回 **glLineWidth** 所指定的線條寬度 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="49812-137">The line width specified by **glLineWidth** is always returned when GL\_LINE\_WIDTH is queried.</span></span> <span data-ttu-id="49812-138">別名和反鋸齒線條的固定和舍入不會影響指定的值。</span><span class="sxs-lookup"><span data-stu-id="49812-138">Clamping and rounding for aliased and antialiased lines have no effect on the specified value.</span></span>

<span data-ttu-id="49812-139">非反鋸齒線條寬度可能會壓制為與執行相關的最大值。</span><span class="sxs-lookup"><span data-stu-id="49812-139">Non-antialiased line width may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="49812-140">雖然無法查詢這個最大值，但它必須小於反鋸齒線的最大值，舍入到最接近的整數值。</span><span class="sxs-lookup"><span data-stu-id="49812-140">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.</span></span>

<span data-ttu-id="49812-141">下列函式會取出與 **glLineWidth** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="49812-141">The following functions retrieve information related to **glLineWidth**:</span></span>

<span data-ttu-id="49812-142">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 行 \_ 寬的 glGet</span><span class="sxs-lookup"><span data-stu-id="49812-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_WIDTH</span></span>

<span data-ttu-id="49812-143">具有引數 GL \_ 行 \_ 寬 \_ 範圍的 glGet</span><span class="sxs-lookup"><span data-stu-id="49812-143">**glGet** with argument GL\_LINE\_WIDTH\_RANGE</span></span>

<span data-ttu-id="49812-144">具有引數 GL \_ 行 \_ 寬 \_ 細微性的 glGet</span><span class="sxs-lookup"><span data-stu-id="49812-144">**glGet** with argument GL\_LINE\_WIDTH\_GRANULARITY</span></span>

<span data-ttu-id="49812-145">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 行 \_ 平滑</span><span class="sxs-lookup"><span data-stu-id="49812-145">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="49812-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="49812-146">Requirements</span></span>



| <span data-ttu-id="49812-147">需求</span><span class="sxs-lookup"><span data-stu-id="49812-147">Requirement</span></span> | <span data-ttu-id="49812-148">值</span><span class="sxs-lookup"><span data-stu-id="49812-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49812-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49812-149">Minimum supported client</span></span><br/> | <span data-ttu-id="49812-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49812-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="49812-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49812-151">Minimum supported server</span></span><br/> | <span data-ttu-id="49812-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49812-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49812-153">標頭</span><span class="sxs-lookup"><span data-stu-id="49812-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="49812-154"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="49812-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="49812-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="49812-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="49812-156"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="49812-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="49812-157">DLL</span><span class="sxs-lookup"><span data-stu-id="49812-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49812-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49812-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49812-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49812-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49812-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="49812-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="49812-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="49812-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="49812-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="49812-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="49812-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="49812-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





