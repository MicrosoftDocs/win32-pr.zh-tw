---
title: 服務工作窗格
description: 服務工作窗格
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player 線上商店、服務工作窗格
- 線上商店、服務工作窗格
- 輸入2個線上商店、服務工作窗格
- Windows Media Player 線上商店、工作窗格
- 線上商店、工作窗格
- 類型2線上商店、工作窗格
- Windows Media Player，服務工作窗格
- Windows Media Player，工作窗格
- 服務工作窗格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445e3fa5393dddb8e3dcc835317c8e5a284cb46f0a4a0e2b1f65fe2ea2d7b30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646508"
---
# <a name="service-task-panes"></a>服務工作窗格

在 Windows Media Player 10 中，線上商店提供者可以設定 Windows Media Player 顯示多達三個工作窗格，稱為「服務工作窗格」。 每個服務工作窗格會以可自訂的按鈕表示，Windows Media Player 在功能工作列右側顯示。

每個服務工作窗格都會裝載一個網頁，該網頁是特定線上商店功能的使用者介面。服務工作窗格的外觀是由 ServiceInfo XML 檔所定義。 在本檔中，服務工作窗格會以三個元素表示： **ServiceTask1**、 **ServiceTask2** 和 **ServiceTask3**。 這些服務工作窗格旨在提供下列各項：

-   音樂服務。
-   影片服務。
-   無線電服務。

您可以依您想要的任何順序將這些功能放在 Windows Media Player 中，但 **ServiceTask1** 必須是參與商務工作的主要工作窗格。

裝載在每個服務工作窗格中的網頁可以存取 **外部** 物件。 這個物件會提供方法、屬性和事件，以提供 Windows Media Player 中網頁的特殊功能。 例如，您可以使用 **外部** 的事件和屬性，讓網頁的外觀符合使用者為 Windows Media Player 選擇的色彩配置。

在 Windows Media Player 11 中，沒有任何服務工作窗格。 相反地，有一個 [ **線上商店** ] 索引標籤，可裝載作用中線上商店的主要網頁。 在 ServiceInfo 檔中，[ **線上商店** ] 索引標籤會以 **ServiceTask1** 元素表示; **ServiceTask2** 和 **ServiceTask3** 元素會被忽略。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Type 2 線上商店**](about-type-2-online-stores.md)
</dt> <dt>

[**類型2線上商店的外部物件**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**適用于 Type 2 線上商店的 ServiceInfo 檔**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




