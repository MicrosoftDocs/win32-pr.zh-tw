---
title: 'glDepthMask 函式 (Gl) '
description: GlDepthMask 函式會啟用或停用寫入深度緩衝區。
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- glDepthMask 函式 OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384817"
---
# <a name="gldepthmask-function"></a><span data-ttu-id="31bce-104">glDepthMask 函式</span><span class="sxs-lookup"><span data-stu-id="31bce-104">glDepthMask function</span></span>

<span data-ttu-id="31bce-105">**GlDepthMask** 函式會啟用或停用寫入深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="31bce-105">The **glDepthMask** function enables or disables writing into the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="31bce-106">語法</span><span class="sxs-lookup"><span data-stu-id="31bce-106">Syntax</span></span>


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="31bce-107">參數</span><span class="sxs-lookup"><span data-stu-id="31bce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31bce-108">*旗標*</span><span class="sxs-lookup"><span data-stu-id="31bce-108">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="31bce-109">指定是否啟用深度緩衝區以進行寫入。</span><span class="sxs-lookup"><span data-stu-id="31bce-109">Specifies whether the depth buffer is enabled for writing.</span></span> <span data-ttu-id="31bce-110">如果 *旗* 標為零，則會停用深度緩衝區寫入。</span><span class="sxs-lookup"><span data-stu-id="31bce-110">If *flag* is zero, depth-buffer writing is disabled.</span></span> <span data-ttu-id="31bce-111">否則，就會啟用它。</span><span class="sxs-lookup"><span data-stu-id="31bce-111">Otherwise, it is enabled.</span></span> <span data-ttu-id="31bce-112">一開始，會啟用深度緩衝區寫入。</span><span class="sxs-lookup"><span data-stu-id="31bce-112">Initially, depth-buffer writing is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31bce-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="31bce-113">Return value</span></span>

<span data-ttu-id="31bce-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="31bce-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="31bce-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="31bce-115">Error codes</span></span>

<span data-ttu-id="31bce-116">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="31bce-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="31bce-117">Name</span><span class="sxs-lookup"><span data-stu-id="31bce-117">Name</span></span>                                                                                                  | <span data-ttu-id="31bce-118">意義</span><span class="sxs-lookup"><span data-stu-id="31bce-118">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31bce-119"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="31bce-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="31bce-120">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="31bce-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="31bce-121">備註</span><span class="sxs-lookup"><span data-stu-id="31bce-121">Remarks</span></span>

<span data-ttu-id="31bce-122">下列函式會抓取 **glDepthMask** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="31bce-122">The following function retrieves information related to **glDepthMask**:</span></span>

<span data-ttu-id="31bce-123">具有引數 GL \_ 深度 \_ WRITEMASK 的 glGet</span><span class="sxs-lookup"><span data-stu-id="31bce-123">**glGet** with argument GL\_DEPTH\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="31bce-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="31bce-124">Requirements</span></span>



| <span data-ttu-id="31bce-125">需求</span><span class="sxs-lookup"><span data-stu-id="31bce-125">Requirement</span></span> | <span data-ttu-id="31bce-126">值</span><span class="sxs-lookup"><span data-stu-id="31bce-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31bce-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31bce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="31bce-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31bce-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31bce-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31bce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="31bce-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31bce-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31bce-131">標頭</span><span class="sxs-lookup"><span data-stu-id="31bce-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="31bce-132"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="31bce-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="31bce-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="31bce-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="31bce-134"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="31bce-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="31bce-135">DLL</span><span class="sxs-lookup"><span data-stu-id="31bce-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31bce-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31bce-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31bce-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31bce-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31bce-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="31bce-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="31bce-139">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="31bce-139">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="31bce-140">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="31bce-140">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="31bce-141">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="31bce-141">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="31bce-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="31bce-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="31bce-143">**glGet**</span><span class="sxs-lookup"><span data-stu-id="31bce-143">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="31bce-144">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="31bce-144">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="31bce-145">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="31bce-145">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





