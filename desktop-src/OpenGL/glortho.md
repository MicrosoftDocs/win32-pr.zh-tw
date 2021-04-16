---
title: 'glOrtho 函式 (Gl) '
description: GlOrtho 函式會將目前的矩陣乘以正向矩陣。
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glOrtho 函式 OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104553311"
---
# <a name="glortho-function"></a><span data-ttu-id="cfd0b-104">glOrtho 函式</span><span class="sxs-lookup"><span data-stu-id="cfd0b-104">glOrtho function</span></span>

<span data-ttu-id="cfd0b-105">**GlOrtho** 函式會將目前的矩陣乘以正向矩陣。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-105">The **glOrtho** function multiplies the current matrix by an orthographic matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd0b-106">語法</span><span class="sxs-lookup"><span data-stu-id="cfd0b-106">Syntax</span></span>


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="cfd0b-107">參數</span><span class="sxs-lookup"><span data-stu-id="cfd0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd0b-108">*離開*</span><span class="sxs-lookup"><span data-stu-id="cfd0b-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd0b-109">左方垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-109">The coordinates for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="cfd0b-110">*對*</span><span class="sxs-lookup"><span data-stu-id="cfd0b-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd0b-111">Theright 垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-111">The coordinates for theright vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="cfd0b-112">*底部*</span><span class="sxs-lookup"><span data-stu-id="cfd0b-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd0b-113">底部水準裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-113">The coordinates for the bottom horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="cfd0b-114">*top*</span><span class="sxs-lookup"><span data-stu-id="cfd0b-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd0b-115">上方水準裁剪計畫的座標。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-115">The coordinates for the top horizontal clipping plans.</span></span>

</dd> <dt>

<span data-ttu-id="cfd0b-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="cfd0b-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd0b-117">靠近深度裁剪平面的距離。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-117">The distances to the nearer depth clipping plane.</span></span> <span data-ttu-id="cfd0b-118">如果平面位於檢視器後方，此距離就會是負數。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-118">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> <dt>

<span data-ttu-id="cfd0b-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="cfd0b-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd0b-120">距離深度裁剪平面的距離。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-120">The distances to the farther depth clipping plane.</span></span> <span data-ttu-id="cfd0b-121">如果平面位於檢視器後方，此距離就會是負數。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-121">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd0b-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfd0b-122">Return value</span></span>

<span data-ttu-id="cfd0b-123">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cfd0b-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cfd0b-124">Error codes</span></span>

<span data-ttu-id="cfd0b-125">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-125">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cfd0b-126">Name</span><span class="sxs-lookup"><span data-stu-id="cfd0b-126">Name</span></span>                                                                                                  | <span data-ttu-id="cfd0b-127">意義</span><span class="sxs-lookup"><span data-stu-id="cfd0b-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfd0b-128"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="cfd0b-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cfd0b-129">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cfd0b-130">備註</span><span class="sxs-lookup"><span data-stu-id="cfd0b-130">Remarks</span></span>

<span data-ttu-id="cfd0b-131">**GlOrtho** 函數描述產生平行投影的透視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-131">The **glOrtho** function describes a perspective matrix that produces a parallel projection.</span></span> <span data-ttu-id="cfd0b-132"> (*左方*、 *底部*、 *接近*) 和 (*right*、 *top*、 *near*) 參數指定接近裁剪平面的點，這些點會分別對應至視窗左下角和右上角，並假設眼睛位於 (0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-132">The (*left*, *bottom*, *near*) and (*right*, *top*, *near*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0).</span></span> <span data-ttu-id="cfd0b-133">最 *遠* 的參數會指定最遠裁剪平面的位置。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-133">The *far* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="cfd0b-134">*ZNear* 和 *zFar* 都可以是正數或負數。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-134">Both *zNear* and *zFar* can be either positive or negative.</span></span> <span data-ttu-id="cfd0b-135">對應的矩陣如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-135">The corresponding matrix is shown in the following image.</span></span>

![此圖顯示 glOrtho 函式所描述的透視圖矩陣。](images/ortho1.png)

<span data-ttu-id="cfd0b-137">其中</span><span class="sxs-lookup"><span data-stu-id="cfd0b-137">where</span></span>

![描述透視圖矩陣的方。](images/ortho2.png)

<span data-ttu-id="cfd0b-139">目前的矩陣會乘以此矩陣，且結果會取代目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-139">The current matrix is multiplied by this matrix with the result replacing the current matrix.</span></span> <span data-ttu-id="cfd0b-140">也就是說，如果 M 是目前的矩陣，而 O 是 ortho 矩陣，則 M 會取代為 M O。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-140">That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M   O.</span></span>

<span data-ttu-id="cfd0b-141">使用 [**glPushMatrix**](glpushmatrix.md) 和 **glPopMatrix** 來儲存和還原目前的矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-141">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the current matrix stack.</span></span> <span data-ttu-id="cfd0b-142">使用 [**glMatrixMode**](glmatrixmode.md) 來設定目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="cfd0b-142">Use [**glMatrixMode**](glmatrixmode.md) to set the current matrix.</span></span>

<span data-ttu-id="cfd0b-143">下列函式會取出與 **glOrtho** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="cfd0b-143">The following functions retrieve information related to **glOrtho**:</span></span>

<span data-ttu-id="cfd0b-144">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="cfd0b-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="cfd0b-145">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="cfd0b-145">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="cfd0b-146">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="cfd0b-146">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="cfd0b-147">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="cfd0b-147">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd0b-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfd0b-148">Requirements</span></span>



| <span data-ttu-id="cfd0b-149">需求</span><span class="sxs-lookup"><span data-stu-id="cfd0b-149">Requirement</span></span> | <span data-ttu-id="cfd0b-150">值</span><span class="sxs-lookup"><span data-stu-id="cfd0b-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd0b-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfd0b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="cfd0b-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfd0b-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cfd0b-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfd0b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="cfd0b-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfd0b-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cfd0b-155">標頭</span><span class="sxs-lookup"><span data-stu-id="cfd0b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfd0b-156"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="cfd0b-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cfd0b-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="cfd0b-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="cfd0b-158"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfd0b-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cfd0b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="cfd0b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfd0b-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfd0b-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd0b-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfd0b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd0b-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cfd0b-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cfd0b-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cfd0b-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cfd0b-164">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="cfd0b-164">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="cfd0b-165">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="cfd0b-165">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="cfd0b-166">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="cfd0b-166">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="cfd0b-167">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="cfd0b-167">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="cfd0b-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="cfd0b-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





