---
title: 'glGetTexEnvfv 函式 (Gl) '
description: 'GlGetTexEnvfv 和 glGetTexEnviv 函數會傳回紋理環境參數。 |glGetTexEnvfv 函式 (Gl) '
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- glGetTexEnvfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d542461b05a824c78bbad82d843735289f2fb4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982832"
---
# <a name="glgettexenvfv-function"></a><span data-ttu-id="3c5b0-105">glGetTexEnvfv 函式</span><span class="sxs-lookup"><span data-stu-id="3c5b0-105">glGetTexEnvfv function</span></span>

<span data-ttu-id="3c5b0-106">**GlGetTexEnvfv** 和 [**glGetTexEnviv**](glgettexenviv.md)函數會傳回紋理環境參數。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-106">The **glGetTexEnvfv** and [**glGetTexEnviv**](glgettexenviv.md) functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c5b0-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c5b0-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="3c5b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="3c5b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c5b0-109">*目標*</span><span class="sxs-lookup"><span data-stu-id="3c5b0-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="3c5b0-110">紋理環境。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-110">A texture environment.</span></span> <span data-ttu-id="3c5b0-111">必須是 GL \_ 紋理 \_ 環境。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="3c5b0-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="3c5b0-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="3c5b0-113">紋理環境參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="3c5b0-114">接受下列值。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-114">The following values are accepted.</span></span>



| <span data-ttu-id="3c5b0-115">值</span><span class="sxs-lookup"><span data-stu-id="3c5b0-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="3c5b0-116">意義</span><span class="sxs-lookup"><span data-stu-id="3c5b0-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="3c5b0-117"><dt>**GL \_ 紋理 \_ 環境 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="3c5b0-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="3c5b0-118">*Params* 參數會傳回單一值紋理環境模式，也就是一個符號常數。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="3c5b0-119"><dt>**GL \_ 紋理 \_ 環境 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="3c5b0-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="3c5b0-120">*Params* 參數會傳回四個整數或浮點值，也就是材質環境的色彩。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="3c5b0-121">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應至最正面的可表示整數，而-1.0 對應至最大的可表示整數。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c5b0-122">*params*</span><span class="sxs-lookup"><span data-stu-id="3c5b0-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3c5b0-123">傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c5b0-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c5b0-124">Return value</span></span>

<span data-ttu-id="3c5b0-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c5b0-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3c5b0-126">Error codes</span></span>

<span data-ttu-id="3c5b0-127">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3c5b0-128">Name</span><span class="sxs-lookup"><span data-stu-id="3c5b0-128">Name</span></span>                                                                                                  | <span data-ttu-id="3c5b0-129">意義</span><span class="sxs-lookup"><span data-stu-id="3c5b0-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c5b0-130"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="3c5b0-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3c5b0-131">*target* 或 *pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="3c5b0-132"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="3c5b0-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3c5b0-133">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3c5b0-134">備註</span><span class="sxs-lookup"><span data-stu-id="3c5b0-134">Remarks</span></span>

<span data-ttu-id="3c5b0-135">**GlGetTexEnv** 函式會傳回以 *params* 選取的材質環境值（以 [**glTexEnv**](gltexenv-functions.md)指定）。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="3c5b0-136">*Target* 參數指定紋理環境。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="3c5b0-137">目前只定義並支援一個材質環境： GL \_ 紋理 \_ ENV。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="3c5b0-138">*Pname* 參數會命名特定的材質環境參數。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="3c5b0-139">如果產生錯誤，則不會對 *參數* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="3c5b0-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c5b0-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c5b0-140">Requirements</span></span>



| <span data-ttu-id="3c5b0-141">需求</span><span class="sxs-lookup"><span data-stu-id="3c5b0-141">Requirement</span></span> | <span data-ttu-id="3c5b0-142">值</span><span class="sxs-lookup"><span data-stu-id="3c5b0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5b0-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c5b0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5b0-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c5b0-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c5b0-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c5b0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5b0-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c5b0-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c5b0-147">標頭</span><span class="sxs-lookup"><span data-stu-id="3c5b0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c5b0-148"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="3c5b0-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3c5b0-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c5b0-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c5b0-150"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c5b0-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c5b0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3c5b0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c5b0-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c5b0-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c5b0-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c5b0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5b0-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3c5b0-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3c5b0-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3c5b0-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3c5b0-156">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="3c5b0-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





