---
description: 受保護的伺服器應用程式必須先檢查用戶端存取許可權，然後才允許用戶端存取受保護的私用物件。
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: 檢查私用物件的存取權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f31f8ed05c16eed09cdd45da78f8fe58ecf41e283f6e6c37e7bc0480e63422d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783172"
---
# <a name="checking-access-to-private-objects"></a>檢查私用物件的存取權

受保護的伺服器應用程式必須先檢查用戶端的存取權限，然後才允許用戶端存取受保護的私用物件。 若要這樣做，伺服器會將模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)、安全描述項，以及一組要求的存取權限傳遞給 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)。 在 [*安全描述項的*](/windows/desktop/SecGloss/s-gly)DACL 中， (ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)會指定對各種受信者允許或拒絕的存取權限。 **AccessCheck** 函式會比較每個 ACE 中的信任者與模擬權杖中識別的信任者。 如需用來授與或拒絕存取權之演算法的描述，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。

[**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)函式會執行類似的存取檢查。 此外，它會根據安全描述項中的 SACL，在安全性事件記錄檔中產生審核記錄。

[**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)和 [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)函式類似于 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)和 [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) ，只不過它們可讓您檢查物件的子物件（例如屬性集或屬性）的存取權。 [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist)和 [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)函式也類似于 **AccessCheck** ，不同之處在于它們會在物件的屬性和屬性集階層中提供每個子物件的存取檢查結果。 這些函式會使用 [**物件 \_ 類型 \_ 清單**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) 結構來描述已檢查存取的物件階層。 產生 audit 訊息的函式會使用 [**audit \_ 事件 \_ 類型**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) 列舉型別，來指出正在檢查的物件是否為目錄服務物件。 如需物件及其子物件階層的詳細資訊，請參閱 [ace 來控制物件屬性的存取](aces-to-control-access-to-an-object-s-properties.md)。

傳遞給 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) 和 [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) 函數的要求存取權限不能包含任何 [一般存取權限](generic-access-rights.md)。 伺服器可以使用 [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) 函式，根據泛型對應結構中指定的對應，將任何泛型存取權限轉換為對應的特定和 [**標準 \_**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) 許可權。

[**AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted)和 [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted)函式會比較所要求的 [*存取遮罩*](/windows/desktop/SecGloss/a-gly)與授與的存取遮罩。

如需使用 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) 函式的範例程式碼，請參閱使用 [c + + 的 Acl 來驗證用戶端存取](verifying-client-access-with-acls-in-c--.md)。

[**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)函式會以允許自動傳播可繼承 ace 的格式，建立並傳回安全描述項。 此安全描述項包含目前安全描述項中的所有 Ace （繼承和 noninherited），而且是 [*自我相關*](/windows/desktop/SecGloss/s-gly) 的格式。 **ConvertToAutoInheritPrivateObjectSecurity** 函式會將目前安全描述項中的所有 ace 與父安全描述項中的所有 ace 進行比較，以決定是否要繼承或 noninherited ace。 兩組 Ace 之間可能不會有一對一的對應關係。 例如，允許讀取/寫入權限的 ACE 可以等同于兩個 Ace：允許讀取權限的 ace，以及允許寫入權限的 ACE。 當目前的安全描述項是父系時，可能無法提供父安全描述項。

 

 
