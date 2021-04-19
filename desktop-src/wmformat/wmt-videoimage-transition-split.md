---
title: 'WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl) '
description: 分割轉換會藉由分割舊影像來顯示新的影像。 分割會沿著框架內的水準水準或垂直線出現。
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981353"
---
# <a name="wmt_videoimage_transition_split"></a><span data-ttu-id="e60f5-105">WMT \_ VIDEOIMAGE \_ 轉換 \_ 分割</span><span class="sxs-lookup"><span data-stu-id="e60f5-105">WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT</span></span>

<span data-ttu-id="e60f5-106">分割轉換會藉由分割舊影像來顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="e60f5-106">The split transition reveals the new image by splitting the old image.</span></span> <span data-ttu-id="e60f5-107">分割會沿著框架內的水準水準或垂直線出現。</span><span class="sxs-lookup"><span data-stu-id="e60f5-107">The split appears along a straight horizontal or vertical line starting inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="e60f5-108">參數</span><span class="sxs-lookup"><span data-stu-id="e60f5-108">Parameters</span></span>

<span data-ttu-id="e60f5-109">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="e60f5-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e60f5-110">參數</span><span class="sxs-lookup"><span data-stu-id="e60f5-110">Parameter</span></span></th>
<th><span data-ttu-id="e60f5-111">結構成員</span><span class="sxs-lookup"><span data-stu-id="e60f5-111">Structure member</span></span></th>
<th><span data-ttu-id="e60f5-112">Description</span><span class="sxs-lookup"><span data-stu-id="e60f5-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e60f5-113">中心 X</span><span class="sxs-lookup"><span data-stu-id="e60f5-113">Center X</span></span></td>
<td><span data-ttu-id="e60f5-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="e60f5-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="e60f5-115">分割之原始線的相對於影片框架的 X 座標。</span><span class="sxs-lookup"><span data-stu-id="e60f5-115">X-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e60f5-116">中心 Y</span><span class="sxs-lookup"><span data-stu-id="e60f5-116">Center Y</span></span></td>
<td><span data-ttu-id="e60f5-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="e60f5-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="e60f5-118">相對於影片框架的 Y 座標（相對於影片框架）。</span><span class="sxs-lookup"><span data-stu-id="e60f5-118">Y-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e60f5-119">距離</span><span class="sxs-lookup"><span data-stu-id="e60f5-119">Distance</span></span></td>
<td><span data-ttu-id="e60f5-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="e60f5-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="e60f5-121">分割的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e60f5-121">Width of the split in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e60f5-122">方向</span><span class="sxs-lookup"><span data-stu-id="e60f5-122">Direction</span></span></td>
<td><span data-ttu-id="e60f5-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="e60f5-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="e60f5-124">分割的方向。設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e60f5-124">Orientation of the split.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="e60f5-125">0-沿著水平線分割。</span><span class="sxs-lookup"><span data-stu-id="e60f5-125">0 - Splits along a horizontal line.</span></span></li>
<li><span data-ttu-id="e60f5-126">1-沿著垂直線分割。</span><span class="sxs-lookup"><span data-stu-id="e60f5-126">1 - Splits along a vertical line.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e60f5-127">Composition</span><span class="sxs-lookup"><span data-stu-id="e60f5-127">Composition</span></span></td>
<td><span data-ttu-id="e60f5-128"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="e60f5-128"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="e60f5-129">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e60f5-129">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="e60f5-130">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="e60f5-130">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="e60f5-131">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="e60f5-131">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="e60f5-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e60f5-132">Requirements</span></span>



| <span data-ttu-id="e60f5-133">需求</span><span class="sxs-lookup"><span data-stu-id="e60f5-133">Requirement</span></span> | <span data-ttu-id="e60f5-134">值</span><span class="sxs-lookup"><span data-stu-id="e60f5-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e60f5-135">標頭</span><span class="sxs-lookup"><span data-stu-id="e60f5-135">Header</span></span><br/> | <dl> <span data-ttu-id="e60f5-136"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e60f5-136"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e60f5-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e60f5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60f5-138">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="e60f5-138">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





