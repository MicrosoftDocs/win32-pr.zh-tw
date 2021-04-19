---
title: 'ID2D1RenderTarget PushAxisAlignedClip 方法 (D2d1 \_ 1 .h) '
description: 指定裁剪所有後續繪圖作業的矩形。
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- PushAxisAlignedClip 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996509"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a><span data-ttu-id="ee790-104">ID2D1RenderTarget：:P ushAxisAlignedClip 方法</span><span class="sxs-lookup"><span data-stu-id="ee790-104">ID2D1RenderTarget::PushAxisAlignedClip methods</span></span>

<span data-ttu-id="ee790-105">指定裁剪所有後續繪圖作業的矩形。</span><span class="sxs-lookup"><span data-stu-id="ee790-105">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ee790-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="ee790-106">Overload list</span></span>



| <span data-ttu-id="ee790-107">方法</span><span class="sxs-lookup"><span data-stu-id="ee790-107">Method</span></span>                                                                                                                                         | <span data-ttu-id="ee790-108">描述</span><span class="sxs-lookup"><span data-stu-id="ee790-108">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee790-109">[**PushAxisAlignedClip (D2D1 \_ RECT \_ F&、D2D1 \_ 消除鋸齒 \_ 模式)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="ee790-109">[**PushAxisAlignedClip(D2D1\_RECT\_F&,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span>  | <span data-ttu-id="ee790-110">指定裁剪所有後續繪圖作業的矩形。</span><span class="sxs-lookup"><span data-stu-id="ee790-110">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |
| <span data-ttu-id="ee790-111">[**PushAxisAlignedClip (D2D1 \_ RECT \_ F \* 、D2D1 \_ 消除鋸齒 \_ 模式)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="ee790-111">[**PushAxisAlignedClip(D2D1\_RECT\_F\*,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span> | <span data-ttu-id="ee790-112">指定裁剪所有後續繪圖作業的矩形。</span><span class="sxs-lookup"><span data-stu-id="ee790-112">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ee790-113">備註</span><span class="sxs-lookup"><span data-stu-id="ee790-113">Remarks</span></span>

<span data-ttu-id="ee790-114">[**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))和 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip)組可以在 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)中進行，但不能重迭。</span><span class="sxs-lookup"><span data-stu-id="ee790-114">A [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pair can occur around or within a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), but cannot overlap.</span></span> <span data-ttu-id="ee790-115">例如， **PushAxisAlignedClip**、 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))、 **PopLayer**、 **PopAxisAlignedClip** 的序列是有效的，但 **PushAxisAlignedClip**、 **PushLayer**、 **PopAxisAlignedClip**、 **PopLayer** 的序列無效。</span><span class="sxs-lookup"><span data-stu-id="ee790-115">For example, the sequence of **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** is valid, but the sequence of **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** is invalid.</span></span>

<span data-ttu-id="ee790-116">如果失敗，這個方法不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee790-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="ee790-117">若要判斷繪圖作業 (如 **PushAxisAlignedClip**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="ee790-117">To determine whether a drawing operation (such as **PushAxisAlignedClip**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="ee790-118">範例</span><span class="sxs-lookup"><span data-stu-id="ee790-118">Examples</span></span>

<span data-ttu-id="ee790-119">如需範例，請參閱 [如何使用 Axis-Aligned 剪切矩形的剪輯](how-to-clip-with-axis-aligned-rects.md)。</span><span class="sxs-lookup"><span data-stu-id="ee790-119">For an example, see the [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee790-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee790-120">Requirements</span></span>



| <span data-ttu-id="ee790-121">需求</span><span class="sxs-lookup"><span data-stu-id="ee790-121">Requirement</span></span> | <span data-ttu-id="ee790-122">值</span><span class="sxs-lookup"><span data-stu-id="ee790-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee790-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ee790-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ee790-124"><dt>D2d1 \_ 1. h (包括 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="ee790-124"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="ee790-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee790-125">Library</span></span><br/> | <dl> <span data-ttu-id="ee790-126"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee790-126"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ee790-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ee790-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="ee790-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee790-128"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="ee790-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee790-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee790-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="ee790-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="ee790-131">�</span><span class="sxs-lookup"><span data-stu-id="ee790-131">�</span></span>

<span data-ttu-id="ee790-132">�</span><span class="sxs-lookup"><span data-stu-id="ee790-132">�</span></span>
