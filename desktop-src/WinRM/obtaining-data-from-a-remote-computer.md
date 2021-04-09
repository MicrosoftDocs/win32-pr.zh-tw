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
# <a name="obtaining-data-from-a-remote-computer"></a>從遠端電腦取得資料

您可以取得資料或管理遠端電腦和本機電腦上的資源。 連接到 Windows 遠端管理腳本中的遠端電腦，與進行本機連接的方式非常類似。 WMI 實例資料可供使用，而且如果遠端電腦具有可使用 WS-Management 通訊協定進行通訊的 BMC 硬體，則也可以使用 [智慧型平臺管理介面 (的 IPMI) ](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) 資料。 如需詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md) 和 [遠端硬體管理](remote-hardware-management.md)。

您可能需要建立 [**ConnectionOptions**](connectionoptions.md) 物件，以指定登入所要求之驗證類型的相關資訊。

如果遠端電腦上的帳戶具有相同的登入使用者名稱和密碼，則您需要的額外資訊是傳輸、功能變數名稱和電腦名稱稱。 由於 [使用者帳戶控制 (UAC) ](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)，因此遠端帳戶必須是網域帳戶和遠端電腦系統管理員群組的成員。 如果帳戶是 Administrators 群組的本機電腦成員，則 UAC 不允許存取 WinRM 服務。 若要存取工作組中的遠端 WinRM 服務，必須藉由建立下列 DWORD 登錄專案，並將其值設定為1： **\[ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 原則 \\ 系統 \] LocalAccountTokenFilterPolicy**，來停用本機帳戶的 UAC 篩選。

**使用登入使用者名稱和密碼連接到遠端電腦**

1.  使用完整功能變數名稱或 IP 位址指定目的電腦，並將其指派給常數。 如果指定了 IPv6 位址，則位址必須以方括弧括住。

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  建立 [**WSMan**](wsman.md) 物件。

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  建立會話、指定傳輸、HTTP 或 HTTPS，然後將它與代表目的電腦的常數串連。

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

下列 VBScript 程式碼範例顯示完整的腳本。 此腳本包含一個副程式，可將資料從原始 XML 轉換為人們可讀取的格式。 如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。


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



**使用不同帳戶連接到遠端電腦**

1.  使用完整功能變數名稱或 IP 位址指定目的電腦，並將其指派給常數。 如果指定了 IPv6 位址，則位址必須以方括弧括住。

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  建立 [**WSMan**](wsman.md) 物件。

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  呼叫 [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) 方法來建立 [**ConnectionOptions**](connectionoptions.md) 物件。 遠端電腦上的帳戶必須是本機電腦系統管理員群組的成員。

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  在 [**CreateSession**](wsman-createsession.md) 呼叫中，于 *flags* 參數中指定適當的會話連接旗標。 如需詳細資訊，請參閱 [會話常數](session-constants.md)。 請使用完整的電腦名稱稱或 IP 位址和傳輸（HTTP 或 HTTPs）來指定目的電腦。 此腳本會向遠端 WinRM 服務要求 [*Kerberos*](windows-remote-management-glossary.md) 驗證。

    不同于 WMI 腳本，您可以在 WinRM 腳本中使用數種驗證方法。 如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  會話物件可供使用之後，您可以呼叫任何 [**會話**](session.md) 物件方法來取得資源的資料。 您可以針對正在執行會話的電腦取得可用資源的資料。 如需詳細資訊，請參閱 [從本機電腦取得資料](obtaining-data-from-the-local-computer.md)。

下列 VBScript 程式碼範例顯示完整的腳本。 此腳本包含一個副程式，可將資料從原始 XML 轉換為人們可讀取的格式。 如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。 腳本會指定 Kerberos 驗證，但是如果遠端電腦是在工作組而非網域中，則指定 Kerberos 會產生錯誤。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理參考](windows-remote-management-reference.md)
</dt> </dl>

 

 