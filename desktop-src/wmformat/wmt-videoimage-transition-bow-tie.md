---
title: 'WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl) '
description: 凸起系結轉換會將新影像顯示在框架的相反邊的一組三角形中。
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992383"
---
# <a name="wmt_videoimage_transition_bow_tie"></a><span data-ttu-id="cc937-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 凸起 \_ 系結</span><span class="sxs-lookup"><span data-stu-id="cc937-104">WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE</span></span>

<span data-ttu-id="cc937-105">凸起系結轉換會將新影像顯示在框架的相反邊的一組三角形中。</span><span class="sxs-lookup"><span data-stu-id="cc937-105">The bow tie transition reveals the new image in a set of triangles on opposite sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc937-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc937-106">Parameters</span></span>

<span data-ttu-id="cc937-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="cc937-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc937-108">參數</span><span class="sxs-lookup"><span data-stu-id="cc937-108">Parameter</span></span></th>
<th><span data-ttu-id="cc937-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="cc937-109">Structure member</span></span></th>
<th><span data-ttu-id="cc937-110">Description</span><span class="sxs-lookup"><span data-stu-id="cc937-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc937-111">寬度</span><span class="sxs-lookup"><span data-stu-id="cc937-111">Width</span></span></td>
<td><span data-ttu-id="cc937-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="cc937-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="cc937-113">凸起系結之每個三角形側的寬度。</span><span class="sxs-lookup"><span data-stu-id="cc937-113">Width of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc937-114">高度</span><span class="sxs-lookup"><span data-stu-id="cc937-114">Height</span></span></td>
<td><span data-ttu-id="cc937-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="cc937-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="cc937-116">凸起系結的每個三角形的高度。</span><span class="sxs-lookup"><span data-stu-id="cc937-116">Height of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc937-117">方向</span><span class="sxs-lookup"><span data-stu-id="cc937-117">Direction</span></span></td>
<td><span data-ttu-id="cc937-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="cc937-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="cc937-119">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cc937-119">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cc937-120">0-指定水準凸起系結效果，其中三角形會從框架的右邊和左邊輸入。</span><span class="sxs-lookup"><span data-stu-id="cc937-120">0 - Specifies horizontal bow tie effect, in which the triangles enter from the right and left sides of the frame.</span></span></li>
<li><span data-ttu-id="cc937-121">1-指定垂直凸起系結效果，其中三角形會從框架的頂端和底部進入。</span><span class="sxs-lookup"><span data-stu-id="cc937-121">1 - Specifies vertical bow tie effect, in which the triangles enter from the top and bottom of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc937-122">Composition</span><span class="sxs-lookup"><span data-stu-id="cc937-122">Composition</span></span></td>
<td><span data-ttu-id="cc937-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="cc937-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="cc937-124">設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cc937-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cc937-125">0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</span><span class="sxs-lookup"><span data-stu-id="cc937-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="cc937-126">1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景。</span><span class="sxs-lookup"><span data-stu-id="cc937-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cc937-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc937-127">Requirements</span></span>



| <span data-ttu-id="cc937-128">需求</span><span class="sxs-lookup"><span data-stu-id="cc937-128">Requirement</span></span> | <span data-ttu-id="cc937-129">值</span><span class="sxs-lookup"><span data-stu-id="cc937-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc937-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cc937-130">Header</span></span><br/> | <dl> <span data-ttu-id="cc937-131"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc937-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc937-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc937-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc937-133">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="cc937-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





