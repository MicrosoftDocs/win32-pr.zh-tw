---
title: 從遠端電腦取得資料
description: 您可以取得資料或管理遠端電腦和本機電腦上的資源。 連接到 Windows 遠端管理腳本中的遠端電腦，與進行本機連接的方式非常類似。
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842316"
---
# <a name="obtaining-data-from-a-remote-computer"></a><span data-ttu-id="4a2e7-104">從遠端電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="4a2e7-104">Obtaining Data from a Remote Computer</span></span>

<span data-ttu-id="4a2e7-105">您可以取得資料或管理遠端電腦和本機電腦上的資源。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-105">You can obtain data or manage resources on remote computers as well as the local computer.</span></span> <span data-ttu-id="4a2e7-106">連接到 Windows 遠端管理腳本中的遠端電腦，與進行本機連接的方式非常類似。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-106">Connecting to a remote computer in a Windows Remote Management script is very similar to making a local connection.</span></span> <span data-ttu-id="4a2e7-107">WMI 實例資料可供使用，而且如果遠端電腦具有可使用 WS-Management 通訊協定進行通訊的 BMC 硬體，則也可以使用 [智慧型平臺管理介面 (的 IPMI) ](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) 資料。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-107">WMI instance data is available and, if the remote computer has BMC hardware that can communicate using the WS-Management protocol, then [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) data is also available.</span></span> <span data-ttu-id="4a2e7-108">如需詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md) 和 [遠端硬體管理](remote-hardware-management.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-108">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md) and [Remote Hardware Management](remote-hardware-management.md).</span></span>

<span data-ttu-id="4a2e7-109">您可能需要建立 [**ConnectionOptions**](connectionoptions.md) 物件，以指定登入所要求之驗證類型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-109">You may need to create a [**ConnectionOptions**](connectionoptions.md) object to specify information about the type of authentication requested for the logon.</span></span>

<span data-ttu-id="4a2e7-110">如果遠端電腦上的帳戶具有相同的登入使用者名稱和密碼，則您需要的額外資訊是傳輸、功能變數名稱和電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-110">If the account on the remote computer has the same logon username and password, the only extra information you need is the transport, the domain name, and the computer name.</span></span> <span data-ttu-id="4a2e7-111">由於 [使用者帳戶控制 (UAC) ](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)，因此遠端帳戶必須是網域帳戶和遠端電腦系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-111">Because of [User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), the remote account must be a domain account and a member of the remote computer Administrators group.</span></span> <span data-ttu-id="4a2e7-112">如果帳戶是 Administrators 群組的本機電腦成員，則 UAC 不允許存取 WinRM 服務。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-112">If the account is a local computer member of the Administrators group, then UAC does not allow access to the WinRM service.</span></span> <span data-ttu-id="4a2e7-113">若要存取工作組中的遠端 WinRM 服務，必須藉由建立下列 DWORD 登錄專案，並將其值設定為1： **\[ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 原則 \\ 系統 \] LocalAccountTokenFilterPolicy**，來停用本機帳戶的 UAC 篩選。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-113">To access a remote WinRM service in a workgroup, UAC filtering for local accounts must be disabled by creating the following DWORD registry entry and setting its value to 1: **\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\] LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="4a2e7-114">**使用登入使用者名稱和密碼連接到遠端電腦**</span><span class="sxs-lookup"><span data-stu-id="4a2e7-114">**To connect to a remote computer using your logon username and password**</span></span>

