---
description: 每個視窗類別都有一個相關聯的視窗程式，由相同類別的所有視窗共用。 視窗程式會處理該類別的所有視窗的訊息，因此會控制其行為和外觀。
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: 關於視窗類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b683176c3fd7904cf3f89b385ce0fa393b89e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194567"
---
# <a name="about-window-classes"></a>關於視窗類別

每個視窗類別都有一個相關聯的視窗程式，由相同類別的所有視窗共用。 視窗程式會處理該類別的所有視窗的訊息，因此會控制其行為和外觀。 如需詳細資訊，請參閱 [Window 程序](window-procedures.md)。

處理常式必須先註冊視窗類別，才能建立該類別的視窗。 註冊視窗類別會將視窗程式、類別樣式和其他類別屬性與類別名稱產生關聯。 當進程在 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式中指定類別名稱時，系統會建立一個視窗，其中含有與該類別名稱相關聯的視窗程式、樣式和其他屬性。

本節將討論下列主題。

-   [視窗類別的類型](#types-of-window-classes)
    -   [系統類別](#system-classes)
    -   [應用程式全域類別](#application-global-classes)
    -   [應用程式區域類別](#application-local-classes)
-   [系統如何尋找視窗類別](#how-the-system-locates-a-window-class)
-   [註冊視窗類別](#registering-a-window-class)
-   [視窗類別的元素](#elements-of-a-window-class)
    -   [類別名稱](#class-name)
    -   [視窗程式位址](#window-procedure-address)
    -   [執行個體控制代碼][](#instance-handle)
    -   [類別資料指標](#class-cursor)
    -   [類別圖示](#class-icons)
    -   [類別背景筆刷](#class-background-brush)
    -   [類別功能表](#class-menu)
    -   [類別樣式][](#class-styles)
    -   [額外類別記憶體](#extra-class-memory)
    -   [額外的視窗記憶體](#extra-window-memory)

## <a name="types-of-window-classes"></a>視窗類別的類型

有三種類型的視窗類別：

-   [系統類別](#system-classes)
-   [應用程式全域類別](#application-global-classes)
-   [應用程式區域類別](#application-local-classes)

這些類型在範圍內與註冊和終結的方式和方式不同。

### <a name="system-classes"></a>系統類別

系統類別是系統註冊的視窗類別。 許多系統類別都可供所有程式使用，而有些則只會由系統在內部使用。 由於系統會註冊這些類別，因此進程無法終結它們。

系統會線上程第一次呼叫使用者或 Windows 圖形裝置介面 (GDI) 函式時，註冊進程的系統類別。

每個應用程式都會收到自己的系統類別複本。 相同的 VDM 中所有16位 Windows 應用程式都會共用系統類別，就像在16位的 Windows 上一樣。

下表描述可供所有進程使用的系統類別。



| 類別     | 描述                         |
|-----------|-------------------------------------|
| 按鈕    | 按鈕的類別。             |
| ComboBox  | 下拉式方塊的類別。          |
| 編輯      | 編輯控制項的類別。      |
| ListBox   | 清單方塊的類別。           |
| MDIClient | MDI 用戶端視窗的類別。 |
| ScrollBar | 捲軸的類別。         |
| Static    | 靜態控制項的類別。     |



 

下表說明僅供系統使用的系統類別。 在這裡會列出它們，以確保完整性。



| 類別      | 描述                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | 下拉式方塊中所含清單方塊的類別。                   |
| DDEMLEvent | 動態資料交換管理程式庫的類別會 (DDEML) 事件。 |
| 訊息    | 僅限訊息視窗的類別。                                   |
| \#32768    | 功能表的類別。                                                  |
| \#32769    | 桌面視窗的類別。                                      |
| \#32770    | 對話方塊的類別。                                            |
| \#32771    | 工作切換視窗的類別。                                  |
| \#32772    | 圖示標題的類別。                                             |



 

### <a name="application-global-classes"></a>應用程式全域類別

[應用程式全域類別](#application-global-classes)是由可執行檔或 DLL 註冊的視窗類別，可供進程中的所有其他模組使用。 例如，您的 .dll 可以呼叫 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) 函式，以註冊將自訂控制項定義為應用程式全域類別的視窗類別，讓載入 .dll 的進程可以建立自訂控制項的實例。

若要建立可用於每個進程的類別，請在 .dll 中建立視窗類別，並在每個進程中載入 .dll。 若要在每個進程中載入 .dll，請在下列登錄機碼中，將其名稱加入至 **AppInit \_ dll** 值：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

每次處理常式啟動時，系統就會在新啟動的進程的內容中載入指定的 .dll，然後呼叫其進入點函數。 .Dll 必須在其初始化程式中註冊類別，而且必須指定 **CS \_ GLOBALCLASS** 樣式。 如需詳細資訊，請參閱 [類別樣式](#class-styles)。

若要移除應用程式全域類別並釋放與其相關聯的儲存體，請使用 [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) 函數。

### <a name="application-local-classes"></a>應用程式區域類別

[應用程式區域類別](#application-local-classes)是可執行檔或 .dll 註冊以供其獨佔使用的任何視窗類別。 雖然您可以註冊任意數目的本機類別，但通常只會註冊一個。 此視窗類別支援應用程式主視窗的視窗程式。

當註冊的模組關閉時，系統會終結區域類別。 應用程式也可以使用 [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) 函式來移除區域類別，並釋放與其相關聯的儲存體。

## <a name="how-the-system-locates-a-window-class"></a>系統如何尋找視窗類別

系統會為這三種視窗類別的類型維護一份結構清單。 當應用程式呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式來建立具有指定類別的視窗時，系統會使用下列程式來找出類別。

1.  搜尋具有指定名稱之類別的應用程式區域類別清單，其實例控制碼符合模組的實例控制碼。  (數個模組可使用相同的名稱，在相同的進程中註冊本機類別。 ) 
2.  如果名稱不在 [應用程式區域類別] 清單中，請搜尋應用程式全域類別的清單。
3.  如果名稱不在 [應用程式全域類別] 清單中，請搜尋系統類別清單。

應用程式所建立的所有視窗都會使用此程式，包括代表系統在應用程式上建立的 windows，例如對話方塊。 您可以覆寫系統類別，而不會影響其他應用程式。 也就是說，應用程式可以註冊應用程式區域類別，其名稱與系統類別相同。 這會取代應用程式內容中的系統類別，但不會防止其他應用程式使用系統類別。

## <a name="registering-a-window-class"></a>註冊視窗類別

視窗類別會定義視窗的屬性，例如其樣式、圖示、游標、功能表和視窗程式。 註冊視窗類別的第一個步驟是在 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構中填入視窗類別資訊。 如需詳細資訊，請參閱 [視窗類別的元素](#elements-of-a-window-class)。 接下來，將結構傳遞給 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) 函數。 如需詳細資訊，請參閱 [使用視窗類別](using-window-classes.md)。

若要註冊應用程式全域類別，請 \_ 在 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **STYLE** 成員中指定 CS GLOBALCLASS 樣式。 註冊應用程式區域類別時，請勿指定 **CS \_ GLOBALCLASS** 樣式。

如果您使用 ANSI 版本的 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)（ **RegisterClassExA**）來註冊視窗類別，則應用程式會要求系統使用 ansi 字元集將訊息的文字參數傳遞至所建立類別的視窗;如果您使用 Unicode 版本的 **RegisterClassEx**（ **RegisterClassExW**）來註冊類別，則應用程式會要求系統使用 unicode 字元集，將訊息的文字參數傳遞至所建立類別的視窗。 [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode)函數可讓應用程式查詢每個視窗的本質。 如需有關 ANSI 和 Unicode 函數的詳細資訊，請參閱 [函數原型的慣例](/windows/desktop/Intl/conventions-for-function-prototypes)。

註冊類別的可執行檔或 DLL 是類別的擁有者。 當註冊類別時，系統會從傳遞給 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)函式之 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hInstance** 成員判斷類別擁有權。 若為 Dll， **hInstance** 成員必須是 .dll 實例的控制碼。

當擁有它的 .dll 卸載時，不會終結類別。 因此，如果系統呼叫該類別之視窗的視窗程式，則會造成存取違規，因為包含視窗程式的 .dll 已不在記憶體中。 此程式必須在卸載 .dll 之前使用類別終結所有視窗，然後呼叫 [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) 函數。

## <a name="elements-of-a-window-class"></a>視窗類別的元素

視窗類別的元素會定義屬於類別之 windows 的預設行為。 註冊視窗類別的應用程式會在 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構中設定適當的成員，並將結構傳遞至 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) 函式，以將元素指派給類別。 [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)和 [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)函式會取得指定之視窗類別的相關資訊。 [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga)函式會變更應用程式已經註冊之本機或全域類別的元素。

雖然完整的視窗類別包含許多元素，但系統只要求應用程式提供類別名稱、視窗程式位址和實例控制碼。 您可以使用其他元素來定義類別視窗的預設屬性，例如游標的形狀和視窗的功能表內容。 您必須將 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構中任何未使用的成員初始化為零或 **Null**。 視窗類別元素如下表所示。



| 元素                                               | 目的                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [類別名稱](#class-name)                             | 區分類別與其他已註冊的類別。                                                                                                                                                                                        |
| [視窗程式位址](#window-procedure-address) | 函式的指標，該函式會處理傳送至類別中之 windows 的所有訊息，並定義視窗的行為。                                                                                                                      |
| [執行個體控制代碼][](#instance-handle)                   | 識別註冊類別的應用程式或 .dll。                                                                                                                                                                                 |
| [類別資料指標](#class-cursor)                         | 定義系統為類別的視窗顯示的滑鼠游標。                                                                                                                                                                  |
| [類別圖示](#class-icons)                           | 定義大型圖示和小圖示。                                                                                                                                                                                                    |
| [類別背景筆刷](#class-background-brush)     | 定義在開啟或繪製視窗時，填滿工作區的色彩和模式。                                                                                                                                                 |
| [類別功能表](#class-menu)                             | 指定未明確定義功能表的 windows 預設功能表。                                                                                                                                                                  |
| [類別樣式][](#class-styles)                         | 定義如何在移動或調整視窗大小時，更新視窗、如何處理滑鼠的按兩下、如何針對裝置內容配置空間，以及視窗的其他層面。                                                       |
| [額外類別記憶體](#extra-class-memory)             | 指定系統應為類別保留的額外記憶體量（以位元組為單位）。 類別中的所有視窗都會共用額外的記憶體，而且可以將它用於任何應用程式定義的用途。 系統會將此記憶體初始化為零。 |
| [額外的視窗記憶體](#extra-window-memory)           | 指定系統應為屬於類別的每個視窗保留的額外記憶體量（以位元組為單位）。 額外的記憶體可用於任何應用程式定義的用途。 系統會將此記憶體初始化為零。          |



 

### <a name="class-name"></a>類別名稱

每個視窗類別都需要 [類別名稱](#class-name) ，才能區分某個類別與另一個類別。 將 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **lpszClassName** 成員設定為指定名稱之以 null 結束的字串位址，藉以指派類別名稱。 因為視窗類別是進程特定的，所以視窗類別名稱在相同的進程中必須是唯一的。 此外，由於類別名稱會佔用系統私用 atom 資料表中的空間，因此您應該盡可能將類別名稱字串保持在最短的位置。

[**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)函式會抓取給定視窗所屬類別的名稱。

### <a name="window-procedure-address"></a>視窗程式位址

每個類別都需要一個視窗程式位址，以定義視窗程式的進入點，用來處理類別中的所有 windows 訊息。 當系統要求視窗執行工作時，系統會將訊息傳遞至程式，例如，繪製其工作區或回應使用者的輸入。 進程會將視窗程式指派給類別，方法是將其位址複製到 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **lpfnWndProc** 成員。 如需詳細資訊，請參閱 [Window 程序](window-procedures.md)。

### <a name="instance-handle"></a>[執行個體控制代碼]

每個視窗類別都需要實例控制碼，以識別註冊類別的應用程式或 .dll。 系統需要實例控制碼來追蹤所有模組。 系統會將控制碼指派給執行中的可執行檔或 .dll 的每個複本。

系統會將實例控制碼傳遞至每個可執行檔的進入點函數 (請參閱 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) 和 .dll (查看 [**DllMain**](/windows/desktop/Dlls/dllmain)) 。 可執行檔或 .dll 會將這個實例控制碼複製到 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hInstance** 成員，藉此將這個實例控制碼指派給類別。

### <a name="class-cursor"></a>類別資料指標

當 *資料指標位於* 類別中視窗的工作區時，會定義資料指標的形狀。 當游標進入視窗的工作區時，系統會自動將游標設定為指定的圖形，並確保它會保留在工作區中。 若要將資料指標圖形指派給視窗類別，請使用 [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora)函數載入預先定義的資料指標圖形，然後將傳回的資料指標控制碼指派給 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hCursor** 成員。 或者，提供自訂的資料指標資源，並使用 **LoadCursor** 函式從應用程式的資源載入它。

系統不需要類別資料指標。 如果應用程式將 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hCursor** 成員設定為 **Null**，則不會定義任何類別資料指標。 系統會假設在每次游標移至視窗時，視窗都會設定資料指標圖形。 視窗可以在每次視窗收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)訊息時呼叫 [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor)函式，藉以設定資料指標圖形。 如需資料指標的詳細資訊，請參閱資料 [指標](/windows/desktop/menurc/cursors)。

### <a name="class-icons"></a>類別圖示

*類別圖示* 是系統用來表示特定類別之視窗的圖片。 應用程式可以有兩個類別圖示—一個是大型的，一個很小。 當使用者按下 ALT + TAB，以及在工作列和 explorer 的大型圖示視圖中時，系統會在工作切換視窗中顯示視窗的 *大型類別圖示* 。 *小型類別圖示* 會出現在視窗的標題列，以及工作列和 explorer 的小圖示視圖中。

若要將大型和小型圖示指派給視窗類別，請在 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hIcon** 和 **hIconSm** 成員中指定圖示的控制碼。 圖示維度必須符合大型和小型類別圖示的必要維度。 針對大型類別的圖示，您可以在 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)函式的呼叫中指定 **Sm \_ CXICON** 和 **sm \_ CYICON** 值，以判斷所需的維度。 若為小型類別圖示，請指定 **sm \_ CXSMICON** 和 **sm \_ CYSMICON** 值。 如需詳細資訊，請參閱 [圖示](/windows/desktop/menurc/icons)。

如果應用程式將 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hIcon** 和 **hIconSm** 成員設為 **Null**，系統就會使用預設應用程式圖示作為視窗類別的大型和小型類別圖示。 如果您指定大型類別圖示，而不是小圖示，系統會根據大型類別圖示來建立小型類別圖示。 但是，如果您指定小型類別圖示，但不是大型類別圖示，系統會使用預設應用程式圖示作為大型類別圖示，並使用指定的圖示作為小型類別圖示。

您可以使用 [**WM \_ SETICON**](wm-seticon.md) 訊息，覆寫特定視窗的大型或小型類別圖示。 您可以使用 [**WM \_ GETICON**](wm-geticon.md) 訊息來取出目前的大型或小型類別圖示。

### <a name="class-background-brush"></a>類別背景筆刷

*類別背景筆刷* 會準備視窗的工作區，以供應用程式後續繪製。 系統會使用筆刷來填滿純色或模式的工作區，藉此從該位置移除所有先前的影像（不論它們是否屬於視窗）。 系統會將 [**WM \_ ERASEBKGND**](wm-erasebkgnd.md) 訊息傳送至視窗，以通知視窗應繪製其背景。 如需詳細資訊，請參閱 [筆刷](/windows/desktop/gdi/brushes)。

若要將背景筆刷指派給類別，請使用適當的 GDI 函數建立筆刷，然後將傳回的筆刷控制碼指派給 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hbrBackground** 成員。

應用程式可以將 **hbrBackground** 成員設定為其中一個標準系統色彩值，而不是建立筆刷。 如需標準系統色彩值的清單，請參閱 [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors)。

若要使用標準系統色彩，應用程式必須將背景色彩值增加一。 例如， **COLOR \_ background** + 1 是系統背景色彩。 或者，您可以使用 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush)函式來取得對應至標準系統色彩之筆刷的控制碼，然後在 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hbrBackground** 成員中指定控制碼。

系統不需要視窗類別具有類別背景筆刷。 如果此參數設定為 **Null**，則視窗必須在收到 [**WM \_ ERASEBKGND**](wm-erasebkgnd.md) 訊息時繪製自己的背景。

### <a name="class-menu"></a>類別功能表

如果在建立視窗時未指定明確功能表， *類別功能表* 會定義類別中的視窗所要使用的預設功能表。 功能表是一份命令清單，使用者可以從中選擇要執行應用程式的動作。

您可以藉由將 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **lpszMenuName** 成員設定為以 null 結束的字串位址（指定功能表的資源名稱），將功能表指派給類別。 此功能表會假設為指定之應用程式中的資源。 系統會在需要時自動載入功能表。 如果功能表資源是以整數來識別，而不是由名稱所識別，應用程式可以在指派值之前套用 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)宏，藉此將 **lpszMenuName** 成員設定為該整數。

系統不需要類別功能表。 如果應用程式將 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **lpszMenuName** 成員設定為 **Null**，則類別中的視窗沒有功能表列。 即使沒有指定 [類別] 功能表，應用程式還是可以在建立視窗時定義視窗的功能表列。

如果為類別指定了功能表，並建立該類別的子視窗，則會忽略該功能表。 如需詳細資訊，請參閱 [功能表](/windows/desktop/menurc/menus)。

### <a name="class-styles"></a>[類別樣式]

類別樣式定義視窗類別的其他元素。 您可以使用位 OR () 運算子來結合兩個或多個樣式 \| 。 若要將樣式指派給視窗類別，請將樣式指派給 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **樣式** 成員。 如需類別樣式的清單，請參閱 [**視窗類別樣式**](window-class-styles.md)。

### <a name="classes-and-device-contexts"></a>類別和裝置內容

*裝置內容* 是一組特殊的值，應用程式會在其視窗的工作區中用來繪圖。 系統需要顯示畫面上每個視窗的裝置內容，但可讓系統儲存和處理該裝置內容的方式有一些彈性。

如果未明確指定任何裝置內容樣式，系統會假設每個視窗使用從系統維護的內容集區中抓取的裝置內容。 在這種情況下，每個視窗都必須先取出並初始化裝置內容，再進行繪製，並在繪製之後釋放。

為了避免每次需要在視窗內繪製裝置內容時，應用程式可以指定視窗類別的 **CS \_ OWNDC** 樣式。 此類別樣式會指示系統建立私用裝置內容，也就是為類別中的每個視窗配置唯一的裝置內容。 應用程式只需要取出內容一次，然後將它用於所有後續的繪製。

### <a name="extra-class-memory"></a>額外類別記憶體

系統會在內部針對系統中的每個視窗類別維護 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構。 當應用程式註冊視窗類別時，它可以指示系統組態和附加一些額外的記憶體位元組至 **WNDCLASSEX** 結構的結尾。 這個記憶體稱為 *額外的類別記憶體* ，且由屬於該類別的所有 windows 共用。 使用額外的類別記憶體來儲存與類別有關的任何資訊。

由於系統的本機堆積會配置額外的記憶體，因此應用程式應謹慎使用額外的類別記憶體。 如果要求的額外類別記憶體數量大於40個位元組， [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) 函式會失敗。 如果應用程式需要超過40個位元組，它應該配置自己的記憶體，並將記憶體指標儲存在額外的類別記憶體中。

[**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)和 [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga)函數會將值複製到額外的類別記憶體。 若要從額外的類別記憶體取出值，請使用 [**GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) 和 [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) 函數。 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **cbClsExtra** 成員會指定要配置的額外類別記憶體量。 未使用額外類別記憶體的應用程式，必須將 **cbClsExtra** 成員初始化為零。

### <a name="extra-window-memory"></a>額外的視窗記憶體

系統會維護每個視窗的內部資料結構。 註冊視窗類別時，應用程式可以指定額外的記憶體位元組數目，稱為 *額外的視窗記憶體*。 建立類別的視窗時，系統會配置指定的額外視窗記憶體量，並將其附加至視窗結構的結尾。 應用程式可以使用此記憶體來儲存特定時間範圍的資料。

由於系統的本機堆積會配置額外的記憶體，因此應用程式應該謹慎使用額外的視窗記憶體。 如果要求的額外視窗記憶體數量大於40個位元組， [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) 函式會失敗。 如果應用程式需要超過40個位元組，它應該配置自己的記憶體，並將記憶體指標儲存在額外的視窗記憶體中。

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)函式會將值複製到額外的記憶體。 [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)函式會從額外的記憶體中抓取值。 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **cbWndExtra** 成員會指定要配置的額外視窗記憶體量。 未使用記憶體的應用程式必須將 **cbWndExtra** 初始化為零。

 

 
