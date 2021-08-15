---
title: 關於資料指標
description: 本主題討論標準資料指標。
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- 資源，資料指標
- 資料指標，關於
- 資料指標，標準
- 標準資料指標
- SetSystemCursor 函式
- 資料指標，自訂
- 自訂資料指標
- 資料指標，作用點
- 資料指標，建立
- 建立資料指標
- 資料指標，位置
- 資料指標，外觀
- 終結資料指標
- 複製資料指標
- 類別資料指標
- 將資料指標
- 資料指標，終結
- 資料指標，複製
- 資料指標、類別
- 資料指標，將
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8d987eb12857779ac85d34cb7e4ff7f3f5ce59ed8a750764c433c88abbccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735374"
---
# <a name="about-cursors"></a>關於資料指標

Windows 提供一組標準資料指標，可供任何應用程式在任何時間使用。 SDK 標頭檔包含標準資料指標的識別碼，識別碼開頭為 **IDC \_** 前置詞。

每一個標準游標都有與其關聯之相對應的預設影像。 使用者或應用程式可以隨時取代與任何標準資料指標相關聯的預設影像。 應用程式會使用 [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) 函數來取代預設影像。 下圖顯示 Windows Vista 的數個標準資料指標：

![標準資料指標，包括手、四箭號加號、有問號的箭號、圓形、畫筆](images/cursorsstandard.png)

應用程式可以使用 [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) 函式來取出資料指標目前的影像，而且可以使用 [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) 函數來繪製資料指標。 若要繪製標準資料指標的預設影像，請在 **DrawIconEx** 的呼叫中指定 **DI \_ 相容** 性旗標。 如果您未指定 **DI \_ 相容** 性旗標， **DrawIconEx** 會使用使用者指定的影像繪製標準資料指標。

自訂資料指標是設計用來在特定應用程式中使用，而且可以是開發人員所定義的設計。 下圖顯示數個自訂資料指標。

![自訂資料指標，包括手形、banana、鼓、wristwatch、metronome](images/cursorscustom.png)

資料指標可以是單色或色彩，也可以是靜態或動畫。 特定電腦系統上所使用的資料指標類型取決於系統的顯示。 舊的顯示器（例如 VGA）不支援色彩或動畫游標。 新顯示器，其顯示驅動程式會使用與裝置無關的點陣圖 (DIB) 引擎支援它們。

資料指標和圖示很類似，而且在許多情況下都可以交替使用。 兩者之間唯一的差異在於，指定為數據指標的影像必須採用顯示器可支援的格式。 例如，資料指標必須是單色才能顯示 VGA。

本總覽提供下列主題的相關資訊：

