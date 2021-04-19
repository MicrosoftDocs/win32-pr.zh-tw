---
title: 'WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl) '
description: 星形轉換會以框架內的五個指向星形顯示新影像。
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989588"
---
# <a name="wmt_videoimage_transition_star"></a><span data-ttu-id="53ceb-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 星星</span><span class="sxs-lookup"><span data-stu-id="53ceb-104">WMT\_VIDEOIMAGE\_TRANSITION\_STAR</span></span>

<span data-ttu-id="53ceb-105">星形轉換會以框架內的五個指向星形顯示新影像。</span><span class="sxs-lookup"><span data-stu-id="53ceb-105">The star transition reveals the new image in a five-pointed star inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="53ceb-106">參數</span><span class="sxs-lookup"><span data-stu-id="53ceb-106">Parameters</span></span>

<span data-ttu-id="53ceb-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="53ceb-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53ceb-108">參數</span><span class="sxs-lookup"><span data-stu-id="53ceb-108">Parameter</span></span></th>
<th><span data-ttu-id="53ceb-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="53ceb-109">Structure member</span></span></th>
<th><span data-ttu-id="53ceb-110">Description</span><span class="sxs-lookup"><span data-stu-id="53ceb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53ceb-111">中心 X</span><span class="sxs-lookup"><span data-stu-id="53ceb-111">Center X</span></span></td>
<td><span data-ttu-id="53ceb-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="53ceb-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="53ceb-113">星形中間的 X 座標（相對於影片框架）。</span><span class="sxs-lookup"><span data-stu-id="53ceb-113">X-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53ceb-114">中心 Y</span><span class="sxs-lookup"><span data-stu-id="53ceb-114">Center Y</span></span></td>
<td><span data-ttu-id="53ceb-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="53ceb-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="53ceb-116">星形中央的 Y 座標（相對於影片框架）。</span><span class="sxs-lookup"><span data-stu-id="53ceb-116">Y-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53ceb-117">半徑</span><span class="sxs-lookup"><span data-stu-id="53ceb-117">Radius</span></span></td>
<td><span data-ttu-id="53ceb-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="53ceb-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="53ceb-119">星形點所定義之圓形的半徑（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="53ceb-119">Radius, in pixels, of the circle defined by the points of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53ceb-120">Composition</span><span class="sxs-lookup"><span data-stu-id="53ceb-120">Composition</span></span></td>
<td><span data-ttu-id="53ceb-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="53ceb-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="53ceb-122">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="53ceb-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="53ceb-123">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="53ceb-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="53ceb-124">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景。</span><span class="sxs-lookup"><span data-stu-id="53ceb-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="53ceb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="53ceb-125">Requirements</span></span>



| <span data-ttu-id="53ceb-126">需求</span><span class="sxs-lookup"><span data-stu-id="53ceb-126">Requirement</span></span> | <span data-ttu-id="53ceb-127">值</span><span class="sxs-lookup"><span data-stu-id="53ceb-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53ceb-128">標頭</span><span class="sxs-lookup"><span data-stu-id="53ceb-128">Header</span></span><br/> | <dl> <span data-ttu-id="53ceb-129"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="53ceb-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53ceb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53ceb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ceb-131">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="53ceb-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





