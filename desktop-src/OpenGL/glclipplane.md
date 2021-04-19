---
title: 'glClipPlane 函式 (Gl) '
description: GlClipPlane 函式會指定用來裁剪所有幾何的平面。
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glClipPlane 函式 OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967550"
---
# <a name="glclipplane-function"></a><span data-ttu-id="35f47-104">glClipPlane 函式</span><span class="sxs-lookup"><span data-stu-id="35f47-104">glClipPlane function</span></span>

<span data-ttu-id="35f47-105">**GlClipPlane** 函式會指定用來裁剪所有幾何的平面。</span><span class="sxs-lookup"><span data-stu-id="35f47-105">The **glClipPlane** function specifies a plane against which all geometry is clipped.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f47-106">語法</span><span class="sxs-lookup"><span data-stu-id="35f47-106">Syntax</span></span>


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="35f47-107">參數</span><span class="sxs-lookup"><span data-stu-id="35f47-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f47-108">*飛機*</span><span class="sxs-lookup"><span data-stu-id="35f47-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="35f47-109">正在放置的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="35f47-109">The clipping plane that is being positioned.</span></span> <span data-ttu-id="35f47-110">表單 GL 剪輯平面 i 的符號名稱，在這種情況下， \_ \_ 會接受0到 GL \*\*  \_ 最大 \_ 剪輯 \_ 平面-1 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="35f47-110">Symbolic names of the form GL\_CLIP\_PLANE *i*, where *i* is an integer between 0 and GL\_MAX\_CLIP\_PLANES - 1, are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="35f47-111">*方程*</span><span class="sxs-lookup"><span data-stu-id="35f47-111">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="35f47-112">四個雙精確度浮點值陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="35f47-112">The address of an array of four double-precision floating-point values.</span></span> <span data-ttu-id="35f47-113">這些值會被視為平面方程式。</span><span class="sxs-lookup"><span data-stu-id="35f47-113">These values are interpreted as a plane equation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f47-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="35f47-114">Return value</span></span>

<span data-ttu-id="35f47-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="35f47-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35f47-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="35f47-116">Error codes</span></span>

<span data-ttu-id="35f47-117">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="35f47-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="35f47-118">Name</span><span class="sxs-lookup"><span data-stu-id="35f47-118">Name</span></span>                                                                                                  | <span data-ttu-id="35f47-119">意義</span><span class="sxs-lookup"><span data-stu-id="35f47-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35f47-120"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="35f47-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="35f47-121">*平面* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="35f47-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="35f47-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="35f47-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="35f47-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="35f47-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="35f47-124">備註</span><span class="sxs-lookup"><span data-stu-id="35f47-124">Remarks</span></span>

<span data-ttu-id="35f47-125">幾何一律會根據 *x*、 *y* 和 *z* 的六平面錐迭界進行裁剪。</span><span class="sxs-lookup"><span data-stu-id="35f47-125">Geometry is always clipped against the boundaries of a six-plane frustum in *x*, *y*, and *z*.</span></span> <span data-ttu-id="35f47-126">**GlClipPlane** 函式可讓您指定其他平面的規格，而不一定是垂直于 *x* 軸、 *y* 軸或 *z* 軸，以裁剪所有幾何。</span><span class="sxs-lookup"><span data-stu-id="35f47-126">The **glClipPlane** function allows the specification of additional planes, not necessarily perpendicular to the *x-* axis, *y-* axis, or *z*-axis, against which all geometry is clipped.</span></span> <span data-ttu-id="35f47-127">最高可指定最高 GL 的 \_ \_ 剪輯 \_ 平面平面，其中 GL \_ 最大 \_ 剪輯 \_ 平面在所有的執行中至少為六個。</span><span class="sxs-lookup"><span data-stu-id="35f47-127">Up to GL\_MAX\_CLIP\_PLANES planes can be specified, where GL\_MAX\_CLIP\_PLANES is at least six in all implementations.</span></span> <span data-ttu-id="35f47-128">因為產生的裁剪區域是所定義之半空格的交集，所以一律為凸間距。</span><span class="sxs-lookup"><span data-stu-id="35f47-128">Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.</span></span>

