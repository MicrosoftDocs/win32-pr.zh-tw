---
description: 具有「SE TCB 名稱」許可權的伺服器（ \_ \_ 例如在 LocalSystem 帳戶中執行的 Windows 服務）可以呼叫 LogonUser 函式，在執行伺服器的電腦上驗證用戶端。
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: 用戶端登入會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1439b27637b0e46df3b468b42cb9c45ac8f759f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512421"
---
# <a name="client-logon-sessions"></a><span data-ttu-id="39c5d-103">用戶端登入會話</span><span class="sxs-lookup"><span data-stu-id="39c5d-103">Client Logon Sessions</span></span>

<span data-ttu-id="39c5d-104">具有「SE TCB 名稱」許可權的伺服器（ \_ \_ 例如在 [LocalSystem 帳戶](/windows/desktop/Services/localsystem-account)中執行的 Windows 服務）可以呼叫 [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) 函式，在執行伺服器的電腦上 [*驗證*](/windows/desktop/SecGloss/a-gly) 用戶端。</span><span class="sxs-lookup"><span data-stu-id="39c5d-104">A server with the SE\_TCB\_NAME privilege, such as a Windows service running in the [LocalSystem Account](/windows/desktop/Services/localsystem-account), can call the [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) function to [*authenticate*](/windows/desktop/SecGloss/a-gly) a client on the computer that the server is running on.</span></span> <span data-ttu-id="39c5d-105">**LogonUser** 函數會啟動新的登入 [*會話*](/windows/desktop/SecGloss/s-gly)，並傳回包含用戶端安全性資訊的 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="39c5d-105">The **LogonUser** function starts a new logon [*session*](/windows/desktop/SecGloss/s-gly) and returns a [*primary access token*](/windows/desktop/SecGloss/p-gly) that contains the client's security information.</span></span> <span data-ttu-id="39c5d-106">您可以在呼叫 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) 函式時，使用此主要權杖來模擬用戶端，或在呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函數來建立在用戶端的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 中執行的處理常式。</span><span class="sxs-lookup"><span data-stu-id="39c5d-106">You can use this primary token in calling the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function to impersonate the client or in calling the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to create a process that runs in the [*security context*](/windows/desktop/SecGloss/s-gly) of the client.</span></span>

<span data-ttu-id="39c5d-107">以這種方式驗證用戶端的優點是，模擬已驗證用戶端的伺服器，或在已驗證用戶端的內容中建立的 [*進程*](/windows/desktop/SecGloss/p-gly) ，可以連線至遠端網路資源作為用戶端。</span><span class="sxs-lookup"><span data-stu-id="39c5d-107">The advantage of authenticating the client in this way is that the server impersonating the authenticated client, or a [*process*](/windows/desktop/SecGloss/p-gly) created in the context of the authenticated client, can connect to remote network resources as the client.</span></span> <span data-ttu-id="39c5d-108">如果未執行此驗證，只有在已取得用戶端的帳戶名稱和密碼以傳遞至 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 函式時，伺服器才能連線到網路資源。</span><span class="sxs-lookup"><span data-stu-id="39c5d-108">If this authentication is not done, the server can connect to network resources only if it has acquired the client's account name and password to pass to the [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function.</span></span>

<span data-ttu-id="39c5d-109">以這種方式驗證用戶端的缺點，是伺服器必須取得用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly) ， (功能變數名稱、使用者名稱和密碼) 。</span><span class="sxs-lookup"><span data-stu-id="39c5d-109">The disadvantage of authenticating the client in this way is that the server must have acquired the client's [*credentials*](/windows/desktop/SecGloss/c-gly) (domain name, user name, and password).</span></span> <span data-ttu-id="39c5d-110">如果遠端用戶端將這些認證提供給伺服器，用戶端和伺服器就必須負責確保以安全的方式傳輸認證。</span><span class="sxs-lookup"><span data-stu-id="39c5d-110">If a remote client supplies these credentials to the server, it is the responsibility of the client and server to ensure that the credentials are transmitted in a secure manner.</span></span>

 

 
