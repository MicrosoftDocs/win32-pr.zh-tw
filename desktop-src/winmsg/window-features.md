---
description: 本總覽討論視窗的功能，例如視窗類型、狀態、大小和位置。
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: 視窗功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228c6b4ab59102cae38a248935fbbad32198f2e0
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/25/2021
ms.locfileid: "106995113"
---
# <a name="window-features"></a>視窗功能

本總覽討論視窗的功能，例如視窗類型、狀態、大小和位置。

-   [視窗類型](#window-types)
    -   [重迭視窗](#overlapped-windows)
    -   [快顯視窗](#pop-up-windows)
    -   [子視窗](#child-windows)
        -   [定位](#positioning)
        -   [裁剪](#clipping)
        -   [父視窗的關聯性](#relationship-to-parent-window)
        -   [訊息](#size-and-position-messages)
    -   [分層視窗](#layered-windows)
    -   [僅限訊息的視窗](#message-only-windows)
-   [視窗關聯性](#window-relationships)
    -   [前景和背景視窗](#foreground-and-background-windows)
    -   [擁有的視窗](#owned-windows)
    -   [Z 順序](#z-order)
-   [視窗顯示狀態](#window-show-state)
    -   [使用中視窗](#active-window)
    -   [停用的視窗](#disabled-windows)
    -   [視窗可見度](#window-visibility)
    -   [最小化、最大化和還原的視窗](#minimized-maximized-and-restored-windows)
-   [視窗大小和位置](#window-size-and-position)
    -   [預設大小和位置](#default-size-and-position)
    -   [追蹤大小](#tracking-size)
    -   [系統命令](#system-commands)
    -   [大小和位置函式](#size-and-position-functions)
    -   [大小和位置訊息](#size-and-position-messages)
-   [視窗動畫](#window-animation)
-   [視窗版面配置和鏡像](#window-layout-and-mirroring)
    -   [鏡像對話方塊和訊息方塊](#mirroring-dialog-boxes-and-message-boxes)
    -   [未與視窗相關聯的鏡像裝置內容](#mirroring-device-contexts-not-associated-with-a-window)
-   [視窗損毀](#window-destruction)

## <a name="window-types"></a>視窗類型

本節包含描述視窗類型的下列主題。

-   [重迭視窗](#overlapped-windows)
-   [快顯視窗](#pop-up-windows)
-   [子視窗](#child-windows)
-   [分層視窗](#layered-windows)
-   [僅限訊息的視窗](#message-only-windows)

### <a name="overlapped-windows"></a>重迭視窗

重迭 *視窗* 是最上層視窗， (具有標題列、框線和工作區的非子視窗) ;它是作為應用程式的主視窗。 它也可以有視窗功能表、最小化和最大化按鈕，以及捲軸。 當做主視窗使用的重迭視窗通常包含所有這些元件。

藉由在 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式中指定 ws 重迭或 **ws \_ OVERLAPPEDWINDOW** 樣式，應用程式會建立一個重迭的視窗。 [**\_**](window-styles.md) 如果您使用 **WS 重 \_** 迭樣式，則視窗具有標題列和框線。 如果您使用 **WS \_ OVERLAPPEDWINDOW** 樣式，則視窗具有標題列、調整大小框線、視窗功能表，以及最小化和最大化按鈕。

### <a name="pop-up-windows"></a>快顯視窗

*快顯視窗* 是一種特殊類型的重迭視窗，用於對話方塊、訊息方塊，以及顯示在應用程式主視窗外部的其他暫存視窗。 標題列是快顯視窗的選擇性專案;否則，快顯視窗與 WS 重迭樣式的重迭視窗相同 [**。 \_**](window-styles.md)

您可以藉由在 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)中指定 [**WS \_ 彈出**](window-styles.md)視窗樣式來建立快顯視窗。 若要包含標題列，請指定 **WS \_ 標題** 樣式。 使用 **WS \_ POPUPWINDOW** 樣式，建立具有框線和視窗功能表的快顯視窗。 **Ws \_ 標題** 樣式必須與 **ws \_ POPUPWINDOW** 樣式結合，才能讓視窗功能表顯示。

### <a name="child-windows"></a>子視窗

*子視窗* 具有 [**WS \_ 子**](window-styles.md)樣式，且受限於其父視窗的工作區。 應用程式通常會使用子視窗將父視窗的工作區分割成功能區域。 您可以藉由在 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式中指定 **WS \_ 子** 系樣式來建立子視窗。

子視窗必須有父視窗。 父視窗可以是重迭的視窗、快顯視窗，甚至是另一個子視窗。 當您呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)時，請指定父視窗。 如果您在 **CreateWindowEx** 中指定 [**WS \_ 子**](window-styles.md)樣式，但是未指定父視窗，系統就不會建立視窗。

子視窗具有工作區，但沒有其他功能，除非明確要求它們。 應用程式可以要求標題列、視窗功能表、最小化和最大化按鈕、框線和子視窗捲軸，但是子視窗不能有功能表。 如果應用程式指定功能表控制碼，則在註冊子視窗類別或建立子視窗時，會忽略功能表控制碼。 如果未指定框線樣式，系統會建立無邊框的視窗。 應用程式可以使用無邊框的子視窗來分割父視窗的工作區，同時讓使用者看不到這些片段。

本節將討論子視窗的下列層面：

-   [定位](#positioning)
-   [裁剪](#clipping)
-   [父視窗的關聯性](#relationship-to-parent-window)
-   [訊息](#size-and-position-messages)

#### <a name="positioning"></a>定位

系統一律會將子視窗相對於其父視窗工作區的左上角。 子視窗的任何部分，都不會出現在其父視窗的框線之外。 如果應用程式建立的子視窗大於父視窗，或將子視窗放置於子視窗之外，使部分或全部的子視窗延伸超過父系的框線，系統就會裁剪子視窗;也就是說，不會顯示父視窗工作區外的部分。 影響父視窗的動作也會影響子視窗，如下所示。



| 父視窗 | 子視窗                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| 終結     | 在父視窗損毀之前終結。                                                                         |
| Hidden        | 隱藏之前隱藏的父視窗。 只有當父視窗可見時，才會顯示子視窗。             |
| 搬         | 使用父視窗的工作區移動。 子視窗負責在移動之後繪製其工作區。 |
| 顯示         | 顯示父視窗之後顯示。                                                                                  |



 

#### <a name="clipping"></a>裁剪

系統不會自動從父視窗的工作區裁剪子視窗。 這表示，如果父視窗在與子視窗相同的位置中執行任何繪圖，則會在子視窗上方繪製。 但是，如果父視窗具有 [**WS \_ CLIPCHILDREN**](window-styles.md) 樣式，系統就會從父視窗的工作區裁剪子視窗。 如果子視窗被裁剪，父視窗就無法在其上繪製。

子視窗可以與相同工作區中的其他子視窗重迭。 與一或多個其他子視窗共用相同父視窗的子視窗稱為「同級」 *視窗*。 除非其中一個子視窗具有 [**WS \_ CLIPSIBLINGS**](window-styles.md) 樣式，否則同輩視窗可以在彼此的工作區中繪製。 如果子視窗有此樣式，則會裁剪其子視窗內任何其同級視窗的任何部分。

如果視窗具有 [**ws \_ CLIPCHILDREN**](window-styles.md) 或 **ws \_ CLIPSIBLINGS** 樣式，效能就會稍微遺失。 每個視窗都會佔用系統資源，因此應用程式不會有不限的使用子視窗。 為了達到最佳效能，需要以邏輯方式分割主視窗的應用程式應該在主視窗的視窗程式中執行，而不是使用子視窗。

#### <a name="relationship-to-parent-window"></a>父視窗的關聯性

應用程式可以藉由呼叫 [**SetParent**](/windows/win32/api/winuser/nf-winuser-setparent) 函數來變更現有子視窗的父視窗。 在這種情況下，系統會從舊的父視窗的工作區中移除子視窗，並將它移至新父視窗的工作區。 如果 **SetParent** 指定 **Null** 控制碼，桌面視窗就會變成新的父視窗。 在此情況下，子視窗會在桌面上繪製于任何其他視窗的框線之外。 [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent)函式會將控制碼捕獲到子視窗的父視窗。

父視窗會將其工作區的一部分會讓出至子視窗，而子視窗則會接收此區域的所有輸入。 父視窗的每個子視窗的視窗類別都不需要相同的。 這表示，應用程式可以使用外觀不同的子視窗來填滿父視窗，並執行不同的工作。 例如，對話方塊可包含許多類型的控制項，每個都有一個子視窗接受來自使用者的不同資料類型。

子視窗只有一個父視窗，但父系可以有任意數目的子視窗。 每個子視窗接著都可以有子視窗。 在這一系列的 windows 中，每個子視窗稱為原始父視窗的子系視窗。 應用程式會使用 [**IsChild**](/windows/win32/api/winuser/nf-winuser-ischild) 函式，來探索指定的視窗是否為指定之父視窗的子視窗或子系視窗。

[**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows)函式會列舉父視窗的子視窗。 然後， **EnumChildWindows** 會將控制碼傳遞至應用程式定義的回呼函數。 也會列舉指定父視窗的子系視窗。

#### <a name="messages"></a>訊息

系統會將子視窗的輸入訊息直接傳遞給子視窗;訊息不會透過父視窗傳遞。 唯一的例外狀況是 [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) 函數已停用子視窗。 在此情況下，系統會改為將已移至子視窗的任何輸入訊息傳送至父視窗。 這可讓父視窗檢查輸入訊息並視需要啟用子視窗。

子視窗可以有唯一的整數識別碼。 使用控制項視窗時，子視窗識別碼相當重要。 應用程式會藉由傳送訊息來導向控制項的活動。 應用程式會使用控制項的子視窗識別碼，將訊息導向至控制項。 此外，控制項會將通知訊息傳送至其父視窗。 通知訊息會包含控制項的子視窗識別碼，父系會使用此識別碼來識別傳送訊息的控制項。 應用程式會藉由將 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式的 *hMenu* 參數設定為值而非功能表控制碼，來指定其他類型之子視窗的子視窗識別碼。

### <a name="layered-windows"></a>分層視窗

使用分層視窗可大幅改善具有複雜圖形、動畫圖形或希望使用 Alpha 混色效果之視窗的效能和視覺效果。 系統會自動撰寫和重新繪製分層視窗和基礎應用程式的視窗。 如此一來，就能順暢地轉譯分層視窗，而不會有複雜視窗區域的閃爍。 此外，分層視窗也可以部分半透明，也就是以 Alpha 混合的方式。

若要建立多層式視窗，請在呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式時指定 **ws \_ ex \_ 分層** 擴充視窗樣式，或呼叫 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)函式，以在建立視窗之後設定 **ws \_ ex \_ 分層**。 在 **CreateWindowEx** 呼叫之後，在此視窗中呼叫 [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) 或 [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) 函式之前，不會顯示多層式視窗。

> [!Note]  
> 從 Windows 8 開始， **WS \_ EX \_ 分層** 可以搭配子視窗和最上層視窗使用。 先前的 Windows 版本僅支援最上層視窗的 **WS 範例 \_ \_ 層** 級。

 

若要為指定的分層視窗設定不透明度層級或透明色彩索引鍵，請呼叫 [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes)。 在呼叫之後，系統可能仍會要求視窗在視窗顯示或調整大小時進行繪製。 不過，由於系統會儲存多層式視窗的影像，因此系統不會要求視窗在顯示時顯示為相對視窗在桌面上移動的結果。 如果繼承應用程式想要為視窗新增半透明度或透明效果，就不需要重新處理其繪製程式碼，因為系統會將呼叫 **SetLayeredWindowAttributes** 的視窗繪製重新導向至非螢幕記憶體，並 recomposes 它以達成所要的效果。

如需更快速且更有效率的動畫，或需要每圖元的 Alpha，請呼叫 [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow)。 當應用程式必須直接提供多層式視窗的圖形和內容時，才應該使用 **UpdateLayeredWindow** ，而不需使用系統透過 [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes)提供的重新導向機制。 此外，使用 **UpdateLayeredWindow** 可讓您更有效率地使用記憶體，因為系統不需要額外的記憶體來儲存重新導向視窗的映射。 為了在建立視窗動畫的最高效率，請呼叫 **UpdateLayeredWindow** 來變更分層視窗的位置和大小。 請注意，呼叫 **SetLayeredWindowAttributes** 之後，後續的 **UpdateLayeredWindow** 呼叫將會失敗，直到分層樣式位已清除並再次設定為止。

分層視窗的點擊測試是以視窗的圖形和透明度為基礎。 這表示，以色彩為色彩或其 Alpha 值為零的視窗區域會讓滑鼠訊息通過。 但是，如果分層視窗具有 [ **WS \_ EX \_ 透明** 擴充] 視窗樣式，則會忽略分層視窗的形狀，並將滑鼠事件傳遞至多層式視窗底下的其他視窗。

### <a name="message-only-windows"></a>Message-Only Windows

*僅限訊息的視窗* 可讓您傳送和接收訊息。 它看不見、沒有迭置順序、無法列舉，也不會收到廣播訊息。 此視窗只會分派訊息。

若要建立僅限訊息的視窗，請在 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函數的 *hWndParent* 參數中，指定 [HWND \_ 訊息](#message-only-windows)常數或現有純訊息視窗的控制碼。 您也可以 \_ 在 [**SetParent**](/windows/win32/api/winuser/nf-winuser-setparent)函數的 *HWNDNEWPARENT* 參數中指定 HWND 訊息，將現有的視窗變更為僅限訊息的視窗。

若要尋找僅限訊息的視窗，請在 [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa)函數的 *hwndParent* 參數中指定 [HWND \_ 訊息](#message-only-windows)。 此外，如果 *hwndParent* 和 *hwndChildAfter* 參數都是 **Null**，則 **FindWindowEx** 會搜尋僅限訊息的視窗以及最上層視窗。

## <a name="window-relationships"></a>視窗關聯性

有許多方式可讓視窗與使用者或另一個視窗相關聯。 視窗可以是擁有的視窗、前景視窗或背景視窗。 視窗也有相對於其他視窗的 z 順序。 如需詳細資訊，請參閱下列主題：

-   [前景和背景視窗](#foreground-and-background-windows)
-   [擁有的視窗](#owned-windows)
-   [Z 順序](#z-order)

### <a name="foreground-and-background-windows"></a>前景和背景視窗

每個進程都可以有多個執行緒，而且每個執行緒都可以建立視窗。 建立使用者目前正在工作之視窗的執行緒稱為「前景執行緒」，而視窗則稱為「 *前景視窗*」。 所有其他執行緒都是背景執行緒，而背景執行緒所建立的視窗稱為 *背景視窗*。

每個執行緒都具有優先權層級，以決定執行緒接收的 CPU 時間量。 雖然應用程式可以設定其執行緒的優先權層級，但通常前景執行緒的優先權層級會比背景執行緒稍微高得多。 因為它的優先順序較高，所以前景執行緒所接收的 CPU 時間會比背景執行緒更多。 前景執行緒的一般基本優先權為 9;背景執行緒的一般基本優先權為7。

使用者可以按一下視窗，或使用 ALT + TAB 或 ALT + ESC 鍵組合來設定前景視窗。 若要取得前景視窗的控制碼，請使用 [**GetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) 函數。 若要檢查您的應用程式視窗是否為前景視窗，請將 **GetForegroundWindow** 傳回的控制碼與您應用程式視窗中的控制碼做比較。

應用程式會使用 [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) 函數來設定前景視窗。

系統會限制哪些進程可以設定前景視窗。 只有在下列情況時，進程才能設定前景視窗：

- 下列所有條件都成立：
  - 呼叫 **SetForegroundWindow** 的程式屬於桌面應用程式，而不是針對 Windows 8 或8.1 所設計的 UWP 應用程式或 Windows Store 應用程式。
  - 前景進程尚未針對 [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow)函式的先前呼叫停用對 **SetForegroundWindow** 的呼叫。
  - 前景鎖定超時已過期 (請參閱 SystemParametersInfo) [中的 **SPI_GETFOREGROUNDLOCKTIMEOUT**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT) 。
  - 沒有作用中的功能表。
- 此外，至少下列其中一個條件成立：
  - 呼叫進程是前景進程。
  - 呼叫進程由前景進程啟動。
  - 目前沒有前景視窗，因此沒有前景進程。
  - 呼叫進程收到最後一個輸入事件。
  - 正在調試前景進程或呼叫進程。

進程可能會被拒絕設定前景視窗的許可權，即使它符合這些條件也是一樣。

可以設定前景視窗的進程，可以藉由呼叫 [**AllowSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) 函式或呼叫 [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) 函式與 **BSF \_ ALLOWSFW** 旗標，讓另一個進程設定前景視窗。 前景進程可以藉由呼叫 [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow)函數來停用對 [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow)的呼叫。

### <a name="owned-windows"></a>擁有的視窗

重迭或快顯視窗可以由另一個重迭或快顯視窗所擁有。 所擁有的會將數個條件約束放在視窗上。

-   擁有的視窗一律高於其擁有者（以 z 順序排列）。
-   當系統的擁有者損毀時，系統會自動終結擁有的視窗。
-   當其擁有者最小化時，會隱藏擁有的視窗。

只有重迭或快顯視窗可以是擁有者視窗;子視窗不可以是擁有者視窗。 應用程式會在建立具有 [**ws \_**](window-styles.md)重迭或 ws 快顯樣式的視窗時，指定擁有者的視窗控制碼做為 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)的 *hwndParent* 參數，以建立所擁有的視窗。 **\_** *HwndParent* 參數必須識別重迭或快顯視窗。 如果 *hwndParent* 識別子視窗，系統會將擁有權指派給子視窗的最上層父視窗。 建立擁有的視窗之後，應用程式無法將視窗的擁有權轉移到另一個視窗。

對話方塊和訊息方塊預設為 windows 擁有的視窗。 應用程式會在呼叫建立對話方塊或訊息方塊的函式時，指定擁有者視窗。

應用程式可以搭配 **GW \_ 擁有** 者旗標使用 [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow)函式，以取得視窗擁有者的控制碼。

### <a name="z-order"></a>Z 順序

視窗的迭置 *順序* 表示視窗在重迭視窗堆疊中的位置。 此視窗堆疊是沿著虛數軸（Z 軸）導向，從畫面向外擴充。 位於 z 順序頂端的視窗會與所有其他視窗重迭。 迭置順序底部的視窗會與所有其他視窗重迭。

系統會在單一清單中維護 z 順序。 它會根據最上層視窗、最上層視窗或子視窗，將視窗新增至 z 順序。 *最上層視窗* 會重迭所有其他非最上層視窗，而不論它是作用中或前景視窗。 最上層的視窗具有 **WS \_ EX \_ 最上層** 的樣式。 所有最上層視窗會在任何非最上層視窗之前以 z 順序顯示。 子視窗會以迭置順序與其父系群組。

當應用程式建立視窗時，系統會將它放在相同類型之視窗的 z 順序頂端。 您可以使用 [**BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) 函式，將視窗帶到相同類型之視窗的 z 順序頂端。 您可以使用 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 和 [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) 函數來重新排列迭置順序。

使用者藉由啟用不同的視窗，來變更 z 順序。 系統會將使用中視窗置於相同類型之視窗的迭置順序頂端。 當視窗指向迭置順序的上方時，就會進行子視窗。 您可以使用 [**GetTopWindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) 函式來搜尋父視窗的所有子視窗，並將控制碼傳回至 z 順序最高的子視窗。 [**GetNextWindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow)函式會以 z 順序抓取下一個或上一個視窗的控制碼。

## <a name="window-show-state"></a>視窗顯示狀態

在任何指定的時間，視窗可能會處於作用中或非作用中;隱藏或可見;以及最小化、最大化或還原。 這些品質統稱為 *視窗顯示狀態*。 下列主題討論視窗顯示狀態：

-   [使用中視窗](#active-window)
-   [停用的視窗](#disabled-windows)
-   [視窗可見度](#window-visibility)
-   [最小化、最大化和還原的視窗](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>使用中視窗

*使用中視窗* 是使用者目前工作的應用程式最上層視窗。 為了讓使用者可以輕鬆地識別使用中視窗，系統會將它放在迭置順序的頂端，並將其標題列和框線的色彩變更為系統定義的使用中視窗色彩。 只有最上層視窗可以是使用中視窗。 當使用者使用子視窗時，系統會啟動與子視窗相關聯的最上層父視窗。

系統中一次只會有一個最上層視窗處於作用中狀態。 使用者可以按一下 (或其中一個子視窗) ，或使用 ALT + ESC 或 ALT + TAB 鍵組合來啟動最上層視窗。 應用程式會藉由呼叫 [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) 函數來啟動最上層視窗。 其他函式可能會導致系統啟用不同的最上層視窗，包括 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)、 [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)、 [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)和 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)。 雖然應用程式可以隨時啟用不同的最上層視窗，但為了避免讓使用者感到混淆，它應該只是為了回應使用者動作。 應用程式會使用 [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) 函式來取得使用中視窗的控制碼。

當啟用從某個應用程式的最上層視窗變更為另一個應用程式的最上層視窗時，系統會將 [**WM \_ ACTI加值稅EAPP**](wm-activateapp.md) 訊息傳送給這兩個應用程式，以通知變更。 當啟用變更至相同應用程式中不同的最上層視窗時，系統會傳送 [**WM \_ 啟動**](../inputdev/wm-activate.md) 訊息給這兩個視窗。

### <a name="disabled-windows"></a>停用的視窗

您可以停用視窗。 *停用的視窗* 不會收到使用者的鍵盤或滑鼠輸入，但可以從其他視窗、從其他應用程式和系統接收訊息。 應用程式通常會停用視窗，以防止使用者使用視窗。 例如，應用程式可能會停用對話方塊中的 [推播] 按鈕，以防止使用者選擇它。 應用程式可以隨時啟用停用的視窗;啟用視窗會還原一般輸入。

根據預設，視窗會在建立時啟用。 但是，應用程式可以指定 [**WS \_ 停用**](window-styles.md) 的樣式，以停用新的視窗。 應用程式會使用 [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) 函數來啟用或停用現有的視窗。 系統會在啟用狀態即將變更時，將 [**WM \_ 啟用**](wm-enable.md) 訊息傳送至視窗。 應用程式可以使用 [**IsWindowEnabled**](/windows/win32/api/winuser/nf-winuser-iswindowenabled) 函數來判斷是否已啟用視窗。

停用子視窗時，系統會將子系的滑鼠輸入訊息傳遞至父視窗。 父系會使用訊息來判斷是否要啟用子視窗。 如需詳細資訊，請參閱 [滑鼠輸入](../inputdev/mouse-input.md)。

一次只能有一個視窗可以接收鍵盤輸入;該視窗稱為鍵盤焦點。 如果應用程式使用 [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) 函式來停用鍵盤焦點視窗，除了停用外，此視窗也會失去鍵盤焦點。 **EnableWindow** 接著會將鍵盤焦點設為 **Null**，表示沒有視窗具有焦點。 如果子視窗或其他子系視窗具有鍵盤焦點，則停用父視窗時，子系視窗會失去焦點。 如需詳細資訊，請參閱 [鍵盤輸入](../inputdev/keyboard-input.md)。

### <a name="window-visibility"></a>視窗可見度

視窗可以顯示或隱藏。 系統會在螢幕上顯示 *可見的視窗* 。 它會隱藏 *隱藏的視窗* ，而不會進行繪製。 如果視窗是顯示的，則使用者可以提供輸入至視窗，並檢視視窗的輸出。 如果隱藏視窗，等於是停用視窗。 隱藏視窗能夠處理來自系統或其他視窗的訊息，但是不能處理來自使用者的輸入或顯示輸出。 應用程式會在建立視窗時設定視窗的可見度狀態。 之後，應用程式可以變更可見度狀態。

當視窗的 [**WS \_ visible**](window-styles.md) 樣式已設定時，就會顯示視窗。 根據預設， [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式會建立隱藏的視窗，除非應用程式指定 **WS \_ 可見** 的樣式。 一般而言，應用程式會在建立視窗之後設定 **WS \_ 可見** 樣式，以保留使用者隱藏的建立程式詳細資料。 例如，應用程式可能會在自訂視窗的外觀時，將新的視窗隱藏起來。 如果在 **CreateWindowEx** 中指定了 **WS \_ VISIBLE** 樣式，系統會在建立視窗之後，但在顯示它之前，將 [**WM \_ SHOWWINDOW**](wm-showwindow.md)訊息傳送至視窗。

應用程式可以使用 [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) 函數來判斷視窗是否可見。 應用程式可以使用 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)、 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)、 [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)或 [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) 或 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函數，顯示 (變成可見) 或隱藏視窗。 這些函式會藉由設定或移除視窗的 [**WS \_ 可見**](window-styles.md) 樣式來顯示或隱藏視窗。 它們也會在顯示或隱藏它之前，將 [**WM \_ SHOWWINDOW**](wm-showwindow.md) 訊息傳送至視窗。

當擁有者視窗最小化時，系統會自動隱藏相關聯的擁有視窗。 同樣地，當擁有者視窗還原時，系統會自動顯示相關聯的擁有視窗。 在這兩種情況下，系統會先將 [**WM \_ SHOWWINDOW**](wm-showwindow.md) 訊息傳送給擁有的視窗，然後再加以隱藏或顯示。 有時候，應用程式可能需要隱藏擁有的視窗，而不需要將擁有者最小化或隱藏。 在此情況下，應用程式會使用 [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) 函數。 此函式會設定或移除所有擁有視窗的 [**WS \_ 可見**](window-styles.md) 樣式，並將 **WM \_ SHOWWINDOW** 訊息傳送給擁有的視窗，然後再隱藏或顯示它們。 隱藏擁有者視窗不會影響所擁有視窗的可見度狀態。

當父視窗可見時，也會顯示其相關聯的子視窗。 同樣地，當父視窗隱藏時，也會隱藏其子視窗。 最小化父視窗不會影響子視窗的可見度狀態;亦即，子視窗會與父系最小化，但不會變更 [**WS \_ 可見**](window-styles.md) 樣式。

即使視窗具有 [**WS \_ 可見**](window-styles.md) 樣式，使用者可能還是看不到畫面上的視窗; 其他視窗可能會完全重迭，或移到螢幕邊緣之外。 此外，可見的子視窗會受其父子式關聯性所建立的裁剪規則所規範。 如果看不到視窗的父視窗，也不會顯示它。 如果父視窗移動超過螢幕邊緣，子視窗也會移動，因為相對於父代的左上角繪製了子視窗。 例如，使用者可以將包含子視窗的父視窗，從畫面的邊緣移到足夠的範圍，讓使用者看不到子視窗，即使子視窗及其父視窗都具有 **WS \_ 可見** 樣式也一樣。

### <a name="minimized-maximized-and-restored-windows"></a>最小化、最大化和還原的視窗

*最大化的視窗* 是具有 [**WS \_ 最大化**](window-styles.md)樣式的視窗。 根據預設值，系統會將最大化視窗放大到佔滿畫面，如果是子視窗，則是放大到佔滿父視窗的工作區 (Client Area)。 雖然視窗的大小可以設定為最大化視窗的大小，但是最大化的視窗會稍有不同。 系統會自動將視窗的標題列移到螢幕頂端，或移至父視窗工作區的頂端。 此外，系統會停用視窗的大小調整框線以及標題列 (的視窗定位功能，讓使用者無法藉由拖曳標題列) 來移動視窗。

*最小化視窗* 是具有 [**WS \_ 最小化**](window-styles.md)樣式的視窗。 根據預設值，系統會將最小化的視窗縮小到工作列按鈕的大小，並將最小化的視窗移至工作列。 *還原的視窗* 是已回到先前大小和位置的視窗，也就是最小化或最大化之前的大小。

如果應用程式在 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式中指定 [**ws \_ 最大化**](window-styles.md)或最 **\_ 小化** 樣式，則會先將視窗最大化或最小化。 建立視窗之後，應用程式可以使用 [**closewindowsg**](/windows/win32/api/winuser/nf-winuser-closewindow) 函式，將視窗最小化。 [**ArrangeIconicWindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows)函式會將圖示排列在桌面上，或將父視窗的最小化子視窗排列在父視窗中。 [**OpenIcon**](/windows/win32/api/winuser/nf-winuser-openicon)函式會將最小化的視窗還原為其先前的大小和位置。

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)函數可以將視窗最小化、最大化或還原。 它也可以設定視窗的可見度和啟用狀態。 [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)函式包含與 **ShowWindow** 相同的功能，但它可以覆寫視窗的預設最小化、最大化和還原的位置。

[**IsZoomed**](/windows/win32/api/winuser/nf-winuser-iszoomed)和 [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic)函式會判斷指定的視窗是否會分別最大化或最小化。 [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement)函式會抓取視窗的最小化、最大化和還原位置，也會決定視窗的顯示狀態。

當系統收到命令以最大化或還原最小化的視窗時，會傳送一個 [**WM \_ QUERYOPEN**](wm-queryopen.md) 訊息給視窗。 如果視窗程式傳回 **FALSE**，則系統會忽略最大化或還原命令。

系統會自動將最大化視窗的大小和位置設定為最大化視窗的系統定義預設值。 若要覆寫這些預設值，應用程式可以呼叫 [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) 函式，或處理當系統即將將視窗最大化時，由視窗接收的 [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) 訊息。 **WM \_GETMINMAXINFO** 包含 [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) 結構的指標，其中包含系統用來設定最大值和位置的值。 取代這些值會覆寫預設值。

## <a name="window-size-and-position"></a>視窗大小和位置

視窗的大小和位置會表示為周框，以相對於螢幕或父視窗的座標來表示。 最上層視窗的座標是相對於畫面的左上角;子視窗的座標是相對於父視窗的左上角。 應用程式會在建立視窗時指定視窗的初始大小和位置，但可以隨時變更視窗的大小和位置。 如需詳細資訊，請參閱 [填滿的圖形](../gdi/filled-shapes.md)。

本節包含下列主題：

-   [預設大小和位置](#default-size-and-position)
-   [追蹤大小](#tracking-size)
-   [系統命令](#system-commands)
-   [大小和位置函式](#size-and-position-functions)
-   [大小和位置訊息](#size-and-position-messages)

### <a name="default-size-and-position"></a>預設大小和位置

應用程式可讓系統藉由 \_ 在 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)中指定 CW USEDEFAULT 來計算最上層視窗的初始大小或位置。 如果應用程式將視窗的座標設定為 [CW USEDEFAULT]， \_ 而且尚未建立任何其他最上層視窗，系統會設定新視窗相對於螢幕左上角的位置; 否則，它會設定相對於最上層視窗的位置，而該位置是最近建立的應用程式。 如果 [寬度] 和 [高度] 參數設定為 [CW \_ USEDEFAULT]，系統就會計算新視窗的大小。 如果應用程式已建立其他最上層視窗，系統會根據應用程式最近建立之最上層視窗的大小，以新視窗的大小為基礎。 \_在建立子系或快顯視窗時指定 CW USEDEFAULT，會導致系統將視窗的大小設定為預設的最小視窗大小。

### <a name="tracking-size"></a>追蹤大小

系統會維持 [**WS \_ THICKFRAME**](window-styles.md) 樣式視窗的最小和最大追蹤大小; 此樣式的視窗具有調整大小框線。 *最小追蹤大小* 是您可以藉由拖曳視窗的大小調整框線來產生的最小視窗大小。 同樣地， *追蹤大小上限* 是您可以藉由拖曳調整大小框線來產生的最大視窗大小。

當系統建立視窗時，視窗的最小和最大追蹤大小會設定為系統定義的預設值。 應用程式可以藉由處理 [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) 訊息來探索預設值並加以覆寫。 如需詳細資訊，請參閱 [大小和位置訊息](#size-and-position-messages)。

### <a name="system-commands"></a>系統命令

具有 [視窗] 功能表的應用程式可以藉由傳送系統命令來變更該視窗的大小和位置。 當使用者從 [視窗] 功能表選擇命令時，會產生系統命令。 應用程式可以藉由將 [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) 訊息傳送至視窗，來模擬使用者動作。 下列系統命令會影響視窗的大小和位置。



| 命令      | 描述                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SC \_ CLOSE    | 關閉視窗。 此命令會將 [**WM \_ 關閉**](wm-close.md) 訊息傳送至視窗。 視窗會執行清除和終結的任何必要步驟。 |
| SC \_ 最大化 | 將視窗最大化。                                                                                                                                                |
| SC \_ 最小化 | 將視窗最小化。                                                                                                                                                |
| SC \_ 移動     | 移動視窗。                                                                                                                                                    |
| SC \_ 還原  | 將最小化或最大化的視窗還原為其先前的大小與位置。                                                                                          |
| SC \_ 大小     | 啟動 size 命令。 若要變更視窗的大小，請使用滑鼠或鍵盤。                                                                                  |



 

### <a name="size-and-position-functions"></a>大小和位置函式

建立視窗之後，應用程式可以藉由呼叫數個不同函式的其中一個來設定視窗的大小或位置，包括 [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)、 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)、 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)和 [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)。 **SetWindowPlacement** 會設定視窗的最小位置、最大化的位置、還原的大小和位置，以及顯示狀態。 **MoveWindow** 和 **SetWindowPos** 函數很類似;同時設定單一應用程式視窗的大小或位置。 **SetWindowPos** 函式包含一組會影響視窗顯示狀態的旗標;**MoveWindow** 不包含這些旗標。 您可以使用 [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)、 **DeferWindowPos** 和 [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) 函式，同時設定許多視窗的位置，包括大小、位置、以 z 順序排列的位置，以及顯示狀態。

應用程式可以使用 [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) 函式來取得視窗周框矩形的座標。 **GetWindowRect** 會以視窗左上角和右下角的座標來填滿 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構。 座標是相對於螢幕左上角，甚至是子視窗。 [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient)或 [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints)函式會將子視窗周框矩形的螢幕座標，對應至父視窗工作區的相對座標。

[**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect)函式會捕獲視窗工作區的座標。 **GetClientRect** 會使用工作區左上角和右下角的座標來填滿 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構，但是座標是相對於用戶端區域本身。 這表示用戶端區域左上角的座標一律是 (0、0) ，而右下角的座標則是工作區的寬度和高度。

[**CascadeWindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows)函式會將桌面上的視窗進行級聯，或將所指定父視窗的子視窗進行串聯。 [**TileWindows**](/windows/win32/api/winuser/nf-winuser-tilewindows)函式會在桌面上並排顯示視窗，或將所指定父視窗的子視窗磚。

### <a name="size-and-position-messages"></a>大小和位置訊息

系統會將 [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) 訊息傳送到其大小或位置即將變更的視窗。 例如，當使用者按一下 [視窗] 功能表中的 [ **移動** ] 或 [ **大小** ]，或按一下調整大小框線或標題列時，就會傳送訊息。當應用程式呼叫 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 來移動或調整視窗大小時，也會傳送此訊息。 **WM \_GETMINMAXINFO** 包含 [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) 結構的指標，其中包含視窗的預設最大大小和位置，以及預設的最小和最大追蹤大小。 應用程式可以藉由處理 **WM \_ GETMINMAXINFO** 並設定適當的 **MINMAXINFO** 成員，來覆寫預設值。 視窗必須有 [**ws \_ THICKFRAME**](window-styles.md) 或 **ws \_ 標題** 樣式才能接收 **WM \_ GETMINMAXINFO**。 具有 **WS \_ THICKFRAME** 樣式的視窗會在視窗建立過程中，以及在移動或調整大小時收到此訊息。

系統會將 [**WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md) 訊息傳送至視窗，該視窗的大小、位置、位置以迭置順序表示，或顯示狀態即將變更。 此訊息包含 [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) 結構的指標，此結構會指定視窗的新大小、位置、以 z 順序排列的位置，以及顯示狀態。 藉由設定 **WINDOWPOS** 的成員，應用程式可能會影響視窗的新大小、位置和外觀。

以迭置順序變更視窗的大小、位置、位置，或顯示狀態之後，系統會將 [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) 訊息傳送至視窗。 此訊息包含 [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) 的指標，該指標會通知視窗其新的大小、位置、在迭置順序中的位置，並顯示狀態。 設定以 **WM \_ WINDOWPOSCHANGED** 傳遞之 **WINDOWPOS** 結構的成員，對此視窗沒有任何作用。 必須處理 [**wm \_ 大小**](wm-size.md) 和 [**WM \_ 移動**](wm-move.md) 訊息的視窗必須將 **wm \_ WINDOWPOSCHANGED** 傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式; 否則，系統不會傳送 **wm \_ 大小** 和 **wm 將訊息 \_ 移** 至視窗。

當建立或調整視窗大小時，系統會將 [**WM \_ NCCALCSIZE**](wm-nccalcsize.md) 訊息傳送至視窗。 系統會使用訊息來計算視窗工作區的大小，以及相對於視窗左上角的工作區位置。 視窗通常會將此訊息傳遞至預設視窗程式;不過，在調整視窗大小時，在自訂視窗的非工作區或保留部分工作區的應用程式中，此訊息可能很有用。 如需詳細資訊，請參閱 [繪製和繪製](../gdi/painting-and-drawing.md)。

## <a name="window-animation"></a>視窗動畫

您可以使用 [**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow) 函式，在顯示或隱藏視窗時產生特殊效果。 以這種方式繪製視窗動畫時，系統會根據您在 **AnimateWindow** 的呼叫中指定的旗標，來變換、滑動或淡化視窗。

根據預設，系統會使用 *滾動動畫*。 使用此效果時，視窗會顯示為 [已開啟]， (顯示視窗) 或 (隱藏視窗) 的關閉。 您可以使用 *dwFlags* 參數來指定視窗是以水準、垂直或對角線方式進行滾動。

當您指定 **AW 投影 \_ 片** 旗標時，系統會使用投影 *片動畫*。 有了這個效果，視窗就會顯示為滑 (顯示視窗) 或滑出視野 (隱藏視窗) 。 您可以使用 *dwFlags* 參數來指定視窗是否以水準、垂直或對角線方式滑出。

當您指定 **AW \_ BLEND** 旗標時，系統會使用 *Alpha 混合的淡化*。

您也可以使用 [ **AW \_ CENTER** ] 旗標讓視窗出現，以向外或向外擴充。

## <a name="window-layout-and-mirroring"></a>視窗版面配置和鏡像

視窗配置會定義文字和 Windows 圖形裝置介面 (GDI) 物件在視窗或裝置內容 (DC) 中的配置方式。 某些語言（例如英文、法文和德文）需要由左至右 (LTR) 版面配置。 其他語言（例如阿拉伯文和希伯來文）需要由右至左的 (RTL) 版面配置。 視窗配置會套用至文字，但也會影響視窗的其他 GDI 元素，包括點陣圖、圖示、原點位置、按鈕、階層式樹狀結構控制項，以及水準座標是否隨著您往左或右增加。 例如，在應用程式設定了 RTL 版面配置之後，原點位於視窗或裝置的右邊緣，而代表水準座標的數位會隨著您左移而增加。 但是，並非所有物件都會受到視窗版面配置的影響。 例如，您必須個別處理對話方塊的配置、訊息方塊，以及未與視窗相關聯的裝置內容，例如中繼檔和印表機 Dc。 本主題稍後將說明這些細節的詳細資訊。

視窗函式可讓您在阿拉伯文和希伯來文版本的 Windows 中，指定或變更視窗版面配置。 請注意，變更為 RTL 版面配置的 (也稱為鏡像) ，其樣式為 [CS \_ OWNDC](about-window-classes.md) 或具有 GM \_ ADVANCED 圖形模式的 DC 則不支援。

根據預設，視窗版面配置是由左至右 (LTR) 。 若要設定 RTL 視窗版面配置，請使用 " **WS \_ EX \_ LAYOUTRTL**" 的樣式來呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 。 此外，根據預設，子視窗 (也就是，在 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)或 **CreateWindowEx**) 的呼叫中，一個以 [**WS \_ 子**](window-styles.md)樣式建立的，且具有有效的父 *hWnd* 參數，其父代具有相同的版面配置。 若要停用對所有子視窗的鏡像繼承，請在 **CreateWindowEx** 的呼叫中指定 **WS \_ EX \_ NOINHERITLAYOUT** 。 請注意，在不使用 **WS \_ 子** 樣式的情況下建立的 windows (不會繼承鏡像，) 或在 **CreateWindowEx** 中以父 *hWnd* 參數建立的不會被設定為 **Null**。 若要停用個別視窗的鏡像繼承，請使用 [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)和 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)來處理 [**WM \_ NCCREATE**](wm-nccreate.md)訊息，以關閉「 **WS \_ EX \_ LAYOUTRTL** 」旗標。 這項處理是除了需要其他任何處理之外。 下列程式碼片段顯示如何完成這項操作。


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



您可以藉由呼叫 [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) (配置 rtl) ，將預設版面配置設定為 rtl \_ 。 在呼叫之後建立的所有 windows 都會進行鏡像，但是現有的視窗不會受到影響。 若要關閉預設鏡像，請呼叫 **SetProcessDefaultLayout** (0) 。

請注意， [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) 只會鏡像鏡像視窗的 dc。 若要鏡像任何 DC，請呼叫 [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) (hdc，以 RTL 的版面配置 \_) 。 如需詳細資訊，請參閱本主題稍後的鏡像未與 windows 相關聯的鏡像裝置內容討論。

鏡像視窗中的點陣圖和圖示預設也是鏡像的。 但是，並非所有這些都應該鏡像。 例如，具有文字、商務標誌或類比時鐘的那些應用程式不應該鏡像。 若要停用點陣圖鏡像， [](/windows/win32/api/wingdi/nf-wingdi-setlayout)請使用 \_ *DWLAYOUT* 中設定的版面配置 BITMAPORIENTATIONPRESERVED 位來呼叫 SetLayout。 若要停用 DC 中的鏡像，請呼叫 **SetLayout** (hdc，0) 。

若要查詢目前的預設版面配置，請呼叫 [**GetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout)。 在成功傳回時， *pdwDefaultLayout* 會包含 \_ RTL 或0的版面配置。 若要查詢裝置內容的版面配置設定，請呼叫 [**GetLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout)。 在成功傳回時， **GetLayout** 會傳回 **DWORD** ，指出版面配置設定（依 \_ RTL 和版面配置 BITMAPORIENTATIONPRESERVED 位）的版面配置設定 \_ 。

建立視窗之後，您可以使用 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式來變更版面配置。 例如，當使用者將現有視窗的使用者介面語言從阿拉伯文或希伯來文變更為德文時，這是必要的。 不過，在變更現有視窗的配置時，您必須使視窗失效並更新，以確保視窗的內容全都以相同的版面配置繪製。 下列程式碼範例是來自視需要變更視窗版面配置的範例程式碼：


```
// Using ANSI versions of GetWindowLong and SetWindowLong because Unicode
// is not needed for these calls

lExStyles = GetWindowLongA(hWnd, GWL_EXSTYLE);

// Check whether new layout is opposite the current layout
if (!!(pLState -> IsRTLLayout) != !!(lExStyles & WS_EX_LAYOUTRTL))
{
    // the following lines will update the window layout

    lExStyles ^= WS_EX_LAYOUTRTL;        // toggle layout
    SetWindowLongA(hWnd, GWL_EXSTYLE, lExStyles);
    InvalidateRect(hWnd, NULL, TRUE);    // to update layout in the client area
}
```



在鏡像中，您應該考慮「近」和「遠」，而不是「左方」和「右方」。 如果無法這麼做，可能會造成問題。 在 [螢幕座標] 和 [用戶端座標] 之間進行對應時，會導致鏡像視窗發生問題的一個常見程式碼撰寫做法。 例如，應用程式通常會使用類似下列的程式碼，將控制項放在視窗中：


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



這會導致鏡像中的問題，因為矩形的左邊緣變成鏡像視窗中的右邊緣，反之亦然。 若要避免這個問題，請將 [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) 呼叫取代為 [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) 的呼叫，如下所示：


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



這段程式碼的運作方式是因為在支援鏡像的平臺上， [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) 會在用戶端視窗已鏡像時修改，以交換左邊和右點的座標。 如需詳細資訊，請參閱 **MapWindowPoints** 的「備註」一節。

另一個可能在鏡像視窗中造成問題的常見做法，是使用螢幕座標中的位移（而非用戶端座標）來定位用戶端視窗中的物件。 例如，下列程式碼會使用螢幕座標中的差異做為用戶端座標中的 x 位置，以將控制項放置在對話方塊中。


```
// OK if LTR layout and mapping mode of client is MM_TEXT,
// but WRONG for a mirrored dialog 

RECT rdDialog;
RECT rcControl;

HWND hControl = GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hDlg, &rcDialog);             // gets rect in screen coordinates
GetWindowRect(hControl, &rcControl);
MoveWindow(hControl,
           rcControl.left - rcDialog.left,  // uses x position in client coords
           rcControl.top - rcDialog.top,
           nWidth,
           nHeight,
           FALSE);
```



當對話方塊視窗具有從左至右 (LTR) 配置，且用戶端的對應模式為 MM TEXT 時，此程式碼就很好用 \_ ，因為用戶端座標中的新 x 位置會對應到控制項左邊緣的差異和螢幕座標中的對話方塊。 不過，在鏡像對話中，left 和 right 會反轉，因此您應該改為使用 [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) ，如下所示：


```
RECT rcDialog;
RECT rcControl;

HWND hControl - GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hControl, &rcControl);

// MapWindowPoints works correctly in both mirrored and non-mirrored windows.
MapWindowPoints(NULL, hDlg, (LPPOINT) &rcControl, 2);

// Now rcControl is in client coordinates.
MoveWindow(hControl, rcControl.left, rcControl.top, nWidth, nHeight, FALSE)
```



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>鏡像對話方塊和訊息方塊

對話方塊和訊息方塊不會繼承版面配置，因此您必須明確地設定版面配置。 若要建立訊息方塊的鏡像，請使用 **MB \_ RTLREADING** 選項來呼叫 [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)或 [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) 。 若要從右至左配置對話方塊，請 \_ \_ 在 [對話方塊範本結構 [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md)] 中使用擴充樣式 WS EX LAYOUTRTL。 屬性工作表是對話方塊的特殊案例。 每一個索引標籤會被視為個別的對話方塊，所以您需要 \_ 在每個要鏡像的索引標籤中包含 WS EX \_ LAYOUTRTL 樣式。

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>未與視窗相關聯的鏡像裝置內容

未與視窗相關聯的 Dc （例如，中繼檔或印表機 Dc）不會繼承配置，因此您必須明確地設定版面配置。 若要變更裝置內容版面配置，請使用 [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) 函數。

[**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)函式很少用於 windows。 一般而言，windows 只會在處理 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息時接收相關聯的 DC。 有時候，程式會藉由呼叫 [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc)來建立視窗的 DC。 無論何種方式，都會根據視窗的 WS [](/windows/win32/api/winuser/nf-winuser-beginpaint) EX  \_ \_ LAYOUTRTL 旗標，設定 DC 的初始配置 BeginPaint 或 GetDC。

[**GetWindowOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex)、 [**GetWindowExtEx**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex)、 [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex)和 [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex)所傳回的值不會受到呼叫 [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)的影響。

當版面配置為 RTL 時， [**GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) 會傳回 mm （ \_ 而不是 mm \_ TEXT）。 使用 MM TEXT 呼叫 [**SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) \_ 將會正確運作，只會影響來自 **GetMapMode** 的傳回值。 同樣地，呼叫 [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) (hdc， \_ 當對應模式為 mm TEXT 時，會) 配置 RTL， \_ 以將報告的對應模式變更為 mm \_ 各向異性。

## <a name="window-destruction"></a>視窗損毀

一般來說，應用程式必須終結它所建立的所有視窗。 它會使用 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 函式來執行這項工作。 當視窗損毀時，系統會隱藏視窗（如果有的話），然後移除與視窗相關聯的任何內部資料。 這會使視窗控制碼失效，應用程式將無法再使用此控制碼。

應用程式會在建立應用程式之後，立即終結它所建立的許多視窗。 例如，當應用程式有足夠的輸入可繼續其工作時，應用程式通常會立即終結對話方塊視窗。 應用程式最後會在終止) 之前終結應用程式 (的主視窗。

在終結視窗之前，應用程式應該儲存或移除任何與視窗相關聯的資料，而且它應該釋出任何為視窗配置的系統資源。 如果應用程式未釋出資源，系統將會釋放應用程式未釋放的任何資源。

終結視窗並不會影響視窗建立所在的視窗類別。 您仍然可以使用該類別來建立新的視窗，且該類別的任何現有視窗都會繼續運作。 終結視窗也會損毀視窗的子系視窗。 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)函式會先將 [**WM 損 \_ 毀**](wm-destroy.md)訊息傳送至視窗，然後傳送至其子視窗和子系視窗。 如此一來，已終結之視窗的所有子系視窗也會終結。

當使用者按一下 [**關閉**] 時，具有視窗功能表的視窗就會收到 [**WM \_ 關閉**](wm-close.md)訊息。 藉由處理此訊息，應用程式可以在終結視窗之前提示使用者進行確認。 如果使用者確認應該終結視窗，應用程式可以呼叫 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 函式來終結視窗。

如果正在終結的視窗是作用中視窗，作用中和焦點狀態都會傳送到另一個視窗。 成為使用中視窗的視窗是下一個視窗，由 ALT + ESC 鍵組合所決定。 新的使用中視窗接著會決定哪個視窗接收到鍵盤焦點。

 

 
