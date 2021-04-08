---
title: 使用 SCP 在 Windows 通訊端服務中進行相互驗證
description: 本節中的主題包含程式碼範例，示範如何使用服務連接點（ (SCP) ）來對服務進行相互驗證。
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- 使用 SCP AD 的 Windows 通訊端服務中的相互驗證
- Active Directory、使用、相互驗證、Windows sockets 服務和 SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527715c4a35dc15cd67f5820e6fa891b56452399
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842060"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a><span data-ttu-id="e1e24-105">使用 SCP 在 Windows 通訊端服務中進行相互驗證</span><span class="sxs-lookup"><span data-stu-id="e1e24-105">Mutual Authentication in a Windows Sockets Service with SCP</span></span>

<span data-ttu-id="e1e24-106">本節中的主題包含程式碼範例，示範如何使用服務連接點（ (SCP) ）來對服務進行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-106">The topics in this section include code examples that show how to perform mutual authentication with a service that publishes itself using a service connection point (SCP).</span></span> <span data-ttu-id="e1e24-107">這些範例是以 Microsoft Windows 通訊端服務為基礎，此服務會使用 SSPI 套件來處理用戶端與服務之間的相互驗證協調。</span><span class="sxs-lookup"><span data-stu-id="e1e24-107">The examples are based on a Microsoft Windows Sockets service that uses an SSPI package to handle the mutual authentication negotiation between a client and the service.</span></span> <span data-ttu-id="e1e24-108">使用下列程式，在此案例中執行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-108">Use the following procedures to implement mutual authentication within this scenario.</span></span>

<span data-ttu-id="e1e24-109">**若要在安裝服務時于目錄中註冊 Spn**</span><span class="sxs-lookup"><span data-stu-id="e1e24-109">**To register SPNs in a directory when a service is installed**</span></span>

