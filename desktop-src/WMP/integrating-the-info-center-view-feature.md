---
title: 整合資訊中心視圖功能
description: 整合資訊中心視圖功能
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player 線上商店，整合資訊中心視圖
- 線上商店，整合資訊中心視圖
- 輸入1個線上商店，整合資訊中心視圖
- 輸入2個線上商店，整合資訊中心視圖
- Windows Media Player 線上商店，資訊中心視圖
- 線上商店，資訊中心視圖
- 輸入1個線上商店，資訊中心視圖
- 類型2線上商店，資訊中心視圖
- 整合資訊中心視圖
- 資訊中心視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caea279f933c3cbb411da72aab9ddf971df5f38c69d7291ae4ac67f7b96ed91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135461"
---
# <a name="integrating-the-info-center-view-feature"></a>整合資訊中心視圖功能

Windows Media Player 可讓使用者開啟和關閉資訊中心視圖功能。 資訊中心視圖是使用者預期尋找有關特定數位媒體內容之豐富、延伸資訊的功能。 當使用者選擇開啟資訊中心視圖時，Windows Media Player 在目前的音樂商店上進行呼叫，以顯示 ServiceInfo 檔的 **資訊中心** 元素的 **URL** 屬性所指定的資訊中心視圖網頁。

若要取得目前播放中數位媒體內容的相關資訊，您必須在網頁中內嵌 Windows Media Player 控制項的實例，並使用 Player 物件模型。 例如，若要取出標題，您可以使用下列 JScript 程式碼：


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>資訊中心視圖的指導方針

建立 **資訊中心視圖** 網頁時，請使用下列指導方針：

-   頁面必須清楚地識別提供資訊的線上商店。 例如，您可以藉由醒目顯示您的標誌來完成這項作業。
-   此頁面必須包含您公司隱私權聲明的連結。
-   請盡可能避免在資訊中心視圖功能內進行頁面導覽。 您應該流覽至您的線上商店以尋找大部分的活動。
-   最好提供寶貴的資訊，而不需要使用者安裝程式或登入您的線上商店。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**資訊中心元素**](infocenter-element.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**在 Web 網頁中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




