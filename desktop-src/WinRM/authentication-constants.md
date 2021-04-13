---
title: '驗證常數 (WSManDisp .h) '
description: 指定驗證方法，以及如何處理要求之 HTTPS 傳輸的憑證伺服器。
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509239"
---
# <a name="authentication-constants"></a><span data-ttu-id="b0a61-103">驗證常數</span><span class="sxs-lookup"><span data-stu-id="b0a61-103">Authentication Constants</span></span>

<span data-ttu-id="b0a61-104">驗證常數是 **\_ \_ WSManSessionFlags** 列舉中的常數，可指定驗證方法，以及如何處理要求之 HTTPS 傳輸的憑證伺服器。</span><span class="sxs-lookup"><span data-stu-id="b0a61-104">Authentication constants are constants in the **\_\_WSManSessionFlags** enumeration that specify the authentication method and how to handle certificate servers for HTTPS transport of requests.</span></span>

<span data-ttu-id="b0a61-105">在呼叫 [**CreateSession**](wsman-createsession.md)或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)連接至遠端電腦的呼叫中，*旗標* 參數中列出的一個或多個常數是必要的。</span><span class="sxs-lookup"><span data-stu-id="b0a61-105">One or more of the constants listed in the following list are required in the *flags* parameter in calls to [**WSMan.CreateSession**](wsman-createsession.md) or in [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span>

<dl> <dt>

<span data-ttu-id="b0a61-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span><span class="sxs-lookup"><span data-stu-id="b0a61-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-107">4096 (0x1000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-107">4096 (0x1000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-108">使用使用者名稱和密碼做為認證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-108">Use the user name and password as the credentials.</span></span> <span data-ttu-id="b0a61-109">當您建立 [**ConnectionOptions**](connectionoptions.md) 物件並提供使用者 [**名稱**](connectionoptions-username.md) 和 [**密碼**](connectionoptions-password.md)時，請設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="b0a61-109">Set this flag when you create a [**ConnectionOptions**](connectionoptions.md) object and supply [**Username**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md).</span></span> <span data-ttu-id="b0a61-110">認證可以是網域帳戶或本機電腦上的帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0a61-110">The credentials can be a domain account or an account on the local computer.</span></span> <span data-ttu-id="b0a61-111">根據預設，此帳戶必須是本機或遠端電腦上本機系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="b0a61-111">By default, the account must be a member of the local Administrators group on the local or remote computer.</span></span> <span data-ttu-id="b0a61-112">不過，您可以將 WinRM 服務設定為允許其他使用者。</span><span class="sxs-lookup"><span data-stu-id="b0a61-112">However, the WinRM service can be configured to allow other users.</span></span> <span data-ttu-id="b0a61-113">如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="b0a61-113">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="b0a61-114">當您指定 Negotiate 驗證的認證 (也稱為「 [*Windows 整合式驗證*](windows-remote-management-glossary.md)) 或 [*基本驗證*](windows-remote-management-glossary.md)時，您可以設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="b0a61-114">You can set this flag when you specify credentials for Negotiate authentication (also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md)) or for [*Basic authentication*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="b0a61-115">相關聯的腳本方法是 [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)，而 c + + 方法是 [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-115">The associated scripting method is [**WSMan.SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), and the C++ method is [**IWSManEx.SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span><span class="sxs-lookup"><span data-stu-id="b0a61-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-117">8192 (0x2000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-117">8192 (0x2000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-118">透過 HTTPS 連線時，用戶端並不會驗證伺服器憑證是否由信任的憑證授權單位單位簽署 (CA) 。</span><span class="sxs-lookup"><span data-stu-id="b0a61-118">When connecting over HTTPS, the client does not validate that the server certificate is signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="b0a61-119">只有在遠端電腦受其他方法信任時才使用此值，例如，如果遠端電腦是實體安全且隔離之網路的一部分，或在 WinRM 設定中將遠端電腦列為受信任的主機。</span><span class="sxs-lookup"><span data-stu-id="b0a61-119">Use this value only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="b0a61-120">相關聯的腳本方法是 [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)，而 c + + 方法是 [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-120">The associated scripting method is [**WSMan.SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span><span class="sxs-lookup"><span data-stu-id="b0a61-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-122">16384 (0x4000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-122">16384 (0x4000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-123">透過 HTTPS 連線時，用戶端將不會驗證伺服器憑證中 (CN) 的一般名稱是否符合連接字串中的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b0a61-123">When connecting over HTTPS, the client will not validate that the common name (CN) in the server certificate matches the computer name in the connection string.</span></span> <span data-ttu-id="b0a61-124">只有在遠端電腦受其他方法信任時才使用，例如，如果遠端電腦是實體安全且隔離之網路的一部分，或在 WinRM 設定中將遠端電腦列為受信任的主機。</span><span class="sxs-lookup"><span data-stu-id="b0a61-124">Use only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="b0a61-125">相關聯的腳本方法是 [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)，而 c + + 方法是 [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-125">The associated scripting method is [**WSMan.SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span><span class="sxs-lookup"><span data-stu-id="b0a61-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-127">32768 (0x8000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-127">32768 (0x8000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-128">不使用驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-128">Use no authentication.</span></span> <span data-ttu-id="b0a61-129">當測試與遠端電腦的連線時，請指定這個常數，以判斷是否已將執行 WS-Management 通訊協定的服務設定為接聽資料要求。</span><span class="sxs-lookup"><span data-stu-id="b0a61-129">Specify this constant when testing a connection to a remote computer to determine if a service that implements the WS-Management protocol is configured to listen for data requests.</span></span> <span data-ttu-id="b0a61-130">**WSManFlagUseNoAuthentication** 無法與任何其他 [**會話**](session.md) 常數合併。</span><span class="sxs-lookup"><span data-stu-id="b0a61-130">**WSManFlagUseNoAuthentication** cannot be combined with any other [**Session**](session.md) constant.</span></span> <span data-ttu-id="b0a61-131">相關聯的腳本方法是 [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)，而 c + + 方法是 [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-131">The associated scripting method is [**WSMan.SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), and the C++ method is [**WSManEx.SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span><span class="sxs-lookup"><span data-stu-id="b0a61-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-133">65536 (0x10000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-133">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-134">使用摘要式驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-134">Use Digest authentication.</span></span> <span data-ttu-id="b0a61-135">只有用戶端電腦可以起始摘要式驗證要求。</span><span class="sxs-lookup"><span data-stu-id="b0a61-135">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="b0a61-136">用戶端會將要求傳送至伺服器，以驗證並接收來自伺服器的權杖字串。</span><span class="sxs-lookup"><span data-stu-id="b0a61-136">The client sends a request to the server to authenticate and receives a token string from the server.</span></span> <span data-ttu-id="b0a61-137">然後，用戶端會傳送資源要求，包括使用者名稱和密碼的密碼編譯雜湊與權杖字串合併。</span><span class="sxs-lookup"><span data-stu-id="b0a61-137">The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="b0a61-138">HTTP 和 HTTPS 支援摘要式驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-138">Digest authentication is supported for HTTP and HTTPS.</span></span> <span data-ttu-id="b0a61-139">WinRM 用戶端腳本和應用程式可以指定摘要式驗證，但不能指定服務。</span><span class="sxs-lookup"><span data-stu-id="b0a61-139">WinRM client scripts and applications can specify Digest authentication, but not the service.</span></span>

<span data-ttu-id="b0a61-140">相關聯的腳本方法是 [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-140">The associated scripting method is [**WSMan.SessionFlagUseDigest**](wsman-sessionflagusedigest.md), and the C++ method is [**IWSManEx.SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span><span class="sxs-lookup"><span data-stu-id="b0a61-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-142">131072 (0x20000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-142">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-143">使用 Negotiate 驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-143">Use Negotiate authentication.</span></span> <span data-ttu-id="b0a61-144">用戶端會將要求傳送至伺服器以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-144">The client sends a request to the server to authenticate.</span></span> <span data-ttu-id="b0a61-145">伺服器會決定是要使用 Kerberos 或 NTLM。</span><span class="sxs-lookup"><span data-stu-id="b0a61-145">The server determines whether to use Kerberos or NTLM.</span></span> <span data-ttu-id="b0a61-146">選取 [Kerberos] 以驗證網域帳戶，並選取 [本機電腦帳戶的 NTLM]。</span><span class="sxs-lookup"><span data-stu-id="b0a61-146">Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="b0a61-147">使用者名稱應以網域 \\ 使用者名稱或 \\ 伺服器電腦上本機使用者的 servername 使用者名稱來指定。</span><span class="sxs-lookup"><span data-stu-id="b0a61-147">The user name should be specified in the form domain\\username for a domain user or servername\\username for a local user on a server computer.</span></span>

<span data-ttu-id="b0a61-148">[ (UAC) 的使用者帳戶控制 ](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) 會影響 WinRM 服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="b0a61-148">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="b0a61-149">當您在工作組或網域中使用「協商驗證」時，只有內建的系統管理員帳戶可以存取該服務。</span><span class="sxs-lookup"><span data-stu-id="b0a61-149">When Negotiate authentication is used in a workgroup or domain, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="b0a61-150">若要允許 Administrators 群組中的所有帳戶存取服務，請將下列登錄機碼設定為1： **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 原則 \\ 系統 \\ LocalAccountTokenFilterPolicy**。</span><span class="sxs-lookup"><span data-stu-id="b0a61-150">To allow all accounts in the Administrators group to access the service, set the following registry key to 1: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\system\\LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="b0a61-151">相關聯的腳本方法是 [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-151">The associated scripting method is [**WSMan.SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), and the C++ method is [**IWSManEx.SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span><span class="sxs-lookup"><span data-stu-id="b0a61-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-153">262144 (0x40000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-153">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-154">使用基本驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-154">Use Basic authentication.</span></span> <span data-ttu-id="b0a61-155">用戶端會以使用者名稱和密碼的形式呈現認證，直接在要求訊息中傳輸。</span><span class="sxs-lookup"><span data-stu-id="b0a61-155">The client presents credentials in the form of a user name and password, directly transmitted in the request message.</span></span> <span data-ttu-id="b0a61-156">您只能指定識別遠端電腦上本機系統管理員帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-156">You can specify only credentials that identify a local administrator account on the remote computer.</span></span>

<span data-ttu-id="b0a61-157">相關聯的腳本方法是 [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-157">The associated scripting method is [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md), and the C++ method is [**IWSManEx.SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span><span class="sxs-lookup"><span data-stu-id="b0a61-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-159">524288 (0x80000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-159">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-160">使用 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-160">Use Kerberos authentication.</span></span> <span data-ttu-id="b0a61-161">用戶端和伺服器會使用 Kerberos 票證相互驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-161">The client and server mutually authenticate using Kerberos tickets.</span></span>

<span data-ttu-id="b0a61-162">相關聯的腳本方法是 [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)，而 c + + 方法是 [**IWSManEx. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-162">The associated scripting method is [**WSMan.SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), and the C++ method is [**IWSManEx.WSMan.SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="b0a61-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-164">1048576 (0x100000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-164">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-165">不使用加密。</span><span class="sxs-lookup"><span data-stu-id="b0a61-165">Use no encryption.</span></span> <span data-ttu-id="b0a61-166">預設不允許未加密的流量，而且必須同時在用戶端和伺服器上啟用。</span><span class="sxs-lookup"><span data-stu-id="b0a61-166">Unencrypted traffic is not allowed by default and must be enabled on both the client and server.</span></span>

<span data-ttu-id="b0a61-167">相關聯的腳本方法是 [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)，而 c + + 方法是 [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-167">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="b0a61-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-169">2097152 (0x200000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-169">2097152 (0x200000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-170">使用以用戶端憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-170">Use client certificate-based authentication.</span></span>

<span data-ttu-id="b0a61-171">相關聯的腳本方法是 [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)，而 c + + 方法是 [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-171">The associated scripting method is [**WSMan.SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), and the C++ method is [**IWSManEx2.SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span><span class="sxs-lookup"><span data-stu-id="b0a61-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-173">16777216 (0x1000000) </span><span class="sxs-lookup"><span data-stu-id="b0a61-173">16777216 (0x1000000)</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-174">使用認證安全性支援提供者 (CredSSP) 驗證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-174">Use Credential Security Support Provider (CredSSP) authentication.</span></span>

<span data-ttu-id="b0a61-175">相關聯的腳本方法是 [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)，而 c + + 方法是 [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp)。</span><span class="sxs-lookup"><span data-stu-id="b0a61-175">The associated scripting method is [**WSMan.SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), and the C++ method is [**IWSManEx3.SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="b0a61-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="b0a61-177">0x2000000</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-178">請勿在驗證期間檢查憑證撤銷。</span><span class="sxs-lookup"><span data-stu-id="b0a61-178">Do not check for certificate revocation during authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span><span class="sxs-lookup"><span data-stu-id="b0a61-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-180">0x4000000</span><span class="sxs-lookup"><span data-stu-id="b0a61-180">0x4000000</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-181">允許隱含的認證。</span><span class="sxs-lookup"><span data-stu-id="b0a61-181">Allow implicit credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a61-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span><span class="sxs-lookup"><span data-stu-id="b0a61-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a61-183">0x8000000</span><span class="sxs-lookup"><span data-stu-id="b0a61-183">0x8000000</span></span>
</dt> <dt>



<span data-ttu-id="b0a61-184">使用安全通訊端層，啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="b0a61-184">Use Secure Socket Layer, enables HTTPS.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0a61-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0a61-185">Requirements</span></span>



| <span data-ttu-id="b0a61-186">需求</span><span class="sxs-lookup"><span data-stu-id="b0a61-186">Requirement</span></span> | <span data-ttu-id="b0a61-187">值</span><span class="sxs-lookup"><span data-stu-id="b0a61-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a61-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0a61-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a61-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0a61-189">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b0a61-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0a61-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a61-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0a61-191">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b0a61-192">標頭</span><span class="sxs-lookup"><span data-stu-id="b0a61-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0a61-193"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0a61-193"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0a61-194">Idl</span><span class="sxs-lookup"><span data-stu-id="b0a61-194">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0a61-195"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0a61-195"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0a61-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0a61-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a61-197">會話常數</span><span class="sxs-lookup"><span data-stu-id="b0a61-197">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

 