<span data-ttu-id="35f47-129">**GlClipPlane** 函式會使用四個元件的平面方程式來指定半個空格。</span><span class="sxs-lookup"><span data-stu-id="35f47-129">The **glClipPlane** function specifies a half-space using a four-component plane equation.</span></span> <span data-ttu-id="35f47-130">當您呼叫 **glClipPlane** 時 *，會* 由模型矩陣的反向轉換方程式，並儲存在產生的眼睛座標中。</span><span class="sxs-lookup"><span data-stu-id="35f47-130">When you call **glClipPlane**,*equation* is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates.</span></span> <span data-ttu-id="35f47-131">模型矩陣的後續變更對預存的平面方程式元件沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="35f47-131">Subsequent changes to the modelview matrix have no effect on the stored plane-equation components.</span></span> <span data-ttu-id="35f47-132">如果具有預存平面方程式元件之頂點的眼睛座標的點乘積為正數或零，則頂點會與該裁剪平面有關。</span><span class="sxs-lookup"><span data-stu-id="35f47-132">If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane.</span></span> <span data-ttu-id="35f47-133">否則，就會退出。</span><span class="sxs-lookup"><span data-stu-id="35f47-133">Otherwise, it is out.</span></span>

<span data-ttu-id="35f47-134">使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 函數來啟用和停用裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="35f47-134">Use the [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions to enable and disable clipping planes.</span></span> <span data-ttu-id="35f47-135">使用引數 GL 的 [剪下] 剪輯平面來呼叫裁剪平面 \_ \_ ，其中 *i* 是平面編號。\*\*</span><span class="sxs-lookup"><span data-stu-id="35f47-135">Call clipping planes with the argument GL\_CLIP\_PLANE *i*, where *i* is the plane number.</span></span>

<span data-ttu-id="35f47-136">依預設，所有裁剪平面都會定義為眼睛座標中的 (0、0、0、0) ，而且會停用。</span><span class="sxs-lookup"><span data-stu-id="35f47-136">By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.</span></span>

<span data-ttu-id="35f47-137">GL \_ 剪輯 \_ 平面 *i* = gl \_ 剪輯 \_ PLANE0 + *i* 是永遠的情況。</span><span class="sxs-lookup"><span data-stu-id="35f47-137">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="35f47-138">下列函式會取出與 **glClipPlane** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="35f47-138">The following functions retrieve information related to **glClipPlane**:</span></span>

[<span data-ttu-id="35f47-139">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="35f47-139">**glGetClipPlane**</span></span>](glgetclipplane.md)

<span data-ttu-id="35f47-140">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 剪輯 \_ 平面 *i*</span><span class="sxs-lookup"><span data-stu-id="35f47-140">[**glIsEnabled**](glisenabled.md) with argument GL\_CLIP\_PLANE *i*</span></span>

## <a name="requirements"></a><span data-ttu-id="35f47-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="35f47-141">Requirements</span></span>



| <span data-ttu-id="35f47-142">需求</span><span class="sxs-lookup"><span data-stu-id="35f47-142">Requirement</span></span> | <span data-ttu-id="35f47-143">值</span><span class="sxs-lookup"><span data-stu-id="35f47-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f47-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35f47-144">Minimum supported client</span></span><br/> | <span data-ttu-id="35f47-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35f47-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="35f47-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35f47-146">Minimum supported server</span></span><br/> | <span data-ttu-id="35f47-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35f47-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35f47-148">標頭</span><span class="sxs-lookup"><span data-stu-id="35f47-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="35f47-149"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="35f47-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="35f47-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="35f47-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="35f47-151"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35f47-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35f47-152">DLL</span><span class="sxs-lookup"><span data-stu-id="35f47-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f47-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f47-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f47-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35f47-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f47-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="35f47-155">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="35f47-156">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="35f47-156">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="35f47-157">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="35f47-157">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="35f47-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="35f47-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="35f47-159">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="35f47-159">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="35f47-160">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="35f47-160">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





