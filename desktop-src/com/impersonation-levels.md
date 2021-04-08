---
title: " (COM) 的模擬層級"
description: 如果模擬成功，就表示用戶端已同意讓伺服器成為用戶端的程度。
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842751"
---
# <a name="impersonation-levels"></a><span data-ttu-id="28586-103">模擬層級</span><span class="sxs-lookup"><span data-stu-id="28586-103">Impersonation Levels</span></span>

<span data-ttu-id="28586-104">如果模擬成功，就表示用戶端已同意讓伺服器成為用戶端的程度。</span><span class="sxs-lookup"><span data-stu-id="28586-104">If impersonation succeeds, it means that the client has agreed to let the server be the client to some degree.</span></span> <span data-ttu-id="28586-105">不同程度的模擬稱為模擬 *層級*，而且會指出當伺服器模擬用戶端時，提供給伺服器的授權數量。</span><span class="sxs-lookup"><span data-stu-id="28586-105">The varying degrees of impersonation are called *impersonation levels*, and they indicate how much authority is given to the server when it is impersonating the client.</span></span>

<span data-ttu-id="28586-106">目前有四個模擬層級：*匿名*、*識別*、*模擬和\*\*委派*。</span><span class="sxs-lookup"><span data-stu-id="28586-106">Currently, there are four impersonation levels: *anonymous*, *identify*, *impersonate*, and *delegate*.</span></span> <span data-ttu-id="28586-107">下列清單簡要描述每個模擬等級：</span><span class="sxs-lookup"><span data-stu-id="28586-107">The following list briefly describes each impersonation level:</span></span>

<dl> <dt>

<span data-ttu-id="28586-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>匿名 (RPC \_ C \_ IMP \_ 層級 \_ 匿名) </span><span class="sxs-lookup"><span data-stu-id="28586-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC\_C\_IMP\_LEVEL\_ANONYMOUS)</span></span>
</dt> <dd>

<span data-ttu-id="28586-109">用戶端對伺服器而言是匿名。</span><span class="sxs-lookup"><span data-stu-id="28586-109">The client is anonymous to the server.</span></span> <span data-ttu-id="28586-110">伺服器處理序可以模擬用戶端，但模擬語彙基元 (Token) 並不包含用戶端的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="28586-110">The server process can impersonate the client, but the impersonation token does not contain any information about the client.</span></span> <span data-ttu-id="28586-111">只有本機進程間的通訊傳輸才支援此層級。</span><span class="sxs-lookup"><span data-stu-id="28586-111">This level is only supported over the local interprocess communication transport.</span></span> <span data-ttu-id="28586-112">所有其他傳輸都會以無訊息方式升級此層級來識別。</span><span class="sxs-lookup"><span data-stu-id="28586-112">All other transports silently promote this level to identify.</span></span>

</dd> <dt>

<span data-ttu-id="28586-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>識別 (RPC \_ C \_ IMP \_ 等級 \_ 識別) </span><span class="sxs-lookup"><span data-stu-id="28586-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY)</span></span>
</dt> <dd>

<span data-ttu-id="28586-114">系統預設層級。</span><span class="sxs-lookup"><span data-stu-id="28586-114">The system default level.</span></span> <span data-ttu-id="28586-115">伺服器可以取得用戶端的識別 (Identity)，而且可以模擬用戶端來做 ACL 檢查。</span><span class="sxs-lookup"><span data-stu-id="28586-115">The server can obtain the client's identity, and the server can impersonate the client to do ACL checks.</span></span>

</dd> <dt>

<span data-ttu-id="28586-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>模擬 (RPC \_ C \_ IMP \_ 層級模擬 \_) </span><span class="sxs-lookup"><span data-stu-id="28586-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE)</span></span>
</dt> <dd>

<span data-ttu-id="28586-117">伺服器代表用戶端動作時可以模擬用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="28586-117">The server can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="28586-118">伺服器可以像用戶端一樣存取本機資源。</span><span class="sxs-lookup"><span data-stu-id="28586-118">The server can access local resources as the client.</span></span> <span data-ttu-id="28586-119">如果伺服器在本機，則可以存取網路資源作為用戶端。</span><span class="sxs-lookup"><span data-stu-id="28586-119">If the server is local, it can access network resources as the client.</span></span> <span data-ttu-id="28586-120">如果伺服器是遠端伺服器，則只能存取與伺服器位於同一部電腦上的資源。</span><span class="sxs-lookup"><span data-stu-id="28586-120">If the server is remote, it can access only resources that are on the same computer as the server.</span></span>

</dd> <dt>

<span data-ttu-id="28586-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>委派 (RPC \_ C \_ IMP \_ 層級 \_ 委派) </span><span class="sxs-lookup"><span data-stu-id="28586-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC\_C\_IMP\_LEVEL\_DELEGATE)</span></span>
</dt> <dd>

<span data-ttu-id="28586-122">功能最強大的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="28586-122">The most powerful impersonation level.</span></span> <span data-ttu-id="28586-123">選取此層級時，伺服器 (不論本機或遠端) 代表用戶端動作時可以模擬用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="28586-123">When this level is selected, the server (whether local or remote) can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="28586-124">在模擬期間， (本機和網路) 的用戶端認證可傳遞至任意數目的電腦。</span><span class="sxs-lookup"><span data-stu-id="28586-124">During impersonation, the client's credentials (both local and network) can be passed to any number of computers.</span></span>

