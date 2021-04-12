---
title: 'glRenderMode 函式 (Gl) '
description: GlRenderMode 函式會設定點陣化模式。
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glRenderMode 函式 OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106199"
---
# <a name="glrendermode-function"></a><span data-ttu-id="3fd1b-104">glRenderMode 函式</span><span class="sxs-lookup"><span data-stu-id="3fd1b-104">glRenderMode function</span></span>

<span data-ttu-id="3fd1b-105">**GlRenderMode** 函式會設定點陣化模式。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-105">The **glRenderMode** function sets the rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd1b-106">語法</span><span class="sxs-lookup"><span data-stu-id="3fd1b-106">Syntax</span></span>


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="3fd1b-107">參數</span><span class="sxs-lookup"><span data-stu-id="3fd1b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd1b-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="3fd1b-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd1b-109">點陣化模式。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-109">The rasterization mode.</span></span> <span data-ttu-id="3fd1b-110">接受下列三個值。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-110">The following three values are accepted.</span></span> <span data-ttu-id="3fd1b-111">預設值為 GL \_ RENDER。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-111">The default value is GL\_RENDER.</span></span>



| <span data-ttu-id="3fd1b-112">值</span><span class="sxs-lookup"><span data-stu-id="3fd1b-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="3fd1b-113">意義</span><span class="sxs-lookup"><span data-stu-id="3fd1b-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <span data-ttu-id="3fd1b-114"><dt>**GL \_ 轉譯**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-114"><dt>**GL\_RENDER**</dt></span></span> </dl>       | <span data-ttu-id="3fd1b-115">轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-115">Render mode.</span></span> <span data-ttu-id="3fd1b-116">基本專案會進行柵格化，並產生會寫入畫面格緩衝區中的圖元片段。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-116">Primitives are rasterized, producing pixel fragments, which are written into the framebuffer.</span></span> <span data-ttu-id="3fd1b-117">這是一般模式，也是預設模式。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-117">This is the normal mode and also the default mode.</span></span><br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <span data-ttu-id="3fd1b-118"><dt>**GL \_ 選取**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-118"><dt>**GL\_SELECT**</dt></span></span> </dl>       | <span data-ttu-id="3fd1b-119">選取模式。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-119">Selection mode.</span></span> <span data-ttu-id="3fd1b-120">不會產生任何圖元片段，也不會對畫面格緩衝區內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-120">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="3fd1b-121">相反地，當轉譯模式為 GL 轉譯時，所要繪製的基本名稱記錄 \_ ，會在選取的緩衝區中傳回， (在輸入選取模式之前，請參閱 [**glSelectBuffer**](glselectbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-121">Instead, a record of the names of primitives that would have been drawn if the render mode was GL\_RENDER is returned in a select buffer, which must be created (see [**glSelectBuffer**](glselectbuffer.md)) before selection mode is entered.</span></span><br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <span data-ttu-id="3fd1b-122"><dt>**GL \_ 意見反應**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-122"><dt>**GL\_FEEDBACK**</dt></span></span> </dl> | <span data-ttu-id="3fd1b-123">意見反應模式。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-123">Feedback mode.</span></span> <span data-ttu-id="3fd1b-124">不會產生任何圖元片段，也不會對畫面格緩衝區內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-124">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="3fd1b-125">相反地，已繪製之頂點的座標和屬性 \_ 會在意見反應緩衝區中傳回，該緩衝區必須建立， (在輸入意見反應模式之前，請參閱 [**glFeedbackBuffer**](glfeedbackbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-125">Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL\_RENDER are returned in a feedback buffer, which must be created (see [**glFeedbackBuffer**](glfeedbackbuffer.md)) before feedback mode is entered.</span></span><br/> |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="3fd1b-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3fd1b-126">Error codes</span></span>

<span data-ttu-id="3fd1b-127">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3fd1b-128">Name</span><span class="sxs-lookup"><span data-stu-id="3fd1b-128">Name</span></span>                                                                                                  | <span data-ttu-id="3fd1b-129">意義</span><span class="sxs-lookup"><span data-stu-id="3fd1b-129">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3fd1b-130"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3fd1b-131">*模式* 不是三個接受的值之一。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-131">*mode* was not one of three accepted values.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="3fd1b-132"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3fd1b-133">呼叫函式時，會使用引數 GL SELECT 來呼叫該函式， \_ 然後至少呼叫 [**glSelectBuffer**](glselectbuffer.md) 一次。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-133">The function was called with argument GL\_SELECT before [**glSelectBuffer**](glselectbuffer.md) was called at least once.</span></span><br/>       |
| <dl> <span data-ttu-id="3fd1b-134"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3fd1b-135">在 \_ 呼叫至少一次 [**glBeedbackBuffer**](glfeedbackbuffer.md) 之前，會使用引數 GL 回饋來呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-135">The function was called with argument GL\_FEEDBACK before [**glBeedbackBuffer**](glfeedbackbuffer.md) was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="3fd1b-136"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3fd1b-137">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="3fd1b-138">備註</span><span class="sxs-lookup"><span data-stu-id="3fd1b-138">Remarks</span></span>

