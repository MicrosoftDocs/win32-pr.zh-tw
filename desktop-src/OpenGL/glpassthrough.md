---
title: 'glPassThrough 函式 (Gl) '
description: GlPassThrough 函式會在意見緩衝區中放置標記。
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glPassThrough 函式 OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685816"
---
# <a name="glpassthrough-function"></a><span data-ttu-id="cb69a-104">glPassThrough 函式</span><span class="sxs-lookup"><span data-stu-id="cb69a-104">glPassThrough function</span></span>

<span data-ttu-id="cb69a-105">**GlPassThrough** 函式會在意見緩衝區中放置標記。</span><span class="sxs-lookup"><span data-stu-id="cb69a-105">The **glPassThrough** function places a marker in the feedback buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb69a-106">語法</span><span class="sxs-lookup"><span data-stu-id="cb69a-106">Syntax</span></span>


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a><span data-ttu-id="cb69a-107">參數</span><span class="sxs-lookup"><span data-stu-id="cb69a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb69a-108">*token*</span><span class="sxs-lookup"><span data-stu-id="cb69a-108">*token*</span></span> 
</dt> <dd>

<span data-ttu-id="cb69a-109">要放置在意見緩衝區中的標記值。</span><span class="sxs-lookup"><span data-stu-id="cb69a-109">A marker value to be placed in the feedback buffer.</span></span> <span data-ttu-id="cb69a-110">它會以下列唯一的識別值表示。</span><span class="sxs-lookup"><span data-stu-id="cb69a-110">It is indicated with the following unique identifying value.</span></span>



| <span data-ttu-id="cb69a-111">值</span><span class="sxs-lookup"><span data-stu-id="cb69a-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="cb69a-112">意義</span><span class="sxs-lookup"><span data-stu-id="cb69a-112">Meaning</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <span data-ttu-id="cb69a-113"><dt>**GL \_ \_ 通過 \_ 權杖**</dt></span><span class="sxs-lookup"><span data-stu-id="cb69a-113"><dt>**GL\_PASS\_THROUGH\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="cb69a-114">會維護 **glPassThrough** 命令與圖形基本規格的相對順序。</span><span class="sxs-lookup"><span data-stu-id="cb69a-114">The order of **glPassThrough** commands with respect to the specification of graphics primitives is maintained.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb69a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb69a-115">Return value</span></span>

<span data-ttu-id="cb69a-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cb69a-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb69a-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cb69a-117">Error codes</span></span>

<span data-ttu-id="cb69a-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cb69a-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cb69a-119">Name</span><span class="sxs-lookup"><span data-stu-id="cb69a-119">Name</span></span>                                                                                                  | <span data-ttu-id="cb69a-120">意義</span><span class="sxs-lookup"><span data-stu-id="cb69a-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb69a-121"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="cb69a-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cb69a-122">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="cb69a-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cb69a-123">備註</span><span class="sxs-lookup"><span data-stu-id="cb69a-123">Remarks</span></span>

<span data-ttu-id="cb69a-124">意見反應是藉由使用 GL 意見反應來呼叫 [**glRenderMode**](glrendermode.md) ，而選取的 OpenGL 轉譯模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cb69a-124">Feedback is an OpenGL render mode selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="cb69a-125">當 OpenGL 處於意見反應模式時，柵格化不會產生任何圖元。</span><span class="sxs-lookup"><span data-stu-id="cb69a-125">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="cb69a-126">相反地，會將已點陣化之基本資訊的相關資訊，由 OpenGL 送回至應用程式。</span><span class="sxs-lookup"><span data-stu-id="cb69a-126">Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL.</span></span> <span data-ttu-id="cb69a-127">如需意見反應緩衝區和其中的值的描述，請參閱 [**glFeedbackBuffer**](glfeedbackbuffer.md) 。</span><span class="sxs-lookup"><span data-stu-id="cb69a-127">See [**glFeedbackBuffer**](glfeedbackbuffer.md) for a description of the feedback buffer and the values in it.</span></span>

<span data-ttu-id="cb69a-128">**GlPassThrough** 函式會在意見反應模式中執行時，在意見緩衝區中插入使用者定義標記。</span><span class="sxs-lookup"><span data-stu-id="cb69a-128">The **glPassThrough** function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode.</span></span> <span data-ttu-id="cb69a-129">*Token* 參數的傳回方式就如同它是基本。</span><span class="sxs-lookup"><span data-stu-id="cb69a-129">The *token* parameter is returned as if it were a primitive.</span></span>

<span data-ttu-id="cb69a-130">如果 OpenGL 不在意見反應模式中，則會忽略 **glPassThrough** 函式。</span><span class="sxs-lookup"><span data-stu-id="cb69a-130">The **glPassThrough** function is ignored if OpenGL is not in feedback mode.</span></span>

<span data-ttu-id="cb69a-131">下列函式會抓取 **glPassThrough** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="cb69a-131">The following function retrieves information related to **glPassThrough**:</span></span>

<span data-ttu-id="cb69a-132">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 轉譯 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="cb69a-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="cb69a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb69a-133">Requirements</span></span>



| <span data-ttu-id="cb69a-134">需求</span><span class="sxs-lookup"><span data-stu-id="cb69a-134">Requirement</span></span> | <span data-ttu-id="cb69a-135">值</span><span class="sxs-lookup"><span data-stu-id="cb69a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb69a-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb69a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cb69a-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb69a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cb69a-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb69a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cb69a-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb69a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb69a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="cb69a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb69a-141"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="cb69a-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cb69a-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb69a-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb69a-143"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb69a-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb69a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cb69a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb69a-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb69a-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb69a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb69a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb69a-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cb69a-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cb69a-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cb69a-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cb69a-149">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb69a-149">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="cb69a-150">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="cb69a-150">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





