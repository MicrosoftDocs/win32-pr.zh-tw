---
title: 'glAreTexturesResident 函式 (Gl) '
description: GlAreTexturesResident 函式會判斷指定的材質物件是否常駐在材質記憶體中。
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glAreTexturesResident 函式 OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965094"
---
# <a name="glaretexturesresident-function"></a><span data-ttu-id="01a74-104">glAreTexturesResident 函式</span><span class="sxs-lookup"><span data-stu-id="01a74-104">glAreTexturesResident function</span></span>

<span data-ttu-id="01a74-105">**GlAreTexturesResident** 函式會判斷指定的材質物件是否常駐在材質記憶體中。</span><span class="sxs-lookup"><span data-stu-id="01a74-105">The **glAreTexturesResident** function determines whether specified texture objects are resident in texture memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a74-106">語法</span><span class="sxs-lookup"><span data-stu-id="01a74-106">Syntax</span></span>


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a><span data-ttu-id="01a74-107">參數</span><span class="sxs-lookup"><span data-stu-id="01a74-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a74-108">*n*</span><span class="sxs-lookup"><span data-stu-id="01a74-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="01a74-109">要查詢的材質數目。</span><span class="sxs-lookup"><span data-stu-id="01a74-109">The number of textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="01a74-110">*紋理*</span><span class="sxs-lookup"><span data-stu-id="01a74-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="01a74-111">陣列的位址，其中包含要查詢之材質的名稱。</span><span class="sxs-lookup"><span data-stu-id="01a74-111">The address of an array containing the names of the textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="01a74-112">*住宅*</span><span class="sxs-lookup"><span data-stu-id="01a74-112">*residences*</span></span> 
</dt> <dd>

<span data-ttu-id="01a74-113">傳回紋理居住狀態的陣列位址。</span><span class="sxs-lookup"><span data-stu-id="01a74-113">The address of an array in which the texture residence status is returned.</span></span> <span data-ttu-id="01a74-114">以 *紋理* 元素命名之材質的居住狀態會在 *residences* 的對應元素中傳回。</span><span class="sxs-lookup"><span data-stu-id="01a74-114">The residence status of a texture named by an element of *textures* is returned in the corresponding element of *residences*.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="01a74-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="01a74-115">Error codes</span></span>

<span data-ttu-id="01a74-116">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="01a74-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="01a74-117">Name</span><span class="sxs-lookup"><span data-stu-id="01a74-117">Name</span></span>                                                                                                  | <span data-ttu-id="01a74-118">意義</span><span class="sxs-lookup"><span data-stu-id="01a74-118">Meaning</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01a74-119"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="01a74-119"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="01a74-120">*n* 為負值、 *材質* 中的元素為零，或 *紋理* 中的元素未包含材質識別碼。</span><span class="sxs-lookup"><span data-stu-id="01a74-120">*n* was a negative value, an element in *textures* was zero, or an element in *textures* did not contain a texture identifier.</span></span><br/> |
| <dl> <span data-ttu-id="01a74-121"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="01a74-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="01a74-122">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="01a74-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="01a74-123">備註</span><span class="sxs-lookup"><span data-stu-id="01a74-123">Remarks</span></span>

<span data-ttu-id="01a74-124">在數量有限的材質記憶體的電腦上，OpenGL 會建立一組可在材質記憶體中使用的材質。</span><span class="sxs-lookup"><span data-stu-id="01a74-124">On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory.</span></span> <span data-ttu-id="01a74-125">這些紋理可以更有效率地系結至紋理目標，比不是常駐的材質更有效率。</span><span class="sxs-lookup"><span data-stu-id="01a74-125">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="01a74-126">**GlAreTexturesResident** 函式會 *查詢紋理的* 元素所命名之 *n* 紋理的材質居住狀態。</span><span class="sxs-lookup"><span data-stu-id="01a74-126">The **glAreTexturesResident** function queries the texture residence status of the *n* textures named by the elements of *textures*.</span></span> <span data-ttu-id="01a74-127">如果所有命名紋理都是常駐的， **glAreTexturesResident** 會傳回 GL \_ TRUE，而 *residences* 的內容不會受到干擾。</span><span class="sxs-lookup"><span data-stu-id="01a74-127">If all the named textures are resident, **glAreTexturesResident** returns GL\_TRUE, and the contents of *residences* are undisturbed.</span></span> <span data-ttu-id="01a74-128">如果任何已命名的紋理都不存在，則 **glAreTexturesResident** 會 \_ 傳回 GL FALSE，並在 *residences* 的 *n* 個元素中傳回詳細的狀態。</span><span class="sxs-lookup"><span data-stu-id="01a74-128">If any of the named textures are not resident, **glAreTexturesResident** returns GL\_FALSE, and detailed status is returned in the *n* elements of *residences*.</span></span>

