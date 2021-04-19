---
title: ID2D1RenderTarget DrawBitmap 方法
description: 繪製指定的 ID2D1Bitmap。
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- DrawBitmap 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989530"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a><span data-ttu-id="7d716-104">ID2D1RenderTarget：:D rawBitmap 方法</span><span class="sxs-lookup"><span data-stu-id="7d716-104">ID2D1RenderTarget::DrawBitmap methods</span></span>

<span data-ttu-id="7d716-105">繪製指定的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)。</span><span class="sxs-lookup"><span data-stu-id="7d716-105">Draws the specified [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

### <a name="overload-list"></a><span data-ttu-id="7d716-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="7d716-106">Overload list</span></span>



| <span data-ttu-id="7d716-107">方法</span><span class="sxs-lookup"><span data-stu-id="7d716-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="7d716-108">描述</span><span class="sxs-lookup"><span data-stu-id="7d716-108">Description</span></span>                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d716-109">[**DrawBitmap (ID2D1Bitmap \* 、D2D1 \_ RECT \_ F&、FLOAT、D2D1 \_ 點陣圖 \_ 插補 \_ 模式、D2D1 \_ RECT \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="7d716-109">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F&,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))</span></span>   | <span data-ttu-id="7d716-110">將指定的點陣圖調整為指定矩形的大小之後，繪製該點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7d716-110">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="7d716-111">[**DrawBitmap (ID2D1Bitmap \* 、D2D1 \_ RECT \_ F&、FLOAT、D2D1 \_ 點陣圖 \_ 插補 \_ 模式、D2D1 \_ RECT \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="7d716-111">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F&,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span></span>  | <span data-ttu-id="7d716-112">將指定的點陣圖調整為指定矩形的大小之後，繪製該點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7d716-112">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="7d716-113">[**DrawBitmap (ID2D1Bitmap \* 、D2D1 \_ RECT \_ F \* 、FLOAT、D2D1 \_ 點陣圖 \_ 插補 \_ 模式、D2D1 \_ RECT \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="7d716-113">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F\*,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span></span> | <span data-ttu-id="7d716-114">將指定的點陣圖調整為指定矩形的大小之後，繪製該點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7d716-114">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="7d716-115">備註</span><span class="sxs-lookup"><span data-stu-id="7d716-115">Remarks</span></span>

<span data-ttu-id="7d716-116">如果失敗，這個方法不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7d716-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="7d716-117">若要判斷繪圖作業 (如 **DrawBitmap**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="7d716-117">To determine whether a drawing operation (such as **DrawBitmap**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="7d716-118">範例</span><span class="sxs-lookup"><span data-stu-id="7d716-118">Examples</span></span>

<span data-ttu-id="7d716-119">如需範例，請參閱 [如何繪製點陣圖](how-to-draw-a-bitmap.md)。</span><span class="sxs-lookup"><span data-stu-id="7d716-119">For an example, see [How to Draw a Bitmap](how-to-draw-a-bitmap.md).</span></span> <span data-ttu-id="7d716-120">如需示範如何從資源或檔案載入點陣圖的範例，請參閱如何從 [資源載入](how-to-load-a-bitmap-from-a-resource.md) 點陣圖，以及 [如何從](how-to-load-a-direct2d-bitmap-from-a-file.md)檔案載入點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7d716-120">For an example showing how to load a bitmap from a resource or a file, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md) and [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d716-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d716-121">Requirements</span></span>



| <span data-ttu-id="7d716-122">需求</span><span class="sxs-lookup"><span data-stu-id="7d716-122">Requirement</span></span> | <span data-ttu-id="7d716-123">值</span><span class="sxs-lookup"><span data-stu-id="7d716-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7d716-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d716-124">Library</span></span><br/> | <dl> <span data-ttu-id="7d716-125"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d716-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d716-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7d716-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d716-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d716-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d716-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d716-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d716-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="7d716-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="7d716-130">如何繪製點陣圖</span><span class="sxs-lookup"><span data-stu-id="7d716-130">How to Draw a Bitmap</span></span>](how-to-draw-a-bitmap.md)
</dt> <dt>

[<span data-ttu-id="7d716-131">如何從資源載入點陣圖</span><span class="sxs-lookup"><span data-stu-id="7d716-131">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[<span data-ttu-id="7d716-132">如何從檔案載入點陣圖</span><span class="sxs-lookup"><span data-stu-id="7d716-132">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

