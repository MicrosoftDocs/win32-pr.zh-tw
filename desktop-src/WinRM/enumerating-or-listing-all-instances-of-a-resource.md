---
title: 列舉或列出資源的所有實例
description: Session 方法是取得指定資源之所有實例的 Windows 遠端管理方法。
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186052"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a><span data-ttu-id="ee339-103">列舉或列出資源的所有實例</span><span class="sxs-lookup"><span data-stu-id="ee339-103">Enumerating or Listing All Instances of a Resource</span></span>

<span data-ttu-id="ee339-104">[**Session**](session-enumerate.md)方法是取得指定資源之所有實例的 Windows 遠端管理方法。</span><span class="sxs-lookup"><span data-stu-id="ee339-104">The [**Session.Enumerate**](session-enumerate.md) method is the Windows Remote Management approach to obtaining all the instances of a specified resource.</span></span>

<span data-ttu-id="ee339-105">[**Session**](session-enumerate.md)方法不會在 [**swbemobjectset 搭配使用**](/windows/desktop/WmiSdk/swbemobjectset)物件中取得集合，例如使用 [WMI 查詢](/windows/desktop/WmiSdk/querying-wmi)作為參數的 [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery)呼叫 (例如 `ExecQuery("SELECT * from Win32_LogicalDisk")`) ，或 [**\_ 呼叫 SWbemObject**](/windows/desktop/WmiSdk/swbemobject-instances-)之類的方法。</span><span class="sxs-lookup"><span data-stu-id="ee339-105">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in a [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) object like a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) call with a [WMI query](/windows/desktop/WmiSdk/querying-wmi) as a parameter (for example, `ExecQuery("SELECT * from Win32_LogicalDisk")`), or a call to a method like [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span> <span data-ttu-id="ee339-106">**Session 和列舉**[**值物件方法**](enumerator.md)更類似于用來將檔案讀取為數據流的腳本 [TextStream](/previous-versions//312a5kbt(v=vs.85))物件作業。</span><span class="sxs-lookup"><span data-stu-id="ee339-106">**Session.Enumerate** and the [**Enumerator**](enumerator.md) object methods are much more similar to the operation of the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object that is used for reading files as a stream.</span></span>

<span data-ttu-id="ee339-107">若要將檔案讀取為文字資料流程，您必須建立腳本 [TextStream](/previous-versions//312a5kbt(v=vs.85)) 物件，並呼叫 [TextStream](/previous-versions//h7se9d4f(v=vs.85)) 方法來讀取檔案的每一行。</span><span class="sxs-lookup"><span data-stu-id="ee339-107">To read files as a text stream, you must create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="ee339-108">以類似的方式，您可以呼叫 [**Session。列舉**](session-enumerate.md) 方法以 [**取得列舉值物件，**](enumerator.md) 並呼叫 [**ReadItem**](enumerator-readitem.md) 方法來取得下一個專案。</span><span class="sxs-lookup"><span data-stu-id="ee339-108">In a similar way, you can call the [**Session.Enumerate**](session-enumerate.md) method to obtain an [**Enumerator**](enumerator.md) object and call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to get the next item.</span></span> <span data-ttu-id="ee339-109">就像從文字檔讀取的情況一樣，您可以呼叫 [**AtEndOfStream**](enumerator-atendofstream.md) 屬性來檢查是否已到達資料項目的結尾。</span><span class="sxs-lookup"><span data-stu-id="ee339-109">As is the case when reading from the text file, you can call the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

<span data-ttu-id="ee339-110">**列舉資源**</span><span class="sxs-lookup"><span data-stu-id="ee339-110">**To enumerate a resource**</span></span>

1.  <span data-ttu-id="ee339-111">建立工作階段。</span><span class="sxs-lookup"><span data-stu-id="ee339-111">Create a session.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  <span data-ttu-id="ee339-112">建立用來識別資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="ee339-112">Construct the URI to identify the resource.</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  <span data-ttu-id="ee339-113">呼叫 [**Session。列舉**](session-enumerate.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ee339-113">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="ee339-114">此呼叫會啟動列舉。</span><span class="sxs-lookup"><span data-stu-id="ee339-114">This call starts an enumeration.</span></span> <span data-ttu-id="ee339-115">在 WinRM 中，列舉作業不會以與 WMI 相同的方式取得集合。</span><span class="sxs-lookup"><span data-stu-id="ee339-115">In WinRM, an enumeration operation does not obtain a collection in the same way that WMI does.</span></span> <span data-ttu-id="ee339-116">相反地， **Session** 方法會建立在 [**列舉**](enumerator.md) 值物件中維護的 WS-Management 通訊協定列舉內容。</span><span class="sxs-lookup"><span data-stu-id="ee339-116">Instead, the **Session.Enumerate** method establishes a WS-Management protocol enumeration context that is maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  <span data-ttu-id="ee339-117">呼叫 [**ReadItem**](enumerator-readitem.md) 方法，以取得結果的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="ee339-117">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="ee339-118">在 WS-Management 通訊協定中，這會對應至提取作業。</span><span class="sxs-lookup"><span data-stu-id="ee339-118">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="ee339-119">使用 [**AtEndOfStream**](enumerator-atendofstream.md) 方法做為控制項，以瞭解何時停止讀取。</span><span class="sxs-lookup"><span data-stu-id="ee339-119">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

<span data-ttu-id="ee339-120">下列 VBScript 程式碼範例顯示完整的腳本。</span><span class="sxs-lookup"><span data-stu-id="ee339-120">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="ee339-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee339-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee339-122">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="ee339-122">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ee339-123">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="ee339-123">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ee339-124">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="ee339-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 