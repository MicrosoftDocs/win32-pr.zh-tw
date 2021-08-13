---
title: '工具列擴充樣式 (CommCtrl .h) '
description: 本節列出工具列控制項支援的延伸樣式。
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25929fdc2d59d5cbed130693e795b722d1b99d831a8ee3d1b6129fe9a1955b78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119387808"
---
# <a name="toolbar-extended-styles"></a>工具列擴充樣式

本節列出工具列控制項支援的延伸樣式。



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
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">版本 4.71</a>。 此樣式可讓按鈕具有個別的下拉式箭號。 具有 <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> 樣式的按鈕會以下拉式箭號繪製在按鈕右邊的個別區段中。 如果按一下箭號，則只會按下按鈕的箭號部分，而工具列控制項會傳送 <a href="tbn-dropdown.md">TBN_DROPDOWN</a> 的通知碼，以提示應用程式顯示下拉式功能表。 如果按一下按鈕的主要部分，工具列控制項會傳送具有按鈕識別碼的 WM_COMMAND 訊息。 應用程式通常會透過啟動功能表上的第一個命令來回應。<br/> 在許多情況下，您可能只想要在具有分隔箭號的工具列上有一些下拉式按鈕。 若要這樣做，請設定 TBSTYLE_EX_DRAWDDARROWS 延伸樣式。 將沒有 <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> 樣式的分隔箭號提供給那些按鈕。 具有此樣式的按鈕會在影像旁邊顯示箭號。 不過，箭號不會分開，而且按一下按鈕的任何部分時，工具列控制項會傳送 <a href="tbn-dropdown.md">TBN_DROPDOWN</a> 的通知碼。 若要避免重新繪製問題，應該先設定此樣式，然後才會顯示工具列控制項。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">版本 5.81</a>。 此樣式會隱藏部分裁剪的按鈕。 此樣式最常見的用法是針對屬於 Rebar 控制項一部分的工具列。 如果連續的頻外涵蓋某個按鈕的一部分，將不會顯示該按鈕。 但是，如果 Rebar 帶 <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> 樣式，則按鈕會顯示在箭號的下拉式功能表中。 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">第6版</a>。 此樣式需要將工具列雙重緩衝。 雙重緩衝是一種機制，可偵測工具列何時變更。 <br/>
<blockquote>
[!Note]<br />
Comctl32.dll 第6版不是可轉散發套件，但包含在 Windows 或更新版本中。 若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。 如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">版本 5.81</a>。 此樣式可讓您設定所有按鈕的文字，但只會顯示具有 [ <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> ] 按鈕樣式的按鈕。 您也必須設定 <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> 的樣式。 一般來說，當按鈕未顯示文字時，您的應用程式必須處理 <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> 或 <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> ，才能顯示工具提示。 使用 TBSTYLE_EX_MIXEDBUTTONS 擴充樣式，已設定但未顯示在按鈕上的文字將會自動做為按鈕的工具提示文字使用。 如果您的應用程式需要更多的彈性來指定工具提示文字，則只需要處理 TBN_GETINFOTIP 或 TTN_GETDISPINFO。 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">版本 5.82</a>。 <strong>適用于內部用途;不建議在應用程式中使用。</strong> 此樣式可讓工具列成為垂直方向，並將工具列按鈕組織成資料行。 按鈕會垂直往下傳送，直到按鈕超過工具列的周框高度為止 (請參閱 <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) ，然後再建立新的資料行。 工具列會以這種方式來流動按鈕，直到所有按鈕都定位為止。 若要使用這個樣式，也必須設定 TBSTYLE_EX_VERTICAL 的樣式。 <br/>
<blockquote>
[!Note]<br />
未來的 Comctl32.dll 版本可能不支援這個樣式。 此外，這個樣式不會在 commctrl 中定義。 將下列定義新增至您應用程式的原始程式檔，以使用此樣式： <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">版本 5.82</a>。 <strong>適用于內部用途;不建議在應用程式中使用。</strong> 此樣式可讓工具列成為垂直方向。 工具列按鈕是從上到下，而不是水準方向。 <br/>
<blockquote>
[!Note]<br />
未來的 Comctl32.dll 版本可能不支援這個樣式。 此外，這個樣式不會在 commctrl 中定義。 將下列定義新增至您應用程式的原始程式檔，以使用此樣式： <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

若要設定擴充樣式，請將 [工具列] 控制項傳送至 [ [**TB] \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) 訊息。 若要判斷目前設定的擴充樣式，請傳送 [**TB 的 \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





