---
description: 提供數個函式，可從存取控制清單取得存取控制資訊 (ACL) 。
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: 從 ACL 取得資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ef90d40058efd19790829f92c37a976359cbc61601d72fa2fee4cc4a93ec7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913670"
---
# <a name="getting-information-from-an-acl"></a>從 ACL 取得資訊

提供數個函式，可從 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 取得存取控制資訊 (ACL) 。 這些函式包括用來決定 ACL 授與或審核指定 [信任者](trustees.md)的存取權限。 其他函式可讓您將 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 的相關資訊解壓縮 (ace) 在 ACL 中。

[**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla)函式會取得 [**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)結構的陣列，以描述 ACL 中的 ace。 將 ACE 資訊從某個 ACL 複製到另一個 ACL 時，這會很有用。 例如，若要在某個 ACL 中取得 Ace 的相關資訊，您可以在呼叫 [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla)函式的呼叫中傳遞傳回的 **明確 \_ 存取** 結構，以在新的 Acl 中建立對等 ace，來呼叫 **GetExplicitEntriesFromAcl** 。

[**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla)函式可讓您判斷 DACL 授與給指定之信任者的有效存取權限。 信任者的有效存取權限是 DACL 授與信任者的存取權限，或信任者為其成員的任何群組。 **GetEffectiveRightsFromAcl** 會在指定的 DACL 中檢查所有允許存取和拒絕存取的 ace。

**使用下列步驟來判斷信任者對物件的存取權限**

1.  呼叫 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) 或 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 函式，以取得物件 DACL 的指標。
2.  呼叫 [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) 函式，以取得 DACL 授與給指定之信任者的存取權限。

[**GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla)函式可讓您檢查 SACL，以判斷指定信任者或受信任者為其成員之任何群組的已審核存取權限。 已審核的許可權會指出導致系統在安全性事件記錄檔中產生審核記錄的存取嘗試類型。 此函式會傳回兩個 [*存取遮罩*](/windows/desktop/SecGloss/a-gly)：一個包含針對失敗存取嘗試所監視的存取權限，另一個則包含針對成功存取所監視的存取權。 **GetAuditedPermissionsFromAcl** 會檢查 SACL 中的所有系統-audit ace。

 

 
