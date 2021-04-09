---
title: '對話方塊 (對話方塊) '
description: 本節討論對話方塊。 對話方塊是應用程式建立以抓取使用者輸入的暫存視窗。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\dialogboxes.htm
keywords:
- 使用者介面，對話方塊
- 對話方塊，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14db9d7e5543bcab9c3b004695e3367d464a3529
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933839"
---
# <a name="dialog-boxes-dialog-boxes"></a>對話方塊 (對話方塊) 

對話方塊是應用程式建立以抓取使用者輸入的暫存視窗。 應用程式通常會使用對話方塊來提示使用者輸入功能表項目的其他資訊。 對話方塊通常會包含一或多個控制項 (子視窗) 使用者輸入文字、選擇選項或指示動作。

Windows 也提供預先定義的對話方塊，支援一般功能表項目，例如 [ **開啟** ] 和 [ **列印**]。 使用這些功能表項目的應用程式應該使用通用對話方塊來提示輸入此使用者，不論應用程式類型為何。

### <a name="in-this-section"></a>本節內容



| Name                                                                           | 描述                                                                                     |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [關於對話方塊](about-dialog-boxes.md)                                   | 討論如何在應用程式的使用者介面中使用對話方塊。<br/>            |
| [對話方塊程式設計考量](dlgbox-programming-considerations.md) | 本總覽討論一些有關對話方塊的程式設計考慮。<br/>     |
| [使用對話方塊](using-dialog-boxes.md)                                   | 您可以使用對話方塊來顯示資訊，並提示使用者輸入。<br/>      |
| [對話方塊參考](dialog-box-reference.md)                               | API 參考<br/>                                                                    |
| [通用對話方塊程式庫](common-dialog-box-library.md)                     | 討論如何在應用程式的使用者介面中使用通用對話方塊。<br/> |



 

### <a name="dialog-box-functions"></a>對話方塊函式



| Name                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga)                           | 從對話方塊範本資源建立非強制回應對話方塊。<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)           | 從記憶體中的對話方塊範本建立非強制回應對話方塊。<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) | 從記憶體中的對話方塊範本建立非強制回應對話方塊。 在顯示對話方塊之前，函數會將應用程式定義的值傳遞至對話方塊程式，做為 [**WM \_ INITDIALOG**](wm-initdialog.md)訊息的 *lParam* 參數。 應用程式可以使用這個值來初始化對話方塊控制項。 <br/>                                                                                           |
| [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)                 | 從對話方塊範本資源建立非強制回應對話方塊。 在顯示對話方塊之前，函數會將應用程式定義的值傳遞至對話方塊程式，做為 [**WM \_ INITDIALOG**](wm-initdialog.md)訊息的 *lParam* 參數。 應用程式可以使用這個值來初始化對話方塊控制項。 <br/>                                                                                            |
| [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)                               | 呼叫預設對話方塊視窗程式，為具有私用視窗類別的對話方塊沒有處理的任何視窗訊息提供預設處理。 <br/>                                                                                                                                                                                                                                                                 |
| [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa)                                 | 從對話方塊範本資源建立強制回應對話方塊。 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 不會傳回控制權，直到指定的回呼函式藉由呼叫 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函數來結束強制回應對話方塊。<br/>                                                                                                                                                                                 |
| [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)                 | 從記憶體中的對話方塊範本建立強制回應對話方塊。 [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) 不會傳回控制權，直到指定的回呼函式藉由呼叫 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函數來結束強制回應對話方塊。<br/>                                                                                                                                                                |
| [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)       | 從記憶體中的對話方塊範本建立強制回應對話方塊。 在顯示對話方塊之前，函數會將應用程式定義的值傳遞至對話方塊程式，做為 [**WM \_ INITDIALOG**](wm-initdialog.md)訊息的 *lParam* 參數。 應用程式可以使用這個值來初始化對話方塊控制項。 <br/>                                                                                              |
| [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)                       | 從對話方塊範本資源建立強制回應對話方塊。 在顯示對話方塊之前，函數會將應用程式定義的值傳遞至對話方塊程式，做為 [**WM \_ INITDIALOG**](wm-initdialog.md)訊息的 *lParam* 參數。 應用程式可以使用這個值來初始化對話方塊控制項。 <br/>                                                                                               |
| [*DialogProc*](/windows/win32/api/winuser/nc-winuser-dlgproc)                                 | 應用程式定義的回呼函式，搭配 [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) 和 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 系列的函式使用。 它會處理傳送至強制回應或非強制回應對話方塊的訊息。 **DLGPROC** 型別定義此回呼函數的指標。 [*DialogProc*](/windows/win32/api/winuser/nc-winuser-dlgproc) 是應用程式定義函數名稱的預留位置。 <br/>                                                    |
| [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog)                                 | 終結強制回應對話方塊，使系統結束對話方塊的任何處理。<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits)               | 抓取系統的對話方塊基礎單位，這是系統字型中字元的平均寬度和高度。 針對使用系統字型的對話方塊，您可以使用這些值來轉換對話方塊範本單位（如對話方塊範本中所指定）和圖元。 針對不使用系統字型的對話方塊，從對話方塊範本單位到圖元的轉換取決於對話方塊使用的字型。<br/> |
| [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid)                           | 抓取指定之控制項的識別碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem)                               | 在指定的對話方塊中，抓取控制項的控制碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint)                         | 將對話方塊中指定之控制項的文字轉譯成整數值。 <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta)                       | 擷取對話方塊中控制項相關聯的標題或文字。 <br/>                                                                                                                                                                                                                                                                                                                                                              |
| [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem)             | 抓取控制項群組中第一個控制項的控制碼，這些控制項在 (或之後) 在對話方塊中的指定控制項之前。 <br/>                                                                                                                                                                                                                                                                                                    |
| [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem)                 | 抓取具有 **WS \_ TABSTOP** 樣式的第一個控制項的控制碼，該控制項之前 (或之後) 指定的控制項。 <br/>                                                                                                                                                                                                                                                                                                        |
| [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea)                     | 判斷訊息是否適用于指定的對話方塊，如果是，則會處理訊息。 <br/>                                                                                                                                                                                                                                                                                                                         |
| [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)                         | 將指定的對話方塊單位轉換為螢幕單位 (圖元) 。 此函式會將指定的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構中的座標取代為已轉換的座標，讓您可以使用結構來建立對話方塊或將控制項放置在對話方塊中。 <br/>                                                                                                                                     |
| [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox)                               | 顯示模式對話方塊，其中包含系統圖示、一組按鈕，以及簡短的應用程式特定訊息，例如狀態或錯誤資訊。 訊息方塊會傳回整數值，指出使用者所按的按鈕。<br/>                                                                                                                                                                                     |
| [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)                           | 建立、顯示及操作訊息方塊。 訊息方塊包含應用程式定義的訊息和標題，以及預先定義的圖示和推送按鈕的任何組合。 按鈕是以系統使用者介面的語言來進行。 <br/>                                                                                                                                                                                          |
| [**MessageBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-messageboxindirecta)               | 建立、顯示及操作訊息方塊。 訊息方塊包含應用程式定義郵件內文和標題、任何圖示，以及任何預先定義之推播按鈕的組合。<br/>                                                                                                                                                                                                                                                        |
| [**SendDlgItemMessage**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea)               | 在對話方塊中，將訊息傳送至指定的控制項。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**SetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint)                         | 將對話方塊中控制項的文字設定為指定整數值的字串表示。 <br/>                                                                                                                                                                                                                                                                                                                               |
| [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta)                       | 在對話方塊中設定控制項的標題或文字。 <br/>                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="dialog-box-messages"></a>對話方塊訊息



