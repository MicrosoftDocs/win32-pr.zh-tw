---
title: 'glGetPolygonStipple 函式 (Gl) '
description: GlGetPolygonStipple 函數會傳回多邊形 stipple 模式。
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- glGetPolygonStipple 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843232"
---
# <a name="glgetpolygonstipple-function"></a><span data-ttu-id="1341b-104">glGetPolygonStipple 函式</span><span class="sxs-lookup"><span data-stu-id="1341b-104">glGetPolygonStipple function</span></span>

<span data-ttu-id="1341b-105">**GlGetPolygonStipple** 函數會傳回多邊形 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="1341b-105">The **glGetPolygonStipple** function returns the polygon stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="1341b-106">語法</span><span class="sxs-lookup"><span data-stu-id="1341b-106">Syntax</span></span>


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="1341b-107">參數</span><span class="sxs-lookup"><span data-stu-id="1341b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1341b-108">*面具*</span><span class="sxs-lookup"><span data-stu-id="1341b-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="1341b-109">傳回 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="1341b-109">Returns the stipple pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1341b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1341b-110">Return value</span></span>

<span data-ttu-id="1341b-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1341b-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1341b-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1341b-112">Error codes</span></span>

<span data-ttu-id="1341b-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1341b-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1341b-114">Name</span><span class="sxs-lookup"><span data-stu-id="1341b-114">Name</span></span>                                                                                                  | <span data-ttu-id="1341b-115">意義</span><span class="sxs-lookup"><span data-stu-id="1341b-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1341b-116"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="1341b-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1341b-117">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="1341b-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1341b-118">備註</span><span class="sxs-lookup"><span data-stu-id="1341b-118">Remarks</span></span>

<span data-ttu-id="1341b-119">**GlGetPolygonStipple** 函數會透過 *mask* 參數傳回32x32 多邊形 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="1341b-119">The **glGetPolygonStipple** function returns a 32x32 polygon stipple pattern through the *mask* parameter.</span></span> <span data-ttu-id="1341b-120">模式會封裝至記憶體中，如同 [**glReadPixels**](glreadpixels.md) 具有32的 *高度* 和 *寬度* 、gl 點陣圖的 *型* 別 \_ ，以及 gl 色彩索引的 *格式* ， \_ \_ 而且 stipple 模式儲存在內部的32x32 色彩索引緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="1341b-120">The pattern is packed into memory as if [**glReadPixels**](glreadpixels.md) with both *height* and *width* of 32, *type* of GL\_BITMAP, and *format* of GL\_COLOR\_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer.</span></span> <span data-ttu-id="1341b-121">不過，不同于 **glReadPixels**，圖元傳輸作業 (shift、offset 和圖元地圖) 不會套用至傳回的 stipple 影像。</span><span class="sxs-lookup"><span data-stu-id="1341b-121">Unlike **glReadPixels**, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.</span></span>

<span data-ttu-id="1341b-122">如果產生錯誤，則不會對 *遮罩* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="1341b-122">If an error is generated, no change is made to the contents of *mask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1341b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1341b-123">Requirements</span></span>



| <span data-ttu-id="1341b-124">需求</span><span class="sxs-lookup"><span data-stu-id="1341b-124">Requirement</span></span> | <span data-ttu-id="1341b-125">值</span><span class="sxs-lookup"><span data-stu-id="1341b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1341b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1341b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1341b-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1341b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1341b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1341b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1341b-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1341b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1341b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1341b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1341b-131"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="1341b-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1341b-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="1341b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="1341b-133"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1341b-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1341b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1341b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1341b-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1341b-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1341b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1341b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1341b-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1341b-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1341b-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1341b-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1341b-139">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="1341b-139">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="1341b-140">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="1341b-140">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="1341b-141">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="1341b-141">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="1341b-142">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="1341b-142">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





