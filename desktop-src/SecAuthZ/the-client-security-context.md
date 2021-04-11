---
description: 如同所有進程，受保護的伺服器具有主要存取權杖，可描述其安全性內容。
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: 用戶端安全性內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d3b4522aa90ade89e2130742346956a396f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943559"
---
# <a name="the-client-security-context"></a><span data-ttu-id="9a5ba-103">用戶端安全性內容</span><span class="sxs-lookup"><span data-stu-id="9a5ba-103">The Client Security Context</span></span>

<span data-ttu-id="9a5ba-104">如同所有 [*進程*](/windows/desktop/SecGloss/p-gly)，受保護的伺服器具有 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly) ，可描述其 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-104">Like all [*processes*](/windows/desktop/SecGloss/p-gly), a protected server has a [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes its [*security context*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="9a5ba-105">當用戶端連接到受保護的伺服器時，伺服器可能會想要使用用戶端的安全性內容來執行動作，而不是使用伺服器的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-105">When a client connects to a protected server, the server may want to perform actions using the client's security context instead of the server's security context.</span></span> <span data-ttu-id="9a5ba-106">例如，當動態資料交換中的用戶端 (DDE) 對話從 DDE 伺服器要求資訊時，伺服器必須確認用戶端是否允許存取訊號。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-106">For example, when a client in a dynamic data exchange (DDE) conversation requests information from a DDE server, the server needs to verify that the client is allowed access to the information.</span></span>

<span data-ttu-id="9a5ba-107">有兩種方式可讓伺服器在用戶端的安全性內容中採取行動：</span><span class="sxs-lookup"><span data-stu-id="9a5ba-107">There are two ways that a server can act in the client's security context:</span></span>

-   <span data-ttu-id="9a5ba-108">伺服器進程的執行緒可以模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-108">A thread of the server process can impersonate the client.</span></span> <span data-ttu-id="9a5ba-109">在此情況下，伺服器的執行緒具有模擬 [*存取權杖*](/windows/desktop/SecGloss/a-gly) ，可識別用戶端、用戶端群組和用戶端的 [*許可權*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-109">In this case, the server's thread has an impersonation [*access token*](/windows/desktop/SecGloss/a-gly) that identifies the client, the client's groups, and the client's [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="9a5ba-110">如需詳細資訊，請參閱 [用戶端](client-impersonation.md)模擬。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-110">For more information, see [Client Impersonation](client-impersonation.md).</span></span>
-   <span data-ttu-id="9a5ba-111">伺服器可以取得用戶端的 [*認證*](/windows/desktop/SecGloss/c-gly) ，並將用戶端記錄到伺服器的電腦上。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-111">The server can get the client's [*credentials*](/windows/desktop/SecGloss/c-gly) and log the client on to the server's computer.</span></span> <span data-ttu-id="9a5ba-112">這會建立新的登入 [*會話*](/windows/desktop/SecGloss/s-gly) ，並產生用戶端的主要存取權杖。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-112">This creates a new logon [*session*](/windows/desktop/SecGloss/s-gly) and produces a primary access token for the client.</span></span> <span data-ttu-id="9a5ba-113">然後伺服器可以使用用戶端的存取權杖來模擬用戶端，或啟動在用戶端的安全性內容中執行的新進程。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-113">The server can then use the client's access token to impersonate the client or to start a new process that runs in the security context of the client.</span></span> <span data-ttu-id="9a5ba-114">如需詳細資訊，請參閱 [用戶端登入會話](client-logon-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-114">For more information, see [Client Logon Sessions](client-logon-sessions.md).</span></span>

<span data-ttu-id="9a5ba-115">在大部分的情況下，模擬用戶端就已足夠。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-115">In most cases, impersonating the client is sufficient.</span></span> <span data-ttu-id="9a5ba-116">模擬可讓伺服器檢查用戶端對安全物件的存取權、檢查用戶端的許可權，以及產生可識別用戶端的審核記錄專案。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-116">Impersonation enables the server to check the client's access to securable objects, check the client's privileges, and generate audit trail entries that identify the client.</span></span> <span data-ttu-id="9a5ba-117">一般來說，只有當伺服器需要使用用戶端的安全性內容來存取網路資源時，才需要啟動用戶端登入會話。</span><span class="sxs-lookup"><span data-stu-id="9a5ba-117">Typically, a server needs to start a client logon session only if it needs to use the client's security context to access network resources.</span></span>

 

 
