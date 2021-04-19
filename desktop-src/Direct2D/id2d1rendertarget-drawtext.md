---
title: ID2D1RenderTarget DrawText 方法
description: 使用 IDWriteTextFormat 物件所提供的格式資訊，繪製指定的文字。
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- DrawText 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978639"
---
# <a name="id2d1rendertargetdrawtext-methods"></a><span data-ttu-id="649c2-104">ID2D1RenderTarget：:D rawText 方法</span><span class="sxs-lookup"><span data-stu-id="649c2-104">ID2D1RenderTarget::DrawText methods</span></span>

<span data-ttu-id="649c2-105">使用 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 物件所提供的格式資訊，繪製指定的文字。</span><span class="sxs-lookup"><span data-stu-id="649c2-105">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="649c2-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="649c2-106">Overload list</span></span>



| <span data-ttu-id="649c2-107">方法</span><span class="sxs-lookup"><span data-stu-id="649c2-107">Method</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="649c2-108">描述</span><span class="sxs-lookup"><span data-stu-id="649c2-108">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="649c2-109">[**DrawText (WCHAR \* 、IDWriteTextFormat \* 、D2D1 \_ RECT \_ F&、ID2D1Brush \* 、D2D1 \_ DRAW \_ text \_ 選項、DWRITE \_ 文字 \_ 測量 \_ 方法)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="649c2-109">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F&,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>  | <span data-ttu-id="649c2-110">使用 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 物件所提供的格式資訊，繪製指定的文字。</span><span class="sxs-lookup"><span data-stu-id="649c2-110">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span><br/>  |
| <span data-ttu-id="649c2-111">[**DrawText (WCHAR \* 、IDWriteTextFormat \* 、D2D1 \_ RECT \_ F \* 、ID2D1Brush \* 、D2D1 \_ DRAW \_ text \_ 選項、DWRITE \_ TEXT \_ 測量 \_ 方法)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="649c2-111">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F\*,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> | <span data-ttu-id="649c2-112">使用 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 物件所提供的格式資訊，繪製指定的文字。</span><span class="sxs-lookup"><span data-stu-id="649c2-112">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="649c2-113">備註</span><span class="sxs-lookup"><span data-stu-id="649c2-113">Remarks</span></span>

<span data-ttu-id="649c2-114">若要使用 Direct2D 來繪製文字，請針對具有單一格式的文字使用 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法，或者，如果您需要多種格式、先進的 OpenType 功能或點擊測試，請使用 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法。</span><span class="sxs-lookup"><span data-stu-id="649c2-114">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format, or the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method when you need multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="649c2-115">這些方法會使用 DirectWrite API 來提供高品質的文字顯示。</span><span class="sxs-lookup"><span data-stu-id="649c2-115">These methods use the DirectWrite API to provide high-quality text display.</span></span>

<span data-ttu-id="649c2-116">如果失敗，這個方法不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="649c2-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="649c2-117">若要判斷繪圖作業 (如 **DrawText**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="649c2-117">To determine whether a drawing operation (such as **DrawText**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="649c2-118">範例</span><span class="sxs-lookup"><span data-stu-id="649c2-118">Examples</span></span>

<span data-ttu-id="649c2-119">如需範例，請參閱 [如何繪製文字](how-to--draw-text.md)。</span><span class="sxs-lookup"><span data-stu-id="649c2-119">For an example, see [How to Draw Text](how-to--draw-text.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="649c2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="649c2-120">Requirements</span></span>



| <span data-ttu-id="649c2-121">需求</span><span class="sxs-lookup"><span data-stu-id="649c2-121">Requirement</span></span> | <span data-ttu-id="649c2-122">值</span><span class="sxs-lookup"><span data-stu-id="649c2-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="649c2-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="649c2-123">Library</span></span><br/> | <dl> <span data-ttu-id="649c2-124"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="649c2-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="649c2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="649c2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="649c2-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="649c2-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649c2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="649c2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649c2-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="649c2-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="649c2-129">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="649c2-129">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="649c2-130">如何繪製文字</span><span class="sxs-lookup"><span data-stu-id="649c2-130">How to Draw Text</span></span>](how-to--draw-text.md)
</dt> <dt>

[<span data-ttu-id="649c2-131">文字格式設定和版面配置總覽</span><span class="sxs-lookup"><span data-stu-id="649c2-131">Text Formatting and Layout Overview</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

