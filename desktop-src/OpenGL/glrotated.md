---
title: 'glRotated 函式 (Gl) '
description: GlRotated 函式會將目前的矩陣乘以旋轉矩陣。
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- glRotated 函式 OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0678e9da6f0b68047708f45fda1c9da66d8139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509411"
---
# <a name="glrotated-function"></a><span data-ttu-id="5d359-104">glRotated 函式</span><span class="sxs-lookup"><span data-stu-id="5d359-104">glRotated function</span></span>

<span data-ttu-id="5d359-105">**GlRotated** 函式會將目前的矩陣乘以旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="5d359-105">The **glRotated** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d359-106">語法</span><span class="sxs-lookup"><span data-stu-id="5d359-106">Syntax</span></span>


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="5d359-107">參數</span><span class="sxs-lookup"><span data-stu-id="5d359-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d359-108">*角度*</span><span class="sxs-lookup"><span data-stu-id="5d359-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="5d359-109">旋轉的角度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d359-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="5d359-110">*x*</span><span class="sxs-lookup"><span data-stu-id="5d359-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="5d359-111">向量的 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="5d359-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="5d359-112">*y*</span><span class="sxs-lookup"><span data-stu-id="5d359-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="5d359-113">向量的 *y* 座標。</span><span class="sxs-lookup"><span data-stu-id="5d359-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="5d359-114">*Z*</span><span class="sxs-lookup"><span data-stu-id="5d359-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="5d359-115">向量的 *z* 座標。</span><span class="sxs-lookup"><span data-stu-id="5d359-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d359-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d359-116">Return value</span></span>

<span data-ttu-id="5d359-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5d359-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d359-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5d359-118">Error codes</span></span>

<span data-ttu-id="5d359-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5d359-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5d359-120">Name</span><span class="sxs-lookup"><span data-stu-id="5d359-120">Name</span></span>                                                                                                  | <span data-ttu-id="5d359-121">意義</span><span class="sxs-lookup"><span data-stu-id="5d359-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d359-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="5d359-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5d359-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="5d359-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5d359-124">備註</span><span class="sxs-lookup"><span data-stu-id="5d359-124">Remarks</span></span>

<span data-ttu-id="5d359-125">**GlRotated** 函式會計算矩陣，此矩陣會執行從原點到 (*x*、 *y*、 *z*) 點之向量的旋轉 *角度* 度數。</span><span class="sxs-lookup"><span data-stu-id="5d359-125">The **glRotated** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="5d359-126">目前的矩陣 (查看 [**glMatrixMode**](glmatrixmode.md)) 乘以這個旋轉矩陣，並將產品取代為目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="5d359-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="5d359-127">也就是說，如果 M 是目前的矩陣，而 R 是轉譯矩陣，則 M 會取代為 M R。</span><span class="sxs-lookup"><span data-stu-id="5d359-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="5d359-128">如果矩陣模式是 GL \_ 模型或 gl \_ 投射，則會呼叫 **glRotated** 之後繪製的所有物件。</span><span class="sxs-lookup"><span data-stu-id="5d359-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotated** is called are rotated.</span></span> <span data-ttu-id="5d359-129">使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) 來儲存及還原未旋轉的座標系統。</span><span class="sxs-lookup"><span data-stu-id="5d359-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="5d359-130">下列函式會取出與 **glRotated** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="5d359-130">The following functions retrieve information related to **glRotated**:</span></span>

<span data-ttu-id="5d359-131">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 轉譯 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="5d359-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="5d359-132">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="5d359-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="5d359-133">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="5d359-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="5d359-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="5d359-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="5d359-135">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="5d359-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="5d359-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d359-136">Requirements</span></span>



| <span data-ttu-id="5d359-137">需求</span><span class="sxs-lookup"><span data-stu-id="5d359-137">Requirement</span></span> | <span data-ttu-id="5d359-138">值</span><span class="sxs-lookup"><span data-stu-id="5d359-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d359-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d359-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5d359-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d359-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5d359-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d359-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5d359-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d359-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d359-143">標頭</span><span class="sxs-lookup"><span data-stu-id="5d359-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d359-144"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="5d359-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5d359-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="5d359-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d359-146"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d359-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5d359-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5d359-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d359-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d359-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d359-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d359-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d359-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5d359-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5d359-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5d359-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5d359-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="5d359-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="5d359-153">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="5d359-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="5d359-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="5d359-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="5d359-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="5d359-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="5d359-156">**glScale**</span><span class="sxs-lookup"><span data-stu-id="5d359-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="5d359-157">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="5d359-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





