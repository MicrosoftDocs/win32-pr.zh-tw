---
description: 當伺服器收到來自用戶端的第一個挑戰回應時，Microsoft Digest 會執行初始驗證。
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft 摘要式驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984641"
---
# <a name="microsoft-digest-authentication"></a><span data-ttu-id="7c3da-103">Microsoft 摘要式驗證</span><span class="sxs-lookup"><span data-stu-id="7c3da-103">Microsoft Digest Authentication</span></span>

<span data-ttu-id="7c3da-104">當伺服器收到來自用戶端的第一個挑戰回應時，Microsoft Digest 會執行初始驗證。</span><span class="sxs-lookup"><span data-stu-id="7c3da-104">Microsoft Digest performs an initial authentication when the server receives the first challenge response from a client.</span></span> <span data-ttu-id="7c3da-105">伺服器會驗證用戶端是否未經過驗證，然後藉由存取網域控制站的服務來執行初始驗證。</span><span class="sxs-lookup"><span data-stu-id="7c3da-105">The server verifies that the client has not been authenticated and then performs the initial authentication by accessing the services of a domain controller.</span></span> <span data-ttu-id="7c3da-106">如需此程式的詳細說明，請參閱 [使用 Microsoft Digest 的初始驗證](initial-authentication-using-microsoft-digest.md)。</span><span class="sxs-lookup"><span data-stu-id="7c3da-106">For a detailed description of this procedure, see [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>

<span data-ttu-id="7c3da-107">當初始驗證成功時，伺服器會收到摘要 [*工作階段金鑰*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7c3da-107">When the initial authentication is successful the server receives a Digest [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="7c3da-108">伺服器會快取此金鑰，並使用它來向用戶端驗證後續的資源要求。</span><span class="sxs-lookup"><span data-stu-id="7c3da-108">The server caches this key and uses it to authenticate subsequent requests for resources from the client.</span></span> <span data-ttu-id="7c3da-109">這是本機驗證，也就是不需要存取網域控制站。</span><span class="sxs-lookup"><span data-stu-id="7c3da-109">This authentication is local, that is, it does not require access to a domain controller.</span></span> <span data-ttu-id="7c3da-110">如需此程式的詳細說明，請參閱 [使用 Microsoft Digest 驗證後續要求](authenticating-subsequent-requests-using-microsoft-digest.md)。</span><span class="sxs-lookup"><span data-stu-id="7c3da-110">For a detailed description of this procedure see [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="7c3da-111">使用 HTTP 時，不會在用戶端與伺服器之間維護連接。</span><span class="sxs-lookup"><span data-stu-id="7c3da-111">When using HTTP, there is no connection maintained between client and server.</span></span> <span data-ttu-id="7c3da-112">為了減少網域控制站流量並改善效能，Microsoft Digest 會在驗證成功後快取所收到的資訊。</span><span class="sxs-lookup"><span data-stu-id="7c3da-112">To reduce domain controller traffic and improve performance, Microsoft Digest caches information received after successful authentication.</span></span> <span data-ttu-id="7c3da-113">如需此程式的詳細資訊，請參閱 [維護連接之間的安全性內容](maintaining-the-security-context-between-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="7c3da-113">For information about this process, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span>

 

 
