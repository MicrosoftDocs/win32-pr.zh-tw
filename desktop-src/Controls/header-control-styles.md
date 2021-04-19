---
title: '標題控制項樣式 (CommCtrl .h) '
description: 標題控制項有許多樣式（如本節所述），可決定控制項的外觀和行為。 當您建立標題控制項時，會設定初始樣式。
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990605"
---
# <a name="header-control-styles"></a><span data-ttu-id="6962c-104">標題控制項樣式</span><span class="sxs-lookup"><span data-stu-id="6962c-104">Header Control Styles</span></span>

<span data-ttu-id="6962c-105">標題控制項有許多樣式（如本節所述），可決定控制項的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="6962c-105">Header controls have a number of styles, described in this section, that determine the control's appearance and behavior.</span></span> <span data-ttu-id="6962c-106">當您建立標題控制項時，會設定初始樣式。</span><span class="sxs-lookup"><span data-stu-id="6962c-106">You set the initial styles when you create the header control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6962c-107">常數</span><span class="sxs-lookup"><span data-stu-id="6962c-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6962c-108">描述</span><span class="sxs-lookup"><span data-stu-id="6962c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <span data-ttu-id="6962c-109"><dt><strong>HDS_BUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-109"><dt><strong>HDS_BUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-110">控制項中的每個專案的外觀和行為就像是按下按鈕。</span><span class="sxs-lookup"><span data-stu-id="6962c-110">Each item in the control looks and behaves like a push button.</span></span> <span data-ttu-id="6962c-111">如果應用程式在使用者按一下標題控制項中的專案時執行工作，此樣式就很有用。</span><span class="sxs-lookup"><span data-stu-id="6962c-111">This style is useful if an application carries out a task when the user clicks an item in the header control.</span></span> <span data-ttu-id="6962c-112">例如，應用程式可以根據使用者按一下的專案，以不同的方式排序資料行中的資訊。</span><span class="sxs-lookup"><span data-stu-id="6962c-112">For example, an application could sort information in the columns differently depending on which item the user clicks.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <span data-ttu-id="6962c-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-114">允許標題專案的拖放重新排列。</span><span class="sxs-lookup"><span data-stu-id="6962c-114">Allows drag-and-drop reordering of header items.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <span data-ttu-id="6962c-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-116">在標準標題控制項中包含篩選列。</span><span class="sxs-lookup"><span data-stu-id="6962c-116">Include a filter bar as part of the standard header control.</span></span> <span data-ttu-id="6962c-117">此列可讓使用者方便地將篩選套用至顯示器。</span><span class="sxs-lookup"><span data-stu-id="6962c-117">This bar allows users to conveniently apply a filter to the display.</span></span> <span data-ttu-id="6962c-118"><a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a>的呼叫會產生控制項的新大小，並導致清單視圖更新。</span><span class="sxs-lookup"><span data-stu-id="6962c-118">Calls to <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> will yield a new size for the control and cause the list view to update.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <span data-ttu-id="6962c-119"><dt><strong>HDS_FLAT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-119"><dt><strong>HDS_FLAT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-120"><a href="common-control-versions.md">6.0 版和更新版本</a>。</span><span class="sxs-lookup"><span data-stu-id="6962c-120"><a href="common-control-versions.md">Version 6.0 and later</a>.</span></span> <span data-ttu-id="6962c-121">當作業系統在傳統模式中執行時，會導致標題控制項成為平面的繪圖。</span><span class="sxs-lookup"><span data-stu-id="6962c-121">Causes the header control to be drawn flat when the operating system is running in classic mode.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6962c-122">Comctl32.dll 第6版不是可轉散發套件，但包含在 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="6962c-122">Comctl32.dll version 6 is not redistributable but it is included in Windows.</span></span> <span data-ttu-id="6962c-123">若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。</span><span class="sxs-lookup"><span data-stu-id="6962c-123">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="6962c-124">如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="6962c-124">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <span data-ttu-id="6962c-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-126">即使使用者調整資料行的大小，也會讓標題控制項顯示資料行內容。</span><span class="sxs-lookup"><span data-stu-id="6962c-126">Causes the header control to display column contents even while the user resizes a column.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <span data-ttu-id="6962c-127"><dt><strong>HDS_HIDDEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-127"><dt><strong>HDS_HIDDEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-128">表示要隱藏的標題控制項。</span><span class="sxs-lookup"><span data-stu-id="6962c-128">Indicates a header control that is intended to be hidden.</span></span> <span data-ttu-id="6962c-129">這個樣式不會隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="6962c-129">This style does not hide the control.</span></span> <span data-ttu-id="6962c-130">相反地，當您將<a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a>訊息傳送至具有 HDS_HIDDEN 樣式的標題控制項時，控制項會在<a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a>結構的<strong>cy</strong>成員中傳回零。</span><span class="sxs-lookup"><span data-stu-id="6962c-130">Instead, when you send the <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> message to a header control with the HDS_HIDDEN style, the control returns zero in the <strong>cy</strong> member of the <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> structure.</span></span> <span data-ttu-id="6962c-131">然後，您可以將控制項的高度設定為零來隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="6962c-131">You would then hide the control by setting its height to zero.</span></span> <span data-ttu-id="6962c-132">當您想要將控制項用作資訊容器而非視覺化控制項時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="6962c-132">This can be useful when you want to use the control as an information container instead of a visual control.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <span data-ttu-id="6962c-133"><dt><strong>HDS_HORZ</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-133"><dt><strong>HDS_HORZ</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-134">建立具有水準方向的標題控制項。</span><span class="sxs-lookup"><span data-stu-id="6962c-134">Creates a header control with a horizontal orientation.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <span data-ttu-id="6962c-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-136">啟用熱追蹤。</span><span class="sxs-lookup"><span data-stu-id="6962c-136">Enables hot tracking.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <span data-ttu-id="6962c-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-138"><a href="common-control-versions.md">6.00 版和更新版本</a>。</span><span class="sxs-lookup"><span data-stu-id="6962c-138"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="6962c-139">允許在標題專案上放置核取方塊。</span><span class="sxs-lookup"><span data-stu-id="6962c-139">Allows the placing of checkboxes on header items.</span></span> <span data-ttu-id="6962c-140">如需詳細資訊，請參閱<a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>的<strong>bcp.fmt</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="6962c-140">For more information, see the <strong>fmt</strong> member of <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <span data-ttu-id="6962c-141"><dt><strong>HDS_NOSIZING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-141"><dt><strong>HDS_NOSIZING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-142"><a href="common-control-versions.md">6.00 版和更新版本</a>。</span><span class="sxs-lookup"><span data-stu-id="6962c-142"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="6962c-143">使用者無法拖曳標題控制項上的分隔線。</span><span class="sxs-lookup"><span data-stu-id="6962c-143">The user cannot drag the divider on the header control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <span data-ttu-id="6962c-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6962c-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6962c-145"><a href="common-control-versions.md">6.00 版和更新版本</a>。</span><span class="sxs-lookup"><span data-stu-id="6962c-145"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="6962c-146">當不是所有專案都可以顯示在標題控制項的矩形內時，會顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="6962c-146">A button is displayed when not all items can be displayed within the header control's rectangle.</span></span> <span data-ttu-id="6962c-147">按一下時，此按鈕會傳送 <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> 通知。</span><span class="sxs-lookup"><span data-stu-id="6962c-147">When clicked, this button sends an <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notification.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="6962c-148">備註</span><span class="sxs-lookup"><span data-stu-id="6962c-148">Remarks</span></span>

<span data-ttu-id="6962c-149">若要在建立控制項之後取得並變更樣式，請使用 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 和 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數。</span><span class="sxs-lookup"><span data-stu-id="6962c-149">To retrieve and change the styles after creating the control, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6962c-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="6962c-150">Requirements</span></span>



| <span data-ttu-id="6962c-151">需求</span><span class="sxs-lookup"><span data-stu-id="6962c-151">Requirement</span></span> | <span data-ttu-id="6962c-152">值</span><span class="sxs-lookup"><span data-stu-id="6962c-152">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6962c-153">標頭</span><span class="sxs-lookup"><span data-stu-id="6962c-153">Header</span></span><br/> | <dl> <span data-ttu-id="6962c-154"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6962c-154"><dt>CommCtrl.h</dt></span></span> </dl> |



