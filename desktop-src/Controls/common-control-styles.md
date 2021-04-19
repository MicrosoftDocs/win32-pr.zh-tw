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
# <a name="common-control-styles"></a>通用控制項樣式

本節列出常見的控制項樣式。 除非有注明，否則這些樣式適用于 Rebar 控制項、工具列控制項和狀態視窗。



| 常數                                                                                                                                                                  | 描述                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**CCS 可 \_ 調整**</dt> </dl>          | 啟用工具列的內建自訂功能，可讓使用者將按鈕拖曳至新位置，或將按鈕拖曳至工具列上以移除按鈕。 此外，使用者可以按兩下工具列顯示 [ **自訂工具列** ] 對話方塊，讓使用者加入、刪除及重新排列工具列按鈕。<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS \_ 底部**</dt> </dl>                      | 讓控制項將本身定位在父視窗的工作區底部，然後將寬度設定為與父視窗寬度相同。 狀態視窗預設具有此樣式。<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**\_左 CCS**</dt> </dl>                            | [版本 4.70](common-controls-intro.md)。 使控制項在父視窗的左側以垂直方式顯示。<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS \_ NODIVIDER**</dt> </dl>             | 防止在控制項頂端繪製兩個圖元的醒目提示。 <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ NOMOVEX**</dt> </dl>                   | [版本 4.70](common-controls-intro.md)。 使控制項的調整大小和移動本身垂直（但不是水準），以回應 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 的訊息。 如果 \_ 使用 CCS NORESIZE，則不適用這個樣式。<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOMOVEY**</dt> </dl>                   | 使控制項以水準方式調整大小並移動本身，但不會垂直移動，以回應 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 的訊息。 如果 \_ 使用 CCS NORESIZE，則不適用這個樣式。 標題視窗預設具有此樣式。<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ NOPARENTALIGN**</dt> </dl> | 防止控制項自動移至父視窗的頂端或底部。 相反地，即使變更父系的大小，控制項仍會在父視窗內保存其位置。 如果 \_ 也使用 CCS TOP 或 CCS \_ 底端，高度會調整為預設值，但位置和寬度會維持不變。 <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NORESIZE**</dt> </dl>                | 在設定初始大小或新的大小時，防止控制項使用預設的寬度和高度。 相反地，控制項會使用要求中所指定的寬度和高度來建立或調整大小。 <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS \_ RIGHT**</dt> </dl>                         | [版本 4.70](common-controls-intro.md)。 使控制項在父視窗的右邊垂直顯示。<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS \_ TOP**</dt> </dl>                               | 讓控制項將本身定位在父視窗的工作區頂端，並將寬度設定為與父視窗寬度相同。 工具列預設具有此樣式。 <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS \_ 垂直**</dt> </dl>                            | [版本 4.70](common-controls-intro.md)。 使控制項垂直顯示。<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>備註

下列主題將描述其他控制項樣式：

-   [**動畫控制項樣式**](animation-control-styles.md)
-   [**按鈕樣式**](button-styles.md)
-   [**下拉式列示方塊樣式**](combo-box-styles.md)
-   [**ComboBoxEx 控制項擴充樣式**](comboboxex-control-extended-styles.md)
-   [**日期和時間選擇器控制項樣式**](date-and-time-picker-control-styles.md)
-   [**編輯控制項樣式**](edit-control-styles.md)
-   [**標題控制項樣式**](header-control-styles.md)
-   [**清單方塊樣式**](list-box-styles.md)
-   [**清單視圖視窗樣式**](list-view-window-styles.md)
-   [**月曆控制項樣式**](month-calendar-control-styles.md)
-   [**呼機控制項樣式**](pager-control-styles.md)
-   [**進度列控制項樣式**](progress-bar-control-styles.md)
-   [**Rebar 控制項樣式**](rebar-control-styles.md)
-   [**Rich Edit 控制項樣式**](rich-edit-control-styles.md)
-   [**捲軸控制項樣式**](scroll-bar-control-styles.md)
-   [靜態控制項樣式](static-control-styles.md)
-   [**狀態列樣式**](status-bar-styles.md)
-   [**SysLink 控制項樣式**](syslink-control-styles.md)
-   [**索引標籤控制項樣式**](tab-control-styles.md)
-   [**Toolbar 控制項和按鈕樣式**](toolbar-control-and-button-styles.md)
-   [**工具提示樣式**](tooltip-styles.md)
-   [**[控制項] 控制項樣式**](trackbar-control-styles.md)
-   [**樹狀檢視控制項視窗樣式**](tree-view-control-window-styles.md)
-   [**上下控制項樣式**](up-down-control-styles.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

