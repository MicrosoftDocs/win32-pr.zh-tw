---
title: 'glDepthRange 函式 (Gl) '
description: GlDepthRange 函式會指定從正規化裝置座標到視窗座標的 z 值對應。
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- glDepthRange 函式 OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384254"
---
# <a name="gldepthrange-function"></a><span data-ttu-id="7492e-104">glDepthRange 函式</span><span class="sxs-lookup"><span data-stu-id="7492e-104">glDepthRange function</span></span>

<span data-ttu-id="7492e-105">**GlDepthRange** 函式會指定從正規化裝置座標到視窗座標的 *z* 值對應。</span><span class="sxs-lookup"><span data-stu-id="7492e-105">The **glDepthRange** function specifies the mapping of *z* values from normalized device coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="7492e-106">語法</span><span class="sxs-lookup"><span data-stu-id="7492e-106">Syntax</span></span>


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a><span data-ttu-id="7492e-107">參數</span><span class="sxs-lookup"><span data-stu-id="7492e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7492e-108">*zNear*</span><span class="sxs-lookup"><span data-stu-id="7492e-108">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="7492e-109">接近裁剪平面與視窗座標的對應。</span><span class="sxs-lookup"><span data-stu-id="7492e-109">The mapping of the near clipping plane to window coordinates.</span></span> <span data-ttu-id="7492e-110">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="7492e-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="7492e-111">*zFar*</span><span class="sxs-lookup"><span data-stu-id="7492e-111">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="7492e-112">最遠裁剪平面到視窗座標的對應。</span><span class="sxs-lookup"><span data-stu-id="7492e-112">The mapping of the far clipping plane to window coordinates.</span></span> <span data-ttu-id="7492e-113">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="7492e-113">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7492e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7492e-114">Return value</span></span>

<span data-ttu-id="7492e-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7492e-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7492e-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7492e-116">Error codes</span></span>

<span data-ttu-id="7492e-117">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7492e-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7492e-118">Name</span><span class="sxs-lookup"><span data-stu-id="7492e-118">Name</span></span>                                                                                                  | <span data-ttu-id="7492e-119">意義</span><span class="sxs-lookup"><span data-stu-id="7492e-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7492e-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7492e-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7492e-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="7492e-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7492e-122">備註</span><span class="sxs-lookup"><span data-stu-id="7492e-122">Remarks</span></span>

<span data-ttu-id="7492e-123">在裁剪和除以 *w* 之後， *z* 座標的範圍從0.0 到1.0，對應至接近或遠裁剪的平面。</span><span class="sxs-lookup"><span data-stu-id="7492e-123">After clipping and division by *w*, *z* -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes.</span></span> <span data-ttu-id="7492e-124">**GlDepthRange** 函式會將此範圍中正規化 *z* 座標的線性對應指定為視窗 *z* 座標。</span><span class="sxs-lookup"><span data-stu-id="7492e-124">The **glDepthRange** function specifies a linear mapping of the normalized *z*-coordinates in this range to window *z*-coordinates.</span></span> <span data-ttu-id="7492e-125">無論實際深度緩衝區的執行程度為何，都可以將視窗座標深度值視為範圍從0.0 到 1.0 (例如色彩元件) 。</span><span class="sxs-lookup"><span data-stu-id="7492e-125">Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components).</span></span> <span data-ttu-id="7492e-126">因此， **glDepthRange** 所接受的值在被接受之前，都會壓制到這個範圍。</span><span class="sxs-lookup"><span data-stu-id="7492e-126">Thus, the values accepted by **glDepthRange** are both clamped to this range before they are accepted.</span></span>

<span data-ttu-id="7492e-127"> (0，1) 的預設對應會將接近的平面對應到0，而將最遠的平面對應至1。</span><span class="sxs-lookup"><span data-stu-id="7492e-127">The default mapping of (0,1) maps the near plane to 0 and the far plane to 1.</span></span> <span data-ttu-id="7492e-128">透過此對應，深度緩衝區範圍會完全使用。</span><span class="sxs-lookup"><span data-stu-id="7492e-128">With this mapping, the depth buffer range is fully utilized.</span></span>

<span data-ttu-id="7492e-129">*ZNear* 小於 *zFar* 是不必要的。</span><span class="sxs-lookup"><span data-stu-id="7492e-129">It is not necessary that *zNear* be less than *zFar*.</span></span> <span data-ttu-id="7492e-130">反向對應，例如 (1、0) 是可接受的。</span><span class="sxs-lookup"><span data-stu-id="7492e-130">Reverse mappings such as (1,0) are acceptable.</span></span>

<span data-ttu-id="7492e-131">下列函式會抓取 **glDepthRange** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="7492e-131">The following function retrieves information related to **glDepthRange**:</span></span>

<span data-ttu-id="7492e-132">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 深度 \_ 範圍的 glGet</span><span class="sxs-lookup"><span data-stu-id="7492e-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_RANGE</span></span>

## <a name="requirements"></a><span data-ttu-id="7492e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7492e-133">Requirements</span></span>



| <span data-ttu-id="7492e-134">需求</span><span class="sxs-lookup"><span data-stu-id="7492e-134">Requirement</span></span> | <span data-ttu-id="7492e-135">值</span><span class="sxs-lookup"><span data-stu-id="7492e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7492e-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7492e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7492e-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7492e-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7492e-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7492e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7492e-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7492e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7492e-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7492e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7492e-141"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="7492e-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7492e-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="7492e-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="7492e-143"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7492e-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7492e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7492e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7492e-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7492e-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7492e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7492e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7492e-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7492e-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7492e-148">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="7492e-148">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="7492e-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7492e-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7492e-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="7492e-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7492e-151">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="7492e-151">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