<span data-ttu-id="3fd1b-139">**GlRenderMode** 函式會採用一個引數，也就是可採用上述三個預先定義值之一的 *模式*。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-139">The **glRenderMode** function takes one argument, *mode*, which can assume one of three predefined values above.</span></span>

<span data-ttu-id="3fd1b-140">**GlRenderMode** 函式的傳回值是由在呼叫 **glRenderMode** 時的轉譯模式來決定，而不是透過 *模式* 來決定。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-140">The return value of the **glRenderMode** function is determined by the render mode at the time **glRenderMode** is called, rather than by *mode*.</span></span> <span data-ttu-id="3fd1b-141">針對三種轉譯模式傳回的值如下所示。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-141">The values returned for the three render modes are as follows.</span></span>



| <span data-ttu-id="3fd1b-142">值</span><span class="sxs-lookup"><span data-stu-id="3fd1b-142">Value</span></span>        | <span data-ttu-id="3fd1b-143">意義</span><span class="sxs-lookup"><span data-stu-id="3fd1b-143">Meaning</span></span>                                                                 |
|--------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3fd1b-144">GL \_ 轉譯</span><span class="sxs-lookup"><span data-stu-id="3fd1b-144">GL\_RENDER</span></span>   | <span data-ttu-id="3fd1b-145">零個。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-145">Zero.</span></span>                                                                   |
| <span data-ttu-id="3fd1b-146">GL \_ 選取</span><span class="sxs-lookup"><span data-stu-id="3fd1b-146">GL\_SELECT</span></span>   | <span data-ttu-id="3fd1b-147">傳送至選取緩衝區的點擊記錄數。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-147">The number of hit records transferred to the select buffer.</span></span>             |
| <span data-ttu-id="3fd1b-148">GL \_ 意見反應</span><span class="sxs-lookup"><span data-stu-id="3fd1b-148">GL\_FEEDBACK</span></span> | <span data-ttu-id="3fd1b-149"> (不是頂點的值數目) 傳送至意見緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-149">The number of values (not vertices) transferred to the feedback buffer.</span></span> |



 

<span data-ttu-id="3fd1b-150">如需有關選取專案和意見反應作業的詳細資訊，請參閱 [**glSelectBuffer**](glselectbuffer.md) 和 [**glFeedbackBuffer**](glfeedbackbuffer.md) 。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-150">Refer to [**glSelectBuffer**](glselectbuffer.md) and [**glFeedbackBuffer**](glfeedbackbuffer.md) for more details concerning selection and feedback operation.</span></span>

<span data-ttu-id="3fd1b-151">如果產生錯誤，不論目前的轉譯模式為何， **glRenderMode** 都會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3fd1b-151">If an error is generated, **glRenderMode** returns zero regardless of the current render mode.</span></span>

<span data-ttu-id="3fd1b-152">下列函式會抓取 **glRenderMode** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="3fd1b-152">The following function retrieves information related to **glRenderMode**:</span></span>

<span data-ttu-id="3fd1b-153">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 轉譯 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="3fd1b-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd1b-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fd1b-154">Requirements</span></span>



| <span data-ttu-id="3fd1b-155">需求</span><span class="sxs-lookup"><span data-stu-id="3fd1b-155">Requirement</span></span> | <span data-ttu-id="3fd1b-156">值</span><span class="sxs-lookup"><span data-stu-id="3fd1b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd1b-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fd1b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd1b-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fd1b-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3fd1b-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fd1b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd1b-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fd1b-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3fd1b-161">標頭</span><span class="sxs-lookup"><span data-stu-id="3fd1b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd1b-162"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3fd1b-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="3fd1b-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="3fd1b-164"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3fd1b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd1b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fd1b-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fd1b-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd1b-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fd1b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd1b-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3fd1b-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3fd1b-170">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-170">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="3fd1b-171">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-171">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="3fd1b-172">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-172">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="3fd1b-173">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-173">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="3fd1b-174">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-174">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="3fd1b-175">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="3fd1b-175">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





