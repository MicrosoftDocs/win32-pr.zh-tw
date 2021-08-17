---
title: " (淘汰的安全音訊路徑模型) "
description: " (淘汰的安全音訊路徑模型) "
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- 'Windows媒體格式 SDK、Microsoft 安全音訊路徑 (SAP) '
- '數位版權管理 (DRM) 、Microsoft 安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 、Microsoft 安全音訊路徑 (SAP) '
- Windows媒體格式 SDK， (SAP) 的安全音訊路徑
- '數位版權管理 (DRM) 的安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 的安全音訊路徑 (SAP) '
- Microsoft 安全音訊路徑 (SAP) ，模型
- " (SAP) 、模型的安全音訊路徑"
- SAP (安全音訊路徑) ，模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a381d29bcbf4b09ae989325cd5b35c332a6f316c1f932868437ac93a7854ab58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084281"
---
# <a name="the-secure-audio-path-model-deprecated"></a> (淘汰的安全音訊路徑模型) 

本頁面記載了在未來版本的 Windows 中，將會受到不同技術解決方案支援的功能。

microsoft 安全音訊路徑 (SAP) 是 microsoft Windows®我和 microsoft Windows XP 的一項功能。 只有透過安全音訊路徑來播放音訊檔案的需求，是在 DRM 授權中指定，並由 DRM 用戶端元件強制執行。 在一開始保護僅限 SAP 的檔案時，不會新增額外的加密。 在播放時，DRM 元件會自動新增 SAP 加密，就像播放時所牽涉到的所有軟體元件的驗證程式一樣。 因此，SAP 的運作方式對應用程式而言是完全透明的，這就是為什麼 Windows 媒體格式 SDK 沒有方法或屬性可啟用或停用 SAP。 如有需要，在建立受保護的檔案時，內容擁有者可以新增名為 "DRMHeader. SAPRequired" 的自訂標頭屬性，以指示授權伺服器將 SAP 需求新增至授權。 這種配置的執行是由內容擁有者和授權服務所組成。

在目前的 DRM 模型中，如果未套用 SAP，當播放受保護的數位音樂時，加密的內容會傳遞至 DRM 用戶端元件。 DRM 用戶端會驗證結合 Windows 媒體格式 SDK 的應用程式和 DRM 元件是否有效。 如果有效，DRM 用戶端會解密內容，並將內容傳送至應用程式，然後將它傳送至較低層的音訊元件。 此時，解密的音樂適用于使用者模式應用程式和外掛程式，以及可以攔截解密音訊位的核心模式驅動程式。

套用安全音訊路徑需求時，該內容不會由應用程式解密，而是會以加密狀態傳遞給較低層級的元件，而這些元件全都由 Microsoft 驗證為值得信任。 受信任的音訊元件是指除了其他特定的受信任元件之外，不會將音訊內容提供給任何系統元件。 如此一來，數位內容就會一直向下保護到驅動程式等級。

下圖顯示與安全音訊路徑模型比較的目前模型。

![安全音訊路徑模型的圖表](images/sap.png)

 

 




