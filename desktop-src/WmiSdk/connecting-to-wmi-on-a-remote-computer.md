---
description: 描述腳本、應用程式和提供者如何在遠端電腦上建立與 WMI 的連接，以取得資料或控制硬體和軟體。
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: 連接至遠端電腦上的 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979259"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a><span data-ttu-id="f9a72-103">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="f9a72-103">Connecting to WMI on a Remote Computer</span></span>

<span data-ttu-id="f9a72-104">WMI 可以用來管理及存取遠端電腦上的 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="f9a72-104">WMI can be used to manage and access WMI data on remote computers.</span></span> <span data-ttu-id="f9a72-105">WMI 中的遠端連線受 [Windows 防火牆](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) 和 DCOM 設定影響。</span><span class="sxs-lookup"><span data-stu-id="f9a72-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) and DCOM settings.</span></span> <span data-ttu-id="f9a72-106">[ (UAC) 的使用者帳戶控制 ](/previous-versions/aa905108(v=msdn.10)) 可能也需要變更某些設定。</span><span class="sxs-lookup"><span data-stu-id="f9a72-106">[User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) may also require changes to some settings.</span></span> <span data-ttu-id="f9a72-107">不過，一旦您的設定正確無誤，遠端系統的呼叫就會與本機 WMI 呼叫非常類似。</span><span class="sxs-lookup"><span data-stu-id="f9a72-107">However, once your have your settings correct, the call to a remote system is very similar to a local WMI call.</span></span> <span data-ttu-id="f9a72-108">不過，您可以選擇使用不同的認證、替代的驗證通訊協定和其他安全性功能，讓它變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="f9a72-108">You may choose to make it more complex however, by using different credentials, alternate authentication protocols, and other security features.</span></span>

## <a name="configuring-a-computer-for-a-remote-connection"></a><span data-ttu-id="f9a72-109">設定遠端連線的電腦</span><span class="sxs-lookup"><span data-stu-id="f9a72-109">Configuring a Computer for a Remote Connection</span></span>

<span data-ttu-id="f9a72-110">在您可以使用 WMI 存取遠端系統之前，您可能需要檢查一些安全性設定，以確認您有存取權。</span><span class="sxs-lookup"><span data-stu-id="f9a72-110">Before you can access a remote system with WMI, you may need to check some security settings to confirm that you have access.</span></span> <span data-ttu-id="f9a72-111">具體來說：</span><span class="sxs-lookup"><span data-stu-id="f9a72-111">Specifically:</span></span>

-   <span data-ttu-id="f9a72-112">Windows 包含一些安全性功能，這些功能可能會封鎖遠端系統上的腳本存取。</span><span class="sxs-lookup"><span data-stu-id="f9a72-112">Windows contains a number of security features that may block access to scripts on remote systems.</span></span> <span data-ttu-id="f9a72-113">因此，在進行 WMI 呼叫之前，您可能需要先修改系統的 Active Directory 和 Windows 防火牆設定。</span><span class="sxs-lookup"><span data-stu-id="f9a72-113">As such, you may need to modify your system's Active Directory and Windows Firewall settings before making a WMI call.</span></span> <span data-ttu-id="f9a72-114">如需詳細資訊，請參閱 [設定遠端 Wmi 連接](connecting-to-wmi-remotely-starting-with-vista.md) 和針對 [遠端 Wmi 連線進行疑難排解](troubleshooting-a-remote-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a72-114">For more information, see [Setting up a Remote WMI Connection](connecting-to-wmi-remotely-starting-with-vista.md) and [Troubleshooting a Remote WMI Connection](troubleshooting-a-remote-wmi-connection.md).</span></span>

-   <span data-ttu-id="f9a72-115">必須啟用正確的 DCOM 設定，遠端連線才能運作。</span><span class="sxs-lookup"><span data-stu-id="f9a72-115">The correct DCOM settings must be enabled for a remote connection to work.</span></span> <span data-ttu-id="f9a72-116">變更 DCOM 設定可讓低許可權使用者存取遠端連線的電腦。</span><span class="sxs-lookup"><span data-stu-id="f9a72-116">Changing DCOM settings can allow low rights users access to a computer for a remote connection.</span></span> <span data-ttu-id="f9a72-117">如需詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a72-117">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="f9a72-118">此外，在某些情況下，您可能會想要透過固定的埠來執行 WMI。</span><span class="sxs-lookup"><span data-stu-id="f9a72-118">In addition, there may be some circumstances in which you may wish to run WMI though a fixed port.</span></span> <span data-ttu-id="f9a72-119">若要這樣做，您也必須變更您的設定。</span><span class="sxs-lookup"><span data-stu-id="f9a72-119">To do this, you will also need to change your settings.</span></span> <span data-ttu-id="f9a72-120">如需詳細資訊，請參閱 [設定 WMI 的固定通訊埠](setting-up-a-fixed-port-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a72-120">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

