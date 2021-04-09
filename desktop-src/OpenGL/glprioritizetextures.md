---
title: 'glPrioritizeTextures 函式 (Gl) '
description: GlPrioritizeTextures 函數會設定紋理的居住優先權。
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glPrioritizeTextures 函式 OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685694"
---
# <a name="glprioritizetextures-function"></a><span data-ttu-id="560be-104">glPrioritizeTextures 函式</span><span class="sxs-lookup"><span data-stu-id="560be-104">glPrioritizeTextures function</span></span>

<span data-ttu-id="560be-105">**GlPrioritizeTextures** 函數會設定紋理的居住優先權。</span><span class="sxs-lookup"><span data-stu-id="560be-105">The **glPrioritizeTextures** function sets the residence priority of textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="560be-106">語法</span><span class="sxs-lookup"><span data-stu-id="560be-106">Syntax</span></span>


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a><span data-ttu-id="560be-107">參數</span><span class="sxs-lookup"><span data-stu-id="560be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="560be-108">*n*</span><span class="sxs-lookup"><span data-stu-id="560be-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="560be-109">要設定優先順序的材質數目。</span><span class="sxs-lookup"><span data-stu-id="560be-109">The number of textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="560be-110">*紋理*</span><span class="sxs-lookup"><span data-stu-id="560be-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="560be-111">陣列的第一個元素的指標，其中包含要設定優先順序的材質名稱。</span><span class="sxs-lookup"><span data-stu-id="560be-111">A pointer to the first element of an array containing the names of the textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="560be-112">*優先 級*</span><span class="sxs-lookup"><span data-stu-id="560be-112">*priorities*</span></span> 
</dt> <dd>

<span data-ttu-id="560be-113">陣列的第一個元素的指標，其中包含材質優先權。</span><span class="sxs-lookup"><span data-stu-id="560be-113">A pointer to the first element of an array containing the texture priorities.</span></span> <span data-ttu-id="560be-114">Priority 參數的元素中 *指定的優先順序* 適用于 *材質* 參數的對應元素所命名的材質。</span><span class="sxs-lookup"><span data-stu-id="560be-114">A priority given in an element of the *priorities* parameter applies to the texture named by the corresponding element of the *textures* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="560be-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="560be-115">Return value</span></span>

<span data-ttu-id="560be-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="560be-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="560be-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="560be-117">Error codes</span></span>

<span data-ttu-id="560be-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="560be-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="560be-119">Name</span><span class="sxs-lookup"><span data-stu-id="560be-119">Name</span></span>                                                                                                  | <span data-ttu-id="560be-120">意義</span><span class="sxs-lookup"><span data-stu-id="560be-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="560be-121"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="560be-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="560be-122">*n* 為負數值。</span><span class="sxs-lookup"><span data-stu-id="560be-122">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="560be-123"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="560be-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="560be-124">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="560be-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="560be-125">備註</span><span class="sxs-lookup"><span data-stu-id="560be-125">Remarks</span></span>

<span data-ttu-id="560be-126">**GlPrioritizeTextures** 函式會將 *優先權* 參數中指定的 *n* 紋理優先順序指派給 *紋理* 參數中所命名的 *n* 紋理。</span><span class="sxs-lookup"><span data-stu-id="560be-126">The **glPrioritizeTextures** function assigns the *n* texture priorities specified in the *priorities* parameter to the *n* textures named in the *textures* parameter.</span></span> <span data-ttu-id="560be-127">在數量有限的材質記憶體的電腦上，OpenGL 會建立位於材質記憶體中之材質的「工作集」。</span><span class="sxs-lookup"><span data-stu-id="560be-127">On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory.</span></span> <span data-ttu-id="560be-128">這些紋理可以更有效率地系結至紋理目標，比不是常駐的材質更有效率。</span><span class="sxs-lookup"><span data-stu-id="560be-128">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="560be-129">藉由指定每個材質的優先順序， **glPrioritizeTextures** 函式可讓您判斷哪些材質應該是常駐的。</span><span class="sxs-lookup"><span data-stu-id="560be-129">By specifying a priority for each texture, the **glPrioritizeTextures** function enables you to determine which textures should be resident.</span></span>

