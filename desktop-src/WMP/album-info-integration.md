---
title: 專輯資訊整合
description: 專輯資訊整合
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player 線上商店，專輯資訊整合
- 線上商店，專輯資訊整合
- 類型2線上商店，專輯資訊整合
- Windows Media Player 線上商店，整合專輯資訊
- 線上商店，整合專輯資訊
- 輸入2個線上商店，整合專輯資訊
- Windows Media Player，整合專輯資訊
- Windows Media Player，專輯資訊整合
- 專輯資訊整合
- 整合專輯資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021367"
---
# <a name="album-info-integration"></a>專輯資訊整合

Windows Media Player 可讓使用者透過按一下按鈕（例如 **詳細資訊**），來要求數位媒體內容所產生的 CD 或 DVD 相關的詳細資訊。 當使用者按一下按鈕時，Windows Media Player 10 或更新版本會在目前的音樂商店上進行呼叫，以顯示專輯詳細資料。 當發生這種情況時，播放程式會開啟 [專輯資訊] 窗格，並顯示 ServiceInfo 檔中 **AlbumInfo** 元素的 [ **URL** ] 屬性所指定的網頁。

Windows Media Player 會將查詢字串附加至 URL，以提供有關使用者所要求內容的線上商店資訊。 查詢字串包含 **標題**、 **專輯** 和 **演出者** 等屬性，可供線上商店用來決定要顯示的正確專輯。 **AlbumInfo** 元素的參考檔會提供查詢字串屬性及其描述的完整清單。

## <a name="guidelines-for-album-info"></a>專輯資訊的指導方針

建立您的專輯資訊網頁時，請使用下列指導方針：

-   頁面必須清楚地識別提供資訊的線上商店。 例如，您可以藉由醒目顯示您的標誌來完成這項作業。
-   此頁面必須包含您公司隱私權聲明的連結。
-   請盡可能避免在專輯資訊功能中進行頁面導覽。 您應該流覽至您的線上商店以尋找大部分的活動。
-   建議您提供寶貴的資訊，而不需要使用者安裝程式或登入您的線上商店。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Type 2 線上商店**](about-type-2-online-stores.md)
</dt> <dt>

[**AlbumInfo 元素**](albuminfo-element.md)
</dt> </dl>

 

 




