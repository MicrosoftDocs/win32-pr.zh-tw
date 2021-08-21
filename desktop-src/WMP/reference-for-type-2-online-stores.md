---
title: 類型 2 線上商店的參考
description: 類型 2 線上商店的參考
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player 線上商店，參考
- 線上商店、參考
- 類型2線上商店，參考
- type 2 線上商店的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fabe66bcb65e5bf6701ef03d91b3f0281fbe65eab3f70d3e279ddabf0552d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118834002"
---
# <a name="reference-for-type-2-online-stores"></a>類型 2 線上商店的參考

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

Windows Media Player 10 或更新版本會提供支援類型2線上商店的物件、介面、屬性和方法。 下列各節將詳細說明這些詳細資料。



| 區段                                                                                                        | 描述                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPSubscriptionService 介面](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | 提供方法來增強 (DRM) 的數位版權管理，並起始背景進程。                                                                              |
| [IWMPSubscriptionService2 介面](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | 提供起始背景進程的方法、提供線上商店活動的相關資訊，以及提供 Windows Media Player 核心介面的指標。 |
| [IWMPSubscriptionServiceCallback 介面](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | 定義線上商店用來在背景進程完成時通知 Windows Media Player 的方法。                                                              |
| [WMPNotifySubscriptionPluginAddRemove](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | 用來通知 Windows Media Player 外掛程式已安裝或卸載的函式。                                                                            |
| [DownloadCollection 物件](downloadcollection-object.md)                                                     | 提供方法和屬性來管理下載專案的集合。                                                                                                    |
| [DownloadItem 物件](downloaditem-object.md)                                                                 | 提供與下載要求相關的方法和屬性。                                                                                                              |
| [DownloadManager 物件](downloadmanager-object.md)                                                           | 提供管理下載集合的方法。                                                                                                                            |
| [類型2線上商店的外部物件](external-object-for-type-2-online-stores.md)                       | 提供可從線上商店網頁存取的屬性、方法和事件。                                                                                           |
| [類型2線上商店的列舉](enumerations-for-type-2-online-stores.md)                             | 描述線上商店使用的列舉。                                                                                                                               |
| [Windows Media PlayerBITS 作業慣例](windows-media-player-bits-job-convention.md)                       | 描述使用背景智慧型傳送服務 (位) 的慣例。                                                                                        |
| [Type 2 線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-2-online-store.md) | 描述線上商店必須在使用者電腦上的登錄中建立的登錄專案。                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**輸入2個線上商店**](type-2-online-stores.md)
</dt> </dl>

 

 




