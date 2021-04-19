---
title: 'WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl) '
description: 翻轉轉換會透過框架的中央旋轉 y 軸上的舊影像。 新映射會顯示為舊影像的背面。
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996314"
---
# <a name="wmt_videoimage_transition_flip"></a><span data-ttu-id="239e4-105">WMT \_ VIDEOIMAGE \_ 轉換 \_ 翻轉</span><span class="sxs-lookup"><span data-stu-id="239e4-105">WMT\_VIDEOIMAGE\_TRANSITION\_FLIP</span></span>

<span data-ttu-id="239e4-106">翻轉轉換會透過框架的中央旋轉 y 軸上的舊影像。</span><span class="sxs-lookup"><span data-stu-id="239e4-106">The flip transition rotates the old image on a y-axis through the center of the frame.</span></span> <span data-ttu-id="239e4-107">新映射會顯示為舊影像的背面。</span><span class="sxs-lookup"><span data-stu-id="239e4-107">The new image is revealed as the back of the old image.</span></span>

## <a name="parameters"></a><span data-ttu-id="239e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="239e4-108">Parameters</span></span>

<span data-ttu-id="239e4-109">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="239e4-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="239e4-110">參數</span><span class="sxs-lookup"><span data-stu-id="239e4-110">Parameter</span></span></th>
<th><span data-ttu-id="239e4-111">結構成員</span><span class="sxs-lookup"><span data-stu-id="239e4-111">Structure member</span></span></th>
<th><span data-ttu-id="239e4-112">Description</span><span class="sxs-lookup"><span data-stu-id="239e4-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="239e4-113">角度</span><span class="sxs-lookup"><span data-stu-id="239e4-113">Angle</span></span></td>
<td><span data-ttu-id="239e4-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="239e4-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="239e4-115">旋轉的角度，從0.0 到180.0 度。</span><span class="sxs-lookup"><span data-stu-id="239e4-115">Angle of the rotation, from 0.0 to 180.0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239e4-116">Composition</span><span class="sxs-lookup"><span data-stu-id="239e4-116">Composition</span></span></td>
<td><span data-ttu-id="239e4-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="239e4-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="239e4-118">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="239e4-118">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="239e4-119">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="239e4-119">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="239e4-120">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</span><span class="sxs-lookup"><span data-stu-id="239e4-120">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="239e4-121">備註</span><span class="sxs-lookup"><span data-stu-id="239e4-121">Remarks</span></span>

<span data-ttu-id="239e4-122">您可以將這項轉換的效果視覺化，就像這兩個影像都是將兩個影像都與後置中的實體相片一起進行。</span><span class="sxs-lookup"><span data-stu-id="239e4-122">You can visualize the effect of this transition as if both images were physical photographs glued together back-to-back.</span></span> <span data-ttu-id="239e4-123">轉換的效果與將兩個這類相片放在下邊緣，並將它們旋轉180度的效果相同。</span><span class="sxs-lookup"><span data-stu-id="239e4-123">The transition has the same effect as holding two such photographs at the center of the bottom edge and rotating them 180 degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="239e4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="239e4-124">Requirements</span></span>



| <span data-ttu-id="239e4-125">需求</span><span class="sxs-lookup"><span data-stu-id="239e4-125">Requirement</span></span> | <span data-ttu-id="239e4-126">值</span><span class="sxs-lookup"><span data-stu-id="239e4-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="239e4-127">標頭</span><span class="sxs-lookup"><span data-stu-id="239e4-127">Header</span></span><br/> | <dl> <span data-ttu-id="239e4-128"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="239e4-128"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239e4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="239e4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239e4-130">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="239e4-130">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





