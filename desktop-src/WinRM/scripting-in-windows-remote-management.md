---
title: Windows 遠端管理中的腳本
description: WinRM 中的腳本 API 和 c + + 隨附的 COM API 是設計來仔細反映 WS-Management 通訊協定的作業。
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Windows 遠端管理中的腳本
- Windows遠端系統管理，腳本
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c10d36420b2826162a6ed5e3fb6bf69408a74032faafac75c84c25a754cf534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795428"
---
# <a name="scripting-in-windows-remote-management"></a>Windows 遠端管理中的腳本

[WinRM 中的腳本 API](winrm-scripting-api.md)和 c + + 隨附的 COM API 是設計來仔細反映 WS-Management 通訊協定的作業。

Windows 遠端管理中的 WinRM 腳本 API 可支援所有 WS-Management 的通訊協定作業（其中一個除外）。 它不允許訂閱事件。 若要訂閱來自 BMC 系統事件記錄檔的事件，您必須使用 >wecutil 或 Wevtutil 命令列工具。 如需詳細資訊，請參閱[事件](events.md)。

WinRM 腳本 API 是由 Winrm.vbs 的命令列工具所呼叫，它是以 Visual Basic 腳本撰寫版 (VBScript) 撰寫的。 Winrm.vbs 提供如何使用 [WinRM 腳本 API](winrm-scripting-api.md)的範例。

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>相較于使用 WMI 腳本，使用 WSman

WMI 會透過 DCOM 連接到遠端電腦，這需要在 [遠端電腦上連線至 WMI](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer)所述的設定。 WinRM 不會使用 DCOM 來連接遠端電腦。 相反地，WS-Management 的通訊協定會傳送 SOAP 訊息，而服務會針對 HTTP 使用單一端口，並使用埠進行 HTTPS 傳輸。

不同于 **winrm** 命令列工具，腳本必須提供傳遞給 WS-Management 通訊協定訊息所需的 XML。 它們也必須提供 Uri。 如需詳細資訊，請參閱[資源 uri](resource-uris.md)和[Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。

WMI 腳本 API 適用于物件（例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例），代表電腦上的資源。 此 WMI 類別定義于 [*受控物件格式 (MOF)*](/windows/desktop/WmiSdk/gloss-m) 檔中，這些檔案會以二進位格式儲存在 WMI 存放庫中。 在 WMI 中，單一資源或查詢有多個實例的 Get 作業會傳回 WMI 物件。

WinRM 腳本不會傳回物件，而是 XML 文字的資料流程。 如需詳細資訊，請參閱[Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。

## <a name="displaying-xml-output-from-winrm-scripts"></a>顯示 WinRM 腳本的 XML 輸出

WinRM 腳本 API 會取得並接收描述資源的 XML 字串。 結果 XML 的格式為文字資料流程，需要以其他方式來顯示 XML 轉換。

下列 WinRM 腳本會產生原始 XML 輸出。


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



下列文字區塊顯示 WinRM 腳本的 XML 輸出。


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



您的腳本可以使用 XML 轉換，讓此輸出更容易讀取。 如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。

下列版本的腳本會將 XML 格式化為人們可讀取的輸出。


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



XSL 轉換會建立下列輸出。


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a>WinRM 腳本和 Winrm .cmd 輸出

WinRM 腳本的輸出會以 Unicode 編碼。 如果您建立 [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) 並從腳本寫入檔案，則產生的檔案為 Unicode。 但是，如果您將輸出重新導向至檔案，則編碼為 ANSI。 如果您將輸出重新導向至 XML 檔案，而且輸出中有 Unicode 字元，XML 將會無效。 請注意， **Winrm** 命令列工具會輸出 ANSI。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[DOM 參考](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 