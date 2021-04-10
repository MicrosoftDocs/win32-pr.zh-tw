---
title: Windows 遠端管理中的腳本
description: WinRM 中的腳本 API 和 c + + 隨附的 COM API 是設計來仔細反映 WS-Management 通訊協定的作業。
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Windows 遠端管理中的腳本
- Windows 遠端管理，腳本
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75af10fea03853de99c884eda0a74ce340683b49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092749"
---
# <a name="scripting-in-windows-remote-management"></a><span data-ttu-id="8542c-105">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="8542c-105">Scripting in Windows Remote Management</span></span>

<span data-ttu-id="8542c-106">[WinRM 中的腳本 API](winrm-scripting-api.md)和 c + + 隨附的 COM API 是設計來仔細反映 WS-Management 通訊協定的作業。</span><span class="sxs-lookup"><span data-stu-id="8542c-106">The [Scripting API in WinRM](winrm-scripting-api.md) and the accompanying COM API for C++ are designed to closely reflect the operations of the WS-Management protocol.</span></span>

<span data-ttu-id="8542c-107">Windows 遠端管理中的 WinRM 腳本 API 可支援所有 WS-Management 的通訊協定作業（其中一個除外）。</span><span class="sxs-lookup"><span data-stu-id="8542c-107">The WinRM Scripting API in Windows Remote Management supports all the WS-Management protocol operations except one.</span></span> <span data-ttu-id="8542c-108">它不允許訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="8542c-108">It does not allow subscriptions to events.</span></span> <span data-ttu-id="8542c-109">若要訂閱來自 BMC 系統事件記錄檔的事件，您必須使用 >wecutil 或 Wevtutil 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="8542c-109">To subscribe to events from the BMC System Event Log, you must use the Wecutil or Wevtutil command-line tools.</span></span> <span data-ttu-id="8542c-110">如需詳細資訊，請參閱[事件](events.md)。</span><span class="sxs-lookup"><span data-stu-id="8542c-110">For more information, see [Events](events.md).</span></span>

<span data-ttu-id="8542c-111">WinRM 腳本 API 是由 Winrm.vbs 的命令列工具所呼叫，它是以 Visual Basic Scripting Edition (VBScript) 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="8542c-111">The WinRM Scripting API is called by Winrm.vbs, a command-line tool, which is written in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="8542c-112">Winrm.vbs 提供如何使用 [WinRM 腳本 API](winrm-scripting-api.md)的範例。</span><span class="sxs-lookup"><span data-stu-id="8542c-112">Winrm.vbs provides examples of how to use the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

## <a name="using-wsman-compared-to-using-wmi-scripting"></a><span data-ttu-id="8542c-113">相較于使用 WMI 腳本，使用 WSman</span><span class="sxs-lookup"><span data-stu-id="8542c-113">Using WSman Compared to Using WMI Scripting</span></span>