## <a name="connecting-to-a-remote-computer"></a><span data-ttu-id="f9a72-121">Connecting to a Remote Computer</span><span class="sxs-lookup"><span data-stu-id="f9a72-121">Connecting to a Remote Computer</span></span>

<span data-ttu-id="f9a72-122">以 WMI 連接至遠端系統的核心，是要確保您具有適當的許可權來存取系統，且您的連線已正確設定。</span><span class="sxs-lookup"><span data-stu-id="f9a72-122">At its heart, connecting to a remote system with WMI consists of making sure that you have the appropriate permissions to access the system, and that your connection is properly configured.</span></span> <span data-ttu-id="f9a72-123">一旦擁有這兩個元素，連接本身就相當簡單。</span><span class="sxs-lookup"><span data-stu-id="f9a72-123">Once you have those two elements, the connection itself is relatively simple.</span></span> <span data-ttu-id="f9a72-124">例如，如果您使用預設的安全性認證，您可以使用下列程式碼，在遠端系統上存取 WMI：</span><span class="sxs-lookup"><span data-stu-id="f9a72-124">For example, if you are using your default security credentials, you can access WMI on a remote system using the following code:</span></span>

<dl> <dt>

<span data-ttu-id="f9a72-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[使用 PowerShell 從遠端連線至 WMI](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="f9a72-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span></span>
</dt> <dd>

