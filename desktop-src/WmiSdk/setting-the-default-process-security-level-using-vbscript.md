---
title: 使用 VBScript 設定預設進程安全性等級
description: 腳本可以使用預設的 WMI 驗證和模擬設定。 不過，腳本可能需要更多安全性的連接，或可能連接到需要加密連接的命名空間。
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195056"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a><span data-ttu-id="bd217-104">使用 VBScript 設定預設進程安全性等級</span><span class="sxs-lookup"><span data-stu-id="bd217-104">Set the default process security level with VBScript</span></span>

<span data-ttu-id="bd217-105">腳本可以使用預設的 WMI 驗證和模擬設定。</span><span class="sxs-lookup"><span data-stu-id="bd217-105">A script can use the default WMI authentication and impersonation settings.</span></span> <span data-ttu-id="bd217-106">不過，腳本可能需要更多安全性的連接，或可能連接到需要加密連接的命名空間。</span><span class="sxs-lookup"><span data-stu-id="bd217-106">However, the script may need a connection with more security or may connect to a namespace that requires an encrypted connection.</span></span> <span data-ttu-id="bd217-107">如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md) 和 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="bd217-107">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md) and [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="bd217-108">在最簡單的情況下，腳本可以使用預設的驗證和模擬設定。</span><span class="sxs-lookup"><span data-stu-id="bd217-108">In the simplest case, a script can use the default authentication and impersonation settings.</span></span> <span data-ttu-id="bd217-109">WMI 通常會在共用服務主機中執行，並與主機中的其他進程共用相同的驗證。</span><span class="sxs-lookup"><span data-stu-id="bd217-109">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="bd217-110">如果您想要以不同的驗證層級執行 WMI 進程，請使用 [**winmgmt**](winmgmt.md) 命令搭配 **/standalonehost** 參數來執行 wmi，並一般設定 wmi 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="bd217-110">If you want to run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="bd217-111">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="bd217-111">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="bd217-112">下列腳本會使用模擬和驗證層級的預設設定。</span><span class="sxs-lookup"><span data-stu-id="bd217-112">The following script uses default settings for impersonation and authentication levels.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="bd217-113">您也可以在對 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)的呼叫中使用 [名字](constructing-a-moniker-string.md)，並設定預設安全性設定，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="bd217-113">You can also use a [moniker](constructing-a-moniker-string.md) in a call to [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), and set the default security settings, as in the following example.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="bd217-114">如需在腳本中設定不同的模擬或驗證層級，或設定電腦預設值的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="bd217-114">For more information about setting different impersonation or authentication levels in a script, or for setting the default values for a computer, see the following topics:</span></span>

