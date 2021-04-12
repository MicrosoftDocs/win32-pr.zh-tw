---
title: 'glDepthFunc 函式 (Gl) '
description: GlDepthFunc 函數會指定用於深度緩衝區比較的值。
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- glDepthFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464725"
---
# <a name="gldepthfunc-function"></a><span data-ttu-id="5d8e8-104">glDepthFunc 函式</span><span class="sxs-lookup"><span data-stu-id="5d8e8-104">glDepthFunc function</span></span>

<span data-ttu-id="5d8e8-105">**GlDepthFunc** 函數會指定用於深度緩衝區比較的值。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-105">The **glDepthFunc** function specifies the value used for depth-buffer comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d8e8-106">語法</span><span class="sxs-lookup"><span data-stu-id="5d8e8-106">Syntax</span></span>


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a><span data-ttu-id="5d8e8-107">參數</span><span class="sxs-lookup"><span data-stu-id="5d8e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d8e8-108">*func*</span><span class="sxs-lookup"><span data-stu-id="5d8e8-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="5d8e8-109">指定深度比較函數。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-109">Specifies the depth-comparison function.</span></span> <span data-ttu-id="5d8e8-110">接受下列符號常數。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-110">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="5d8e8-111">值</span><span class="sxs-lookup"><span data-stu-id="5d8e8-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="5d8e8-112">意義</span><span class="sxs-lookup"><span data-stu-id="5d8e8-112">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="5d8e8-113"><dt>**GL \_ 永不**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="5d8e8-114">永遠不會通過。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-114">Never passes.</span></span><br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="5d8e8-115"><dt>**GL \_ LESS**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="5d8e8-116">如果連入的 *z* 值小於儲存的 *z* 值，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-116">Passes if the incoming *z* value is less than the stored *z* value.</span></span> <span data-ttu-id="5d8e8-117">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-117">This is the default value.</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="5d8e8-118"><dt>**GL \_ LEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-118"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="5d8e8-119">如果連入的 z 值小於或等於儲存的 z 值，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-119">Passes if the incoming z value is less than or equal to the stored z value.</span></span><br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="5d8e8-120"><dt>**GL \_ 相等**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-120"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="5d8e8-121">如果連入的 z 值等於儲存的 z 值，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-121">Passes if the incoming z value is equal to the stored z value.</span></span><br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="5d8e8-122"><dt>**GL \_ 更高**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-122"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="5d8e8-123">如果連入的 z 值大於儲存的 z 值，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-123">Passes if the incoming z value is greater than the stored z value.</span></span><br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="5d8e8-124"><dt>**GL \_ NOTEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-124"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="5d8e8-125">如果連入的 z 值不等於儲存的 z 值，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-125">Passes if the incoming z value is not equal to the stored z value.</span></span><br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="5d8e8-126"><dt>**GL \_ GEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-126"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="5d8e8-127">如果連入的 z 值大於或等於儲存的 z 值，則會傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-127">Passes if the incoming z value is greater than or equal to the stored z value.</span></span><br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="5d8e8-128"><dt>**GL \_ 一律**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="5d8e8-129">一律傳遞。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-129">Always passes.</span></span><br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d8e8-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d8e8-130">Return value</span></span>

<span data-ttu-id="5d8e8-131">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d8e8-132">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5d8e8-132">Error codes</span></span>

<span data-ttu-id="5d8e8-133">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-133">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5d8e8-134">Name</span><span class="sxs-lookup"><span data-stu-id="5d8e8-134">Name</span></span>                                                                                                  | <span data-ttu-id="5d8e8-135">意義</span><span class="sxs-lookup"><span data-stu-id="5d8e8-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d8e8-136"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5d8e8-137">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5d8e8-138">備註</span><span class="sxs-lookup"><span data-stu-id="5d8e8-138">Remarks</span></span>

<span data-ttu-id="5d8e8-139">**GlDepthFunc** 函式會指定用來比較每個內送圖元 *z* 值與深度緩衝區中的 *z* 值的函式。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-139">The **glDepthFunc** function specifies the function used to compare each incoming pixel *z* value with the *z* value present in the depth buffer.</span></span> <span data-ttu-id="5d8e8-140">只有在啟用深度測試時，才會執行比較。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-140">The comparison is performed only if depth testing is enabled.</span></span> <span data-ttu-id="5d8e8-141"> (參閱[](glenable.md)具有引數 GL \_ 深度測試的 glEnable \_ 。 ) </span><span class="sxs-lookup"><span data-stu-id="5d8e8-141">(See [**glEnable**](glenable.md) with the argument GL\_DEPTH\_TEST.)</span></span>

<span data-ttu-id="5d8e8-142">一開始，深度測試已停用。</span><span class="sxs-lookup"><span data-stu-id="5d8e8-142">Initially, depth testing is disabled.</span></span>

<span data-ttu-id="5d8e8-143">下列函式會取出與 **glDepthFunc** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="5d8e8-143">The following functions retrieve information related to **glDepthFunc**:</span></span>

<span data-ttu-id="5d8e8-144">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 深度 \_ FUNC 的 glGet</span><span class="sxs-lookup"><span data-stu-id="5d8e8-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_FUNC</span></span>

<span data-ttu-id="5d8e8-145">[](glisenabled.md)具有引數 GL \_ 深度 \_ 測試的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="5d8e8-145">[**glIsEnabled**](glisenabled.md) with argument GL\_DEPTH\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="5d8e8-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d8e8-146">Requirements</span></span>



| <span data-ttu-id="5d8e8-147">需求</span><span class="sxs-lookup"><span data-stu-id="5d8e8-147">Requirement</span></span> | <span data-ttu-id="5d8e8-148">值</span><span class="sxs-lookup"><span data-stu-id="5d8e8-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8e8-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d8e8-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5d8e8-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d8e8-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5d8e8-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d8e8-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5d8e8-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d8e8-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d8e8-153">標頭</span><span class="sxs-lookup"><span data-stu-id="5d8e8-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d8e8-154"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5d8e8-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="5d8e8-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d8e8-156"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5d8e8-157">DLL</span><span class="sxs-lookup"><span data-stu-id="5d8e8-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d8e8-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d8e8-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d8e8-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d8e8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8e8-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5d8e8-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5d8e8-161">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="5d8e8-161">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="5d8e8-162">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="5d8e8-162">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="5d8e8-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5d8e8-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5d8e8-164">**glGet**</span><span class="sxs-lookup"><span data-stu-id="5d8e8-164">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="5d8e8-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5d8e8-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





