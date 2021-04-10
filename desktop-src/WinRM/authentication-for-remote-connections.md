---
title: 遠端連線的驗證
description: Windows 遠端管理藉由支援數種標準的驗證方法和訊息加密，來維護電腦間通訊的安全性。
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e9aa125f2ccf5d8c224eee645a6dba1ec2fd96e
ms.sourcegitcommit: 25c6d442ab55cbf0e065398a006b1d409349fffd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2020
ms.locfileid: "104023179"
---
# <a name="authentication-for-remote-connections"></a><span data-ttu-id="e4a01-103">遠端連線的驗證</span><span class="sxs-lookup"><span data-stu-id="e4a01-103">Authentication for Remote Connections</span></span>

<span data-ttu-id="e4a01-104">Windows 遠端管理藉由支援數種標準的驗證方法和訊息加密，來維護電腦間通訊的安全性。</span><span class="sxs-lookup"><span data-stu-id="e4a01-104">Windows Remote Management maintains security for communication between computers by supporting several standard methods of authentication and message encryption.</span></span>

## <a name="default-group-access"></a><span data-ttu-id="e4a01-105">預設群組存取</span><span class="sxs-lookup"><span data-stu-id="e4a01-105">Default Group Access</span></span>

<span data-ttu-id="e4a01-106">在安裝期間，WinRM 會建立本地 **組 \_ \_ WinRMRemoteWMIUsers**。</span><span class="sxs-lookup"><span data-stu-id="e4a01-106">During setup, WinRM creates the local group **WinRMRemoteWMIUsers\_\_**.</span></span> <span data-ttu-id="e4a01-107">WinRM 接著會限制遠端存取不屬於本機系統管理群組或 **WinRMRemoteWMIUsers \_ \_** 群組成員的任何使用者。</span><span class="sxs-lookup"><span data-stu-id="e4a01-107">WinRM then restricts remote access to any user that is not a member of either the local administration group or the **WinRMRemoteWMIUsers\_\_** group.</span></span> <span data-ttu-id="e4a01-108">您可以在命令提示字元中輸入 **net localgroup WinRMRemoteWMIUsers \_ \_ /add <domain> \\ <username>** ，將本機使用者、網域使用者或網域群組新增至 **WinRMRemoteWMIUsers \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="e4a01-108">You can add a local user, domain user, or domain group to **WinRMRemoteWMIUsers\_\_** by typing **net localgroup WinRMRemoteWMIUsers\_\_ /add <domain>\\<username>** at the command prompt.</span></span> <span data-ttu-id="e4a01-109">（選擇性）您可以使用群組原則將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="e4a01-109">Optionally, you can use the Group Policy to add a user to the group.</span></span>

## <a name="default-authentication-settings"></a><span data-ttu-id="e4a01-110">預設驗證設定</span><span class="sxs-lookup"><span data-stu-id="e4a01-110">Default Authentication Settings</span></span>

<span data-ttu-id="e4a01-111">預設認證（使用者名稱和密碼）是執行腳本之登入使用者帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="e4a01-111">The default credentials, user name, and password, are the credentials for the logged-on user account that runs the script.</span></span>

<span data-ttu-id="e4a01-112">**若要變更為遠端電腦上的另一個帳戶**</span><span class="sxs-lookup"><span data-stu-id="e4a01-112">**To change to another account on a remote computer**</span></span>

