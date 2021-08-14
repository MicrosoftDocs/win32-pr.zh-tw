---
description: 物件擁有者隱含擁有 \_ 物件的寫入 DAC 存取權。 這表示擁有者可以在 (DACL) 的情況下，修改物件的任意存取控制清單，因此可以控制物件的存取權。
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: 新物件的擁有者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b787603e9225548e4213259866a6658d637bb85e46588f7260322fc2646128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912124"
---
# <a name="owner-of-a-new-object"></a>新物件的擁有者

物件的擁有者隱含擁有 \_ 物件的寫入 DAC 存取權。 這表示擁有者可以修改物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，因此可以控制物件的存取權。

新物件的擁有者是預設的擁有者 [*安全識別碼*](/windows/desktop/SecGloss/s-gly)， (SID) 來自建立 [*進程*](/windows/desktop/SecGloss/p-gly)的 [*主要*](/windows/desktop/SecGloss/p-gly)或模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)。 若要取得或設定 [*存取權杖*](/windows/desktop/SecGloss/a-gly)中的預設擁有者，請使用 [**權杖 \_ 擁有**](/windows/desktop/api/Winnt/ns-winnt-token_owner)者結構來呼叫 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)或 [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)函數。 系統不允許您將權杖的預設擁有者設定為不正確 SID，例如另一個使用者帳戶的 SID。

啟用「SE \_ 取得擁有權」許可權的進程， \_ 可以將自己設定為物件的擁有者。 \_啟用 SE RESTORE \_ NAME 許可權或具有物件寫入擁有者存取權的進程， \_ 可以將任何有效的使用者或群組 SID 設定為物件的擁有者。

 

 
