---
description: 若要使用 WMI 連接到遠端電腦，請確定已針對連線啟用正確的 DCOM 設定和 WMI 命名空間安全性設定。
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: 保護遠端 WMI 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2a044e49fed5eaa27fbc246dca3306a6c29650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512992"
---
# <a name="securing-a-remote-wmi-connection"></a><span data-ttu-id="89cd5-103">保護遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="89cd5-103">Securing a Remote WMI Connection</span></span>

<span data-ttu-id="89cd5-104">若要使用 WMI 連接到遠端電腦，請確定已針對連線啟用正確的 DCOM 設定和 WMI 命名空間安全性設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-104">To connect to a remote computer using WMI, ensure that the correct DCOM settings and WMI namespace security settings are enabled for the connection.</span></span>

<span data-ttu-id="89cd5-105">WMI 具有預設的模擬、驗證和驗證服務 (遠端連線中的目的電腦所需的 NTLM 或 Kerberos) 設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-105">WMI has default impersonation, authentication, and authentication service (NTLM or Kerberos) settings that the target computer in a remote connection requires.</span></span> <span data-ttu-id="89cd5-106">您的本機電腦可以使用目標系統不接受的不同預設值。</span><span class="sxs-lookup"><span data-stu-id="89cd5-106">Your local machine may use different defaults that the target system does not accept.</span></span> <span data-ttu-id="89cd5-107">您可以在連接呼叫中變更這些設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-107">You can change these settings in the connection call.</span></span>

