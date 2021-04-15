---
title: 'glScissor 函式 (Gl) '
description: GlScissor 函式會定義剪式方塊。
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glScissor 函式 OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466917"
---
# <a name="glscissor-function"></a><span data-ttu-id="23a16-104">glScissor 函式</span><span class="sxs-lookup"><span data-stu-id="23a16-104">glScissor function</span></span>

<span data-ttu-id="23a16-105">**GlScissor** 函式會定義剪式方塊。</span><span class="sxs-lookup"><span data-stu-id="23a16-105">The **glScissor** function defines the scissor box.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a16-106">語法</span><span class="sxs-lookup"><span data-stu-id="23a16-106">Syntax</span></span>


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="23a16-107">參數</span><span class="sxs-lookup"><span data-stu-id="23a16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a16-108">*x*</span><span class="sxs-lookup"><span data-stu-id="23a16-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="23a16-109">垂直軸的 x (垂直軸) 座標（剪下方塊的左下角）。</span><span class="sxs-lookup"><span data-stu-id="23a16-109">The x (vertical axis) coordinate for the lower-left corner of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="23a16-110">*y*</span><span class="sxs-lookup"><span data-stu-id="23a16-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="23a16-111">[剪下] 方塊左上角的 y (水準軸) 座標。</span><span class="sxs-lookup"><span data-stu-id="23a16-111">The y (horizontal axis) coordinate for the lower-left corner of the scissor box.</span></span> <span data-ttu-id="23a16-112">同時，x 和 y 會指定剪下方塊的左下角。</span><span class="sxs-lookup"><span data-stu-id="23a16-112">Together, x and y specify the lower-left corner of the scissor box.</span></span> <span data-ttu-id="23a16-113">一開始 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="23a16-113">Initially (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="23a16-114">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="23a16-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="23a16-115">剪式方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="23a16-115">The width of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="23a16-116">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="23a16-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="23a16-117">剪式方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="23a16-117">The height of the scissor box.</span></span> <span data-ttu-id="23a16-118">當 OpenGL 內容 *第一次* 附加至視窗時，會將 *寬度* 和 *高度* 設定為該視窗的維度。</span><span class="sxs-lookup"><span data-stu-id="23a16-118">When an OpenGL context is *first* attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a16-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="23a16-119">Return value</span></span>

<span data-ttu-id="23a16-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="23a16-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="23a16-121">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="23a16-121">Error codes</span></span>

<span data-ttu-id="23a16-122">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="23a16-122">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="23a16-123">Name</span><span class="sxs-lookup"><span data-stu-id="23a16-123">Name</span></span>                                                                                                  | <span data-ttu-id="23a16-124">意義</span><span class="sxs-lookup"><span data-stu-id="23a16-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23a16-125"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="23a16-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="23a16-126">*寬度* 或 *高度* 都是負數。</span><span class="sxs-lookup"><span data-stu-id="23a16-126">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="23a16-127"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="23a16-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="23a16-128">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="23a16-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="23a16-129">備註</span><span class="sxs-lookup"><span data-stu-id="23a16-129">Remarks</span></span>

<span data-ttu-id="23a16-130">**GlScissor** 函式會在視窗座標中定義稱為剪下方塊的矩形。</span><span class="sxs-lookup"><span data-stu-id="23a16-130">The **glScissor** function defines a rectangle, called the scissor box, in window coordinates.</span></span> <span data-ttu-id="23a16-131">前兩個參數 *x* 和 *y* 指定方塊左下角。</span><span class="sxs-lookup"><span data-stu-id="23a16-131">The first two parameters, *x* and *y*, specify the lower-left corner of the box.</span></span> <span data-ttu-id="23a16-132">*寬度* 和 *高度* 參數會指定方塊的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="23a16-132">The *width* and *height* parameters specify the width and height of the box.</span></span>

<span data-ttu-id="23a16-133">使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 剪下測試，可啟用和停用剪式測試 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="23a16-133">The scissor test is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_SCISSOR\_TEST.</span></span> <span data-ttu-id="23a16-134">當剪下測試啟用時，繪製命令只能修改位於剪下方塊內的圖元。</span><span class="sxs-lookup"><span data-stu-id="23a16-134">While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands.</span></span> <span data-ttu-id="23a16-135">視窗座標在畫面格緩衝區圖元的共用角落具有整數值，因此 **glScissor** (0、0、1、1) 只允許修改視窗中的左下圖元，而 **glScissor** (0、0、0、0) 不允許修改視窗中的所有圖元。</span><span class="sxs-lookup"><span data-stu-id="23a16-135">Window coordinates have integer values at the shared corners of framebuffer pixels, so **glScissor**(0,0,1,1) allows only the lower-left pixel in the window to be modified, and **glScissor**(0,0,0,0) disallows modification to all pixels in the window.</span></span>

<span data-ttu-id="23a16-136">當剪式測試停用時，就如同剪下方塊包含整個視窗一樣。</span><span class="sxs-lookup"><span data-stu-id="23a16-136">When the scissor test is disabled, it is as though the scissor box includes the entire window.</span></span>

<span data-ttu-id="23a16-137">下列函式會取出與 **glScissor** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="23a16-137">The following functions retrieve information related to **glScissor**:</span></span>

<span data-ttu-id="23a16-138">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 剪狀方塊的 glGet \_</span><span class="sxs-lookup"><span data-stu-id="23a16-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SCISSOR\_BOX</span></span>

<span data-ttu-id="23a16-139">[](glisenabled.md)具有引數 GL \_ 剪式測試的 glIsEnabled \_</span><span class="sxs-lookup"><span data-stu-id="23a16-139">[**glIsEnabled**](glisenabled.md) with argument GL\_SCISSOR\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="23a16-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="23a16-140">Requirements</span></span>



| <span data-ttu-id="23a16-141">需求</span><span class="sxs-lookup"><span data-stu-id="23a16-141">Requirement</span></span> | <span data-ttu-id="23a16-142">值</span><span class="sxs-lookup"><span data-stu-id="23a16-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23a16-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23a16-143">Minimum supported client</span></span><br/> | <span data-ttu-id="23a16-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23a16-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="23a16-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23a16-145">Minimum supported server</span></span><br/> | <span data-ttu-id="23a16-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23a16-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23a16-147">標頭</span><span class="sxs-lookup"><span data-stu-id="23a16-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="23a16-148"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="23a16-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="23a16-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="23a16-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="23a16-150"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="23a16-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="23a16-151">DLL</span><span class="sxs-lookup"><span data-stu-id="23a16-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23a16-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23a16-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23a16-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23a16-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a16-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="23a16-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="23a16-155">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="23a16-155">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="23a16-156">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="23a16-156">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="23a16-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="23a16-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="23a16-158">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="23a16-158">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





