---
title: 'glPopAttrib 函式 (Gl) '
description: 彈出屬性堆疊。
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glPopAttrib 函式 OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968171"
---
# <a name="glpopattrib-function"></a><span data-ttu-id="61f70-104">glPopAttrib 函式</span><span class="sxs-lookup"><span data-stu-id="61f70-104">glPopAttrib function</span></span>

<span data-ttu-id="61f70-105">彈出屬性堆疊。</span><span class="sxs-lookup"><span data-stu-id="61f70-105">Pops the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f70-106">語法</span><span class="sxs-lookup"><span data-stu-id="61f70-106">Syntax</span></span>


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="61f70-107">參數</span><span class="sxs-lookup"><span data-stu-id="61f70-107">Parameters</span></span>

<span data-ttu-id="61f70-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="61f70-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61f70-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="61f70-109">Return value</span></span>

<span data-ttu-id="61f70-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="61f70-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="61f70-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="61f70-111">Error codes</span></span>

<span data-ttu-id="61f70-112">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61f70-112">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="61f70-113">Name</span><span class="sxs-lookup"><span data-stu-id="61f70-113">Name</span></span>                                                                                                  | <span data-ttu-id="61f70-114">意義</span><span class="sxs-lookup"><span data-stu-id="61f70-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61f70-115"><dt>**GL \_ 堆疊 \_ 下溢**</dt></span><span class="sxs-lookup"><span data-stu-id="61f70-115"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="61f70-116">當屬性堆疊是空的時，就會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="61f70-116">The function was called while the attribute stack was empty.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="61f70-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="61f70-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="61f70-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="61f70-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="61f70-119">備註</span><span class="sxs-lookup"><span data-stu-id="61f70-119">Remarks</span></span>

<span data-ttu-id="61f70-120">[**GlPushAttrib**](glpushattrib.md)函式會採用一個引數，此遮罩會指出要在屬性堆疊上儲存的狀態變數群組。</span><span class="sxs-lookup"><span data-stu-id="61f70-120">The [**glPushAttrib**](glpushattrib.md) function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="61f70-121">符號常數用來設定遮罩中的位。</span><span class="sxs-lookup"><span data-stu-id="61f70-121">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="61f70-122">Mask 參數通常是由 **或** 將數個常陣列成。</span><span class="sxs-lookup"><span data-stu-id="61f70-122">The mask parameter is typically constructed by **OR** ing several of these constants together.</span></span> <span data-ttu-id="61f70-123">特殊遮罩 GL \_ 所有的 \_ ATTRIB \_ 位都可以用來儲存所有可堆疊的狀態。</span><span class="sxs-lookup"><span data-stu-id="61f70-123">The special mask GL\_ALL\_ATTRIB\_BITS can be used to save all stackable states.</span></span>

<span data-ttu-id="61f70-124">**GlPopAttrib** 函式會還原使用 last [**glPushAttrib**](glpushattrib.md)命令所儲存之狀態變數的值。</span><span class="sxs-lookup"><span data-stu-id="61f70-124">The **glPopAttrib** function restores the values of the state variables saved with the last [**glPushAttrib**](glpushattrib.md) command.</span></span> <span data-ttu-id="61f70-125">未儲存的會保持不變。</span><span class="sxs-lookup"><span data-stu-id="61f70-125">Those not saved are left unchanged.</span></span>

<span data-ttu-id="61f70-126">將屬性推送至完整堆疊，或從空白堆疊取出屬性是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="61f70-126">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="61f70-127">在任一種情況下，都會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。</span><span class="sxs-lookup"><span data-stu-id="61f70-127">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="61f70-128">一開始，屬性堆疊是空的。</span><span class="sxs-lookup"><span data-stu-id="61f70-128">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="61f70-129">並非所有 OpenGL 狀態的值都可以儲存在屬性堆疊上。</span><span class="sxs-lookup"><span data-stu-id="61f70-129">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="61f70-130">例如，您無法儲存圖元 pack 和解除封裝狀態、轉譯模式狀態，以及選取和意見反應狀態。</span><span class="sxs-lookup"><span data-stu-id="61f70-130">For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.</span></span>

<span data-ttu-id="61f70-131">屬性堆疊的深度取決於執行，但必須至少為16。</span><span class="sxs-lookup"><span data-stu-id="61f70-131">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="61f70-132">下列函式會取出 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="61f70-132">The following functions retrieve information related to [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**:</span></span>

<span data-ttu-id="61f70-133">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ATTRIB \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="61f70-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="61f70-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ ATTRIB 參數 \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="61f70-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="61f70-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="61f70-135">Requirements</span></span>



| <span data-ttu-id="61f70-136">需求</span><span class="sxs-lookup"><span data-stu-id="61f70-136">Requirement</span></span> | <span data-ttu-id="61f70-137">值</span><span class="sxs-lookup"><span data-stu-id="61f70-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61f70-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61f70-138">Minimum supported client</span></span><br/> | <span data-ttu-id="61f70-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61f70-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="61f70-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61f70-140">Minimum supported server</span></span><br/> | <span data-ttu-id="61f70-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61f70-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61f70-142">標頭</span><span class="sxs-lookup"><span data-stu-id="61f70-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="61f70-143"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="61f70-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="61f70-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="61f70-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="61f70-145"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61f70-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="61f70-146">DLL</span><span class="sxs-lookup"><span data-stu-id="61f70-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61f70-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61f70-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f70-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61f70-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f70-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="61f70-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="61f70-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="61f70-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="61f70-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="61f70-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="61f70-152">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="61f70-152">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="61f70-153">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="61f70-153">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="61f70-154">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="61f70-154">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="61f70-155">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="61f70-155">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="61f70-156">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="61f70-156">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="61f70-157">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="61f70-157">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="61f70-158">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="61f70-158">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="61f70-159">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="61f70-159">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="61f70-160">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="61f70-160">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="61f70-161">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="61f70-161">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="61f70-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="61f70-162">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="61f70-163">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="61f70-163">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="61f70-164">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="61f70-164">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="61f70-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="61f70-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





