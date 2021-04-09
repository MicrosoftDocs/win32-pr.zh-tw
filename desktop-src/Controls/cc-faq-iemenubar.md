---
title: 如何建立網際網路 Explorer-Style 功能表列
description: 乍看之下，Microsoft Internet Explorer 5 和更新版本中的功能表列看起來類似于標準功能表。 但是，當您開始使用它時，它看起來會非常不同。
ms.assetid: e0fe25f2-3d49-4c5a-a3f9-2f468f2cfef2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b262bc55407d263c97d4bd7e3938a9794d3a58f5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842772"
---
# <a name="how-to-create-an-internet-explorer-style-menu-bar"></a>如何建立網際網路 Explorer-Style 功能表列

乍看之下，Microsoft Internet Explorer 5 和更新版本中的功能表列看起來類似于標準功能表。 但是，當您開始使用它時，它看起來會非常不同。

下列螢幕擷取畫面顯示已選取 [工具] 功能表的 [Windows Internet Explorer] 功能表列。

![顯示 windows internet explorer 功能表列的螢幕擷取畫面，其中已選取 [工具] 功能表](images/howto8.jpg)

功能表列實際上是一個看起來像標準功能表的工具列控制項。 功能表列除了最上層功能表項目之外，還包含一系列的純文字按鈕，可在按一下時顯示下拉式功能表。 但是，以特殊類型的工具列來說，功能表列具有標準功能表缺乏的一些功能：

-   您可以使用標準的工具列技術來自訂它，讓使用者可以移動、刪除或新增專案。
-   它可能會有熱追蹤，讓使用者知道他們何時超過最上層專案，而不需要先按一下。

功能表列可以併入 Rebar 控制項中，提供下列功能：

-   它可以有移動流覽線，可讓使用者移動或調整寬線的大小。
-   它可以與其他群組（例如上圖中的標準工具列）共用 Rebar 控制項中的條紋。
-   它可以在連續的頻外涵蓋時顯示箭號，讓使用者存取隱藏的專案。
-   它可以有應用程式定義的背景點陣圖。

本主題討論如何執行功能表列。 因為功能表列是工具列控制項的特殊執行，所以焦點會放在功能表列特定的主題上。 如需如何將工具列併入 Rebar 控制項的討論，請參閱 [如何建立網際網路 Explorer-Style 工具列](cc-faq-ietoolbar.md) 和 [Rebar 控制項](rebar-controls.md)。

