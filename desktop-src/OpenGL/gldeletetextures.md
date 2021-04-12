---
title: 'glDeleteTextures 函式 (Gl) '
description: GlDeleteTextures 函式會刪除已命名的材質。
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- glDeleteTextures 函式 OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464613"
---
# <a name="gldeletetextures-function"></a><span data-ttu-id="1d3ca-104">glDeleteTextures 函式</span><span class="sxs-lookup"><span data-stu-id="1d3ca-104">glDeleteTextures function</span></span>

<span data-ttu-id="1d3ca-105">**GlDeleteTextures** 函式會刪除已命名的材質。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-105">The **glDeleteTextures** function deletes named textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3ca-106">語法</span><span class="sxs-lookup"><span data-stu-id="1d3ca-106">Syntax</span></span>


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="1d3ca-107">參數</span><span class="sxs-lookup"><span data-stu-id="1d3ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d3ca-108">*n*</span><span class="sxs-lookup"><span data-stu-id="1d3ca-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="1d3ca-109">要刪除的材質數目。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-109">The number of textures to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="1d3ca-110">*紋理*</span><span class="sxs-lookup"><span data-stu-id="1d3ca-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="1d3ca-111">要刪除之材質的陣列。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-111">An array of textures to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d3ca-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d3ca-112">Return value</span></span>

<span data-ttu-id="1d3ca-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1d3ca-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1d3ca-114">Error codes</span></span>

<span data-ttu-id="1d3ca-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1d3ca-116">Name</span><span class="sxs-lookup"><span data-stu-id="1d3ca-116">Name</span></span>                                                                                                  | <span data-ttu-id="1d3ca-117">意義</span><span class="sxs-lookup"><span data-stu-id="1d3ca-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d3ca-118"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="1d3ca-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1d3ca-119">*n* 為負數值。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="1d3ca-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="1d3ca-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1d3ca-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1d3ca-122">備註</span><span class="sxs-lookup"><span data-stu-id="1d3ca-122">Remarks</span></span>

<span data-ttu-id="1d3ca-123">**GlDeleteTextures** 函式會刪除由陣列 *紋理* 的元素所命名的 *n* 紋理。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-123">The **glDeleteTextures** function deletes *n* textures named by the elements of the array *textures*.</span></span> <span data-ttu-id="1d3ca-124">在刪除材質之後，它沒有任何內容或維度，而且其名稱可自由重複使用 (例如， **glGenTextures**) 。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-124">After a texture is deleted, it has no contents or dimensionality, and its name is free for reuse (for example, by **glGenTextures**).</span></span> <span data-ttu-id="1d3ca-125">**GlDeleteTextures** 函式會忽略未對應至現有材質的零和名稱。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-125">The **glDeleteTextures** function ignores zeros and names that do not correspond to existing textures.</span></span>

<span data-ttu-id="1d3ca-126">如果刪除目前系結的材質，系結會還原為零 (預設材質) 。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-126">If a texture that is currently bound is deleted, the binding reverts to zero (the default texture).</span></span>

<span data-ttu-id="1d3ca-127">您不能在顯示清單中包含 **glDeleteTextures** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-127">You cannot include calls to **glDeleteTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="1d3ca-128">**GlDeleteTextures** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1d3ca-128">The **glDeleteTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="1d3ca-129">下列函式會抓取 **glDeleteTextures** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="1d3ca-129">The following function retrieves information related to **glDeleteTextures**:</span></span>

-   [<span data-ttu-id="1d3ca-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="1d3ca-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d3ca-131">Requirements</span></span>



| <span data-ttu-id="1d3ca-132">需求</span><span class="sxs-lookup"><span data-stu-id="1d3ca-132">Requirement</span></span> | <span data-ttu-id="1d3ca-133">值</span><span class="sxs-lookup"><span data-stu-id="1d3ca-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3ca-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d3ca-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3ca-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d3ca-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1d3ca-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d3ca-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3ca-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d3ca-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1d3ca-138">標頭</span><span class="sxs-lookup"><span data-stu-id="1d3ca-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d3ca-139"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="1d3ca-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1d3ca-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d3ca-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d3ca-141"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d3ca-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1d3ca-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1d3ca-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d3ca-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d3ca-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d3ca-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d3ca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3ca-145">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-145">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-147">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-147">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-149">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-149">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-151">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-151">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-152">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-152">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-153">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-153">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-154">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-154">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-155">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-155">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-156">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-156">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1d3ca-157">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1d3ca-157">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





