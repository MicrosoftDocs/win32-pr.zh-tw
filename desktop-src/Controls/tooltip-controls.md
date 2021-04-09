---
title: 關於工具提示控制項
description: 當使用者將滑鼠指標暫停在工具或其他 UI 元素上方時，工具提示會自動出現或快顯。
ms.assetid: 1020cec7-57b4-4463-9419-f80fd14fa12c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9c1042523c86e794865da5d38fb023ee37d60b4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024173"
---
# <a name="about-tooltip-controls"></a>關於工具提示控制項

當使用者將滑鼠指標暫停在工具或其他 UI 元素上方時，工具提示會自動出現或快顯。 工具提示會出現在指標附近，並在使用者按一下滑鼠按鍵時消失、將指標移離工具，或只是等候幾秒鐘。

下圖中的工具提示控制項顯示 Windows 桌面上檔案的相關資訊。 當您將滑鼠移到圖上時，您也應該會看到包含描述性文字的即時工具提示。

![顯示工具提示中顯示在桌面上的檔案之文字的螢幕擷取畫面](images/tt-desktop.png)

本節說明工具提示控制項的運作方式，以及如何建立。

-   [工具提示行為和外觀](#tooltip-behavior-and-appearance)
-   [建立工具提示控制項](#creating-tooltip-controls)
-   [啟用工具提示控制項](#activating-tooltip-controls)
-   [支援工具](#supporting-tools)
-   [顯示文字](#displaying-text)
-   [訊息與通知](#messaging-and-notification)
-   [點擊測試](#hit-testing)
-   [預設訊息處理](#default-message-processing)

## <a name="tooltip-behavior-and-appearance"></a>工具提示行為和外觀

工具提示控制項可以顯示一行或多行文字。 它們的角落可以是圓角或方形。 它們不一定會有指向像是卡通語音球的工具。 工具提示文字可以是固定的，也可以使用滑鼠指標（稱為「追蹤」）移動。 靜止文字可以顯示在工具的旁邊，也可以透過工具（稱為就地）來顯示。 標準工具提示為固定、顯示單一文字、具有方形邊角，而且沒有指向工具的主幹。

[版本 4.70](common-control-versions.md)的通用控制項支援的追蹤工具提示，會動態變更螢幕上的位置。 藉由快速更新位置，這些工具提示控制項看似可順暢地移動或「追蹤」。 當您想要工具提示文字移動時，當滑鼠指標的位置遵循時，這些功能就很有用。 如需追蹤工具提示的詳細資訊，以及顯示如何建立程式碼的範例，請參閱 [追蹤工具提示](using-tooltip-contro.md)。

多行工具提示（共4.70 版的通用控制項也支援）會將文字顯示在一行以上。 這些很適合用來顯示冗長的訊息。 如需詳細資訊和示範如何建立多行工具提示的範例，請參閱 [多行工具提示](using-tooltip-contro.md)。

氣球工具提示會顯示在具有圓角的方塊和指向工具的主幹中。 它們可以是單行或多行。 下圖顯示在其預設位置中有詞幹和矩形的氣球工具提示。 如需氣球工具提示的詳細資訊，以及示範如何建立它們的範例，請參閱 [使用工具提示控制項](using-tooltip-contro.md)。

![顯示工具提示的螢幕擷取畫面，其中包含一行文字，位於對話方塊的按鈕上方](images/tt-balloon.png)

工具提示也可以有標題文字和圖示，如下圖所示。 請注意，工具提示必須有文字;如果只有標題文字，則不會顯示工具提示。 此外，除非有標題，否則不會出現圖示。

![顯示工具提示圖示、標題和文字的螢幕擷取畫面，其位於對話方塊的按鈕下方](images/tt-titled.png)

有時候文字字串會被裁剪，因為它們太長，無法完全顯示在小視窗中。 就地工具提示會用來顯示已裁剪之物件的文字字串，例如下圖中的檔案名。 如需示範如何建立就地工具提示的範例，請參閱就地 [工具提示](using-tooltip-contro.md)。

![顯示工具提示的螢幕擷取畫面，其中包含位於樹狀目錄控制項中檔案圖示旁邊的檔案名](images/tt-inplace.png)

游標必須停留在工具上一段時間，才會顯示工具提示。 此超時的預設持續時間是由使用者的按兩下時間來控制，通常約為半秒。 若要指定非預設的超時值，請將 [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md) 訊息傳送給工具提示控制項。

## <a name="creating-tooltip-controls"></a>建立工具提示控制項

若要建立工具提示控制項，請呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 並指定 [**工具提示 \_ 類別**](common-control-window-classes.md) 視窗類別。 載入通用控制項 DLL 時，會註冊這個類別。 若要確定已載入此 DLL，請在您的應用程式中包含 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式。 您必須將工具提示控制項明確定義為最上層。 否則，它可能會包含在父視窗中。 下列程式碼片段顯示如何建立工具提示控制項。


```
HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                            WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            hwndParent, NULL, hinstMyDll,
                            NULL);

SetWindowPos(hwndTip, HWND_TOPMOST,0, 0, 0, 0,
             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);
```



工具提示控制項的視窗程式會自動設定控制項的大小、位置和可見度。 工具提示視窗的高度是以目前在工具提示控制項的裝置內容中所選取字型的高度為基礎。 寬度會根據目前在工具提示視窗中的字串長度而有所不同。

## <a name="activating-tooltip-controls"></a>啟用工具提示控制項

工具提示控制項可以是作用中或非作用中。 當使用中時，當滑鼠指標位於工具上時，就會顯示工具提示文字。 當它處於非使用中狀態時，即使指標在工具上，也不會出現工具提示文字。 [**TTM \_ 啟動**](ttm-activate.md)訊息會啟用並停用工具提示控制項。

## <a name="supporting-tools"></a>支援工具

工具提示控制項可支援任意數目的工具。 若要支援特定的工具，您必須透過將 [**TTM \_ ADDTOOL**](ttm-addtool.md) 訊息傳送給控制項，向工具提示控制項註冊工具。 訊息包含 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的位址，其提供工具提示控制項顯示工具文字所需的資訊。 **TOOLINFO** 結構的 **uID** 成員是由應用程式所定義。 每次加入工具時，您的應用程式都會提供唯一的識別碼。 **TOOLINFO** 結構的 **cbSize** 成員是必要的，而且必須指定結構的大小。

工具提示控制項支援實作為 windows (的工具，例如子視窗或控制 windows) ，以及視窗工作區中的矩形區域。 當您加入實作為矩形區域的工具時， [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **hwnd** 成員必須指定包含該區域之視窗的控制碼，而 **rect** 成員必須指定區域周框矩形的用戶端座標。 此外， **uID** 成員必須為工具指定應用程式定義的識別碼。

當您加入實作為視窗的工具時， [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uID** 成員必須包含工具的視窗控制碼。 此外， **uFlags** 成員還必須指定 **TTF \_ IDISHWND** 值，告知工具提示控制項將 **uID** 成員解讀為視窗控制碼。

## <a name="displaying-text"></a>顯示文字

當您將工具加入至工具提示控制項時， [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **lpszText** 成員必須指定要顯示給工具的字串位址。 新增工具之後，您可以使用 [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md) 訊息來變更文字。

如果 **lpszText** 的高序位字是零，則低序位字必須是字串資源的識別碼。 當工具提示控制項需要文字時，系統會從 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **hinst** 成員所識別的應用程式實例載入指定的字串資源。

如果您 \_ 在 **lpszText** 成員中指定 LPSTR TEXTCALLBACK 值，每當工具提示控制項需要顯示工具的文字時，工具提示控制項就會通知 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **hwnd** 成員中指定的視窗。 工具提示控制項會將 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 通知程式碼傳送至視窗。 訊息包含 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) 結構的位址，其中包含視窗控制碼以及工具的應用程式定義識別碼。 此視窗會檢查結構，以判斷需要文字的工具，並使用工具提示控制項所需的資訊來填滿適當的結構成員，以便顯示字串。

> [!Note]  
> 標準工具提示文字的最大長度是80個字元。 如需詳細資訊，請參閱 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) 結構。 多行工具提示文字可能較長。

 

許多應用程式會建立包含對應至功能表命令之工具的工具列。 針對這類工具，工具提示控制項顯示與對應功能表項目相同的文字是很方便的。 系統會自動從所有傳遞給工具提示控制項的字串中移除連字號 (&) 快速鍵字元， \\ 除非控制項有 [**TTS \_ NOPREFIX**](tooltip-styles.md) 樣式，否則會在第一個索引標籤字元 (t) 上結束字串。

若要取出工具的文字，請使用 [**TTM \_ GETTEXT**](ttm-gettext.md) 訊息。

## <a name="messaging-and-notification"></a>訊息與通知

當滑鼠指標停留在區域上時，通常會顯示工具提示文字，通常是由按鈕控制項等工具所定義的矩形。 不過，Microsoft Windows 只會將滑鼠相關的訊息傳送至包含指標的視窗，而不是工具提示控制項本身。 滑鼠相關資訊必須轉送至工具提示控制項，才能讓它在適當的時間和位置顯示工具提示文字。

如果有下列情況，您就可以自動轉送訊息：

-   此工具是一個控制項，或定義為工具 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構中的矩形。
-   與工具相關聯的視窗會在與工具提示控制項相同的執行緒中。

如果符合這兩個條件，當您使用 [**TTM \_ ADDTOOL**](ttm-addtool.md)將工具新增至工具提示控制項時，請在工具 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中設定 **TTF 子 \_ 類別** 旗標。 必要的滑鼠訊息會自動轉送至工具提示控制項。

設定 **TTF 子 \_ 類別** ，以將滑鼠訊息轉送至控制項，對於大多數用途都已足夠。 不過，在工具提示控制項和工具視窗之間沒有直接連接的情況下，它將無法運作。 例如，如果在應用程式定義的視窗中將工具實作為矩形區域，則視窗程式會收到滑鼠訊息。 設定 **TTF 子 \_ 類別** 就足以確保將它們傳遞給控制項。 但是，如果工具是實作為系統定義的視窗，則會將滑鼠訊息傳送至該視窗，且不會直接提供給應用程式使用。 在此情況下，您必須將視窗子類別化或使用訊息攔截來存取滑鼠訊息。 然後，您必須使用 [**TTM \_ RELAYEVENT**](ttm-relayevent.md)，將滑鼠訊息明確地轉送至工具提示控制項。 如需如何使用 **TTM \_ RELAYEVENT** 的範例，請參閱 [追蹤工具提示](using-tooltip-contro.md)。

當工具提示控制項收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息時，它會判斷滑鼠指標是否在工具的周框中。 如果是，則工具提示控制項會設定計時器。 在逾時間隔結束時，工具提示控制項會檢查指標的位置，以查看是否已移動指標。 如果沒有，工具提示控制項會抓取工具的文字，並顯示工具提示。 工具提示控制項會繼續顯示視窗，直到它收到轉送的按鈕或按鈕下的訊息，或直到 **WM \_ MOUSEMOVE** 訊息指出指標已移至工具的周框以外的範圍。

工具提示控制項實際上有三個相關聯的時間持續時間。 初始持續時間是在顯示工具提示視窗之前，滑鼠指標必須保持在工具周框內的靜止時間。 Reshow 持續時間是在指標從一個工具移至另一個工具時，顯示後續工具提示視窗之前的延遲時間長度。 快顯視窗持續時間是工具提示視窗在隱藏之前保持顯示狀態的時間。 亦即，如果指標在顯示工具提示視窗之後，在周框內保持不變，則會在快顯期間結束時自動隱藏工具提示視窗。 您可以使用 [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md) 訊息來調整所有超時時間。

如果應用程式包含實作為矩形區域的工具，以及控制項的大小或位置變更，則應用程式可以使用 [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md) 訊息來報告工具提示控制項的變更。 應用程式不需要針對實作為視窗的工具報告大小和位置變更，因為工具提示控制項使用工具的視窗控制碼來判斷滑鼠指標是否在工具上，而不是工具的周框。

當工具提示即將顯示時，工具提示控制項會將 [TTN \_ 顯示](ttn-show.md) 通知碼傳送給擁有者視窗。 當工具提示即將隱藏時，擁有者視窗會收到 [TTN 的 \_ POP](ttn-pop.md) 通知碼。 每個通知碼都會在 [**WM \_ 通知**](wm-notify.md) 訊息的內容中傳送。

## <a name="hit-testing"></a>點擊測試

[**TTM \_ system.windows.media.visualtreehelper.hittest**](ttm-hittest.md)訊息可讓您取得工具提示控制項維護有關特定點之工具的資訊。 此訊息包含 [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) 結構，其中包含視窗控制碼、點的座標，以及 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的位址。 工具提示控制項會判斷工具是否會佔用點，如果有的話，會以工具的相關資訊填滿 **TOOLINFO** 。

## <a name="default-message-processing"></a>預設訊息處理

下表描述工具提示控制項的視窗程式所處理的訊息。



| 訊息                                        | 描述                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)             | 確保工具提示控制項具有 [**ws \_ EX \_ 工具視窗**](/windows/desktop/winmsg/window-styles) 和 [**ws \_ 彈出**](/windows/desktop/winmsg/window-styles) 視窗樣式。 它也會配置記憶體並初始化內部變數。 |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)           | 釋出配置給工具提示控制項的資源。                                                                                                                                                                                                                |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | 傳回工具提示控制項將用來繪製文字的字型控制碼。                                                                                                                                                                                    |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)     | 隱藏工具提示視窗。                                                                                                                                                                                                                                         |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                  | 繪製工具提示視窗。                                                                                                                                                                                                                                         |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)           | 設定工具提示控制項將用來繪製文字的字型控制碼。                                                                                                                                                                                       |
| [**WM \_ 計時器**](/windows/desktop/winmsg/wm-timer)               | 如果工具已變更位置，或滑鼠指標移至工具外，則隱藏工具提示視窗。 否則，它會顯示工具提示視窗。                                                                                                             |
| [**WM \_ WININICHANGE**](/windows/desktop/winmsg/wm-wininichange) | 重設以系統計量為基礎的內部變數。                                                                                                                                                                                                       |



 

 

 