<span data-ttu-id="28586-125">若要讓模擬在委派層級運作，必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="28586-125">For impersonation to work at the delegate level, the following requirements must be met:</span></span>

-   <span data-ttu-id="28586-126">用戶端必須將模擬層級設定為 RPC \_ C \_ IMP \_ 層級 \_ 委派。</span><span class="sxs-lookup"><span data-stu-id="28586-126">The client must set the impersonation level to RPC\_C\_IMP\_LEVEL\_DELEGATE.</span></span>
-   <span data-ttu-id="28586-127">在 Active Directory 服務中，用戶端帳戶不得標示為「帳戶為機密，無法委派」。</span><span class="sxs-lookup"><span data-stu-id="28586-127">The client account must not be marked "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>
-   <span data-ttu-id="28586-128">伺服器帳戶必須標示 Active Directory 服務中的「受信任的委派」屬性。</span><span class="sxs-lookup"><span data-stu-id="28586-128">The server account must be marked with the "Trusted for delegation" attribute in the Active Directory Service.</span></span>
-   <span data-ttu-id="28586-129">裝載用戶端、伺服器和任何「下游」伺服器的電腦都必須在網域中執行。</span><span class="sxs-lookup"><span data-stu-id="28586-129">The computers hosting the client, the server, and any "downstream" servers must all be running in a domain.</span></span>

</dd> </dl>

<span data-ttu-id="28586-130">藉由選擇模擬等級，用戶端會向伺服器告知模擬用戶端的進度。</span><span class="sxs-lookup"><span data-stu-id="28586-130">By choosing the impersonation level, the client tells the server how far it can go in impersonating the client.</span></span> <span data-ttu-id="28586-131">用戶端會在用來與伺服器通訊的 proxy 上設定模擬等級。</span><span class="sxs-lookup"><span data-stu-id="28586-131">The client sets the impersonation level on the proxy it uses to communicate with the server.</span></span>

## <a name="setting-the-impersonation-level"></a><span data-ttu-id="28586-132">設定模擬等級</span><span class="sxs-lookup"><span data-stu-id="28586-132">Setting the Impersonation Level</span></span>

<span data-ttu-id="28586-133">有兩種方式可以設定模擬等級：</span><span class="sxs-lookup"><span data-stu-id="28586-133">There are two ways to set the impersonation level:</span></span>

-   <span data-ttu-id="28586-134">用戶端可以透過呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來設定 processwide。</span><span class="sxs-lookup"><span data-stu-id="28586-134">The client can set it processwide, through a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="28586-135">用戶端可以透過呼叫 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (或 Helper 函數 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)) ，在遠端物件的介面上設定 proxy 層級安全性。</span><span class="sxs-lookup"><span data-stu-id="28586-135">A client can set proxy-level security on an interface of a remote object through a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (or the helper function [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span></span>

<span data-ttu-id="28586-136">您可以透過 DwImpLevel 參數傳遞適當的 RPC \_ C \_ IMP \_ level \_ xxx 值給 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)或 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)  ，藉以設定模擬等級。</span><span class="sxs-lookup"><span data-stu-id="28586-136">You set the impersonation level by passing an appropriate RPC\_C\_IMP\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwImpLevel* parameter.</span></span>

<span data-ttu-id="28586-137">不同的驗證服務支援委派層級的模擬至不同的範圍。</span><span class="sxs-lookup"><span data-stu-id="28586-137">Different authentication services support delegate-level impersonation to different extents.</span></span> <span data-ttu-id="28586-138">例如，NTLMSSP 支援跨執行緒和跨進程的委派層級模擬，但不支援跨電腦。</span><span class="sxs-lookup"><span data-stu-id="28586-138">For instance, NTLMSSP supports cross-thread and cross-process delegate-level impersonation, but not cross-computer.</span></span> <span data-ttu-id="28586-139">另一方面，Kerberos 通訊協定支援跨電腦界限的委派層級模擬，而 Schannel 則不支援在委派層級進行任何模擬。</span><span class="sxs-lookup"><span data-stu-id="28586-139">On the other hand, the Kerberos protocol supports delegate-level impersonation across computer boundaries, while Schannel does not support any impersonation at the delegate level.</span></span> <span data-ttu-id="28586-140">如果您在模擬層級擁有 proxy，而且想要將模擬層級設定為委派，則應該使用每個參數的預設常數來呼叫 [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) ，但模擬等級除外。</span><span class="sxs-lookup"><span data-stu-id="28586-140">If you have a proxy at impersonate level and you want to set the impersonation level to delegate, you should call [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) using the default constants for every parameter except the impersonation level.</span></span> <span data-ttu-id="28586-141">COM 會在本機選擇 NTLM 和 Kerberos 通訊協定，當 Kerberos 通訊協定) 時，會從遠端 (。</span><span class="sxs-lookup"><span data-stu-id="28586-141">COM will choose NTLM locally and the Kerberos protocol remotely (when the Kerberos protocol will work).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28586-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="28586-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28586-143">委派和模擬</span><span class="sxs-lookup"><span data-stu-id="28586-143">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 