1.  <span data-ttu-id="4a2e7-115">使用完整功能變數名稱或 IP 位址指定目的電腦，並將其指派給常數。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-115">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="4a2e7-116">如果指定了 IPv6 位址，則位址必須以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-116">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="4a2e7-117">建立 [**WSMan**](wsman.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  <span data-ttu-id="4a2e7-118">建立會話、指定傳輸、HTTP 或 HTTPS，然後將它與代表目的電腦的常數串連。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-118">Create the session, specifying the transport, HTTP or HTTPS, and concatenating it with the constant representing the target computer.</span></span>

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

<span data-ttu-id="4a2e7-119">下列 VBScript 程式碼範例顯示完整的腳本。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-119">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="4a2e7-120">此腳本包含一個副程式，可將資料從原始 XML 轉換為人們可讀取的格式。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-120">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="4a2e7-121">如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-121">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



<span data-ttu-id="4a2e7-122">**使用不同帳戶連接到遠端電腦**</span><span class="sxs-lookup"><span data-stu-id="4a2e7-122">**To connect to a remote computer using a different account**</span></span>

1.  <span data-ttu-id="4a2e7-123">使用完整功能變數名稱或 IP 位址指定目的電腦，並將其指派給常數。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-123">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="4a2e7-124">如果指定了 IPv6 位址，則位址必須以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-124">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="4a2e7-125">建立 [**WSMan**](wsman.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-125">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  <span data-ttu-id="4a2e7-126">呼叫 [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) 方法來建立 [**ConnectionOptions**](connectionoptions.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-126">Call the [**WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) method to create a [**ConnectionOptions**](connectionoptions.md) object.</span></span> <span data-ttu-id="4a2e7-127">遠端電腦上的帳戶必須是本機電腦系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-127">The account on the remote computer must be a member of the local computer administrators group.</span></span>

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  <span data-ttu-id="4a2e7-128">在 [**CreateSession**](wsman-createsession.md) 呼叫中，于 *flags* 參數中指定適當的會話連接旗標。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-128">On the [**WSman.CreateSession**](wsman-createsession.md) call, specify the appropriate session connection flags in the *flags* parameter.</span></span> <span data-ttu-id="4a2e7-129">如需詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-129">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="4a2e7-130">請使用完整的電腦名稱稱或 IP 位址和傳輸（HTTP 或 HTTPs）來指定目的電腦。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-130">Specify the target computer with a fully qualified computer name or an IP address and the transport—http or https.</span></span> <span data-ttu-id="4a2e7-131">此腳本會向遠端 WinRM 服務要求 [*Kerberos*](windows-remote-management-glossary.md) 驗證。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-131">This script requests [*Kerberos*](windows-remote-management-glossary.md) authentication from the remote WinRM service.</span></span>

    <span data-ttu-id="4a2e7-132">不同于 WMI 腳本，您可以在 WinRM 腳本中使用數種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-132">Unlike WMI scripts, you can use several methods of authentication in WinRM scripts.</span></span> <span data-ttu-id="4a2e7-133">如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-133">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  <span data-ttu-id="4a2e7-134">會話物件可供使用之後，您可以呼叫任何 [**會話**](session.md) 物件方法來取得資源的資料。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-134">After the session object is available, you can call any of the [**Session**](session.md) object methods to obtain data for a resource.</span></span> <span data-ttu-id="4a2e7-135">您可以針對正在執行會話的電腦取得可用資源的資料。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-135">You can get data for any resource that is available on the computer on which the session is running.</span></span> <span data-ttu-id="4a2e7-136">如需詳細資訊，請參閱 [從本機電腦取得資料](obtaining-data-from-the-local-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-136">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span>

<span data-ttu-id="4a2e7-137">下列 VBScript 程式碼範例顯示完整的腳本。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-137">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="4a2e7-138">此腳本包含一個副程式，可將資料從原始 XML 轉換為人們可讀取的格式。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-138">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="4a2e7-139">如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-139">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span> <span data-ttu-id="4a2e7-140">腳本會指定 Kerberos 驗證，但是如果遠端電腦是在工作組而非網域中，則指定 Kerberos 會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a2e7-140">The script specifies Kerberos authentication, but if the remote computer is in a workgroup rather than a domain, specifying Kerberos generates an error.</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="4a2e7-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a2e7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a2e7-142">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="4a2e7-142">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4a2e7-143">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="4a2e7-143">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4a2e7-144">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="4a2e7-144">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 