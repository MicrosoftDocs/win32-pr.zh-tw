---
title: 'WM_SYSCOMMAND 訊息 (Winuser .h) '
description: 當使用者選擇 [視窗])  (功能表中的命令時，如果使用者選擇 [最大化] 按鈕、[最小化] 按鈕、[還原] 按鈕或 [關閉] 按鈕，就會收到此訊息。
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978420"
---
# <a name="wm_syscommand-message"></a>WM \_ SYSCOMMAND 訊息

當使用者選擇 [ **視窗]**)  (功能表中的命令時，如果使用者選擇 [最大化] 按鈕、[最小化] 按鈕、[還原] 按鈕或 [關閉] 按鈕，就會收到此訊息。


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a>範例

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) 取得的範例。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要求的系統命令類型。 此參數可以是下列其中一個值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </dl></td>
<td>關閉視窗。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </dl></td>
<td>將游標變更為具有指標的問號。 如果使用者接著按一下對話方塊中的控制項，控制項就會收到 <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> 的訊息。<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </dl></td>
<td>選取預設專案;使用者按兩下 [視窗] 功能表。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </dl></td>
<td>啟用與應用程式指定之熱鍵相關聯的視窗。 <em>LParam</em>參數會識別要啟動的視窗。<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </dl></td>
<td>水準滾動。<br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </dl></td>
<td>指出螢幕保護裝置是否安全。 <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </dl></td>
<td>以按鍵的結果形式抓取視窗功能表。 如需詳細資訊，請參閱＜備註＞一節。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </dl></td>
<td>將視窗最大化。<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </dl></td>
<td>將視窗最小化。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </dl></td>
<td>設定顯示器的狀態。 此命令支援具有省電功能的裝置，例如電池供電的個人電腦。 <br/> <em>LParam</em>參數可以有下列值：<br/>
<ul>
<li>-1 (顯示器開啟電源) </li>
<li>1 (顯示器會進入低電源) </li>
<li>2 (正在關閉顯示) </li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </dl></td>
<td>以滑鼠點擊的結果形式抓取視窗功能表。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </dl></td>
<td>移動視窗。<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </dl></td>
<td>移至下一個視窗。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </dl></td>
<td>移至上一個視窗。<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </dl></td>
<td>將視窗還原成其正常位置和大小。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </dl></td>
<td>執行 System.ini 檔案的 [boot] 區段中指定的螢幕保護裝置應用程式。<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </dl></td>
<td>調整視窗的大小。<br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </dl></td>
<td>啟用 [ <strong>開始</strong> ] 功能表。<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </dl></td>
<td>垂直捲動。<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字會指定游標的水準位置（在螢幕座標中），如果已選擇使用滑鼠的視窗功能表命令。 否則，就不會使用此參數。

高序位單字會指定游標的垂直位置（在螢幕座標中），如果使用滑鼠來選擇視窗功能表命令，則為。 如果使用系統加速器選擇命令，此參數為1，如果使用助憶鍵，則為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

若要取得螢幕座標中的位置座標，請使用下列程式碼：


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會針對上表中指定的預先定義動作，執行視窗功能表要求。

在 **WM \_ SYSCOMMAND** 訊息中，系統會在內部使用 *wParam* 參數的四個低序位位。 若要在測試 *wParam* 的值時取得正確的結果，應用程式必須使用位 and 運算子，將值0XFFF0 與 *wParam* 值結合。

您可以使用 [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)、 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)、 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)、 [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)、 [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)和 [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) 函數來修改視窗功能表中的功能表項目。 修改視窗功能表的應用程式必須處理 **WM \_ SYSCOMMAND** 訊息。

應用程式可以在任何時間執行任何系統命令，方法是將 **WM \_ SYSCOMMAND** 訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。 應用程式未處理的任何 **WM \_ SYSCOMMAND** 訊息都必須傳遞至 **DefWindowProc**。 應用程式所新增的任何命令值都必須由應用程式處理，而且無法傳遞至 **DefWindowProc**。

如果原則啟用密碼保護，則不論應用程式如何使用 **SC \_ SCREENSAVE** 通知，即使無法將它傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，也會啟動畫面保護。

定義為從 [視窗] 功能表選擇專案的快速鍵會轉譯成 **wm \_ SYSCOMMAND** 訊息; 所有其他快速鍵按鍵都會轉譯成 [**wm \_ 命令**](wm-command.md) 訊息。

如果 *wParam* 是 **SC \_ KEYMENU**， *lParam* 就會包含用來顯示快顯功能表的 ALT 鍵的字元碼。 例如，按 ALT + F 顯示檔案快顯視窗，會導致 *wParam* 等於 **SC \_ KEYMENU** 且 *LParam* 等於 ' F ' 的 **WM \_ SYSCOMMAND** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**取得 \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**WM \_ 命令**](wm-command.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

