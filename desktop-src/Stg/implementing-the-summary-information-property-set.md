---
title: 執行摘要資訊屬性集
description: 針對結構化的儲存體執行摘要資訊屬性集時，有一些指導方針。
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- 執行摘要資訊屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe847d9a7353074727c94250d0f1ec1fec2194b5b7d250099464a86667861f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796908"
---
# <a name="implementing-the-summary-information-property-set"></a>執行摘要資訊屬性集

針對結構化的儲存體執行摘要資訊屬性集時，有一些指導方針。

以下是執行 [摘要資訊屬性集](the-summary-information-property-set.md)的指導方針：

-   **PID \_範本** 指的是包含格式和樣式資訊的外部檔。 範本所在的處理常式是由實作為定義。
-   **PID \_LASTAUTHOR** 是應用程式儲存在使用者資訊中的名稱。 例如，Mary 在電腦上建立一份檔，並將它提供給 John，然後修改並儲存它。 Mary 是作者，John 是最後一個儲存的值。
-   **PID \_REVNUMBER** 是在這份檔上呼叫檔案/儲存命令的次數。
-   每個日期/時間值都必須以全球協調時間儲存 (UTC) 。
-   **PID \_建立 \_ DTM** 是唯讀屬性;這個屬性應該在建立檔時設定，但之後不應變更。
-   針對 **PID \_ 縮圖**，應用程式應該以 **CF \_ .dib** 或 **cf \_ METAFILEPICT** 格式儲存資料。 **CF \_** 建議使用 METAFILEPICT。
-   **PID \_安全性** 是建議的檔安全性層級。 藉由記下檔的安全性層級，檔的建立者以外的應用程式就可以將其使用者介面調整為屬性。 應用程式不應該顯示任何有關受密碼保護之檔的資訊，或是啟用 Read-Only 或鎖定註釋檔的強制修改。 如果使用者嘗試修改屬性，應用程式應該向使用者警告 Read-Only 建議的狀態。



| 安全性層級         | 值 |
|------------------------|-------|
| 無                   | 0     |
| 密碼保護     | 1     |
| 建議使用唯讀  | 2     |
| 強制唯讀     | 4     |
| 鎖定批註 | 8     |



 

 

 




