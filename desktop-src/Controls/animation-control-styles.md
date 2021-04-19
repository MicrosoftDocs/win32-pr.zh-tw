---
title: '動畫控制項樣式 (CommCtrl .h) '
description: 此區段會列出與動畫控制項搭配使用的視窗樣式。
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976053"
---
# <a name="animation-control-styles"></a>動畫控制項樣式

此區段會列出與動畫控制項搭配使用的視窗樣式。



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
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <dt><strong>ACS_AUTOPLAY</strong></dt> </dl></td>
<td style="text-align: left;">當 AVI 剪輯開啟時，就會立即開始播放動畫。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <dt><strong>ACS_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">在動畫控制項的視窗中將動畫置中。 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <dt><strong>ACS_TIMER</strong></dt> </dl></td>
<td style="text-align: left;">根據預設，控制項會建立執行緒來播放 AVI 剪輯。 如果設定此旗標，控制項會在不建立執行緒的情況下播放剪輯;在內部，控制項會使用 Win32 計時器來同步播放。 <br/> <strong>Comctl32.dll 第6版和更新版本：</strong> 不支援這個樣式。 依預設，此控制項會在不建立執行緒的情況下，播放 AVI 剪輯。<br/>
<blockquote>
[!Note]<br />
Comctl32.dll 第6版無法轉散發。 若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。 如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <dt><strong>ACS_TRANSPARENT</strong></dt> </dl></td>
<td style="text-align: left;">可讓您將動畫的背景色彩與基礎視窗的色彩進行比對，以建立 &quot; 透明 &quot; 背景。 動畫控制項的父系不能有 WS_CLIPCHILDREN 樣式 (請參閱 <a href="/windows/desktop/winmsg/window-styles">視窗樣式</a>) 。 控制項會將 <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> 訊息傳送到其父系。 使用 <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> 將裝置內容的背景色彩設定為適當的值。 控制項會將第一個框架的左上角圖元解釋為動畫的預設背景色彩。 它會將該色彩的所有圖元重新對應到您在回應 WM_CTLCOLORSTATIC 時所提供的值。 <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



