---
title: 關於工具列控制項
description: 工具列是包含一或多個按鈕的控制項。
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d95b13ddee54561cf1b0bb9d003d5d34cdf8d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933637"
---
# <a name="about-toolbar-controls"></a>關於工具列控制項

工具列是包含一或多個按鈕的控制項。 當使用者按下每個按鈕時，會將命令訊息傳送至父視窗。 通常，工具列中的按鈕對應於應用程式功能表中的項目，為使用者提供其他更直接的方式來存取應用程式的命令。

下列螢幕擷取畫面顯示一個視窗，其中包含檔案作業的簡單工具列。 應用程式已啟用視覺化樣式。 [儲存] 按鈕為「熱」，因為在拍攝螢幕擷取畫面時，游標停留在其上方。 控制項的實際外觀會依據作業系統和使用者選取的主題而有所不同。

![具有三個按鈕工具列之視窗的螢幕擷取畫面;一個按鈕是熱的](images/tb-withstyles.png)

下列螢幕擷取畫面顯示在未啟用視覺化樣式的情況下編譯之應用程式中的相同控制項。

![沒有視覺化樣式之視窗的螢幕擷取畫面：沒有任何按鈕看起來很熱](images/tb-wostyles.png)

下列主題討論在規劃工具列時要考慮的功能。 如需有關執行的特定資訊和範例程式碼，請參閱 [使用工具列控制項](using-toolbar-controls.md)。

