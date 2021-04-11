---
description: 若要建立安全描述項，受保護的伺服器可以使用應用程式用來建立安全物件安全描述項的相同程式。
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: 私用物件的安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c40dc5c4e9f0a3d0e641874153d2862d038a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943561"
---
# <a name="security-descriptors-for-private-objects"></a>私用物件的安全描述項

若要建立 [*安全描述項*](/windows/desktop/SecGloss/s-gly)，受保護的伺服器可以使用應用程式用來建立安全物件安全描述項的相同程式。 如需範例程式碼，請參閱 [在 c + + 中建立新物件的安全描述項](creating-a-security-descriptor-for-a-new-object-in-c--.md)。 或者，受保護的伺服器應用程式可以呼叫 [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) 函式來進行此作業。 如果將現有的 [*自我相關安全描述項*](/windows/desktop/SecGloss/s-gly) 指標提供給 **BuildSecurityDescriptor**，它會建立新的安全描述項，其中包含來自該安全描述項的資訊，並與新的存取控制資訊合併在函式呼叫中做為參數傳遞。 傳遞給函式的信任結構可以選擇性地指定擁有 [**者**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) 和群組。 **BuildSecurityDescriptor** 所建立的安全描述項會採用 *自我對應* 的格式。

此外，Windows API 還提供一組函式，用來合併用戶端安全性資訊，以及繼承自父物件之安全描述項或預設安全描述項的資訊。 [**CreatePrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity)、 [**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)、 [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)和 [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity)函數可讓您從 [*存取權杖*](/windows/desktop/SecGloss/a-gly)取出預設資訊、支援繼承，以及操作安全描述項的特定部分。 當用戶端在安全物件的階層中建立私用物件時，這會很有用。 例如，您可以使用 **CreatePrivateObjectSecurity** 函式來建立安全描述項，其中包含用戶端所指定的 ace、繼承自父物件的 ace，以及建立用戶端存取權杖的預設擁有者。 雖然 [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) 會從傳遞至函式呼叫的存取控制資訊或從現有的安全描述項建立安全描述項，但 **CreatePrivateObjectSecurity** 只會根據現有安全描述項中的資訊來建立安全描述項。

[**LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) 函式會從現有的 [*自我相關安全描述項*](/windows/desktop/SecGloss/s-gly)取得安全描述項資訊。 這項資訊包括擁有者和群組規格、SACL 或 DACL 中的 Ace 數目，以及 SACL 或 DACL 中的 Ace 清單。

 

 
