---
description: 說明存取控制模型的各個部分。
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: 存取控制模型的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bffdbf6542a9e29360437c50f47495d83467334e09c7aa55e8a136a8fc7556d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785668"
---
# <a name="parts-of-the-access-control-model"></a>存取控制模型的元件

存取控制模型有兩個基本部分：

-   [存取權杖](access-tokens.md)，其中包含已登入使用者的相關資訊
-   [安全描述項](security-descriptors.md)，其中包含保護安全[物件](securable-objects.md)的安全性資訊

當使用者登入時，系統會 [*驗證*](/windows/desktop/SecGloss/a-gly) 使用者的帳戶名稱和密碼。 如果登入成功，系統會建立存取權杖。 代表此使用者執行的每個 [*進程*](/windows/desktop/SecGloss/p-gly) 都會有此存取權杖的複本。 存取權杖包含 [安全識別碼](security-identifiers.md) ，可識別使用者的帳戶，以及使用者所屬的任何群組帳戶。 此權杖也包含使用者或使用者群組所持有的 [許可權](privileges.md) 清單。 當進程嘗試存取安全物件或執行需要許可權的系統管理工作時，系統會使用此權杖來識別相關聯的使用者。

建立安全物件時，系統會為它指派一個 [*安全描述項*](/windows/desktop/SecGloss/s-gly) ，其中包含其建立者所指定的安全性資訊，或者，如果未指定，則為預設的安全性資訊。 應用程式可以使用函式來取得和設定現有物件的安全性資訊。

安全描述項會識別物件的擁有者，也可以包含下列 [存取控制清單](access-control-lists.md)：

-    (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) ，識別允許或拒絕存取物件的使用者和群組
-   [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) ，可 [控制系統如何](audit-generation.md)嘗試存取物件。

ACL 包含 (Ace) 的 [存取控制專案](access-control-entries.md) 清單。 每個 ACE 都會指定一組 [存取權限](access-rights-and-access-masks.md) ，而且會包含 SID 來識別允許、拒絕或審核許可權的 [信任者](trustees.md) 。 信任者可以是使用者帳戶、群組帳戶或登入 [*會話*](/windows/desktop/SecGloss/l-gly)。

使用函式來操作安全描述項、Sid 和 Acl 的內容，而不是直接存取它們。 這有助於確保這些結構的語法正確，並防止安全性系統的未來增強功能破壞現有的程式碼。

下列主題提供存取控制模型各部分的相關資訊：

-   [存取權杖](access-tokens.md)
-   [安全性描述項](security-descriptors.md)
-   [存取控制清單](access-control-lists.md)
-   [存取控制專案](access-control-entries.md)
-   [存取權限和存取遮罩](access-rights-and-access-masks.md)
-   [AccessCheck 的運作方式](how-dacls-control-access-to-an-object.md)
-   [集中式授權原則](centralized-authorization-policy.md)
-   [安全識別碼](security-identifiers.md)

 

 
