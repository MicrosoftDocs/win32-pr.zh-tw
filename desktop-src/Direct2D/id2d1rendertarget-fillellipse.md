---
title: 'ID2D1RenderTarget FillEllipse 方法 (D2d1 .h) '
description: 繪製指定橢圓形的內部。
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- FillEllipse 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999994"
---
# <a name="id2d1rendertargetfillellipse-methods"></a><span data-ttu-id="42720-104">ID2D1RenderTarget：： FillEllipse 方法</span><span class="sxs-lookup"><span data-stu-id="42720-104">ID2D1RenderTarget::FillEllipse methods</span></span>

<span data-ttu-id="42720-105">繪製指定橢圓形的內部。</span><span class="sxs-lookup"><span data-stu-id="42720-105">Paints the interior of the specified ellipse.</span></span>

### <a name="overload-list"></a><span data-ttu-id="42720-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="42720-106">Overload list</span></span>



| <span data-ttu-id="42720-107">方法</span><span class="sxs-lookup"><span data-stu-id="42720-107">Method</span></span>                                                                                                             | <span data-ttu-id="42720-108">描述</span><span class="sxs-lookup"><span data-stu-id="42720-108">Description</span></span>                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span data-ttu-id="42720-109">[**FillEllipse (D2D1 \_ 橢圓形&、ID2D1Brush \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="42720-109">[**FillEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span>  | <span data-ttu-id="42720-110">繪製指定橢圓形的內部。</span><span class="sxs-lookup"><span data-stu-id="42720-110">Paints the interior of the specified ellipse.</span></span> <br/> |
| <span data-ttu-id="42720-111">[**FillEllipse (D2D1 \_ 橢圓形 \* 、ID2D1Brush \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="42720-111">[**FillEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span> | <span data-ttu-id="42720-112">繪製指定橢圓形的內部。</span><span class="sxs-lookup"><span data-stu-id="42720-112">Paints the interior of the specified ellipse.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="42720-113">備註</span><span class="sxs-lookup"><span data-stu-id="42720-113">Remarks</span></span>

<span data-ttu-id="42720-114">如果失敗，這個方法不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="42720-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="42720-115">若要判斷繪圖作業 (如 **FillEllipse**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="42720-115">To determine whether a drawing operation (such as **FillEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="42720-116">範例</span><span class="sxs-lookup"><span data-stu-id="42720-116">Examples</span></span>

<span data-ttu-id="42720-117">如需範例，請參閱 [如何繪製和填滿基本圖形](how-to-draw-an-ellipse.md)。</span><span class="sxs-lookup"><span data-stu-id="42720-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42720-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="42720-118">Requirements</span></span>



| <span data-ttu-id="42720-119">需求</span><span class="sxs-lookup"><span data-stu-id="42720-119">Requirement</span></span> | <span data-ttu-id="42720-120">值</span><span class="sxs-lookup"><span data-stu-id="42720-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42720-121">標頭</span><span class="sxs-lookup"><span data-stu-id="42720-121">Header</span></span><br/>  | <dl> <span data-ttu-id="42720-122"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="42720-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="42720-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="42720-123">Library</span></span><br/> | <dl> <span data-ttu-id="42720-124"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42720-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="42720-125">DLL</span><span class="sxs-lookup"><span data-stu-id="42720-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="42720-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42720-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42720-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42720-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42720-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="42720-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="42720-129">如何繪製和填滿基本圖形</span><span class="sxs-lookup"><span data-stu-id="42720-129">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="42720-130">�</span><span class="sxs-lookup"><span data-stu-id="42720-130">�</span></span>

<span data-ttu-id="42720-131">�</span><span class="sxs-lookup"><span data-stu-id="42720-131">�</span></span>