-   [<span data-ttu-id="bd217-115">使用 VBScript 變更預設驗證認證</span><span class="sxs-lookup"><span data-stu-id="bd217-115">Changing the Default Authentication Credentials Using VBScript</span></span>](#changing-the-default-authentication-credentials-using-vbscript)
-   [<span data-ttu-id="bd217-116">使用 VBScript 變更預設模擬設定</span><span class="sxs-lookup"><span data-stu-id="bd217-116">Changing the Default Impersonation Settings Using VBScript</span></span>](#changing-the-default-impersonation-levels-using-vbscript)
-   [<span data-ttu-id="bd217-117">使用登錄設定預設模擬等級</span><span class="sxs-lookup"><span data-stu-id="bd217-117">Setting the Default Impersonation Level Using the Registry</span></span>](#setting-the-default-impersonation-level-using-the-registry)
-   [<span data-ttu-id="bd217-118">存取 VBScript 中的 SWbemSecurity 物件</span><span class="sxs-lookup"><span data-stu-id="bd217-118">Accessing the SWbemSecurity Object in VBScript</span></span>](#accessing-the-swbemsecurity-object-in-vbscript)
-   [<span data-ttu-id="bd217-119">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="bd217-119">**SWbemSecurity**</span></span>](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a><span data-ttu-id="bd217-120">使用 VBScript 變更預設驗證認證</span><span class="sxs-lookup"><span data-stu-id="bd217-120">Changing the Default Authentication Credentials Using VBScript</span></span>

<span data-ttu-id="bd217-121">您可以使用 [標記](constructing-a-moniker-string.md) 字串和 [**wbemscripting.swbemlocator**](swbemlocator.md) 和 [**SWbemSecurity**](swbemsecurity.md) 物件來變更腳本中的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="bd217-121">You can change the authentication level in a script using a [moniker](constructing-a-moniker-string.md) string, and the [**SWbemLocator**](swbemlocator.md) and [**SWbemSecurity**](swbemsecurity.md) objects.</span></span>

<span data-ttu-id="bd217-122">驗證層級必須根據您要連接的目標作業系統需求來設定。</span><span class="sxs-lookup"><span data-stu-id="bd217-122">The authentication level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="bd217-123">如需詳細資訊，請參閱 [在不同的作業系統之間進行連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)。</span><span class="sxs-lookup"><span data-stu-id="bd217-123">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="bd217-124">下列 VBScript 程式碼範例示範如何變更腳本中的驗證層級，以從名為 "Server1" 的遠端電腦取得可用空間資料。</span><span class="sxs-lookup"><span data-stu-id="bd217-124">The following VBScript code example shows how to change the authentication level in a script that obtains the free space data from a remote computer named "Server1".</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



<span data-ttu-id="bd217-125">在 [腳本的標記與 WMI 的連接] 中，使用下表的 "名字/描述" 資料行中顯示的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="bd217-125">In script moniker connections to WMI, use the short name shown in the "Moniker name/description" column of the table below.</span></span> <span data-ttu-id="bd217-126">例如，在下列腳本中，驗證層級會設定為 **WbemAuthenticationLevelPktIntegrity**。</span><span class="sxs-lookup"><span data-stu-id="bd217-126">For example, in the following script, the authentication level is set to **WbemAuthenticationLevelPktIntegrity**.</span></span>


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



<span data-ttu-id="bd217-127">下表列出您可以設定的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="bd217-127">The following table lists the authentication levels you can set.</span></span> <span data-ttu-id="bd217-128">這些層級會在列舉 [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)的 >wbemdisp.tlb 中定義。</span><span class="sxs-lookup"><span data-stu-id="bd217-128">These levels are defined in Wbemdisp.tlb in the enumeration [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>



| <span data-ttu-id="bd217-129">名稱/值</span><span class="sxs-lookup"><span data-stu-id="bd217-129">Name/value</span></span>                                                      | <span data-ttu-id="bd217-130">Description</span><span class="sxs-lookup"><span data-stu-id="bd217-130">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd217-131">**WbemAuthenticationLevelDefault**</span><span class="sxs-lookup"><span data-stu-id="bd217-131">**WbemAuthenticationLevelDefault**</span></span><br/> <span data-ttu-id="bd217-132">0</span><span class="sxs-lookup"><span data-stu-id="bd217-132">0</span></span><br/>      | <span data-ttu-id="bd217-133">標記：預設值</span><span class="sxs-lookup"><span data-stu-id="bd217-133">Moniker: Default</span></span><br/> <span data-ttu-id="bd217-134">WMI 會使用預設的 Windows 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="bd217-134">WMI uses the default Windows authentication setting.</span></span> <span data-ttu-id="bd217-135">這是建議的設定，可讓 WMI 協調伺服器傳回資料所需的層級。</span><span class="sxs-lookup"><span data-stu-id="bd217-135">This is the recommended setting that allows WMI to negotiate to the level required by the server returning data.</span></span> <span data-ttu-id="bd217-136">但是，如果命名空間需要加密，請使用 **WbemAuthenticationLevelPktPrivacy**。</span><span class="sxs-lookup"><span data-stu-id="bd217-136">However, if the namespace requires encryption, use **WbemAuthenticationLevelPktPrivacy**.</span></span><br/> |
| <span data-ttu-id="bd217-137">**WbemAuthenticationLevelNone**</span><span class="sxs-lookup"><span data-stu-id="bd217-137">**WbemAuthenticationLevelNone**</span></span><br/> <span data-ttu-id="bd217-138">1</span><span class="sxs-lookup"><span data-stu-id="bd217-138">1</span></span><br/>         | <span data-ttu-id="bd217-139">標記：無</span><span class="sxs-lookup"><span data-stu-id="bd217-139">Moniker: None</span></span><br/> <span data-ttu-id="bd217-140">不使用驗證。</span><span class="sxs-lookup"><span data-stu-id="bd217-140">Uses no authentication.</span></span><br/>                                                                                                                                                                                                                                            |
| <span data-ttu-id="bd217-141">**WbemAuthenticationLevelConnect**</span><span class="sxs-lookup"><span data-stu-id="bd217-141">**WbemAuthenticationLevelConnect**</span></span><br/> <span data-ttu-id="bd217-142">2</span><span class="sxs-lookup"><span data-stu-id="bd217-142">2</span></span><br/>      | <span data-ttu-id="bd217-143">標記：連接</span><span class="sxs-lookup"><span data-stu-id="bd217-143">Moniker: Connect</span></span><br/> <span data-ttu-id="bd217-144">只有當用戶端建立與伺服器之間的關聯性時，才會驗證用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="bd217-144">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span><br/>                                                                                                                                                    |
| <span data-ttu-id="bd217-145">**WbemAuthenticationLevelCall**</span><span class="sxs-lookup"><span data-stu-id="bd217-145">**WbemAuthenticationLevelCall**</span></span><br/> <span data-ttu-id="bd217-146">3</span><span class="sxs-lookup"><span data-stu-id="bd217-146">3</span></span><br/>         | <span data-ttu-id="bd217-147">呼叫</span><span class="sxs-lookup"><span data-stu-id="bd217-147">Call</span></span><br/> <span data-ttu-id="bd217-148">當伺服器收到要求時，只會在每次呼叫的開頭進行驗證。</span><span class="sxs-lookup"><span data-stu-id="bd217-148">Authenticates only at the beginning of each call when the server receives the request.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="bd217-149">**WbemAuthenticationLevelPkt**</span><span class="sxs-lookup"><span data-stu-id="bd217-149">**WbemAuthenticationLevelPkt**</span></span><br/> <span data-ttu-id="bd217-150">4</span><span class="sxs-lookup"><span data-stu-id="bd217-150">4</span></span><br/>          | <span data-ttu-id="bd217-151">標記： Pkt</span><span class="sxs-lookup"><span data-stu-id="bd217-151">Moniker: Pkt</span></span><br/> <span data-ttu-id="bd217-152">驗證收到的所有資料都是來自預期的用戶端。</span><span class="sxs-lookup"><span data-stu-id="bd217-152">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                                                                                   |
| <span data-ttu-id="bd217-153">**WbemAuthenticationLevelPktIntegrity**</span><span class="sxs-lookup"><span data-stu-id="bd217-153">**WbemAuthenticationLevelPktIntegrity**</span></span><br/> <span data-ttu-id="bd217-154">5</span><span class="sxs-lookup"><span data-stu-id="bd217-154">5</span></span><br/> | <span data-ttu-id="bd217-155">標記： PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="bd217-155">Moniker: PktIntegrity</span></span><br/> <span data-ttu-id="bd217-156">驗證並確認在用戶端與伺服器之間傳送的資料都沒有修改。</span><span class="sxs-lookup"><span data-stu-id="bd217-156">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="bd217-157">**WbemAuthenticationLevelPktPrivacy**</span><span class="sxs-lookup"><span data-stu-id="bd217-157">**WbemAuthenticationLevelPktPrivacy**</span></span><br/> <span data-ttu-id="bd217-158">6</span><span class="sxs-lookup"><span data-stu-id="bd217-158">6</span></span><br/>   | <span data-ttu-id="bd217-159">標記： PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="bd217-159">Moniker: PktPrivacy</span></span><br/> <span data-ttu-id="bd217-160">驗證所有先前的模擬層級，並加密每個遠端程序呼叫的引數值。</span><span class="sxs-lookup"><span data-stu-id="bd217-160">Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.</span></span> <span data-ttu-id="bd217-161">如果您要連接的命名空間需要加密的連接，請使用此設定。</span><span class="sxs-lookup"><span data-stu-id="bd217-161">Use this setting if the namespace to which you are connecting requires an encrypted connection.</span></span><br/>                                               |



 

<span data-ttu-id="bd217-162">若要判斷成功的呼叫，請在變更驗證等級之後，檢查傳回值。</span><span class="sxs-lookup"><span data-stu-id="bd217-162">To determine a successful call, check the return value after you change the authentication level.</span></span>

<span data-ttu-id="bd217-163">例如，由於本機連接一律具有 **wbemAuthenticationLevelPktPrivacy** 的驗證層級，因此下列範例無法設定驗證層級，因為它會連接到本機電腦。</span><span class="sxs-lookup"><span data-stu-id="bd217-163">For example, because local connections always have an authentication level of **wbemAuthenticationLevelPktPrivacy**, the following example fails to set the authentication level because it connects to the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="bd217-164">提供者可以設定命名空間的安全性，如此就不會傳回任何資料，除非您在與該命名空間的連接中使用封包隱私權 (PktPrivacy) 。</span><span class="sxs-lookup"><span data-stu-id="bd217-164">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (PktPrivacy) in your connection to that namespace.</span></span> <span data-ttu-id="bd217-165">這可確保資料會在網路上進行加密。</span><span class="sxs-lookup"><span data-stu-id="bd217-165">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="bd217-166">如果您嘗試設定較低的驗證等級，您將會收到拒絕存取的訊息。</span><span class="sxs-lookup"><span data-stu-id="bd217-166">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="bd217-167">如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="bd217-167">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a><span data-ttu-id="bd217-168">使用 VBScript 變更預設模擬等級</span><span class="sxs-lookup"><span data-stu-id="bd217-168">Changing the Default Impersonation Levels Using VBScript</span></span>

<span data-ttu-id="bd217-169">當您對 WMI 的腳本 API 進行呼叫時，建議您使用 WMI 為模擬等級提供的預設值。</span><span class="sxs-lookup"><span data-stu-id="bd217-169">When you make calls to the Scripting API for WMI, it is recommended that you use the defaults that WMI provides for the impersonation level.</span></span> <span data-ttu-id="bd217-170">遠端呼叫和某些具有多個網路躍點的提供者所需的模擬層級比 WMI 使用的更高。</span><span class="sxs-lookup"><span data-stu-id="bd217-170">Remote calls and some providers with more than one network hop require a higher impersonation level than WMI uses.</span></span> <span data-ttu-id="bd217-171">如果模擬層級不足，提供者可能會拒絕要求或提供不完整的資訊。</span><span class="sxs-lookup"><span data-stu-id="bd217-171">If the impersonation level is not sufficient, a provider might refuse a request or provide incomplete information.</span></span>

<span data-ttu-id="bd217-172">如果您未設定 SWbemSecurity 中的模擬等級，或是在安全物件上設定 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) ，請設定作業系統的預設 DCOM 模擬等級。</span><span class="sxs-lookup"><span data-stu-id="bd217-172">If you do not set the impersonation level in either a moniker or by setting [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on a securable object, then set the default DCOM impersonation level for the operating system.</span></span> <span data-ttu-id="bd217-173">模擬等級必須根據您要連接的目標作業系統需求來設定。</span><span class="sxs-lookup"><span data-stu-id="bd217-173">The impersonation level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="bd217-174">如需詳細資訊，請參閱 [在不同的作業系統之間進行連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)。</span><span class="sxs-lookup"><span data-stu-id="bd217-174">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="bd217-175">下列 VBScript 程式碼範例示範如何變更上述相同腳本中的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="bd217-175">The following VBScript code example shows changing the impersonation level in the same script shown above.</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



<span data-ttu-id="bd217-176">下表列出 [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) 中使用的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="bd217-176">The following table lists the authentication levels in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) that use.</span></span>



| <span data-ttu-id="bd217-177">名稱/值</span><span class="sxs-lookup"><span data-stu-id="bd217-177">Name/value</span></span>                                                    | <span data-ttu-id="bd217-178">Description</span><span class="sxs-lookup"><span data-stu-id="bd217-178">Description</span></span>                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd217-179">**wbemImpersonationLevelAnonymous**</span><span class="sxs-lookup"><span data-stu-id="bd217-179">**wbemImpersonationLevelAnonymous**</span></span><br/> <span data-ttu-id="bd217-180">1</span><span class="sxs-lookup"><span data-stu-id="bd217-180">1</span></span><br/>   | <span data-ttu-id="bd217-181">標記：匿名</span><span class="sxs-lookup"><span data-stu-id="bd217-181">Moniker: Anonymous</span></span><br/> <span data-ttu-id="bd217-182">隱藏呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="bd217-182">Hides the credentials of the caller.</span></span> <span data-ttu-id="bd217-183">對 WMI 的呼叫可能會因為這個模擬等級而失敗。</span><span class="sxs-lookup"><span data-stu-id="bd217-183">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                                  |
| <span data-ttu-id="bd217-184">**wbemImpersonationLevelIdentify**</span><span class="sxs-lookup"><span data-stu-id="bd217-184">**wbemImpersonationLevelIdentify**</span></span><br/> <span data-ttu-id="bd217-185">2</span><span class="sxs-lookup"><span data-stu-id="bd217-185">2</span></span><br/>    | <span data-ttu-id="bd217-186">標記：識別</span><span class="sxs-lookup"><span data-stu-id="bd217-186">Moniker: Identify</span></span><br/> <span data-ttu-id="bd217-187">允許物件查詢呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="bd217-187">Allows objects to query the credentials of the caller.</span></span> <span data-ttu-id="bd217-188">對 WMI 的呼叫可能會因為這個模擬等級而失敗。</span><span class="sxs-lookup"><span data-stu-id="bd217-188">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                 |
| <span data-ttu-id="bd217-189">**wbemImpersonationLevelImpersonate**</span><span class="sxs-lookup"><span data-stu-id="bd217-189">**wbemImpersonationLevelImpersonate**</span></span><br/> <span data-ttu-id="bd217-190">3</span><span class="sxs-lookup"><span data-stu-id="bd217-190">3</span></span><br/> | <span data-ttu-id="bd217-191">標記：模擬</span><span class="sxs-lookup"><span data-stu-id="bd217-191">Moniker: Impersonate</span></span><br/> <span data-ttu-id="bd217-192">允許物件使用呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="bd217-192">Allows objects to use the credentials of the caller.</span></span> <span data-ttu-id="bd217-193">這是針對 WMI 呼叫編寫腳本 API 的建議模擬等級。</span><span class="sxs-lookup"><span data-stu-id="bd217-193">This is the recommended impersonation level for Scripting API for WMI calls.</span></span><br/>                                                        |
| <span data-ttu-id="bd217-194">**wbemImpersonationLevelDelegate**</span><span class="sxs-lookup"><span data-stu-id="bd217-194">**wbemImpersonationLevelDelegate**</span></span><br/> <span data-ttu-id="bd217-195">4</span><span class="sxs-lookup"><span data-stu-id="bd217-195">4</span></span><br/>    | <span data-ttu-id="bd217-196">標記：委派</span><span class="sxs-lookup"><span data-stu-id="bd217-196">Moniker: Delegate</span></span><br/> <span data-ttu-id="bd217-197">允許物件許可其他物件使用呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="bd217-197">Allows objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="bd217-198">這種模擬適用于 WMI 呼叫的腳本 API，但可能構成不必要的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="bd217-198">This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.</span></span><br/> |



 

<span data-ttu-id="bd217-199">下列範例示範如何在取得 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process)程式的特定實例時，在標記字串中設定模擬。</span><span class="sxs-lookup"><span data-stu-id="bd217-199">The following example shows how to set the impersonation in a moniker string when obtaining a specific instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



<span data-ttu-id="bd217-200">如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。</span><span class="sxs-lookup"><span data-stu-id="bd217-200">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

## <a name="setting-the-default-impersonation-level-using-the-registry"></a><span data-ttu-id="bd217-201">使用登錄設定預設模擬等級</span><span class="sxs-lookup"><span data-stu-id="bd217-201">Setting the Default Impersonation Level Using the Registry</span></span>

<span data-ttu-id="bd217-202">如果您可以存取登錄，也可以設定預設的模擬層級登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="bd217-202">If you have access to the registry, you can also set the default impersonation level registry key.</span></span> <span data-ttu-id="bd217-203">此索引鍵會指定適用于 WMI 的腳本 API 所使用的模擬層級（除非另有指定）。</span><span class="sxs-lookup"><span data-stu-id="bd217-203">This key specifies which impersonation level the Scripting API for WMI uses unless otherwise specified.</span></span> <span data-ttu-id="bd217-204">下列路徑會識別登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="bd217-204">The following path identifies the registry path.</span></span>

<span data-ttu-id="bd217-205">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本** \\ **預設模擬等級**</span><span class="sxs-lookup"><span data-stu-id="bd217-205">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Impersonation Level**</span></span>

<span data-ttu-id="bd217-206">根據預設，登錄機碼會設定為3，指定模擬模擬等級。</span><span class="sxs-lookup"><span data-stu-id="bd217-206">By default, the registry key is set to 3, specifying the Impersonate impersonation level.</span></span> <span data-ttu-id="bd217-207">某些提供者可能需要較高的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="bd217-207">Some providers may require a higher level of impersonation.</span></span>

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a><span data-ttu-id="bd217-208">存取 VBScript 中的 SWbemSecurity 物件</span><span class="sxs-lookup"><span data-stu-id="bd217-208">Accessing the SWbemSecurity Object in VBScript</span></span>

<span data-ttu-id="bd217-209">您可以設定模擬等級的另一種方式是從 [**SWbemSecurity**](swbemsecurity.md)安全性物件，此物件會顯示為 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemEventSource**](swbemeventsource.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**wbemscripting.swbemlocator**](swbemlocator.md)物件的 [**security \_**](swbemservices-security-.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="bd217-209">The other way you can set the impersonation level is from the [**SWbemSecurity**](swbemsecurity.md) security object, which appears as the [**Security\_**](swbemservices-security-.md) property of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects.</span></span>

<span data-ttu-id="bd217-210">WMI 會將父物件的安全性設定傳遞至原始物件的子系。</span><span class="sxs-lookup"><span data-stu-id="bd217-210">WMI passes the security setting of a parent object to the descendants of the original object.</span></span> <span data-ttu-id="bd217-211">因此，您可以在使用這個物件或從中建立的物件（例如 [**SWbemObject**](swbemobject.md)類型的物件）登入 WMI 和 API 呼叫之後，設定 [**SWbemServices**](swbemservices.md)物件的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="bd217-211">Therefore, you can set the impersonation level of an [**SWbemServices**](swbemservices.md) object after logging on to WMI and API calls using this object or objects created from it, such as objects of type [**SWbemObject**](swbemobject.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd217-212">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd217-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd217-213">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="bd217-213">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="bd217-214">保護腳本用戶端</span><span class="sxs-lookup"><span data-stu-id="bd217-214">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

