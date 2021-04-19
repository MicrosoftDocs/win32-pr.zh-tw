---
title: 'WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl) '
description: 頁面變換轉換會以頁面翻轉效果轉換舊影像，並在下方顯示新的影像。
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990531"
---
# <a name="wmt_videoimage_transition_page_roll"></a><span data-ttu-id="1d41a-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 頁面 \_ 滾動</span><span class="sxs-lookup"><span data-stu-id="1d41a-104">WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL</span></span>

<span data-ttu-id="1d41a-105">頁面變換轉換會以頁面翻轉效果轉換舊影像，並在下方顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="1d41a-105">The page roll transition transforms the old image with a page-flipping effect, revealing the new image underneath.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d41a-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d41a-106">Parameters</span></span>

<span data-ttu-id="1d41a-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="1d41a-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d41a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1d41a-108">Parameter</span></span></th>
<th><span data-ttu-id="1d41a-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="1d41a-109">Structure member</span></span></th>
<th><span data-ttu-id="1d41a-110">Description</span><span class="sxs-lookup"><span data-stu-id="1d41a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d41a-111">半徑</span><span class="sxs-lookup"><span data-stu-id="1d41a-111">Radius</span></span></td>
<td><span data-ttu-id="1d41a-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="1d41a-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="1d41a-113">頁面滾動效果中的滾動半徑。</span><span class="sxs-lookup"><span data-stu-id="1d41a-113">Radius of the roll in the page roll effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d41a-114">距離</span><span class="sxs-lookup"><span data-stu-id="1d41a-114">Distance</span></span></td>
<td><span data-ttu-id="1d41a-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="1d41a-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="1d41a-116">頁面滾動效果所顯示的新影像數量（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1d41a-116">Amount of the new image that is revealed by the page roll effect, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d41a-117">方向</span><span class="sxs-lookup"><span data-stu-id="1d41a-117">Direction</span></span></td>
<td><span data-ttu-id="1d41a-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="1d41a-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="1d41a-119">頁面變換來源的影片框架邊角或側邊。設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1d41a-119">Corner or side of the video frame, from which the page roll originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="1d41a-120">0-左邊</span><span class="sxs-lookup"><span data-stu-id="1d41a-120">0 - Left side</span></span></li>
<li><span data-ttu-id="1d41a-121">1-右端</span><span class="sxs-lookup"><span data-stu-id="1d41a-121">1 - Right side</span></span></li>
<li><span data-ttu-id="1d41a-122">2-下</span><span class="sxs-lookup"><span data-stu-id="1d41a-122">2 - Bottom</span></span></li>
<li><span data-ttu-id="1d41a-123">3-上方</span><span class="sxs-lookup"><span data-stu-id="1d41a-123">3 - Top</span></span></li>
<li><span data-ttu-id="1d41a-124">4-左下角</span><span class="sxs-lookup"><span data-stu-id="1d41a-124">4 - Bottom left corner</span></span></li>
<li><span data-ttu-id="1d41a-125">5-右下角</span><span class="sxs-lookup"><span data-stu-id="1d41a-125">5 - Bottom right corner</span></span></li>
<li><span data-ttu-id="1d41a-126">6-左上角</span><span class="sxs-lookup"><span data-stu-id="1d41a-126">6 - Upper left corner</span></span></li>
<li><span data-ttu-id="1d41a-127">7-右上角</span><span class="sxs-lookup"><span data-stu-id="1d41a-127">7 - Upper right corner</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d41a-128">Composition</span><span class="sxs-lookup"><span data-stu-id="1d41a-128">Composition</span></span></td>
<td><span data-ttu-id="1d41a-129"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="1d41a-129"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="1d41a-130">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1d41a-130">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="1d41a-131">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="1d41a-131">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="1d41a-132">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="1d41a-132">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1d41a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d41a-133">Requirements</span></span>



| <span data-ttu-id="1d41a-134">需求</span><span class="sxs-lookup"><span data-stu-id="1d41a-134">Requirement</span></span> | <span data-ttu-id="1d41a-135">值</span><span class="sxs-lookup"><span data-stu-id="1d41a-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d41a-136">標頭</span><span class="sxs-lookup"><span data-stu-id="1d41a-136">Header</span></span><br/> | <dl> <span data-ttu-id="1d41a-137"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d41a-137"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d41a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d41a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d41a-139">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="1d41a-139">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