<span data-ttu-id="01a74-129">如果 *residences* 的元素是 GL \_ TRUE，則由 *紋理的* 對應元素所命名的材質會在材質記憶體中。</span><span class="sxs-lookup"><span data-stu-id="01a74-129">If an element of *residences* is GL\_TRUE, then the texture named by the corresponding element of *textures* is resident in texture memory.</span></span>

<span data-ttu-id="01a74-130">若要查詢單一系結材質的居住狀態，請呼叫 [**glGetTexParameter**](glgettexparameter.md) ，並將 *目標* 參數設定為目標材質（目標材質），並將 *PNAME* 參數設定為 [GL \_ 紋理常駐] \_ 。</span><span class="sxs-lookup"><span data-stu-id="01a74-130">To query the residence status of a single bound texture, call [**glGetTexParameter**](glgettexparameter.md) with the *target* parameter set to the target texture to which the target is bound and set the *pname* parameter to GL\_TEXTURE\_RESIDENT.</span></span> <span data-ttu-id="01a74-131">您必須使用這個方法來查詢預設材質的常駐狀態。</span><span class="sxs-lookup"><span data-stu-id="01a74-131">You must use this method to query the resident status of a default texture.</span></span>

<span data-ttu-id="01a74-132">您無法在顯示清單中包含 **glAreTexturesResident** 。</span><span class="sxs-lookup"><span data-stu-id="01a74-132">You cannot include **glAreTexturesResident** in display lists.</span></span>

<span data-ttu-id="01a74-133">**GlAreTexturesResident** 函式會在叫用時，傳回紋理的常駐狀態。</span><span class="sxs-lookup"><span data-stu-id="01a74-133">The **glAreTexturesResident** function returns the residency status of the textures at the time of invocation.</span></span> <span data-ttu-id="01a74-134">這並不保證紋理會在任何其他時間保持存留。</span><span class="sxs-lookup"><span data-stu-id="01a74-134">It does not guarantee that the textures will remain resident at any other time.</span></span>

<span data-ttu-id="01a74-135">如果材質位於虛擬記憶體中 (沒有紋理記憶體) ，則會被視為持續存在。</span><span class="sxs-lookup"><span data-stu-id="01a74-135">If textures reside in virtual memory (there is no texture memory), they are considered always resident.</span></span>

> [!Note]  
> <span data-ttu-id="01a74-136">**GlAreTexturesResident** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="01a74-136">The **glAreTexturesResident** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01a74-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="01a74-137">Requirements</span></span>



| <span data-ttu-id="01a74-138">需求</span><span class="sxs-lookup"><span data-stu-id="01a74-138">Requirement</span></span> | <span data-ttu-id="01a74-139">值</span><span class="sxs-lookup"><span data-stu-id="01a74-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a74-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01a74-140">Minimum supported client</span></span><br/> | <span data-ttu-id="01a74-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01a74-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="01a74-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01a74-142">Minimum supported server</span></span><br/> | <span data-ttu-id="01a74-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01a74-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01a74-144">標頭</span><span class="sxs-lookup"><span data-stu-id="01a74-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a74-145"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="01a74-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="01a74-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="01a74-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="01a74-147"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="01a74-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="01a74-148">DLL</span><span class="sxs-lookup"><span data-stu-id="01a74-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01a74-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a74-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a74-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01a74-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a74-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="01a74-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="01a74-152">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="01a74-152">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="01a74-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="01a74-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="01a74-154">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="01a74-154">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="01a74-155">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="01a74-155">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="01a74-156">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="01a74-156">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="01a74-157">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="01a74-157">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





