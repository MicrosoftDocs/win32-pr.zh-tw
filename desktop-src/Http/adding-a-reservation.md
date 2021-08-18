---
title: 新增保留
description: 路由資料庫包含保留清單。
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac683c48748fa0e644f2f7569590b3783c521f1d10a1a5852a638a29731daf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014946"
---
# <a name="adding-a-reservation"></a>新增保留

路由資料庫包含保留清單。 保留清單包含允許存取命名空間的使用者，以及保留下所列每位使用者的存取層級。 新增或刪除保留時，會搜尋路由資料庫來決定存取權限。

除了檢查使用者識別碼之外，HTTP 伺服器 API 也會在安裝新的保留專案之前，先檢查現有保留中的衝突。

**若要加入新的保留**

1.  如果 UrlPrefix 中的埠號碼具有與 UrlPrefix 中配置不同的配置保留或註冊，則註冊會失敗。 在相同的埠上無法支援 HTTP 和 HTTPS。
2.  找出適當的註冊值區， (查看 [路由傳入要求](routing-incoming-requests.md) ] 區段) ，根據主機類型。 其餘步驟則相對於此值區。
3.  選取具有配置、主機和埠元件的保留專案，以符合保留的 UrlPrefix。 從這些專案中找出具有最長相符 *relativeUri* 的專案，該專案不等於保留 (中的 relativeUri，也就是 *父節點*) 。 如果專案存在，則根據指派給該專案的 ACL 來評估存取權限。
4.  如果找不到父節點，這是具有空白 relativeUri 或 *根保留* 的保留。 只有在以 LocalSystem 或系統管理員帳戶註冊呼叫端時，才授與存取權限。
5.  如果授與存取權限，請檢查是否有重複的保留。 如果存在具有相同配置、埠、主機和 relativeUri 的保留專案， \_ \_ 則會傳回錯誤已存在的程式碼。
    > [!Note]  
    > 若要更新現有的專案，請執行下列兩個步驟：刪除專案，並新增一個新專案。

     

如果上述步驟成功，則會在保留資料庫中輸入新的保留專案。

> [!Note]  
> 新的專案會以指定的 ACL 建立，且不會從 *父* 專案繼承 acl。

 

下列範例說明保留流程。

-   保留1： `https://+:80/vroot/subdir/` 使用者 A 和使用者 C 的系統管理員成功，並輸入 "+" bucket。
-   保留2： `https://adatum.com:80/vroot/` 使用者 B 的系統管理員成功，並輸入「明確主機」 bucket。
-   保留3：使用者 `https://adatum.com:80/vroot/subdir/otherdir/` C 的使用者 B 成功，因為保留2。
-   保留4： `https://+:80/vroot/subdir/otherdir/` 使用者 E 的使用者 A 成功，因為保留1。
-   保留5： `https://adatum.com:80/vroot/subdir/otherdir/` 使用者 E 的使用者 A 失敗。 因保留2而拒絕存取。
-   保留6： `https://+:80/vroot/subdir/` 使用者 A 的管理員失敗。 保留與保留1衝突。
-   保留7：使用者 a 的 `https://adatum.com:80/newroot/` 使用者 a 失敗。 因為 LocalSystem 或系統管理員的隱含根保留，所以拒絕存取 `https://adatum.com:80/` 。

保留可能會影響傳遞至先前註冊 UrlPrefix 之進程的要求中的一組 Url。 例如，請設想下列情況。

-   註冊： `https://adatum.com:80/vroot/` 使用者 A 的應用程式1。
-   的要求 `https://adatum.com:80/vroot/subdir/file.htm` 會傳遞至應用程式1。
-   保留： `https://+:80/vroot/subdir/` 適用于使用者 B。
-   的要求 `https://adatum.com:80/vroot/subdir/file.htm` 現在已遭到拒絕。
-   註冊： `https://adatum.com:80/vroot/subdir/` 依應用程式2為使用者 B。
-   的要求 `https://adatum.com:80/vroot/subdir/file.htm` 會傳遞至應用程式2。

 

 




