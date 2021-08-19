---
description: 具有 SE \_ TCB 名稱許可權的伺服器（ \_ 例如在 LocalSystem 帳戶中執行的 Windows 服務）可以呼叫 LogonUser 函式，在執行伺服器的電腦上驗證用戶端。
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: 用戶端登入會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baafdc46800cc5b334a5496be5502b97e18d4702bdf9b839d8431a92110c3d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783020"
---
# <a name="client-logon-sessions"></a>用戶端登入會話

具有 SE \_ TCB 名稱許可權的伺服器（ \_ 例如在 [LocalSystem 帳戶](/windows/desktop/Services/localsystem-account)中執行的 Windows 服務）可以呼叫 [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera)函式，在執行伺服器的電腦上 [*驗證*](/windows/desktop/SecGloss/a-gly)用戶端。 **LogonUser** 函數會啟動新的登入 [*會話*](/windows/desktop/SecGloss/s-gly)，並傳回包含用戶端安全性資訊的 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly)。 您可以在呼叫 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) 函式時，使用此主要權杖來模擬用戶端，或在呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函數來建立在用戶端的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 中執行的處理常式。

以這種方式驗證用戶端的優點是，模擬已驗證用戶端的伺服器，或在已驗證用戶端的內容中建立的 [*進程*](/windows/desktop/SecGloss/p-gly) ，可以連線至遠端網路資源作為用戶端。 如果未執行此驗證，只有在已取得用戶端的帳戶名稱和密碼以傳遞至 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 函式時，伺服器才能連線到網路資源。

以這種方式驗證用戶端的缺點，是伺服器必須取得用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly) ， (功能變數名稱、使用者名稱和密碼) 。 如果遠端用戶端將這些認證提供給伺服器，用戶端和伺服器就必須負責確保以安全的方式傳輸認證。

 

 
