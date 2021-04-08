---
title: RPC 應用程式中的相互驗證
description: RPC 服務可以使用服務連接點來發佈本身，也可以使用 RPC 名稱服務 (RpcNs) Api。
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- RPC 應用程式中的相互驗證 AD
- Active Directory，使用，相互驗證，RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842059"
---
# <a name="mutual-authentication-in-rpc-applications"></a><span data-ttu-id="ef124-105">RPC 應用程式中的相互驗證</span><span class="sxs-lookup"><span data-stu-id="ef124-105">Mutual Authentication in RPC Applications</span></span>

<span data-ttu-id="ef124-106">RPC 服務可以使用服務連接點來發佈本身，也可以使用 RPC 名稱服務 (RpcNs) Api。</span><span class="sxs-lookup"><span data-stu-id="ef124-106">RPC services can use service connection points to publish themselves, or they can use the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="ef124-107">本主題討論如何使用 rpc 服務來執行相互驗證，此服務會使用 RPC 名稱服務 (RpcNs) Api 來發佈本身。</span><span class="sxs-lookup"><span data-stu-id="ef124-107">This topic discusses how to perform mutual authentication with an RPC service that publishes itself using the RPC name service (RpcNs) APIs.</span></span>

<span data-ttu-id="ef124-108">**在目錄中註冊 SPN**</span><span class="sxs-lookup"><span data-stu-id="ef124-108">**To register an SPN in the directory**</span></span>

1.  <span data-ttu-id="ef124-109">呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函式，為服務 (SPN) 撰寫服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="ef124-109">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose a service principal name (SPN) for the service.</span></span>
2.  <span data-ttu-id="ef124-110">呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函式，在服務將在其內容中執行的服務帳戶或電腦帳戶上註冊 SPN。</span><span class="sxs-lookup"><span data-stu-id="ef124-110">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPN on the service account or computer account in whose context the service will run.</span></span>

<span data-ttu-id="ef124-111">**向 RPC 命名服務註冊服務**</span><span class="sxs-lookup"><span data-stu-id="ef124-111">**To register a service with the RPC naming service**</span></span>

1.  <span data-ttu-id="ef124-112">確認已在執行服務的帳戶上註冊適當的 Spn。</span><span class="sxs-lookup"><span data-stu-id="ef124-112">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="ef124-113">如需詳細資訊，請參閱 [登入帳戶維護](logon-account-maintenance-tasks.md)工作。</span><span class="sxs-lookup"><span data-stu-id="ef124-113">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>
2.  <span data-ttu-id="ef124-114">呼叫 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式，以使用 rpc 驗證服務來註冊服務 SPN，並指定 **rpc \_ C \_ 驗證 \_ GSS \_ NEGOTIATE** 作為要使用的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="ef124-114">Call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function to register the service SPN with the RPC authentication service, and specify **RPC\_C\_AUTHN\_GSS\_NEGOTIATE** as the authentication service to use.</span></span>

