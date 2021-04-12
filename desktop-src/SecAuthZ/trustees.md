---
description: 信任者是 (ACE) 套用存取控制專案的使用者帳戶、群組帳戶或登入會話。  (ACL) 的存取控制清單中的每個 ACE 都有一個安全識別碼 (SID) 可識別信任者。
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: 受託 人
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90084a0b6bfc7f63db12b7f47eba335adc87239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195413"
---
# <a name="trustees"></a>受託 人

信任者是 (ACE) 套用 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)的使用者帳戶、群組帳戶或 [*登入會話*](/windows/desktop/SecGloss/l-gly)。  (ACL) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 中的每個 ACE 都有一個 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 可識別信任者。

使用者帳戶包含使用者或程式（例如 Windows 服務）用來登入本機電腦的帳戶。

群組帳戶無法用來登入電腦，但它們在 Ace 中很有用，可允許或拒絕一或多個使用者帳戶的存取權限集。

識別目前登入會話的 [*登入 SID*](/windows/desktop/SecGloss/l-gly) ，只有在使用者登出後才允許或拒絕存取權限，是很有用的。

存取控制功能會使用 [**受信任**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) 結構來識別信任者。 **受信任** 結構可讓您使用名稱字串或 SID 來識別信任者。 如果您使用名稱，從 **受信任** 結構建立 ACE 的函式會執行配置 sid 緩衝區的工作，並查閱對應到帳戶名稱的 sid。 有兩個 helper 函式（ [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) 和 [**BuildTrusteeWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea)）會使用指定的 SID 或名稱來初始化 **信任者** 結構。 [**BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) 和 [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) 可讓您使用物件特有的 ACE 資訊來初始化 **信任者** 結構。 還有其他三個 helper 函式（ [**GetTrusteeForm**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma)、 [**GetTrusteeName**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)和 [**GetTrusteeType**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea)），會抓取 **受信任** 結構的各種成員的值。

[**受信任**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a)結構的 **ptstrName** 成員可以是物件的指標 [**\_ 、 \_ 名稱**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a)或 [**物件 \_ 以及 \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid)結構。 除了信任者名稱或 SID 之外，這些結構會指定 [物件特定 ACE](object-specific-aces.md) 的相關資訊。 這可讓 [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla)和 [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla)等函數將特定物件的 ACE 資訊儲存在 [**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)結構的 **受信任** 成員中。

 

 
