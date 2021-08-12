---
title: 關於快速鍵控制項
description: 快速鍵控制項是一種視窗，可讓使用者輸入按鍵的組合，以做為快速鍵使用。
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256fcfde87a1fb6603f90e8a2a41cb4f2cc9356f9f45d861efdc6836aa5344fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672239"
---
# <a name="about-hot-key-controls"></a>關於快速鍵控制項

快速鍵控制項是一種視窗，可讓使用者輸入按鍵的組合，以做為快速鍵使用。 快速鍵是使用者可以按來快速執行動作的按鍵組合。 例如，使用者可以建立啟動指定視窗的熱鍵，然後將它放到迭置順序的最上層。 快速鍵控制項會顯示使用者的選項，並確保使用者選取有效的按鍵組合。 下列螢幕擷取畫面顯示當使用者按下 ALT 鍵之後，快速鍵控制項如何出現在對話方塊中。

![包含快速鍵控制項之對話方塊的螢幕擷取畫面](images/hotkey.png)

## <a name="using-hot-key-controls"></a>使用快速鍵控制項

當使用者輸入要做為快速鍵的按鍵組合時，索引鍵的名稱會出現在熱鍵控制項中。 按鍵組合可以包含輔助按鍵 (例如 CTRL、ALT 或 SHIFT) ，以及伴隨的按鍵 (例如，字元鍵、箭號、函式索引鍵等) 。

當使用者選擇了按鍵組合之後，應用程式會從快速鍵控制項抓取按鍵組合，並使用它來設定系統中的快速鍵。 從快速鍵控制項取出的資訊包括一個旗標，指出所附索引鍵的輔助按鍵和虛擬金鑰碼。

應用程式可以使用快速鍵控制項所提供的資訊，來設定全域熱鍵或執行緒特定的快速鍵。 全域快速鍵會與特定視窗相關聯;它可讓使用者從系統的任何部分啟動視窗。 應用程式會使用 [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) 訊息來設定全域快速鍵。 每當使用者按下全域快速鍵時，在 **wm \_ SETHOTKEY** 中指定的視窗就會收到指定 [**SC \_ 熱鍵**](/windows/desktop/inputdev/wm-sethotkey)值的 [**wm \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)訊息。 此訊息會啟用接收它的視窗。 在呼叫 **WM \_ SETHOTKEY** 的應用程式結束之前，快速鍵會保持有效。

執行緒特定的熱鍵會產生可張貼至特定執行緒開頭的 [**WM \_ 熱鍵**](/windows/desktop/inputdev/wm-hotkey) 訊息，以便在訊息迴圈的下一個反復專案中移除。 應用程式會使用 [**RegisterHotKey**](/windows/desktop/api/winuser/nf-winuser-registerhotkey) 函數來設定執行緒特定的熱鍵。

### <a name="hot-key-control-messages"></a>快速鍵控制訊息

建立熱鍵控制項之後，應用程式會使用三個訊息與其互動： [**HKM \_ SETRULES**](hkm-setrules.md)、 [**HKM \_ SETHOTKEY**](hkm-sethotkey.md)和 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md)。

應用程式可以傳送 [**HKM \_ SETRULES**](hkm-setrules.md) 訊息，以指定一組被視為無效快速鍵的 CTRL、ALT 和 SHIFT 鍵組合。 如果應用程式指定不正確按鍵組合，則也應該在使用者選取不正確組合時，指定要使用的預設修飾片語合。 當使用者輸入不正確組合時，系統會針對不正確組合和預設的組合執行邏輯 OR 運算。 結果會被視為有效的組合;它會轉換成字串並顯示在控制項中。

[**HKM \_ SETHOTKEY**](hkm-sethotkey.md)訊息可讓應用程式設定快速鍵控制項的快速鍵組合。 此訊息通常也會在建立快速鍵控制項時使用。

應用程式會使用 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息來取得使用者所選擇之快速鍵的虛擬機器碼和修飾詞旗標。

### <a name="hot-key-control-notifications"></a>快速鍵控制通知

快速鍵控制項不會透過 [**WM \_ 通知**](wm-notify.md) 訊息傳送任何通知碼。 不過，它會在使用者變更控制項的內容時，透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息傳送 [EN \_ 變更](en-change.md)通知。

### <a name="default-hot-key-message-processing"></a>預設的快速鍵訊息處理

本節說明使用快速鍵控制項之預先定義之快速鍵 [**\_ 類別**](common-control-window-classes.md) 視窗類別的視窗程式所處理的視窗訊息。

|    訊息                                            |    處理已執行                               |
|------------------------------------------------|--------------------------------------------------------------|
| [**WM \_ 字元**](/windows/desktop/inputdev/wm-char)               | 抓取虛擬金鑰程式碼。             |
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)             | 初始化熱鍵控制項、清除任何熱鍵規則，並使用系統字型。   |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)     | 隱藏插入號、呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，然後再次顯示插入號。   |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)     | 傳回 [**DLGC \_ WANTCHARS**](/windows/desktop/dlgbox/wm-getdlgcode) 和 [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) 值的組合。   |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | 抓取字型。                         |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | 如果索引鍵為 ENTER、TAB、空格鍵、DEL、ESC 或倒退鍵，則呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 如果索引鍵是 SHIFT、CTRL 或 ALT，它會檢查組合是否有效，如果是，則會使用組合來設定快速鍵。 所有其他金鑰都會設定為快速鍵，而不會先檢查其有效性。 |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | 抓取虛擬金鑰程式碼。             |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)     | 終結插入號。                         |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | 將焦點設定至視窗。               |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)         | 設定 [**WS \_ EX \_ CLIENTEDGE**](/windows/desktop/winmsg/extended-window-styles) 視窗樣式。        |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                  | 繪製快速鍵控制項。                 |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)       | 建立並顯示插入號。                |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)           | 設定字型。                              |
| [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)           | 抓取虛擬金鑰程式碼。             |
| [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)   | 如果索引鍵為 ENTER、TAB、空格鍵、DEL、ESC 或倒退鍵，則呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 如果索引鍵是 SHIFT、CTRL 或 ALT，它會檢查組合是否有效，如果是，則會使用組合來設定快速鍵。 所有其他金鑰都會設定為快速鍵，而不會先檢查其有效性。 |
| [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)       | 抓取虛擬金鑰程式碼。             |
