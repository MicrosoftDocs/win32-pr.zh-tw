---
description: 從 Microsoft Windows XP Tablet pc Edition 軟體發展工具組 (SDK) 1.0 版起，系統層級的 Tablet pc 輸入面板會提供通用機制來完成跨 Windows 平臺的文字輸入，不過它不會提供程式設計的存取。 Tablet PC SDK 1.5 版 PenInputPanel 物件將文字輸入工具整合至應用程式。
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: 關於輸入面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044e8c3a43127bd765fd5004329352956e4be8bb9f214f8dda8896fa318832a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844408"
---
# <a name="about-the-input-panel"></a>關於輸入面板

\[[**PenInputPanel**](peninputpanel-class.md) 已被 [**>textinput**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)取代。 如需詳細資訊，請參閱程式 [設計文字輸入面板](programming-the-text-input-panel.md)。\]

從 Microsoft Windows XP Tablet pc Edition 軟體發展工具組 (SDK) 1.0 版起，系統層級的 Tablet pc 輸入面板會提供通用機制來完成跨 Windows 平臺的文字輸入，不過它不會提供程式設計的存取。 Tablet PC SDK 1.5 版 [**PenInputPanel**](peninputpanel-class.md) 物件將文字輸入工具整合至應用程式。

下圖顯示 [ [自動宣告表單範例](auto-claims-form-sample.md) ] 範例中顯示的畫筆輸入面板。

