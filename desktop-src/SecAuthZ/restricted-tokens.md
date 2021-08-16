---
description: 受限的權杖是 CreateRestrictedToken 函式已修改的主要或模擬存取權杖。
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: 受限的權杖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f63402997d9e1304ca75ca117554ce52c3aa727f44b3b8316c28e1ecfcea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912006"
---
# <a name="restricted-tokens"></a>受限的權杖

受限的權杖是 [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken)函式已修改的 [*主要*](/windows/desktop/SecGloss/p-gly)或模擬 [*存取權杖*](/windows/desktop/SecGloss/a-gly)。 在受限權杖的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)中執行的 [*處理*](/windows/desktop/SecGloss/p-gly)程式或模擬執行緒，其存取安全物件或執行特殊許可權作業的能力會受到限制。 **CreateRestrictedToken** 函式可透過下列方式限制權杖：

-   移除權杖中的 [許可權](privileges.md) 。
-   將僅限拒絕的屬性套用至權杖中的 Sid，讓它們無法用來存取受保護的物件。 如需有關僅限拒絕屬性的詳細資訊，請參閱 [存取權杖中的 SID 屬性](sid-attributes-in-an-access-token.md)。
-   指定限制 Sid 的清單，這會限制對安全物件的存取。

當系統檢查安全物件的權杖存取權時，系統會使用限制 Sid 的清單。 當受限制的進程或執行緒嘗試存取安全物件時，系統會執行兩項存取檢查：一個使用權杖啟用的 Sid，另一個使用限制 Sid 的清單。 只有在這兩個存取檢查都允許要求的存取權限時，才會授與存取權。 如需有關存取檢查的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](how-dacls-control-access-to-an-object.md)。

在 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)函式的呼叫中，您可以使用受限制的 [*主要權杖*](/windows/desktop/SecGloss/p-gly)。 一般而言，呼叫 **CreateProcessAsUser** 的程式必須具有 SE \_ ASSIGNPRIMARYTOKEN \_ NAME 許可權，這通常只會由系統程式碼或 LocalSystem 帳戶中執行的服務所持有。 但是，如果 **CreateProcessAsUser** 呼叫指定受限制版本的呼叫端主要權杖，則不需要此許可權。 這可讓一般的應用程式建立受限的進程。

您也可以在 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)函數中使用受限制的主要或模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)。

若要判斷權杖是否有限制 Sid 的清單，請呼叫 [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) 函數。

> [!Note]  
> 使用受限制權杖的應用程式應該在預設桌面以外的桌上型電腦上執行受限制的應用程式。 這是為了避免受限制的應用程式（使用 **SendMessage** 或 **PostMessage**）在預設桌上型電腦上不受限制的應用程式所造成的攻擊。 如有必要，請在桌上型電腦之間切換，以進行應用程式用途。

 

 

 
