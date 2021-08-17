---
description: 存取控制清單 (ACL) 是存取控制項目 (ACE) 的清單。
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: 存取控制清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7021767830dead84f2ea965c46ca205257a2f18443f352ec85becc0139e30e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785658"
---
# <a name="access-control-lists"></a>存取控制清單

[*存取控制清單*](/windows/desktop/SecGloss/a-gly) (ACL) 是 (ACE) 的 [存取控制專案](access-control-entries.md)清單。 ACL 中的每個 ACE 可識別[「信任者」](trustees.md)(Trustee)，並指定該信任者所允許、拒絕或稽核的[「存取權限」](access-rights-and-access-masks.md)(Access Right)。 安全[物件](securable-objects.md)的[安全描述項](security-descriptors.md)可包含兩種類型的 ACL： DACL 和 SACL。

 (DACL 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)) 識別允許或拒絕存取安全物件的信任者。 當 [*進程*](/windows/desktop/SecGloss/p-gly) 嘗試存取安全物件時，系統會檢查物件 DACL 中的 ace，以判斷是否要授與存取權。 如果物件沒有 DACL，系統會將完整存取權授與所有人。 如果物件的 DACL 沒有 Ace，系統就會拒絕所有存取物件的嘗試，因為 DACL 不允許任何存取權限。 系統會依序檢查 Ace，直到找到允許所有要求之存取權限的一或多個 Ace，或直到任何要求的存取權限遭到拒絕為止。 如需詳細資訊，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。 如需有關如何正確建立 DACL 的詳細資訊，請參閱 [建立 dacl](/windows/desktop/SecBP/creating-a-dacl)。

[*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 可讓系統管理員記錄存取安全物件的嘗試。 每個 ACE 都會指定由指定的受信任者所嘗試的存取類型，讓系統在安全性事件記錄檔中產生記錄。 SACL 中的 ACE 可以在存取嘗試失敗、成功時或兩者都產生審核記錄。 如需 Sacl 的詳細資訊，請參閱「立即 [產生](audit-generation.md) 和 [SACL」存取權限](sacl-access-right.md)。

請勿嘗試直接使用 ACL 的內容。 若要確定 Acl 的語義正確，請使用適當的函式來建立和操作 Acl。 如需詳細資訊，請參閱 [從 Acl 取得資訊](getting-information-from-an-acl.md) 和 [建立或修改 acl](creating-or-modifying-an-acl.md)。

Acl 也提供 Microsoft Active Directory Directory 服務物件的存取控制。 Active Directory 服務介面 (ADSI) 包含可建立和修改這些 Acl 內容的常式。 如需詳細資訊，請參閱 [控制 Active Directory 物件的存取權](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services)。

 

 
