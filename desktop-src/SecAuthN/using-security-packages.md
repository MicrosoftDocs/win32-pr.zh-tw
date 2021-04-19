---
description: 列出可與 SSPI 搭配使用的安全性封裝。
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: 使用安全性封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df24bba0f910ba74a633e8a43f961cee4fb505db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980581"
---
# <a name="using-security-packages"></a><span data-ttu-id="8eff4-103">使用安全性封裝</span><span class="sxs-lookup"><span data-stu-id="8eff4-103">Using Security Packages</span></span>

<span data-ttu-id="8eff4-104">[*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 可搭配下列 [*安全性套件*](../secgloss/s-gly.md)使用：</span><span class="sxs-lookup"><span data-stu-id="8eff4-104">The [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) can be used with the following [*security packages*](../secgloss/s-gly.md):</span></span>

-   [<span data-ttu-id="8eff4-105">Kerberos 安全性套件</span><span class="sxs-lookup"><span data-stu-id="8eff4-105">Kerberos Security Package</span></span>](#kerberos-security-package)
-   [<span data-ttu-id="8eff4-106">NTLM 安全性封裝</span><span class="sxs-lookup"><span data-stu-id="8eff4-106">NTLM Security Package</span></span>](#ntlm-security-package)

<span data-ttu-id="8eff4-107">[*Kerberos*](../secgloss/k-gly.md)和 NTLM 通訊協定會實作為作業系統提供的 Secur32.dll [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 的安全性套件。</span><span class="sxs-lookup"><span data-stu-id="8eff4-107">The [*Kerberos*](../secgloss/k-gly.md) and NTLM protocols are implemented as security packages from the Secur32.dll [*security support provider*](../secgloss/s-gly.md) (SSP) supplied with the operating system.</span></span> <span data-ttu-id="8eff4-108">根據預設，在系統啟動時，電腦上的 [*本機安全機構*](../secgloss/l-gly.md) 會將 KERBEROS 和 NTLM 驗證的支援載入 (LSA) 。</span><span class="sxs-lookup"><span data-stu-id="8eff4-108">By default, support for both Kerberos and NTLM authentication are loaded by the [*local security authority*](../secgloss/l-gly.md) (LSA) on a computer when the system starts.</span></span> <span data-ttu-id="8eff4-109">在 Windows Server 或 Windows 網域中，可以使用這兩種套件來驗證網路登入和用戶端/伺服器連接。</span><span class="sxs-lookup"><span data-stu-id="8eff4-109">In Windows Server or Windows domains, either package can be used to authenticate network logons and client/server connections.</span></span> <span data-ttu-id="8eff4-110">使用哪一種取決於連接另一端的電腦功能。</span><span class="sxs-lookup"><span data-stu-id="8eff4-110">Which one is used depends on the capabilities of the computer on the other side of the connection.</span></span> <span data-ttu-id="8eff4-111">Kerberos 通訊協定一律是慣用的（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8eff4-111">The Kerberos protocol is always preferred, if available.</span></span>

<span data-ttu-id="8eff4-112">建立互動式使用者的安全性內容之後，就可以在使用者的安全性內容中執行的進程載入 Kerberos 或 NTLM 封裝的另一個實例，以支援交換、簽署、驗證、加密和解密訊息。</span><span class="sxs-lookup"><span data-stu-id="8eff4-112">After a security context for an interactive user has been established, another instance of the Kerberos or NTLM package can be loaded by a process running in the security context of the user to support the exchanging, signing, verifying, encrypting, and decrypting of messages.</span></span> <span data-ttu-id="8eff4-113">不過，除了 LSA 以外的任何程式都不允許存取認證快取中的 [*工作階段金鑰*](../secgloss/s-gly.md) 或票證。</span><span class="sxs-lookup"><span data-stu-id="8eff4-113">However, no process other than the LSA is ever permitted access to [*session keys*](../secgloss/s-gly.md) or tickets in the credentials cache.</span></span>

<span data-ttu-id="8eff4-114">系統服務和傳輸層級的應用程式會透過 SSPI 存取 SSP，以提供用來列舉系統上可用之安全性封裝的函式、選取封裝，以及使用該套件來取得已驗證的連接。</span><span class="sxs-lookup"><span data-stu-id="8eff4-114">System services and transport-level applications access an SSP through SSPI, which provides functions for enumerating the security packages available on a system, selecting a package, and using that package to obtain an authenticated connection.</span></span>

<span data-ttu-id="8eff4-115">SSPI 中的方法是一般常式，開發人員可以在不知道特定 [*安全性通訊協定*](../secgloss/s-gly.md)的詳細資料的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="8eff4-115">The methods in SSPI are generic routines that developers can use without knowing the details of a particular [*security protocol*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="8eff4-116">例如，當用戶端/伺服器連接通過驗證時：</span><span class="sxs-lookup"><span data-stu-id="8eff4-116">For example, when a client/server connection is authenticated:</span></span>

1.  <span data-ttu-id="8eff4-117">用戶端上的應用程式會使用 SSPI 函式 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)將 [*認證*](../secgloss/c-gly.md)傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="8eff4-117">The application on the client side of the connection sends [*credentials*](../secgloss/c-gly.md) to the server using the SSPI function [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
2.  <span data-ttu-id="8eff4-118">連接之伺服器端上的應用程式會使用 SSPI 函式 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)來回應。</span><span class="sxs-lookup"><span data-stu-id="8eff4-118">The application on the server side of the connection responds with the SSPI function [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span>
3.  <span data-ttu-id="8eff4-119">連接經過驗證之後，伺服器上的 LSA 會使用來自用戶端的資訊來建立 [*存取權杖*](../secgloss/a-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="8eff4-119">After the connection has been authenticated, the LSA on the server uses information from the client to build an [*access token*](../secgloss/a-gly.md).</span></span>
4.  <span data-ttu-id="8eff4-120">伺服器接著可以呼叫 SSPI 函式 [**ImpersonateSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) ，將存取權杖附加至服務的模擬執行緒。</span><span class="sxs-lookup"><span data-stu-id="8eff4-120">The server can then call the SSPI function [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) to attach the access token to an impersonation thread for the service.</span></span>

## <a name="kerberos-security-package"></a><span data-ttu-id="8eff4-121">Kerberos 安全性套件</span><span class="sxs-lookup"><span data-stu-id="8eff4-121">Kerberos Security Package</span></span>

<span data-ttu-id="8eff4-122">Kerberos [*安全性套件*](../secgloss/s-gly.md) 是以 [*kerberos 驗證通訊協定*](../secgloss/k-gly.md)為基礎。</span><span class="sxs-lookup"><span data-stu-id="8eff4-122">The Kerberos [*security package*](../secgloss/s-gly.md) is based on the [*Kerberos authentication protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="8eff4-123">如果使用 Kerberos 通訊協定來驗證用戶端/伺服器連接， [**InitializeSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 會產生 GSSAPI 訊息，其中包含 \_ 來自用戶端的 KRB AP 要求 \_ 訊息。</span><span class="sxs-lookup"><span data-stu-id="8eff4-123">If the Kerberos protocol is being used to authenticate a client/server connection, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) generates a GSSAPI message that includes a KRB\_AP\_REQ message from the client.</span></span> <span data-ttu-id="8eff4-124">[**AcceptSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 接著會產生 GSSAPI 訊息，其中包含 \_ 來自伺服器的 KRB AP \_ REP 訊息。</span><span class="sxs-lookup"><span data-stu-id="8eff4-124">[**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) then generates a GSSAPI message that includes a KRB\_AP\_REP message from the server.</span></span>

<span data-ttu-id="8eff4-125">如需在 Kerberos 通訊協定的執行幕後進行之步驟的背景資訊，請參閱 [Microsoft Kerberos](microsoft-kerberos.md)。</span><span class="sxs-lookup"><span data-stu-id="8eff4-125">For background information on the steps that take place behind the scenes in the implementation of a Kerberos protocol, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

<span data-ttu-id="8eff4-126">所有分散式服務都會使用 SSPI 來存取 Kerberos 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8eff4-126">All distributed services use SSPI to access the Kerberos protocol.</span></span> <span data-ttu-id="8eff4-127">Kerberos 通訊協定用於驗證的方式部分清單包括：</span><span class="sxs-lookup"><span data-stu-id="8eff4-127">A partial list of the ways in which the Kerberos protocol is used for authentication includes:</span></span>

-   <span data-ttu-id="8eff4-128">列印多工緩衝處理器服務</span><span class="sxs-lookup"><span data-stu-id="8eff4-128">Print spooler services</span></span>
-   <span data-ttu-id="8eff4-129">CIFS/SMB 遠端檔案存取</span><span class="sxs-lookup"><span data-stu-id="8eff4-129">CIFS/SMB remote file access</span></span>
-   <span data-ttu-id="8eff4-130">Active Directory 的 [*LDAP*](../secgloss/l-gly.md)查詢</span><span class="sxs-lookup"><span data-stu-id="8eff4-130">[*LDAP*](../secgloss/l-gly.md) queries to the Active Directory</span></span>
-   <span data-ttu-id="8eff4-131">分散式檔案系統管理與參考</span><span class="sxs-lookup"><span data-stu-id="8eff4-131">Distributed file system management and referrals</span></span>
-   <span data-ttu-id="8eff4-132">IPsec 主機對主機安全性授權單位驗證</span><span class="sxs-lookup"><span data-stu-id="8eff4-132">IPsec host-to-host security authority authentication</span></span>
-   <span data-ttu-id="8eff4-133">網路服務品質的保留要求</span><span class="sxs-lookup"><span data-stu-id="8eff4-133">Reservation requests for network Quality of Service</span></span>
-   <span data-ttu-id="8eff4-134">Internet Information Services 的內部網路驗證</span><span class="sxs-lookup"><span data-stu-id="8eff4-134">Intranet authentication to Internet Information Services</span></span>
-   <span data-ttu-id="8eff4-135">使用已驗證 RPC 的遠端伺服器或工作站管理</span><span class="sxs-lookup"><span data-stu-id="8eff4-135">Remote server or workstation management using authenticated RPC</span></span>
-   <span data-ttu-id="8eff4-136">網域使用者和電腦的憑證服務 [*憑證要求*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="8eff4-136">[*Certificate requests*](../secgloss/c-gly.md) to Certificate Services for domain users and computers</span></span>

## <a name="ntlm-security-package"></a><span data-ttu-id="8eff4-137">NTLM 安全性封裝</span><span class="sxs-lookup"><span data-stu-id="8eff4-137">NTLM Security Package</span></span>

<span data-ttu-id="8eff4-138">NTLM 安全性封裝是以 NTLM 驗證通訊協定為基礎。</span><span class="sxs-lookup"><span data-stu-id="8eff4-138">The NTLM security package is based on the NTLM authentication protocol.</span></span>

 

 
