---
title: 'WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl) '
description: 矩形轉換會顯示框架內矩形內的新影像。
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978448"
---
# <a name="wmt_videoimage_transition_rectangle"></a><span data-ttu-id="49631-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 矩形</span><span class="sxs-lookup"><span data-stu-id="49631-104">WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE</span></span>

<span data-ttu-id="49631-105">矩形轉換會顯示框架內矩形內的新影像。</span><span class="sxs-lookup"><span data-stu-id="49631-105">The rectangle transition reveals the new image in a rectangle within the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="49631-106">參數</span><span class="sxs-lookup"><span data-stu-id="49631-106">Parameters</span></span>

<span data-ttu-id="49631-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="49631-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49631-108">參數</span><span class="sxs-lookup"><span data-stu-id="49631-108">Parameter</span></span></th>
<th><span data-ttu-id="49631-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="49631-109">Structure member</span></span></th>
<th><span data-ttu-id="49631-110">Description</span><span class="sxs-lookup"><span data-stu-id="49631-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49631-111">中心 X</span><span class="sxs-lookup"><span data-stu-id="49631-111">Center X</span></span></td>
<td><span data-ttu-id="49631-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="49631-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="49631-113">矩形中央的相對於影片框架的 X 座標。</span><span class="sxs-lookup"><span data-stu-id="49631-113">X-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49631-114">中心 Y</span><span class="sxs-lookup"><span data-stu-id="49631-114">Center Y</span></span></td>
<td><span data-ttu-id="49631-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="49631-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="49631-116">矩形中央的 Y 座標（相對於影片框架）。</span><span class="sxs-lookup"><span data-stu-id="49631-116">Y-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49631-117">寬度</span><span class="sxs-lookup"><span data-stu-id="49631-117">Width</span></span></td>
<td><span data-ttu-id="49631-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="49631-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="49631-119">矩形的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="49631-119">Width of the rectangle in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49631-120">高度</span><span class="sxs-lookup"><span data-stu-id="49631-120">Height</span></span></td>
<td><span data-ttu-id="49631-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="49631-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="49631-122">矩形的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="49631-122">Height of the rectangle in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49631-123">Composition</span><span class="sxs-lookup"><span data-stu-id="49631-123">Composition</span></span></td>
<td><span data-ttu-id="49631-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="49631-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="49631-125">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="49631-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="49631-126">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="49631-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="49631-127">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="49631-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="49631-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="49631-128">Requirements</span></span>



| <span data-ttu-id="49631-129">需求</span><span class="sxs-lookup"><span data-stu-id="49631-129">Requirement</span></span> | <span data-ttu-id="49631-130">值</span><span class="sxs-lookup"><span data-stu-id="49631-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49631-131">標頭</span><span class="sxs-lookup"><span data-stu-id="49631-131">Header</span></span><br/> | <dl> <span data-ttu-id="49631-132"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="49631-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49631-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49631-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49631-134">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="49631-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





