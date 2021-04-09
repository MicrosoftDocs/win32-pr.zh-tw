---
description: 在用戶端/伺服器應用程式模型中，用戶端是代表需要完成某些工作之使用者的程式。
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: 基本驗證概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114313"
---
# <a name="basic-authentication-concepts"></a>基本驗證概念

在用戶端/伺服器應用程式模型中，用戶端是代表需要完成某些工作之使用者的程式。 這可能是開啟和使用檔案、存取信箱、查詢資料庫或列印檔案。 伺服器是提供服務給用戶端的程式，例如檔案儲存體、郵件處理、查詢處理和列印幕後處理。 用戶端會起始動作，而伺服器會回應。 一般來說，伺服器會在通訊埠上接聽，等候用戶端連接並要求服務。

在 Kerberos 通訊協定模型中，每個用戶端/伺服器連接一開始都會進行驗證。 用戶端和伺服器會依次逐步執行一系列動作，向連接的兩端驗證對端是真的。 如果驗證成功，工作階段的安裝隨即完成且建立安全的用戶端/伺服器工作階段。

Kerberos 通訊協定利用：

-   [金鑰驗證](key-authentication.md)
-   [驗證器訊息](authenticator-messages.md)
-   [金鑰散發](key-distribution.md)
-   [會話票證](session-tickets.md)
-   [票證授權票證](ticket-granting-tickets.md)

 

 



