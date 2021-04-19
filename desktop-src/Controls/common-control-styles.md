---
title: '通用控制項樣式 (CommCtrl .h) '
description: 本節列出常見的控制項樣式。 除非有注明，否則這些樣式適用于 Rebar 控制項、工具列控制項和狀態視窗。
ms.assetid: aab0cd68-ede7-474b-8695-c75805669716
topic_type:
- apiref
api_name:
- CCS_ADJUSTABLE
- CCS_BOTTOM
- CCS_LEFT
- CCS_NODIVIDER
- CCS_NOMOVEX
- CCS_NOMOVEY
- CCS_NOPARENTALIGN
- CCS_NORESIZE
- CCS_RIGHT
- CCS_TOP
- CCS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a50b28a95d94a97da2fb6ac3522dbc568af111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984050"
---
# <a name="common-control-styles"></a><span data-ttu-id="3dbd7-104">通用控制項樣式</span><span class="sxs-lookup"><span data-stu-id="3dbd7-104">Common Control Styles</span></span>

<span data-ttu-id="3dbd7-105">本節列出常見的控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-105">This section lists common control styles.</span></span> <span data-ttu-id="3dbd7-106">除非有注明，否則這些樣式適用于 Rebar 控制項、工具列控制項和狀態視窗。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-106">Except where noted, these styles apply to rebar controls, toolbar controls, and status windows.</span></span>



