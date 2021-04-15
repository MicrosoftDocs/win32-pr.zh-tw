---
title: WinRM 中的多重躍點支援
description: Windows 遠端管理 (WinRM) 支援跨多部遠端電腦委派使用者認證。
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22c3d66e8605e932fe15b812f92d51350da2d69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467989"
---
# <a name="multi-hop-support-in-winrm"></a><span data-ttu-id="7058c-103">WinRM 中的多重躍點支援</span><span class="sxs-lookup"><span data-stu-id="7058c-103">Multi-Hop Support in WinRM</span></span>

<span data-ttu-id="7058c-104">Windows 遠端管理 (WinRM) 支援跨多部遠端電腦委派使用者認證。</span><span class="sxs-lookup"><span data-stu-id="7058c-104">Windows Remote Management (WinRM) supports the delegation of user credentials across multiple remote computers.</span></span> <span data-ttu-id="7058c-105">多重躍點支援功能現在可使用 (CredSSP) 的認證安全性服務提供者進行驗證。</span><span class="sxs-lookup"><span data-stu-id="7058c-105">The multi-hop support functionality can now use Credential Security Service Provider (CredSSP) for authentication.</span></span> <span data-ttu-id="7058c-106">CredSSP 可讓應用程式將使用者的認證從用戶端電腦委派至目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="7058c-106">CredSSP enables an application to delegate the user's credentials from the client computer to the target server.</span></span>

<span data-ttu-id="7058c-107">CredSSP 驗證適用于無法使用 Kerberos 委派的環境。</span><span class="sxs-lookup"><span data-stu-id="7058c-107">CredSSP authentication is intended for environments where Kerberos delegation cannot be used.</span></span> <span data-ttu-id="7058c-108">已新增 CredSSP 的支援，可讓使用者連線到遠端伺服器，而且能夠存取第二躍點的電腦，例如檔案共用。</span><span class="sxs-lookup"><span data-stu-id="7058c-108">Support for CredSSP was added to allow a user to connect to a remote server and have the ability to access a second-hop machine, such as a file share.</span></span>

