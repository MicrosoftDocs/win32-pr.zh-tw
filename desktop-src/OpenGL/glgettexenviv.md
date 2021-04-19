---
title: 'glGetTexEnviv 函式 (Gl) '
description: 'GlGetTexEnvfv 和 glGetTexEnviv 函數會傳回紋理環境參數。 |glGetTexEnviv 函式 (Gl) '
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- glGetTexEnviv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993822"
---
# <a name="glgettexenviv-function"></a><span data-ttu-id="55c03-105">glGetTexEnviv 函式</span><span class="sxs-lookup"><span data-stu-id="55c03-105">glGetTexEnviv function</span></span>

<span data-ttu-id="55c03-106">[**GlGetTexEnvfv**](glgettexenvfv.md)和 **glGetTexEnviv** 函數會傳回紋理環境參數。</span><span class="sxs-lookup"><span data-stu-id="55c03-106">The [**glGetTexEnvfv**](glgettexenvfv.md) and **glGetTexEnviv** functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c03-107">語法</span><span class="sxs-lookup"><span data-stu-id="55c03-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="55c03-108">參數</span><span class="sxs-lookup"><span data-stu-id="55c03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c03-109">*目標*</span><span class="sxs-lookup"><span data-stu-id="55c03-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="55c03-110">紋理環境。</span><span class="sxs-lookup"><span data-stu-id="55c03-110">A texture environment.</span></span> <span data-ttu-id="55c03-111">必須是 GL \_ 紋理 \_ 環境。</span><span class="sxs-lookup"><span data-stu-id="55c03-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="55c03-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="55c03-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="55c03-113">紋理環境參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="55c03-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="55c03-114">接受下列值。</span><span class="sxs-lookup"><span data-stu-id="55c03-114">The following values are accepted.</span></span>



| <span data-ttu-id="55c03-115">值</span><span class="sxs-lookup"><span data-stu-id="55c03-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="55c03-116">意義</span><span class="sxs-lookup"><span data-stu-id="55c03-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="55c03-117"><dt>**GL \_ 紋理 \_ 環境 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="55c03-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="55c03-118">*Params* 參數會傳回單一值紋理環境模式，也就是一個符號常數。</span><span class="sxs-lookup"><span data-stu-id="55c03-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="55c03-119"><dt>**GL \_ 紋理 \_ 環境 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="55c03-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="55c03-120">*Params* 參數會傳回四個整數或浮點值，也就是材質環境的色彩。</span><span class="sxs-lookup"><span data-stu-id="55c03-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="55c03-121">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應至最正面的可表示整數，而-1.0 對應至最大的可表示整數。</span><span class="sxs-lookup"><span data-stu-id="55c03-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="55c03-122">*params*</span><span class="sxs-lookup"><span data-stu-id="55c03-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="55c03-123">傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="55c03-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c03-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="55c03-124">Return value</span></span>

<span data-ttu-id="55c03-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="55c03-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55c03-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="55c03-126">Error codes</span></span>

<span data-ttu-id="55c03-127">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="55c03-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="55c03-128">Name</span><span class="sxs-lookup"><span data-stu-id="55c03-128">Name</span></span>                                                                                                  | <span data-ttu-id="55c03-129">意義</span><span class="sxs-lookup"><span data-stu-id="55c03-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55c03-130"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="55c03-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="55c03-131">*target* 或 *pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="55c03-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="55c03-132"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="55c03-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="55c03-133">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="55c03-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="55c03-134">備註</span><span class="sxs-lookup"><span data-stu-id="55c03-134">Remarks</span></span>

<span data-ttu-id="55c03-135">**GlGetTexEnv** 函式會傳回以 *params* 選取的材質環境值（以 [**glTexEnv**](gltexenv-functions.md)指定）。</span><span class="sxs-lookup"><span data-stu-id="55c03-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="55c03-136">*Target* 參數指定紋理環境。</span><span class="sxs-lookup"><span data-stu-id="55c03-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="55c03-137">目前只定義並支援一個材質環境： GL \_ 紋理 \_ ENV。</span><span class="sxs-lookup"><span data-stu-id="55c03-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="55c03-138">*Pname* 參數會命名特定的材質環境參數。</span><span class="sxs-lookup"><span data-stu-id="55c03-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="55c03-139">如果產生錯誤，則不會對 *參數* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="55c03-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c03-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="55c03-140">Requirements</span></span>



| <span data-ttu-id="55c03-141">需求</span><span class="sxs-lookup"><span data-stu-id="55c03-141">Requirement</span></span> | <span data-ttu-id="55c03-142">值</span><span class="sxs-lookup"><span data-stu-id="55c03-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55c03-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55c03-143">Minimum supported client</span></span><br/> | <span data-ttu-id="55c03-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55c03-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55c03-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55c03-145">Minimum supported server</span></span><br/> | <span data-ttu-id="55c03-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55c03-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55c03-147">標頭</span><span class="sxs-lookup"><span data-stu-id="55c03-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="55c03-148"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="55c03-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="55c03-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="55c03-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="55c03-150"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="55c03-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="55c03-151">DLL</span><span class="sxs-lookup"><span data-stu-id="55c03-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55c03-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c03-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c03-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55c03-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c03-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="55c03-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="55c03-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="55c03-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="55c03-156">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="55c03-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





