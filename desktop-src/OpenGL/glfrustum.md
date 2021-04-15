---
title: 'glFrustum 函式 (Gl) '
description: GlFrustum 函式會將目前的矩陣乘以透視圖矩陣。
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glFrustum 函式 OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104554978"
---
# <a name="glfrustum-function"></a><span data-ttu-id="34fc1-104">glFrustum 函式</span><span class="sxs-lookup"><span data-stu-id="34fc1-104">glFrustum function</span></span>

<span data-ttu-id="34fc1-105">**GlFrustum** 函式會將目前的矩陣乘以透視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="34fc1-105">The **glFrustum** function multiplies the current matrix by a perspective matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="34fc1-106">語法</span><span class="sxs-lookup"><span data-stu-id="34fc1-106">Syntax</span></span>


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="34fc1-107">參數</span><span class="sxs-lookup"><span data-stu-id="34fc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34fc1-108">*離開*</span><span class="sxs-lookup"><span data-stu-id="34fc1-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="34fc1-109">左方垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="34fc1-109">The coordinate for the left-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="34fc1-110">*對*</span><span class="sxs-lookup"><span data-stu-id="34fc1-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="34fc1-111">右垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="34fc1-111">The coordinate for the right-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="34fc1-112">*底部*</span><span class="sxs-lookup"><span data-stu-id="34fc1-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="34fc1-113">下水準裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="34fc1-113">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="34fc1-114">*top*</span><span class="sxs-lookup"><span data-stu-id="34fc1-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="34fc1-115">下水準裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="34fc1-115">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="34fc1-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="34fc1-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="34fc1-117">接近深度裁剪平面的距離。</span><span class="sxs-lookup"><span data-stu-id="34fc1-117">The distances to the near-depth clipping plane.</span></span> <span data-ttu-id="34fc1-118">必須是正數。</span><span class="sxs-lookup"><span data-stu-id="34fc1-118">Must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="34fc1-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="34fc1-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="34fc1-120">距離最深度裁剪平面的距離。</span><span class="sxs-lookup"><span data-stu-id="34fc1-120">The distances to the far-depth clipping planes.</span></span> <span data-ttu-id="34fc1-121">必須是正數。</span><span class="sxs-lookup"><span data-stu-id="34fc1-121">Must be positive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34fc1-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="34fc1-122">Return value</span></span>

<span data-ttu-id="34fc1-123">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="34fc1-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34fc1-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="34fc1-124">Error codes</span></span>

<span data-ttu-id="34fc1-125">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="34fc1-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="34fc1-126">Name</span><span class="sxs-lookup"><span data-stu-id="34fc1-126">Name</span></span>                                                                                                  | <span data-ttu-id="34fc1-127">意義</span><span class="sxs-lookup"><span data-stu-id="34fc1-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34fc1-128"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="34fc1-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="34fc1-129">未 postitive *zNear* 或 *zFar* 。</span><span class="sxs-lookup"><span data-stu-id="34fc1-129">*zNear* or *zFar* was not postitive.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="34fc1-130"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="34fc1-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34fc1-131">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="34fc1-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="34fc1-132">備註</span><span class="sxs-lookup"><span data-stu-id="34fc1-132">Remarks</span></span>

