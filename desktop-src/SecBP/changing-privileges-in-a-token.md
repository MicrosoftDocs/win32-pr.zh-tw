---
description: 說明如何使用 AdjustTokenPrivileges 和 CreateRestrictedToken 函數來變更權杖中的許可權。
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: 變更權杖中的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c511ca66c5d4739057f5ea75cae589ee97e849f659002a612e7d22fd6be8eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622748"
---
# <a name="changing-privileges-in-a-token"></a>變更權杖中的許可權

您可以透過兩種方式來變更主要或模擬權杖中的許可權：

-   使用 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函數來啟用或停用許可權。
-   使用 [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) 函數來限制或移除許可權。

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 無法新增或移除權杖中的許可權。 它只能啟用目前停用的現有許可權，或停用目前已啟用的現有許可權。 如需範例，請參閱 [啟用和停用 c + + 中的許可權](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)。

若要將許可權指派給使用者帳戶，請參閱將 [許可權指派給帳戶](assigning-privileges-to-an-account.md)。

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) 具有更廣泛的功能，如下所示：

-   移除許可權。 請注意，移除許可權與停用許可權不同。 從權杖移除許可權之後，就無法將它放回。
-   將拒絕屬性附加至權杖中的 Sid。 這會造成不允許特定群組或帳戶的影響，例如拒絕 Everyone 群組刪除特定檔案的存取權。 如需限制 Sid 的詳細資訊，請參閱 [存取權杖中的 SID 屬性](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token)。
-   指定限制權杖中 Sid 的清單。 如需限制 Sid 的詳細資訊，請參閱 [限制的權杖](/windows/desktop/SecAuthZ/restricted-tokens)。

 

 
