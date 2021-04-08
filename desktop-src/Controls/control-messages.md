---
title: 控制訊息
description: 本章節包含如何使用 Windows 訊息與控制項通訊的相關資訊。
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842944"
---
# <a name="control-messages"></a>控制訊息

本章節包含如何使用 Windows 訊息與控制項通訊的相關資訊。

討論下列主題。

-   [傳送至通用控制項的訊息](#messages-to-common-controls)
-   [來自控制項的通知](#notifications-from-controls)
-   [相關主題](#related-topics)

## <a name="messages-to-common-controls"></a>傳送至通用控制項的訊息

由於通用控制項是 windows，因此應用程式可以使用常見的 Microsoft Win32 訊息（例如 [**wm \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) 或 [**wm \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)）來與其通訊。 此外，每個通用控制項的視窗類別都支援一組控制項特定的訊息。 一般而言，應用程式會使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 或 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) 將訊息傳遞至控制項， (通常會在傳回值) 中接收資訊。

某些常見的控制項也有一組可供應用程式使用的宏，而不是 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)。 這些宏通常比函數更容易使用。 下列範例程式碼會先使用原始訊息來抓取所選樹狀檢視專案的文字，第二個則是使用對等宏。 假設 *hwnd* 是控制項視窗的控制碼。


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



當系統色彩設定進行變更時，Windows 會將 [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) 訊息傳送至所有最上層視窗。 您的最上層視窗必須將 **WM \_ SYSCOLORCHANGE** 訊息轉寄到其通用控制項; 否則，將不會通知控制項色彩變更。 轉送訊息可確保通用控制項使用的色彩與其他使用者介面物件所使用的色彩一致。 例如，工具列控制項會使用「立體物件」色彩來繪製其按鈕。 如果使用者變更立體物件的色彩，但卻未將 **WM \_ SYSCOLORCHANGE** 訊息轉寄至工具列，工具列按鈕將會維持原來的色彩 (甚至會變更為舊色彩和新色彩的組合) 而系統中其他按鈕的色彩也會變更。

## <a name="notifications-from-controls"></a>來自控制項的通知

控制項是子視窗，會在控制項中發生事件（通常是由使用者輸入觸發）時，將通知訊息傳送至父視窗。 應用程式仰賴這些通知訊息來判斷使用者要其採取的動作。 除了 trackbars，它會使用 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息來通知其父系的變更，通用控制項會以 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 或 [**wm \_ 通知**](wm-notify.md) 訊息的形式傳送通知，如通知的參考主題中所指定。 一般情況下，較舊的通知 (已在 API 中的較長時間) 使用 **WM \_ 命令**。

[**WM \_ 通知**](wm-notify.md)的 *lParam* 參數是 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的位址，或是包含 **NMHDR** 作為其第一個成員的較大結構位址。 結構包含通知碼，並識別傳送通知訊息的通用控制項。 其餘結構成員（如果有的話）的意義會根據通知碼而有所不同。

每種類型的通用控制項都有一組對應的通知碼。 通用控制項程式庫也提供可由一個以上的通用控制項類型傳送的通知碼。 請參閱相關控制項的檔，以判斷要傳送的通知碼，以及他們所採用的格式。

如需顯示如何處理 [**WM \_ 通知**](wm-notify.md) 訊息的程式碼範例，請參閱該訊息的參考主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般控制項參考](common-control-reference.md)
</dt> </dl>

 

 
