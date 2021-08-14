---
title: 狀態列
description: 本章節包含與狀態列控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1be3ea518b63118fc80b02b382943c40ba2fd13b15713488b351b5d6cc827e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696488"
---
# <a name="status-bar"></a>狀態列

本章節包含與狀態列控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                          | 目錄                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [狀態列](status-bars.md) | *狀態列* 是父視窗底部的水準視窗，其中應用程式可以顯示各種類型的狀態資訊。<br/> |



 

### <a name="functions"></a>函式



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>目錄</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></td>
<td>建立狀態視窗，通常用來顯示應用程式的狀態。 視窗通常會出現在父視窗的底部，並且包含指定的文字。
<blockquote>
[!Note]<br />
此函式已過時。 請改用 <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> 。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></td>
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a>函式會以具有框線的狀態視窗樣式來繪製指定文字。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></td>
<td>處理 <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> 和 <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> 訊息，並在指定的狀態視窗中顯示目前功能表的解說文字。<br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>訊息



| 主題                                               | 目錄                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SB \_ GETBORDERS**](sb-getborders.md)             | 抓取狀態視窗水準和垂直框線的目前寬度。 <br/>                                                                                                  |
| [**SB \_ GETICON**](sb-geticon.md)                   | 抓取狀態列中元件的圖示。 <br/>                                                                                                                                           |
| [**SB \_ GETPARTS**](sb-getparts.md)                 | 捕獲狀態視窗中的部分計數。 此訊息也會抓取指定之部分數目的右邊緣座標。 <br/>                                         |
| [**SB \_ GETRECT**](sb-getrect.md)                   | 抓取狀態視窗中某部分的周框。 <br/>                                                                                                                           |
| [**SB \_ GETTEXT**](sb-gettext.md)                   | [**SB \_ GETTEXT**](sb-gettext.md)訊息會從狀態視窗的指定部分抓取文字。 <br/>                                                                             |
| [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)       | [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)訊息會從狀態視窗的指定部分抓取文字的長度（以字元為單位）。 <br/>                                   |
| [**SB \_ GETTIPTEXT**](sb-gettiptext.md)             | 抓取狀態列中某部分的工具提示文字。 您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。 <br/>         |
| [**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md) | 抓取控制項的 Unicode 字元格式旗標。 <br/>                                                                                                                             |
| [**SB \_ ISSIMPLE**](sb-issimple.md)                 | 檢查狀態列控制項是否為簡單模式。 <br/>                                                                                                                        |
| [**SB \_ SETBKCOLOR**](sb-setbkcolor.md)             | 設定狀態列中的背景色彩。 <br/>                                                                                                                                               |
| [**SB \_ SETICON**](sb-seticon.md)                   | 設定狀態列中元件的圖示。 <br/>                                                                                                                                                |
| [**SB \_ SETMINHEIGHT**](sb-setminheight.md)         | 設定狀態視窗之繪圖區域的最小高度。 <br/>                                                                                                                               |
| [**SB \_ SETPARTS**](sb-setparts.md)                 | 設定狀態視窗中的部分數目，以及每個元件右邊緣的座標。 <br/>                                                                                           |
| [**SB \_ SETTEXT**](sb-settext.md)                   | SB \_ SETTEXT 訊息會在狀態視窗的指定部分設定文字。<br/>                                                                                                           |
| [**SB \_ SETTIPTEXT**](sb-settiptext.md)             | 設定狀態列中某部分的工具提示文字。 您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。<br/>        |
| [**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md) | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 <br/> |
| [**SB \_ 簡單**](sb-simple.md)                     | 指定狀態視窗是否顯示簡單文字，或顯示先前 [**SB \_ SETPARTS**](sb-setparts.md) 訊息所設定的所有視窗元件。 <br/>                                       |



 

### <a name="notifications"></a>通知



| 主題                                                 | 目錄                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ 按一下 (狀態列) ](nm-click-status-bar.md)     | 通知狀態列控制項的父視窗，使用者在控制項內按一下滑鼠左鍵。 [NM \_按一下 [ (狀態列](nm-click-status-bar.md) ]，) 以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>              |
| [NM \_ DBLCLK (狀態列) ](nm-dblclk-status-bar.md)   | 通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                       |
| [NM \_ RCLICK (狀態列) ](nm-rclick-status-bar.md)   | 通知狀態列控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                             |
| [NM \_ RDBLCLK (狀態列) ](nm-rdblclk-status-bar.md) | 通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 [NM \_RDBLCLK (狀態列)](nm-rdblclk-status-bar.md) 會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/> |
| [SBN \_ SIMPLEMODECHANGE](sbn-simplemodechange.md)     | 當簡單模式因為 [**SB \_ 簡單**](sb-simple.md) 訊息而變更時，由狀態列控制項傳送。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                        |



 

### <a name="constants"></a>常數



| 主題                                      | 目錄                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [狀態列樣式](status-bar-styles.md) | 除了由 *狀態列* 控制項支援的標準視窗樣式之外，本節還會列出樣式。 <br/> |



 

 

