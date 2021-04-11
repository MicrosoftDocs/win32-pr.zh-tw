---
description: 模擬是指執行緒使用與擁有線程的進程不同的安全性資訊來執行的能力。
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: " (授權) 的用戶端模擬"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e72abb17c9f5f6271f55fbfc77da4f6b93ca2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943666"
---
# <a name="client-impersonation-authorization"></a><span data-ttu-id="dd77d-103"> (授權) 的用戶端模擬</span><span class="sxs-lookup"><span data-stu-id="dd77d-103">Client Impersonation (Authorization)</span></span>

<span data-ttu-id="dd77d-104">模擬 [*是指*](/windows/desktop/SecGloss/i-gly)執行緒使用與擁有線程的進程不同的安全性資訊來執行的能力。</span><span class="sxs-lookup"><span data-stu-id="dd77d-104">[*Impersonation*](/windows/desktop/SecGloss/i-gly) is the ability of a thread to execute using different security information than the process that owns the thread.</span></span> <span data-ttu-id="dd77d-105">一般來說，伺服器應用程式中的執行緒會模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="dd77d-105">Typically, a thread in a server application impersonates a client.</span></span> <span data-ttu-id="dd77d-106">這可讓伺服器執行緒代表該用戶端進行行動，以存取伺服器上的物件，或驗證對用戶端本身物件的存取。</span><span class="sxs-lookup"><span data-stu-id="dd77d-106">This allows the server thread to act on behalf of that client to access objects on the server or validate access to the client's own objects.</span></span>

<span data-ttu-id="dd77d-107">Microsoft Windows API 提供下列功能來開始模擬：</span><span class="sxs-lookup"><span data-stu-id="dd77d-107">The Microsoft Windows API provides the following functions to begin an impersonation:</span></span>

-   <span data-ttu-id="dd77d-108">DDE 伺服器應用程式可以呼叫 [**DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) 函數來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="dd77d-108">A DDE server application can call the [**DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) function to impersonate a client.</span></span>
-   <span data-ttu-id="dd77d-109">具名管道伺服器可以呼叫 [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) 函數。</span><span class="sxs-lookup"><span data-stu-id="dd77d-109">A named-pipe server can call the [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) function.</span></span>
-   <span data-ttu-id="dd77d-110">您可以呼叫 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) 函式，以模擬已登入使用者 [*存取權杖*](/windows/desktop/SecGloss/a-gly)的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="dd77d-110">You can call the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function to impersonate the security context of a logged-on user's [*access token*](/windows/desktop/SecGloss/a-gly).</span></span>
-   <span data-ttu-id="dd77d-111">[**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself)函式可讓執行緒產生其本身存取權杖的複本。</span><span class="sxs-lookup"><span data-stu-id="dd77d-111">The [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) function enables a thread to generate a copy of its own access token.</span></span> <span data-ttu-id="dd77d-112">當應用程式需要變更單一線程的安全性內容時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="dd77d-112">This is useful when an application needs to change the security context of a single thread.</span></span> <span data-ttu-id="dd77d-113">例如，有時只有一個進程的執行緒需要啟用 [*許可權*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="dd77d-113">For example, sometimes only one thread of a process needs to enable a [*privilege*](/windows/desktop/SecGloss/p-gly).</span></span>
-   <span data-ttu-id="dd77d-114">您可以呼叫 [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) 函式，使目標執行緒在指定之模擬 [*token*](/windows/desktop/SecGloss/i-gly)的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="dd77d-114">You can call the [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) function to cause the target thread to run in the security context of a specified [*impersonation token*](/windows/desktop/SecGloss/i-gly).</span></span>
-   <span data-ttu-id="dd77d-115">Microsoft 遠端程序呼叫 (RPC) server 應用程式可以呼叫 [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) 函數來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="dd77d-115">A Microsoft Remote Procedure Call (RPC) server application can call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate a client.</span></span>
-   <span data-ttu-id="dd77d-116">[*安全性封裝*](/windows/desktop/SecGloss/s-gly)或應用程式伺服器可以呼叫 [**ImpersonateSecurityCoNtext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext)函式來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="dd77d-116">A [*security package*](/windows/desktop/SecGloss/s-gly) or application server can call the [**ImpersonateSecurityContext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) function to impersonate a client.</span></span>

<span data-ttu-id="dd77d-117">在這些模擬中，模擬執行緒可以藉由呼叫 [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函式來還原為它自己的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="dd77d-117">For most of these impersonations, the impersonating thread can revert to its own security context by calling the [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) function.</span></span> <span data-ttu-id="dd77d-118">例外狀況是 RPC 模擬，其中 RPC 伺服器應用程式會呼叫 [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) 或 [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) 來還原為其本身的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="dd77d-118">The exception is the RPC impersonation, in which the RPC server application calls [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) or [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) to revert to its own security context.</span></span>

 

 
