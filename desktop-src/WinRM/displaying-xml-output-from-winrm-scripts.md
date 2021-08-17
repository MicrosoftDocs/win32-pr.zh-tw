---
title: 顯示 WinRM 腳本的 XML 輸出
description: Windows遠端系統管理腳本會傳回 XML 而非物件。 XML 不是人類看得懂的格式。 您可以使用 MSXML API 的方法和預先安裝的 XSL 檔案，將資料轉換成人類看得懂的格式。
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df5c27c1fe22ae87395357aeefe681af7c041420d32b7bccbf595fab38bb060b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680018"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>顯示 WinRM 腳本的 XML 輸出

Windows遠端系統管理腳本會傳回 XML 而非物件。 XML 不是人類看得懂的格式。 您可以使用[MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API 的方法和預先安裝的 XSL 檔案，將資料轉換成人類看得懂的格式。

如需 WinRM xml 輸出和 raw 和格式化 XML 範例的詳細資訊，請參閱[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)。

**Winrm** 命令列工具隨附名為 WsmTxt 的轉換檔案，會以表格形式顯示輸出。 如果您的腳本將此檔案提供給執行會將的 MSXML 方法，則輸出會與 **Winrm** 工具的輸出相同。

**格式化原始 XML 輸出**

1.  建立 [**WSMan**](wsman.md) 物件並建立會話。

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  建立 MSXML 物件，代表 XML 回應輸出和 XSL 轉換。

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  透過 [**會話**](session.md) 物件方法取得資料。

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  提供 MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85))方法的回應，以及用來儲存轉換檔案的[load](/previous-versions/windows/desktop/ms762722(v=vs.85))方法。

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  使用 MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85))方法，並顯示或儲存輸出。

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

下列 VBScript 程式碼範例顯示完整的腳本。


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>新增可移植的副程式以將 XML 轉換成您的腳本

您可以將副程式新增至腳本，以使用預先安裝的 XSL 檔案，將未經處理的 XML 輸出從 WinRM 腳本轉換成表格式格式。

下列副程式會使用 MSXML 腳本方法的呼叫，將輸出提供給 WsmTxt。


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



下列副程式會轉換資料的每一行，如下列範例所示。


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
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

[Windows遠端系統管理參考](windows-remote-management-reference.md)
</dt> </dl>

 

 