<span data-ttu-id="f9a72-126">使用大部分 WMI Cmdlet 通用的 *-ComputerName* 參數，例如 [>get-wmiobject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="f9a72-126">Use the *-ComputerName* parameter common to most WMI cmdlets, such as [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span></span>


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span data-ttu-id="f9a72-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[使用 VBScript 從遠端連線至 WMI](connecting-to-wmi-remotely-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="f9a72-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span></span>
</dt> <dd>

<span data-ttu-id="f9a72-128">在對 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的呼叫中，使用包含遠端系統名稱的標記。</span><span class="sxs-lookup"><span data-stu-id="f9a72-128">Use a moniker that contains the name of the remote system in the call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span data-ttu-id="f9a72-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[使用 C 遠端連線至 WMI#](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="f9a72-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="f9a72-130">針對目前版本的 WMI managed [介面 (的](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))) ，請使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) 物件來代表與遠端主機的連線。</span><span class="sxs-lookup"><span data-stu-id="f9a72-130">For the current version of the WMI managed interface ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use the [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object to represent a connection to a remote host.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span data-ttu-id="f9a72-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[使用 C 遠端連線至 WMI#](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="f9a72-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="f9a72-132">若為 ([管理](/dotnet/api/system.management)) 的 WMI managed 介面 v1 版本，請使用 [ManagementScope](/dotnet/api/system.management.managementscope) 物件來代表與遠端主機的連接。</span><span class="sxs-lookup"><span data-stu-id="f9a72-132">For the v1 version of the WMI managed interface ([System.Management](/dotnet/api/system.management)), use the [ManagementScope](/dotnet/api/system.management.managementscope) object to represent a connection to a remote host.</span></span>


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span data-ttu-id="f9a72-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[範例：從遠端電腦取得 WMI 資料 (c + +) ](example--getting-wmi-data-from-a-remote-computer.md)</span><span class="sxs-lookup"><span data-stu-id="f9a72-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Example: Getting WMI Data from a Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span></span>
</dt> <dd>

<span data-ttu-id="f9a72-134">您可以使用 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 方法，在 *strNetworkResource* 參數中指定遠端電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a72-134">Use the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method to specify the name of the remote computer in the *strNetworkResource* parameter.</span></span>


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

<span data-ttu-id="f9a72-135">先前的程式碼範例是您可以使用 WMI 執行的最基本遠端連線。</span><span class="sxs-lookup"><span data-stu-id="f9a72-135">The previous code samples are arguably the most basic remote connection you can perform with WMI.</span></span> <span data-ttu-id="f9a72-136">具體而言，範例會假設下列各項：</span><span class="sxs-lookup"><span data-stu-id="f9a72-136">Specifically, the samples assume the following:</span></span>

-   <span data-ttu-id="f9a72-137">您是遠端電腦上的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="f9a72-137">You are an administrator on the remote machine.</span></span> <span data-ttu-id="f9a72-138">由於 [使用者帳戶控制](/previous-versions/aa905108(v=msdn.10))，遠端系統上的帳戶必須是 Administrators 群組中的網域帳戶。</span><span class="sxs-lookup"><span data-stu-id="f9a72-138">Due to [User Account Control](/previous-versions/aa905108(v=msdn.10)), the account on the remote system must be a domain account in the Administrators group.</span></span> <span data-ttu-id="f9a72-139">如需詳細資訊，請參閱使用者帳戶控制和 WMI。</span><span class="sxs-lookup"><span data-stu-id="f9a72-139">For more information, see User Account Control and WMI.</span></span>
-   <span data-ttu-id="f9a72-140">您目前本機電腦上的密碼不是空白的。</span><span class="sxs-lookup"><span data-stu-id="f9a72-140">The password on your current local machine is not blank.</span></span> <span data-ttu-id="f9a72-141">這基本上是 Windows 安全性需求，您必須使用密碼登入系統。</span><span class="sxs-lookup"><span data-stu-id="f9a72-141">This is essentially a Windows security requirement that you must have logged onto your system with a password.</span></span>
-   <span data-ttu-id="f9a72-142">您的本機和遠端電腦都位於相同的網域中。</span><span class="sxs-lookup"><span data-stu-id="f9a72-142">Both your local and remote computers are within the same domain.</span></span> <span data-ttu-id="f9a72-143">如果您需要跨網域界限，您需要提供其他資訊或使用稍微不同的程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="f9a72-143">If you need to cross domain boundaries, you would need to supply additional information or use a slightly different programming model.</span></span>
-   <span data-ttu-id="f9a72-144">您使用自己的帳戶來存取遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="f9a72-144">You are using your own account to access the remote machine.</span></span> <span data-ttu-id="f9a72-145">如果您嘗試存取不同的帳戶，則需要提供其他認證。</span><span class="sxs-lookup"><span data-stu-id="f9a72-145">If you were trying to access a different account, you would need to supply additional credentials.</span></span> <span data-ttu-id="f9a72-146"> (請注意，不允許在本機使用與您目前帳戶不同的認證來存取 WMI。 ) </span><span class="sxs-lookup"><span data-stu-id="f9a72-146">(Note that trying to access WMI locally with credentials different than your current account is not permitted.)</span></span>
-   <span data-ttu-id="f9a72-147">這兩部電腦都執行 IPv6。</span><span class="sxs-lookup"><span data-stu-id="f9a72-147">Both computers are running IPv6.</span></span> <span data-ttu-id="f9a72-148">WMI 支援連接到執行 IPv6 的電腦。</span><span class="sxs-lookup"><span data-stu-id="f9a72-148">WMI supports connections to computers running IPv6.</span></span> <span data-ttu-id="f9a72-149">不過，您的本機電腦和「電腦 \_ B」都必須執行 IPv6。</span><span class="sxs-lookup"><span data-stu-id="f9a72-149">However, both your local machine and "Computer\_B" must be running IPv6.</span></span> <span data-ttu-id="f9a72-150">其中一部電腦也可能正在執行 IPv4。</span><span class="sxs-lookup"><span data-stu-id="f9a72-150">Either computer may be running IPv4 also.</span></span> <span data-ttu-id="f9a72-151">如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a72-151">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>
-   <span data-ttu-id="f9a72-152">您的腳本不需要委派-也就是說，它不需要透過目標遠端電腦來存取其他遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="f9a72-152">Your script does not need to delegate - that is, it does not need to access additional remote computers through the targeted remote computer.</span></span> <span data-ttu-id="f9a72-153">如需詳細資訊，請參閱 [使用 WMI 委派](connecting-to-a-3rd-computer-delegation.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a72-153">For more information, see [Delegating with WMI](connecting-to-a-3rd-computer-delegation.md).</span></span>
-   <span data-ttu-id="f9a72-154">您正在嘗試進行特定呼叫，而不是建立遠端進程。</span><span class="sxs-lookup"><span data-stu-id="f9a72-154">You are trying to make a specific call, rather than creating a remote process.</span></span> <span data-ttu-id="f9a72-155">如需詳細資訊，請參閱 [使用 WMI 從遠端建立進程](creating-processes-remotely.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a72-155">For more information, see [Creating Processes Remotely using WMI](creating-processes-remotely.md).</span></span>

<span data-ttu-id="f9a72-156">在考慮這些限制的情況下，遠端 WMI 呼叫與本機 WMI 呼叫非常類似，唯一的差別在於您必須指定遠端系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a72-156">With those restrictions in mind, a remote WMI call is very similar to a local WMI call - the only difference being that you must specify the name of the remote system.</span></span> <span data-ttu-id="f9a72-157">不過，您可以選擇變更許多這些功能：使用不同的認證，或透過協力廠商電腦路由傳送您的電話，或存取不同的網域。</span><span class="sxs-lookup"><span data-stu-id="f9a72-157">However, you may choose to change many of those features: using different credentials, or routing your call through a 3rd party computer, or accessing a different domain.</span></span>

 

 