<span data-ttu-id="7058c-109">如需 CredSSP 的詳細資訊，請參閱 [KB 951608](https://support.microsoft.com/kb/951608)。</span><span class="sxs-lookup"><span data-stu-id="7058c-109">For more information about CredSSP, see [KB 951608](https://support.microsoft.com/kb/951608).</span></span>

> [!Note]  
> <span data-ttu-id="7058c-110">WinRM 用戶端和伺服器將僅支援使用明確認證的 CredSSP 驗證。</span><span class="sxs-lookup"><span data-stu-id="7058c-110">WinRM clients and servers will support CredSSP authentication only with explicit credentials.</span></span>

 

## <a name="multi-hop-support-configuration-setup-and-details"></a><span data-ttu-id="7058c-111">多重躍點支援設定和詳細資料</span><span class="sxs-lookup"><span data-stu-id="7058c-111">Multi-Hop Support Configuration Setup and Details</span></span>

<span data-ttu-id="7058c-112">有多個機制可設定 WinRM 設定。</span><span class="sxs-lookup"><span data-stu-id="7058c-112">There are multiple mechanisms for configuring WinRM settings.</span></span> <span data-ttu-id="7058c-113">在下列程式中，會使用 [ **winrm** 公用程式] 和 [群組原則編輯器] (**gpedit.msc**) 。</span><span class="sxs-lookup"><span data-stu-id="7058c-113">In the following procedure, the **winrm** utility and Group Policy editor (**GPEdit.msc**) are used.</span></span> <span data-ttu-id="7058c-114">您也可以使用 Windows PowerShell，針對 WinRM 啟用 CredSSP。</span><span class="sxs-lookup"><span data-stu-id="7058c-114">CredSSP can also be enabled for WinRM by using Windows PowerShell.</span></span> <span data-ttu-id="7058c-115">如需詳細的設定資訊和使用範例，請參閱 [WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true)、 [WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)和 [Disable WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Windows PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7058c-115">See the [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true), and [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Windows PowerShell cmdlets for detailed configuration information and usage examples.</span></span>

<span data-ttu-id="7058c-116">您必須在用戶端設定和遠端電腦上的服務設定中啟用 CredSSP 委派。</span><span class="sxs-lookup"><span data-stu-id="7058c-116">CredSSP delegation must be enabled in the client settings and in the service settings on the remote computer.</span></span> <span data-ttu-id="7058c-117">此外，使用 CredSSP 需要在伺服器上設定 HTTP [*或 HTTPS 接聽*](windows-remote-management-glossary.md) 程式。</span><span class="sxs-lookup"><span data-stu-id="7058c-117">In addition, using CredSSP requires setting up an HTTP or HTTPS [*listener*](windows-remote-management-glossary.md) on the server.</span></span>

<span data-ttu-id="7058c-118">**若要使用適用于 WinRM 的 CredSSP 驗證設定多重躍點支援**</span><span class="sxs-lookup"><span data-stu-id="7058c-118">**To configure multi-hop support using CredSSP authentication for WinRM**</span></span>

1.  <span data-ttu-id="7058c-119">您必須在用戶端設定中啟用 CredSSP。</span><span class="sxs-lookup"><span data-stu-id="7058c-119">CredSSP must be enabled in the client configuration settings.</span></span> <span data-ttu-id="7058c-120">您可以手動或透過群組原則設定來啟用此旗標。</span><span class="sxs-lookup"><span data-stu-id="7058c-120">This flag can be enabled manually or through a Group Policy setting.</span></span> <span data-ttu-id="7058c-121">預設值是 **False**。</span><span class="sxs-lookup"><span data-stu-id="7058c-121">The default setting is **False**.</span></span> <span data-ttu-id="7058c-122">**允許 CredSSP 驗證** 原則位於下列路徑：電腦設定系統 \\ 管理範本 \\ Windows 元件 \\ Windows 遠端管理 (winrm) \\ winrm 用戶端。</span><span class="sxs-lookup"><span data-stu-id="7058c-122">The **Allow CredSSP authentication** policy is located at the following path: Computer Configuration\\Administrative template\\Windows Components\\Windows Remote Management (WinRM)\\WinRM Client.</span></span>

    <span data-ttu-id="7058c-123">下列命令示範如何使用 winrm 公用程式在 WinRM 用戶端上啟用 CredSSP：</span><span class="sxs-lookup"><span data-stu-id="7058c-123">The following command demonstrates how to use the winrm utility to enable CredSSP on the WinRM client:</span></span>

    <span data-ttu-id="7058c-124">**winrm set winrm/config/client/auth @ {CredSSP = "true"}**</span><span class="sxs-lookup"><span data-stu-id="7058c-124">**winrm set winrm/config/client/auth @{CredSSP="true"}**</span></span>

2.  <span data-ttu-id="7058c-125">您必須在 WinRM 服務設定中啟用 CredSSP。</span><span class="sxs-lookup"><span data-stu-id="7058c-125">CredSSP must be enabled in the WinRM service configuration settings.</span></span> <span data-ttu-id="7058c-126">您可以手動或透過群組原則設定來啟用此旗標。</span><span class="sxs-lookup"><span data-stu-id="7058c-126">This flag can be enabled manually or through a Group Policy setting.</span></span> <span data-ttu-id="7058c-127">預設值是 **False**。</span><span class="sxs-lookup"><span data-stu-id="7058c-127">The default setting is **False**.</span></span> <span data-ttu-id="7058c-128">**允許 CredSSP 驗證** 原則位於下列路徑：電腦設定系統 \\ 管理範本 \\ Windows 元件 \\ Windows 遠端管理 (winrm) \\ winrm 服務。</span><span class="sxs-lookup"><span data-stu-id="7058c-128">The **Allow CredSSP authentication** policy is located at the following path: Computer Configuration\\Administrative template\\Windows Components\\Windows Remote Management (WinRM)\\WinRM Service.</span></span>

    <span data-ttu-id="7058c-129">下列命令示範如何使用 winrm 公用程式在 WinRM 服務上啟用 CredSSP：</span><span class="sxs-lookup"><span data-stu-id="7058c-129">The following command demonstrates how to use the winrm utility to enable CredSSP on the WinRM service:</span></span>

    <span data-ttu-id="7058c-130">**winrm set winrm/config/service/auth @ {CredSSP = "true"}**</span><span class="sxs-lookup"><span data-stu-id="7058c-130">**winrm set winrm/config/service/auth @{CredSSP="true"}**</span></span>

3.  <span data-ttu-id="7058c-131">必須在 WinRM 用戶端上啟用 [允許委派新認證 (**AllowFreshCredentials** ]) 原則設定，以及必須將具有 WSMAN 首碼 (SPN) 的服務主體名稱新增至原則。</span><span class="sxs-lookup"><span data-stu-id="7058c-131">The Allow Delegating Fresh Credentials (**AllowFreshCredentials**) policy setting must be enabled on the WinRM client, and a Service Principal Name (SPN) with the WSMAN prefix must be added to the policy.</span></span> <span data-ttu-id="7058c-132">SPN 代表可以委派使用者認證的目的電腦。</span><span class="sxs-lookup"><span data-stu-id="7058c-132">The SPN represents the target computer to which the user credentials can be delegated.</span></span> <span data-ttu-id="7058c-133">SPN 可以設定為一或多部電腦。</span><span class="sxs-lookup"><span data-stu-id="7058c-133">The SPN can be set to one or more computers.</span></span> <span data-ttu-id="7058c-134">下表包含 Spn 的有效格式範例。</span><span class="sxs-lookup"><span data-stu-id="7058c-134">The following table contains examples of valid formats for SPNs.</span></span>

    

    | <span data-ttu-id="7058c-135">SPN</span><span class="sxs-lookup"><span data-stu-id="7058c-135">SPN</span></span>                                       | <span data-ttu-id="7058c-136">Description</span><span class="sxs-lookup"><span data-stu-id="7058c-136">Description</span></span>                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="7058c-137">WSMAN/myComputer</span><span class="sxs-lookup"><span data-stu-id="7058c-137">WSMAN/myComputer.myDomain.com</span></span><br/>  | <span data-ttu-id="7058c-138">在 myComputer.myDomain.com 上執行的 WinRM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="7058c-138">WinRM server running on myComputer.myDomain.com.</span></span><br/>                         |
    | <span data-ttu-id="7058c-139">WSMAN/ \* . myDomain.com</span><span class="sxs-lookup"><span data-stu-id="7058c-139">WSMAN/\*.myDomain.com</span></span><br/>          | <span data-ttu-id="7058c-140">所有在 myDomain.com 中執行的 WinRM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="7058c-140">All WinRM servers running in myDomain.com.</span></span><br/>                               |
    | <span data-ttu-id="7058c-141">WSMAN/ \* . fabrikam.myDomain.com</span><span class="sxs-lookup"><span data-stu-id="7058c-141">WSMAN/\*.fabrikam.myDomain.com</span></span><br/> | <span data-ttu-id="7058c-142">所有在 fabrikam.myDomain.com 中的電腦上執行的 WinRM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="7058c-142">All WinRM servers running in on all computers in .fabrikam.myDomain.com.</span></span><br/> |

    

     

    <span data-ttu-id="7058c-143">如需設定群組原則的詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="7058c-143">For more information about setting Group Policies, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

    <span data-ttu-id="7058c-144">如需 **AllowFreshCredentials** 原則的詳細資訊，請參閱群組原則編輯器提供的原則描述和 [KB 951608](https://support.microsoft.com/kb/951608)。</span><span class="sxs-lookup"><span data-stu-id="7058c-144">For more information about the **AllowFreshCredentials** policy, see the policy description provided by the Group Policy editor and [KB 951608](https://support.microsoft.com/kb/951608).</span></span> <span data-ttu-id="7058c-145">**AllowFreshCredentials** 原則位於下列路徑： \\ 系統管理範本 \\ 系統認證委派的電腦配置 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7058c-145">The **AllowFreshCredentials** policy is located at the following path: Computer Configuration\\Administrative Templates\\System\\Credentials Delegation.</span></span>

4.  <span data-ttu-id="7058c-146">[*必須在*](windows-remote-management-glossary.md)伺服器上設定 HTTPS 或 HTTP 接聽程式。</span><span class="sxs-lookup"><span data-stu-id="7058c-146">An HTTPS or HTTP [*listener*](windows-remote-management-glossary.md) must be configured on the server.</span></span> <span data-ttu-id="7058c-147">用於設定 HTTPS 接聽程式的憑證指紋也用來設定 WinRM 服務設定下的 [CertificateThumbprint *]* 設定。</span><span class="sxs-lookup"><span data-stu-id="7058c-147">The certificate thumbprint used for configuring the HTTPS *listener* is also used to configure the CertificateThumbprint setting under the WinRM service settings.</span></span>

    <span data-ttu-id="7058c-148">下列命令示範如何使用 winrm 公用程式來 [*設定 HTTPS 接聽*](windows-remote-management-glossary.md)程式：</span><span class="sxs-lookup"><span data-stu-id="7058c-148">The following command demonstrates how to use the winrm utility to configure an HTTPS [*listener*](windows-remote-management-glossary.md):</span></span>

    <span data-ttu-id="7058c-149">**winrm quickconfig-傳輸： HTTPs**</span><span class="sxs-lookup"><span data-stu-id="7058c-149">**winrm quickconfig -transport:https**</span></span>

<span data-ttu-id="7058c-150">如果用戶端與伺服器之間無法進行 Kerberos 驗證，則使用者必須針對多重躍點支援設定下列其中一項設定：</span><span class="sxs-lookup"><span data-stu-id="7058c-150">If Kerberos authentication between the client and server is not possible, the user must configure one of the following settings for multi-hop support:</span></span>

-   <span data-ttu-id="7058c-151">為了提高安全性，使用者應該將 **CertificateThumbprint** 屬性新增至 WinRM 服務設定。</span><span class="sxs-lookup"><span data-stu-id="7058c-151">For better security, the user should add the **CertificateThumbprint** attribute to the WinRM service setting.</span></span> <span data-ttu-id="7058c-152">如果 WinRM 服務設定了 **CertificateThumbprint** 屬性，服務就會嘗試在本機電腦存放區中找出對應的憑證，並使用此憑證進行 CredSSP 驗證。</span><span class="sxs-lookup"><span data-stu-id="7058c-152">If the WinRM service is configured with a **CertificateThumbprint** attribute, the service attempts to locate the corresponding certificate in the Local Machine store and uses this certificate for the CredSSP authentication.</span></span> <span data-ttu-id="7058c-153">如果 WinRM 服務使用本機電腦存放區中的憑證來驗證服務器，則必須允許 Network Service 帳戶存取憑證的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7058c-153">If the WinRM service uses a certificate from the Local Machine store to authenticate the server, the Network Service account must be allowed access to the private key of the certificate.</span></span>

    > [!Note]  
    > <span data-ttu-id="7058c-154">如果未設定服務設定，則 WinRM 伺服器會使用在記憶體中建立的自我簽署憑證來加密傳送至用戶端的訊息。</span><span class="sxs-lookup"><span data-stu-id="7058c-154">If the service setting is not configured, the WinRM server uses a self-signed certificate that is created in memory to encrypt messages sent to the client.</span></span> <span data-ttu-id="7058c-155">不過，此憑證不會用來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="7058c-155">However, this certificate is not used for authentication.</span></span>

     

-   <span data-ttu-id="7058c-156">如果 Kerberos 驗證和憑證指紋皆無法使用，則使用者可以啟用 NTLM 驗證。</span><span class="sxs-lookup"><span data-stu-id="7058c-156">If neither Kerberos authentication nor certificate thumbprints are available, the user can enable NTLM authentication.</span></span> <span data-ttu-id="7058c-157">如果使用 NTLM 驗證，則必須啟用 [僅限 NTLM 伺服器驗證的全新認證] (**AllowFreshCredentialsWhenNTLMOnly**) 原則，而且必須將具有 WSMAN 首碼的 SPN 新增至原則。</span><span class="sxs-lookup"><span data-stu-id="7058c-157">If NTLM authentication is used, the Allow Fresh Credentials with NTLM-only Server Authentication (**AllowFreshCredentialsWhenNTLMOnly**) policy must be enabled, and an SPN with the WSMAN prefix must be added to the policy.</span></span> <span data-ttu-id="7058c-158">這項設定比 Kerberos 驗證和憑證指紋的安全性低，因為認證會傳送到未經驗證的伺服器。</span><span class="sxs-lookup"><span data-stu-id="7058c-158">This setting is less secure than both Kerberos authentication and certificate thumbprints, because credentials are sent to an unauthenticated server.</span></span>

    <span data-ttu-id="7058c-159">如需 **AllowFreshCredentialsWhenNTLMOnly** 原則的詳細資訊，請參閱群組原則編輯器提供的原則描述和 [KB 951608](https://support.microsoft.com/kb/951608)。</span><span class="sxs-lookup"><span data-stu-id="7058c-159">For more information about the **AllowFreshCredentialsWhenNTLMOnly** policy, see the policy description provided by the Group Policy editor and [KB 951608](https://support.microsoft.com/kb/951608).</span></span> <span data-ttu-id="7058c-160">**AllowFreshCredentialsWhenNTLMOnly** 原則位於下列路徑： \\ 系統管理範本 \\ 系統認證委派的電腦配置 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7058c-160">The **AllowFreshCredentialsWhenNTLMOnly** policy is located at the following path: Computer Configuration\\Administrative Templates\\System\\Credentials Delegation.</span></span>

## <a name="using-credssp-authentication-with-explicit-credentials"></a><span data-ttu-id="7058c-161">使用具有明確認證的 CredSSP 驗證</span><span class="sxs-lookup"><span data-stu-id="7058c-161">Using CredSSP Authentication with Explicit Credentials</span></span>

<span data-ttu-id="7058c-162">使用者可以透過 HTTP 和 HTTPS 指定明確的認證。</span><span class="sxs-lookup"><span data-stu-id="7058c-162">A user can specify explicit credentials over both HTTP and HTTPS.</span></span> <span data-ttu-id="7058c-163">下列命令示範如何使用 winrm 公用程式搭配透過 HTTPS 的明確認證來執行遠端操作：</span><span class="sxs-lookup"><span data-stu-id="7058c-163">The following command demonstrates how to use the winrm utility to perform a remote operation using CredSSP authentication with explicit credentials over HTTPS:</span></span>

<span data-ttu-id="7058c-164">**winrm 操作-遠端： https://myMachine -驗證： CredSSP-username： myUsername-password： myPassword**</span><span class="sxs-lookup"><span data-stu-id="7058c-164">**winrm OPERATION -remote:https://myMachine -authentication:CredSSP -username:myUsername -password:myPassword**</span></span>

 

