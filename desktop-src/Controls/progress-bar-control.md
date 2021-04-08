---
title: 關於進度列控制項
description: 進度列是一種視窗，可讓應用程式用來指出冗長作業的進度。 它是由在作業進行時動畫的矩形所組成。
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00c80b1f9e97cec1657fe979a19437f607251b8
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683145"
---
# <a name="about-progress-bar-controls"></a>關於進度列控制項

進度列是一種視窗，可讓應用程式用來指出冗長作業的進度。

它是由在作業進行時動畫的矩形所組成。

下圖顯示不使用視覺化樣式的進度列。

![進度列的螢幕擷取畫面，可線上條中新增矩形以表示進度](images/pb-oldstyle.png)

下圖顯示使用視覺化樣式的進度列。 控制項的外觀會依作業系統和選取的主題而有所不同。 如需詳細資訊，請參閱 [視覺化樣式](themes-overview.md)。

![進度列的螢幕擷取畫面，可延長動畫的綠色矩形以表示進度](images/pb-newstyle.png)

下列標題底下包含詳細資訊。

-   [使用進度列](#using-progress-bars)
    -   [範圍和目前的位置](#range-and-current-position)
    -   [預設進度列訊息處理](#default-progress-bar-message-processing)
    -   [天棚樣式](#marquee-style)

## <a name="using-progress-bars"></a>使用進度列

您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立進度列，並指定 [**進度 \_ 類別**](common-control-window-classes.md) 視窗類別。 載入通用控制項 DLL 時，會註冊此視窗類別。 如需詳細資訊，請參閱 [關於通用控制項](common-controls-intro.md)。

您也可以在 Microsoft Visual Studio 的 [工具箱] 中取得控制項，在其中呼叫進度控制項。

### <a name="range-and-current-position"></a>範圍和目前的位置

進度列的 *範圍* 代表整個作業的持續時間，而 *目前的位置* 則代表應用程式完成作業所完成的進度。 視窗程式會使用範圍和目前的位置，來決定要以醒目提示色彩填滿的進度列百分比。

如果您未設定範圍值，系統會將最小值設定為0，並將最大值設定為100。 您可以使用 [**PBM \_ SETRANGE**](pbm-setrange.md) 訊息，將範圍調整為方便的整數。

進度列提供數個可供您用來設定目前位置的訊息。 [**PBM \_ SETPOS**](pbm-setpos.md)訊息會將位置設定為指定的值。 [**PBM \_ DELTAPOS**](pbm-deltapos.md)訊息會將指定的值加入至目前的位置，以將位置往前移。

[**PBM \_ SETSTEP**](pbm-setstep.md)訊息可讓您指定進度列的步驟增量。 之後，每當您將 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息傳送到進度列時，目前的位置就會以指定的增量前進。 依預設，步驟遞增會設定為10。

### <a name="default-progress-bar-message-processing"></a>預設進度列訊息處理

本節說明由 [**進度 \_ 類別**](common-control-window-classes.md) 類別的視窗程式所處理的訊息。



| 訊息            | 處理已執行                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ 建立**     | 配置並初始化初始結構。                                                                                                                                    |
| **WM 損 \_ 毀**    | 釋出與進度列相關聯的所有資源。                                                                                                                              |
| **WM \_ ERASEBKGND** | 繪製進度列的背景和框線。                                                                                                                              |
| **WM \_ GETFONT**    | 傳回目前字型的控制碼。 進度列目前不會繪製文字，因此傳送此訊息不會影響控制項。                                       |
| **WM \_ 油漆**      | 繪製進度列。 如果 *wParam* 參數不是 **Null**，則控制項會假設值為 HDC，並且使用該裝置內容繪製。                              |
| **WM \_ SETFONT**    | 將控制碼儲存至新的字型，並將控制碼傳回至先前的字型。 進度列目前不會繪製文字，因此傳送此訊息不會影響控制項。 |



 

### <a name="marquee-style"></a>天棚樣式

藉由建立具有 [**PBS \_ 字幕**](progress-bar-control-styles.md) 樣式的進度列控制項，您可以用顯示活動的方式建立動畫，但不會指出工作的完成比例。 進度列反白顯示的部分會隨著橫條的長度重複移動。 您可以藉由傳送 [**PBM \_ SETMARQUEE**](pbm-setmarquee.md) 訊息來開始和停止動畫，以及控制其速度。 天棚進度列沒有範圍或位置。

下圖顯示捲軸模式的進度列。 反白顯示的部分會在橫條之間移動。

![進度列的螢幕擷取畫面，在灰色矩形上移動綠色醒目提示以表示進度](images/pb-marquee.png)

 

 