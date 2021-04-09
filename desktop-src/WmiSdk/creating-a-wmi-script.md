---
description: 您可以使用腳本來查看或操作 WMI 所提供的任何資訊。
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: 建立 WMI 腳本
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945390"
---
# <a name="creating-a-wmi-script"></a>建立 WMI 腳本

您可以使用腳本來查看或操作 WMI 所提供的任何資訊。 腳本可以用任何支援 Microsoft ActiveX script 裝載的指令碼語言撰寫，包括 Visual Basic Scripting Edition (VBScript) 、PowerShell 和 Perl。 Windows Script Host (WSH) 、Active Server Pages 和 Internet Explorer 都可以裝載 WMI 腳本。

> [!Note]
>
> WMI 目前支援的主要指令碼語言是 PowerShell。 但是 WMI 也包含一套強大的腳本支援主體，也就是存取 [WMI 的腳本 API](scripting-api-for-wmi.md)的 VBScript 和其他語言。

 

## <a name="wmi-scripting-languages"></a>WMI 指令碼語言

WMI 所支援的兩種主要語言，是透過 Windows Script Host 或 WSH)  (PowerShell 和 VBScript。

-   **PowerShell** 是設計成與 WMI 緊密整合的概念。 因此，WMI 的許多基礎元素都內建于 WMI Cmdlet 中： [>get-wmiobject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1)、 [set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1)、 [>invoke-wmimethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)和 [Remove->get-wmiobject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1)。 下表說明用來存取 WMI 資訊的一般處理常式。 請注意，雖然這些範例大多使用 >get-wmiobject，但許多 PowerShell WMI Cmdlet 都有相同的參數，例如 *類別* 或 *-認證*。 因此，其中許多程式也適用于其他物件。 如需更深入的 PowerShell 和 WMI 討論，請參閱 [使用 Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) 和 [Windows PowerShell-WMI 連接](/previous-versions/technet-magazine/cc162365(v=msdn.10))。

-   相反地， **VBScript** 會明確呼叫 [WMI 的腳本 API](scripting-api-for-wmi.md)（如上所述）。 其他語言（例如 Perl）也可以使用適用于 WMI 的腳本 API。 不過，基於本檔的目的，大部分示範適用于 WMI 的腳本 API 的範例都會使用 VBScript。 不過，當程式設計技術是 VBScript 專屬的時候，就會呼叫它。

    VBScript 基本上有兩種不同的方式可以存取 WMI。 第一個是使用 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件來連接至 WMI。 或者，您也可以使用 [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) 和名字標記。 「名字標記」（namespace）是一種字串，可描述數個元素：您的認證、模擬設定、要連接的目的電腦、WMI [*命名空間*](gloss-n.md) (IE、wmi 用來儲存物件群組) 的一般位置，以及您想要取出的 wmi 物件。 下列許多範例都會說明這兩種技術。 如需詳細資訊，請參閱 [建立標記字串](constructing-a-moniker-string.md) 和 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

    無論您使用哪一種技術來連接至 WMI，都可能會從腳本 API 中取出一或多個物件。 最常見的 [**SWbemObject**](swbemobject.md)是 wmi 用來描述 wmi 物件的。 或者，您可以使用 [**SWbemServices**](swbemservices.md) 物件來描述 wmi 服務本身，或使用 [**SWbemObjectPath**](swbemobjectpath.md) 物件來描述 wmi 物件的位置。 如需詳細資訊，請參閱使用 SWbemObject 和腳本協助程式[物件](scripting-helper-objects.md)[編寫腳本](scripting-with-swbemobject.md)。

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>使用 WMI 和指令碼語言，如何 .。。

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...連接到 WMI？
</dt> <dd>

若為 VBScript 和適用于 WMI 的腳本 API，請使用具有標記的 [**SWbemServices**](swbemservices.md) 物件和對 [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))的呼叫來取出。 或者，您也可以呼叫 [**wbemscripting.swbemlocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)來連接到伺服器。 然後，您可以使用物件來存取特定的 WMI 命名空間或 WMI 類別實例。

針對 PowerShell，連線至 WMI 通常會直接在 Cmdlet 呼叫中執行;因此，不需要額外的步驟。

如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)、 [建立標記字串](constructing-a-moniker-string.md)，以及 [使用 VBScript 連接至 WMI](connecting-to-wmi-with-vbscript.md)。


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...從 WMI 取出資訊？
</dt> <dd>

針對 VBScript 和適用于 WMI 的腳本 API，請使用抓取函式，例如 [**WbemServices. Get**](swbemservices-get.md) 或 [**WbemServices. InstancesOf**](swbemservices-instancesof.md)。 您也可以放置物件的類別名稱，以便在標記中取得，這可能更有效率。

針對 PowerShell，請使用 *-Class* 參數。 請注意，-Class 是預設參數;因此，您不需要明確陳述。

如需詳細資訊，請參閱抓取 [WMI 類別或實例資料](retrieving-class-or-instance-data.md)。


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...建立 WMI 查詢？
</dt> <dd>

針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 方法。

針對 PowerShell，請使用 *-Query* 參數。 您也可以使用 *-filter* 參數進行篩選。

