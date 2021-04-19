---
title: 'WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl) '
description: 對角線轉換會沿著框架的一個角落以對角線線顯示新影像。
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976000"
---
# <a name="wmt_videoimage_transition_diagonal"></a><span data-ttu-id="3a6bc-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 對角線</span><span class="sxs-lookup"><span data-stu-id="3a6bc-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL</span></span>

<span data-ttu-id="3a6bc-105">對角線轉換會沿著框架的一個角落以對角線線顯示新影像。</span><span class="sxs-lookup"><span data-stu-id="3a6bc-105">The diagonal transition reveals the new image along a diagonal line originating in one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a6bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="3a6bc-106">Parameters</span></span>

<span data-ttu-id="3a6bc-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="3a6bc-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a6bc-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a6bc-108">Parameter</span></span></th>
<th><span data-ttu-id="3a6bc-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="3a6bc-109">Structure member</span></span></th>
<th><span data-ttu-id="3a6bc-110">Description</span><span class="sxs-lookup"><span data-stu-id="3a6bc-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a6bc-111">寬度</span><span class="sxs-lookup"><span data-stu-id="3a6bc-111">Width</span></span></td>
<td><span data-ttu-id="3a6bc-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="3a6bc-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="3a6bc-113">對角線區段的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a6bc-113">Width of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a6bc-114">高度</span><span class="sxs-lookup"><span data-stu-id="3a6bc-114">Height</span></span></td>
<td><span data-ttu-id="3a6bc-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="3a6bc-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="3a6bc-116">對角線區段的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a6bc-116">Height of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a6bc-117">方向</span><span class="sxs-lookup"><span data-stu-id="3a6bc-117">Direction</span></span></td>
<td><span data-ttu-id="3a6bc-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="3a6bc-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="3a6bc-119">決定轉換來源的邊角。設定為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="3a6bc-119">Determines the corner from which the transition originates.Set to one of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="3a6bc-120">0-右上</span><span class="sxs-lookup"><span data-stu-id="3a6bc-120">0 - Upper right</span></span></li>
<li><span data-ttu-id="3a6bc-121">1-左上</span><span class="sxs-lookup"><span data-stu-id="3a6bc-121">1 - Upper left</span></span></li>
<li><span data-ttu-id="3a6bc-122">2-右下</span><span class="sxs-lookup"><span data-stu-id="3a6bc-122">2 - Lower right</span></span></li>
<li><span data-ttu-id="3a6bc-123">3-左下角</span><span class="sxs-lookup"><span data-stu-id="3a6bc-123">3 - Lower left</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a6bc-124">Composition</span><span class="sxs-lookup"><span data-stu-id="3a6bc-124">Composition</span></span></td>
<td><span data-ttu-id="3a6bc-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="3a6bc-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="3a6bc-126">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="3a6bc-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="3a6bc-127">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="3a6bc-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="3a6bc-128">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景。</span><span class="sxs-lookup"><span data-stu-id="3a6bc-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3a6bc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a6bc-129">Requirements</span></span>



| <span data-ttu-id="3a6bc-130">需求</span><span class="sxs-lookup"><span data-stu-id="3a6bc-130">Requirement</span></span> | <span data-ttu-id="3a6bc-131">值</span><span class="sxs-lookup"><span data-stu-id="3a6bc-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6bc-132">標頭</span><span class="sxs-lookup"><span data-stu-id="3a6bc-132">Header</span></span><br/> | <dl> <span data-ttu-id="3a6bc-133"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a6bc-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a6bc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a6bc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6bc-135">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="3a6bc-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