| Name                                    | 描述                                                                                                                                                                                                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ GETDEFID**](dm-getdefid.md)     | 抓取對話方塊的預設按鈕控制項識別碼。 <br/>                                                                                                                           |
| [**DM 重新 \_ 定位**](dm-reposition.md) | 重新置放最上層對話方塊，使其符合桌面上的範圍。 應用程式可以在調整大小後將此訊息傳送至對話方塊，以確保整個對話方塊保持可見。<br/> |
| [**DM \_ SETDEFID**](dm-setdefid.md)     | 變更對話方塊的預設按鈕的識別碼。 <br/>                                                                                                                                     |



 

### <a name="dialog-box-notifications"></a>對話方塊通知



| Name                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) | 在系統繪製對話方塊之前，傳送至對話方塊。 藉由回應此訊息，對話方塊可以使用指定的顯示裝置內容控制碼來設定其文字和背景色彩。 <br/>                                                                                                                                                                                       |
| [**WM \_ ENTERIDLE**](wm-enteridle.md)     | 傳送至進入閒置狀態之強制回應對話方塊或功能表的擁有者視窗。 強制回應對話方塊或功能表在處理一或多個先前的訊息之後，就會進入閒置狀態，當佇列中沒有任何訊息在佇列中等候時。 <br/>                                                                                                                                                     |
| [**WM \_ GETDLGCODE**](wm-getdlgcode.md)   | 傳送至與控制項相關聯的視窗程式。 根據預設，系統會處理所有鍵盤輸入至控制項;系統會將特定類型的鍵盤輸入視為對話方塊流覽鍵。 若要覆寫此預設行為，控制項可以回應 [**WM \_ GETDLGCODE**](wm-getdlgcode.md) 訊息，以指出它所要處理的輸入類型。<br/> |
| [**WM \_ INITDIALOG**](wm-initdialog.md)   | 在對話方塊顯示之前，立即傳送至對話方塊程式。 對話方塊程式通常會使用這個訊息來初始化控制項，並執行任何其他會影響對話方塊外觀的初始作業。 <br/>                                                                                                                                          |
| [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md)   | 傳送至對話方塊程式，將鍵盤焦點設定至對話方塊中的不同控制項。 <br/>                                                                                                                                                                                                                                                                                         |



 

### <a name="dialog-box-structures"></a>對話方塊結構



| Name                                           | 描述                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate)     | 在對話方塊中定義控制項的維度和樣式。 其中一或多個結構會與 [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) 結構結合，以形成對話方塊的標準範本。 <br/>                                                                                                                                   |
| [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) | 描述擴充的對話方塊。 如需延伸對話方塊範本格式的描述，請參閱 [**DLGTEMPLATEEX**](dlgtemplateex.md)。<br/>                                                                                                                                                                                                |
| [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate)             | 定義對話方塊的維度和樣式。 此結構（一律為對話方塊的標準範本中的第一個）也會指定對話方塊中的控制項數目，因此會指定範本中後續 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構的數目。 <br/>                                     |
| [**DLGTEMPLATEEX**](dlgtemplateex.md)         | 擴充的對話方塊範本以描述對話方塊的 **DLGTEMPLATEEX** 標頭開頭，並在對話方塊中指定控制項數目。 針對對話方塊中的每個控制項，擴充的對話方塊範本都有一個使用 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 格式來描述控制項的資料區塊。 <br/> |
| [**MSGBOXPARAMS**](/windows/win32/api/winuser/ns-winuser-msgboxparamsa)           | 包含用來顯示訊息方塊的資訊。 [**MessageBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-messageboxindirecta)函式會使用此結構。<br/>                                                                                                                                                                                                           |



 

 

