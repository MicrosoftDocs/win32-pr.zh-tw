---
description: 在用戶端/伺服器應用程式協定中，伺服器系結至通訊埠，例如通訊端或 RPC 介面。
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: 使用驗證建立安全連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a43483893c8dcf56e6db6b3c7d7aa1451bf9540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985064"
---
# <a name="establishing-a-secure-connection-with-authentication"></a><span data-ttu-id="1e8eb-103">使用驗證建立安全連線</span><span class="sxs-lookup"><span data-stu-id="1e8eb-103">Establishing a Secure Connection with Authentication</span></span>

<span data-ttu-id="1e8eb-104">在用戶端/伺服器 [*應用程式協定*](/windows/desktop/SecGloss/a-gly)中，伺服器系結至通訊埠，例如通訊端或 RPC 介面。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-104">In a client/server [*application protocol*](/windows/desktop/SecGloss/a-gly), a server binds to a communication port such as a socket or an RPC interface.</span></span> <span data-ttu-id="1e8eb-105">然後伺服器會等候用戶端連接並要求服務。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-105">The server then waits for a client to connect and request service.</span></span> <span data-ttu-id="1e8eb-106">在相互驗證的情況下，連接設定的安全性角色是雙折迭的角色：</span><span class="sxs-lookup"><span data-stu-id="1e8eb-106">The role of security at connection setup is two-fold in the case of mutual authentication:</span></span>

-   <span data-ttu-id="1e8eb-107">伺服器的用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-107">Client authentication by the server.</span></span>
-   <span data-ttu-id="1e8eb-108">用戶端的伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-108">Server authentication by the client.</span></span>

<span data-ttu-id="1e8eb-109">傳輸應用程式的用戶端和伺服器元件會使用 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 來建立安全的連接來傳輸訊息。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-109">The client and server components of a transport application use a [*security package*](/windows/desktop/SecGloss/s-gly) to establish a secure connection for transmitting messages.</span></span> <span data-ttu-id="1e8eb-110">建立安全連線的第一個步驟是建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly);亦即，包含與連線相關之安全性資料的不透明資料結構，例如 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly) 和會話的持續時間。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-110">The first step in establishing a secure connection is to create a [*security context*](/windows/desktop/SecGloss/s-gly); that is, an opaque data structure that contains the security data relevant to a connection, such as a [*session key*](/windows/desktop/SecGloss/s-gly) and the duration of the session.</span></span>

<span data-ttu-id="1e8eb-111">安全性內容基本上是從與用戶端相關聯之安全性封裝的訊息，與與伺服器相關聯的安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-111">A security context is essentially a message from the security package associated with the client to the security package associated with the server.</span></span> <span data-ttu-id="1e8eb-112">因此，建立安全性內容通常會要求用戶端和伺服器對其各自的安全性套件進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-112">Consequently, creating a security context typically requires both client and server to make calls to their respective security packages.</span></span> <span data-ttu-id="1e8eb-113">如需內容函數的詳細資訊，請參閱 [內容管理](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-113">For more information on context functions, see [Context Management](authentication-functions.md).</span></span>

<span data-ttu-id="1e8eb-114">用來建立安全驗證連線的通訊協定，需要在用戶端與伺服器之間交換一或多個「安全性權杖」。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-114">The protocol used to establish a secure, authenticated connection involves the exchange of one or more "security tokens" between the client and the server.</span></span> <span data-ttu-id="1e8eb-115">這些權杖會以不透明訊息的形式連同任何其他 [*應用程式通訊協定*](/windows/desktop/SecGloss/a-gly)特定資訊的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-115">These tokens are sent as opaque messages by the two sides along with any other [*application protocol*](/windows/desktop/SecGloss/a-gly)-specific information.</span></span> <span data-ttu-id="1e8eb-116">以不透明的訊息而言，用戶端會從安全性封裝函式接收權杖，其無法解讀或變更，而是以訊息的形式轉送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-116">As an opaque message, the token is received from a security package function by the client, which cannot interpret or change it, and forwarded as a message to the server.</span></span> <span data-ttu-id="1e8eb-117">此權杖對伺服器也是不透明的，不能解讀或變更權杖。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-117">The token is also opaque to the server, which can neither interpret nor change the token.</span></span> <span data-ttu-id="1e8eb-118">伺服器會將不透明的權杖轉送到其安全性封裝以進行解讀。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-118">The server forwards the opaque token to its security package for interpretation.</span></span> <span data-ttu-id="1e8eb-119">封裝接著會通知伺服器用戶端驗證，或驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-119">The package then informs the server of the client authentication or failure to authenticate.</span></span>

<span data-ttu-id="1e8eb-120">用戶端會在訊息中接收伺服器的權杖、從接收的訊息抓取權杖，並在對其安全性封裝的呼叫中使用該權杖。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-120">The client receives the server's token in a message, retrieves the token from the received message, and uses that token in a call to its security package.</span></span> <span data-ttu-id="1e8eb-121">然後，用戶端會再次呼叫安全性封裝，指出是否已建立安全連線，或是在安全連線準備就緒之前，是否需要進一步的交換。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-121">The client then calls the security package again indicating whether a secure connection has been established or whether further exchanges are needed before a secure connection is ready.</span></span> <span data-ttu-id="1e8eb-122">理論上，所需的安全性權杖交換數量沒有限制。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-122">Theoretically, there is no limit to the number of exchanges of security tokens needed.</span></span> <span data-ttu-id="1e8eb-123">在實務上，只需要有限的交換數目。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-123">In practice, only a limited number of exchanges is required.</span></span> <span data-ttu-id="1e8eb-124">NTLM 驗證是以挑戰/回應配置為基礎，而且會使用三個腿來驗證服務器的用戶端。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-124">NTLM authentication is based on the challenge/response scheme, and uses three legs to authenticate a client to the server.</span></span> <span data-ttu-id="1e8eb-125">[*Kerberos*](/windows/desktop/SecGloss/k-gly) 5.0 版通訊協定可能需要額外的訊息交換。</span><span class="sxs-lookup"><span data-stu-id="1e8eb-125">The [*Kerberos*](/windows/desktop/SecGloss/k-gly) version 5.0 protocol can require additional message exchanges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e8eb-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e8eb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e8eb-127">用戶端內容初始化</span><span class="sxs-lookup"><span data-stu-id="1e8eb-127">Client Context Initialization</span></span>](client-context-initialization.md)
</dt> <dt>

[<span data-ttu-id="1e8eb-128">伺服器內容初始化</span><span class="sxs-lookup"><span data-stu-id="1e8eb-128">Server Context Initialization</span></span>](server-context-initialization.md)
</dt> </dl>

 

 