| <span data-ttu-id="3dbd7-107">常數</span><span class="sxs-lookup"><span data-stu-id="3dbd7-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="3dbd7-108">描述</span><span class="sxs-lookup"><span data-stu-id="3dbd7-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <span data-ttu-id="3dbd7-109"><dt>**CCS 可 \_ 調整**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-109"><dt>**CCS\_ADJUSTABLE**</dt></span></span> </dl>          | <span data-ttu-id="3dbd7-110">啟用工具列的內建自訂功能，可讓使用者將按鈕拖曳至新位置，或將按鈕拖曳至工具列上以移除按鈕。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-110">Enables a toolbar's built-in customization features, which let the user to drag a button to a new position or to remove a button by dragging it off the toolbar.</span></span> <span data-ttu-id="3dbd7-111">此外，使用者可以按兩下工具列顯示 [ **自訂工具列** ] 對話方塊，讓使用者加入、刪除及重新排列工具列按鈕。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-111">In addition, the user can double-click the toolbar to display the **Customize Toolbar** dialog box, which enables the user to add, delete, and rearrange toolbar buttons.</span></span><br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <span data-ttu-id="3dbd7-112"><dt>**CCS \_ 底部**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-112"><dt>**CCS\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="3dbd7-113">讓控制項將本身定位在父視窗的工作區底部，然後將寬度設定為與父視窗寬度相同。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-113">Causes the control to position itself at the bottom of the parent window's client area and sets the width to be the same as the parent window's width.</span></span> <span data-ttu-id="3dbd7-114">狀態視窗預設具有此樣式。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-114">Status windows have this style by default.</span></span><br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <span data-ttu-id="3dbd7-115"><dt>**\_左 CCS**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-115"><dt>**CCS\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="3dbd7-116">[版本 4.70](common-controls-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-116">[Version 4.70](common-controls-intro.md).</span></span> <span data-ttu-id="3dbd7-117">使控制項在父視窗的左側以垂直方式顯示。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-117">Causes the control to be displayed vertically on the left side of the parent window.</span></span><br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <span data-ttu-id="3dbd7-118"><dt>**CCS \_ NODIVIDER**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-118"><dt>**CCS\_NODIVIDER**</dt></span></span> </dl>             | <span data-ttu-id="3dbd7-119">防止在控制項頂端繪製兩個圖元的醒目提示。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-119">Prevents a two-pixel highlight from being drawn at the top of the control.</span></span> <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <span data-ttu-id="3dbd7-120"><dt>**CCS \_ NOMOVEX**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-120"><dt>**CCS\_NOMOVEX**</dt></span></span> </dl>                   | <span data-ttu-id="3dbd7-121">[版本 4.70](common-controls-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-121">[Version 4.70](common-controls-intro.md).</span></span> <span data-ttu-id="3dbd7-122">使控制項的調整大小和移動本身垂直（但不是水準），以回應 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 的訊息。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-122">Causes the control to resize and move itself vertically, but not horizontally, in response to a [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span> <span data-ttu-id="3dbd7-123">如果 \_ 使用 CCS NORESIZE，則不適用這個樣式。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-123">If CCS\_NORESIZE is used, this style does not apply.</span></span><br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <span data-ttu-id="3dbd7-124"><dt>**CCS \_ NOMOVEY**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-124"><dt>**CCS\_NOMOVEY**</dt></span></span> </dl>                   | <span data-ttu-id="3dbd7-125">使控制項以水準方式調整大小並移動本身，但不會垂直移動，以回應 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 的訊息。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-125">Causes the control to resize and move itself horizontally, but not vertically, in response to a [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span> <span data-ttu-id="3dbd7-126">如果 \_ 使用 CCS NORESIZE，則不適用這個樣式。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-126">If CCS\_NORESIZE is used, this style does not apply.</span></span> <span data-ttu-id="3dbd7-127">標題視窗預設具有此樣式。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-127">Header windows have this style by default.</span></span><br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <span data-ttu-id="3dbd7-128"><dt>**CCS \_ NOPARENTALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-128"><dt>**CCS\_NOPARENTALIGN**</dt></span></span> </dl> | <span data-ttu-id="3dbd7-129">防止控制項自動移至父視窗的頂端或底部。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-129">Prevents the control from automatically moving to the top or bottom of the parent window.</span></span> <span data-ttu-id="3dbd7-130">相反地，即使變更父系的大小，控制項仍會在父視窗內保存其位置。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-130">Instead, the control keeps its position within the parent window despite changes to the size of the parent.</span></span> <span data-ttu-id="3dbd7-131">如果 \_ 也使用 CCS TOP 或 CCS \_ 底端，高度會調整為預設值，但位置和寬度會維持不變。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-131">If CCS\_TOP or CCS\_BOTTOM is also used, the height is adjusted to the default, but the position and width remain unchanged.</span></span> <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <span data-ttu-id="3dbd7-132"><dt>**CCS \_ NORESIZE**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-132"><dt>**CCS\_NORESIZE**</dt></span></span> </dl>                | <span data-ttu-id="3dbd7-133">在設定初始大小或新的大小時，防止控制項使用預設的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-133">Prevents the control from using the default width and height when setting its initial size or a new size.</span></span> <span data-ttu-id="3dbd7-134">相反地，控制項會使用要求中所指定的寬度和高度來建立或調整大小。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-134">Instead, the control uses the width and height specified in the request for creation or sizing.</span></span> <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <span data-ttu-id="3dbd7-135"><dt>**CCS \_ RIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-135"><dt>**CCS\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="3dbd7-136">[版本 4.70](common-controls-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-136">[Version 4.70](common-controls-intro.md).</span></span> <span data-ttu-id="3dbd7-137">使控制項在父視窗的右邊垂直顯示。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-137">Causes the control to be displayed vertically on the right side of the parent window.</span></span><br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <span data-ttu-id="3dbd7-138"><dt>**CCS \_ TOP**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-138"><dt>**CCS\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="3dbd7-139">讓控制項將本身定位在父視窗的工作區頂端，並將寬度設定為與父視窗寬度相同。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-139">Causes the control to position itself at the top of the parent window's client area and sets the width to be the same as the parent window's width.</span></span> <span data-ttu-id="3dbd7-140">工具列預設具有此樣式。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-140">Toolbars have this style by default.</span></span> <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <span data-ttu-id="3dbd7-141"><dt>**CCS \_ 垂直**</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-141"><dt>**CCS\_VERT**</dt></span></span> </dl>                            | <span data-ttu-id="3dbd7-142">[版本 4.70](common-controls-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-142">[Version 4.70](common-controls-intro.md).</span></span> <span data-ttu-id="3dbd7-143">使控制項垂直顯示。</span><span class="sxs-lookup"><span data-stu-id="3dbd7-143">Causes the control to be displayed vertically.</span></span><br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="3dbd7-144">備註</span><span class="sxs-lookup"><span data-stu-id="3dbd7-144">Remarks</span></span>

<span data-ttu-id="3dbd7-145">下列主題將描述其他控制項樣式：</span><span class="sxs-lookup"><span data-stu-id="3dbd7-145">The following topics describe additional control styles:</span></span>