1.  <span data-ttu-id="e1e24-110">呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函式，為服務)  (spn 撰寫服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="e1e24-110">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose service principal names (SPNs) for the service.</span></span>
2.  <span data-ttu-id="e1e24-111">呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函式，在服務將在其內容中執行的服務帳戶或電腦帳戶上註冊 spn。</span><span class="sxs-lookup"><span data-stu-id="e1e24-111">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPNs on the service account or computer account in whose context the service will run.</span></span> <span data-ttu-id="e1e24-112">此步驟必須由網域系統管理員執行;例外狀況是，在 LocalSystem 帳戶下執行的服務可以在 <service class> / <host> 服務主機的電腦帳戶上，以 "" 形式註冊其 SPN。</span><span class="sxs-lookup"><span data-stu-id="e1e24-112">This step must be performed by a domain administrator; an exception is that a service running under the LocalSystem account can register its SPN in the form "<service class>/<host>" on the computer account of the service host.</span></span>

<span data-ttu-id="e1e24-113">**確認服務啟動時的設定**</span><span class="sxs-lookup"><span data-stu-id="e1e24-113">**To verify configuration at service startup**</span></span>

-   <span data-ttu-id="e1e24-114">確認已在執行服務的帳戶上註冊適當的 Spn。</span><span class="sxs-lookup"><span data-stu-id="e1e24-114">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="e1e24-115">如需詳細資訊，請參閱 [登入帳戶維護](logon-account-maintenance-tasks.md)工作。</span><span class="sxs-lookup"><span data-stu-id="e1e24-115">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>

<span data-ttu-id="e1e24-116">**在用戶端啟動時驗證服務**</span><span class="sxs-lookup"><span data-stu-id="e1e24-116">**To authenticate the service at client startup**</span></span>

1.  <span data-ttu-id="e1e24-117">從服務的服務連接點取出連接資料。</span><span class="sxs-lookup"><span data-stu-id="e1e24-117">Retrieve connection data from the service's service connection point.</span></span>
2.  <span data-ttu-id="e1e24-118">建立與服務的連接。</span><span class="sxs-lookup"><span data-stu-id="e1e24-118">Establish a connection to the service.</span></span>
3.  <span data-ttu-id="e1e24-119">呼叫 [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) 函數，以撰寫服務的 SPN。</span><span class="sxs-lookup"><span data-stu-id="e1e24-119">Call the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function to compose an SPN for the service.</span></span> <span data-ttu-id="e1e24-120">撰寫來自已知服務類別字串的 SPN，以及從服務連接點取出的資料。</span><span class="sxs-lookup"><span data-stu-id="e1e24-120">Compose the SPN from the known service class string, and the data retrieved from the service connection point.</span></span> <span data-ttu-id="e1e24-121">這項資料包含執行服務之伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="e1e24-121">This data includes the host name of the server on which the service is running.</span></span> <span data-ttu-id="e1e24-122">請注意，主機名稱必須是 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="e1e24-122">Be aware that the host name must be a DNS name.</span></span>
4.  <span data-ttu-id="e1e24-123">使用 SSPI 安全性套件來執行驗證：</span><span class="sxs-lookup"><span data-stu-id="e1e24-123">Use an SSPI security package to perform the authentication:</span></span>
    1.  <span data-ttu-id="e1e24-124">呼叫 [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) 函數，以取得用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-124">Call the [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) function to acquire the client's credentials.</span></span>
    2.  <span data-ttu-id="e1e24-125">將用戶端認證和 SPN 傳遞至 [**InitializeSecurityCoNtext**](../SecAuthN/initializesecuritycontext--general.md) 函式，以產生要傳送至服務的安全性 blob 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-125">Pass the client credentials and the SPN to the [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) function to generate a security blob to send to the service for authentication.</span></span> <span data-ttu-id="e1e24-126">將 [ **ISC \_ 要求 \_ 相互 \_** 驗證] 旗標設定為要求相互驗證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-126">Set the **ISC\_REQ\_MUTUAL\_AUTH** flag to request mutual authentication.</span></span>
    3.  <span data-ttu-id="e1e24-127">使用服務交換 blob，直到驗證完成為止。</span><span class="sxs-lookup"><span data-stu-id="e1e24-127">Exchange blobs with the service until the authentication is complete.</span></span>
5.  <span data-ttu-id="e1e24-128">確認「適用于 **ISC 要求 \_ \_ 相互 \_** 驗證」旗標的傳回功能遮罩，以確認已執行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-128">Verify the returned capabilities mask for the **ISC\_REQ\_MUTUAL\_AUTH** flag to verify that mutual authentication was performed.</span></span>
6.  <span data-ttu-id="e1e24-129">如果驗證成功，請與已驗證的服務交換流量。</span><span class="sxs-lookup"><span data-stu-id="e1e24-129">If the authentication was successful, exchange traffic with the authenticated service.</span></span> <span data-ttu-id="e1e24-130">使用數位簽章來確保用戶端與服務之間的訊息不會遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="e1e24-130">Use digital signing to ensure that messages between client and service have not been tampered with.</span></span> <span data-ttu-id="e1e24-131">除非效能需求很嚴重，否則請使用加密。</span><span class="sxs-lookup"><span data-stu-id="e1e24-131">Unless performance requirements are severe, use encryption.</span></span> <span data-ttu-id="e1e24-132">如需詳細資訊和示範如何在 SSPI 封裝中使用 [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature)、 [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature)、 [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)和 [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) 函式的程式碼範例，請參閱 [確保訊息交換期間的通訊完整性](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange)。</span><span class="sxs-lookup"><span data-stu-id="e1e24-132">For more information and a code example that shows how to use the [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md), and [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) functions in an SSPI package, see [Ensuring Communication Integrity During Message Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).</span></span>

<span data-ttu-id="e1e24-133">**當用戶端連線時，由服務驗證用戶端**</span><span class="sxs-lookup"><span data-stu-id="e1e24-133">**To authenticate the client by the service when a client connects**</span></span>

1.  <span data-ttu-id="e1e24-134">載入支援相互驗證的 SSPI 安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="e1e24-134">Load an SSPI security package that supports mutual authentication.</span></span>
2.  <span data-ttu-id="e1e24-135">當用戶端連接時，請使用安全性套件來執行驗證：</span><span class="sxs-lookup"><span data-stu-id="e1e24-135">When a client connects, use the security package to perform the authentication:</span></span>
    1.  <span data-ttu-id="e1e24-136">呼叫 [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) 函數來取得服務認證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-136">Call the [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) function to acquire the service credentials.</span></span>
    2.  <span data-ttu-id="e1e24-137">將從用戶端接收的服務認證和安全性 blob 傳遞至 [**AcceptSecurityCoNtext**](../SecAuthN/acceptsecuritycontext--general.md) 函式，以產生要傳送回用戶端的安全性 blob。</span><span class="sxs-lookup"><span data-stu-id="e1e24-137">Pass the service credentials and the security blob received from the client to the [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) function to generate a security blob to send back to the client.</span></span>
    3.  <span data-ttu-id="e1e24-138">與用戶端交換 blob，直到驗證完成為止。</span><span class="sxs-lookup"><span data-stu-id="e1e24-138">Exchange blobs with the client until the authentication is complete.</span></span>
3.  <span data-ttu-id="e1e24-139">檢查「 **ASC \_ RET \_ 相互 \_ 驗證** 」旗標的傳回功能遮罩，確認是否已執行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="e1e24-139">Check the returned capabilities mask for the **ASC\_RET\_MUTUAL\_AUTH** flag to verify that mutual authentication was performed.</span></span>
4.  <span data-ttu-id="e1e24-140">如果驗證成功，請與已驗證的用戶端交換流量。</span><span class="sxs-lookup"><span data-stu-id="e1e24-140">If the authentication was successful, exchange traffic with the authenticated client.</span></span> <span data-ttu-id="e1e24-141">除非發生效能問題，否則請使用數位簽章和加密。</span><span class="sxs-lookup"><span data-stu-id="e1e24-141">Use digital signing and encryption unless performance is an issue.</span></span>

<span data-ttu-id="e1e24-142">如需此相互驗證案例的詳細資訊和程式碼範例，請參閱：</span><span class="sxs-lookup"><span data-stu-id="e1e24-142">For more information and a code example for this mutual authentication scenario, see:</span></span>

-   [<span data-ttu-id="e1e24-143">用戶端如何驗證 SCP 型 Windows 通訊端服務</span><span class="sxs-lookup"><span data-stu-id="e1e24-143">How a Client Authenticates an SCP-based Windows Sockets Service</span></span>](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [<span data-ttu-id="e1e24-144">針對 SCP 型 Windows 通訊端服務撰寫和註冊 Spn</span><span class="sxs-lookup"><span data-stu-id="e1e24-144">Composing and Registering SPNs for an SCP-based Windows Sockets Service</span></span>](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [<span data-ttu-id="e1e24-145">Windows 通訊端服務如何驗證用戶端</span><span class="sxs-lookup"><span data-stu-id="e1e24-145">How a Windows Sockets Service Authenticates a Client</span></span>](how-a-windows-sockets-service-authenticates-a-client.md)

<span data-ttu-id="e1e24-146">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="e1e24-146">For more information, see:</span></span>

-   [<span data-ttu-id="e1e24-147">使用服務連接點發佈</span><span class="sxs-lookup"><span data-stu-id="e1e24-147">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="e1e24-148">SSPI 檔</span><span class="sxs-lookup"><span data-stu-id="e1e24-148">SSPI documentation</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="e1e24-149">Windows 通訊端檔</span><span class="sxs-lookup"><span data-stu-id="e1e24-149">Windows Sockets documentation</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 