<span data-ttu-id="560be-130">*優先順序* 中的材質優先順序元素會先壓制到 \[ 0.0、1.0 範圍， \] 然後再指派。</span><span class="sxs-lookup"><span data-stu-id="560be-130">The texture priorities elements in *priorities* are clamped to the range \[0.0, 1.0\] before being assigned.</span></span> <span data-ttu-id="560be-131">零表示最低優先順序;因此，優先順序為零的材質最不可能是常駐的。</span><span class="sxs-lookup"><span data-stu-id="560be-131">Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident.</span></span> <span data-ttu-id="560be-132">值1.0 表示最高優先順序;因此，具有優先順序1.0 的材質最有可能是常駐的。</span><span class="sxs-lookup"><span data-stu-id="560be-132">The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident.</span></span> <span data-ttu-id="560be-133">不過，在系結之前，不保證紋理是常駐的。</span><span class="sxs-lookup"><span data-stu-id="560be-133">However, textures are not guaranteed to be resident until they are bound.</span></span>

<span data-ttu-id="560be-134">**GlPrioritizeTextures** 函式會忽略設定材質0順序的嘗試，或未對應至現有材質的任何材質名稱。</span><span class="sxs-lookup"><span data-stu-id="560be-134">The **glPrioritizeTextures** function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture.</span></span> <span data-ttu-id="560be-135">*材質* 參數所命名的任何函式都必須系結至材質目標。</span><span class="sxs-lookup"><span data-stu-id="560be-135">None of the functions named by the *textures* parameter need to be bound to a texture target.</span></span>

<span data-ttu-id="560be-136">如果材質目前已系結，您也可以使用 [**glTexParameter**](gltexparameter-functions.md) 函式來設定其優先順序。</span><span class="sxs-lookup"><span data-stu-id="560be-136">If a texture is currently bound, you can also use the [**glTexParameter**](gltexparameter-functions.md) function to set its priority.</span></span> <span data-ttu-id="560be-137">這是設定預設材質優先權的唯一方式。</span><span class="sxs-lookup"><span data-stu-id="560be-137">This is the only way to set the priority of a default texture.</span></span>

<span data-ttu-id="560be-138">您可以在顯示清單中包含 **glPrioritizeTextures** 。</span><span class="sxs-lookup"><span data-stu-id="560be-138">You can include **glPrioritizeTextures** in display lists.</span></span>

<span data-ttu-id="560be-139">下列函式會抓取與 **glPrioritizeTextures** 相關之目前系結材質的優先順序：</span><span class="sxs-lookup"><span data-stu-id="560be-139">The following function retrieves the priority of a currently-bound texture related to **glPrioritizeTextures**:</span></span>

-   <span data-ttu-id="560be-140">[](glgettexparameter.md)具有參數名稱 GL \_ 材質 \_ 優先權的 glGetTexParameter</span><span class="sxs-lookup"><span data-stu-id="560be-140">[**glGetTexParameter**](glgettexparameter.md) with parameter name GL\_TEXTURE\_PRIORITY</span></span>

> [!Note]  
> <span data-ttu-id="560be-141">**GlPrioritizeTextures** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="560be-141">The **glPrioritizeTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="560be-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="560be-142">Requirements</span></span>



| <span data-ttu-id="560be-143">需求</span><span class="sxs-lookup"><span data-stu-id="560be-143">Requirement</span></span> | <span data-ttu-id="560be-144">值</span><span class="sxs-lookup"><span data-stu-id="560be-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="560be-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="560be-145">Minimum supported client</span></span><br/> | <span data-ttu-id="560be-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="560be-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="560be-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="560be-147">Minimum supported server</span></span><br/> | <span data-ttu-id="560be-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="560be-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="560be-149">標頭</span><span class="sxs-lookup"><span data-stu-id="560be-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="560be-150"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="560be-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="560be-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="560be-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="560be-152"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="560be-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="560be-153">DLL</span><span class="sxs-lookup"><span data-stu-id="560be-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="560be-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="560be-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="560be-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="560be-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="560be-156">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="560be-156">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="560be-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="560be-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="560be-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="560be-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="560be-159">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="560be-159">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="560be-160">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="560be-160">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="560be-161">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="560be-161">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="560be-162">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="560be-162">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





