---
title: 'WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl) '
description: 已填滿的 V 轉換會顯示來自框架某一端的三角形中的新影像。
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982919"
---
# <a name="wmt_videoimage_transition_filled_v"></a><span data-ttu-id="ee06b-104">WMT \_ VIDEOIMAGE \_ 轉換已 \_ 填滿 \_ V</span><span class="sxs-lookup"><span data-stu-id="ee06b-104">WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V</span></span>

<span data-ttu-id="ee06b-105">已填滿的 V 轉換會顯示來自框架某一端的三角形中的新影像。</span><span class="sxs-lookup"><span data-stu-id="ee06b-105">The filled V transition reveals the new image in a triangle originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee06b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee06b-106">Parameters</span></span>

<span data-ttu-id="ee06b-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="ee06b-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee06b-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee06b-108">Parameter</span></span></th>
<th><span data-ttu-id="ee06b-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="ee06b-109">Structure member</span></span></th>
<th><span data-ttu-id="ee06b-110">Description</span><span class="sxs-lookup"><span data-stu-id="ee06b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee06b-111">寬度</span><span class="sxs-lookup"><span data-stu-id="ee06b-111">Width</span></span></td>
<td><span data-ttu-id="ee06b-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="ee06b-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="ee06b-113">填滿 V 的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee06b-113">Width of the filled V in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee06b-114">高度</span><span class="sxs-lookup"><span data-stu-id="ee06b-114">Height</span></span></td>
<td><span data-ttu-id="ee06b-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="ee06b-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="ee06b-116">填滿 V 的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee06b-116">Height of the filled V in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee06b-117">方向</span><span class="sxs-lookup"><span data-stu-id="ee06b-117">Direction</span></span></td>
<td><span data-ttu-id="ee06b-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="ee06b-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="ee06b-119">填滿 V 來源的方向。設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="ee06b-119">Direction from which the filled V originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="ee06b-120">0-從框架左邊進入。</span><span class="sxs-lookup"><span data-stu-id="ee06b-120">0 - Enters from the left side of the frame.</span></span></li>
<li><span data-ttu-id="ee06b-121">1-從框架的右邊進入。</span><span class="sxs-lookup"><span data-stu-id="ee06b-121">1 - Enters from the right side of the frame.</span></span></li>
<li><span data-ttu-id="ee06b-122">2-從框架底部進入。</span><span class="sxs-lookup"><span data-stu-id="ee06b-122">2 - Enters from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="ee06b-123">3-從框架頂端進入。</span><span class="sxs-lookup"><span data-stu-id="ee06b-123">3 - Enters from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee06b-124">Composition</span><span class="sxs-lookup"><span data-stu-id="ee06b-124">Composition</span></span></td>
<td><span data-ttu-id="ee06b-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="ee06b-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="ee06b-126">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="ee06b-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="ee06b-127">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="ee06b-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="ee06b-128">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="ee06b-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="ee06b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee06b-129">Requirements</span></span>



| <span data-ttu-id="ee06b-130">需求</span><span class="sxs-lookup"><span data-stu-id="ee06b-130">Requirement</span></span> | <span data-ttu-id="ee06b-131">值</span><span class="sxs-lookup"><span data-stu-id="ee06b-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee06b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ee06b-132">Header</span></span><br/> | <dl> <span data-ttu-id="ee06b-133"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee06b-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee06b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee06b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee06b-135">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="ee06b-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





