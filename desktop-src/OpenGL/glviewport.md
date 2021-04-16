---
title: 'glViewport 函式 (Gl) '
description: GlViewport 函式會設定此功能區。
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport 函式 OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104553505"
---
# <a name="glviewport-function"></a><span data-ttu-id="fae3a-104">glViewport 函式</span><span class="sxs-lookup"><span data-stu-id="fae3a-104">glViewport function</span></span>

<span data-ttu-id="fae3a-105">**GlViewport** 函式會設定此功能區。</span><span class="sxs-lookup"><span data-stu-id="fae3a-105">The **glViewport** function sets the viewport.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae3a-106">語法</span><span class="sxs-lookup"><span data-stu-id="fae3a-106">Syntax</span></span>


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="fae3a-107">參數</span><span class="sxs-lookup"><span data-stu-id="fae3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae3a-108">*x*</span><span class="sxs-lookup"><span data-stu-id="fae3a-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="fae3a-109">以圖元為單位的區式矩形左下角。</span><span class="sxs-lookup"><span data-stu-id="fae3a-109">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="fae3a-110">預設值為 (0,0)。</span><span class="sxs-lookup"><span data-stu-id="fae3a-110">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="fae3a-111">*y*</span><span class="sxs-lookup"><span data-stu-id="fae3a-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="fae3a-112">以圖元為單位的區式矩形左下角。</span><span class="sxs-lookup"><span data-stu-id="fae3a-112">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="fae3a-113">預設值為 (0,0)。</span><span class="sxs-lookup"><span data-stu-id="fae3a-113">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="fae3a-114">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="fae3a-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="fae3a-115">區的寬度。</span><span class="sxs-lookup"><span data-stu-id="fae3a-115">The width of the viewport.</span></span> <span data-ttu-id="fae3a-116">當 OpenGL 內容第一次附加至視窗時，會將 *寬度* 和 *高度* 設定為該視窗的維度。</span><span class="sxs-lookup"><span data-stu-id="fae3a-116">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> <dt>

<span data-ttu-id="fae3a-117">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="fae3a-117">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="fae3a-118">視口的高度。</span><span class="sxs-lookup"><span data-stu-id="fae3a-118">The height of the viewport.</span></span> <span data-ttu-id="fae3a-119">當 OpenGL 內容第一次附加至視窗時，會將 *寬度* 和 *高度* 設定為該視窗的維度。</span><span class="sxs-lookup"><span data-stu-id="fae3a-119">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae3a-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="fae3a-120">Return value</span></span>

<span data-ttu-id="fae3a-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fae3a-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fae3a-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fae3a-122">Error codes</span></span>

<span data-ttu-id="fae3a-123">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fae3a-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fae3a-124">Name</span><span class="sxs-lookup"><span data-stu-id="fae3a-124">Name</span></span>                                                                                                  | <span data-ttu-id="fae3a-125">意義</span><span class="sxs-lookup"><span data-stu-id="fae3a-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fae3a-126"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="fae3a-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fae3a-127">*寬度* 或 *高度* 都是負數。</span><span class="sxs-lookup"><span data-stu-id="fae3a-127">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="fae3a-128"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="fae3a-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fae3a-129">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="fae3a-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fae3a-130">備註</span><span class="sxs-lookup"><span data-stu-id="fae3a-130">Remarks</span></span>

<span data-ttu-id="fae3a-131">**GlViewport** 函式會指定從標準化裝置座標到視窗座標之 *x* 和 *y* 的仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="fae3a-131">The **glViewport** function specifies the affine transformation of *x* and *y* from normalized device coordinates to window coordinates.</span></span> <span data-ttu-id="fae3a-132">讓 (*x*<sub>nd</sub> ， *y*<sub>nd</sub> ) 為標準化裝置座標。</span><span class="sxs-lookup"><span data-stu-id="fae3a-132">Let (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) be normalized device coordinates.</span></span> <span data-ttu-id="fae3a-133">視窗座標 (*x*<sub>w</sub> ， *y*<sub>w</sub> ) 接著計算如下：</span><span class="sxs-lookup"><span data-stu-id="fae3a-133">The window coordinates (*x*<sub>w</sub> , *y*<sub>w</sub> ) are then computed as follows:</span></span>

![顯示視窗座標計算的方程式。](images/view01.png)

<span data-ttu-id="fae3a-135">當區寬度和高度以無訊息方式壓制至相依于執行的範圍時。</span><span class="sxs-lookup"><span data-stu-id="fae3a-135">Viewport width and height are silently clamped to a range that depends on the implementation.</span></span> <span data-ttu-id="fae3a-136">藉由呼叫 **glGet** 與引數 GL \_ 最大值區變暗，即可查詢此範圍 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="fae3a-136">This range is queried by calling **glGet** with argument GL\_MAX\_VIEWPORT\_DIMS.</span></span>

<span data-ttu-id="fae3a-137">下列函式會取出與 **glViewport** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="fae3a-137">The following functions retrieve information related to **glViewport**:</span></span>

<span data-ttu-id="fae3a-138">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 區的 glGet</span><span class="sxs-lookup"><span data-stu-id="fae3a-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VIEWPORT</span></span>

<span data-ttu-id="fae3a-139">具有引數 GL \_ 最大區的 glGet 變 \_ \_ 暗</span><span class="sxs-lookup"><span data-stu-id="fae3a-139">**glGet** with argument GL\_MAX\_VIEWPORT\_DIMS</span></span>

## <a name="requirements"></a><span data-ttu-id="fae3a-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="fae3a-140">Requirements</span></span>



| <span data-ttu-id="fae3a-141">需求</span><span class="sxs-lookup"><span data-stu-id="fae3a-141">Requirement</span></span> | <span data-ttu-id="fae3a-142">值</span><span class="sxs-lookup"><span data-stu-id="fae3a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fae3a-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fae3a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fae3a-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fae3a-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fae3a-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fae3a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fae3a-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fae3a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fae3a-147">標頭</span><span class="sxs-lookup"><span data-stu-id="fae3a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae3a-148"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="fae3a-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fae3a-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="fae3a-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="fae3a-150"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fae3a-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fae3a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="fae3a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae3a-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae3a-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fae3a-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fae3a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae3a-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fae3a-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fae3a-155">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="fae3a-155">**glDepthRange**</span></span>](gldepthrange.md)
</dt> </dl>

 

 





