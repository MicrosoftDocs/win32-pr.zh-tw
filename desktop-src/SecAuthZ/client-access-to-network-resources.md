---
description: 說明用來存取網路資源的策略。
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: 用戶端對網路資源的存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0873a10c708f9aab2e9c250375a63e8a2167873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977184"
---
# <a name="client-access-to-network-resources"></a><span data-ttu-id="4f27f-103">用戶端對網路資源的存取</span><span class="sxs-lookup"><span data-stu-id="4f27f-103">Client Access to Network Resources</span></span>

<span data-ttu-id="4f27f-104">伺服器可以使用下列策略來存取網路資源：</span><span class="sxs-lookup"><span data-stu-id="4f27f-104">A server can use the following strategies to access network resources:</span></span>

-   <span data-ttu-id="4f27f-105">如果伺服器具有用戶端的帳戶名稱和密碼，則可以使用用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly)來呼叫 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ，以將本機磁碟機號對應到網路共用。</span><span class="sxs-lookup"><span data-stu-id="4f27f-105">If the server has the account name and password of a client, it can call [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) with the client's [*credentials*](/windows/desktop/SecGloss/c-gly) to map a local drive letter to a network share.</span></span>
-   <span data-ttu-id="4f27f-106">使用用戶端認證呼叫 [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) 之後，伺服器可以呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式來 [建立用戶端的進程](processes-in-the-client-security-context.md)。</span><span class="sxs-lookup"><span data-stu-id="4f27f-106">After calling [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) with client credentials, the server can call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to [create a process for the client](processes-in-the-client-security-context.md).</span></span> <span data-ttu-id="4f27f-107">這個新的用戶端進程可以使用用戶端的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)來存取網路資源。</span><span class="sxs-lookup"><span data-stu-id="4f27f-107">This new client process can access network resources using the client's [*security context*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="4f27f-108">例如，程式可以呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數來開啟遠端電腦上的檔案。</span><span class="sxs-lookup"><span data-stu-id="4f27f-108">For example, the process can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a file on a remote computer.</span></span> <span data-ttu-id="4f27f-109">系統會使用用戶端的 [*主要權杖*](/windows/desktop/SecGloss/p-gly) 來檢查用戶端進程的存取嘗試。</span><span class="sxs-lookup"><span data-stu-id="4f27f-109">The system uses the client's [*primary token*](/windows/desktop/SecGloss/p-gly) to check access attempts by the client process.</span></span>
-   <span data-ttu-id="4f27f-110">伺服器可以使用 null 認證來呼叫 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ，以建立具有伺服器存取權或預設連線的網路資源連接。</span><span class="sxs-lookup"><span data-stu-id="4f27f-110">A server can call [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) with null credentials to establish either a connection to a network resource with server access or a default connection.</span></span> <span data-ttu-id="4f27f-111">如果伺服器是以 LocalSystem 帳戶執行，則會向網域伺服器的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 下的網路資源進行驗證。</span><span class="sxs-lookup"><span data-stu-id="4f27f-111">If the server is running as the LocalSystem account, it authenticates to the network resource under the [*security context*](/windows/desktop/SecGloss/s-gly) of the domain server.</span></span> <span data-ttu-id="4f27f-112">如果伺服器是在服務帳戶下執行，則會以該帳戶進行驗證。</span><span class="sxs-lookup"><span data-stu-id="4f27f-112">If the server is running under a service account, it authenticates as that account.</span></span> <span data-ttu-id="4f27f-113">如需詳細資訊，請參閱 [LocalSystem 帳戶](/windows/desktop/Services/localsystem-account)。</span><span class="sxs-lookup"><span data-stu-id="4f27f-113">For more information, see the [LocalSystem Account](/windows/desktop/Services/localsystem-account).</span></span>

<span data-ttu-id="4f27f-114">如需保護密碼的相關資訊，請參閱 [處理密碼](/windows/desktop/SecBP/handling-passwords)。</span><span class="sxs-lookup"><span data-stu-id="4f27f-114">For information about protecting passwords, see [Handling Passwords](/windows/desktop/SecBP/handling-passwords).</span></span> <span data-ttu-id="4f27f-115">如需取得認證的詳細資訊，請參閱 [要求使用者提供認證](/windows/desktop/SecBP/asking-the-user-for-credentials)。</span><span class="sxs-lookup"><span data-stu-id="4f27f-115">For information about acquiring credentials, see [Asking the User for Credentials](/windows/desktop/SecBP/asking-the-user-for-credentials).</span></span>

 

 
