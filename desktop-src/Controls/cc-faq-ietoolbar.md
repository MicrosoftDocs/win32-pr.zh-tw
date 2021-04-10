---
title: 如何建立網際網路 Explorer-Style 工具列
description: Windows Internet Explorer 的主要使用者介面功能之一，就是工具列。 它不僅可讓使用者存取廣泛的功能，還可讓使用者根據個人喜好來自訂版面配置。
ms.assetid: d24969ec-4dea-44c6-b045-5611de8f1cce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32228f941a7c7e1253884ab5d72368f66f25c7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093387"
---
# <a name="how-to-create-an-internet-explorer-style-toolbar"></a>如何建立網際網路 Explorer-Style 工具列

Windows Internet Explorer 的主要使用者介面功能之一，就是工具列。 它不僅可讓使用者存取廣泛的功能，還可讓使用者根據個人喜好來自訂版面配置。

下列螢幕擷取畫面顯示 Internet Explorer 的工具列，並強調一些重要功能。

![windows internet explorer 工具列的螢幕擷取畫面，其中包含8項功能的標籤](images/howto1a.jpg)

此工具列基本上是由具有四個群組的 Rebar 控制項所組成：三個工具列和一個功能表列。 由於它是以通用控制項 API 來執行，因此開發人員可以建立具有任何或所有功能的工具列。 本主題討論 Internet Explorer 工具列的基本功能，以及如何在您的應用程式中加以執行。

