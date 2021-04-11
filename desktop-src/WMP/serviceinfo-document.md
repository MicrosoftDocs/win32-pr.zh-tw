---
title: ServiceInfo 檔
description: ServiceInfo 檔
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入1個線上商店、ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539c4e1a58e5dbf88e1fc79909791a7dab767ef1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021097"
---
# <a name="serviceinfo-document"></a>ServiceInfo 檔

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

線上商店必須撰寫 ServiceInfo.xml 檔。 這是當 Windows Media Player 10 或更新版本裝載線上商店時，線上商店用來設定 Windows Media Player 使用者介面的檔。

Windows Media Player 線上商店支援下列元素及其屬性。



| 元素                                      | 描述                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | 指定當使用者選擇要查看特定媒體專案的詳細資訊時，Windows Media Player 顯示之網頁的 URL。類型1：選擇性<br/> 類型2音樂：必要<br/> 類型2商務：已忽略<br/>                                |
| [ButtonText](buttontext-element.md)         | 指定 Windows Media Player 針對工作窗格按鈕顯示的文字字串。類型1：必要<br/> 類型2音樂：必要<br/> 類型2商務：必要<br/>                                                                                             |
| [ButtonTip](buttontip-element.md)           | 指定當使用者指向工作窗格按鈕時所顯示的工具提示。類型1：選擇性<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | 指定當使用者選擇進行購買時，Windows Media Player 顯示的網頁 Url。類型1：必要<br/> 類型2音樂：必要<br/> 類型2商務：已忽略<br/>                                                                      |
| [色彩](color-element.md)                   | 指定線上商店導覽按鈕的背景色彩。類型1：選擇性<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                                                             |
| [說明](description-element.md)       | 指定在安裝 Windows Media Player 的第一次體驗期間顯示的線上商店描述。 需要 Windows Media Player 11。類型1：必要<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/> |
| [DownloadStatus](downloadstatus-element.md) | 指定 Windows Media Player 顯示為連結的 URL，讓使用者能夠查看下載狀態。類型1：已忽略<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | 指定 Windows Media Player 顯示給使用者以識別線上商店的文字字串。類型1：必要<br/> 類型2音樂：必要<br/> 類型2商務：必要<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | 指定 HTMLView 網頁的基底 URL。類型1：選擇性<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                                                                                   |
| [影像](image-element.md)                   | 指定 Windows Media Player 顯示給使用者以代表線上商店的影像。類型1：必要<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                               |
| [資訊中心](infocenter-element.md)         | 指定當線上商店為使用中狀態時，Windows Media Player 顯示在 [資訊中心] 視圖功能 **中的網頁** URL。類型1：必要<br/> 類型2音樂：必要<br/> 類型2商務：已忽略<br/>                           |
| [安裝](install-element.md)               | 指定 Windows Media Player 安裝程式用來安裝預設線上存放區的值。類型1：必要<br/> 類型2音樂：選擇性<br/> 類型2商務：已忽略<br/>                                                                                          |
| [導航](navigate-element.md)             | 指定呼叫 **外部. NavigateTaskPaneURL** 所使用的基底 URL。類型1：選擇性<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | 表示 ServiceInfo.xml 檔的主要元素。類型1：必要<br/> 類型2音樂：必要<br/> 類型2商務：必要<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | 代表第一個線上商店工作窗格。類型1：必要<br/> 類型2音樂：必要<br/> 類型2商務：必要<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | 表示第二個線上商店工作窗格。類型1：已忽略<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | 代表第三個線上商店工作窗格。類型1：已忽略<br/> 類型2音樂：選擇性<br/> 類型2商務：選擇性<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