![顯示在自動宣告表單範例範例中的畫筆輸入面板](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

[**PenInputPanel**](peninputpanel-class.md)物件對應用程式開發人員而言很方便。 不需要取代現有表單上的控制項。 您可以直接將 **PenInputPanel** 物件附加至接收文字輸入的現有控制項，而且可以開始接收來自 **PenInputPanel** 物件的輸入。

[**PenInputPanel**](peninputpanel-class.md)物件會從輸入面板採用下列屬性的設定：

-   Layout
-   筆墨厚度
-   辨識超時
-   字體大小、傳送模式，以及東亞的亞洲方塊輸入特定的其他設定

[**PenInputPanel**](peninputpanel-class.md)物件不會提供基礎筆墨的存取權。 若要取得筆墨，請使用 [InkPicture](inkpicture-control-reference.md) 控制項。

[**PenInputPanel**](peninputpanel-class.md)物件提供 (UI) 的就地使用者介面，可供您的應用程式使用者輕鬆地探索。 當使用者使用 tablet 畫筆以 **PenInputPanel** 物件來點擊視窗時，就會自動啟用此功能。 當系統偵測到已附加 **PenInputPanel** 物件之視窗的 CursorButtonUp 事件時，會自動顯示 [畫筆輸入面板]。 您可以 [**將 [自動**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) 啟動] 屬性設定為 **FALSE**，以停用自動啟用。

滑鼠事件上不會自動顯示 [畫筆輸入面板]。 使用終端機服務時，畫筆事件會轉換成滑鼠事件。 [**PenInputPanel**](peninputpanel-class.md)物件無法透過終端機服務連接來運作。

## <a name="pen-input-panel-input-modes"></a>畫筆輸入面板輸入模式

[**PenInputPanel**](peninputpanel-class.md)物件允許鍵盤功能或手寫輸入，以及額外的鍵盤來協助輸入。 [畫筆輸入面板] 的 UI 包括：

-   寫字板
-   適用于東亞語言的書寫板
-   QuickKeys 鍵盤
-   就地鍵盤

書寫板與東亞語言書寫板的可用性，取決於作業系統中使用者的預設地區設定。

### <a name="writing-pad"></a>書寫板

書寫板類似于熟悉的輸入面板 UI。

書寫板會收集終端使用者的手寫。 基本 UI 包含單一書寫線，使用者可以用數位畫筆來撰寫文字。 當使用者完成寫入，並按下 [傳送] 按鈕或等候等待時間時，手寫會傳送至辨識器。

自上次播放筆墨筆劃以來經過一段指定的時間之後，就會辨識筆跡。 當發生超時時，會從收集介面移除筆墨，並進行辨識。 接著會將已辨識的文字插入至 [**PenInputPanel**](peninputpanel-class.md) 物件附加的控制項中。

### <a name="east-asian-multibox-pad"></a>東亞 Multibox Pad

[畫筆輸入面板] 的 [東亞] 版本會顯示輸入亞洲字元的 multibox 介面。 它會提供替代方案，類似于輸入面板的 UI。 使用者可以藉由在 [書寫] 方塊上，然後從 [畫筆輸入] 面板頂端的橫條清單中選取正確的字元，來更正將字元。 篩選按鈕可用來將辨識替代清單範圍縮小為指定的字元類型，例如符號。

除了所有語言外觀通用的迷你快速鍵，書寫板的韓文和日文版還具有轉換金鑰。

若要在東亞語言的書寫板中取得拉丁字元，請設定 [ [**模擬**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) ] 屬性以提高拉丁字元識別的精確度。 針對字母和數位字元，[**設定模擬物件**](factoid-constants.md)**的數位** 字元或 **OneChar** 成員 **的數位字元成員。**

### <a name="quickkeys-keypads"></a>QuickKeys 鍵盤

[畫筆輸入面板] 提供兩個小型鍵盤來輸入符號和數位。

### <a name="in-place-keyboard"></a>就地鍵盤

手寫辨識不足夠的情況下，[畫筆輸入] 面板會提供鍵盤模式。 例如，輸入密碼或元件編號時，使用者可能會使用 [畫筆輸入面板] 鍵盤比書寫板更成功。 這是因為密碼或元件編號不太可能在書寫板的辨識器字典中。

## <a name="recognizer-support"></a>辨識器支援

[**PenInputPanel**](peninputpanel-class.md)物件支援 Windows XP Tablet pc Edition 1.0 版和 Tablet pc SDK 1.5 版的出貨辨識器。

## <a name="automatic-positioning"></a>自動定位

依預設，畫筆輸入面板會自動定位於其附加的控制項。 它不會與控制項重迭，除非畫筆輸入面板和控制項沒有足夠的螢幕空間，或除非開發人員明確地設定畫筆輸入面板的位置。

只有當開發人員未使用 [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) 方法明確設定位置時，才會自動定位函數。 若要覆寫自動定位，請在 [**PanelMoving**](peninputpanel-panelmoving.md)事件處理常式中變更 [**Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)和 [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)屬性的值。

畫筆輸入面板的位置受到螢幕邊緣的限制。 任何螢幕框線的畫筆輸入面板邊緣都不能接近0.25 英寸。

依預設，畫筆輸入面板的頂端會顯示在其所附加之控制項的底部，並以 [**system.windows.controls.primitives.popup.verticaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) 屬性的值分隔控制項。 如果控制項下方沒有足夠的空間，[畫筆輸入面板] 的底部會顯示在其所附加之控制項的頂端，並以 **system.windows.controls.primitives.popup.verticaloffset** 屬性的值與控制項區隔。 如果仍然沒有足夠的空間，例如全螢幕編輯控制項，則畫筆輸入面板會與控制項重迭。

左邊緣的 [輸入面板] 會出現在其所附加之控制項的左邊緣，並以 [**system.windows.controls.primitives.popup.horizontaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) 屬性的值與控制項分隔，但不包括螢幕所限定。 如果所需的位置會將畫筆輸入面板放在可用的螢幕界限之外，畫筆輸入面板會採用最接近可能的水準位置。

### <a name="forced-overlap"></a>強制重迭

畫筆輸入面板有時必須與附加控制項重迭，就像全螢幕編輯控制項的情況一樣。 在這種情況下，會使用下列規則來決定畫筆輸入面板的自動定位：

-   當插入點位於附加控制項的上半部時，畫筆輸入面板的垂直位置會位於畫面底部，可能會放在控制項的下半部。
-   當插入點位於附加控制項的下半部時，畫筆輸入面板的垂直位置會位於畫面頂端，可能會放在控制項的上半部。

### <a name="windowless-controls"></a>無視窗控制項

在 [**PenInputPanel**](peninputpanel-class.md) 物件附加至無視窗控制項的情況下，[畫筆輸入面板] 的位置會相對於無視窗控制項的父代。 在 [**PanelMoving**](peninputpanel-panelmoving.md)事件處理常式中設定 [**Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)和 [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)屬性，或使用 [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)方法手動放置畫筆輸入面板。

 

 
