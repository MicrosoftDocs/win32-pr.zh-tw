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
# <a name="connecting-to-wmi-on-a-remote-computer"></a>連接至遠端電腦上的 WMI

WMI 可以用來管理及存取遠端電腦上的 WMI 資料。 WMI 中的遠端連線受 [Windows 防火牆](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) 和 DCOM 設定影響。 [ (UAC) 的使用者帳戶控制 ](/previous-versions/aa905108(v=msdn.10)) 可能也需要變更某些設定。 不過，一旦您的設定正確無誤，遠端系統的呼叫就會與本機 WMI 呼叫非常類似。 不過，您可以選擇使用不同的認證、替代的驗證通訊協定和其他安全性功能，讓它變得更複雜。

## <a name="configuring-a-computer-for-a-remote-connection"></a>設定遠端連線的電腦

在您可以使用 WMI 存取遠端系統之前，您可能需要檢查一些安全性設定，以確認您有存取權。 具體來說：

-   Windows 包含一些安全性功能，這些功能可能會封鎖遠端系統上的腳本存取。 因此，在進行 WMI 呼叫之前，您可能需要先修改系統的 Active Directory 和 Windows 防火牆設定。 如需詳細資訊，請參閱 [設定遠端 Wmi 連接](connecting-to-wmi-remotely-starting-with-vista.md) 和針對 [遠端 Wmi 連線進行疑難排解](troubleshooting-a-remote-wmi-connection.md)。

-   必須啟用正確的 DCOM 設定，遠端連線才能運作。 變更 DCOM 設定可讓低許可權使用者存取遠端連線的電腦。 如需詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。

此外，在某些情況下，您可能會想要透過固定的埠來執行 WMI。 若要這樣做，您也必須變更您的設定。 如需詳細資訊，請參閱 [設定 WMI 的固定通訊埠](setting-up-a-fixed-port-for-wmi.md)。

## <a name="connecting-to-a-remote-computer"></a>Connecting to a Remote Computer

以 WMI 連接至遠端系統的核心，是要確保您具有適當的許可權來存取系統，且您的連線已正確設定。 一旦擁有這兩個元素，連接本身就相當簡單。 例如，如果您使用預設的安全性認證，您可以使用下列程式碼，在遠端系統上存取 WMI：

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[使用 PowerShell 從遠端連線至 WMI](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

使用大部分 WMI Cmdlet 通用的 *-ComputerName* 參數，例如 [>get-wmiobject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true)。


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[使用 VBScript 從遠端連線至 WMI](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

在對 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的呼叫中，使用包含遠端系統名稱的標記。


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[使用 C 遠端連線至 WMI#](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

針對目前版本的 WMI managed [介面 (的](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))) ，請使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) 物件來代表與遠端主機的連線。


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[使用 C 遠端連線至 WMI#](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

若為 ([管理](/dotnet/api/system.management)) 的 WMI managed 介面 v1 版本，請使用 [ManagementScope](/dotnet/api/system.management.managementscope) 物件來代表與遠端主機的連接。


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[範例：從遠端電腦取得 WMI 資料 (c + +) ](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

您可以使用 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 方法，在 *strNetworkResource* 參數中指定遠端電腦的名稱。


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

先前的程式碼範例是您可以使用 WMI 執行的最基本遠端連線。 具體而言，範例會假設下列各項：

-   您是遠端電腦上的系統管理員。 由於 [使用者帳戶控制](/previous-versions/aa905108(v=msdn.10))，遠端系統上的帳戶必須是 Administrators 群組中的網域帳戶。 如需詳細資訊，請參閱使用者帳戶控制和 WMI。
-   您目前本機電腦上的密碼不是空白的。 這基本上是 Windows 安全性需求，您必須使用密碼登入系統。
-   您的本機和遠端電腦都位於相同的網域中。 如果您需要跨網域界限，您需要提供其他資訊或使用稍微不同的程式設計模型。
-   您使用自己的帳戶來存取遠端電腦。 如果您嘗試存取不同的帳戶，則需要提供其他認證。  (請注意，不允許在本機使用與您目前帳戶不同的認證來存取 WMI。 ) 
-   這兩部電腦都執行 IPv6。 WMI 支援連接到執行 IPv6 的電腦。 不過，您的本機電腦和「電腦 \_ B」都必須執行 IPv6。 其中一部電腦也可能正在執行 IPv4。 如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)。
-   您的腳本不需要委派-也就是說，它不需要透過目標遠端電腦來存取其他遠端電腦。 如需詳細資訊，請參閱 [使用 WMI 委派](connecting-to-a-3rd-computer-delegation.md)。
-   您正在嘗試進行特定呼叫，而不是建立遠端進程。 如需詳細資訊，請參閱 [使用 WMI 從遠端建立進程](creating-processes-remotely.md)。

在考慮這些限制的情況下，遠端 WMI 呼叫與本機 WMI 呼叫非常類似，唯一的差別在於您必須指定遠端系統的名稱。 不過，您可以選擇變更許多這些功能：使用不同的認證，或透過協力廠商電腦路由傳送您的電話，或存取不同的網域。

 

 
