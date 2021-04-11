---
title: 關於服務發行
description: 服務是讓網路用戶端可以使用資料或作業的應用程式。 服務通常會實作為正式的 Microsoft Win32 型服務，但這不是必要的。
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34c1f0955f45f1bd4c689455ac03e79d987480
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931794"
---
# <a name="about-service-publication"></a>關於服務發行

服務是讓網路用戶端可以使用資料或作業的應用程式。 服務通常會實作為正式的 Microsoft Win32 型服務，但這不是必要的。

服務發行集是建立和維護指定服務的一或多個實例之相關資料的動作，讓網路用戶端可以尋找及使用服務。 在 Active Directory Domain Services 中發佈服務，可讓用戶端和系統管理員從以電腦為中心的分散式系統觀點移至以服務為中心的觀點。

**Microsoft Windows NT 3.51 和更新版本的作業系統：** 分散式系統是一組執行各種服務的電腦。 若要存取服務，應用程式需要有哪些電腦提供服務的相關資料。

**Windows 2000 Server、windows 2000 Advanced Server 和 Windows 2000 Datacenter Server：** 服務會使用 Active Directory Domain Services 物件來發佈其存在。 這些物件包含用戶端應用程式用來連接到服務實例的系結資訊。 若要存取服務，用戶端不需要知道特定電腦： Active Directory 伺服器中的物件包含這項資訊。 用戶端會向 Active Directory 伺服器查詢代表服務的物件 (稱為連接點物件) 並使用來自物件的系結資料來連接至服務。

下表顯示系結的範例。



| 服務      | 繫結                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 檔案服務 | 共用的 UNC 名稱。 例如 " \\ \\ MyServer \\ MyshareName"。                                                                                                                                                              |
| Web 服務  | Url。 例如 " https://www.fabrikam.com "。                                                                                                                                                                                 |
| RPC 服務  | 遠端程序呼叫 (RPC) 系結：用來連接到 RPC 伺服器的特殊編碼資訊。 RPC 系結可以使用 RPC Api 在字串之間來回轉換。 例如： "ncacn \_ ip \_ tcp:server]。 |



 

在分散式系統中，電腦是引擎，而有趣的實體就是可用的服務。 從使用者的觀點來看，提供特定服務的電腦身分識別並不重要。 存取服務本身是很重要的。

這也是服務管理的情況。 指定 DNS 區域的系統管理員對執行 DNS 服務的電腦不感興趣;系統管理員想要管理 DNS。 DNS 服務可能會有多個實例，其中一個是授權的。 支援 DNS 服務的電腦對 DNS 系統管理員而言並不重要。 重要的是如何將服務當作單一分散式資源來管理，而不是在不同電腦上執行的個別進程。

 

 




