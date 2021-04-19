---
title: 'glPopMatrix 函式 (Gl) '
description: 'GlPushMatrix 和 glPopMatrix 函式會推送並取出目前的矩陣堆疊。 |glPopMatrix 函式 (Gl) '
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- glPopMatrix 函式 OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106975625"
---
# <a name="glpopmatrix-function"></a><span data-ttu-id="9d61d-105">glPopMatrix 函式</span><span class="sxs-lookup"><span data-stu-id="9d61d-105">glPopMatrix function</span></span>

<span data-ttu-id="9d61d-106">[**GlPushMatrix**](glpushmatrix.md)和 **glPopMatrix** 函式會推送並取出目前的矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="9d61d-106">The [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d61d-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d61d-107">Syntax</span></span>


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="9d61d-108">參數</span><span class="sxs-lookup"><span data-stu-id="9d61d-108">Parameters</span></span>

<span data-ttu-id="9d61d-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="9d61d-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d61d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d61d-110">Return value</span></span>

<span data-ttu-id="9d61d-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9d61d-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d61d-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9d61d-112">Error codes</span></span>

<span data-ttu-id="9d61d-113">推送完整的矩陣堆疊或 pop 只包含單一矩陣的矩陣堆疊是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="9d61d-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="9d61d-114">在任一種情況下，都會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。</span><span class="sxs-lookup"><span data-stu-id="9d61d-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="9d61d-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9d61d-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9d61d-116">Name</span><span class="sxs-lookup"><span data-stu-id="9d61d-116">Name</span></span>                                                                                                  | <span data-ttu-id="9d61d-117">意義</span><span class="sxs-lookup"><span data-stu-id="9d61d-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d61d-118"><dt>**GL \_ 堆疊 \_ 下溢**</dt></span><span class="sxs-lookup"><span data-stu-id="9d61d-118"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="9d61d-119">當目前的矩陣堆疊只包含單一矩陣時，會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="9d61d-119">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="9d61d-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="9d61d-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9d61d-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="9d61d-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9d61d-122">備註</span><span class="sxs-lookup"><span data-stu-id="9d61d-122">Remarks</span></span>

<span data-ttu-id="9d61d-123">每個矩陣模式都有一個矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="9d61d-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="9d61d-124">在 GL \_ 模型模式中，堆疊深度至少為32。</span><span class="sxs-lookup"><span data-stu-id="9d61d-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="9d61d-125">在其他兩種模式中，則 \_ 是 gl 投射和 gl \_ 材質，深度至少是2。</span><span class="sxs-lookup"><span data-stu-id="9d61d-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="9d61d-126">在任何模式下，目前的矩陣都是該模式之堆疊頂端的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9d61d-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="9d61d-127">[**GlPushMatrix**](glpushmatrix.md)函式會將目前的矩陣堆疊向下推一，以複製目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9d61d-127">The [**glPushMatrix**](glpushmatrix.md) function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="9d61d-128">也就是說，在 **glPushMatrix** 呼叫之後，堆疊頂端的矩陣與下面的矩陣相同。</span><span class="sxs-lookup"><span data-stu-id="9d61d-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="9d61d-129">**GlPopMatrix** 函式會取出目前的矩陣堆疊，並將目前的矩陣取代為堆疊上的下一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="9d61d-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="9d61d-130">一開始，每個堆疊都會包含一個矩陣，也就是一個識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="9d61d-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="9d61d-131">下列函式會取出 [**glPushMatrix**](glpushmatrix.md) 和 **glPopMatrix** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="9d61d-131">The following functions retrieve information related to [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix**:</span></span>

<span data-ttu-id="9d61d-132">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="9d61d-133">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="9d61d-134">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="9d61d-135">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="9d61d-136">具有引數 GL \_ 模型 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="9d61d-137">具有引數 GL \_ 投射 \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="9d61d-138">具有引數 GL \_ 紋理 \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="9d61d-139">具有引數 GL \_ 最大 \_ 模型 \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="9d61d-140">具有引數 GL \_ 最大 \_ 投射 \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="9d61d-141">具有引數 GL \_ 最大 \_ 材質 \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="9d61d-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="9d61d-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d61d-142">Requirements</span></span>



| <span data-ttu-id="9d61d-143">需求</span><span class="sxs-lookup"><span data-stu-id="9d61d-143">Requirement</span></span> | <span data-ttu-id="9d61d-144">值</span><span class="sxs-lookup"><span data-stu-id="9d61d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d61d-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d61d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9d61d-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d61d-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d61d-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d61d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9d61d-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d61d-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d61d-149">標頭</span><span class="sxs-lookup"><span data-stu-id="9d61d-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d61d-150"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="9d61d-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9d61d-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d61d-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d61d-152"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d61d-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d61d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="9d61d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d61d-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d61d-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d61d-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d61d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d61d-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9d61d-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9d61d-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9d61d-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9d61d-158">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="9d61d-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="9d61d-159">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="9d61d-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="9d61d-160">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="9d61d-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="9d61d-161">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="9d61d-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="9d61d-162">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="9d61d-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="9d61d-163">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="9d61d-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="9d61d-164">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="9d61d-164">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="9d61d-165">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="9d61d-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="9d61d-166">**glScale**</span><span class="sxs-lookup"><span data-stu-id="9d61d-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="9d61d-167">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="9d61d-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="9d61d-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="9d61d-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





