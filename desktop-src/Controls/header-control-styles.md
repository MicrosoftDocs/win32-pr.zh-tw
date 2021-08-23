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
ms.openlocfilehash: fe76446196c565796388a5bcd402e9fb3a071e1b14626d7ead949ab9eb0e3b61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435098"
---
# <a name="header-control-styles"></a>標題控制項樣式

標題控制項有許多樣式（如本節所述），可決定控制項的外觀和行為。 當您建立標題控制項時，會設定初始樣式。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <dt><strong>HDS_BUTTONS</strong></dt> </dl></td>
<td style="text-align: left;">控制項中的每個專案的外觀和行為就像是按下按鈕。 如果應用程式在使用者按一下標題控制項中的專案時執行工作，此樣式就很有用。 例如，應用程式可以根據使用者按一下的專案，以不同的方式排序資料行中的資訊。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <dt><strong>HDS_DRAGDROP</strong></dt> </dl></td>
<td style="text-align: left;">允許標題專案的拖放重新排列。 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <dt><strong>HDS_FILTERBAR</strong></dt> </dl></td>
<td style="text-align: left;">在標準標題控制項中包含篩選列。 此列可讓使用者方便地將篩選套用至顯示器。 <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a>的呼叫會產生控制項的新大小，並導致清單視圖更新。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <dt><strong>HDS_FLAT</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">6.0 版和更新版本</a>。 當作業系統在傳統模式中執行時，會導致標題控制項成為平面的繪圖。 <br/>
<blockquote>
[!Note]<br />
Comctl32.dll 第6版不是可轉散發套件，但包含在 Windows 中。 若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。 如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <dt><strong>HDS_FULLDRAG</strong></dt> </dl></td>
<td style="text-align: left;">即使使用者調整資料行的大小，也會讓標題控制項顯示資料行內容。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <dt><strong>HDS_HIDDEN</strong></dt> </dl></td>
<td style="text-align: left;">表示要隱藏的標題控制項。 這個樣式不會隱藏控制項。 相反地，當您將<a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a>訊息傳送至具有 HDS_HIDDEN 樣式的標題控制項時，控制項會在<a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a>結構的<strong>cy</strong>成員中傳回零。 然後，您可以將控制項的高度設定為零來隱藏控制項。 當您想要將控制項用作資訊容器而非視覺化控制項時，這會很有用。 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <dt><strong>HDS_HORZ</strong></dt> </dl></td>
<td style="text-align: left;">建立具有水準方向的標題控制項。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <dt><strong>HDS_HOTTRACK</strong></dt> </dl></td>
<td style="text-align: left;">啟用熱追蹤。 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <dt><strong>HDS_CHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">6.00 版和更新版本</a>。 允許在標題專案上放置核取方塊。 如需詳細資訊，請參閱<a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>的<strong>bcp.fmt</strong>成員。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <dt><strong>HDS_NOSIZING</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">6.00 版和更新版本</a>。 使用者無法拖曳標題控制項上的分隔線。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <dt><strong>HDS_OVERFLOW</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">6.00 版和更新版本</a>。 當不是所有專案都可以顯示在標題控制項的矩形內時，會顯示按鈕。 按一下時，此按鈕會傳送 <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> 通知。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

若要在建立控制項之後取得並變更樣式，請使用 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 和 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



