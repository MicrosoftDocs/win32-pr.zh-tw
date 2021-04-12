---
title: 關於自訂繪圖
description: 本章節包含有關自訂繪製功能的一般資訊，並提供應用程式如何支援自訂繪製的概念總覽。
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121a4df5aa6fab222a5c4387ebdcfba51a7977b2
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463864"
---
# <a name="about-custom-draw"></a>關於自訂繪圖

本章節包含有關自訂繪製功能的一般資訊，並提供應用程式如何支援自訂繪製的概念總覽。 目前，下列控制項支援自訂繪製功能：

-   標題控制項
-   清單視圖控制項
-   Rebar 控制項
-   工具列控制項
-   工具提示控制項
-   [請] 控制項
-   樹狀檢視控制項

<!-- -->

-   [關於自訂繪製通知訊息](#about-custom-draw-notification-messages)
-   [繪製迴圈、繪製階段和通知訊息](#paint-cycles-drawing-stages-and-notification-messages)
-   [利用自訂繪圖服務](#taking-advantage-of-custom-draw-services)
    -   [回應 prepaint 通知](#responding-to-the-prepaint-notification)
    -   [要求專案特定通知](#requesting-item-specific-notifications)
    -   [自行繪製專案](#drawing-the-item-yourself)
    -   [變更字型和色彩](#changing-fonts-and-colors)
-   [使用 List-View 和 Tree-View 控制項的自訂繪圖](#custom-draw-with-list-view-and-tree-view-controls)
    -   [使用 List-View 控制項的自訂繪圖](#custom-draw-with-list-view-controls)
-   [相關主題](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>關於自訂繪製通知訊息

所有支援自訂繪製的通用控制項，會在繪圖作業期間的特定點傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 這些通知碼描述適用于整個控制項的繪圖作業，以及控制項內專案特定的繪製作業。 如同許多通知碼，NM \_ CUSTOMDRAW 通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。

自訂繪製通知的 *lParam* 參數將會是 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) 結構的位址，或是包含 **NMCUSTOMDRAW** 結構作為其第一個成員的控制項特定結構。 下表說明控制項與其使用的結構之間的關聯性。



| 結構                                | 使用對象                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Rebar、頁首及標題控制項 |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | 清單視圖控制項                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | 工具列控制項                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | 工具提示控制項                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | 樹狀檢視控制項                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>繪製迴圈、繪製階段和通知訊息

如同所有 Windows 應用程式，通用控制項會根據從系統或其他應用程式接收到的訊息，定期進行繪製和清除。 控制項繪製或清除的進程稱為「 *繪製迴圈*」。 支援自訂繪製的控制項會透過每個油漆週期定期傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 此通知碼伴隨著 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) 結構或另一個結構，其中包含 **NMCUSTOMDRAW** 結構作為其第一個成員。

[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構所包含的其中一項資訊是繪製週期的目前階段。 這稱為「 *繪製階段* 」，並以結構 **dwDrawStage** 成員中的值表示。 控制項會通知其父系大約四個基本繪圖階段。 這些基本或全域繪圖階段會以下列旗標值在結構中表示， (在 Commctrl 中定義) 。



| 全域繪製階段值 | Description                        |
|--------------------------|------------------------------------|
| CDDS \_ PREPAINT           | 開始繪製迴圈之前。     |
| CDDS \_ POSTPAINT          | 繪製迴圈完成之後。 |
| CDDS \_ PREERASE           | 開始清除迴圈之前。     |
| CDDS \_ POSTERASE          | 清除迴圈完成之後。 |



 

上述每個值都可以與 CDDS \_ 專案旗標結合，以指定專案特定的繪製階段。 為了方便起見，Commctrl 包含下列專案特定的值。



| 專案特定的繪製階段值 | Description                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDDS \_ ITEMPREPAINT              | 繪製專案之前。                                                                                                                                                                                                                                                            |
| CDDS \_ ITEMPOSTPAINT             | 繪製專案之後。                                                                                                                                                                                                                                                       |
| CDDS \_ ITEMPREERASE              | 清除專案之前。                                                                                                                                                                                                                                                           |
| CDDS \_ ITEMPOSTERASE             | 清除專案之後。                                                                                                                                                                                                                                                      |
| CDDS \_ 子項                   | [通用控制項版本](common-control-versions.md) 4.71。 \_ \_ 如果正在繪製子工作，則為與 CDDS ITEMPREPAINT 或 CDDS ITEMPOSTPAINT 結合的旗標。 只有在 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) 是從 CDDS PREPAINT 傳回時才會設定 \_ 。 |



 

您的應用程式必須處理 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼，然後傳回特定值，通知控制項它必須做什麼。 如需這些傳回值的詳細資訊，請參閱下列各節。

## <a name="taking-advantage-of-custom-draw-services"></a>利用自訂繪圖服務

利用自訂繪製功能的關鍵是回應控制項所傳送的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 應用程式為了回應這些通知所傳送的傳回值，會決定該繪製週期的控制項行為。

本節包含有關應用程式如何使用 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知傳回值來判斷控制項行為的資訊。

詳細資料分成下列主題：

-   [回應 prepaint 通知](#responding-to-the-prepaint-notification)
-   [要求專案特定通知](#requesting-item-specific-notifications)
-   [自行繪製專案](#drawing-the-item-yourself)
-   [變更字型和色彩](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>回應 prepaint 通知

在每個繪製週期的開頭，控制項會傳送 [nm \_ CUSTOMDRAW](nm-customdraw.md) 通知碼， \_ 在隨附的 NM CUSTOMDRAW 結構的 **dwDrawStage** 成員中指定 CDDS PREPAINT 值 \_ 。 您的應用程式傳回給第一個通知的值，會指定控制項如何和何時針對該繪製迴圈的其餘部分傳送後續的自訂繪製通知。 您的應用程式可以傳回下列旗標的組合，以回應第一個通知。



| 傳回值            | 效果                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDRF \_ DODEFAULT         | 控制項將會自行繪製。 它不會針對此繪製週期傳送額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知。 此旗標不可與任何其他旗標一起使用。                                                                                                                                                                                                                                                                               |
| CDRF \_ DOERASE           | 控制項只會繪製背景。                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CDRF \_ NEWFONT           | 您的應用程式已為專案指定新字型;控制項將會使用新的字型。 如需變更字型的詳細資訊，請參閱 [變更字型和色彩](#changing-fonts-and-colors)。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。                                                                                                                                                                                                       |
| CDRF \_ NOTIFYITEMDRAW    | 控制項將會通知任何專案特定繪圖作業的父系。 它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。                                                                                                                                                                                                                       |
| CDRF \_ NOTIFYPOSTERASE   | 控制項將會在清除專案之後通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。                                                                                                                                                                                                                                                                                                                                             |
| CDRF \_ NOTIFYPOSTPAINT   | 當整個控制項的繪製迴圈完成時，控制項將傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。                                                                                                                                                                                                                                                                 |
| CDRF \_ NOTIFYSUBITEMDRAW | [版本 4.71](common-control-versions.md)。 您的應用程式將會在[ \_ ](nm-customdraw.md)  \_ \| \_ 繪製每個清單-view 子集合之前，收到 CUSTOMDRAW 通知，並將 dwDrawStage 設定為 CDDS ITEMPREPAINT CDDS 子。 然後，您可以分別為每個子項指定字型和色彩，或針對預設處理傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md) 。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。 |
| CDRF \_ SKIPDEFAULT       | 您的應用程式會以手動方式繪製專案。 控制項不會繪製專案。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。                                                                                                                                                                                                                                                                                                                      |
| CDRF \_ SKIPPOSTPAINT     | 控制項不會在專案周圍繪製焦點矩形。                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>要求專案特定通知

如果您的應用程式將 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) 傳回到初始 prepaint 自訂繪製通知，此控制項就會傳送該繪製迴圈期間所繪製之每個專案的通知。 這些專案特定的通知 \_ 在隨附 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員中將會有 CDDS ITEMPREPAINT 值。 您可以要求控制項在完成繪製專案時傳送另一個通知，方法是將 [**CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) 傳給這些專案特定的通知。 否則，會傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md) ，而且控制項在開始繪製下一個專案之前，不會通知父視窗。

### <a name="drawing-the-item-yourself"></a>自行繪製專案

如果您的應用程式繪製整個專案，請傳回 [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md)。 這可讓控制項略過不需要繪製的專案，藉此減少系統額外負荷。 請記住，傳回這個值表示控制項不會繪製專案的任何部分。

### <a name="changing-fonts-and-colors"></a>變更字型和色彩

您的應用程式可以使用自訂繪製來變更專案的字型。 只要選取您想要的 HFONT 到與自訂繪製通知相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **hdc** 成員所指定的裝置內容中。 由於您選取的字型可能會有不同于預設字型的度量，請確定您在通知訊息的傳回值中包含 [**CDRF \_ NEWFONT**](cdrf-constants.md) 位。 如需使用這項功能的詳細資訊，請參閱 [使用自訂繪製](using-custom-draw.md)的範例程式碼。 您的應用程式所指定的字型會用來顯示未選取的專案。 自訂繪圖不允許您變更所選取專案的字型屬性。

若要變更所有支援自訂繪製之控制項的文字色彩，但清單視圖和樹狀檢視除外，只要在自訂繪製通知結構所提供的裝置內容中，使用 [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) 和 [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) 函式來設定所需的文字和背景色彩。 若要修改清單視圖或樹狀檢視中的文字色彩，您需要將所需的色彩值放在 [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw)或 [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw)結構的 **clrText** 和 **clrTextBk** 成員中。

> [!Note]  
> 在 [6.0 版](common-control-versions.md) 的通用控制項之前，工具列會忽略 [**CDRF \_ NEWFONT**](cdrf-constants.md) 旗標。 版本6.0 支援 **CDRF \_ NEWFONT** 旗標，您可以使用它來為工具列選取不同的字型。 不過，視覺效果樣式為作用中時，您無法變更工具列的色彩。 若要變更6.0 版中的工具列色彩，您必須先藉由呼叫 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) 並不指定視覺化樣式來停用視覺化樣式：

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>使用 List-View 和 Tree-View 控制項的自訂繪圖

大部分的常見控制項都可以用相同的方式來處理。 不過，清單視圖和樹狀檢視控制項有一些功能需要稍微不同的方式來自訂繪圖。

針對 [版本 5.0](common-control-versions.md)，如果您藉由傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)來變更字型，則這兩個控制項可能會顯示裁剪的文字。 這是與舊版通用控制項的回溯相容性所需的行為。 如果您想要變更清單視圖或樹狀檢視控制項的字型，如果您在將任何專案加入至控制項之前，將 *wParam* 值設定為5，則會得到更 [**好的結果 \_**](ccm-setversion.md) 。 如需使用自訂繪製的樹狀檢視控制項範例，請參閱知識庫檔 [範例： CustDTv 說明 TreeView 中的自訂繪製 (Q248496) ]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)。

### <a name="custom-draw-with-list-view-controls"></a>使用 List-View 控制項的自訂繪圖

由於清單視圖控制項有子工作和多個顯示模式，因此您必須以不同于其他常見控制項的方式來處理 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知。

若為報表模式，請使用下列程式。

1.  第一個 [NM \_ CUSTOMDRAW](nm-customdraw.md)通知會將相關聯 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員設為 CDDS \_ PREPAINT。 傳回 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md)。
2.  然後，您會收到具有 **dwDrawStage** 設定為 CDDS ITEMPREPAINT 的 [NM \_ CUSTOMDRAW](nm-customdraw.md)通知 \_ 。 如果您指定新的字型或色彩並傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)，則會變更專案的所有子專案。 如果您想要改為個別處理每個子項，請傳回 [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md)。
3.  如果您在上一個步驟中傳回 [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md) ，您就會收到每個子項的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知， **dwDrawStage** 設定為 CDDS 子工作 \_ \| CDDS \_ ITEMPREPAINT。 若要變更該子工作的字型或色彩，請指定新的字型或色彩，並傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)。

針對大型圖示、小型圖示和清單模式，請使用下列程式。

1.  第一個 [NM \_ CUSTOMDRAW](nm-customdraw.md)通知會將相關聯 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員設為 CDDS \_ PREPAINT。 傳回 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md)。
2.  然後，您會收到具有 **dwDrawStage** 設定為 CDDS ITEMPREPAINT 的 [NM \_ CUSTOMDRAW](nm-customdraw.md)通知 \_ 。 您可以藉由指定新的字型和色彩並傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)，來變更專案的字型或色彩。 因為這些模式沒有子項，所以您不會收到任何額外的 NM \_ CUSTOMDRAW 通知。

如需清單-view [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知處理常式的範例，請參閱 [使用自訂繪製](using-custom-draw.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[使用自訂繪圖](using-custom-draw.md)
</dt> <dt>

[自訂繪圖參考](custom-draw-reference.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[範例： CustDTv 說明 TreeView 中的自訂繪製 (Q248496) ]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 