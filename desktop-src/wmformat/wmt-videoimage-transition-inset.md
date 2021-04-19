---
title: 'WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl) '
description: 內凹轉換會在源自框架某一個角落的矩形中顯示新影像。
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987066"
---
# <a name="wmt_videoimage_transition_inset"></a><span data-ttu-id="61372-104">WMT \_ VIDEOIMAGE \_ 轉換內 \_ 凹</span><span class="sxs-lookup"><span data-stu-id="61372-104">WMT\_VIDEOIMAGE\_TRANSITION\_INSET</span></span>

<span data-ttu-id="61372-105">內凹轉換會在源自框架某一個角落的矩形中顯示新影像。</span><span class="sxs-lookup"><span data-stu-id="61372-105">The inset transition reveals the new image in a rectangle originating from one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="61372-106">參數</span><span class="sxs-lookup"><span data-stu-id="61372-106">Parameters</span></span>

<span data-ttu-id="61372-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="61372-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61372-108">參數</span><span class="sxs-lookup"><span data-stu-id="61372-108">Parameter</span></span></th>
<th><span data-ttu-id="61372-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="61372-109">Structure member</span></span></th>
<th><span data-ttu-id="61372-110">Description</span><span class="sxs-lookup"><span data-stu-id="61372-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61372-111">寬度</span><span class="sxs-lookup"><span data-stu-id="61372-111">Width</span></span></td>
<td><span data-ttu-id="61372-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="61372-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="61372-113">內凹的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="61372-113">Width of the inset in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61372-114">高度</span><span class="sxs-lookup"><span data-stu-id="61372-114">Height</span></span></td>
<td><span data-ttu-id="61372-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="61372-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="61372-116">內凹的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="61372-116">Height of the inset in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61372-117">方向</span><span class="sxs-lookup"><span data-stu-id="61372-117">Direction</span></span></td>
<td><span data-ttu-id="61372-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="61372-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="61372-119">內凹來源的邊角。設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="61372-119">Corner from which the inset originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="61372-120">0-左下角</span><span class="sxs-lookup"><span data-stu-id="61372-120">0 - Lower left</span></span></li>
<li><span data-ttu-id="61372-121">1-右下</span><span class="sxs-lookup"><span data-stu-id="61372-121">1 - Lower right</span></span></li>
<li><span data-ttu-id="61372-122">2-左上</span><span class="sxs-lookup"><span data-stu-id="61372-122">2 - Upper left</span></span></li>
<li><span data-ttu-id="61372-123">3-右上</span><span class="sxs-lookup"><span data-stu-id="61372-123">3 - Upper right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61372-124">Composition</span><span class="sxs-lookup"><span data-stu-id="61372-124">Composition</span></span></td>
<td><span data-ttu-id="61372-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="61372-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="61372-126">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="61372-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="61372-127">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="61372-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="61372-128">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="61372-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="61372-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="61372-129">Requirements</span></span>



| <span data-ttu-id="61372-130">需求</span><span class="sxs-lookup"><span data-stu-id="61372-130">Requirement</span></span> | <span data-ttu-id="61372-131">值</span><span class="sxs-lookup"><span data-stu-id="61372-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61372-132">標頭</span><span class="sxs-lookup"><span data-stu-id="61372-132">Header</span></span><br/> | <dl> <span data-ttu-id="61372-133"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="61372-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61372-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61372-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61372-135">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="61372-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





