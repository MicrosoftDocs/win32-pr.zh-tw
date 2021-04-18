---
title: 在伺服器上使用傳輸層級安全性
description: 在具有遠端程序呼叫的伺服器上使用傳輸層級安全性， (RPC) 。
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- 在伺服器上使用傳輸層級安全性的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39af5b8fb43a57683804eb7b91067ca9faad4390
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463292"
---
# <a name="using-transport-level-security-on-the-server"></a><span data-ttu-id="66487-104">在伺服器上使用傳輸層級安全性</span><span class="sxs-lookup"><span data-stu-id="66487-104">Using Transport-level Security on the Server</span></span>

<span data-ttu-id="66487-105">本節提供傳輸層級安全性的討論，分為下列主題：</span><span class="sxs-lookup"><span data-stu-id="66487-105">This section presents discussions of transport-level security, divided into the following topics:</span></span>

-   [<span data-ttu-id="66487-106">在用戶端上使用 Transport-Level 安全性</span><span class="sxs-lookup"><span data-stu-id="66487-106">Using Transport-Level Security on the Client</span></span>](using-transport-level-security-on-the-client.md)

<span data-ttu-id="66487-107">當您使用 [ncacn \_ np](/windows/desktop/Midl/ncacn-np) 或 [ncalrpc](/windows/desktop/Midl/ncalrpc) 做為通訊協定順序時，伺服器會在選取通訊協定順序時，指定端點的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="66487-107">When you use [ncacn\_np](/windows/desktop/Midl/ncacn-np) or [ncalrpc](/windows/desktop/Midl/ncalrpc) as the protocol sequence, the server specifies a security descriptor for the endpoint at the time it selects the protocol sequence.</span></span> <span data-ttu-id="66487-108">如需通訊協定順序的詳細資訊，請參閱 [指定通訊協定順序](specifying-protocol-sequences.md)。</span><span class="sxs-lookup"><span data-stu-id="66487-108">For more information on protocol sequences, see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="66487-109">您的應用程式會將安全描述項提供為額外的參數， (標準憑證-DCE 參數的擴充功能，) 所有開頭為首碼 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 和 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)的函式。</span><span class="sxs-lookup"><span data-stu-id="66487-109">Your application provides the security descriptor as an additional parameter (an extension to the standard OSF-DCE parameters) on all functions that start with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs).</span></span> <span data-ttu-id="66487-110">安全描述項可控制用戶端是否可以連接到端點。</span><span class="sxs-lookup"><span data-stu-id="66487-110">The security descriptor controls whether a client can connect to the endpoint.</span></span>

<span data-ttu-id="66487-111">每個進程和執行緒都與安全性權杖相關聯。</span><span class="sxs-lookup"><span data-stu-id="66487-111">Each process and thread is associated with a security token.</span></span> <span data-ttu-id="66487-112">此權杖包含預設安全描述項，可用於處理常式所建立的任何物件，例如端點。</span><span class="sxs-lookup"><span data-stu-id="66487-112">This token includes a default security descriptor that is used for any objects that the process creates, such as the endpoint.</span></span> <span data-ttu-id="66487-113">如果您的應用程式在呼叫 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 和 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)首碼的函式時未指定安全描述項，則 RPC 執行時間程式庫會將預設安全描述項從進程安全性權杖套用至端點。</span><span class="sxs-lookup"><span data-stu-id="66487-113">If your application does not specify a security descriptor when calling a function with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), the RPC run-time library applies the default security descriptor from the process security token to the endpoint.</span></span>

<span data-ttu-id="66487-114">為了保證所有用戶端都可以存取伺服器應用程式，系統管理員應該在具有所有用戶端可使用之預設安全描述項的進程上啟動伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="66487-114">To guarantee that the server application is accessible to all clients, the administrator should start the server application on a process that has a default security descriptor that all clients can use.</span></span> <span data-ttu-id="66487-115">一般來說，只有系統進程會有預設的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="66487-115">Generally, only system processes have a default security descriptor.</span></span>

<span data-ttu-id="66487-116">如需這些函式和函數的詳細資訊， [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) 和 [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself)。</span><span class="sxs-lookup"><span data-stu-id="66487-116">For more information about these functions and the functions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span></span>

 

 