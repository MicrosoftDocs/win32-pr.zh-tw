---
title: 顯示 WinRM 腳本的 XML 輸出
description: Windows 遠端管理腳本會傳回 XML 而非物件。 XML 不是人類看得懂的格式。 您可以使用 MSXML API 的方法和預先安裝的 XSL 檔案，將資料轉換成人類看得懂的格式。
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023869"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="5d2b6-105">顯示 WinRM 腳本的 XML 輸出</span><span class="sxs-lookup"><span data-stu-id="5d2b6-105">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="5d2b6-106">Windows 遠端管理腳本會傳回 XML 而非物件。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-106">Windows Remote Management scripts return XML rather than objects.</span></span> <span data-ttu-id="5d2b6-107">XML 不是人類看得懂的格式。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-107">The XML is not in a human-readable format.</span></span> <span data-ttu-id="5d2b6-108">您可以使用 [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API 的方法和預先安裝的 XSL 檔案，將資料轉換成人類看得懂的格式。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API and the preinstalled XSL file to transform the data into human-readable format.</span></span>

<span data-ttu-id="5d2b6-109">如需 WinRM XML 輸出和 raw 和格式化 XML 範例的詳細資訊，請參閱 [Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-109">For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="5d2b6-110">**Winrm** 命令列工具隨附名為 WsmTxt 的轉換檔案，會以表格形式顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-110">The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form.</span></span> <span data-ttu-id="5d2b6-111">如果您的腳本將此檔案提供給執行會將的 MSXML 方法，則輸出會與 **Winrm** 工具的輸出相同。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-111">If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.</span></span>

<span data-ttu-id="5d2b6-112">**格式化原始 XML 輸出**</span><span class="sxs-lookup"><span data-stu-id="5d2b6-112">**To format raw XML output**</span></span>

1.  <span data-ttu-id="5d2b6-113">建立 [**WSMan**](wsman.md) 物件並建立會話。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-113">Create the [**WSMan**](wsman.md) object and create a session.</span></span>

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  <span data-ttu-id="5d2b6-114">建立代表 XML 回應輸出和 XSL 轉換的 MSXML 物件。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-114">Create MSXML objects that represent the XML response output and the XSL transform.</span></span>

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  <span data-ttu-id="5d2b6-115">透過 [**會話**](session.md) 物件方法取得資料。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-115">Obtain data through [**Session**](session.md) object methods.</span></span>

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  <span data-ttu-id="5d2b6-116">提供 MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) 方法的回應，以及用來儲存轉換檔案的 [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) 方法。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-116">Supply the response to the MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) method and the [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) method to store the transform file.</span></span>

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  <span data-ttu-id="5d2b6-117">使用 MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) 方法，並顯示或儲存輸出。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-117">Use the MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) method and display or save the output.</span></span>

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

<span data-ttu-id="5d2b6-118">下列 VBScript 程式碼範例顯示完整的腳本。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-118">The following VBScript code example shows the complete script.</span></span>


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a><span data-ttu-id="5d2b6-119">新增可移植的副程式以將 XML 轉換成您的腳本</span><span class="sxs-lookup"><span data-stu-id="5d2b6-119">Adding a Portable Subroutine to Transform XML to Your Scripts</span></span>

<span data-ttu-id="5d2b6-120">您可以將副程式新增至腳本，以使用預先安裝的 XSL 檔案，將未經處理的 XML 輸出從 WinRM 腳本轉換成表格式格式。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-120">You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.</span></span>

<span data-ttu-id="5d2b6-121">下列副程式會使用 MSXML 腳本方法的呼叫，將輸出提供給 WsmTxt。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-121">The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.</span></span>


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



<span data-ttu-id="5d2b6-122">下列副程式會轉換資料的每一行，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="5d2b6-122">The following subroutine transforms each line of your data as shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5d2b6-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d2b6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d2b6-124">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="5d2b6-124">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="5d2b6-125">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="5d2b6-125">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="5d2b6-126">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="5d2b6-126">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 