-   [指定工具列大小和位置](#specifying-toolbar-size-and-position)
-   [透明工具列](#transparent-toolbars)
-   [清單樣式的工具列](#list-style-toolbars)
-   [定義按鈕影像](#defining-button-images)
    -   [使用點陣圖定義按鈕影像](#defining-button-images-by-using-bitmaps)
    -   [使用影像清單定義按鈕影像](#defining-button-images-by-using-image-lists)
-   [定義按鈕的文字](#defining-text-for-buttons)
-   [新增工具列按鈕](#adding-toolbar-buttons)
    -   [工具列按鈕樣式](#toolbar-button-styles)
    -   [工具列按鈕狀態](#toolbar-button-states)
    -   [命令識別碼](#command-identifier)
    -   [按鈕大小和位置](#button-size-and-position)
-   [啟用自訂](#enabling-customization)
-   [啟用熱追蹤](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>指定工具列大小和位置

如果您使用 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)建立工具列，此函式可讓您以圖元為單位來指定工具列的高度和寬度。

> [!Note]  
> 不建議使用 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) ，因為它不支援工具列的新功能，包括影像清單。 如需建立工具列的詳細資訊，請參閱 [使用工具列控制項](using-toolbar-controls.md)。

 

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函式沒有可指定工具列大小的參數。 工具列視窗程式會自動設定工具列視窗的大小和位置。 高度是以工具列中按鈕的高度為基礎。 寬度與父視窗工作區的寬度相同。 若要變更自動調整規模設定，請傳送 [**TB 的 \_ SETBUTTONSIZE**](tb-setbuttonsize.md) 訊息。 [ [**CCS \_ TOP**](common-control-styles.md) ] 和 [ [**CCS] \_ 下方**](common-control-styles.md) 的 [常用] 控制項樣式可決定工具列是否位於工作區的頂端或底部。 依預設，工具列具有 CCS 的 **\_ 最上層** 樣式。

此外，工具列視窗程式會在每次收到 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 或 TB 的自動 [**\_ 調整**](tb-autosize.md) 訊息時，自動調整工具列的大小。 每當父視窗的大小變更時，或傳送需要調整工具列大小的訊息（例如， [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) 訊息）之後，應用程式就應該傳送這些訊息中的任一個。

您可以藉由設定 [**CCS \_ NORESIZE**](common-control-styles.md) 和 [**CCS \_ NOPARENTALIGN**](common-control-styles.md) 通用控制項樣式來關閉工具列預設大小調整和定位行為。 Rebar 控制項所裝載的工具列控制項必須設定這些樣式，因為 Rebar 控制項的大小和定位工具列。

## <a name="transparent-toolbars"></a>透明工具列

Toolbar 控制項支援可讓工具列下的工作區顯示的透明外觀。 有兩種透明的工具列，其中有一個具有平面按鈕的透明工具列，以及一個具有三維按鈕的工具列。 如果您想要讓應用程式符合 Windows 介面，請使用「一般透明樣式」工具列。

下列螢幕擷取畫面顯示兩種透明工具列，而不是使用視覺化樣式。

![兩個視窗的螢幕擷取畫面，其中包含不同樣式的工具列，但兩個工具列都是透明的](images/toolbartrans.jpg)

下列螢幕擷取畫面顯示透明工具列，因為它可能會出現在 Windows Vista 中，並啟用視覺化樣式。 對話方塊的背景色彩已變更，使透明度更明顯。

![windows vista 中具有透明工具列之視窗的螢幕擷取畫面](images/tb-transparent.png)

若要建立透明的工具列，您只需要在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的視窗樣式參數中加入 TBSTYLE 的 [一般] 或 [ [**TBSTYLE \_**](toolbar-control-and-button-styles.md) ]。 [**\_**](toolbar-control-and-button-styles.md) 如果您不想讓一行出現來指出工具列底部，請勿使用 [ [**WS \_ 框線**](/windows/desktop/winmsg/window-styles) 視窗樣式]。

> [!Note]  
> 使用視覺化樣式時，工具列預設可能是平面的。

 

## <a name="list-style-toolbars"></a>清單樣式的工具列

工具列按鈕可讓您同時顯示文字和點陣圖。 使用 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式建立的工具列上的按鈕，會將文字放到點陣圖右邊，而不是在其下。

下列螢幕擷取畫面顯示具有清單樣式的工具列。

![具有每個圖示右邊文字的工具列螢幕擷取畫面](images/tb-liststyle.png)

您可以搭配使用 [ [**TBSTYLE] \_ 清單**](toolbar-control-and-button-styles.md) 工具列樣式與 [ [**TBSTYLE] \_ 平面**](toolbar-control-and-button-styles.md) 樣式，建立具有平面按鈕的工具列。

## <a name="defining-button-images"></a>定義按鈕影像

有兩種方式可以指定按鈕的影像：依點陣圖或影像清單。 應用程式必須選擇要使用的方法。 它無法同時使用這兩種方法與相同的工具列控制項。 請注意， [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) 函數會使用 bitmap 方法。 想要使用影像清單方法的應用程式必須使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立工具列控制項。

### <a name="defining-button-images-by-using-bitmaps"></a>使用點陣圖定義按鈕影像

工具列中的每個按鈕都可以包含點陣圖影像。 工具列會使用內部清單來儲存繪製影像所需的資訊。 當您呼叫 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) 函式時，您會指定包含初始影像的單色或色彩點陣圖，而工具列會將資訊新增至影像的內部清單。 您稍後可以使用 [**TB \_ ADDBITMAP**](tb-addbitmap.md) 訊息來新增其他映射。

每個映射都有以零為基底的索引。 新增至內部清單的第一個影像的索引為0，第二個影像的索引為1，依此類推。 [**TB \_ADDBITMAP**](tb-addbitmap.md) 會將影像新增至清單的結尾，並傳回它所新增之第一個新映射的索引。 若要將影像與按鈕建立關聯，您必須在將點陣圖新增至內部影像清單之後傳送 [**TB \_ ADDBUTTONS**](tb-addbuttons.md) 訊息，並指定映射的索引。

Windows 假設所有工具列的點陣圖影像大小都相同。 您可以使用 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)來指定建立工具列時的大小。 如果您使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立工具列，影像的大小會設定為預設維度 16 x 15 圖元。 您可以使用 [**TB 的 \_ SETBITMAPSIZE**](tb-setbitmapsize.md) 訊息來變更點陣圖影像的維度，但您必須先執行此動作，才能將任何影像新增至內部清單。

### <a name="defining-button-images-by-using-image-lists"></a>使用影像清單定義按鈕影像

您也可以將按鈕影像儲存在一組 [影像清單](image-lists.md)中。 影像清單是相同大小的影像集合，每個影像都可由其索引參考。 影像清單可用來管理大型的圖示或點陣圖集。 您最多可以使用三個不同的影像清單來顯示各種狀態下的按鈕，如下表所示。



|          |                                                                                                                                                                                              |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 正常   | 處於預設狀態的按鈕。                                                                                                                                                              |
| 經常性存取層      | 指標或按下的按鈕。 只有具有 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式的工具列控制項才支援熱專案。 |
| Disabled | 已停用的按鈕。                                                                                                                                                                   |



 

終結工具列之後，應用程式必須釋放任何已建立的影像清單。

## <a name="defining-text-for-buttons"></a>定義按鈕的文字

除了影像之外，每個按鈕都可以顯示字串，而不是。 工具列會維護內部清單，其中包含工具列按鈕的所有可用字串。 您可以使用 [**TB \_ ADDSTRING**](tb-addstring.md) 訊息將字串加入至內部清單，指定包含要加入之字串的緩衝區位址。 每個字串都必須以 null 終止，而最後一個字串必須以兩個 null 字元結束。

每個字串都有以零為基底的索引。 新增至字串內部清單的第一個字串的索引為0，第二個字串的索引為1，依此類推。 [**TB \_ADDSTRING**](tb-addstring.md) 會將字串加入至清單的結尾，並傳回第一個新字串的索引。 您可以使用字串的索引，將字串與按鈕產生關聯。

使用 [**TB \_ ADDSTRING**](tb-addstring.md) 並非將字串新增至工具列的唯一方法。 您可以在傳遞至 [**TB \_ ADDBUTTONS**](tb-addbuttons.md)之 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的 **iString** 成員中傳遞字串指標，藉以在按鈕中顯示字串。 此外，您可以使用 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) 將文字指派給工具列按鈕。

## <a name="adding-toolbar-buttons"></a>新增工具列按鈕

如果您使用 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) 函式來建立工具列，則可以將按鈕加入至工具列，方法是填入 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構的陣列，並在函式呼叫中指定陣列的位址。 不過， [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式沒有可傳遞 **TBBUTTON** 結構的參數。 **CreateWindowEx** 會建立一個空白工具列，您可以藉由傳送 [**TB \_ ADDBUTTONS**](tb-addbuttons.md) 訊息來填滿，並指定 **TBBUTTON** 結構的位址。

建立工具列之後，您可以藉由傳送 [**tb \_ INSERTBUTTON**](tb-insertbutton.md) 或 [**tb \_ ADDBUTTONS**](tb-addbuttons.md) 訊息來新增按鈕。 每個按鈕都會以 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構描述，此結構會定義按鈕的屬性，包括其字串和點陣圖的索引，以及其樣式、狀態、命令識別碼和應用程式定義的32位值。

> [!Note]  
> 如果您使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立工具列，則必須在新增任何按鈕之前傳送 [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) 訊息。 訊息會將 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構的大小傳遞給工具列。

 

### <a name="toolbar-button-styles"></a>工具列按鈕樣式

按鈕的樣式可決定按鈕的顯示方式，以及它如何回應使用者輸入。 例如，[ [**BTNS] \_ 按鈕**](toolbar-control-and-button-styles.md) 樣式建立的工具列按鈕，其行為類似標準的 [推送] 按鈕。 具有 [**BTNS \_ 檢查**](toolbar-control-and-button-styles.md) 樣式的按鈕類似于標準推播按鈕，不同之處在于它會在每次使用者按一下時，于按下和 nonpressed 狀態之間切換。

您可以使用 [**BTNS \_ GROUP**](toolbar-control-and-button-styles.md) 或 [**BTNS \_ CHECKGROUP**](toolbar-control-and-button-styles.md) 樣式，建立與選項按鈕類似的工具列按鈕群組。 這會讓按鈕保持按下狀態，直到使用者選擇群組中的另一個按鈕為止。 群組會定義為連續的按鈕集合，全部都有 **BTNS \_ Group** 或 **BTNS \_ CHECKGROUP** 樣式。

[**BTNS \_ SEP**](toolbar-control-and-button-styles.md)樣式會建立按鈕之間的小間距，或在一般工具列上的按鈕之間繪製 etch 若。 具有 **BTNS \_ SEP** 樣式的按鈕不會接收使用者輸入。

版本5.80 的通用控制項引進了一些新的工具列按鈕樣式，並重新命名一些較舊的樣式。 所有按鈕樣式旗標現在都以 BTNS xxx 開頭， \_ 而不是 TBSTYLE \_ xxx。 如需按鈕樣式的清單和討論，請參閱 [工具列控制項和按鈕樣式](toolbar-control-and-button-styles.md)。

### <a name="toolbar-button-states"></a>工具列按鈕狀態

工具列中的每個按鈕都有一個狀態。 工具列會更新按鈕的狀態，以反映使用者動作，例如按一下按鈕。 狀態會指出按鈕目前為按下或未按下、啟用或停用、隱藏或顯示。 雖然應用程式會在將按鈕新增至工具列時設定按鈕的初始狀態，但它可以藉由將 [**tb \_ >getstate**](tb-getstate.md) 和 [**tb \_ SETSTATE**](tb-setstate.md) 訊息傳送至工具列，來變更和取得狀態。 如需工具列按鈕狀態的清單，請參閱 [工具列狀態](toolbar-button-states.md)。

### <a name="command-identifier"></a>命令識別碼

每個按鈕都有與其相關聯的應用程式定義命令識別碼。 按鈕識別碼通常是在應用程式標頭檔中定義。 例如，[貼上] 按鈕可以定義為：


```
#define ID_PASTE 100
```



當使用者選取按鈕時，工具列會將包含按鈕命令識別碼的 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 或 [**wm \_ 通知**](wm-notify.md) 訊息傳送至父視窗。 父視窗會檢查命令識別碼，並執行與按鈕相關聯的命令。 如需控制項何時傳送 **wm \_ 命令** 訊息，以及何時傳送 **wm \_ 通知** 的詳細資訊，請參閱 [**WM \_ 通知**](wm-notify.md) 檔的「備註」一節。

### <a name="button-size-and-position"></a>按鈕大小和位置

工具列會藉由指派每個按鈕的位置索引來追蹤其按鈕。 索引是以零為基底;也就是說，最左邊的按鈕索引為0，右邊的下一個按鈕索引為1，依此類推。 應用程式在傳送訊息以抓取按鈕的相關資訊或設定按鈕的屬性時，必須指定按鈕的索引。

當插入和移除按鈕時，工具列會更新位置索引。 應用程式可以使用 [**TB \_ COMMANDTOINDEX**](tb-commandtoindex.md) 訊息來取出按鈕的目前位置索引。 訊息會指定按鈕的命令識別碼，而工具列視窗會使用識別碼來找出按鈕，並傳回其位置索引。

工具列中的所有按鈕都有相同的大小。 當您建立工具列時， [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) 函式會要求您設定按鈕的初始大小。 當您使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式時，初始大小會設定為預設維度24乘以22圖元。 您可以使用 [ [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) ] 訊息來變更按鈕大小，但您必須先執行此動作，才能將任何按鈕新增至工具列。 [**TB 的 \_ GETITEMRECT**](tb-getitemrect.md)訊息會抓取按鈕目前的維度。

當您加入的字串長度超過工具列目前的任何字串時，工具列會自動重設其按鈕的寬度。 寬度設定為容納工具列中最長的字串。

## <a name="enabling-customization"></a>啟用自訂

工具列具有內建的自訂功能，可讓使用者透過提供 [**CCS 可 \_ 調整**](common-control-styles.md) 的通用控制項樣式來提供給使用者使用。 自訂功能可讓使用者將按鈕拖曳至新的位置，或者拖曳出工具列以移除按鈕。 此外，使用者可以按兩下工具列顯示 [自訂工具列] 對話方塊，讓使用者加入、刪除及重新排列工具列按鈕。 若要顯示對話方塊，請使用 [**TB \_ 自訂**](tb-customize.md) 訊息。 應用程式會決定使用者是否可用自訂功能，以及控制使用者可自訂工具列的範圍。

在自訂程式中，應用程式通常需要儲存和還原工具列的狀態。 例如，許多應用程式會在使用者開始自訂工具列之前儲存工具列狀態，以防使用者稍後想要將工具列還原為其原始狀態。 工具列控制項不會自動保留其 precustomization 狀態的記錄。 您的應用程式必須儲存工具列狀態，才能進行還原。 如需詳細資訊，請參閱 [使用工具列控制項](using-toolbar-controls.md)。

## <a name="enabling-hot-tracking"></a>啟用熱追蹤

熱追蹤表示當指標移到專案上時，按鈕的外觀會變更。 啟用視覺化樣式時，工具列預設會支援熱追蹤。 否則，只有以 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式建立的工具列控制項才支援熱追蹤。 您可以使用其他視窗樣式搭配 **TBSTYLE \_ 平面** 來產生可啟用熱追蹤的工具列，但從一般工具列有不同的外觀。 如需詳細資訊，請參閱 [使用工具列控制項](using-toolbar-controls.md)。

 

 