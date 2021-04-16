---
description: 連接至遠端電腦上的 WMI 命名空間，可能需要您變更 Windows 防火牆、使用者帳戶控制 (UAC) 、DCOM 或通用訊息模型物件管理員的設定， (CIMOM) 。
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: 設定遠端 WMI 連接
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513072"
---
# <a name="setting-up-a-remote-wmi-connection"></a><span data-ttu-id="5def9-103">設定遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="5def9-103">Setting up a Remote WMI Connection</span></span>

<span data-ttu-id="5def9-104">連接至遠端電腦上的 WMI 命名空間，可能需要您變更 [Windows 防火牆](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))、 [使用者帳戶控制 (UAC) ](/previous-versions/aa905108(v=msdn.10))、DCOM 或通用訊息模型物件管理員的設定， (CIMOM) 。</span><span class="sxs-lookup"><span data-stu-id="5def9-104">Connecting to a WMI namespace on a remote computer may require that you change the settings for [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM, or Common Information Model Object Manager (CIMOM).</span></span>

<span data-ttu-id="5def9-105">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="5def9-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="5def9-106">Windows 防火牆設定</span><span class="sxs-lookup"><span data-stu-id="5def9-106">Windows Firewall Settings</span></span>](#windows-firewall-settings)
-   [<span data-ttu-id="5def9-107">使用者帳戶控制設定</span><span class="sxs-lookup"><span data-stu-id="5def9-107">User Account Control Settings</span></span>](#user-account-control-settings)
-   [<span data-ttu-id="5def9-108">DCOM 設定</span><span class="sxs-lookup"><span data-stu-id="5def9-108">DCOM Settings</span></span>](#dcom-settings)
-   [<span data-ttu-id="5def9-109">CIMOM 設定</span><span class="sxs-lookup"><span data-stu-id="5def9-109">CIMOM Settings</span></span>](#cimom-settings)
-   [<span data-ttu-id="5def9-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="5def9-110">Related topics</span></span>](#related-topics)

## <a name="windows-firewall-settings"></a><span data-ttu-id="5def9-111">Windows 防火牆設定</span><span class="sxs-lookup"><span data-stu-id="5def9-111">Windows Firewall Settings</span></span>

<span data-ttu-id="5def9-112">Windows 防火牆設定的 WMI 設定只會啟用 WMI 連接，而不是其他 DCOM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5def9-112">WMI settings for Windows Firewall settings enable only WMI connections, rather than other DCOM applications as well.</span></span>

<span data-ttu-id="5def9-113">您必須在遠端目的電腦上的適用于 WMI 的防火牆中設定例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5def9-113">An exception must be set in the firewall for WMI on the remote target computer.</span></span> <span data-ttu-id="5def9-114">WMI 的例外狀況可讓 WMI 接收遠端連線，以及 Unsecapp.exe 的非同步回呼。</span><span class="sxs-lookup"><span data-stu-id="5def9-114">The exception for WMI allows WMI to receive remote connections and asynchronous callbacks to Unsecapp.exe.</span></span> <span data-ttu-id="5def9-115">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="5def9-115">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="5def9-116">如果用戶端應用程式建立自己的接收，則必須明確地將該接收器新增至防火牆例外狀況，以允許回呼成功。</span><span class="sxs-lookup"><span data-stu-id="5def9-116">If a client application creates its own sink, that sink must be explicitly added to the firewall exceptions to allow callbacks to succeed.</span></span>

<span data-ttu-id="5def9-117">WMI 的例外狀況也適用于 WMI 以固定通訊埠啟動時，使用 **winmgmt/standalonehost** 命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-117">The exception for WMI also works if WMI has been started with a fixed port, using the **winmgmt /standalonehost** command.</span></span> <span data-ttu-id="5def9-118">如需詳細資訊，請參閱 [設定 WMI 的固定通訊埠](setting-up-a-fixed-port-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="5def9-118">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="5def9-119">您可以透過 Windows 防火牆 UI 啟用或停用 WMI 流量。</span><span class="sxs-lookup"><span data-stu-id="5def9-119">You can enable or disable WMI traffic through the Windows Firewall UI.</span></span>

<span data-ttu-id="5def9-120">**使用防火牆 UI 啟用或停用 WMI 流量**</span><span class="sxs-lookup"><span data-stu-id="5def9-120">**To enable or disable WMI traffic using firewall UI**</span></span>

1.  <span data-ttu-id="5def9-121">在 [ **主控台** 中，按一下 [ **安全性** ]，然後按一下 [ **Windows 防火牆**]。</span><span class="sxs-lookup"><span data-stu-id="5def9-121">In the **Control Panel**, click **Security** and then click **Windows Firewall**.</span></span>
2.  <span data-ttu-id="5def9-122">按一下 [ **變更設定** ]，然後按一下 [ **例外** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5def9-122">Click **Change Settings** and then click the **Exceptions** tab.</span></span>
3.  <span data-ttu-id="5def9-123">在 [例外狀況] 視窗中，選取 [ **wmi) 的 Windows Management Instrumentation (** ] 核取方塊，以啟用通過防火牆的 wmi 流量。</span><span class="sxs-lookup"><span data-stu-id="5def9-123">In the Exceptions window, select the check box for **Windows Management Instrumentation (WMI)** to enable WMI traffic through the firewall.</span></span> <span data-ttu-id="5def9-124">若要停用 WMI 流量，請清除此核取方塊。</span><span class="sxs-lookup"><span data-stu-id="5def9-124">To disable WMI traffic, clear the check box.</span></span>

<span data-ttu-id="5def9-125">您可以在命令提示字元中，透過防火牆啟用或停用 WMI 流量。</span><span class="sxs-lookup"><span data-stu-id="5def9-125">You can enable or disable WMI traffic through the firewall at the command prompt.</span></span>

<span data-ttu-id="5def9-126">**若要在命令提示字元使用 WMI 規則群組啟用或停用 WMI 流量**</span><span class="sxs-lookup"><span data-stu-id="5def9-126">**To enable or disable WMI traffic at command prompt using WMI rule group**</span></span>

-   <span data-ttu-id="5def9-127">在命令提示字元中使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-127">Use the following commands at a command prompt.</span></span> <span data-ttu-id="5def9-128">輸入下列各項，以啟用通過防火牆的 WMI 流量。</span><span class="sxs-lookup"><span data-stu-id="5def9-128">Type the following to enable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="5def9-129">**netsh advfirewall firewall set rule group = "windows management instrumentation (wmi) " new enable = yes**</span><span class="sxs-lookup"><span data-stu-id="5def9-129">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**</span></span>

    <span data-ttu-id="5def9-130">輸入下列命令，以停用透過防火牆的 WMI 流量。</span><span class="sxs-lookup"><span data-stu-id="5def9-130">Type the following command to disable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="5def9-131">**netsh advfirewall firewall set rule group = "windows management instrumentation (wmi) " new enable = no**</span><span class="sxs-lookup"><span data-stu-id="5def9-131">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**</span></span>

<span data-ttu-id="5def9-132">您也可以針對每個 DCOM、WMI 服務和接收器使用個別命令，而不是使用 [單一 WMI 規則群組] 命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-132">Rather than using the single WMI rule group command, you also can use individual commands for each of the DCOM, WMI service, and sink.</span></span>

<span data-ttu-id="5def9-133">**針對 DCOM、WMI、回呼接收和連出連線使用不同的規則來啟用 WMI 流量**</span><span class="sxs-lookup"><span data-stu-id="5def9-133">**To enable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="5def9-134">若要建立 DCOM 通訊埠135的防火牆例外，請使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-134">To establish a firewall exception for DCOM port 135, use the following command.</span></span>

    <span data-ttu-id="5def9-135">**netsh advfirewall firewall add rule dir = in name = "DCOM" program =% systemroot% \\ system32 \\svchost.exe service = rpcss action = allow PROTOCOL = TCP localport = 135**</span><span class="sxs-lookup"><span data-stu-id="5def9-135">**netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot%\\system32\\svchost.exe service=rpcss action=allow protocol=TCP localport=135**</span></span>

2.  <span data-ttu-id="5def9-136">若要建立 WMI 服務的防火牆例外狀況，請使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-136">To establish a firewall exception for the WMI service, use the following command.</span></span>

    <span data-ttu-id="5def9-137">**netsh advfirewall firewall add rule dir = in name = "WMI" 程式 =% systemroot% \\ system32 \\svchost.exe service = winmgmt action = allow PROTOCOL = TCP localport = any**</span><span class="sxs-lookup"><span data-stu-id="5def9-137">**netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot%\\system32\\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**</span></span>

3.  <span data-ttu-id="5def9-138">若要針對接收遠端電腦回呼的接收建立防火牆例外，請使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-138">To establish a firewall exception for the sink that receives callbacks from a remote computer, use the following command.</span></span>

    <span data-ttu-id="5def9-139">**netsh advfirewall firewall add rule dir = in name = "Unsecapp.exe" program =% systemroot% \\ system32 \\ wbem \\unsecapp.exe action = allow**</span><span class="sxs-lookup"><span data-stu-id="5def9-139">**netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot%\\system32\\wbem\\unsecapp.exe action=allow**</span></span>

4.  <span data-ttu-id="5def9-140">若要針對本機電腦與本機電腦進行通訊的遠端電腦，建立外寄連線的防火牆例外，請使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-140">To establish a firewall exception for outgoing connections to a remote computer that the local computer is communicating with asynchronously, use the following command.</span></span>

    <span data-ttu-id="5def9-141">**netsh advfirewall firewall add rule dir = out name = "WMI \_ out" 程式 =% systemroot% \\ system32 \\svchost.exe service = winmgmt action = ALLOW protocol = TCP localport = any**</span><span class="sxs-lookup"><span data-stu-id="5def9-141">**netsh advfirewall firewall add rule dir=out name ="WMI\_OUT" program=%systemroot%\\system32\\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**</span></span>

<span data-ttu-id="5def9-142">若要分別停用防火牆例外狀況，請使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="5def9-142">To disable the firewall exceptions separately, use the following commands.</span></span>

<span data-ttu-id="5def9-143">**使用 DCOM、WMI、回呼接收和傳出連線的個別規則來停用 WMI 流量**</span><span class="sxs-lookup"><span data-stu-id="5def9-143">**To disable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="5def9-144">停用 DCOM 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5def9-144">To disable the DCOM exception.</span></span>

    <span data-ttu-id="5def9-145">**netsh advfirewall firewall delete rule name = "DCOM"**</span><span class="sxs-lookup"><span data-stu-id="5def9-145">**netsh advfirewall firewall delete rule name="DCOM"**</span></span>

2.  <span data-ttu-id="5def9-146">停用 WMI 服務例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5def9-146">To disable the WMI service exception.</span></span>

    <span data-ttu-id="5def9-147">**netsh advfirewall firewall delete rule name = "WMI"**</span><span class="sxs-lookup"><span data-stu-id="5def9-147">**netsh advfirewall firewall delete rule name="WMI"**</span></span>

3.  <span data-ttu-id="5def9-148">停用接收例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5def9-148">To disable the sink exception.</span></span>

    <span data-ttu-id="5def9-149">**netsh advfirewall firewall delete rule name = "Unsecapp.exe"**</span><span class="sxs-lookup"><span data-stu-id="5def9-149">**netsh advfirewall firewall delete rule name="UnsecApp"**</span></span>

4.  <span data-ttu-id="5def9-150">停用外寄例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5def9-150">To disable the outgoing exception.</span></span>

    <span data-ttu-id="5def9-151">**netsh advfirewall firewall delete rule name = "WMI \_ OUT"**</span><span class="sxs-lookup"><span data-stu-id="5def9-151">**netsh advfirewall firewall delete rule name="WMI\_OUT"**</span></span>

## <a name="user-account-control-settings"></a><span data-ttu-id="5def9-152">使用者帳戶控制設定</span><span class="sxs-lookup"><span data-stu-id="5def9-152">User Account Control Settings</span></span>

<span data-ttu-id="5def9-153">使用者帳戶控制 (UAC) 存取權杖篩選可能會影響 WMI 命名空間中允許的作業或傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="5def9-153">User Account Control (UAC) access-token filtering can affect which operations are allowed in WMI namespaces or what data is returned.</span></span> <span data-ttu-id="5def9-154">在 UAC 下，本機 Administrators 群組中的所有帳戶都是以標準使用者 [*存取權杖*](/windows/desktop/SecGloss/a-gly)（也稱為 UAC 存取權杖篩選）來執行。</span><span class="sxs-lookup"><span data-stu-id="5def9-154">Under UAC, all accounts in the local Administrators group run with a standard user [*access token*](/windows/desktop/SecGloss/a-gly), also known as UAC access-token filtering.</span></span> <span data-ttu-id="5def9-155">系統管理員帳戶可以使用較高的許可權（「以系統管理員身分執行」）來執行腳本。</span><span class="sxs-lookup"><span data-stu-id="5def9-155">An administrator account can run a script with an elevated privilege—"Run as Administrator".</span></span>

<span data-ttu-id="5def9-156">當您未連線到內建的系統管理員帳戶時，UAC 會根據兩部電腦是否位於網域或工作組中，以不同的方式影響遠端電腦的連線。</span><span class="sxs-lookup"><span data-stu-id="5def9-156">When you are not connecting to the built-in Administrator account, UAC affects connections to a remote computer differently depending on whether the two computers are in a domain or a workgroup.</span></span> <span data-ttu-id="5def9-157">如需 UAC 和遠端連線的詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="5def9-157">For more information about UAC and remote connections, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="dcom-settings"></a><span data-ttu-id="5def9-158">DCOM 設定</span><span class="sxs-lookup"><span data-stu-id="5def9-158">DCOM Settings</span></span>

<span data-ttu-id="5def9-159">如需 DCOM 設定的詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="5def9-159">For more information on DCOM settings, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span> <span data-ttu-id="5def9-160">不過，UAC 會影響非網域使用者帳戶的連接。</span><span class="sxs-lookup"><span data-stu-id="5def9-160">However, UAC affects connections for nondomain user accounts.</span></span> <span data-ttu-id="5def9-161">如果您使用遠端電腦的 [本機系統管理員] 群組中包含的非網域使用者帳戶連接到遠端電腦，則必須明確授與遠端 DCOM 存取、啟動及啟動帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="5def9-161">If you connect to a remote computer using a nondomain user account included in the local Administrators group of the remote computer, then you must explicitly grant remote DCOM access, activation, and launch rights to the account.</span></span>

## <a name="cimom-settings"></a><span data-ttu-id="5def9-162">CIMOM 設定</span><span class="sxs-lookup"><span data-stu-id="5def9-162">CIMOM Settings</span></span>

<span data-ttu-id="5def9-163">如果遠端連線是在沒有信任關係的電腦之間，則必須更新 CIMOM 設定;否則，非同步連接將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5def9-163">The CIMOM settings need to be updated if the remote connection is between computers that do not have a trust relationship; otherwise, an asynchronous connection will fail.</span></span> <span data-ttu-id="5def9-164">針對相同網域或受信任網域中的電腦，不應修改此設定。</span><span class="sxs-lookup"><span data-stu-id="5def9-164">This setting should not be modified for computers in the same domain or in trusted domains.</span></span>

<span data-ttu-id="5def9-165">您必須修改下列登錄專案，才能允許匿名回呼：</span><span class="sxs-lookup"><span data-stu-id="5def9-165">The following registry entry needs to be modified to allow anonymous callbacks:</span></span>

<span data-ttu-id="5def9-166">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**</span><span class="sxs-lookup"><span data-stu-id="5def9-166">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**AllowAnonymousCallback**</span></span><dl> <dt>

               Data type
</dt> <dd>               <span data-ttu-id="5def9-167">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5def9-167">REG\_DWORD</span></span></dd> </dl>

<span data-ttu-id="5def9-168">如果 **AllowAnonymousCallback** 值設定為0，則 WMI 服務會防止用戶端匿名回呼。</span><span class="sxs-lookup"><span data-stu-id="5def9-168">If the **AllowAnonymousCallback** value is set to 0, the WMI service prevents anonymous callbacks to the client.</span></span> <span data-ttu-id="5def9-169">如果值設定為1，則 WMI 服務允許對用戶端進行匿名回呼。</span><span class="sxs-lookup"><span data-stu-id="5def9-169">If the value is set to 1, the WMI service allows anonymous callbacks to the client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5def9-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="5def9-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5def9-171">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="5def9-171">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
