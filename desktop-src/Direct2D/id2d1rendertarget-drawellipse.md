---
title: 'ID2D1RenderTarget DrawEllipse 方法 (D2d1 .h) '
description: 繪製具有指定維度和筆劃的橢圓形大綱。
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- DrawEllipse 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994626"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a><span data-ttu-id="f379d-104">ID2D1RenderTarget：:D rawEllipse 方法</span><span class="sxs-lookup"><span data-stu-id="f379d-104">ID2D1RenderTarget::DrawEllipse methods</span></span>

<span data-ttu-id="f379d-105">繪製具有指定維度和筆劃的橢圓形大綱。</span><span class="sxs-lookup"><span data-stu-id="f379d-105">Draws the outline of an ellipse with the specified dimensions and stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f379d-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="f379d-106">Overload list</span></span>



| <span data-ttu-id="f379d-107">方法</span><span class="sxs-lookup"><span data-stu-id="f379d-107">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="f379d-108">描述</span><span class="sxs-lookup"><span data-stu-id="f379d-108">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f379d-109">[**DrawEllipse (D2D1 \_ 橢圓形&、ID2D1Brush \* 、FLOAT、ID2D1StrokeStyle \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="f379d-109">[**DrawEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="f379d-110">使用指定的筆觸樣式繪製指定之橢圓形的輪廓。</span><span class="sxs-lookup"><span data-stu-id="f379d-110">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |
| <span data-ttu-id="f379d-111">[**DrawEllipse (D2D1 \_ 橢圓形 \* 、ID2D1Brush \* 、FLOAT、ID2D1StrokeStyle \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="f379d-111">[**DrawEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="f379d-112">使用指定的筆觸樣式繪製指定之橢圓形的輪廓。</span><span class="sxs-lookup"><span data-stu-id="f379d-112">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="f379d-113">備註</span><span class="sxs-lookup"><span data-stu-id="f379d-113">Remarks</span></span>

<span data-ttu-id="f379d-114">**DrawEllipse** 方法不會在失敗時傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f379d-114">The **DrawEllipse** method doesn't return an error code if it fails.</span></span> <span data-ttu-id="f379d-115">若要判斷繪圖作業 (如 **DrawEllipse**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="f379d-115">To determine whether a drawing operation (such as **DrawEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="f379d-116">範例</span><span class="sxs-lookup"><span data-stu-id="f379d-116">Examples</span></span>

<span data-ttu-id="f379d-117">如需範例，請參閱 [如何繪製和填滿基本圖形](how-to-draw-an-ellipse.md)。</span><span class="sxs-lookup"><span data-stu-id="f379d-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f379d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f379d-118">Requirements</span></span>



| <span data-ttu-id="f379d-119">需求</span><span class="sxs-lookup"><span data-stu-id="f379d-119">Requirement</span></span> | <span data-ttu-id="f379d-120">值</span><span class="sxs-lookup"><span data-stu-id="f379d-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f379d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f379d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f379d-122"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="f379d-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="f379d-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f379d-123">Library</span></span><br/> | <dl> <span data-ttu-id="f379d-124"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f379d-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="f379d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f379d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f379d-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f379d-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f379d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f379d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f379d-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="f379d-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

<span data-ttu-id="f379d-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="f379d-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span></span>
</dt> </dl>

<span data-ttu-id="f379d-130">�</span><span class="sxs-lookup"><span data-stu-id="f379d-130">�</span></span>

<span data-ttu-id="f379d-131">�</span><span class="sxs-lookup"><span data-stu-id="f379d-131">�</span></span>