-   [作用點](#the-hot-spot)
-   [滑鼠和游標](#the-mouse-and-the-cursor)
-   [資料指標建立](#cursor-creation)
-   [游標位置和外觀](#cursor-location-and-appearance)
-   [資料指標 Confinement](#cursor-confinement)
-   [資料指標損毀](#cursor-destruction)
-   [資料指標重複](#cursor-duplication)
-   [視窗類別游標](#the-window-class-cursor)

## <a name="the-hot-spot"></a>作用點

在資料指標中，稱為「 *作用點* 」的圖元會標示受滑鼠事件影響的確切畫面位置，例如按一下滑鼠按鍵。 通常，作用點是資料指標的焦點。 系統會追蹤此點，並將其辨識為數據指標的位置。 例如，一般的作用點是箭號形狀游標的尖端圖元，以及十字形狀游標中間的圖元。 下列影像顯示來自繪圖程式的兩個數據指標，其中的作用點與筆刷的秘訣相關聯，而繪製的十字線則可以。

![兩個數據指標上的作用點](images/cursorhotspot.png)

當滑鼠輸入事件發生時，滑鼠驅動程式會將事件轉譯為適當的滑鼠訊息，其中包含作用點的座標。 系統會將滑鼠訊息傳送至視窗，其中包含作用點或正在捕捉滑鼠輸入的視窗。 如需詳細資訊，請參閱 [滑鼠輸入](/windows/desktop/inputdev/mouse-input)。

## <a name="the-mouse-and-the-cursor"></a>滑鼠和游標

系統會將游標移至畫面上，以反映滑鼠的移動。 當游標移至不同的視窗部分或不同的視窗時，系統 (或應用程式) 變更游標的外觀。 例如，當資料指標跨越超連結時，系統會將游標從箭號變更為手。

![超連結時，標準資料指標變更為手形](images/cursorchangingstate.png)

如果系統沒有滑鼠，系統只會在使用者選擇特定的系統命令（例如用來調整視窗大小或移動視窗）時，才會顯示並移動游標。 若要為使用者提供當無法使用滑鼠時顯示和移動游標的方法，應用程式可以使用資料指標函式來模擬滑鼠移動。 由於這項模擬功能，使用者可以使用方向鍵來移動游標。

## <a name="cursor-creation"></a>資料指標建立

因為標準資料指標是預先定義的，所以不需要建立它們。 若要使用標準資料指標，應用程式會使用 [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) 或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 函數來抓取資料指標控制碼。 資料 *指標控制碼* 是識別標準或自訂資料指標之 **HCURSOR** 類型的唯一值。

若要建立應用程式的自訂資料指標，您通常會使用圖形應用程式，並在應用程式的資源定義檔中包含資料指標做為資源。 在執行時間，呼叫 [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) 以取得資料指標控制碼。 資料指標資源包含數種不同顯示裝置的資料。 **LoadCursor** 函式會自動選取最適合目前顯示裝置的資料。 從直接載入資料指標。的或。ANI 檔案，請使用 [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea) 函數。

您也可以在執行時間使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函式建立自訂資料指標，該函數會根據 [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) 結構的內容建立資料指標。 [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)函式會以作用點座標和相關遮罩和色彩的相關資訊來填滿此結構。

應用程式應該將自訂資料指標實作為資源，並使用 [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)、 [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) ，而不是在執行時間建立資料指標。 使用資料指標資源可避免裝置的相依性、簡化當地語系化，以及讓應用程式共用資料指標設計。

[**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)函式可讓應用程式根據資源資料建立圖示和資料指標。 **CreateIconFromResourceEx** 會根據二進位資源資料，從其他可執行檔 (.exe) 檔案或 dll 中建立資料指標。 它之前必須先呼叫 [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) 函式，以及數個資源函數。 **LookupIconIdFromDirectoryEx** 會識別目前顯示裝置最適當的資料指標資料。 如需資源函式的詳細資訊，請參閱 [資源](resources.md)。

## <a name="cursor-location-and-appearance"></a>游標位置和外觀

系統會自動顯示滑鼠游標，並更新其在畫面上的位置。 您可以使用 [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) 和 [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) 函式，取得游標目前的螢幕座標，並將游標移至畫面上的任何位置。

您也可以使用 [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) 函數來抓取目前資料指標的控制碼，而且可以使用 [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) 函數來設定資料指標。 呼叫 **SetCursor** 之後，游標的外觀不會變更，直到滑鼠移動、將游標明確設定為不同的資料指標，或執行系統命令。

當使用者移動滑鼠時，系統會在新位置重新繪製游標。 系統會自動重新繪製與游標所指向之視窗相關聯的資料指標設計。

您可以使用 [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor) 函數，隱藏和重新顯示資料指標，而不需要變更資料指標設計。 此函數會使用內部計數器來決定何時要隱藏或顯示資料指標。 嘗試顯示資料指標會遞增計數器。嘗試隱藏資料指標會遞減計數器。 只有當這個計數器大於或等於零時，才會顯示資料指標。

[**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)函式會取得全域資料指標的下列資訊：資料指標是否隱藏或顯示、資料指標的控制碼，以及資料指標的座標。

## <a name="cursor-confinement"></a>資料指標 Confinement

您可以使用 [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) 函式，將游標限制在螢幕上的矩形區域。 當使用者必須在矩形的限制區域內回應某個事件時，這非常有用。 例如，您可以使用 **ClipCursor** 將資料指標限制為強制回應對話方塊，以防止使用者在對話方塊關閉之前與其他視窗互動。

[**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)函式會抓取暫時限制游標的矩形區域螢幕座標。 當需要限制資料指標時，您也可以使用這個函數來儲存可以移動資料指標的原始區域座標。 然後，您可以在不再需要新的 confinement 時，將游標還原到原始區域。

## <a name="cursor-destruction"></a>資料指標損毀

您可以終結資料指標控制碼，並釋放呼叫 [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) 函數所使用的資料指標。 不過，此函數對共用資料指標沒有任何作用。 只要已載入它的模組保留在記憶體中，共用資料指標就會有效。 下列函數會取得共用資料指標：

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   如果您使用 **LR \_ 共用** 旗標， [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) () 
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (如果您使用 **LR \_ COPYRETURNORG** 旗標，且 *hImage* 是共用的資料指標) 

當您不再需要使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函數所建立的資料指標時，您應該終結資料指標。 [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)函式會終結資料指標控制碼，並釋放資料指標所使用的任何記憶體。 此函數僅適用于使用 **CreateIconIndirect** 所建立的資料指標。

## <a name="cursor-duplication"></a>資料指標重複

[**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)函式會複製資料指標控制碼。 這可讓應用程式或 DLL 程式碼抓取另一個模組所擁有之資料指標的控制碼。 然後，如果釋放其他模組，則複製資料指標的模組仍然可以使用資料指標設計。

如需有關如何在可執行檔中加入、移除或取代資料指標資源的詳細資訊，請參閱 [資源](resources.md)。

## <a name="the-window-class-cursor"></a>視窗類別游標

當您使用 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) 函式註冊視窗類別時，您可以為它指派預設的資料指標，稱為 *類別資料指標*。 在應用程式註冊視窗類別之後，該類別的每個視窗都會有指定的類別游標。

若要覆寫類別資料指標，請處理 [**WM \_ SETCURSOR**](wm-setcursor.md) 訊息。 您也可以使用 [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) 函數來取代類別資料指標。 此函式會變更指定類別之所有視窗的預設視窗設定。 如需詳細資訊，請參閱 [類別游標](/windows/desktop/winmsg/about-window-classes)。

 

 