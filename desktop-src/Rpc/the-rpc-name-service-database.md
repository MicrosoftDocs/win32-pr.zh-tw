---
title: RPC 名稱服務資料庫
description: 名稱服務是將名稱對應至物件的服務，通常會在資料庫中維護 (的名稱、物件) 組。
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- 遠端程序呼叫 RPC，描述，名稱服務資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462297"
---
# <a name="the-rpc-name-service-database"></a>RPC 名稱服務資料庫

名稱服務是將名稱對應至物件的服務，通常會在資料庫中維護 (的名稱、物件) 組。 一般而言，名稱是可讓使用者記住和使用的邏輯名稱。 例如，名稱服務可讓使用者使用邏輯名稱 "laserprinter"。 名稱服務會將此名稱對應至列印伺服器所使用的網路特定名稱。

為了使用簡單的說明，RPC 名稱服務會將名稱對應至系結控制碼，並在 RPC 名稱服務資料庫中維護 (名稱、系結控制碼) 對應。 RPC 名稱服務可讓用戶端應用程式使用邏輯名稱，而不是特定的通訊協定順序和網路位址。 使用邏輯名稱可讓網路系統管理員更輕鬆地安裝和設定您的分散式應用程式。

RPC 名稱服務資料庫專案具有下列其中一個屬性： **伺服器**、 **群組** 或 **設定檔**。 在 Microsoft 的執行中，專案只能有一個屬性，因此這些專案也稱為「伺服器專案」、「群組專案」和「設定檔專案」。

伺服器專案是由介面 Uuid、物件 Uuid (在伺服器執行多重進入點) 、網路位址、通訊協定順序，以及與已知端點相關聯的任何端點資訊時所需。 使用動態端點時，端點資訊會保存在端點對應資料庫中，而不是名稱服務資料庫中，而端點的解析就像任何其他動態端點一樣。 伺服器專案是由開頭為 "RpcNsBinding" 前置詞的函式所管理。

群組專案可以包含伺服器專案或其他群組專案。 群組專案是由開頭為 "RpcNsGroup" 前置詞的函式所管理。

設定檔專案可以包含設定檔、群組或伺服器專案。 設定檔專案是由開頭為 "RpcNsProfile" 前置詞的函式所管理。

本節提供下列主題中名稱服務資料庫的總覽：

-   [名稱服務應用程式指導方針](name-service-application-guidelines.md)
-   [名稱服務專案的總覽](an-overview-of-the-name-service-entry.md)
-   [名稱服務專案的準則](criteria-for-name-service-entries.md)
-   [名稱服務專案清除](name-service-entry-cleanup.md)
-   [查詢期間發生的情況](what-happens-during-a-query.md)
-   [使用 Microsoft 定位器](using-microsoft-locator.md)
-   [使用 Cell Directory 服務 (CD) ](using-the-cell-directory-service-cds-.md)
-   [名稱語法](name-syntax.md)

 

 




