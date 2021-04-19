---
title: 'WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl) '
description: 鳶尾花轉換會沿著 X 軸和 y 軸顯示新的影像。 此轉換的視覺效果是新的影像會出現在擴展交叉到達框架的所有側邊。
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983100"
---
# <a name="wmt_videoimage_transition_iris"></a><span data-ttu-id="8d864-105">WMT \_ VIDEOIMAGE \_ 轉換 \_ 鳶尾花</span><span class="sxs-lookup"><span data-stu-id="8d864-105">WMT\_VIDEOIMAGE\_TRANSITION\_IRIS</span></span>

<span data-ttu-id="8d864-106">鳶尾花轉換會沿著 X 軸和 y 軸顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="8d864-106">The iris transition reveals the new image along an x-axis and a y-axis.</span></span> <span data-ttu-id="8d864-107">此轉換的視覺效果是新的影像會出現在擴展交叉到達框架的所有側邊。</span><span class="sxs-lookup"><span data-stu-id="8d864-107">The visual effect of this transition is that the new image appears in a widening cross reaching to all sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d864-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d864-108">Parameters</span></span>

<span data-ttu-id="8d864-109">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="8d864-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d864-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d864-110">Parameter</span></span></th>
<th><span data-ttu-id="8d864-111">結構成員</span><span class="sxs-lookup"><span data-stu-id="8d864-111">Structure member</span></span></th>
<th><span data-ttu-id="8d864-112">Description</span><span class="sxs-lookup"><span data-stu-id="8d864-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d864-113">中心 X</span><span class="sxs-lookup"><span data-stu-id="8d864-113">Center X</span></span></td>
<td><span data-ttu-id="8d864-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="8d864-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="8d864-115">相對於影片框架的 X 座標，鳶尾花效果的中心。</span><span class="sxs-lookup"><span data-stu-id="8d864-115">X-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d864-116">中心 Y</span><span class="sxs-lookup"><span data-stu-id="8d864-116">Center Y</span></span></td>
<td><span data-ttu-id="8d864-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="8d864-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="8d864-118">相對於影片框架的 Y 座標，鳶尾花效果的中心。</span><span class="sxs-lookup"><span data-stu-id="8d864-118">Y-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d864-119">寬度</span><span class="sxs-lookup"><span data-stu-id="8d864-119">Width</span></span></td>
<td><span data-ttu-id="8d864-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="8d864-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="8d864-121">垂直線的寬度，以圖元為單位顯示新影像。</span><span class="sxs-lookup"><span data-stu-id="8d864-121">Width of the vertical line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d864-122">高度</span><span class="sxs-lookup"><span data-stu-id="8d864-122">Height</span></span></td>
<td><span data-ttu-id="8d864-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="8d864-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="8d864-124">水平線的高度會顯示新影像（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8d864-124">Height of the horizontal line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d864-125">Composition</span><span class="sxs-lookup"><span data-stu-id="8d864-125">Composition</span></span></td>
<td><span data-ttu-id="8d864-126"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="8d864-126"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="8d864-127">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="8d864-127">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="8d864-128">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="8d864-128">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="8d864-129">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="8d864-129">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="8d864-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d864-130">Requirements</span></span>



| <span data-ttu-id="8d864-131">需求</span><span class="sxs-lookup"><span data-stu-id="8d864-131">Requirement</span></span> | <span data-ttu-id="8d864-132">值</span><span class="sxs-lookup"><span data-stu-id="8d864-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d864-133">標頭</span><span class="sxs-lookup"><span data-stu-id="8d864-133">Header</span></span><br/> | <dl> <span data-ttu-id="8d864-134"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d864-134"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d864-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d864-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d864-136">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="8d864-136">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





