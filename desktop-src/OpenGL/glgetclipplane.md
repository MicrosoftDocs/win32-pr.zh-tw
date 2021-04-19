---
title: 'glGetClipPlane 函式 (Gl) '
description: GlGetClipPlane 函數會傳回指定裁剪平面的係數。
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glGetClipPlane 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967771"
---
# <a name="glgetclipplane-function"></a><span data-ttu-id="de4c0-104">glGetClipPlane 函式</span><span class="sxs-lookup"><span data-stu-id="de4c0-104">glGetClipPlane function</span></span>

<span data-ttu-id="de4c0-105">**GlGetClipPlane** 函數會傳回指定裁剪平面的係數。</span><span class="sxs-lookup"><span data-stu-id="de4c0-105">The **glGetClipPlane** function returns the coefficients of the specified clipping plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4c0-106">語法</span><span class="sxs-lookup"><span data-stu-id="de4c0-106">Syntax</span></span>


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="de4c0-107">參數</span><span class="sxs-lookup"><span data-stu-id="de4c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4c0-108">*飛機*</span><span class="sxs-lookup"><span data-stu-id="de4c0-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="de4c0-109">裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="de4c0-109">A clipping plane.</span></span> <span data-ttu-id="de4c0-110">裁剪平面的數目取決於執行，但至少支援六個裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="de4c0-110">The number of clipping planes depends on the implementation, but at least six clipping planes are supported.</span></span> <span data-ttu-id="de4c0-111">它們是以 [GL 的格式] 剪輯平面的符號名稱來識別 \_ \_ ，其中 0 = *i* < GL  \_ 最大 \_ 剪輯 \_ 平面。</span><span class="sxs-lookup"><span data-stu-id="de4c0-111">They are identified by symbolic names of the form GL\_CLIP\_PLANE *i* where 0 = *i* < GL\_MAX\_CLIP\_PLANES.</span></span>

</dd> <dt>

<span data-ttu-id="de4c0-112">*方程*</span><span class="sxs-lookup"><span data-stu-id="de4c0-112">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="de4c0-113">傳回四個雙精確度值，這是眼睛座標 *平面* 的平面方程式係數。</span><span class="sxs-lookup"><span data-stu-id="de4c0-113">Returns four double-precision values that are the coefficients of the plane equation of *plane* in eye coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4c0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="de4c0-114">Return value</span></span>

<span data-ttu-id="de4c0-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="de4c0-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="de4c0-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="de4c0-116">Error codes</span></span>

<span data-ttu-id="de4c0-117">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="de4c0-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="de4c0-118">Name</span><span class="sxs-lookup"><span data-stu-id="de4c0-118">Name</span></span>                                                                                                  | <span data-ttu-id="de4c0-119">意義</span><span class="sxs-lookup"><span data-stu-id="de4c0-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de4c0-120"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="de4c0-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="de4c0-121">*平面* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="de4c0-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="de4c0-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="de4c0-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="de4c0-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="de4c0-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="de4c0-124">備註</span><span class="sxs-lookup"><span data-stu-id="de4c0-124">Remarks</span></span>

<span data-ttu-id="de4c0-125">**GlGetClipPlane** 函 *式* 會在方程式中傳回 *平面* 的平面方程式四個係數。</span><span class="sxs-lookup"><span data-stu-id="de4c0-125">The **glGetClipPlane** function returns in *equation* the four coefficients of the plane equation for *plane*.</span></span>

<span data-ttu-id="de4c0-126">GL \_ 剪輯 \_ 平面 *i* = gl \_ 剪輯 \_ PLANE0 + *i* 是永遠的情況。</span><span class="sxs-lookup"><span data-stu-id="de4c0-126">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="de4c0-127">如果產生錯誤，則不會對方程式內容進行任何變更 *。*</span><span class="sxs-lookup"><span data-stu-id="de4c0-127">If an error is generated, no change is made to the contents of *equation*.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4c0-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="de4c0-128">Requirements</span></span>



| <span data-ttu-id="de4c0-129">需求</span><span class="sxs-lookup"><span data-stu-id="de4c0-129">Requirement</span></span> | <span data-ttu-id="de4c0-130">值</span><span class="sxs-lookup"><span data-stu-id="de4c0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de4c0-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de4c0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="de4c0-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de4c0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="de4c0-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de4c0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="de4c0-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de4c0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de4c0-135">標頭</span><span class="sxs-lookup"><span data-stu-id="de4c0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="de4c0-136"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="de4c0-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="de4c0-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="de4c0-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="de4c0-138"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="de4c0-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="de4c0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="de4c0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de4c0-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de4c0-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4c0-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de4c0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4c0-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="de4c0-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="de4c0-143">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="de4c0-143">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="de4c0-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="de4c0-144">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





