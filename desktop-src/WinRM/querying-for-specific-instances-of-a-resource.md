---
title: 查詢資源的特定實例
description: 呼叫 Session. 列舉具有可將列舉範圍縮小為查詢的選擇性參數。
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966862"
---
# <a name="querying-for-specific-instances-of-a-resource"></a><span data-ttu-id="e1828-103">查詢資源的特定實例</span><span class="sxs-lookup"><span data-stu-id="e1828-103">Querying for Specific Instances of a Resource</span></span>

<span data-ttu-id="e1828-104">呼叫 [**Session. 列舉**](session-enumerate.md) 具有可將列舉範圍縮小為查詢的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="e1828-104">The call to [**Session.Enumerate**](session-enumerate.md) has optional parameters that narrow the enumeration into a query.</span></span> <span data-ttu-id="e1828-105">由於 [Winrm 腳本 api](winrm-scripting-api.md) 和 [Winrm c + + API](winrm-c---api.md) 是以基礎 WS-Management 通訊協定為基礎，因此參數會使用與用來查詢通訊協定（*篩選* 和 *篩選方言*）相同的術語。</span><span class="sxs-lookup"><span data-stu-id="e1828-105">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) are closely modeled on the underlying WS-Management protocol, the parameters use the same terminology for querying as the protocol—*filter* and *filter dialect*.</span></span>

<span data-ttu-id="e1828-106">您可以使用 [**Session**](session-enumerate.md) 的篩選和方言參數，也可以建立並提供 [**ResourceLocator**](resourcelocator.md) 物件和 [**AddSelector**](resourcelocator-addselector.md) 方法，但不能同時執行這兩者。</span><span class="sxs-lookup"><span data-stu-id="e1828-106">You can either use the filter and dialect parameters of [**Session.Enumerate**](session-enumerate.md) or you can construct and supply a [**ResourceLocator**](resourcelocator.md) object and the [**AddSelector**](resourcelocator-addselector.md) method, but you cannot do both.</span></span>

<span data-ttu-id="e1828-107">此程式會針對已系結 TCP/IP 和啟用的網路介面卡執行查詢。</span><span class="sxs-lookup"><span data-stu-id="e1828-107">This procedure executes a query for network adapters that have TCP/IP bound and enabled.</span></span> <span data-ttu-id="e1828-108">此查詢會要求將 **IpEnabled** 屬性設定為 **True** 的所有 [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)實例。</span><span class="sxs-lookup"><span data-stu-id="e1828-108">The query requests all the instances of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) that have the **IpEnabled** property set to **True**.</span></span> <span data-ttu-id="e1828-109">除了新增 *篩選* 和 *方言* 以外，查詢的處理方式類似簡單列舉。</span><span class="sxs-lookup"><span data-stu-id="e1828-109">Except for the addition of the *filter* and *dialect*, the query is handled like a simple enumeration.</span></span>

<span data-ttu-id="e1828-110">在此範例中，資源常數的資源名稱是以星號 "" 表示， \* 因為 *strFilter* 字串中已提及類別名稱（ [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)）。</span><span class="sxs-lookup"><span data-stu-id="e1828-110">In this example, the resource name for the Resource constant is represented by an asterisk "\*" because the class name, [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), is already mentioned in the *strFilter* string.</span></span>

<span data-ttu-id="e1828-111">**查詢資源的特定實例**</span><span class="sxs-lookup"><span data-stu-id="e1828-111">**To query for specific instances of a resource**</span></span>

1.  <span data-ttu-id="e1828-112">為了方便閱讀，請將 Uri 定義為常數。</span><span class="sxs-lookup"><span data-stu-id="e1828-112">For ease-of-reading, define URIs as constants.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  <span data-ttu-id="e1828-113">建立工作階段。</span><span class="sxs-lookup"><span data-stu-id="e1828-113">Create a session.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  <span data-ttu-id="e1828-114">建立篩選字串。</span><span class="sxs-lookup"><span data-stu-id="e1828-114">Construct the filter string.</span></span> <span data-ttu-id="e1828-115">Windows 遠端管理支援 [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) 做為篩選方言。</span><span class="sxs-lookup"><span data-stu-id="e1828-115">Windows Remote Management supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as the filter dialect.</span></span>

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  <span data-ttu-id="e1828-116">在 *旗標* 參數中設定任何必要的 [**列舉常數**](enumeration-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e1828-116">Set any required [**enumeration constants**](enumeration-constants.md) in the *flags* parameter.</span></span>

    <span data-ttu-id="e1828-117">請注意，如果旗標包含 [**列舉常數**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** 或 **WSManFlagHierarchyShallow** ，則 WinRM 服務會傳回 **\_ \_ \_ \_ 不支援** 的錯誤錯誤碼錯誤的 WSMAN 多型模式。</span><span class="sxs-lookup"><span data-stu-id="e1828-117">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then WinRM service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

5.  <span data-ttu-id="e1828-118">呼叫 [**Session。列舉**](session-enumerate.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e1828-118">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="e1828-119">此呼叫會啟動列舉。</span><span class="sxs-lookup"><span data-stu-id="e1828-119">This call starts an enumeration.</span></span> <span data-ttu-id="e1828-120">**Session** 方法會建立 WS-Management 的通訊協定列舉內容，並保留在 [**列舉**](enumerator.md)值物件中。</span><span class="sxs-lookup"><span data-stu-id="e1828-120">The **Session.Enumerate** method establishes a WS-Management protocol enumeration context, maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  <span data-ttu-id="e1828-121">呼叫 [**ReadItem**](enumerator-readitem.md) 方法，以取得結果的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="e1828-121">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="e1828-122">在 WS-Management 通訊協定中，這會對應至提取作業。</span><span class="sxs-lookup"><span data-stu-id="e1828-122">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="e1828-123">使用 [**AtEndOfStream**](enumerator-atendofstream.md) 方法做為控制項，以瞭解何時停止讀取。</span><span class="sxs-lookup"><span data-stu-id="e1828-123">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

<span data-ttu-id="e1828-124">下列 VBScript 程式碼範例顯示完整的腳本。</span><span class="sxs-lookup"><span data-stu-id="e1828-124">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
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



## <a name="related-topics"></a><span data-ttu-id="e1828-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1828-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1828-126">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="e1828-126">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="e1828-127">列舉或列出資源的所有實例</span><span class="sxs-lookup"><span data-stu-id="e1828-127">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="e1828-128">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="e1828-128">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 