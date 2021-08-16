---
title: 按鈕類型
description: 有數種類型的按鈕，以及一或多個按鈕樣式來區別相同類型的按鈕。
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c3614f90c36d5a81603153ec7c8612d61e73e2e98c7f668cb53a6ad2bb584b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832491"
---
# <a name="button-types"></a>按鈕類型

有數種類型的按鈕，以及一或多個按鈕樣式來區別相同類型的按鈕。

本檔討論下列主題。

-   [按鈕類型和樣式](#button-types-and-styles)
-   [核取方塊](#check-boxes)
-   [群組方塊](#group-boxes)
-   [推播按鈕](#push-buttons)
-   [選項按鈕](#radio-buttons)
-   [相關主題](#related-topics)

## <a name="button-types-and-styles"></a>按鈕類型和樣式

按鈕屬於某個類型，而且可能會有會影響其外觀和行為的其他樣式。 如需按鈕樣式的表格，請參閱 [按鈕樣式](button-styles.md)。

下列螢幕擷取畫面顯示不同類型的按鈕。

![對話方塊的螢幕擷取畫面，其中顯示八種按鈕類型的範例](images/buttontypes.png)

螢幕擷取畫面會顯示 Windows Vista 中的按鈕可能出現的方式。 外觀會因不同的作業系統版本而異，而且會根據使用者設定的主題而有所不同。

請注意下列關於圖例的重點：

-   這三個狀態的核取方塊會顯示為 [不定] 狀態。 核取或取消核取時，看起來像是正常核取方塊。
-   大型推播按鈕已設定為以程式設計方式 (，方法是將 [**BM \_ SETSTATE**](bm-setstate.md) 訊息傳送) ，讓它保留其外觀，即使未按下也是一樣。
-   在顯示的視覺化樣式中，預設的 [推送] 按鈕 (或另一個具有輸入焦點的推播按鈕) 在藍色和灰色之間迴圈。

## <a name="check-boxes"></a>核取方塊

*核取方塊* 是由方塊和應用程式定義的標籤、圖示或點陣圖所組成，表示使用者可以藉由選取按鈕來進行選擇。 應用程式通常會顯示覆選框，讓使用者可以選擇一或多個非互斥的選項。

核取方塊可以是下列四種樣式之一：標準、自動、三狀態和自動三種狀態，如常數 [**BS \_ 核取方塊**](button-styles.md)、 [**BS \_ AUTOCHECKBOX**](button-styles.md)、 [**BS \_ 3STATE**](button-styles.md)和 [**BS \_ AUTO3STATE**](button-styles.md)分別定義。 每個樣式都可以假設有兩個檢查狀態：核取 () 中的核取記號，或已清除 (no 核取記號) 。 此外，三個狀態的核取方塊可假設有不定的狀態 (核取方塊) 內的陰影方塊，這可能表示使用者尚未進行選擇。 重複按一下 [標準] 或 [自動] 核取方塊，會將它從 checked 切換為已清除，然後再重新開啟。 重複按三個狀態的核取方塊，會將它從 checked 切換為不確定，然後重複迴圈。

當使用者按一下任何樣式)  (的核取方塊時，此核取方塊就會收到鍵盤焦點。 系統會傳送包含 [BN \_ 點擊](bn-clicked.md)通知碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息給核取方塊的父視窗。 如果父視窗來自自動核取方塊或自動三態核取方塊，則不需要處理此訊息，因為系統會自動設定這些樣式的檢查狀態。 但是，如果父視窗負責設定這些樣式的檢查狀態，父視窗就必須處理訊息，因為它來自非自動核取方塊或三個狀態的核取方塊。 無論核取方塊樣式為何，系統都會在其狀態變更時自動重新繪製核取方塊。

應用程式可以使用 [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) 函數來確定核取方塊的狀態。

## <a name="group-boxes"></a>群組方塊

*群組方塊* 是圍繞一組控制項（例如核取方塊或選項按鈕）的矩形，其左上角有應用程式定義的文字標籤。 群組方塊的唯一目的是要組織一般用途所相關的控制項， (通常是由標籤) 來表示。 [群組] 方塊只有一個樣式，由常數 [**BS \_ 分組**](button-styles.md)框所定義。 因為無法選取群組方塊，所以不會有檢查狀態、焦點狀態或推送狀態。

## <a name="push-buttons"></a>推播按鈕

下拉 *按鈕* 是一個矩形，其中包含應用程式定義的文字標籤、圖示或點陣圖，指出當使用者選取按鈕時，該按鈕的功能。

推播按鈕可以是下列兩種樣式的其中一個： [標準] 或 [預設]，如 [常數] [**BS \_ 按鈕**](button-styles.md) 和 [ [**BS \_ DEFPUSHBUTTON**](button-styles.md)] 所定義。 標準的 [推送] 按鈕通常用來啟動操作。 當使用者按一下該按鈕時，它就會收到鍵盤焦點。 預設的 [推送] 按鈕通常用來指出最常見或預設的選項，例如關閉對話方塊。 它是使用者可以選取的按鈕，只要在對話方塊中沒有其他的 [推播] 按鈕具有輸入焦點時按下 ENTER 即可。

當使用者按一下 [按下] 按鈕時，它會收到鍵盤焦點。 系統會傳送包含 [BN \_ 點擊](bn-clicked.md)通知碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息給按鈕的父視窗。

[*分割] 按鈕* 是 Windows Vista 和 [6.00 版](common-control-versions.md)引進的一種特殊的推播按鈕。 分割按鈕分為兩個部分。 主要部分的功能就像一般或預設的推播按鈕。 第二個部分的箭號指向向下。 按一下箭號時，通常會顯示功能表。

[分割] 按鈕具有 [ [**BS] \_ SPLITBUTTON**](button-styles.md) 樣式，或 [ [**BS \_ DEFSPLITBUTTON**](button-styles.md) ] 樣式（如果它是對話方塊中的 [預設值] 按鈕）。 您可以使用 [ [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md) ] 訊息或對應的 [**按鈕 \_ SETSPLITINFO**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) 宏來修改按鈕的外觀。

當使用者按一下 [分割] 按鈕的主要部分時，它會傳送 [BN 按 \_ ](bn-clicked.md) 下通知，就像一般的推播按鈕一樣。 但是，當使用者按一下向下箭號時，就會傳送 [BCN 的 \_ 下拉式清單](bcn-dropdown.md) 通知。 應用程式必須負責顯示功能表以回應 BCN \_ 下拉式清單。

WindowsVista 和 [6.00 版](common-control-versions.md)也引進了另一種推播按鈕，也就是 *命令連結*。 命令連結會以視覺化方式與一般的 [推送] 按鈕不同，但具有相同的功能。 命令連結通常會以較小的字型顯示箭號圖示、文字行和其他文字。

## <a name="radio-buttons"></a>選項按鈕

選項按鈕 (也稱為 *單選* 按鈕) 是由圓形按鈕和應用程式定義的標籤、圖示或點陣圖所組成，表示使用者可以藉由選取按鈕所做的選擇。 應用程式通常會在群組方塊中使用選項按鈕，讓使用者可以選擇一組相關但互斥選項的其中一個。

選項按鈕可以是下列兩種樣式之一： [標準] 或 [自動]，如 [樣式常數] [**BS \_ 選項按鈕**](button-styles.md) 和 [ [**BS \_ AUTORADIOBUTTON**](button-styles.md)] 所定義。 每個樣式都可以假設有兩個檢查狀態：已核取 (按鈕中的點) 或已清除 (按鈕) 中沒有任何點。

當使用者選取其中一個狀態時，選項按鈕會收到鍵盤焦點。 系統會傳送包含 [BN \_ 點擊](bn-clicked.md)通知碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息給按鈕的父視窗。 如果父視窗來自自動選項按鈕，就不需要處理此訊息，因為系統會自動設定該樣式的檢查狀態。 但是，父視窗應該處理來自非自動選項按鈕的訊息，因為父視窗負責設定該樣式的檢查狀態。 不論選項按鈕樣式為何，系統都會自動將按鈕重新繪製為其狀態變更。

選項按鈕會以群組排列，而且可以隨時檢查群組中的一個按鈕。 如果已設定任何選項按鈕的 [**WS \_ 群組**](/windows/desktop/winmsg/window-styles) 旗標，該按鈕會是群組中的第一個按鈕，而緊接在定位順序中的所有按鈕會立即在定位順序中 (但不會有 **WS \_ 群組** 旗標) 屬於其群組的一部分。 如果沒有任何選項按鈕具有 **WS \_ 群組** 旗標，則對話方塊中的所有選項按鈕都會被視為單一群組。

應用程式可以使用 [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) 函數來確定是否已核取選項按鈕。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[按鈕樣式](button-styles.md)
</dt> <dt>

**概念**
</dt> <dt>

[使用按鈕](using-buttons.md)
</dt> </dl>

 

 