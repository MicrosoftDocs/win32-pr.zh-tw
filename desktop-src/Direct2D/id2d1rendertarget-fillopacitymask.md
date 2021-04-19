---
title: ID2D1RenderTarget FillOpacityMask 方法
description: 將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- FillOpacityMask 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989700"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a><span data-ttu-id="3de21-104">ID2D1RenderTarget：： FillOpacityMask 方法</span><span class="sxs-lookup"><span data-stu-id="3de21-104">ID2D1RenderTarget::FillOpacityMask methods</span></span>

<span data-ttu-id="3de21-105">將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。</span><span class="sxs-lookup"><span data-stu-id="3de21-105">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3de21-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="3de21-106">Overload list</span></span>



| <span data-ttu-id="3de21-107">方法</span><span class="sxs-lookup"><span data-stu-id="3de21-107">Method</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="3de21-108">描述</span><span class="sxs-lookup"><span data-stu-id="3de21-108">Description</span></span>                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de21-109">[**FillOpacityMask (ID2D1Bitmap \* 、ID2D1Brush \* 、D2D1 \_ 不透明度 \_ 遮罩 \_ 內容、D2D \_ rect \_ f&、D2D \_ rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="3de21-109">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F&,D2D\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span></span>       | <span data-ttu-id="3de21-110">將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。</span><span class="sxs-lookup"><span data-stu-id="3de21-110">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |
| <span data-ttu-id="3de21-111">[**FillOpacityMask (ID2D1Bitmap \* 、ID2D1Brush \* 、D2D1 \_ 不透明度 \_ 遮罩 \_ 內容、 \_ D2D rect \_ f \* 、D2D \_ rect \_ f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="3de21-111">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F\*,D2D\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span></span> | <span data-ttu-id="3de21-112">將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。</span><span class="sxs-lookup"><span data-stu-id="3de21-112">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="3de21-113">備註</span><span class="sxs-lookup"><span data-stu-id="3de21-113">Remarks</span></span>

<span data-ttu-id="3de21-114">為了讓這個方法正常運作，轉譯目標必須使用 [**D2D1 的消除鋸齒 \_ \_ 模式 \_ 別名**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) 消除鋸齒模式。</span><span class="sxs-lookup"><span data-stu-id="3de21-114">For this method to work properly, the render target must be using the [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialiasing mode.</span></span> <span data-ttu-id="3de21-115">您可以藉由呼叫 [**ID2D1RenderTarget：： SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) 方法來設定消除鋸齒模式。</span><span class="sxs-lookup"><span data-stu-id="3de21-115">You can set the antialiasing mode by calling the [**ID2D1RenderTarget::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) method.</span></span>

<span data-ttu-id="3de21-116">如果失敗，這個方法不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3de21-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="3de21-117">若要判斷繪圖作業 (如 **FillOpacityMask**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="3de21-117">To determine whether a drawing operation (such as **FillOpacityMask**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de21-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de21-118">Requirements</span></span>



| <span data-ttu-id="3de21-119">需求</span><span class="sxs-lookup"><span data-stu-id="3de21-119">Requirement</span></span> | <span data-ttu-id="3de21-120">值</span><span class="sxs-lookup"><span data-stu-id="3de21-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3de21-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="3de21-121">Library</span></span><br/> | <dl> <span data-ttu-id="3de21-122"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3de21-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="3de21-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3de21-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="3de21-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3de21-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de21-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de21-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de21-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="3de21-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