<span data-ttu-id="89cd5-108">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="89cd5-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="89cd5-109">適用于 WMI 的 DCOM 模擬和驗證設定</span><span class="sxs-lookup"><span data-stu-id="89cd5-109">DCOM Impersonation and Authentication Settings for WMI</span></span>](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [<span data-ttu-id="89cd5-110">設定 DCOM 安全性以允許使用者從遠端存取電腦</span><span class="sxs-lookup"><span data-stu-id="89cd5-110">Setting DCOM Security to Allow a User to Access a Computer Remotely</span></span>](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [<span data-ttu-id="89cd5-111">允許使用者存取特定的 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="89cd5-111">Allowing Users Access to a Specific WMI Namespace</span></span>](#allowing-users-access-to-a-specific-wmi-namespace)
-   [<span data-ttu-id="89cd5-112">將命名空間安全性設定為需要遠端連線的資料加密</span><span class="sxs-lookup"><span data-stu-id="89cd5-112">Setting Namespace Security to Require Data Encryption for Remote Connections</span></span>](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [<span data-ttu-id="89cd5-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="89cd5-113">Related topics</span></span>](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a><span data-ttu-id="89cd5-114">適用于 WMI 的 DCOM 模擬和驗證設定</span><span class="sxs-lookup"><span data-stu-id="89cd5-114">DCOM Impersonation and Authentication Settings for WMI</span></span>

<span data-ttu-id="89cd5-115">WMI 具有預設 DCOM 模擬、驗證和驗證服務 (遠端系統所需的 NTLM 或 Kerberos) 設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-115">WMI has default DCOM impersonation, authentication, and authentication service (NTLM or Kerberos) settings that the a remote system requires.</span></span> <span data-ttu-id="89cd5-116">您的本機系統可能會使用目標遠端系統不接受的不同預設值。</span><span class="sxs-lookup"><span data-stu-id="89cd5-116">Your local system may use different defaults that the target remote system does not accept.</span></span> <span data-ttu-id="89cd5-117">您可以在連接呼叫中變更這些設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-117">You can change these settings in the connection call.</span></span> <span data-ttu-id="89cd5-118">如需詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="89cd5-118">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="89cd5-119">不過，針對驗證服務，建議您指定 **RPC \_ C \_ 驗證 \_ 預設值** ，並允許 DCOM 為目的電腦選擇適當的服務。</span><span class="sxs-lookup"><span data-stu-id="89cd5-119">However, for the authentication service, it is recommended that you specify **RPC\_C\_AUTHN\_DEFAULT** and allow DCOM to choose the appropriate service for the target computer.</span></span>

<span data-ttu-id="89cd5-120">您可以在 c + + 中對 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 的呼叫提供參數中的設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-120">You can supply settings in parameters for the calls to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) in C++.</span></span> <span data-ttu-id="89cd5-121">在腳本中，您可以在呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)、 [**SWbemSecurity**](swbemsecurity.md) 物件或腳本的 [標記](constructing-a-moniker-string.md) 字串中建立安全性設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-121">In scripts, you can establish security settings in calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), in an [**SWbemSecurity**](swbemsecurity.md) object, or in the scripting [moniker](constructing-a-moniker-string.md) string.</span></span>

<span data-ttu-id="89cd5-122">如需所有 c + + 模擬常數的清單，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="89cd5-122">For a list of all the C++ impersonation constants, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="89cd5-123">如需使用「標記」連接的 Visual Basic 常數和腳本字串，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="89cd5-123">For the Visual Basic constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="89cd5-124">下表列出遠端連線 (電腦 B) 的目的電腦所需的預設 DCOM 模擬、驗證和驗證服務設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-124">The following table lists the default DCOM impersonation, authentication, and authentication service settings required by the target computer (Computer B) in a remote connection.</span></span> <span data-ttu-id="89cd5-125">如需詳細資訊，請參閱保護遠端 WMI 連接。</span><span class="sxs-lookup"><span data-stu-id="89cd5-125">For more information, see Securing a Remote WMI Connection.</span></span>



| <span data-ttu-id="89cd5-126">電腦 B 作業系統</span><span class="sxs-lookup"><span data-stu-id="89cd5-126">Computer B operating system</span></span> | <span data-ttu-id="89cd5-127">模擬層級腳本字串</span><span class="sxs-lookup"><span data-stu-id="89cd5-127">Impersonation level scripting string</span></span> | <span data-ttu-id="89cd5-128">驗證層級腳本字串</span><span class="sxs-lookup"><span data-stu-id="89cd5-128">Authentication level scripting string</span></span> | <span data-ttu-id="89cd5-129">驗證服務</span><span class="sxs-lookup"><span data-stu-id="89cd5-129">Authentication service</span></span> |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| <span data-ttu-id="89cd5-130">Windows Vista 或更新版本</span><span class="sxs-lookup"><span data-stu-id="89cd5-130">Windows Vista or later</span></span>      | <span data-ttu-id="89cd5-131">Impersonate</span><span class="sxs-lookup"><span data-stu-id="89cd5-131">Impersonate</span></span>                          | <span data-ttu-id="89cd5-132">Pkt</span><span class="sxs-lookup"><span data-stu-id="89cd5-132">Pkt</span></span>                                   | <span data-ttu-id="89cd5-133">Kerberos</span><span class="sxs-lookup"><span data-stu-id="89cd5-133">Kerberos</span></span>               |



 

<span data-ttu-id="89cd5-134">WMI 遠端連線受 (UAC) 和[Windows 防火牆](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx)的[使用者帳戶控制](/previous-versions/aa905108(v=msdn.10))影響。</span><span class="sxs-lookup"><span data-stu-id="89cd5-134">WMI remote connections are affected by [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) and [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx).</span></span> <span data-ttu-id="89cd5-135">如需詳細資訊，請參閱 [從 Vista 遠端連線至 WMI](connecting-to-wmi-remotely-starting-with-vista.md) ，並 [透過 Windows 防火牆進行連接](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)。</span><span class="sxs-lookup"><span data-stu-id="89cd5-135">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="89cd5-136">請注意，連接到本機電腦上的 WMI 具有預設的驗證層級 **PktPrivacy**。</span><span class="sxs-lookup"><span data-stu-id="89cd5-136">Be aware that connecting to WMI on the local computer has a default authentication level of **PktPrivacy**.</span></span>

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a><span data-ttu-id="89cd5-137">設定 DCOM 安全性以允許使用者從遠端存取電腦</span><span class="sxs-lookup"><span data-stu-id="89cd5-137">Setting DCOM Security to Allow a User to Access a Computer Remotely</span></span>

<span data-ttu-id="89cd5-138">WMI 中的安全性與連接至 WMI 命名空間有關。</span><span class="sxs-lookup"><span data-stu-id="89cd5-138">Security in WMI is related to connecting to a WMI namespace.</span></span> <span data-ttu-id="89cd5-139">WMI 使用 DCOM 來處理遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="89cd5-139">WMI uses DCOM to handle remote calls.</span></span> <span data-ttu-id="89cd5-140">連線到遠端電腦失敗的原因之一，是因為 DCOM 失敗 (錯誤「DCOM 拒絕存取」的十進位-2147024891 或 hex 0x80070005) 。</span><span class="sxs-lookup"><span data-stu-id="89cd5-140">One reason for failure to connect to a remote computer is due to a DCOM failure (error "DCOM Access Denied" decimal -2147024891 or hex 0x80070005).</span></span> <span data-ttu-id="89cd5-141">如需適用于 c + + 應用程式之 WMI 中 DCOM 安全性的詳細資訊，請參閱 [設定用戶端應用程式安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="89cd5-141">For more information about DCOM security in WMI for C++ applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="89cd5-142">您可以使用 [DCOM 設定公用程式] (**DCOMCnfg.exe**) 在 **主控台** 的 [系統 **管理工具**] 中找到，來設定 WMI 的 dcom 設定。</span><span class="sxs-lookup"><span data-stu-id="89cd5-142">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="89cd5-143">此公用程式會公開設定，讓某些使用者透過 DCOM 從遠端連線到電腦。</span><span class="sxs-lookup"><span data-stu-id="89cd5-143">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="89cd5-144">系統管理員群組的成員預設允許遠端連線到電腦。</span><span class="sxs-lookup"><span data-stu-id="89cd5-144">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="89cd5-145">您可以使用此公用程式來設定安全性，以啟動、存取及設定 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="89cd5-145">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="89cd5-146">下列程式描述如何授與特定使用者和群組的 DCOM 遠端啟動和啟用許可權。</span><span class="sxs-lookup"><span data-stu-id="89cd5-146">The following procedure describes how to grant DCOM remote startup and activation permissions for certain users and groups.</span></span> <span data-ttu-id="89cd5-147">如果電腦 A 從遠端連線到電腦 B，您可以在電腦 B 上設定這些許可權，以允許不屬於電腦 B 上 Administrators 群組的使用者或群組，在電腦 B 上執行 DCOM 啟動和啟用呼叫。</span><span class="sxs-lookup"><span data-stu-id="89cd5-147">If Computer A is connecting remotely to Computer B, you can set these permissions on Computer B to allow a user or group that is not part of the Administrators group on Computer B to execute DCOM startup and activation calls on Computer B.</span></span>

<span data-ttu-id="89cd5-148">**授與使用者或群組的 DCOM 遠端啟動和啟用許可權**</span><span class="sxs-lookup"><span data-stu-id="89cd5-148">**To grant DCOM remote launch and activation permissions for a user or group**</span></span>

1.  <span data-ttu-id="89cd5-149">按一下 [ **開始**]，按一下 [ **執行**]，輸入 **DCOMCNFG**，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="89cd5-149">Click **Start**, click **Run**, type **DCOMCNFG**, and then click **OK**.</span></span>
2.  <span data-ttu-id="89cd5-150">在 [**元件服務**] 對話方塊中，依序展開 [**元件服務**]、[**電腦**]，然後以滑鼠右鍵按一下 **我的電腦** 然後按一下 [內容 **]。**</span><span class="sxs-lookup"><span data-stu-id="89cd5-150">In the **Component Services** dialog box, expand **Component Services**, expand **Computers**, and then right-click **My Computer** and click **Properties**.</span></span>
3.  <span data-ttu-id="89cd5-151">在 [ **我的電腦屬性** ] 對話方塊中，按一下 [ **COM 安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="89cd5-151">In the **My Computer Properties** dialog box, click the **COM Security** tab.</span></span>
4.  <span data-ttu-id="89cd5-152">在 [ **啟動和啟用許可權**] 下，按一下 [ **編輯限制**]。</span><span class="sxs-lookup"><span data-stu-id="89cd5-152">Under **Launch and Activation Permissions**, click **Edit Limits**.</span></span>
5.  <span data-ttu-id="89cd5-153">如果您的名稱或群組沒有出現在 [**群組或使用者名稱] 清單** 中，請在 [**啟動許可權**] 對話方塊中，依照下列步驟執行：</span><span class="sxs-lookup"><span data-stu-id="89cd5-153">In the **Launch Permission** dialog box, follow these steps if your name or your group does not appear in the **Groups or user names list**:</span></span>

    1.  <span data-ttu-id="89cd5-154">在 [ **啟動許可權** ] 對話方塊中，按一下 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="89cd5-154">In the **Launch Permission** dialog box, click **Add**.</span></span>
    2.  <span data-ttu-id="89cd5-155">在 [ **選取使用者、電腦或群組** ] 對話方塊的 [ **輸入物件名稱來選取** ] 方塊中，新增您的名稱和群組，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="89cd5-155">In the **Select Users, Computers, or Groups** dialog box, add your name and the group in the **Enter the object names to select** box, and then click **OK**.</span></span>

6.  <span data-ttu-id="89cd5-156">在 [ **啟動許可權** ] 對話方塊中，選取 [ **群組或使用者名稱** ] 方塊中的使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="89cd5-156">In the **Launch Permission** dialog box, select your user and group in the **Group or user names** box.</span></span> <span data-ttu-id="89cd5-157">在 [ **允許** 使用者的 **許可權**] 欄位中，選取 [ **遠端啟動** ] 並選取 [ **遠端啟用**]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="89cd5-157">In the **Allow** column under **Permissions for User**, select **Remote Launch** and select **Remote Activation**, and then click **OK**.</span></span>

<span data-ttu-id="89cd5-158">下列程式描述如何授與特定使用者和群組的 DCOM 遠端存取許可權。</span><span class="sxs-lookup"><span data-stu-id="89cd5-158">The following procedure describes how to grant DCOM remote access permissions for certain users and groups.</span></span> <span data-ttu-id="89cd5-159">如果電腦 A 從遠端連線到電腦 B，您可以在電腦 B 上設定這些許可權，以允許不屬於電腦 b 上 Administrators 群組的使用者或群組連接到電腦 B。</span><span class="sxs-lookup"><span data-stu-id="89cd5-159">If Computer A is connecting remotely to Computer B, you can set these permissions on Computer B to allow a user or group that is not part of the Administrators group on Computer B to connect to Computer B.</span></span>

<span data-ttu-id="89cd5-160">**授與 DCOM 遠端存取許可權**</span><span class="sxs-lookup"><span data-stu-id="89cd5-160">**To grant DCOM remote access permissions**</span></span>

1.  <span data-ttu-id="89cd5-161">按一下 [ **開始**]，按一下 [ **執行**]，輸入 **DCOMCNFG**，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="89cd5-161">Click **Start**, click **Run**, type **DCOMCNFG**, and then click **OK**.</span></span>
2.  <span data-ttu-id="89cd5-162">在 [**元件服務**] 對話方塊中，依序展開 [**元件服務**]、[**電腦**]，然後以滑鼠右鍵按一下 **我的電腦** 然後按一下 [內容 **]。**</span><span class="sxs-lookup"><span data-stu-id="89cd5-162">In the **Component Services** dialog box, expand **Component Services**, expand **Computers**, and then right-click **My Computer** and click **Properties**.</span></span>
3.  <span data-ttu-id="89cd5-163">在 [ **我的電腦屬性** ] 對話方塊中，按一下 [ **COM 安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="89cd5-163">In the **My Computer Properties** dialog box, click the **COM Security** tab.</span></span>
4.  <span data-ttu-id="89cd5-164">在 [ **存取權限**] 下，按一下 [ **編輯限制**]。</span><span class="sxs-lookup"><span data-stu-id="89cd5-164">Under **Access Permissions**, click **Edit Limits**.</span></span>
5.  <span data-ttu-id="89cd5-165">在 [**存取權限**] 對話方塊中，選取 [**群組或使用者名稱**] 方塊中的 [**匿名登** 入名稱]。</span><span class="sxs-lookup"><span data-stu-id="89cd5-165">In the **Access Permission** dialog box, select **ANONYMOUS LOGON** name in the **Group or user names** box.</span></span> <span data-ttu-id="89cd5-166">在 [ **允許** 使用者的 **許可權**] 底下的 [允許] 欄中，選取 [ **遠端存取**]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="89cd5-166">In the **Allow** column under **Permissions for User**, select **Remote Access**, and then click **OK**.</span></span>

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a><span data-ttu-id="89cd5-167">允許使用者存取特定的 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="89cd5-167">Allowing Users Access to a Specific WMI Namespace</span></span>

<span data-ttu-id="89cd5-168">您可以設定命名空間之 WMI 控制項中的「遠端啟用」許可權，以允許或禁止使用者存取特定的 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="89cd5-168">You can allow or disallow users access to a specific WMI namespace by setting the "Remote Enable" permission in the WMI Control for a namespace.</span></span> <span data-ttu-id="89cd5-169">如果使用者嘗試連接到不允許其存取的命名空間，則會收到錯誤0x80041003。</span><span class="sxs-lookup"><span data-stu-id="89cd5-169">If a user tries to connect to a namespace they are not allowed access to, they will receive error 0x80041003.</span></span> <span data-ttu-id="89cd5-170">根據預設，系統只會針對系統管理員啟用此許可權。</span><span class="sxs-lookup"><span data-stu-id="89cd5-170">By default, this permission is enabled only for administrators.</span></span> <span data-ttu-id="89cd5-171">系統管理員可以遠端存取非系統管理員使用者的特定 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="89cd5-171">An administrator can enable remote access to specific WMI namespaces for a nonadministrator user.</span></span>

<span data-ttu-id="89cd5-172">下列程式會設定非系統管理員使用者的遠端啟用許可權。</span><span class="sxs-lookup"><span data-stu-id="89cd5-172">The following procedure sets remote enable permissions for a non-administrator user.</span></span>

<span data-ttu-id="89cd5-173">**設定遠端啟用許可權**</span><span class="sxs-lookup"><span data-stu-id="89cd5-173">**To set remote enable permissions**</span></span>

1.  <span data-ttu-id="89cd5-174">使用 WMI 控制連接到遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="89cd5-174">Connect to the remote computer using the WMI Control.</span></span>

    <span data-ttu-id="89cd5-175">如需 WMI 控制項的詳細資訊，請參閱 [使用 Wmi 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。</span><span class="sxs-lookup"><span data-stu-id="89cd5-175">For more information about the WMI Control, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

2.  <span data-ttu-id="89cd5-176">在 [ **安全性** ] 索引標籤中，選取命名空間，然後按一下 [ **安全性**]。</span><span class="sxs-lookup"><span data-stu-id="89cd5-176">In the **Security** tab, select the namespace and click **Security**.</span></span>
3.  <span data-ttu-id="89cd5-177">找出適當的帳戶，並勾選 [**許可權**] 清單中的 [**遠端啟用**]。</span><span class="sxs-lookup"><span data-stu-id="89cd5-177">Locate the appropriate account and check **Remote Enable** in the **Permissions** list.</span></span>

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a><span data-ttu-id="89cd5-178">將命名空間安全性設定為需要遠端連線的資料加密</span><span class="sxs-lookup"><span data-stu-id="89cd5-178">Setting Namespace Security to Require Data Encryption for Remote Connections</span></span>

<span data-ttu-id="89cd5-179">系統管理員或 MOF 檔案可以設定 WMI 命名空間，如此一來就不會傳回任何資料，除非您使用封包隱私權 (**RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權** 或 **PktPrivacy** 做為腳本) 在該命名空間的連接中的標記。</span><span class="sxs-lookup"><span data-stu-id="89cd5-179">An administrator or a MOF file can configure a WMI namespace so that no data is returned unless you use packet privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **PktPrivacy** as a moniker in a script) in a connection to that namespace.</span></span> <span data-ttu-id="89cd5-180">這可確保資料會在網路上進行加密。</span><span class="sxs-lookup"><span data-stu-id="89cd5-180">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="89cd5-181">如果您嘗試設定較低的驗證等級，您將會收到拒絕存取的訊息。</span><span class="sxs-lookup"><span data-stu-id="89cd5-181">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="89cd5-182">如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="89cd5-182">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="89cd5-183">下列 VBScript 程式碼範例示範如何使用 "pktPrivacy" 連接至加密的命名空間。</span><span class="sxs-lookup"><span data-stu-id="89cd5-183">The following VBScript code example shows how to connect to an encrypted namespace using "pktPrivacy".</span></span>


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a><span data-ttu-id="89cd5-184">相關主題</span><span class="sxs-lookup"><span data-stu-id="89cd5-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89cd5-185">使用 WMI 委派</span><span class="sxs-lookup"><span data-stu-id="89cd5-185">Delegating with WMI</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[<span data-ttu-id="89cd5-186">使用 WMI 從遠端建立進程</span><span class="sxs-lookup"><span data-stu-id="89cd5-186">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> <dt>

[<span data-ttu-id="89cd5-187">保護 c + + 用戶端和提供者</span><span class="sxs-lookup"><span data-stu-id="89cd5-187">Securing C++ Clients and Providers</span></span>](securing-c---clients-and-providers.md)
</dt> <dt>

[<span data-ttu-id="89cd5-188">保護腳本用戶端</span><span class="sxs-lookup"><span data-stu-id="89cd5-188">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 