-   [<span data-ttu-id="3dbd7-146">**動畫控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-146">**Animation Control Styles**</span></span>](animation-control-styles.md)
-   [<span data-ttu-id="3dbd7-147">**按鈕樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-147">**Button Styles**</span></span>](button-styles.md)
-   [<span data-ttu-id="3dbd7-148">**下拉式列示方塊樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-148">**Combo Box Styles**</span></span>](combo-box-styles.md)
-   [<span data-ttu-id="3dbd7-149">**ComboBoxEx 控制項擴充樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-149">**ComboBoxEx Control Extended Styles**</span></span>](comboboxex-control-extended-styles.md)
-   [<span data-ttu-id="3dbd7-150">**日期和時間選擇器控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-150">**Date and Time Picker Control Styles**</span></span>](date-and-time-picker-control-styles.md)
-   [<span data-ttu-id="3dbd7-151">**編輯控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-151">**Edit Control Styles**</span></span>](edit-control-styles.md)
-   [<span data-ttu-id="3dbd7-152">**標題控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-152">**Header Control Styles**</span></span>](header-control-styles.md)
-   [<span data-ttu-id="3dbd7-153">**清單方塊樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-153">**List Box Styles**</span></span>](list-box-styles.md)
-   [<span data-ttu-id="3dbd7-154">**清單視圖視窗樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-154">**List-View Window Styles**</span></span>](list-view-window-styles.md)
-   [<span data-ttu-id="3dbd7-155">**月曆控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-155">**Month Calendar Control Styles**</span></span>](month-calendar-control-styles.md)
-   [<span data-ttu-id="3dbd7-156">**呼機控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-156">**Pager Control Styles**</span></span>](pager-control-styles.md)
-   [<span data-ttu-id="3dbd7-157">**進度列控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-157">**Progress Bar Control Styles**</span></span>](progress-bar-control-styles.md)
-   [<span data-ttu-id="3dbd7-158">**Rebar 控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-158">**Rebar Control Styles**</span></span>](rebar-control-styles.md)
-   [<span data-ttu-id="3dbd7-159">**Rich Edit 控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-159">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
-   [<span data-ttu-id="3dbd7-160">**捲軸控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-160">**Scroll Bar Control Styles**</span></span>](scroll-bar-control-styles.md)
-   [<span data-ttu-id="3dbd7-161">靜態控制項樣式</span><span class="sxs-lookup"><span data-stu-id="3dbd7-161">Static Control Styles</span></span>](static-control-styles.md)
-   [<span data-ttu-id="3dbd7-162">**狀態列樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-162">**Status Bar Styles**</span></span>](status-bar-styles.md)
-   [<span data-ttu-id="3dbd7-163">**SysLink 控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-163">**SysLink Control Styles**</span></span>](syslink-control-styles.md)
-   [<span data-ttu-id="3dbd7-164">**索引標籤控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-164">**Tab Control Styles**</span></span>](tab-control-styles.md)
-   [<span data-ttu-id="3dbd7-165">**Toolbar 控制項和按鈕樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-165">**Toolbar Control and Button Styles**</span></span>](toolbar-control-and-button-styles.md)
-   [<span data-ttu-id="3dbd7-166">**工具提示樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-166">**Tooltip Styles**</span></span>](tooltip-styles.md)
-   <span data-ttu-id="3dbd7-167">[**[控制項] 控制項樣式**](trackbar-control-styles.md)</span><span class="sxs-lookup"><span data-stu-id="3dbd7-167">[**Trackbar Control Styles**](trackbar-control-styles.md)</span></span>
-   [<span data-ttu-id="3dbd7-168">**樹狀檢視控制項視窗樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-168">**Tree-View Control Window Styles**</span></span>](tree-view-control-window-styles.md)
-   [<span data-ttu-id="3dbd7-169">**上下控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="3dbd7-169">**Up-Down Control Styles**</span></span>](up-down-control-styles.md)

## <a name="requirements"></a><span data-ttu-id="3dbd7-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dbd7-170">Requirements</span></span>



| <span data-ttu-id="3dbd7-171">需求</span><span class="sxs-lookup"><span data-stu-id="3dbd7-171">Requirement</span></span> | <span data-ttu-id="3dbd7-172">值</span><span class="sxs-lookup"><span data-stu-id="3dbd7-172">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbd7-173">標頭</span><span class="sxs-lookup"><span data-stu-id="3dbd7-173">Header</span></span><br/> | <dl> <span data-ttu-id="3dbd7-174"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbd7-174"><dt>CommCtrl.h</dt></span></span> </dl> |



 

