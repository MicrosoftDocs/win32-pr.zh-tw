---
title: 'glIsTexture 函式 (Gl) '
description: GlIsTexture 函式會判斷名稱是否對應至材質。
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- glIsTexture 函式 OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466637"
---
# <a name="glistexture-function"></a><span data-ttu-id="503ac-104">glIsTexture 函式</span><span class="sxs-lookup"><span data-stu-id="503ac-104">glIsTexture function</span></span>

<span data-ttu-id="503ac-105">**GlIsTexture** 函式會判斷名稱是否對應至材質。</span><span class="sxs-lookup"><span data-stu-id="503ac-105">The **glIsTexture** function determines if a name corresponds to a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="503ac-106">語法</span><span class="sxs-lookup"><span data-stu-id="503ac-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="503ac-107">參數</span><span class="sxs-lookup"><span data-stu-id="503ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="503ac-108">*紋理*</span><span class="sxs-lookup"><span data-stu-id="503ac-108">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="503ac-109">值，這個值是材質的名稱。</span><span class="sxs-lookup"><span data-stu-id="503ac-109">A value that is the name of a texture.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="503ac-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="503ac-110">Error codes</span></span>

<span data-ttu-id="503ac-111">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="503ac-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="503ac-112">Name</span><span class="sxs-lookup"><span data-stu-id="503ac-112">Name</span></span>                                                                                                  | <span data-ttu-id="503ac-113">意義</span><span class="sxs-lookup"><span data-stu-id="503ac-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="503ac-114"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="503ac-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="503ac-115">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="503ac-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="503ac-116">備註</span><span class="sxs-lookup"><span data-stu-id="503ac-116">Remarks</span></span>

<span data-ttu-id="503ac-117">如果 *材質* 參數目前是材質的名稱， **glIsTexture** 函數會傳回 GL \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="503ac-117">If the *texture* parameter is currently the name of a texture, the **glIsTexture** function returns GL\_TRUE.</span></span> <span data-ttu-id="503ac-118">如果材質為零，則 **glIsTexture** 函數會傳回 GL \_ FALSE。 </span><span class="sxs-lookup"><span data-stu-id="503ac-118">The **glIsTexture** function returns GL\_FALSE if *texture* is zero.</span></span> <span data-ttu-id="503ac-119">\_如果它是非零值，且不是材質的名稱，或發生錯誤時，它也會傳回 GL FALSE。</span><span class="sxs-lookup"><span data-stu-id="503ac-119">It also returns GL\_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.</span></span>

<span data-ttu-id="503ac-120">您不能在顯示清單中包含 **glIsTexture** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="503ac-120">You cannot include calls to **glIsTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="503ac-121">**GlIsTexture** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="503ac-121">The **glIsTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="503ac-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="503ac-122">Requirements</span></span>



| <span data-ttu-id="503ac-123">需求</span><span class="sxs-lookup"><span data-stu-id="503ac-123">Requirement</span></span> | <span data-ttu-id="503ac-124">值</span><span class="sxs-lookup"><span data-stu-id="503ac-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="503ac-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="503ac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="503ac-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="503ac-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="503ac-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="503ac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="503ac-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="503ac-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="503ac-129">標頭</span><span class="sxs-lookup"><span data-stu-id="503ac-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="503ac-130"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="503ac-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="503ac-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="503ac-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="503ac-132"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="503ac-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="503ac-133">DLL</span><span class="sxs-lookup"><span data-stu-id="503ac-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="503ac-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="503ac-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="503ac-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="503ac-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503ac-136">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="503ac-136">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="503ac-137">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="503ac-137">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="503ac-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="503ac-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="503ac-139">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="503ac-139">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="503ac-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="503ac-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="503ac-141">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="503ac-141">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="503ac-142">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="503ac-142">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="503ac-143">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="503ac-143">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="503ac-144">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="503ac-144">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





