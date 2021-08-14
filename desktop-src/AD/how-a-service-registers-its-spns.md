---
title: 服務如何註冊其 Spn
description: 必須先在服務實例將用來登入的使用者或電腦帳戶上註冊 SPN，用戶端才能使用 SPN 來驗證服務的實例。
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- 服務如何註冊其 Spn AD
- 服務主體名稱 AD，服務如何註冊其 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ebf33ed0f28dff3acffdcdc96a880c21ec532ff677801dd52ac1801f44c80e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188581"
---
# <a name="how-a-service-registers-its-spns"></a>服務如何註冊其 Spn

必須先在服務實例將用來登入的使用者或電腦帳戶上註冊 SPN，用戶端才能使用 SPN 來驗證服務的實例。 通常，SPN 註冊是由以網域系統管理員許可權執行的服務安裝程式所完成。

在主機電腦上安裝服務實例的服務安裝程式通常會執行下列程式。

**註冊服務實例的 Spn**

1.  呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函數，為服務實例建立一個或多個唯一的 spn。 如需詳細資訊，請參閱 [唯一 spn 的名稱格式](name-formats-for-unique-spns.md)。
2.  呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函數，以在服務的登入帳戶上註冊名稱。

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 會將 spn 註冊為目錄中使用者或電腦帳戶物件的屬性。 **使用者** 和 **電腦** 物件具有 **servicePrincipalName** 屬性，它是用來儲存所有與使用者或電腦帳戶相關聯之 spn 的多重值屬性。 如果服務是在使用者帳戶下執行，則 Spn 會儲存在該帳戶的 **servicePrincipalName** 屬性中。 如果服務是在 LocalSystem 帳戶中執行，則 Spn 會儲存在服務主機電腦帳戶的 **servicePrincipalName** 屬性中。 **DsWriteAccountSpn** 呼叫端必須指定用來儲存 spn 之帳戶物件的分辨名稱。

為了確保登錄的 Spn 是安全的，無法直接寫入 **servicePrincipalName** 屬性;它只能透過呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)寫入。 呼叫端必須具有目標帳戶之 **servicePrincipalName** 屬性的寫入權限。 一般而言，寫入權限預設只會授與網域系統管理員。 不過，有一個特殊情況，即系統允許在 LocalSystem 帳戶下執行的服務，在服務主機的電腦帳戶上註冊自己的 Spn。 在此情況下，所寫入的 SPN 必須有 " <service class> / <host> " 和 "host" 格式，而且 &lt; &gt; 必須是本機電腦的 DNS 名稱。

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 也可以移除帳戶中的 spn。 Operation 參數會指出是否要將 Spn 新增至帳戶、從帳戶移除，或用來完全取代帳戶的所有目前 Spn。 卸載服務實例時，請移除任何針對該實例註冊的 Spn。

如需註冊或取消註冊服務 Spn 的詳細資訊和程式碼範例，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。

使用簡單 SPN 格式 "" 的主機服務 <service class> / <host> ，可以選擇使用 [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)函式，這兩個方法都會建立並註冊服務實例的 spn。 **DsServerRegisterSpn** 是呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 和 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)的 helper 函數。

如需詳細資訊，請參閱 [服務登入帳戶](service-logon-accounts.md)。

 

 




