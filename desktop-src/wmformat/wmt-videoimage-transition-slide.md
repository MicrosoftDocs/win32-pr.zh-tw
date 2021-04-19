---
title: 'WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl) '
description: 投影片轉換會將舊影像從框架滑出，以顯示新的影像。
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992907"
---
# <a name="wmt_videoimage_transition_slide"></a><span data-ttu-id="851b4-104">WMT \_ VIDEOIMAGE \_ 轉換投影 \_ 片</span><span class="sxs-lookup"><span data-stu-id="851b4-104">WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE</span></span>

<span data-ttu-id="851b4-105">投影片轉換會將舊影像從框架滑出，以顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="851b4-105">The slide transition reveals the new image by sliding the old image out of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="851b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="851b4-106">Parameters</span></span>

<span data-ttu-id="851b4-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="851b4-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="851b4-108">參數</span><span class="sxs-lookup"><span data-stu-id="851b4-108">Parameter</span></span></th>
<th><span data-ttu-id="851b4-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="851b4-109">Structure member</span></span></th>
<th><span data-ttu-id="851b4-110">Description</span><span class="sxs-lookup"><span data-stu-id="851b4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="851b4-111">距離</span><span class="sxs-lookup"><span data-stu-id="851b4-111">Distance</span></span></td>
<td><span data-ttu-id="851b4-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="851b4-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="851b4-113">舊影像滑出框架的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="851b4-113">Distance, in pixels, that the old image slides out of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="851b4-114">方向</span><span class="sxs-lookup"><span data-stu-id="851b4-114">Direction</span></span></td>
<td><span data-ttu-id="851b4-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="851b4-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="851b4-116">舊影像滑出的方向。設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="851b4-116">Direction in which the old image slides.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="851b4-117">0-滑到右邊。</span><span class="sxs-lookup"><span data-stu-id="851b4-117">0 - Slide to the right.</span></span></li>
<li><span data-ttu-id="851b4-118">1-滑至左方。</span><span class="sxs-lookup"><span data-stu-id="851b4-118">1 - Slide to the left.</span></span></li>
<li><span data-ttu-id="851b4-119">2-向上滑。</span><span class="sxs-lookup"><span data-stu-id="851b4-119">2 - Slide upward.</span></span></li>
<li><span data-ttu-id="851b4-120">3-向下滑動。</span><span class="sxs-lookup"><span data-stu-id="851b4-120">3 - Slide downward.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="851b4-121">Composition</span><span class="sxs-lookup"><span data-stu-id="851b4-121">Composition</span></span></td>
<td><span data-ttu-id="851b4-122"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="851b4-122"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="851b4-123">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="851b4-123">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="851b4-124">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="851b4-124">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="851b4-125">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="851b4-125">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="851b4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="851b4-126">Requirements</span></span>



| <span data-ttu-id="851b4-127">需求</span><span class="sxs-lookup"><span data-stu-id="851b4-127">Requirement</span></span> | <span data-ttu-id="851b4-128">值</span><span class="sxs-lookup"><span data-stu-id="851b4-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="851b4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="851b4-129">Header</span></span><br/> | <dl> <span data-ttu-id="851b4-130"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="851b4-130"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="851b4-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="851b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="851b4-132">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="851b4-132">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





