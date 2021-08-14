---
title: 如何在新的目錄物件上設定安全描述項
description: 當您在 Active Directory Domain Services 中建立新的物件時，您可以明確建立安全描述項，然後將該安全描述項設定為物件的 nTSecurityDescriptor 屬性。
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- 物件 AD，如何在新的目錄物件上設定安全描述項
- 安全性描述項 AD，如何設定新的目錄物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d2009367c4d5604d359913b0154320332cd4be58e50dc5f065c574f8ea5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188109"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>如何在新的目錄物件上設定安全描述項

當您在 Active Directory Domain Services 中建立新的物件時，您可以明確建立安全描述項，然後將該安全描述項設定為物件的 **nTSecurityDescriptor** 屬性。 如需詳細資訊，請參閱 [建立新目錄物件的安全描述項](creating-a-security-descriptor-for-a-new-directory-object.md)。

Active Directory Domain Services 使用下列規則來設定新物件的安全描述項中的 DACL：

-   如果您在建立物件時明確指定安全描述項，系統會將父物件的任何可繼承 ace 合併到指定的 dacl，除非在安全描述項的控制位中設定 **SE \_ DACL \_ 保護** 的位。
-   如果您未指定安全描述項，系統會將父物件的任何可繼承 Ace，從物件類別的 **classSchema** 物件合併到預設 dacl，以建立物件的 dacl。
-   如果架構沒有預設的 DACL，則物件的 DACL 是建立者之主要或模擬權杖中的預設 DACL。
-   如果沒有指定、繼承或預設的 DACL，系統就會建立沒有 DACL 的物件，讓每個人都能完全存取該物件。

系統會使用類似的演算法來建立目錄服務物件的 SACL。

當您建立物件時，新物件安全描述項中的擁有者和主要群組會設定為您在 **nTSecurityDescriptor** 屬性中指定的值。 如果您未設定這些值，Active Directory Domain Services 會使用下表所列的規則來設定這些值。



| 規則          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 擁有者         | 預設安全描述項中的擁有者會從建立進程的主要或模擬權杖設定為預設擁有者 SID。 對於大部分的使用者而言，預設擁有者 SID 與識別使用者帳戶的 SID 相同。 請注意，對於屬於內建 administrators 群組成員的使用者，系統會自動將存取權杖中的預設擁有者 SID 設定為系統管理員群組;因此，由 administrators 群組成員建立的物件通常是由 administrators 群組所擁有。 若要取得或設定存取權杖中的預設擁有者，請使用 [**權杖 \_ 擁有**](/windows/desktop/api/winnt/ns-winnt-token_owner)者結構來呼叫 [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)或 [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation)函數。 |
| 主要群組 | 預設安全描述項中的主要群組會設定為來自建立者主要或模擬權杖的預設主要群組。 請注意，主要群組不會用於 Active Directory Domain Services 的內容中。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

如需 ACE 繼承的詳細資訊，請參閱系統 [管理的繼承與委派](inheritance-and-delegation-of-administration.md)。

如需有關架構中預設安全描述項的詳細資訊，請參閱 [預設安全描述項](default-security-descriptor.md)。

如需 **classSchema** 物件的詳細資訊，請參閱 [Active Directory 架構](active-directory-schema.md)。

 

 