-   [在功能表列中建立工具列](#making-a-toolbar-into-a-menu-bar)
-   [已停用功能表 Hot-Tracking 處理導覽](#handling-navigation-with-menu-hot-tracking-disabled)
    -   [滑鼠導覽](#mouse-navigation)
    -   [鍵盤流覽](#keyboard-navigation)
    -   [混合導覽](#mixed-navigation)
-   [已啟用功能表 Hot-Tracking 的處理導覽](#handling-navigation-with-menu-hot-tracking-enabled)
    -   [功能表熱追蹤的訊息處理](#message-processing-for-menu-hot-tracking)
    -   [滑鼠導覽](#mouse-navigation)
    -   [鍵盤流覽](#keyboard-navigation)

## <a name="making-a-toolbar-into-a-menu-bar"></a>在功能表列中建立工具列

若要將工具列設為功能表列：

-   藉由將 TBSTYLE 包含在 [**其他 \_**](toolbar-control-and-button-styles.md) 視窗樣式旗標中，來建立一般工具列。 **TBSTYLE 的 \_ 平面** 樣式也可啟用熱追蹤。 使用此樣式時，功能表列看起來很像標準功能表，直到使用者啟動按鈕為止。 然後，按鈕會顯示在工具列上，然後按下按鍵，就像標準按鈕一樣。 因為已啟用熱追蹤，所以啟動按鈕所需的一切都是要將游標停留在其上方。 如果游標移至另一個按鈕，將會啟用它，並停用舊的按鈕。
-   藉由包含 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 與其他視窗樣式旗標，建立清單樣式的按鈕。 此樣式會建立更精簡的按鈕，看起來更像是標準最上層功能表項目。
-   將按鈕 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的 **iBitmap** 成員設定為 I \_ IMAGENONE，並將 **iString** 成員設為按鈕文字，以將按鈕設為純文字。
-   為每個按鈕提供 [**BTNS \_ 下拉式**](toolbar-control-and-button-styles.md) 樣式。 按一下按鈕時，工具列控制項會傳送 [TBN 的 \_ 下拉式](tbn-dropdown.md) 通知給您的應用程式，提示它顯示按鈕的功能表。
-   將功能表列併入 Rebar 區中。 啟用 grippers 和燕尾，如 [如何建立網際網路 Explorer-Style 的工具列](cc-faq-ietoolbar.md)中所述。
-   執行 [TBN 的 \_](tbn-dropdown.md) 下拉式處理常式，以在按 *下* 按鈕時顯示按鈕的下拉式功能表。 下拉式功能表是快顯功能表的一種類型。 它是使用 [**trackpopupmenu 讓**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) 函式來建立，其左上角與按鈕的左下角對齊。
-   執行鍵盤導覽，讓功能表列可在沒有滑鼠的情況下完整存取。
-   執行功能表熱追蹤。 使用標準功能表，在顯示最上層功能表項目的功能表之後，將游標移至另一個最上層專案，會自動顯示其功能表並折迭上一個專案的功能表。 工具列控制項將會熱追蹤游標並變更按鈕影像，但會自動顯示新的功能表。 您的應用程式必須明確地完成。

這些專案大多都可直接執行，並在其他地方討論。 如需如何使用工具列和 Rebar 控制項的一般討論，請參閱 [如何建立網際網路 Explorer-Style 工具列](cc-faq-ietoolbar.md)、 [工具列控制項](toolbar-controls-overview.md)或 [關於 Rebar 控制項](rebar-controls.md) 。 如需如何處理快顯功能表的討論，請參閱 [功能表](/windows/desktop/menurc/menus) 。 本主題的其餘部分將討論最後兩個專案：鍵盤導覽和功能表熱追蹤。

## <a name="handling-navigation-with-menu-hot-tracking-disabled"></a>已停用功能表 Hot-Tracking 處理導覽

使用者可以選擇使用滑鼠、鍵盤或兩者的混合來流覽功能表列。 若要執行功能表列流覽，您的應用程式必須處理工具列通知，並監視滑鼠和鍵盤。 這項工作可分成兩個不同的部分：不論是否有功能表熱追蹤。 本節討論如何在沒有顯示功能表且未啟用功能表熱追蹤的情況下處理導覽。

### <a name="mouse-navigation"></a>滑鼠導覽

如果停用功能表熱追蹤，您可以將功能表列視為一般工具列。 如果使用者是使用滑鼠流覽，則您的所有應用程式都需要處理 TBN 的 [ \_ 下拉式清單](tbn-dropdown.md) 通知。 收到此通知時，會顯示適當的下拉式功能表，並啟用功能表熱追蹤。 從那開始，您會在 [處理導覽] 功能表中所討論的 [熱追蹤] 制度中， [Hot-Tracking 已啟用](#handling-navigation-with-menu-hot-tracking-enabled)。

如 [混合導覽](#mixed-navigation)所述，您也需要處理 [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) 通知，以追蹤作用中的按鈕。 如果使用者只是使用滑鼠流覽，但在混合滑鼠和鍵盤流覽時需要此通知，則這項通知是不相關的。

### <a name="keyboard-navigation"></a>鍵盤導覽

如上一節所述，當功能表熱追蹤停用時，使用者可以使用鍵盤進行一些流覽作業。 只有當工具列控制項有焦點時，工具列控制項才支援鍵盤流覽。 它們也不會處理功能表列所需的所有按鍵按鍵。 處理鍵盤導覽最簡單的方法，就是明確地處理相關的按鍵事件。

如果停用功能表熱追蹤，您的應用程式必須以下列方式處理這些按鍵事件：

-   F10 鍵。 啟用具有 [**TB \_ SETHOTITEM**](tb-sethotitem.md)的第一個按鈕。
-   向左鍵和向右箭號。 啟用具有 [**TB \_ SETHOTITEM**](tb-sethotitem.md)的相鄰按鈕。 如果使用者嘗試流覽功能表列的任一端，請啟用另一端的第一個按鈕。
-   ESCAPE 鍵。 停用具有 [**TB \_ SETHOTITEM**](tb-sethotitem.md)的作用中按鈕。 功能表列應該會回到啟用第一個按鈕之前的狀態。
-   ALT *鍵* 加速器鍵。 使用 [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) 訊息來判斷索引 *鍵* 字元所對應的按鈕。 顯示按鈕的下拉式功能表，並啟用功能表熱追蹤。
-   向下鍵。 如果按鈕為作用中，但未顯示任何功能表，則會顯示按鈕的功能表，並啟用功能表熱追蹤。
-   ENTER 鍵。 停用具有 [**TB \_ SETHOTITEM**](tb-sethotitem.md)的作用中按鈕。 功能表列應該會回到啟用第一個按鈕之前的狀態。

### <a name="mixed-navigation"></a>混合導覽

上一節中所述的鍵盤導覽處理常式基本上會執行兩項工作：追蹤使用中的按鈕，並在選取按鈕時顯示適當的功能表。 只要使用者只流覽鍵盤，這些處理常式就已足夠。 不過，使用者通常會混合鍵盤和滑鼠導覽。 例如，他們可能會以 F10 鍵啟動第一個按鈕，使用滑鼠來啟用不同的按鈕，然後使用向下鍵開啟其功能表。 如果您只監視按鍵來追蹤使用中的金鑰，您將會顯示錯誤的功能表。 您也必須處理 [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) 通知，以精確地追蹤使用中的按鈕。

## <a name="handling-navigation-with-menu-hot-tracking-enabled"></a>已啟用功能表 Hot-Tracking 的處理導覽

啟用功能表熱追蹤時，您的應用程式必須變更回應使用者流覽的方式。 若要複製標準功能表的行為，您必須明確地執行下列功能。

使用滑鼠流覽：

-   如果使用者將游標移至另一個按鈕上，則會立即顯示該功能表，並顯示上一個功能表。
-   功能表熱追蹤會保持作用中，直到使用者選取命令或按一下不是功能表區域一部分的點為止。 這兩個動作都會停用功能表熱追蹤，直到按一下另一個按鈕為止。
-   如果游標移出功能表，則目前的下拉式功能表會一直保留到游標移回之前，或使用者按一下外點以外的位置，也就是功能表所涵蓋的區域。 如果資料指標返回的按鈕和目前顯示的不同，則舊功能表會折迭，並顯示新功能表。

使用鍵盤流覽：

-   向右箭號會將焦點向右移動。 如果專案有子功能表，請顯示子功能表。 如果專案沒有子功能表，請折迭功能表和任何子功能表，以 [ [**TB] \_ SETHOTITEM**](tb-sethotitem.md)啟動 [下一步] 按鈕，並顯示相鄰按鈕的功能表。 如果接收到此訊息時，最後一個按鈕是作用中，則會顯示第一個按鈕的功能表。
-   向左箭號會將焦點向左移動。 如果專案是子功能表，請折迭該專案並將焦點移至其父功能表。 如果專案不是子功能表，請折迭功能表，以 [ [**TB] \_ SETHOTITEM**](tb-sethotitem.md)啟用 [下一步] 按鈕，然後顯示該按鈕的功能表。

<!-- -->

-   ESCAPE 鍵可將顯示一個步驟。
    -   如果顯示子功能表，則會折迭並將焦點移至父功能表。
    -   如果顯示按鈕的功能表，則會折迭並停用功能表熱追蹤。 專案的按鈕會保持作用中狀態。
    -   如果未顯示任何功能表，但按鈕為使用中，則會停用按鈕，並停用功能表熱追蹤。
-   向上鍵和向下鍵只用于在特定功能表中流覽。
-   ENTER 鍵會啟動與功能表項目相關聯的命令。 如果功能表項目有子功能表，則 ENTER 鍵會顯示它。

如同功能表熱追蹤已停用的情況，您的應用程式必須能夠處理滑鼠、鍵盤和混合導覽。 不過，顯示功能表的事實表示訊息必須以不同的方式處理。

### <a name="message-processing-for-menu-hot-tracking"></a>功能表 Hot-Tracking 的訊息處理

功能表熱追蹤需要在任何時間顯示功能表，除了切換至新功能表所需的短暫間隔以外。 不過， [**trackpopupmenu 讓**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) 所顯示的下拉式功能表為強制回應。 您的應用程式將會繼續直接接收部分訊息，包括 [**wm \_ 命令**](/windows/desktop/menurc/wm-command)、 [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)，以及一般功能表相關訊息（例如 [**wm \_ MENUSELECT**](/windows/desktop/menurc/wm-menuselect)）。 但是，它不會直接收到低層級的鍵盤或滑鼠訊息。 若要處理諸如 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)之類的訊息，您必須設定訊息勾點，以攔截導向至功能表的訊息。

出現下拉式功能表時，請呼叫 [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) 函式，並將 *idHook* 參數設定為 WH MSGFILTER，以設定訊息掛勾 \_ 。 所有適用于功能表的訊息都會傳遞至您的 [勾](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85))點程式。 例如，下列程式碼片段會設定訊息攔截，以將會攔截到下拉式功能表的訊息。 `MsgHook` 這是攔截程式的名稱，而 `hhookMsg` 則是程式的控制碼。


```
hhookMsg = SetWindowsHookEx(WH_MSGFILTER, MsgHook, HINST_THISDLL, 0);
```



藉由將攔截程式的 *nCode* 參數設定為 [MSGF] 功能表，即可識別功能表訊息 \_ 。 *LParam* 參數會指向含有 [**訊息的訊息結構。**](/windows/win32/api/winuser/ns-winuser-msg) 本主題的其餘部分將討論哪些訊息需要處理的詳細資訊，以及如何處理這些訊息。

您的應用程式必須藉由呼叫 [**CallNextHookEx**](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，將所有訊息傳遞至下一個訊息勾點。 您也必須將滑鼠訊息直接傳送到工具列控制項，以確保將任何點座標轉換成工具列用戶端座標空間。 直接傳送訊息可確保工具列控制項收到適當的滑鼠訊息。 例如，工具列必須接收 [**WM 的 \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，才能對其按鈕進行熱追蹤。

啟用新按鈕時，您的應用程式必須以 [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) 訊息折迭舊的下拉式功能表，並顯示新的功能表。 當焦點取自具有鍵盤導覽的功能表列，或按一下功能表區域以外的地方時，也必須折迭下拉式功能表。 當您折迭功能表時，您應該使用 [**UnhookWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-unhookwindowshookex) 函式來釋出它的訊息勾點。 如果您需要顯示另一個下拉式功能表，請建立新的訊息勾點。 啟動命令時，功能表將會自動折迭，但您必須明確釋放訊息掛勾。

下列程式碼範例會釋出先前範例中所設定的訊息掛勾。


```
UnhookWindowsHookEx(hhookMsg);
```



### <a name="mouse-navigation"></a>滑鼠導覽

當一般工具列控制項熱追蹤按鈕時，它會反白顯示 [使用中] 按鈕，並在每次啟用新按鈕時，傳送 [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) 通知給應用程式。 您的應用程式會負責顯示適當的下拉式功能表。 它必須：

-   處理 [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) 通知，以追蹤作用中的按鈕。 當使用中的按鈕變更時，請折迭舊的功能表並建立新的功能表。
-   處理按一下按鈕時所傳送的 [TBN \_ 下拉式清單](tbn-dropdown.md) 通知。 接著，它會折迭功能表並停用功能表熱追蹤。 按鈕會保持作用中狀態。
-   處理訊息攔截程式中的 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)、 [**wm \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)和 [**wm \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，以追蹤滑鼠位置。 如果按一下功能表區域以外的滑鼠，請折迭目前的下拉式功能表、停用功能表熱追蹤，然後將功能表列返回其 preactivation 狀態。
-   啟動功能表命令時，請停用功能表熱追蹤。 此功能表會自動折迭，但您必須明確釋放訊息掛勾。

您也必須處理與功能表相關的訊息，例如，當功能表項目需要顯示子功能表時，所傳送的 [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) 訊息。 如需如何處理這類訊息的討論，請參閱 [功能表](/windows/desktop/menurc/menus)。

### <a name="keyboard-navigation"></a>鍵盤導覽

您的應用程式必須處理訊息攔截程式中的鍵盤訊息，並對影響功能表熱追蹤的程式採取行動。 必須處理下列按鍵：

-   ESCAPE 鍵。 ESCAPE 鍵可將顯示層級備份為一層。 如果正在顯示子功能表，則必須折迭。 如果顯示按鈕的主要功能表，請將它折迭並停用功能表熱追蹤。 按鈕會保持作用中狀態。
-   向右鍵。 如果專案有子功能表，則會顯示它。 如果專案沒有子功能表，請折迭功能表和任何子功能表，以 [ [**TB] \_ SETHOTITEM**](tb-sethotitem.md)啟用 [下一步] 按鈕，並顯示其功能表。 如果收到此通知時，最後一個按鈕是作用中，則會顯示第一個按鈕的功能表。
-   向左鍵。 如果專案在子功能表中，請折迭並將焦點移至其父功能表。 如果專案不是子功能表，請折迭功能表，啟動具有 [TB] [**\_ SETHOTITEM**](tb-sethotitem.md)的相鄰按鈕，並顯示其功能表。 如果收到此通知時，第一個按鈕是作用中，則會顯示 [上一步] 按鈕的功能表。
-   向上鍵和向下鍵。 這些金鑰是用來在功能表內流覽，但不會直接影響功能表熱追蹤。
-   ALT *鍵* 加速器鍵。 使用 [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) 訊息來判斷索引 *鍵* 字元所對應的按鈕。 如果它對應的按鈕與目前使用中的按鈕不同，請折迭目前的下拉式功能表，以 [ [**TB] \_ SETHOTITEM**](tb-sethotitem.md)啟動新按鈕，並顯示相鄰按鈕的功能表。 如果索引 *鍵字元* 對應到目前顯示的按鈕，請折迭下拉式功能表，並停用功能表熱追蹤。 按鈕應該保持作用中狀態。

 

 