1.  <span data-ttu-id="e4a01-113">在 [**ConnectionOptions**](connectionoptions.md) 或 [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) 物件中指定認證，並將其提供給 [**CreateSession**](wsman-createsession.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="e4a01-113">Specify the credentials in a [**ConnectionOptions**](connectionoptions.md) or [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) object and supply that to the [**CreateSession**](wsman-createsession.md) call.</span></span>
2.  <span data-ttu-id="e4a01-114">在 [**CreateSession**](wsman-createsession.md)呼叫的 *旗標* 參數中設定 **WSManFlagCredUserNamePassword** 。</span><span class="sxs-lookup"><span data-stu-id="e4a01-114">Set the **WSManFlagCredUserNamePassword** in the *flags* parameter in the [**CreateSession**](wsman-createsession.md) call.</span></span>

<span data-ttu-id="e4a01-115">以下清單包含在預設認證下執行腳本或應用程式時所發生的情況：</span><span class="sxs-lookup"><span data-stu-id="e4a01-115">The following list contains a list of what occurs when a script or application runs under the default credentials:</span></span>

-   <span data-ttu-id="e4a01-116">當用戶端位於網域中，而遠端目的地字串不是下列其中一項時， [*Kerberos*](windows-remote-management-glossary.md)是驗證的預設方法： localhost、127.0.0.1 或 \[ ：： 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="e4a01-116">[*Kerberos*](windows-remote-management-glossary.md) is the default method of authentication when the client is in a domain and the remote destination string is not one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>
-   <span data-ttu-id="e4a01-117">當用戶端不在網域中，但遠端目的地字串為下列其中一項時， [*Negotiate*](windows-remote-management-glossary.md)即為預設方法： localhost、127.0.0.1 或 \[ ：： 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="e4a01-117">[*Negotiate*](windows-remote-management-glossary.md) is the default method when the client is not in a domain, but the remote destination string is one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>

<span data-ttu-id="e4a01-118">如果您以 [**ConnectionOptions**](connectionoptions.md) 物件提供明確的認證，Negotiate 即為預設方法。</span><span class="sxs-lookup"><span data-stu-id="e4a01-118">If you supply explicit credentials with a [**ConnectionOptions**](connectionoptions.md) object, Negotiate is the default method.</span></span> <span data-ttu-id="e4a01-119">「協商驗證」會根據電腦是否位於網域或工作組，判斷進行中的驗證方法是否為 Kerberos 或 NTLM。</span><span class="sxs-lookup"><span data-stu-id="e4a01-119">Negotiate authentication determines whether the ongoing authentication method is Kerberos or NTLM, depending on whether the computers are in a domain or workgroup.</span></span> <span data-ttu-id="e4a01-120">如果使用本機帳戶連接到遠端目的電腦，則帳戶的前面應該會加上電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="e4a01-120">If connecting to a remote target computer using a local account, then the account should be prefixed with the computer name.</span></span> <span data-ttu-id="e4a01-121">例如，myComputer \\ myUsername。</span><span class="sxs-lookup"><span data-stu-id="e4a01-121">For example, myComputer\\myUsername.</span></span>

<span data-ttu-id="e4a01-122">如果您指定 Negotiate、摘要式或基本驗證，但無法提供 [**ConnectionOptions**](connectionoptions.md) 物件，則您會收到錯誤，指出需要明確的認證。</span><span class="sxs-lookup"><span data-stu-id="e4a01-122">If you specify Negotiate, Digest, or Basic authentication and fail to supply a [**ConnectionOptions**](connectionoptions.md) object, then you will receive an error indicating that explicit credentials are required.</span></span> <span data-ttu-id="e4a01-123">如果 HTTPS 不是傳輸，則必須在信任的主機電腦清單中設定目標遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e4a01-123">If HTTPS is not the transport, then the target remote computer must be configured in the list of trusted host computers.</span></span>

<span data-ttu-id="e4a01-124">如需有關在預設設定中啟用之驗證類型的詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="e4a01-124">For more information about the authentication types that are enabled in the default configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="basic-authentication"></a><span data-ttu-id="e4a01-125">基本驗證</span><span class="sxs-lookup"><span data-stu-id="e4a01-125">Basic Authentication</span></span>

<span data-ttu-id="e4a01-126">若要在 [**CreateSession**](wsman-createsession.md)的呼叫中明確建立 [*基本*](windows-remote-management-glossary.md)身份驗證，請在 *flags* 參數中設定 **WSManFlagUseBasic** 和 **WSManFlagCredUserNamePassword** 旗標。</span><span class="sxs-lookup"><span data-stu-id="e4a01-126">To explicitly establish [*Basic*](windows-remote-management-glossary.md) authentication in the call to [**WSMan.CreateSession**](wsman-createsession.md), set the **WSManFlagUseBasic** and **WSManFlagCredUserNamePassword** flags in the *flags* parameter.</span></span> <span data-ttu-id="e4a01-127">在 WinRM 用戶端和 WinRM 伺服器的預設設定中，已停用基本驗證。</span><span class="sxs-lookup"><span data-stu-id="e4a01-127">Basic authentication is disabled in the default configuration settings for both the WinRM client and the WinRM server.</span></span>

## <a name="digest-authentication"></a><span data-ttu-id="e4a01-128">摘要式驗證</span><span class="sxs-lookup"><span data-stu-id="e4a01-128">Digest Authentication</span></span>

<span data-ttu-id="e4a01-129">若要在 [**CreateSession**](wsman-createsession.md)的呼叫中明確建立 [*摘要式*](windows-remote-management-glossary.md)驗證，請在 Flags 參數中設定 **WSManFlagUseDigest** 旗 *標*。</span><span class="sxs-lookup"><span data-stu-id="e4a01-129">To explicitly establish [*Digest*](windows-remote-management-glossary.md) authentication in the call to [**WSMan.CreateSession**](wsman-createsession.md), set the **WSManFlagUseDigest** flag in the *flags* parameter.</span></span> <span data-ttu-id="e4a01-130">不支援摘要。</span><span class="sxs-lookup"><span data-stu-id="e4a01-130">Digest is not supported.</span></span> <span data-ttu-id="e4a01-131">它無法針對 WinRM 伺服器元件進行設定。</span><span class="sxs-lookup"><span data-stu-id="e4a01-131">It cannot be configured, for the WinRM server component.</span></span>

## <a name="negotiate-authentication"></a><span data-ttu-id="e4a01-132">協商驗證</span><span class="sxs-lookup"><span data-stu-id="e4a01-132">Negotiate Authentication</span></span>

<span data-ttu-id="e4a01-133">若要明確建立 [*Negotiate*](windows-remote-management-glossary.md) 驗證（也稱為「Windows 整合式驗證」），請在 [**CreateSession**](wsman-createsession.md)的呼叫中，設定 Flags 參數中的 **WSManFlagUseNegotiate** 旗 *標* 。</span><span class="sxs-lookup"><span data-stu-id="e4a01-133">To explicitly establish [*Negotiate*](windows-remote-management-glossary.md) authentication, also known as Windows Integrated Authentication, in the call to [**WSMan.CreateSession**](wsman-createsession.md), set the **WSManFlagUseNegotiate** flag in the *flags* parameter.</span></span>

<span data-ttu-id="e4a01-134">[ (UAC) 的使用者帳戶控制 ](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) 會影響 WinRM 服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="e4a01-134">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="e4a01-135">在工作組中使用「協商驗證」時，只有內建的系統管理員帳戶可以存取該服務。</span><span class="sxs-lookup"><span data-stu-id="e4a01-135">When Negotiate authentication is used in a workgroup, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="e4a01-136">若要允許 Administrators 群組中的所有帳戶存取服務，請設定下列登錄值：</span><span class="sxs-lookup"><span data-stu-id="e4a01-136">To allow all accounts in the Administrators group to access the service, set the following registry value:</span></span>

<span data-ttu-id="e4a01-137">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **原則** \\ **系統** \\ **LocalAccountTokenFilterPolicy** = 1</span><span class="sxs-lookup"><span data-stu-id="e4a01-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**System**\\**LocalAccountTokenFilterPolicy** = 1</span></span>

## <a name="kerberos-authentication"></a><span data-ttu-id="e4a01-138">Kerberos 驗證</span><span class="sxs-lookup"><span data-stu-id="e4a01-138">Kerberos Authentication</span></span>

<span data-ttu-id="e4a01-139">若要在 [**CreateSession**](wsman-createsession.md)的呼叫中明確建立 [*Kerberos*](windows-remote-management-glossary.md)驗證，請在 Flags 參數中設定 **WSManFlagUseKerberos** 旗 *標*。</span><span class="sxs-lookup"><span data-stu-id="e4a01-139">To explicitly establish [*Kerberos*](windows-remote-management-glossary.md) authentication in the call to [**WSMan.CreateSession**](wsman-createsession.md), set the **WSManFlagUseKerberos** flag in the *flags* parameter.</span></span> <span data-ttu-id="e4a01-140">用戶端和伺服器電腦都必須加入網域。</span><span class="sxs-lookup"><span data-stu-id="e4a01-140">Both the client and the server computers must be joined to a domain.</span></span> <span data-ttu-id="e4a01-141">如果您使用 Kerberos 作為驗證方法，則不能在 [**CreateSession**](wsman-createsession.md) 或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)的呼叫中使用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e4a01-141">If you use Kerberos as the authentication method, you cannot use an IP address in the call to [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).</span></span>

## <a name="client-certificate-based-authentication"></a><span data-ttu-id="e4a01-142">以用戶端憑證為基礎的驗證</span><span class="sxs-lookup"><span data-stu-id="e4a01-142">Client Certificate-based Authentication</span></span>

<span data-ttu-id="e4a01-143">若要在 [**CreateSession**](wsman-createsession.md)的呼叫中建立用戶端憑證型驗證，請在 flags 參數中設定 **WSManFlagUseClientCertificate** 旗 *標* 。</span><span class="sxs-lookup"><span data-stu-id="e4a01-143">To establish client certificate-based authentication in the call to [**WSMan.CreateSession**](wsman-createsession.md), set the **WSManFlagUseClientCertificate** flag in the *flags* parameter.</span></span>

<span data-ttu-id="e4a01-144">您必須先使用 Winrm 命令列工具，在用戶端和服務上啟用憑證驗證。</span><span class="sxs-lookup"><span data-stu-id="e4a01-144">You must first enable certificate authentication on both the client and service by using the Winrm command line tool.</span></span> <span data-ttu-id="e4a01-145">如需詳細資訊，請參閱 [啟用驗證選項](#enabling-or-disabling-authentication-options)。</span><span class="sxs-lookup"><span data-stu-id="e4a01-145">For more information, see [Enabling Authentication Options](#enabling-or-disabling-authentication-options).</span></span> <span data-ttu-id="e4a01-146">您也必須在 WinRM 伺服器電腦上的 CertMapping 資料表中建立專案。</span><span class="sxs-lookup"><span data-stu-id="e4a01-146">You must also create an entry in the CertMapping table on the WinRM server computer.</span></span> <span data-ttu-id="e4a01-147">這會建立一或多個憑證與本機帳戶之間的對應。</span><span class="sxs-lookup"><span data-stu-id="e4a01-147">This establishes a mapping between one or more certificates and a local account.</span></span> <span data-ttu-id="e4a01-148">使用憑證進行驗證和授權之後，會使用對應的本機帳戶進行 WinRM 服務所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="e4a01-148">After the certificate has been used for authentication and authorization, the corresponding local account is used for operations performed by the WinRM service.</span></span>

<span data-ttu-id="e4a01-149">您可以針對特定的資源 URI 來建立對應。</span><span class="sxs-lookup"><span data-stu-id="e4a01-149">The mapping can be created for a specific resource URI.</span></span> <span data-ttu-id="e4a01-150">若要深入瞭解，包括如何建立 CertMapping 資料表專案，請在命令提示字元中輸入 **winrm help CertMapping** 。</span><span class="sxs-lookup"><span data-stu-id="e4a01-150">To learn more, including how to create a CertMapping table entry, type **winrm help certmapping** at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="e4a01-151">WinRM 在此內容中可用的憑證大小上限為16KB。</span><span class="sxs-lookup"><span data-stu-id="e4a01-151">The maximum size certificate usable by WinRM in this context is 16KB.</span></span>

 

## <a name="enabling-or-disabling-authentication-options"></a><span data-ttu-id="e4a01-152">啟用或停用驗證選項</span><span class="sxs-lookup"><span data-stu-id="e4a01-152">Enabling or Disabling Authentication Options</span></span>

<span data-ttu-id="e4a01-153">系統安裝時的預設驗證選項是 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="e4a01-153">The default authentication option at system installation is Kerberos.</span></span> <span data-ttu-id="e4a01-154">如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="e4a01-154">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="e4a01-155">如果您的腳本或應用程式需要未啟用的特定驗證方法，您必須變更設定，以啟用這種類型的驗證。</span><span class="sxs-lookup"><span data-stu-id="e4a01-155">If your script or application requires a specific authentication method that is not enabled, you must change the configuration to enable this type of authentication.</span></span> <span data-ttu-id="e4a01-156">您可以使用 **Winrm** 命令列工具，或透過 **Windows 遠端管理群組原則物件** 的群組原則來進行這種變更。</span><span class="sxs-lookup"><span data-stu-id="e4a01-156">This change can be made using the **Winrm** command-line tool or through Group Policy for the **Windows Remote Management Group Policy Object**.</span></span> <span data-ttu-id="e4a01-157">您也可以選擇停用某些驗證方法。</span><span class="sxs-lookup"><span data-stu-id="e4a01-157">You may also choose to disable certain methods of authentication.</span></span>

<span data-ttu-id="e4a01-158">**若要使用 Winrm 工具啟用或停用驗證**</span><span class="sxs-lookup"><span data-stu-id="e4a01-158">**To enable or disable authentication with the Winrm tool**</span></span>

1.  <span data-ttu-id="e4a01-159">若要設定 WinRM 用戶端的設定，請使用 **Winrm set** 命令並指定用戶端。</span><span class="sxs-lookup"><span data-stu-id="e4a01-159">To set the configuration for the WinRM client, use the **Winrm Set** command and specify the client.</span></span> <span data-ttu-id="e4a01-160">例如，下列命令會停用用戶端的摘要式驗證。</span><span class="sxs-lookup"><span data-stu-id="e4a01-160">For example, the following command disables digest authentication for the client.</span></span>

    <span data-ttu-id="e4a01-161">**winrm set winrm/config/client/auth @ {Digest = "false"}**</span><span class="sxs-lookup"><span data-stu-id="e4a01-161">**winrm set winrm/config/client/auth @{Digest="false"}**</span></span>

2.  <span data-ttu-id="e4a01-162">若要設定 WinRM 伺服器的設定，請使用 **Winrm set** 命令並指定服務。</span><span class="sxs-lookup"><span data-stu-id="e4a01-162">To set the configuration for the WinRM server, use the **Winrm Set** command and specify the service.</span></span> <span data-ttu-id="e4a01-163">例如，下列命令會啟用服務的 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="e4a01-163">For example, the following command enables Kerberos authentication for the service.</span></span>

    <span data-ttu-id="e4a01-164">**winrm set winrm/config/service/auth @ {Kerberos = "true"}**</span><span class="sxs-lookup"><span data-stu-id="e4a01-164">**winrm set winrm/config/service/auth @{Kerberos="true"}**</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4a01-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4a01-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4a01-166">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="e4a01-166">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="e4a01-167">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="e4a01-167">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="e4a01-168">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="e4a01-168">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> </dl>

 

 




