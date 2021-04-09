---
title: 'glGenTextures 函式 (Gl) '
description: GlGenTextures 函式會產生材質名稱。
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glGenTextures 函式 OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934988"
---
# <a name="glgentextures-function"></a><span data-ttu-id="86a58-104">glGenTextures 函式</span><span class="sxs-lookup"><span data-stu-id="86a58-104">glGenTextures function</span></span>

<span data-ttu-id="86a58-105">**GlGenTextures** 函式會產生材質名稱。</span><span class="sxs-lookup"><span data-stu-id="86a58-105">The **glGenTextures** function generates texture names.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a58-106">語法</span><span class="sxs-lookup"><span data-stu-id="86a58-106">Syntax</span></span>


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="86a58-107">參數</span><span class="sxs-lookup"><span data-stu-id="86a58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a58-108">*n*</span><span class="sxs-lookup"><span data-stu-id="86a58-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="86a58-109">要產生的材質名稱數目。</span><span class="sxs-lookup"><span data-stu-id="86a58-109">The number of texture names to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="86a58-110">*紋理*</span><span class="sxs-lookup"><span data-stu-id="86a58-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="86a58-111">陣列的第一個元素的指標，其中會儲存產生的材質名稱。</span><span class="sxs-lookup"><span data-stu-id="86a58-111">A pointer to the first element of an array in which the generated texture names are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a58-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="86a58-112">Return value</span></span>

<span data-ttu-id="86a58-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="86a58-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86a58-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="86a58-114">Error codes</span></span>

<span data-ttu-id="86a58-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="86a58-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="86a58-116">Name</span><span class="sxs-lookup"><span data-stu-id="86a58-116">Name</span></span>                                                                                                  | <span data-ttu-id="86a58-117">意義</span><span class="sxs-lookup"><span data-stu-id="86a58-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86a58-118"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="86a58-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="86a58-119">*n* 為負數值。</span><span class="sxs-lookup"><span data-stu-id="86a58-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="86a58-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="86a58-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="86a58-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="86a58-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="86a58-122">備註</span><span class="sxs-lookup"><span data-stu-id="86a58-122">Remarks</span></span>

<span data-ttu-id="86a58-123">**GlGenTextures** 函數會在 *材質* 參數中傳回 *n* 個材質名稱。</span><span class="sxs-lookup"><span data-stu-id="86a58-123">The **glGenTextures** function returns *n* texture names in the *textures* parameter.</span></span> <span data-ttu-id="86a58-124">紋理名稱不一定是連續的整數集合，不過，在呼叫 **glGenTextures** 函式之前，不會立即使用任何傳回的名稱。</span><span class="sxs-lookup"><span data-stu-id="86a58-124">The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the **glGenTextures** function.</span></span> <span data-ttu-id="86a58-125">產生的材質會假設紋理目標的維度維度會先與 [**glBindTexture**](glbindtexture.md) 函數系結。</span><span class="sxs-lookup"><span data-stu-id="86a58-125">The generated textures assume the dimensionality of the texture target to which they are first bound with the [**glBindTexture**](glbindtexture.md) function.</span></span> <span data-ttu-id="86a58-126">後續的 **glGenTextures** 呼叫不會傳回 **glGenTextures** 所傳回的材質名稱，除非先藉由呼叫 [**glDeleteTextures**](gldeletetextures.md)來刪除它們。</span><span class="sxs-lookup"><span data-stu-id="86a58-126">Texture names returned by **glGenTextures** are not returned by subsequent calls to **glGenTextures** unless they are first deleted by calling [**glDeleteTextures**](gldeletetextures.md).</span></span>

<span data-ttu-id="86a58-127">您無法在顯示清單中包含 **glGenTextures** 。</span><span class="sxs-lookup"><span data-stu-id="86a58-127">You cannot include **glGenTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="86a58-128">**GlGenTextures** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="86a58-128">The **glGenTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="86a58-129">下列函式會抓取 **glGenTextures** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="86a58-129">The following function retrieves information related to **glGenTextures**:</span></span>

-   [<span data-ttu-id="86a58-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="86a58-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="86a58-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="86a58-131">Requirements</span></span>



| <span data-ttu-id="86a58-132">需求</span><span class="sxs-lookup"><span data-stu-id="86a58-132">Requirement</span></span> | <span data-ttu-id="86a58-133">值</span><span class="sxs-lookup"><span data-stu-id="86a58-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86a58-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86a58-134">Minimum supported client</span></span><br/> | <span data-ttu-id="86a58-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86a58-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="86a58-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86a58-136">Minimum supported server</span></span><br/> | <span data-ttu-id="86a58-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86a58-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86a58-138">標頭</span><span class="sxs-lookup"><span data-stu-id="86a58-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="86a58-139"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="86a58-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="86a58-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="86a58-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="86a58-141"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="86a58-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="86a58-142">DLL</span><span class="sxs-lookup"><span data-stu-id="86a58-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86a58-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a58-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86a58-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86a58-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a58-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="86a58-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="86a58-146">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="86a58-146">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="86a58-147">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="86a58-147">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="86a58-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="86a58-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="86a58-149">**glGet**</span><span class="sxs-lookup"><span data-stu-id="86a58-149">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="86a58-150">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="86a58-150">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="86a58-151">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="86a58-151">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="86a58-152">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="86a58-152">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="86a58-153">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="86a58-153">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="86a58-154">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="86a58-154">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





