---
title: 'glBindTexture 函式 (Gl) '
description: GlBindTexture 函數可讓您建立系結至材質目標的命名材質。
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture 函式 OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384829"
---
# <a name="glbindtexture-function"></a><span data-ttu-id="67614-104">glBindTexture 函式</span><span class="sxs-lookup"><span data-stu-id="67614-104">glBindTexture function</span></span>

<span data-ttu-id="67614-105">**GlBindTexture** 函數可讓您建立系結至材質目標的命名材質。</span><span class="sxs-lookup"><span data-stu-id="67614-105">The **glBindTexture** function enables the creation of a named texture that is bound to a texture target.</span></span>

## <a name="syntax"></a><span data-ttu-id="67614-106">語法</span><span class="sxs-lookup"><span data-stu-id="67614-106">Syntax</span></span>


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="67614-107">參數</span><span class="sxs-lookup"><span data-stu-id="67614-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67614-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="67614-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="67614-109">材質所系結的目標。</span><span class="sxs-lookup"><span data-stu-id="67614-109">The target to which the texture is bound.</span></span> <span data-ttu-id="67614-110">必須具有值 GL \_ 紋理 \_ 1D 或 GL \_ 紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="67614-110">Must have the value GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="67614-111">*紋理*</span><span class="sxs-lookup"><span data-stu-id="67614-111">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="67614-112">材質的名稱;材質名稱目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="67614-112">The name of a texture; the texture name cannot currently be in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67614-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="67614-113">Return value</span></span>

<span data-ttu-id="67614-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="67614-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="67614-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="67614-115">Error codes</span></span>

<span data-ttu-id="67614-116">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="67614-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="67614-117">Name</span><span class="sxs-lookup"><span data-stu-id="67614-117">Name</span></span>                                                                                                  | <span data-ttu-id="67614-118">意義</span><span class="sxs-lookup"><span data-stu-id="67614-118">Meaning</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67614-119"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="67614-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="67614-120">參數 *目標* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="67614-120">The parameter *target* was not an accepted value.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="67614-121"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="67614-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="67614-122">參數 *材質* 沒有與 *目標* 相同的維度，或呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="67614-122">The parameter *texture* did not have the same dimensionality as *target*, or the function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="67614-123">備註</span><span class="sxs-lookup"><span data-stu-id="67614-123">Remarks</span></span>

<span data-ttu-id="67614-124">**GlBindTexture** 函數可讓您建立命名紋理。</span><span class="sxs-lookup"><span data-stu-id="67614-124">The **glBindTexture** function enables you to create a named texture.</span></span> <span data-ttu-id="67614-125">將 *目標* 設定為 GL  \_ 紋理 \_ 1d 或 gl \_ 材質 \_ 2d，並將材質設定為您所建立之新材質的名稱時，會將材質名稱系結至適當的材質目標，來呼叫 glBindTexture。</span><span class="sxs-lookup"><span data-stu-id="67614-125">Calling **glBindTexture** with *target* set to GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, and *texture* set to the name of the new texture you have created binds the texture name to the appropriate texture target.</span></span> <span data-ttu-id="67614-126">當材質系結至目標時，該目標的先前系結將不再有效。</span><span class="sxs-lookup"><span data-stu-id="67614-126">When a texture is bound to a target, the previous binding for that target is no longer in effect.</span></span>

<span data-ttu-id="67614-127">材質名稱是一種不帶正負號的整數，其值為零，表示每個材質目標的預設材質。</span><span class="sxs-lookup"><span data-stu-id="67614-127">Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target.</span></span> <span data-ttu-id="67614-128">材質名稱和對應的材質內容位於目前 OpenGL 轉譯內容的共用顯示清單空間區域中;只有當兩個轉譯內容也共用顯示清單時，才會共用材質名稱。</span><span class="sxs-lookup"><span data-stu-id="67614-128">Texture names and the corresponding texture contents are local to the shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists.</span></span> <span data-ttu-id="67614-129">您可以使用 [**glGenTextures**](glgentextures.md)來產生一組新的材質名稱。</span><span class="sxs-lookup"><span data-stu-id="67614-129">You can generate a set of new texture names using [**glGenTextures**](glgentextures.md).</span></span>

