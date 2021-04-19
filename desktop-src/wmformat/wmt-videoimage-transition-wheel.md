---
title: 'WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl) '
description: 滾輪轉換會在一般的軸點周圍旋轉四行（例如滾輪的輪輻）來顯示新的影像。
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996116"
---
# <a name="wmt_videoimage_transition_wheel"></a><span data-ttu-id="7fc42-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 輪子</span><span class="sxs-lookup"><span data-stu-id="7fc42-104">WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL</span></span>

<span data-ttu-id="7fc42-105">滾輪轉換會在一般的軸點周圍旋轉四行（例如滾輪的輪輻）來顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="7fc42-105">The wheel transition reveals the new image by rotating four lines around a common pivot point, like the spokes of a wheel.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fc42-106">參數</span><span class="sxs-lookup"><span data-stu-id="7fc42-106">Parameters</span></span>

<span data-ttu-id="7fc42-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="7fc42-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7fc42-108">參數</span><span class="sxs-lookup"><span data-stu-id="7fc42-108">Parameter</span></span></th>
<th><span data-ttu-id="7fc42-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="7fc42-109">Structure member</span></span></th>
<th><span data-ttu-id="7fc42-110">Description</span><span class="sxs-lookup"><span data-stu-id="7fc42-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7fc42-111">中心 X</span><span class="sxs-lookup"><span data-stu-id="7fc42-111">Center X</span></span></td>
<td><span data-ttu-id="7fc42-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="7fc42-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="7fc42-113">滾輪效果中心相對於影片框架的 X 座標。</span><span class="sxs-lookup"><span data-stu-id="7fc42-113">X-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7fc42-114">中心 Y</span><span class="sxs-lookup"><span data-stu-id="7fc42-114">Center Y</span></span></td>
<td><span data-ttu-id="7fc42-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="7fc42-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="7fc42-116">滾輪效果中間的 Y 座標（相對於影片框架）。</span><span class="sxs-lookup"><span data-stu-id="7fc42-116">Y-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7fc42-117">角度</span><span class="sxs-lookup"><span data-stu-id="7fc42-117">Angle</span></span></td>
<td><span data-ttu-id="7fc42-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="7fc42-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="7fc42-119">滾輪效果輪輻的旋轉角度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fc42-119">Angle of rotation, in degrees, of the spokes of the wheel effect.</span></span> <span data-ttu-id="7fc42-120">值為0.0 表示舊影像，而不會顯示任何新的影像。</span><span class="sxs-lookup"><span data-stu-id="7fc42-120">A value of 0.0 indicates the old image without any of the new image revealed.</span></span> <span data-ttu-id="7fc42-121">值為90.0 表示已完全顯示新的影像。從0.0 到90.0 的移動會顯示為輪輻的順時針旋轉。</span><span class="sxs-lookup"><span data-stu-id="7fc42-121">A value of 90.0 indicates the new image fully revealed.Movement from 0.0 to 90.0 appears as clockwise rotation of the spokes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7fc42-122">Composition</span><span class="sxs-lookup"><span data-stu-id="7fc42-122">Composition</span></span></td>
<td><span data-ttu-id="7fc42-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="7fc42-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="7fc42-124">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="7fc42-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="7fc42-125">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="7fc42-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="7fc42-126">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="7fc42-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="7fc42-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fc42-127">Requirements</span></span>



| <span data-ttu-id="7fc42-128">需求</span><span class="sxs-lookup"><span data-stu-id="7fc42-128">Requirement</span></span> | <span data-ttu-id="7fc42-129">值</span><span class="sxs-lookup"><span data-stu-id="7fc42-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc42-130">標頭</span><span class="sxs-lookup"><span data-stu-id="7fc42-130">Header</span></span><br/> | <dl> <span data-ttu-id="7fc42-131"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc42-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc42-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fc42-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc42-133">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="7fc42-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





