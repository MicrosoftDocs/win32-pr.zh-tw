---
title: 'EM_GETEDITSTYLE 訊息 (Richedit .h) '
description: 抓取目前的編輯樣式旗標。
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025211"
---
# <a name="em_geteditstyle-message"></a>EM \_ GETEDITSTYLE 訊息

抓取目前的編輯樣式旗標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回目前的編輯樣式旗標，其中可包含下列一或多個值：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>傳回碼</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>SES_BEEPONMAXTEXT</strong></dt> </dl></td>
<td>如果使用者嘗試輸入的字元數超過最大值，Rich Edit 將會呼叫系統 beeper。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>開啟雙向處理。 如果下列任一視窗樣式為作用中，就會自動開啟此功能： <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>、 <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>。 不過，使用 <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> 的自訂執行時，這項設定適用于處理這些視窗樣式 (預設值： 0) 。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>WINDOWS XP （含 SP1</strong>）：允許使用 TSF 插入內嵌物件 (預設值： 0) 。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>WINDOWS XP （含 SP1</strong>）：允許 TSF 的校對提示 (預設值： 0) 。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>WINDOWS XP （含 SP1</strong>）：允許 TSF 的智慧標籤提示 (預設值： 0) 。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：不允許 TSF 鎖定讀取/寫入存取。 這會暫停 TSF 輸入。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：使用預設 OpenType 功能來顯示具有 wi-fi 連字的字型，以產生改良的印刷樣式 (預設值： 0) 。 <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>WINDOWS XP （含 SP1</strong>）：使用草稿模式字型來顯示文字。 草稿模式是一個協助工具選項，可讓控制項顯示具有單一字型的文字;字型是由訊息方塊中所使用之字型的系統設定所決定。 例如，可存取的使用者可以更輕鬆地讀取文字，而不是將字型和樣式混合 (預設值： 0) 。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：模擬 RichEdit 1.0 行為。 <br/>
<blockquote>
[!Note]<br />
如果您真的想要此行為，請使用 Windows riched32.dll，而不是 riched20.dll 或 msftedit.dll。 Riched32.dll 有更多功能。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>當這個位開啟時，豐富的編輯會嘗試模擬系統編輯控制項 (預設值： 0) 。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>將背景色彩全部延伸至用戶端矩形的邊緣 (預設值： 0) 。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>WINDOWS XP （含 SP1</strong>）：如果資料表格線的寬度為零，則不會顯示格線。 這相當於 Word 的 [表格] 功能表中的 [隱藏格線] 功能 (預設值： 0) 。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：當游標停留在連結上時，會顯示具有目標連結位址的工具提示 (預設值： 0) 。 <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：提供邏輯插入號資訊，而不是插入號點陣圖，如 <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost：： TxSetCaretPos</strong></a> (default： 0) 所述。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_LOWERCASE</strong></dt> </dl></td>
<td>將所有輸入字元轉換成小寫 (預設值： 0) 。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_MAPCPS</strong></dt> </dl></td>
<td>已過時。 請勿使用。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_MULTISELECT</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：啟用多重選取，並在按下 Ctrl 鍵時進行個別選取 (預設： 0) 。 <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：不要調整東亞文字的行高 (預設值：0，將行高調整為 15% ) 。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>從沒有焦點的連結傳送 <a href="en-link.md">EN_LINK</a> 通知。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>不允許這個 rich edit 控制項實例的 Ime (預設值： 0) 。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>當這個位開啟時，rich edit 不會驗證輸入文字的順序。 某些語言 (例如泰文和越南) 需要先驗證輸入順序，再將它提交至備份存放區 (預設值： 0) 。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>發生 KillFocus 時，請將文字的開頭 (字元位置等於 0)  (預設值： 0) 。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：在卸載文字 (預設值： 0) 時，根據內容新增或刪除空格。 <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>已過時。 請勿使用。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>：如果 [word 選取] 為 [使用中]，請確定放置位置位於單字界限 (預設值： 0) 。 <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>將所有輸入字元轉換成大寫 (預設值： 0) 。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>使用隨附于 Internet Explorer 4.0 或更新版本的主動式 IMM 輸入方法元件 (預設值： 0) 。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>WINDOWS XP （含 SP1</strong>）：使用 @ 字型，其設計目的為垂直文字;這會與 <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> 視窗樣式搭配使用。 @ 字型的名稱是以 @ 符號開頭，例如 &quot; @Batang &quot; (預設值：0，但是會自動開啟垂直文字配置) 。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>WINDOWS XP （含 SP1</strong>）：開啟 TSF 支援。  (預設值： 0) <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>開啟將 CRCRLFs 轉譯為 CRs。 當這個位開啟且已讀取檔案時，CRCRLF 的所有實例都會在內部轉換成硬性 CRs。 這會影響文字換行。 請注意，如果這類檔案儲存為純文字，則 CRs 將會被 CRLFs 取代。 這是純文字的 .txt 標準 (預設值：0，會刪除輸入) 上的 CRCRLFs。 <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETEDITSTYLE**](em-seteditstyle.md)
</dt> </dl>

 