<span data-ttu-id="67614-130">第一次系結材質時，它會假設其材質目標的維度。系結至 GL \_ 紋理1d 的材質 \_ 會變成一維，且系結至 gl \_ 材質2d 的材質 \_ 會變成二維。</span><span class="sxs-lookup"><span data-stu-id="67614-130">When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL\_TEXTURE\_1D becomes one-dimensional and a texture bound to GL\_TEXTURE\_2D becomes two-dimensional.</span></span> <span data-ttu-id="67614-131">您在紋理目標上執行的作業也會影響系結至目標的材質。</span><span class="sxs-lookup"><span data-stu-id="67614-131">Operations you perform on a texture target also affect a texture bound to the target.</span></span> <span data-ttu-id="67614-132">當您查詢材質目標時，傳回值會是所系結之材質的狀態。</span><span class="sxs-lookup"><span data-stu-id="67614-132">When you query a texture target, the return value is the state of the texture bound to it.</span></span> <span data-ttu-id="67614-133">紋理目標會成為目前系結之紋理的別名。</span><span class="sxs-lookup"><span data-stu-id="67614-133">Texture targets become aliases for textures currently bound to them.</span></span>

<span data-ttu-id="67614-134">當您使用 **glBindTexture** 系結材質時，系結會保持作用中，直到不同的材質系結至相同的目標，或使用 [**glDeleteTextures**](gldeletetextures.md) 函式刪除系結的材質為止。</span><span class="sxs-lookup"><span data-stu-id="67614-134">When you bind a texture with **glBindTexture**, the binding remains active until a different texture is bound to the same target or you delete the bound texture with the [**glDeleteTextures**](gldeletetextures.md) function.</span></span> <span data-ttu-id="67614-135">建立命名材質之後，您可以將它系結至具有相同維度的材質目標（視需要一樣）。</span><span class="sxs-lookup"><span data-stu-id="67614-135">Once you create a named texture you can bind it to a texture target that has the same dimensionality as often as needed.</span></span>

<span data-ttu-id="67614-136">使用 **glBindTexture** 將現有的指名材質系結至其中一個材質目標，通常會比使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)重載紋理影像更快。</span><span class="sxs-lookup"><span data-stu-id="67614-136">It is usually much faster to use **glBindTexture** to bind an existing named texture to one of the texture targets than it is to reload the texture image using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="67614-137">若要進一步控制紋理效能，請使用 [**glPrioritizeTextures**](glprioritizetextures.md)。</span><span class="sxs-lookup"><span data-stu-id="67614-137">For additional control of texturing performance, use [**glPrioritizeTextures**](glprioritizetextures.md).</span></span>

<span data-ttu-id="67614-138">您可以在顯示清單中加入 **glBindTexture** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="67614-138">You can include calls to **glBindTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="67614-139">**GlBindTexture** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="67614-139">The **glBindTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="67614-140">下列函式會取出與 **glBindTexture** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="67614-140">The following functions retrieve information related to **glBindTexture**:</span></span>

-   <span data-ttu-id="67614-141">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 紋理 \_ 1D 系結的 glGet \_</span><span class="sxs-lookup"><span data-stu-id="67614-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_1D\_BINDING</span></span>

<span data-ttu-id="67614-142">具有引數 GL \_ 材質 \_ 2D 系結的 glGet \_</span><span class="sxs-lookup"><span data-stu-id="67614-142">**glGet** with argument GL\_TEXTURE\_2D\_BINDING</span></span>

## <a name="requirements"></a><span data-ttu-id="67614-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="67614-143">Requirements</span></span>



| <span data-ttu-id="67614-144">需求</span><span class="sxs-lookup"><span data-stu-id="67614-144">Requirement</span></span> | <span data-ttu-id="67614-145">值</span><span class="sxs-lookup"><span data-stu-id="67614-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67614-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67614-146">Minimum supported client</span></span><br/> | <span data-ttu-id="67614-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67614-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="67614-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67614-148">Minimum supported server</span></span><br/> | <span data-ttu-id="67614-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67614-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67614-150">標頭</span><span class="sxs-lookup"><span data-stu-id="67614-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="67614-151"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="67614-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="67614-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="67614-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="67614-153"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="67614-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="67614-154">DLL</span><span class="sxs-lookup"><span data-stu-id="67614-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67614-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67614-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67614-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67614-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67614-157">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="67614-157">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="67614-158">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="67614-158">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="67614-159">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="67614-159">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="67614-160">**glGet**</span><span class="sxs-lookup"><span data-stu-id="67614-160">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="67614-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="67614-161">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="67614-162">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="67614-162">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="67614-163">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="67614-163">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="67614-164">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="67614-164">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="67614-165">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="67614-165">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="67614-166">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="67614-166">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





