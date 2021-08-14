---
title: 如何在存取控制中使用安全性群組
description: 當使用者或群組基於安全性目的使用時， (SID) 的安全識別碼是使用者或安全性群組的物件識別碼。
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- 如何在存取控制中使用安全性群組
- 存取控制，使用的安全性群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8e14d4d8c371d07619d93f4a6d06318f91e7ec011a4c4fe6d436074ac8ff94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188129"
---
# <a name="how-security-groups-are-used-in-access-control"></a>如何在存取控制中使用安全性群組

當使用者或群組基於安全性目的使用時， (SID) 的安全識別碼是使用者或安全性群組的物件識別碼。 使用者或群組的名稱不會用來做為系統內的唯一識別碼。 SID 會儲存在 user objects 和 security group 物件的 **objectSid** 屬性中。 建立使用者或群組時，Active Directory 伺服器會產生 **objectSid** 。 系統可確保 Sid 在樹系中是唯一的。 請注意， **objectGuid** 是使用者、群組或任何其他目錄物件的唯一識別碼。 如果使用者或群組移至另一個網域，則 SID 會變更; **objectGuid** 維持不變。

當使用者或群組被授與資源的存取權，例如印表機或檔案共用時，會將使用者或群組的 SID 新增至存取控制專案 (ACE) 在資源的任意存取控制清單中定義授與的許可權 (DACL) 。 在 Active Directory Domain Services 中，每個物件都有 **nTSecurityDescriptor** 屬性，它會儲存 DACL，以定義該物件的存取權或該物件的屬性。 如需有關在 Active Directory Domain Services 中設定物件之存取控制的詳細資訊，請參閱 [控制 Active Directory Domain Services 中物件的存取權](controlling-access-to-objects-in-active-directory-domain-services.md)。

當使用者登入 Windows 2000 網域時，作業系統會產生存取權杖。 此存取權杖可用來決定使用者可以存取的資源。 使用者存取權杖包含下列資料：

-   使用者 SID。
-   使用者為其成員之所有全域和通用安全性群組的 Sid。
-   所有嵌套全域和通用安全性群組的 Sid。

代表此使用者執行的每個處理常式都有此存取權杖的複本。

當使用者嘗試存取電腦上的資源時，使用者用來存取資源的服務將會根據在使用者登入時建立的存取權杖來建立新的存取權杖來模擬使用者。 這個新的存取權杖也會包含下列 Sid：

-   目標網域中使用者所屬的所有網域本機群組的 Sid。
-   目的電腦上使用者所屬之所有電腦本機群組的 Sid。

服務會使用這個新的存取權杖來評估資源的存取權。 如果存取權杖中的 SID 出現在 DACL 中的任何 Ace 中，則服務會為使用者提供這些 Ace 中指定的許可權。

 

 




