---
title: 自訂控制項
description: 本節包含應用程式定義或自訂控制項的相關資訊。
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d1a31a44f1f71d99088f7729c2de6d5fdb597e14507f5f994dfaca1b96613d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059708"
---
# <a name="custom-controls"></a>自訂控制項

本節包含應用程式定義或自訂控制項的相關資訊。

討論下列主題。

-   [建立 Owner-Drawn 控制項](#creating-owner-drawn-controls)
-   [子類別化現有控制項的視窗類別](#subclassing-the-window-class-of-an-existing-control)
-   [執行 Application-Defined 視窗類別](#implementing-an-application-defined-window-class)
-   [從控制項傳送通知](#sending-notifications-from-a-control)
-   [協助工具](#accessibility)
-   [相關主題](#related-topics)

## <a name="creating-owner-drawn-controls"></a>建立 Owner-Drawn 控制項

您可以使用主控描繪樣式旗標來建立按鈕、功能表、靜態文字控制項、清單方塊和下拉式方塊。 當控制項具有主控描繪的樣式時，系統會像往常一樣處理使用者與控制項的互動，執行這類工作，像是在使用者選擇按鈕和通知按鈕的事件擁有者時偵測。 不過，因為控制項是主控描繪的，所以控制項的父視窗會負責控制項的視覺外觀。 每次必須繪製控制項時，父視窗就會收到訊息。

若為按鈕和靜態文字控制項，擁有者繪製的樣式會影響系統繪製整個控制項的方式。 針對清單方塊和下拉式方塊，父視窗會繪製控制項內的專案，而控制項則會繪製自己的外框。 例如，應用程式可以自訂清單方塊，使其在清單中的每個專案旁顯示一個小點陣圖。

下列範例程式碼顯示如何建立主控描繪的靜態文字控制項。 假設已定義 Unicode。


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



在下列範例中，從包含在上一個範例中所建立之控制項之對話方塊的視窗程式中，會使用預設字型以自訂色彩顯示文字來處理 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。 請注意，您不需要在處理 **WM \_ DRAWITEM** 時呼叫 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint)和 [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) 。


```
case WM_DRAWITEM:
{
    LPDRAWITEMSTRUCT pDIS = (LPDRAWITEMSTRUCT)lParam;
    if (pDIS->hwndItem == g_myStatic)
    {
        SetTextColor(pDIS->hDC, RGB(100, 0, 100));
        WCHAR staticText[99];
        int len = SendMessage(myStatic, WM_GETTEXT, 
            ARRAYSIZE(staticText), (LPARAM)staticText);
        TextOut(pDIS->hDC, pDIS->rcItem.left, pDIS->rcItem.top, staticText, len);
    }
    return TRUE;
}
```



如需主控描繪控制項的詳細資訊，請參閱建立主控描繪 [清單方塊](using-list-boxes.md) 和 [擁有者繪製](about-combo-boxes.md)的下拉式方塊。

## <a name="subclassing-the-window-class-of-an-existing-control"></a>子類別化現有控制項的視窗類別

將現有控制項子類別化是另一種建立自訂控制項的方式。 子類別程式可以藉由處理影響所選行為的訊息，來改變控制項的選取行為。 所有其他訊息都會傳遞至控制項的原始視窗程式。 例如，應用程式可以將控制項子類別化並處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，以在唯讀、單行編輯控制項中的文字旁邊顯示小型點陣圖。 如需詳細資訊，請參閱 [關於視窗程式](/windows/desktop/winmsg/about-window-procedures) 和子類別化 [控制項](subclassing-overview.md)。

## <a name="implementing-an-application-defined-window-class"></a>執行 Application-Defined 視窗類別

若要建立未根據現有控制項明確地建立的控制項，應用程式必須建立並註冊視窗類別。 註冊自訂控制項之應用程式定義視窗類別的程式，與註冊一般視窗的類別相同。 若要建立自訂控制項，請在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數或對話方塊範本中指定視窗類別的名稱。 每個類別都必須有唯一的名稱、對應的視窗程式和其他資訊。

視窗程式至少會繪製控制項。 如果應用程式使用控制項來讓使用者輸入資訊，則視窗程式也會處理鍵盤和滑鼠的輸入訊息，並將通知訊息傳送至父視窗。 此外，如果控制項支援控制訊息，則視窗程式會處理由父視窗或其他視窗傳送給它的訊息。 例如，控制項通常會處理由對話方塊傳送的 [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) 訊息，以指示對話方塊以指定的方式處理鍵盤輸入。

如果訊息影響控制項的操作，則應用程式定義控制項的視窗程式應處理下表中任何預先定義的控制訊息。



| 訊息                                          | 建議                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)       | 如果控制項使用 ENTER、ESC、TAB 或方向鍵，則為進程。 [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea)函式會將此訊息傳送給對話方塊中的控制項，以判斷是否要處理索引鍵或將它們傳遞給控制項。 |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)             | 如果同時處理了 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息，則為進程。                                                                                                                                                                  |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)             | 如果控制項文字與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數所指定的標題不同，則為進程。                                                                                                                 |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) | 如果控制項文字與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數所指定的標題不同，則為進程。                                                                                                                 |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)       | 如果控制項顯示插入號、焦點矩形或另一個專案，表示它有輸入焦點，則為 [進程]。                                                                                                                            |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)         | 如果控制項顯示插入號、焦點矩形或另一個專案，表示它有輸入焦點，則為 [進程]。                                                                                                                            |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)             | 如果控制項文字與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數所指定的標題不同，則為進程。                                                                                                                 |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)             | 如果控制項顯示文字，則為進程。 當您建立具有 DS SETFONT 樣式的對話方塊時，系統會傳送此訊息 \_ 。                                                                                                                  |



 

