---
title: 控制 Spy 2.0 版
description: Control Spy 是一種工具，可協助開發人員瞭解一般控制項如何將樣式套用至這些控制項，以及它們如何回應訊息和通知。
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104024260"
---
# <a name="control-spy-v20"></a>控制 Spy 2.0 版

Control Spy 是協助開發人員瞭解通用控制項的工具：如何將樣式套用至這些控制項，以及它們如何回應訊息和通知。 您可以使用 Control Spy 來立即查看不同的樣式如何影響每個控制項的行為和外觀，也可以透過傳送訊息來變更每個控制項的狀態。

有兩個版本的 Control Spy 可供使用，一個用於 [Comctl32.dll 5.X 版](common-control-versions.md) ，另一個用於 Comctl32.dll 6.0 版和更新版本。 ControlSpyV6.exe 有內建的應用程式資訊清單，因此它會使用較新的主題控制項。 ControlSpyV5.exe 沒有這個資訊清單，因此預設為較舊的版本。

本主題包含下列各節。

-   [概觀](#overview)
-   [樣式](#styles)
-   [訊息](#messages)
-   [大小/色彩](#sizecolor)
-   [哪裡可以取得 Control Spy](#where-to-get-control-spy)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

Control Spy 會將選取的通用控制項裝載在其應用程式視窗的中央。 您可以從視窗左側的清單方塊中選取不同的控制項，來變更顯示的控制項。 控制項所收到的訊息或通知，將會列在視窗的右側。 您可以使用 [接收到的 **訊息** 和 **收到的通知** ] 核取方塊來啟用或停用這項功能。

下圖顯示「控制項 Spy」應用程式。

![控制 spy 視窗](images/controlspy-main.png)

在視窗底部，有數個索引標籤會呈現更多功能。

## <a name="styles"></a>樣式

[ **樣式** ] 索引標籤可讓您變更控制項目前的視窗樣式。 選取或取消選取任何列出的樣式，然後按一下 [套用 **] 按鈕來** 變更所顯示控制項的樣式。 或者，您可以使用 [ **重新** 建立] 按鈕，以選取的樣式來建立新的控制項。 [ **重設** ] 按鈕會將控制項傳回到預設樣式。

索引標籤下方的 **複製樣式** 和 **複製 ExStyle** 按鈕會將選取的樣式常數複製到剪貼簿，作為位或 (\|) 分隔清單。 您可以將此清單直接貼到 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 的呼叫中，以在您自己的應用程式中以相同的樣式提供控制項。

下圖顯示按鈕控制項的 [ **樣式** ] 索引標籤。

![控制 spy 樣式索引標籤](images/controlspy-styles.png)

## <a name="messages"></a>訊息

[ **訊息** ] 索引標籤可讓您將幾乎任何訊息傳送至控制項。 從清單方塊中選取訊息之後，您就可以輸入資料，而該資料會以 *wParam* 和 *lParam* 參數的形式傳送至 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)的呼叫。 當您按一下 [ **傳送**] 之後，訊息會傳送至控制項，而且任何結果都會顯示在索引標籤底部的文字方塊中。

下圖顯示選取特定訊息時的 [訊息] 索引標籤。

![控制 spy 訊息索引標籤](images/controlspy-messages.png)

## <a name="sizecolor"></a>大小/色彩

[ **大小]/[色彩** ] 索引標籤可以用來變更控制項的大小，以及其背景的色彩。

## <a name="where-to-get-control-spy"></a>哪裡可以取得 Control Spy

您可以從 MSDN 下載 [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) 。 這兩個版本都包含在下載中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 控制項](window-controls.md)
</dt> <dt>

[啟用視覺化樣式](cookbook-overview.md)
</dt> </dl>

 

 