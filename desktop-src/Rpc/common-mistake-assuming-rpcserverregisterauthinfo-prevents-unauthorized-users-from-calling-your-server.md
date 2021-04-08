---
title: 常見的錯誤假設 RpcServerRegisterAuthInfo 可防止未經授權的使用者呼叫您的伺服器
description: 當安全性提供者在伺服器上使用 RpcServerRegisterAuthInfo 函式註冊時，就會新增一個選項，而不是需求。
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675092"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a><span data-ttu-id="bc5c0-103">常見錯誤：假設 RpcServerRegisterAuthInfo 可防止未經授權的使用者呼叫您的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc5c0-103">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>

<span data-ttu-id="bc5c0-104">當安全性提供者在伺服器上使用 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式註冊時，就會新增一個選項，而不是需求。</span><span class="sxs-lookup"><span data-stu-id="bc5c0-104">When security providers are registered on the server with the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function, an option is added, not a requirement.</span></span> <span data-ttu-id="bc5c0-105">這表示不會取代先前的 **RpcServerRegisterAuthInfo** 註冊。</span><span class="sxs-lookup"><span data-stu-id="bc5c0-105">This means previous registrations with **RpcServerRegisterAuthInfo** are not replaced.</span></span> <span data-ttu-id="bc5c0-106">這也表示未經驗證的用戶端仍然可以連接。</span><span class="sxs-lookup"><span data-stu-id="bc5c0-106">This also means unauthenticated clients still can connect.</span></span> <span data-ttu-id="bc5c0-107">藉由呼叫 **RpcServerRegisterAuthInfo** 函式，不允許未經驗證的用戶端進行連接;它們仍然可以連接，但 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) 和 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) 之類的函式呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="bc5c0-107">By calling the **RpcServerRegisterAuthInfo** function, unauthenticated clients are not disallowed from connecting; they can still connect, but function calls such as [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) will fail.</span></span> <span data-ttu-id="bc5c0-108">因此，當呼叫 **RpcServerRegisterAuthInfo** 函式時，潛在的攻擊者也不會被 weeded 出，而應該有存取權的用戶端也有機會證明其身分識別。</span><span class="sxs-lookup"><span data-stu-id="bc5c0-108">So when the **RpcServerRegisterAuthInfo** function is called, potential attackers have not been weeded out—rather, clients that ought to have access are given a chance to prove their identity.</span></span> <span data-ttu-id="bc5c0-109">檢查仍必須備妥，以判斷是否有潛在攻擊者嘗試連接。</span><span class="sxs-lookup"><span data-stu-id="bc5c0-109">Checks must still be in place to determine whether potential attackers are attempting to connect.</span></span>

 

 




