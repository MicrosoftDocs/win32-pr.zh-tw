---
title: 第2型線上商店的購買整合
description: 第2型線上商店的購買整合
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player 線上商店、購買整合
- 線上商店、購買整合
- 類型2線上商店，購買整合
- Windows Media Player 線上商店，整合購買專案
- 線上商店，整合購買
- 輸入2個線上商店，整合購買
- Windows Media Player，購買整合
- Windows Media Player，整合購買
- 購買整合
- 整合購買
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d854ecfd91cd0a887c242ad743874a6ec1a469ebcca3aa788bf57c2c59041d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746692"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>第2型線上商店的購買整合

當 Windows Media Player 播放數位媒體內容或使用者選擇 [**尋找專輯資訊**] 時，播放程式會提供一個連結，讓使用者在有可用的連結時，購買內容所源自的 CD 或 DVD。 當使用者按一下連結時，會在目前的音樂商店上 Windows Media Player 10 或更新的呼叫，以處理購買要求。 發生這種情況時，播放程式會流覽至第一個服務工作窗格 (Windows Media Player 10) 或 Windows Media Player 11) 中的 [線上商店] 索引標籤 (，並顯示 ServiceInfo 檔之 **BuyCD** 元素的 **MediaPlayerURL** 屬性所指定的網頁。  (**MediaCenterURL** 和 **BrowserURL** 屬性會以類似的方式使用，以處理來自 Windows XP Media Center Edition 2004 和 Windows XP Service Pack 2) 的呼叫。

Windows Media Player 會將查詢字串附加至 URL，以提供有關使用者選擇要購買之內容的線上商店資訊。 查詢字串包含 **標題**、 **專輯** 和 **演出者** 等屬性，可供線上商店用來判斷要銷售的正確專輯。 **BuyCD** 元素的參考檔會提供查詢字串屬性及其描述的完整清單。

## <a name="guidelines-for-the-buycd-page"></a>BuyCD 頁面的指導方針

建立 BuyCD 網頁時，請使用下列指導方針：

-   頁面必須清楚地識別提供資訊的線上商店。 例如，您可以藉由醒目顯示您的標誌來完成這項作業。
-   此頁面必須包含您公司隱私權聲明的連結。
-   最好提供初始購買資訊，而不需要使用者安裝程式或登入您的線上商店。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Type 2 線上商店**](about-type-2-online-stores.md)
</dt> <dt>

[**BuyCD 元素**](buycd-element.md)
</dt> </dl>

 

 




