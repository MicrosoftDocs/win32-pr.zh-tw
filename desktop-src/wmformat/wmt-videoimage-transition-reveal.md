---
title: 'WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl) '
description: 「顯示」轉換會顯示來自框架某一端之直線的新影像。
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987902"
---
# <a name="wmt_videoimage_transition_reveal"></a><span data-ttu-id="ee88c-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 顯示</span><span class="sxs-lookup"><span data-stu-id="ee88c-104">WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL</span></span>

<span data-ttu-id="ee88c-105">「顯示」轉換會顯示來自框架某一端之直線的新影像。</span><span class="sxs-lookup"><span data-stu-id="ee88c-105">The reveal transition reveals the new image along a straight line originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee88c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee88c-106">Parameters</span></span>

<span data-ttu-id="ee88c-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="ee88c-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee88c-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee88c-108">Parameter</span></span></th>
<th><span data-ttu-id="ee88c-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="ee88c-109">Structure member</span></span></th>
<th><span data-ttu-id="ee88c-110">Description</span><span class="sxs-lookup"><span data-stu-id="ee88c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee88c-111">距離</span><span class="sxs-lookup"><span data-stu-id="ee88c-111">Distance</span></span></td>
<td><span data-ttu-id="ee88c-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="ee88c-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="ee88c-113">顯示的新影像數量（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee88c-113">Amount of the new image revealed, in pixels.</span></span> <span data-ttu-id="ee88c-114">此值相對於框架的原始端。</span><span class="sxs-lookup"><span data-stu-id="ee88c-114">This value is relative to the originating side of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee88c-115">方向</span><span class="sxs-lookup"><span data-stu-id="ee88c-115">Direction</span></span></td>
<td><span data-ttu-id="ee88c-116"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="ee88c-116"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="ee88c-117">洩漏的方向。設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="ee88c-117">Direction of the revealing.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="ee88c-118">0-向右顯示;源自框架的左邊。</span><span class="sxs-lookup"><span data-stu-id="ee88c-118">0 - Reveal to the right; originate from the left side of the frame.</span></span></li>
<li><span data-ttu-id="ee88c-119">1-向左顯示;源自框架的右側。</span><span class="sxs-lookup"><span data-stu-id="ee88c-119">1 - Reveal to the left; originate from the right side of the frame.</span></span></li>
<li><span data-ttu-id="ee88c-120">2-向上顯示;源自框架的底部。</span><span class="sxs-lookup"><span data-stu-id="ee88c-120">2 - Reveal upward; originate from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="ee88c-121">3-向下顯示;源自框架的頂端。</span><span class="sxs-lookup"><span data-stu-id="ee88c-121">3 - Reveal downward; originate from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee88c-122">Composition</span><span class="sxs-lookup"><span data-stu-id="ee88c-122">Composition</span></span></td>
<td><span data-ttu-id="ee88c-123"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="ee88c-123"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="ee88c-124">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="ee88c-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="ee88c-125">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="ee88c-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="ee88c-126">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="ee88c-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="ee88c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee88c-127">Requirements</span></span>



| <span data-ttu-id="ee88c-128">需求</span><span class="sxs-lookup"><span data-stu-id="ee88c-128">Requirement</span></span> | <span data-ttu-id="ee88c-129">值</span><span class="sxs-lookup"><span data-stu-id="ee88c-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee88c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ee88c-130">Header</span></span><br/> | <dl> <span data-ttu-id="ee88c-131"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee88c-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee88c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee88c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee88c-133">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="ee88c-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