應用程式定義的控制項訊息是特定的控制項，而且必須使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 或 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) 函式明確地傳送給控制項。 每個訊息的數值都必須是唯一的，且不能與其他視窗訊息的值衝突。 為了確保應用程式定義的訊息值不會衝突，應用程式應該將唯一的數位新增至 [**WM \_ 使用者**](/windows/desktop/winmsg/wm-user) 值，以建立每個值。

## <a name="sending-notifications-from-a-control"></a>從控制項傳送通知

可能需要自訂控制項才能將事件通知傳送至父視窗，讓主應用程式可以回應這些事件。 例如，自訂清單視圖可能會在使用者選取專案時傳送通知，而當按兩下專案時，可能會傳送另一則通知。

通知會以 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 或 [**wm \_ 通知**](wm-notify.md) 訊息的形式傳送。 **WM \_通知** 訊息會包含超過 **WM \_ 命令** 訊息的資訊。

控制項識別碼是應用程式用來識別傳送訊息之控制項的唯一數位。 應用程式會在建立控制項時，設定控制項的識別碼。 應用程式會在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函數的 *HMenu* 參數或 [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex)結構的 **id** 成員中指定識別碼。

因為控制項本身不會設定控制項識別碼，所以控制項必須先取得識別碼，然後才能傳送通知訊息。 控制項必須使用 [**GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) 函式來取出其本身的控制項識別碼。 雖然控制項識別碼是在控制項建立時指定為功能表控制碼，但無法使用 [**GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) 函式來取得識別碼。 或者，當處理 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息時，控制項可以從 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構中的 **hMenu** 成員取得識別碼。

下列範例，其中 *hwndControl* 是控制視窗的控制碼，而 CN \_ VALUECHANGED 是自訂通知定義，會顯示傳送控制項特定通知的兩種方式。


```
 // Send as WM_COMMAND.
SendMessage(GetParent(hwndControl), 
    WM_COMMAND,
    MAKEWPARAM(GetDlgCtrlID(hwndControl), CN_VALUECHANGED),
    (LPARAM)hwndControl);

// Send as WM_NOTIFY.           
NMHDR nmh;
nmh.code = CN_VALUECHANGED;
nmh.idFrom = GetDlgCtrlID(hwndControl);
nmh.hwndFrom = hwndControl;
SendMessage(GetParent(hwndControl), 
    WM_NOTIFY, 
    (WPARAM)hwndControl, 
    (LPARAM)&nmh);
```



請注意， [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構可以是包含其他資訊之大型控制項定義結構的一部分。 在此範例中，控制項的舊值和新值可能包含在此結構中。  (這類擴充結構用於許多標準通知;例如，請參閱使用 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的 [LVN \_ INSERTITEM](lvn-insertitem.md)。 ) 

## <a name="accessibility"></a>協助工具選項

所有的通用控制項都支援 Microsoft Active Accessibility (MSAA) ，可讓您以程式設計方式存取螢幕讀取器之類的可存取技術應用程式。 MSAA 也可讓消費者介面自動化（較新的技術）與控制項互動。

自訂控制項應該執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面 (，以支援 MSAA) 或消費者介面自動化介面，或兩者都支援。 否則，可存取的技術產品將只能取得控制項視窗的極有限資訊、無法存取控制項的屬性，而且將無法在控制項中觸發事件。

如需讓控制項可供存取的詳細資訊，請參閱[Windows Automation API](/windows/desktop/WinAuto/windows-automation-api-portal)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[一般控制項參考](common-control-reference.md)
</dt> <dt>

[使用自訂繪圖自訂控制項的外觀](custom-draw.md)
</dt> <dt>

[控制訊息](control-messages.md)
</dt> <dt>

[搭配 Owner-Drawn 控制項使用視覺化樣式](using-visual-styles.md)
</dt> </dl>

 

 