<span data-ttu-id="34fc1-133">**GlFrustum** 函式描述會產生透視圖投影的透視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="34fc1-133">The **glFrustum** function describes a perspective matrix that produces a perspective projection.</span></span> <span data-ttu-id="34fc1-134"> (*left*、top\ **、 *zNear*) 和 (*righ\t*、 *top*、 *zNear*) 參數指定接近裁剪平面的點，這些點會分別對應至視窗左下角和右上角，並假設眼睛位於 (0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="34fc1-134">The (*left*, *bottom*, *zNear*) and (*right*, *top*, *zNear*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0,0,0).</span></span> <span data-ttu-id="34fc1-135">*ZFar* 參數會指定最遠裁剪平面的位置。</span><span class="sxs-lookup"><span data-stu-id="34fc1-135">The *zFar* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="34fc1-136">*ZNear* 和 *zFar* 都必須是正數。</span><span class="sxs-lookup"><span data-stu-id="34fc1-136">Both *zNear* and *zFar* must be positive.</span></span> <span data-ttu-id="34fc1-137">對應的矩陣如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="34fc1-137">The corresponding matrix is shown in the following image.</span></span>

![顯示產生觀點投射之透視圖矩陣的圖表。](images/frust01.png)![顯示描述透視圖矩陣之 glFrustum 函數的方程式。](images/frust02.png)

<span data-ttu-id="34fc1-140">**GlFrustum** 函式會將目前的矩陣乘以此矩陣，並將結果取代為目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="34fc1-140">The **glFrustum** function multiplies the current matrix by this matrix, with the result replacing the current matrix.</span></span> <span data-ttu-id="34fc1-141">也就是說，如果 M 是目前的矩陣，而 F 是截錐的觀點矩陣，則 **glFrustum** 會以 m F 取代 m。</span><span class="sxs-lookup"><span data-stu-id="34fc1-141">That is, if M is the current matrix and F is the frustum perspective matrix, then **glFrustum** replaces M with M   F.</span></span>

<span data-ttu-id="34fc1-142">使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) 來儲存和還原目前的矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="34fc1-142">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the current matrix stack.</span></span>

<span data-ttu-id="34fc1-143">深度緩衝區精確度會受到針對 *zNear* 和 *zFar* 指定的值所影響。</span><span class="sxs-lookup"><span data-stu-id="34fc1-143">Depth-buffer precision is affected by the values specified for *zNear* and *zFar*.</span></span> <span data-ttu-id="34fc1-144">*ZFar* 與 *zNear* 的比率愈大，深度緩衝區就越不會區分彼此接近的表面。</span><span class="sxs-lookup"><span data-stu-id="34fc1-144">The greater the ratio of *zFar* to *zNear* is, the less effective the depth buffer will be at distinguishing between surfaces that are near each other.</span></span> <span data-ttu-id="34fc1-145">如果</span><span class="sxs-lookup"><span data-stu-id="34fc1-145">If</span></span>

![顯示距離接近的比率的方程式。](images/frust03.png)

<span data-ttu-id="34fc1-147">大約 *記錄* 2 (*r*) 深度緩衝區精確度的位會遺失。</span><span class="sxs-lookup"><span data-stu-id="34fc1-147">roughly *log* 2 (*r*) bits of depth buffer precision are lost.</span></span> <span data-ttu-id="34fc1-148">因為 *r* 的 *zNear* 方法為零，所以不應該將 *zNear* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="34fc1-148">Because *r* approaches infinity as *zNear* approaches zero, you should never set *zNear* to zero.</span></span>

<span data-ttu-id="34fc1-149">下列函式會取出 **glFrustum** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="34fc1-149">The following functions retrieve information about **glFrustum**:</span></span>

<span data-ttu-id="34fc1-150">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="34fc1-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="34fc1-151">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="34fc1-151">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="34fc1-152">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="34fc1-152">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="34fc1-153">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="34fc1-153">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="34fc1-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="34fc1-154">Requirements</span></span>



| <span data-ttu-id="34fc1-155">需求</span><span class="sxs-lookup"><span data-stu-id="34fc1-155">Requirement</span></span> | <span data-ttu-id="34fc1-156">值</span><span class="sxs-lookup"><span data-stu-id="34fc1-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34fc1-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34fc1-157">Minimum supported client</span></span><br/> | <span data-ttu-id="34fc1-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34fc1-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="34fc1-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34fc1-159">Minimum supported server</span></span><br/> | <span data-ttu-id="34fc1-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34fc1-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34fc1-161">標頭</span><span class="sxs-lookup"><span data-stu-id="34fc1-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="34fc1-162"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="34fc1-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="34fc1-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="34fc1-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="34fc1-164"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="34fc1-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="34fc1-165">DLL</span><span class="sxs-lookup"><span data-stu-id="34fc1-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34fc1-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34fc1-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34fc1-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34fc1-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34fc1-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="34fc1-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="34fc1-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="34fc1-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="34fc1-170">**glGet**</span><span class="sxs-lookup"><span data-stu-id="34fc1-170">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="34fc1-171">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="34fc1-171">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="34fc1-172">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="34fc1-172">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="34fc1-173">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="34fc1-173">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="34fc1-174">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="34fc1-174">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="34fc1-175">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="34fc1-175">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="34fc1-176">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="34fc1-176">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