-   [Rebar 控制項](#the-rebar-control)
    -   [執行 Rebar 控制項](#implementing-the-rebar-control)
-   [工具列](#how-to-create-an-internet-explorer-style-toolbar)
    -   [下拉按鈕](#drop-down-buttons)
    -   [清單樣式按鈕](#list-style-buttons)
    -   [角括弧](#handling-chevrons)
    -   [熱追蹤](#hot-tracking)
-   [相關主題](#related-topics)

## <a name="the-rebar-control"></a>Rebar 控制項

Internet Explorer 工具列的基礎結構是由 [Rebar 控制項](rebar-controls.md)提供。 此控制項可讓使用者自訂工具集合的相片順序。 每個 Rebar 都包含一 *或多個* 群組，通常是長、包含子視窗的窄矩形，通常是工具列控制項。

Rebar 控制項會在矩形區域中顯示其區段，通常是在視窗的頂端。 這個矩形會細分為一個或多個寬線的寬線。 每個波段都可以位於不同的區域上，或多個群組可放置在相同的區域上。

Rebar 控制項為使用者提供兩種方式來排列其工具：

-   每個波段的左邊緣通常都有一個 *控制* 者。 當單一區域的兩個或多個波段超過視窗寬度時，會使用 Grippers。 藉由將移出手柄向左或向右拖曳，使用者可以控制要配置給每個波段的空間量。
-   使用者可以藉由拖放來移動 Rebar 顯示矩形內的條紋。 Rebar 控制項接著會變更顯示，以容納新的條紋相片順序。 如果從區域中移除所有的條紋，則 Rebar 的高度將會縮小，放大視圖區域。

應用程式可以視需要新增或移除區段。 一般情況下，應用程式可讓使用者透過 [View] 功能表或快捷方式功能表來選取要顯示的波段。

如果帶狀線的組合寬度超過視窗的寬度，則 Rebar 控制項將視需要調整其寬度。 部分工具可能會涵蓋在連續的頻外。

[版本 5.80](common-control-versions.md) 的通用控制項提供了一種方式，讓使用者可以存取另一個範圍所涵蓋的工具。 如果您 \_ 在頻外 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的 **FSTYLE** 成員中設定 RBBS USECHEVRON 旗標，則會顯示已涵蓋的工具列的 *燕* 號。 當使用者按一下箭號時，就會顯示功能表，讓他或她可以使用隱藏的工具。 下列來自 Microsoft Internet Explorer 6 的螢幕擷取畫面，會顯示在涵蓋標準工具列的一部分時所顯示的功能表。

![顯示功能表的螢幕擷取畫面，其中按一下箭號按鈕](images/howto2.jpg)

由於每個波段都包含一個控制項，因此您可以透過控制項的 API 提供額外的彈性。 例如，您可以執行工具列自訂，讓使用者加入、移動或移除工具欄上的按鈕。

### <a name="implementing-the-rebar-control"></a>執行 Rebar 控制項

Internet Explorer 工具列的大部分功能實際上都是在個別的區段中實作為。 Rebar 控制項本身的執行相當簡單，如下所示。

1.  使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)建立 Rebar 控制項。 將 *dwExStyle* 設定 [**為 WS \_ EX \_ 工具視窗**](/windows/desktop/winmsg/extended-window-styles) ，並將 *lpClassName* 設定為 [**REBARCLASSNAME**](common-control-window-classes.md)。 Internet Explorer 會使用下列視窗樣式：

    -   [**RBS \_ BANDBORDERS**](rebar-control-styles.md)
    -   [**RBS \_ DBLCLKTOGGLE**](rebar-control-styles.md)
    -   [**RBS \_ REGISTERDROP**](rebar-control-styles.md)
    -   [**RBS \_ VARHEIGHT**](rebar-control-styles.md)
    -   [**CCS \_ NODIVIDER**](common-control-styles.md)
    -   [**CCS \_ NOPARENTALIGN**](common-control-styles.md)
    -   [**WS \_ 框線**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ 子系**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPCHILDREN**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ 可見**](/windows/desktop/winmsg/window-styles)

    設定適用于您應用程式的其他參數。

2.  使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或特製化控制項建立功能（例如 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)）來建立控制項。
3.  填入 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)的成員，以初始化控制項的頻外。 包含 RBBS \_ USECHEVRON 樣式與 **fStyle** 成員，以啟用燕形。
4.  使用 [**RB \_ INSERTBAND**](rb-insertband.md) 訊息，將頻外新增至 Rebar 控制項。
5.  針對其餘的區段重複步驟2-4。
6.  執行 Rebar 通知的處理常式。 尤其是，您必須在按下箭號時，處理 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) ，以顯示下拉式功能表。 如需詳細資訊，請參閱 [處理燕形](#handling-chevrons)。

預設會包含 grippers。 若要省略頻外的控制器，請 \_ 在波段 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的 **FSTYLE** 成員中設定 RBBS NOGRIPPER 旗標。 如需有關實施 Rebar 控制項的詳細資訊，請參閱 [關於 Rebar 控制項](rebar-controls.md)。

### <a name="handling-chevrons"></a>處理燕尾

當使用者按一下箭號時，Rebar 控制項會傳送 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) 通知給您的應用程式。 與通知一起傳遞的 [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)結構包含帶線的識別碼，以及帶有箭號所佔用之 [**矩形的矩形結構。**](/previous-versions//dd162897(v=vs.85)) 您的處理常式必須判斷哪些按鈕是隱藏的，並在快顯功能表上顯示相關聯的命令。

下列程式概述如何處理 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) 通知：

1.  將 Rebar 控制項傳送至 [**RB \_ GETRECT**](rb-getrect.md) 訊息，以抓取所選範圍的目前周框。
2.  藉由將寬線的工具列控制項傳送至 [**TB 的 \_ BUTTONCOUNT**](tb-buttoncount.md) 訊息，以抓取按鈕的總數目。
3.  從最左邊的按鈕開始，藉由將工具列控制項傳送至 [**TB 的 \_ GETITEMRECT**](tb-getitemrect.md) 訊息，來取出按鈕的周框。
4.  將頻外和按鈕矩形傳遞給 [**IntersectRect**](/windows/desktop/api/winuser/nf-winuser-intersectrect) 函數。 此函式會傳回對應至按鈕可見部分的 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構。
5.  將按鈕的可見部分的按鈕矩形和矩形傳遞給 [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) 函數。
6.  如果 [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) 傳回 **TRUE**，則會顯示整個按鈕。 針對工具列上的 [下一步] 按鈕重複步驟3-5。 如果 **EqualRect** 傳回 **FALSE**，則按鈕至少為部分隱藏，而且所有剩餘的按鈕都將完全隱藏。 繼續進行下一個步驟。
7.  建立快顯功能表，其中包含每個隱藏按鈕的專案。
8.  使用 [**trackpopupmenu 讓**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) 函數來顯示快顯功能表。 使用以 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) 通知傳遞的燕形矩形來定位功能表。 功能表應該緊接在箭號正下方，且左邊緣對齊。
9.  處理功能表命令。

## <a name="the-toolbars"></a>工具列

Internet Explorer 工具列的大部分複雜性都是在組成 Rebar 群組的控制項中執行。 Internet Explorer 通常會顯示四個區段：

-   功能表列
-   標準工具列
-   連結工具列
-   位址工具列

所有這些等量（包括功能表列）實際上都會保存工具列控制項。 本節討論標準和連結工具列的執行。 功能表列稍微複雜一點，在 [如何建立網際網路 Explorer-Style 功能表列](cc-faq-iemenubar.md)中也會分別討論。

[關於] 工具列 [控制項](toolbar-controls-overview.md)中會討論執行工具列控制項的基本程式。 本節著重于 Internet Explorer 用來提高控制項可用性的一些較新工具列功能。

-   [下拉按鈕](#drop-down-buttons)
-   [清單樣式按鈕](#list-style-buttons)
-   [角括弧](#handling-chevrons)
-   [熱追蹤](#hot-tracking)

### <a name="drop-down-buttons"></a>下拉按鈕

下拉式按鈕支援多個命令。 當使用者按一下下拉式按鈕時，按鈕會顯示快顯功能表，而不是啟動命令。 使用者從功能表中選取命令來啟動命令。 下列螢幕擷取畫面顯示 Internet Explorer 標準工具列中的下拉式按鈕和功能表。

![顯示郵件下拉式功能表的螢幕擷取畫面](images/howto3.jpg)

您可以藉由將樣式旗標新增至按鈕 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的 **fStyle** 成員，將下拉式功能新增至任何按鈕樣式。 下拉式按鈕有三種樣式，Internet Explorer 使用這些樣式：

-   純下拉式按鈕具有 [ [**BTNS] 下拉式 \_ 清單**](toolbar-control-and-button-styles.md) 樣式。 它們看起來像是一般按鈕，但是按一下時會顯示功能表，而不是啟動命令。
-   簡單的下拉箭號按鈕具有 [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) 樣式。 它們旁邊會顯示按鈕影像或文字旁邊的箭號。 除了外觀的差異以外，它們與一般下拉按鈕相同。 在上圖中當做範例使用的 [郵件] 按鈕是下拉箭號按鈕。
-   將 [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md) 擴充樣式新增至 [**BTNS \_ 下拉式清單**](toolbar-control-and-button-styles.md) 的下拉箭號按鈕，具有與文字或影像分開的箭號。 此按鈕樣式結合下拉式清單和標準按鈕的功能。 如果使用者按一下箭號，就會顯示功能表，而使用者可以從數個命令中選擇。 如果使用者按一下連續的按鈕，就會啟動預設命令。 下列螢幕擷取畫面顯示 Internet Explorer 的 [ **上一頁** ] 按鈕，其使用分隔箭號。

    ![顯示 [上一頁] 分割按鈕功能表的螢幕擷取畫面](images/howto4.jpg)

當使用者按一下具有一般或簡單箭號樣式的下拉式按鈕時，工具列控制項會傳送 TBN 的下拉式通知給您的 [應用 \_ ](tbn-dropdown.md) 程式。 當您的應用程式收到此訊息時，它會負責建立及顯示功能表，以及處理選取的命令。

當使用者按一下分隔箭號時，工具列控制項會傳送 [TBN 的 \_ 下拉式](tbn-dropdown.md) 通知給您的應用程式。 您的應用程式應該處理它的方式，與處理其他兩種類型的下拉按鈕相同。 如果使用者按一下 [main] 按鈕，您的應用程式會收到 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，其中包含按鈕的命令識別碼，就像是標準按鈕一樣。 應用程式通常會在下拉式功能表中啟動 top 命令來回應，但您可以隨意地以任何適當的方式回應。

### <a name="list-style-buttons"></a>List-Style 按鈕

使用標準按鈕時，如果您新增文字，則會顯示在點陣圖下方。 下列螢幕擷取畫面顯示 [Internet Explorer **搜尋**] 和 [我的最愛 **]** 按鈕與標準按鈕文字。

![顯示 [搜尋] 和 [我的最愛] 工具列與標準按鈕的螢幕擷取畫面](images/howto6.jpg)

Microsoft Internet Explorer 5 和更新版本會使用 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式。 文字位於點陣圖的右邊，減少按鈕的高度並放大觀看區域。 下圖顯示 [Internet Explorer 6 **搜尋** **]** 和 [我的最愛] 按鈕與 **TBSTYLE \_ 清單** 樣式。

![顯示 [搜尋] 和 [我的最愛] 工具列使用清單樣式按鈕的螢幕擷取畫面](images/howto5.jpg)

### <a name="chevrons"></a>角括弧

當使用者重新排列 Rebar 控制項中的條紋時，可能會涵蓋工具列的一部分。 如果使用 RBBS \_ USECHEVRON 樣式來建立頻外，Rebar 控制項將會在工具列的右邊緣顯示箭號。 使用者按一下箭號可顯示具有隱藏工具的功能表。

### <a name="hot-tracking"></a>Hot-Tracking

啟用熱追蹤時，當游標停留在按鈕上時，按鈕會變成 *熱* 。 [經常性存取] 按鈕通常會與工具列上的其他按鈕（依特殊影像區別）。 根據預設，作用中按鈕會出現在工具列的其餘部分上方。 當新按鈕變得熱時，您的應用程式會收到 [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) 通知。 下圖顯示 [Internet Explorer 5 **搜尋**] 和 [我的最愛] 按鈕，以及 [熱 **搜尋** **]** 按鈕。 除了具有引發的外觀之外，按鈕的灰色點陣圖也已被彩色的點陣圖取代。

![顯示 [搜尋] 和 [我的最愛] 按鈕的螢幕擷取畫面，其中包含熱搜尋按鈕](images/howto7.jpg)

若要啟用熱追蹤，請使用 [**TBSTYLE 的 \_ 平面**](toolbar-control-and-button-styles.md) 或 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式建立工具列控制項。 這些 *稱為一般工具列，* 因為個別按鈕通常不會以任何方式反白顯示。 點陣圖只會顯示在旁邊。 他們只會在熱時採用類似按鈕的外觀。 這兩種樣式也是透明的，這表示圖示的背景會是基礎用戶端視窗的色彩。

若要在按鈕作用時顯示不同的點陣圖，請建立第二個 [影像清單](image-lists.md) ，其中包含工具列上所有按鈕的熱影像。 這些影像的大小和順序應該與預設影像清單中的相同。 將 [**\_ SETHOTIMAGELIST**](tb-sethotimagelist.md) 訊息傳送至工具列控制項，以設定熱影像清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何建立網際網路 Explorer-Style 功能表列](cc-faq-iemenubar.md)
</dt> </dl>

 

 