如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...列舉 WMI 物件清單嗎？
</dt> <dd>

針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**swbemobjectset 搭配使用**](swbemobjectset.md) 容器物件，該物件在腳本中會被視為可列舉的集合。 您可以從 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)或 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)的呼叫取出 **swbemobjectset 搭配使用**。

PowerShell 可以像處理任何其他物件一樣，取得和處理列舉;WMI 沒有什麼特別唯一的。

如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...存取不同的 WMI 命名空間？
</dt> <dd>

若為 VBScript 和適用于 WMI 的腳本 API，請在 [標記] 中陳述命名空間，否則您可以在 [**wbemscripting.swbemlocator**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)的呼叫中明確陳述命名空間。

針對 PowerShell，請使用 *-Namespace* 參數。 預設命名空間是「根 \\ cimV2」; 不過，許多較舊的類別會儲存為「根 \\ 預設值」。

若要尋找指定 WMI 類別的位置，請查看參考頁面。 或者，您也可以使用 >get-wmiobject 手動探索命名空間。


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...取出類別的所有子實例？
</dt> <dd>

針對直接針對 WMI 和 PowerShell 使用腳本 API 的語言，WMI 支援抓取基類的子類別。 因此，為了抓取子實例，您只需要搜尋父類別。 下列範例會搜尋 [**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)，這是預先安裝的 WMI 類別，代表 Windows 電腦系統上的邏輯磁片。 因此，搜尋這個父類別也會傳回 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例，這是 Windows 用來描述硬碟的實例。 如需詳細資訊，請參閱 [通用訊息模型](common-information-model.md)。 WMI 提供這類預先安裝類別的完整架構，可讓您存取和控制受管理的物件。 如需詳細資訊，請參閱 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider) 和 [WMI 類別](wmi-classes.md)。


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...找出 WMI 物件？
</dt> <dd>

針對 WMI 和 PowerShell 的腳本 API，WMI 會使用命名空間、類別名稱和索引鍵屬性的組合，來唯一識別指定的 WMI 實例。 這就是所謂的 WMI 物件路徑。 對於 VBScript 而言， [**SWbemObject \_**](swbemobject-path-.md)屬性會描述腳本 API 所傳回之任何指定物件的路徑。 針對 PowerShell，每個 WMI 物件都會有一個 \_ \_ PATH 屬性。 如需詳細資訊，請參閱[描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

除了命名空間和類別名稱之外，WMI 物件也會有一個索引鍵屬性，它可唯一識別該實例與您電腦上的其他實例的比較。 例如， **DeviceID** 屬性是 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的索引鍵屬性。 如需詳細資訊，請參閱 [受控物件格式 (MOF) ](managed-object-format--mof-.md)。

最後，相對路徑只是路徑的縮寫形式，並且包含類別名稱和金鑰值。 在下列範例中，路徑可能是 " \\ \\ computerName \\ Root \\ Cimv2： Win32 \_ LogicalDisk DeviceID =" d： ""，而相對路徑則是 "" Win32LogicalDisk. deviceid = "D" ""。


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...設定 WMI 中的資訊？
</dt> <dd>

針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**SWbemObject. \_ Put**](swbemobject-put-.md)方法。

針對 PowerShell，您可以使用 Put 方法，或 [設定-set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true)。

如需詳細資訊，請參閱 [修改實例屬性](modifying-an-instance-property.md)。


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...使用不同的認證？
</dt> <dd>

針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)方法中的使用者 *名稱* 和 *密碼* 參數。

針對 PowerShell，請使用 *-Credential* 參數。

請注意，您只能在遠端系統上使用替代認證。 如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...要存取遠端電腦嗎？
</dt> <dd>

若為 VBScript 和適用于 WMI 的腳本 API，請明確地在 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)的呼叫中陳述電腦的名稱。 如需詳細資訊，請參閱 [使用 VBScript 從遠端連線到 WMI](connecting-to-wmi-remotely-with-vbscript.md)。

針對 PowerShell，使用 *-ComputerName* 參數。 如需詳細資訊，請參閱 [使用 PowerShell 從遠端連線到 WMI](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)。


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...要設定驗證和模擬層級嗎？
</dt> <dd>

若為 VBScript 和適用于 WMI 的腳本 API，請在傳回的伺服器物件上使用 [**SWbemServices \_**](swbemlocator-security-.md)屬性，否則請在 [名字] 中設定相關的值。

針對 PowerShell，請分別使用 *-驗證* 和 *-* 模擬參數。 如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。

如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...處理 WMI 中的錯誤？
</dt> <dd>

針對 WMI 的腳本 API，提供者可能會提供 [**SWbemLastError**](swbemlasterror.md) 物件，以提供有關錯誤的進一步資訊。

尤其在 VBScript 中，使用原生 **Err** 物件也支援錯誤處理。 您也可以如上面所述存取 [**SWbemLastError**](swbemlasterror.md)物件。 如需詳細資訊，請參閱 [取出錯誤碼](retrieving-an-error-code.md)。

針對 PowerShell，您可以使用標準 PowerShell 錯誤處理技術。 如需詳細資訊，請參閱 [PowerShell 中的錯誤處理簡介](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell)。


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
