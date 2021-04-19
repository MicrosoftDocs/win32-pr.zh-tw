---
title: '進度列控制項樣式 (CommCtrl .h) '
description: 進度列控制項支援下列控制項樣式
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999225"
---
# <a name="progress-bar-control-styles"></a><span data-ttu-id="3265c-103">進度列控制項樣式</span><span class="sxs-lookup"><span data-stu-id="3265c-103">Progress Bar Control Styles</span></span>

<span data-ttu-id="3265c-104">[進度](progress-bar-control.md)列控制項支援下列控制項樣式：</span><span class="sxs-lookup"><span data-stu-id="3265c-104">The following control styles are supported by [Progress Bar](progress-bar-control.md) controls:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3265c-105">常數</span><span class="sxs-lookup"><span data-stu-id="3265c-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3265c-106">描述</span><span class="sxs-lookup"><span data-stu-id="3265c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <span data-ttu-id="3265c-107"><dt><strong>PBS_MARQUEE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3265c-107"><dt><strong>PBS_MARQUEE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3265c-108"><a href="common-control-versions.md">6.0 版</a> 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3265c-108"><a href="common-control-versions.md">Version 6.0</a> or later.</span></span> <span data-ttu-id="3265c-109">進度指示器的大小不會增加，而是沿著橫條的長度重複移動，表示活動，而不指定進度的比例。</span><span class="sxs-lookup"><span data-stu-id="3265c-109">The progress indicator does not grow in size but instead moves repeatedly along the length of the bar, indicating activity without specifying what proportion of the progress is complete.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3265c-110">Comctl32.dll 第6版不是可轉散發套件，但包含在 Windows 或更新版本中。</span><span class="sxs-lookup"><span data-stu-id="3265c-110">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="3265c-111">若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。</span><span class="sxs-lookup"><span data-stu-id="3265c-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="3265c-112">如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="3265c-112">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <span data-ttu-id="3265c-113"><dt><strong>PBS_SMOOTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3265c-113"><dt><strong>PBS_SMOOTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3265c-114"><a href="common-control-versions.md">4.70 版</a> 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3265c-114"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="3265c-115">進度列會在平滑捲軸中顯示進度狀態，而不是以預設分割的橫條圖顯示。</span><span class="sxs-lookup"><span data-stu-id="3265c-115">The progress bar displays progress status in a smooth scrolling bar instead of the default segmented bar.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3265c-116">只有 Windows 傳統主題才支援這個樣式。</span><span class="sxs-lookup"><span data-stu-id="3265c-116">This style is supported only in the Windows Classic theme.</span></span> <span data-ttu-id="3265c-117">所有其他主題都會覆寫這個樣式。</span><span class="sxs-lookup"><span data-stu-id="3265c-117">All other themes override this style.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <span data-ttu-id="3265c-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3265c-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3265c-119"><a href="common-control-versions.md">6.0 版</a> 或更新版本和 <strong>Windows Vista 版本。</strong></span><span class="sxs-lookup"><span data-stu-id="3265c-119"><a href="common-control-versions.md">Version 6.0</a> or later and <strong>Windows Vista.</strong></span></span> <span data-ttu-id="3265c-120">決定當 (從較高的值移至較低的值) 時，進度列應使用的動畫行為。</span><span class="sxs-lookup"><span data-stu-id="3265c-120">Determines the animation behavior that the progress bar should use when moving backward (from a higher value to a lower value).</span></span> <span data-ttu-id="3265c-121">如果設定此值，則 &quot; &quot; 會發生平滑轉換，否則控制項會 &quot; 跳 &quot; 至較低的值。</span><span class="sxs-lookup"><span data-stu-id="3265c-121">If this is set, then a &quot;smooth&quot; transition will occur, otherwise the control will &quot;jump&quot; to the lower value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <span data-ttu-id="3265c-122"><dt><strong>PBS_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3265c-122"><dt><strong>PBS_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3265c-123"><a href="common-control-versions.md">4.70 版</a> 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3265c-123"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="3265c-124">進度列會從下到上垂直顯示進度狀態。</span><span class="sxs-lookup"><span data-stu-id="3265c-124">The progress bar displays progress status vertically, from bottom to top.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3265c-125">備註</span><span class="sxs-lookup"><span data-stu-id="3265c-125">Remarks</span></span>

<span data-ttu-id="3265c-126">您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)、 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)或 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)，以與其他通用控制項相同的方式設定進度列樣式。</span><span class="sxs-lookup"><span data-stu-id="3265c-126">You can set progress bar styles, in the same way as other common controls, with [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga), or [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="3265c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3265c-127">Requirements</span></span>



| <span data-ttu-id="3265c-128">需求</span><span class="sxs-lookup"><span data-stu-id="3265c-128">Requirement</span></span> | <span data-ttu-id="3265c-129">值</span><span class="sxs-lookup"><span data-stu-id="3265c-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3265c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3265c-130">Header</span></span><br/> | <dl> <span data-ttu-id="3265c-131"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3265c-131"><dt>CommCtrl.h</dt></span></span> </dl> |



 

