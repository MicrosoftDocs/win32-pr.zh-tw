---
title: 'glScaled 函式 (Gl) '
description: 'GlScaled 和 glScalef 函數會將目前的矩陣乘以一般調整矩陣。 |glScaled 函式 (Gl) '
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- glScaled 函式 OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2655924f5716e142832882441066d4772d0e63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104563230"
---
# <a name="glscaled-function"></a><span data-ttu-id="014d9-105">glScaled 函式</span><span class="sxs-lookup"><span data-stu-id="014d9-105">glScaled function</span></span>

<span data-ttu-id="014d9-106">**GlScaled** 和 [**glScalef**](glscalef.md)函數會將目前的矩陣乘以一般調整矩陣。</span><span class="sxs-lookup"><span data-stu-id="014d9-106">The **glScaled** and [**glScalef**](glscalef.md) functions multiply the current matrix by a general scaling matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="014d9-107">語法</span><span class="sxs-lookup"><span data-stu-id="014d9-107">Syntax</span></span>


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="014d9-108">參數</span><span class="sxs-lookup"><span data-stu-id="014d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="014d9-109">*x*</span><span class="sxs-lookup"><span data-stu-id="014d9-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="014d9-110">沿著 *x* 軸的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="014d9-110">Scale factors along the *x* axis.</span></span>

</dd> <dt>

<span data-ttu-id="014d9-111">*y*</span><span class="sxs-lookup"><span data-stu-id="014d9-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="014d9-112">沿著 *y* 軸的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="014d9-112">Scale factors along the *y* axis.</span></span>

</dd> <dt>

<span data-ttu-id="014d9-113">*Z*</span><span class="sxs-lookup"><span data-stu-id="014d9-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="014d9-114">沿著 *z* 軸的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="014d9-114">Scale factors along the *z* axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="014d9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="014d9-115">Return value</span></span>

<span data-ttu-id="014d9-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="014d9-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="014d9-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="014d9-117">Error codes</span></span>

<span data-ttu-id="014d9-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="014d9-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="014d9-119">Name</span><span class="sxs-lookup"><span data-stu-id="014d9-119">Name</span></span>                                                                                                  | <span data-ttu-id="014d9-120">意義</span><span class="sxs-lookup"><span data-stu-id="014d9-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="014d9-121"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="014d9-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="014d9-122">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="014d9-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="014d9-123">備註</span><span class="sxs-lookup"><span data-stu-id="014d9-123">Remarks</span></span>

<span data-ttu-id="014d9-124">**GlScaled** 函式會沿著 *x*、 *y* 和 *z* 軸產生一般調整。</span><span class="sxs-lookup"><span data-stu-id="014d9-124">The **glScaled** function produces a general scaling along the *x*, *y*, and *z* axes.</span></span> <span data-ttu-id="014d9-125">三個引數會指出所需的縮放比例，以及三個軸的每一個。</span><span class="sxs-lookup"><span data-stu-id="014d9-125">The three arguments indicate the desired scale factors along each of the three axes.</span></span> <span data-ttu-id="014d9-126">產生的矩陣是</span><span class="sxs-lookup"><span data-stu-id="014d9-126">The resulting matrix is</span></span>

![此圖顯示沿著 x、y 和 Z 軸的縮放因數矩陣。](images/scale01.png)

<span data-ttu-id="014d9-128">目前的矩陣 (查看 [**glMatrixMode**](glmatrixmode.md)) 乘以此尺規矩陣，並將產品取代為目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="014d9-128">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this scale matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="014d9-129">也就是說，如果 M 是目前的矩陣，而 S 是尺規矩陣，則 M 會取代為 M S。</span><span class="sxs-lookup"><span data-stu-id="014d9-129">That is, if M is the current matrix and S is the scale matrix, then M is replaced with M   S.</span></span>

<span data-ttu-id="014d9-130">如果矩陣模式是 GL \_ 模型或 gl \_ 投射，則會呼叫 **glScaled** 之後繪製的所有物件。</span><span class="sxs-lookup"><span data-stu-id="014d9-130">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glScaled** is called are scaled.</span></span> <span data-ttu-id="014d9-131">使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) 來儲存及還原未縮放的座標系統。</span><span class="sxs-lookup"><span data-stu-id="014d9-131">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unscaled coordinate system.</span></span>

<span data-ttu-id="014d9-132">如果將1.0 以外的縮放因數套用至模型矩陣且已啟用光源，則應該也要啟用法線的自動正規化 ([**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) ，並將引數 GL \_ 標準化) 。</span><span class="sxs-lookup"><span data-stu-id="014d9-132">If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled ([**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_NORMALIZE).</span></span>

<span data-ttu-id="014d9-133">下列函式會取出與 **glScaled** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="014d9-133">The following functions retrieve information related to **glScaled**:</span></span>

<span data-ttu-id="014d9-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="014d9-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="014d9-135">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="014d9-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="014d9-136">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="014d9-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="014d9-137">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="014d9-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="014d9-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="014d9-138">Requirements</span></span>



| <span data-ttu-id="014d9-139">需求</span><span class="sxs-lookup"><span data-stu-id="014d9-139">Requirement</span></span> | <span data-ttu-id="014d9-140">值</span><span class="sxs-lookup"><span data-stu-id="014d9-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="014d9-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="014d9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="014d9-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="014d9-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="014d9-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="014d9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="014d9-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="014d9-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="014d9-145">標頭</span><span class="sxs-lookup"><span data-stu-id="014d9-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="014d9-146"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="014d9-146"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="014d9-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="014d9-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="014d9-148"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="014d9-148"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="014d9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="014d9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="014d9-150"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="014d9-150"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="014d9-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="014d9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014d9-152">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="014d9-152">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="014d9-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="014d9-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="014d9-154">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="014d9-154">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="014d9-155">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="014d9-155">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="014d9-156">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="014d9-156">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="014d9-157">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="014d9-157">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="014d9-158">**glRotated**</span><span class="sxs-lookup"><span data-stu-id="014d9-158">**glRotated**</span></span>](glrotated.md)
</dt> <dt>

[<span data-ttu-id="014d9-159">**glRotatef**</span><span class="sxs-lookup"><span data-stu-id="014d9-159">**glRotatef**</span></span>](glrotatef.md)
</dt> <dt>

[<span data-ttu-id="014d9-160">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="014d9-160">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





