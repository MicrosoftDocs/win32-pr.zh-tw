---
title: 'glPolygonStipple 函式 (Gl) '
description: GlPolygonStipple 函數會設定多邊形 stippling 模式。
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glPolygonStipple 函式 OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465653"
---
# <a name="glpolygonstipple-function"></a><span data-ttu-id="73740-104">glPolygonStipple 函式</span><span class="sxs-lookup"><span data-stu-id="73740-104">glPolygonStipple function</span></span>

<span data-ttu-id="73740-105">**GlPolygonStipple** 函數會設定多邊形 stippling 模式。</span><span class="sxs-lookup"><span data-stu-id="73740-105">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="73740-106">語法</span><span class="sxs-lookup"><span data-stu-id="73740-106">Syntax</span></span>


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="73740-107">參數</span><span class="sxs-lookup"><span data-stu-id="73740-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73740-108">*面具*</span><span class="sxs-lookup"><span data-stu-id="73740-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="73740-109">32 stipple 模式的指標，會以 [**glDrawPixels**](gldrawpixels.md) 解壓縮圖元的相同方式從記憶體解壓縮。</span><span class="sxs-lookup"><span data-stu-id="73740-109">A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that [**glDrawPixels**](gldrawpixels.md) unpacks pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73740-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="73740-110">Return value</span></span>

<span data-ttu-id="73740-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="73740-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73740-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="73740-112">Error codes</span></span>

<span data-ttu-id="73740-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73740-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="73740-114">Name</span><span class="sxs-lookup"><span data-stu-id="73740-114">Name</span></span>                                                                                                  | <span data-ttu-id="73740-115">意義</span><span class="sxs-lookup"><span data-stu-id="73740-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73740-116"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="73740-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="73740-117">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="73740-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="73740-118">備註</span><span class="sxs-lookup"><span data-stu-id="73740-118">Remarks</span></span>

<span data-ttu-id="73740-119">**GlPolygonStipple** 函數會設定多邊形 stippling 模式。</span><span class="sxs-lookup"><span data-stu-id="73740-119">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span> <span data-ttu-id="73740-120">多邊形 stippling，例如行 stippling (查看 [**glLineStipple**](gllinestipple.md)) 、遮罩由點陣產生的特定片段，並建立模式。</span><span class="sxs-lookup"><span data-stu-id="73740-120">Polygon stippling, like line stippling (see [**glLineStipple**](gllinestipple.md)), masks out certain fragments produced by rasterization, creating a pattern.</span></span> <span data-ttu-id="73740-121">Stippling 與多邊形消除鋸齒無關。</span><span class="sxs-lookup"><span data-stu-id="73740-121">Stippling is independent of polygon antialiasing.</span></span>

<span data-ttu-id="73740-122">*Mask* 參數是 32 stipple 模式的指標，其儲存在記憶體中，就像提供給 **glDrawPixels** 且 *高度* 和 *寬度* 都等於32的圖元資料、GL 色彩索引的圖元 *格式* \_ \_ ，以及 gl 點陣圖的資料 *類型* \_ 。</span><span class="sxs-lookup"><span data-stu-id="73740-122">The *mask* parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to **glDrawPixels** with *height* and *width* both equal to 32, a pixel *format* of GL\_COLOR\_INDEX, and data *type* of GL\_BITMAP.</span></span> <span data-ttu-id="73740-123">也就是說，stipple 模式會以非符號位元組封裝的1位色彩索引的32x32 陣列來表示。</span><span class="sxs-lookup"><span data-stu-id="73740-123">That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes.</span></span> <span data-ttu-id="73740-124">[**GlPixelStore**](glpixelstore-functions.md)函式參數（例如 GL \_ 解壓縮 \_ 交換 \_ 位元組和 gl \_ 解壓縮 \_ LSB \_ ）會先影響將位組合成 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="73740-124">The [**glPixelStore**](glpixelstore-functions.md) function parameters, such as GL\_UNPACK\_SWAP\_BYTES and GL\_UNPACK\_LSB\_FIRST, affect the assembling of the bits into a stipple pattern.</span></span> <span data-ttu-id="73740-125">不過，圖元傳輸作業 (shift、offset 和圖元地圖) 不會套用至 stipple 影像。</span><span class="sxs-lookup"><span data-stu-id="73740-125">Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.</span></span>

<span data-ttu-id="73740-126">使用引數 GL 多邊形 STIPPLE，可使用 [**glEnable**](glenable.md) 和 **glDisable** 來啟用和停用多邊形 stippling \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="73740-126">Polygon stippling is enabled and disabled with [**glEnable**](glenable.md) and **glDisable**, using argument GL\_POLYGON\_STIPPLE.</span></span> <span data-ttu-id="73740-127">如果啟用，則只有在 (*x*<sub>w</sub> mod 32) 位在 stipple 模式的第一個資料列中的 (*y*<sub>w</sub> mod 32) 第一個資料列時，才會將具有視窗座標 *x*<sub>w</sub>和 *y*<sub>w</sub>的柵格化多邊形片段傳送至 OpenGL 的下一個階段。</span><span class="sxs-lookup"><span data-stu-id="73740-127">If enabled, a rasterized polygon fragment with window coordinates *x*<sub>w</sub> and *y*<sub>w</sub> is sent to the next stage of OpenGL if and only if the (*x*<sub>w</sub> mod 32)th bit in the (*y*<sub>w</sub> mod 32)th row of the stipple pattern is one.</span></span> <span data-ttu-id="73740-128">當多邊形 stippling 停用時，就如同 stipple 模式都是一樣。</span><span class="sxs-lookup"><span data-stu-id="73740-128">When polygon stippling is disabled, it is as if the stipple pattern were all ones.</span></span>

<span data-ttu-id="73740-129">下列函式會取出與 **glPolygonStipple** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="73740-129">The following functions retrieve information related to **glPolygonStipple**:</span></span>

[<span data-ttu-id="73740-130">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="73740-130">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)

<span data-ttu-id="73740-131">[](glisenabled.md)具有引數 GL \_ 多邊形 \_ STIPPLE 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="73740-131">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="73740-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="73740-132">Requirements</span></span>



| <span data-ttu-id="73740-133">需求</span><span class="sxs-lookup"><span data-stu-id="73740-133">Requirement</span></span> | <span data-ttu-id="73740-134">值</span><span class="sxs-lookup"><span data-stu-id="73740-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73740-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73740-135">Minimum supported client</span></span><br/> | <span data-ttu-id="73740-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73740-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="73740-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73740-137">Minimum supported server</span></span><br/> | <span data-ttu-id="73740-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73740-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73740-139">標頭</span><span class="sxs-lookup"><span data-stu-id="73740-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="73740-140"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="73740-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="73740-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="73740-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="73740-142"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="73740-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="73740-143">DLL</span><span class="sxs-lookup"><span data-stu-id="73740-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73740-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73740-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73740-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73740-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73740-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="73740-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="73740-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="73740-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="73740-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="73740-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="73740-149">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="73740-149">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="73740-150">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="73740-150">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="73740-151">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="73740-151">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> </dl>

 

 