<span data-ttu-id="8542c-114">WMI 會透過 DCOM 連接到遠端電腦，這需要在 [遠端電腦上連線至 WMI](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer)所述的設定。</span><span class="sxs-lookup"><span data-stu-id="8542c-114">WMI connects to remote computers through DCOM, which requires the configuration described in [Connecting to WMI on a Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span></span> <span data-ttu-id="8542c-115">WinRM 不會使用 DCOM 來連接遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="8542c-115">WinRM does not use DCOM to connect to a remote computer.</span></span> <span data-ttu-id="8542c-116">相反地，WS-Management 的通訊協定會傳送 SOAP 訊息，而服務會針對 HTTP 使用單一端口，並使用埠進行 HTTPS 傳輸。</span><span class="sxs-lookup"><span data-stu-id="8542c-116">Instead, the WS-Management protocol sends SOAP messages and the service uses a single port for HTTP and a port for HTTPS transport.</span></span>

<span data-ttu-id="8542c-117">不同于 **winrm** 命令列工具，腳本必須提供傳遞給 WS-Management 通訊協定訊息所需的 XML。</span><span class="sxs-lookup"><span data-stu-id="8542c-117">Unlike the **winrm** command-line tool, scripts must provide the XML required to pass to the WS-Management protocol messages.</span></span> <span data-ttu-id="8542c-118">它們也必須提供 Uri。</span><span class="sxs-lookup"><span data-stu-id="8542c-118">They must also provide URIs.</span></span> <span data-ttu-id="8542c-119">如需詳細資訊，請參閱 [資源 uri](resource-uris.md) 和 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="8542c-119">For more information, see [Resource URIs](resource-uris.md) and [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="8542c-120">WMI 腳本 API 適用于物件（例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例），代表電腦上的資源。</span><span class="sxs-lookup"><span data-stu-id="8542c-120">The WMI Scripting API works with objects, such as instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which represent resources on a computer.</span></span> <span data-ttu-id="8542c-121">此 WMI 類別定義于 [*受控物件格式 (MOF)*](/windows/desktop/WmiSdk/gloss-m) 檔中，這些檔案會以二進位格式儲存在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="8542c-121">This WMI class is defined in [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) files, which are stored in binary form in the WMI repository.</span></span> <span data-ttu-id="8542c-122">在 WMI 中，單一資源或查詢有多個實例的 Get 作業會傳回 WMI 物件。</span><span class="sxs-lookup"><span data-stu-id="8542c-122">In WMI, a Get operation for a single resource or a query for multiple instances returns WMI objects.</span></span>

<span data-ttu-id="8542c-123">WinRM 腳本不會傳回物件，而是 XML 文字的資料流程。</span><span class="sxs-lookup"><span data-stu-id="8542c-123">A WinRM script does not return objects, but rather streams of XML text.</span></span> <span data-ttu-id="8542c-124">如需詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="8542c-124">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="8542c-125">顯示 WinRM 腳本的 XML 輸出</span><span class="sxs-lookup"><span data-stu-id="8542c-125">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="8542c-126">WinRM 腳本 API 會取得並接收描述資源的 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="8542c-126">The WinRM Scripting API gets and receives XML strings that describe resources.</span></span> <span data-ttu-id="8542c-127">結果 XML 的格式為文字資料流程，需要以其他方式來顯示 XML 轉換。</span><span class="sxs-lookup"><span data-stu-id="8542c-127">The resultant XML is in the form of a text stream and requires an XML transform to be displayed in some other way.</span></span>

<span data-ttu-id="8542c-128">下列 WinRM 腳本會產生原始 XML 輸出。</span><span class="sxs-lookup"><span data-stu-id="8542c-128">The following WinRM script produces raw XML output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



<span data-ttu-id="8542c-129">下列文字區塊顯示 WinRM 腳本的 XML 輸出。</span><span class="sxs-lookup"><span data-stu-id="8542c-129">The following block of text shows the XML output from the WinRM script.</span></span>


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



<span data-ttu-id="8542c-130">您的腳本可以使用 XML 轉換，讓此輸出更容易讀取。</span><span class="sxs-lookup"><span data-stu-id="8542c-130">Your scripts can use an XML transform to make this output more readable.</span></span> <span data-ttu-id="8542c-131">如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="8542c-131">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="8542c-132">下列版本的腳本會將 XML 格式化為人們可讀取的輸出。</span><span class="sxs-lookup"><span data-stu-id="8542c-132">The following version of the script formats the XML into human-readable output.</span></span>


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



<span data-ttu-id="8542c-133">XSL 轉換會建立下列輸出。</span><span class="sxs-lookup"><span data-stu-id="8542c-133">The XSL transform creates the following output.</span></span>


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



## <a name="winrm-script-and-winrmcmd-output"></a><span data-ttu-id="8542c-134">WinRM 腳本和 Winrm .cmd 輸出</span><span class="sxs-lookup"><span data-stu-id="8542c-134">WinRM Script and Winrm.cmd Output</span></span>

<span data-ttu-id="8542c-135">WinRM 腳本的輸出會以 Unicode 編碼。</span><span class="sxs-lookup"><span data-stu-id="8542c-135">The output from a WinRM script is encoded in Unicode.</span></span> <span data-ttu-id="8542c-136">如果您建立 [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) 並從腳本寫入檔案，則產生的檔案為 Unicode。</span><span class="sxs-lookup"><span data-stu-id="8542c-136">If you create a [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) and write a file from the script, the resulting file is Unicode.</span></span> <span data-ttu-id="8542c-137">但是，如果您將輸出重新導向至檔案，則編碼為 ANSI。</span><span class="sxs-lookup"><span data-stu-id="8542c-137">However, if you redirect the output to a file, the encoding is ANSI.</span></span> <span data-ttu-id="8542c-138">如果您將輸出重新導向至 XML 檔案，而且輸出中有 Unicode 字元，XML 將會無效。</span><span class="sxs-lookup"><span data-stu-id="8542c-138">If you redirect the output to an XML file and there are Unicode characters in the output, the XML will be invalid.</span></span> <span data-ttu-id="8542c-139">請注意， **Winrm** 命令列工具會輸出 ANSI。</span><span class="sxs-lookup"><span data-stu-id="8542c-139">Be aware that the **Winrm** command-line tool outputs ANSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8542c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="8542c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8542c-141">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="8542c-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="8542c-142">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="8542c-142">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

<span data-ttu-id="8542c-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8542c-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8542c-144">[DOM 參考](/previous-versions/windows/desktop/ms764730(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8542c-144">[DOM Reference](/previous-versions/windows/desktop/ms764730(v=vs.85))</span></span>
</dt> </dl>

 

 