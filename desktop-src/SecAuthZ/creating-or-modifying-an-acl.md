---
description: Windows 支援一組函式，這些函式會建立存取控制清單 (acl) 或修改現有 acl 中 (ace) 的存取控制專案。
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: 建立或修改 ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120b445d37f8c4b82c2b0b2a775a06d68faa46ab5752cc25e913d43676e9a72e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782163"
---
# <a name="creating-or-modifying-an-acl"></a>建立或修改 ACL

Windows 支援一組函式，這些函式會建立 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) (acl) 或修改現有 acl 中 (ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)。

[**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla)函式會建立新的 ACL。 **SetEntriesInAcl** 可以為 ACL 指定一組全新的 ace，也可以使用現有 ACL 的 ace 來合併一或多個新的 ace。 **SetEntriesInAcl** 函數會使用 [**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)結構的陣列來指定新 ace 的資訊。 每個 **明確的 \_ 存取** 結構都會包含描述單一 ACE 的資訊。 這項資訊包括存取權限、ACE 類型、控制 ACE 繼承的旗標，以及識別信任者的 [**信任**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) 結構。

**將新的 ACE 新增至現有的 ACL**

1.  使用 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) 或 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 函數，從物件的 [*安全描述項*](/windows/desktop/SecGloss/s-gly)取得現有的 DACL 或 SACL。
2.  針對每個新的 ACE 呼叫 [**BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) 函式，以使用描述 ACE 的資訊來填滿 [**明確的 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) 結構。
3.  呼叫 [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla)，為新的 ace 指定現有的 ACL 和 [**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) 結構的陣列。 **SetEntriesInAcl** 函式會配置並初始化 ACL 及其 ace。
4.  呼叫 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) 或 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 函數，將新的 ACL 附加至物件的安全描述項。

如果呼叫端指定現有的 ACL， [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) 會將新的 ace 資訊與 acl 中的現有 ace 合併。 例如，假設現有的 ACL 會授與指定之受信任者的存取權，而 [**明確的 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) 結構會拒絕對相同信任者的存取。 在此情況下， **SetEntriesInAcl** 會為信任者新增拒絕存取拒絕的 ace，並刪除或修改受信任者的現有存取權允許 ace。

如需將新的 ACE 合併至現有 ACL 的範例程式碼，請參閱 [使用 c + + 修改物件的 acl](modifying-the-acls-of-an-object-in-c--.md)。

 

 
