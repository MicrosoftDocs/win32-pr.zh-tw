---
title: 對網路的最佳路由變更
description: 針對指定目的地網路的最佳路由，下列其中一個值的變更，會導致路由表管理員產生傳送至每個已註冊用戶端和轉寄站的通知訊息。
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fe96a0b339325c2290c346ba581d5b892db24d1cd972f7a83a0b2ec525eeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030358"
---
# <a name="changes-to-the-best-route-to-a-network"></a>對網路的最佳路由變更

**Windows Server 2003：** 此 api 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 新的應用程式應該使用路由表管理員第2版 API。

針對指定目的地網路的最佳路由，下列其中一個值的變更，會導致路由表管理員產生傳送至每個已註冊用戶端和轉寄站的通知訊息：

-   通訊協定識別碼
-   介面索引
-   下個躍點路由器的位址
-   包含路由計量的通訊協定系列特定資料

新增、更好的路由專案，或當目前的最佳路由專案已刪除或過時，並將另一個路由保留為新的最佳路由時，就會發生通訊協定識別碼、介面索引或下一個躍點路由器位址的變更。

 

 