<span data-ttu-id="ef124-115">如需在 RPC 服務中執行相互驗證的詳細資訊，請參閱 [撰寫經過驗證的 SSPI 伺服器](/windows/desktop/Rpc/writing-an-authenticated-sspi-server)。</span><span class="sxs-lookup"><span data-stu-id="ef124-115">For more information about performing mutual authentication in an RPC service, see [Writing an Authenticated SSPI Server](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span></span>

<span data-ttu-id="ef124-116">**從用戶端驗證服務**</span><span class="sxs-lookup"><span data-stu-id="ef124-116">**To authenticate the service from the client**</span></span>

1.  <span data-ttu-id="ef124-117">從 RPC 系結中解壓縮主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ef124-117">Extract the host name from the RPC Binding.</span></span>
2.  <span data-ttu-id="ef124-118">使用服務類別、DNS 主機名稱和服務名稱呼叫 [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) 函式，以撰寫服務的 SPN;這是 RpcNs 案例中連接點的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="ef124-118">Compose the SPN for the service by calling the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function with the service class, the DNS host name, and the service name; that is the distinguished name of the connection point in the case of RpcNs.</span></span>

    <span data-ttu-id="ef124-119">如需撰寫 RpcNs 服務之 SPN 的詳細資訊，請參閱 [撰寫 RpcNs 服務的 spn](composing-spns-for-an-rpcns-service.md)。</span><span class="sxs-lookup"><span data-stu-id="ef124-119">For more information about composing an SPN for an RpcNs service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

3.  <span data-ttu-id="ef124-120">設定 [**RPC \_ 安全性 \_ QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) 結構以要求相互驗證。</span><span class="sxs-lookup"><span data-stu-id="ef124-120">Set up an [**RPC\_SECURITY\_QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) structure to request mutual authentication.</span></span>
4.  <span data-ttu-id="ef124-121">呼叫 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函數，以設定 RPC 系結的驗證資料。</span><span class="sxs-lookup"><span data-stu-id="ef124-121">Call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="ef124-122">用戶端至少必須要求 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 完整性** ，以確保通訊未遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="ef124-122">The client must request at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** to ensure that communications have not been tampered.</span></span> <span data-ttu-id="ef124-123">為了提高安全性，用戶端應該指定 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權** 來要求加密。</span><span class="sxs-lookup"><span data-stu-id="ef124-123">For increased security, the client should specify **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** to request encryption.</span></span>
5.  <span data-ttu-id="ef124-124">執行 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ef124-124">Perform the RPC call.</span></span>

<span data-ttu-id="ef124-125">如需在 RPC 用戶端中執行相互驗證的詳細資訊，請參閱 [撰寫經過驗證的 SSPI 用戶端](/windows/desktop/Rpc/writing-an-authenticated-sspi-client)。</span><span class="sxs-lookup"><span data-stu-id="ef124-125">For more information about performing mutual authentication in an RPC client, see [Writing an Authenticated SSPI Client](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span></span>

<span data-ttu-id="ef124-126">**從服務驗證用戶端**</span><span class="sxs-lookup"><span data-stu-id="ef124-126">**To authenticate the client from the service**</span></span>

1.  <span data-ttu-id="ef124-127">呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數來驗證用戶端所指定的驗證參數。</span><span class="sxs-lookup"><span data-stu-id="ef124-127">Call the [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) function to verify the authentication parameters specified by the client.</span></span> <span data-ttu-id="ef124-128">如果用戶端未要求所需的驗證層級，請拒絕呼叫。</span><span class="sxs-lookup"><span data-stu-id="ef124-128">If the client has not requested the desired level of authentication, reject the call.</span></span> <span data-ttu-id="ef124-129">請注意，RPC 服務必須在每次呼叫時驗證驗證等級、驗證服務和用戶端身分識別，以確保用戶端已通過適當的驗證。</span><span class="sxs-lookup"><span data-stu-id="ef124-129">Be aware that an RPC service must verify the authentication level, authentication service, and client identity on every call to ensure that the client has been properly authenticated.</span></span>
2.  <span data-ttu-id="ef124-130">呼叫 [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) 函數來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="ef124-130">Call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate the client.</span></span>
3.  <span data-ttu-id="ef124-131">執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="ef124-131">Perform the requested operation.</span></span>
4.  <span data-ttu-id="ef124-132">呼叫 [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) 函式來還原至服務安全性內容。</span><span class="sxs-lookup"><span data-stu-id="ef124-132">Call the [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) function to revert to the service security context.</span></span>

<span data-ttu-id="ef124-133">如需 RPC 用戶端模擬的詳細資訊，請參閱 [用戶端](/windows/desktop/Rpc/client-impersonation)模擬。</span><span class="sxs-lookup"><span data-stu-id="ef124-133">For more information about RPC client impersonation, see [Client Impersonation](/windows/desktop/Rpc/client-impersonation).</span></span>

<span data-ttu-id="ef124-134">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="ef124-134">For more information, see:</span></span>

-   [<span data-ttu-id="ef124-135">使用 RPC 名稱服務發行 (RpcNs) </span><span class="sxs-lookup"><span data-stu-id="ef124-135">Publishing with the RPC Name Service (RpcNs)</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="ef124-136">RPC 安全性基本知識</span><span class="sxs-lookup"><span data-stu-id="ef124-136">RPC Security Essentials</span></span>](/windows/desktop/Rpc/rpc-security-essentials)

 

 