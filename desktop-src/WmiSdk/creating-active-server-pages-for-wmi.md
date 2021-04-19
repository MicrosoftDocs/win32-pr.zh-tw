---
description: 說明如何建立 Microsoft Active Server Pages (ASP) ，將遠端電腦的相關資訊顯示到未安裝 WMI 的電腦。
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: 建立 WMI 的 Active Server Pages
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52143284be54868d36b55a6dd86e0b49c82d863d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983930"
---
# <a name="creating-active-server-pages-for-wmi"></a><span data-ttu-id="40817-103">建立 WMI 的 Active Server Pages</span><span class="sxs-lookup"><span data-stu-id="40817-103">Creating Active Server Pages for WMI</span></span>

<span data-ttu-id="40817-104">Microsoft Active Server Pages (ASP) 可以同時包含伺服器端和用戶端腳本，藉此建立動態網頁。</span><span class="sxs-lookup"><span data-stu-id="40817-104">Microsoft Active Server Pages (ASP) can create dynamic webpages by including both server-side and client-side scripts.</span></span> <span data-ttu-id="40817-105">ASP 頁面的速度會比用戶端 HTML 網頁快許多，因為大部分的工作都是在伺服器上完成。</span><span class="sxs-lookup"><span data-stu-id="40817-105">ASP pages can be much faster than client HTML pages because most of the work is done on the server.</span></span> <span data-ttu-id="40817-106">您也可以使用 ASP 頁面，將遠端電腦的相關資訊顯示到未安裝 Windows Management Instrumentation (WMI) 的其他電腦。</span><span class="sxs-lookup"><span data-stu-id="40817-106">You can also use ASP pages to display information about remote computers to other computers that do not have Windows Management Instrumentation (WMI) installed.</span></span>

<span data-ttu-id="40817-107">下列程式說明如何搭配使用 WMI 與 ASP。</span><span class="sxs-lookup"><span data-stu-id="40817-107">The following procedure describes how to use WMI with ASP.</span></span>

<span data-ttu-id="40817-108">**使用 WMI 搭配 ASP**</span><span class="sxs-lookup"><span data-stu-id="40817-108">**To use WMI with ASP**</span></span>

1.  <span data-ttu-id="40817-109">撰寫使用 WMI 的 ASP 網頁 ( .asp) ，並將它放在 web 伺服器可存取的目錄中。</span><span class="sxs-lookup"><span data-stu-id="40817-109">Write an ASP page (.asp) that uses WMI, and place it in a directory accessible to your web server.</span></span>

    <span data-ttu-id="40817-110">您可以使用數種指令碼語言（包括 VBScript）來開發 WMI 的 ASP 腳本。</span><span class="sxs-lookup"><span data-stu-id="40817-110">ASP scripts for WMI can be developed with several scripting languages, including VBScript.</span></span> <span data-ttu-id="40817-111">您可以建立 ASP 頁面的 WMI 腳本部分，就像是使用 WMI 來建立任何其他使用 WMI 的腳本一樣，有一個重要的限制：您無法在 ASP 頁面內使用非同步 WMI 方法。</span><span class="sxs-lookup"><span data-stu-id="40817-111">You can construct the WMI script part of an ASP page exactly as you construct any other script that uses WMI, with one important restriction: you cannot use asynchronous WMI methods within ASP pages.</span></span> <span data-ttu-id="40817-112">另請注意，對 **GetObject** 或 **CreateObject** 的任何呼叫都必須在伺服器端程式碼中。</span><span class="sxs-lookup"><span data-stu-id="40817-112">Note also that any calls to **GetObject** or **CreateObject** must be in the server-side code.</span></span> <span data-ttu-id="40817-113">如需詳細資訊，請參閱 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="40817-113">For more information, see [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="40817-114">設定 Internet Information Services (IIS) 的驗證設定。</span><span class="sxs-lookup"><span data-stu-id="40817-114">Set up authentication configuration for Internet Information Services (IIS).</span></span> <span data-ttu-id="40817-115">如需詳細資訊，請參閱 [針對 WMI ASP 腳本設定 IIS 5 和更新版本](configuring-iis-5-for-wmi-asp-scripting.md)。</span><span class="sxs-lookup"><span data-stu-id="40817-115">For more information, see [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>
3.  <span data-ttu-id="40817-116">停用匿名存取，並啟用 ASP 檔案的 Windows 整合式驗證。</span><span class="sxs-lookup"><span data-stu-id="40817-116">Disable anonymous access, and enable Windows Integrated Authentication for the ASP file.</span></span> <span data-ttu-id="40817-117">您可以使用位於 **主控台**[系統 **管理工具**] 資料夾中的 IIS 嵌入式管理單元，來設定 ASP 頁面的這些設定。</span><span class="sxs-lookup"><span data-stu-id="40817-117">You can configure these settings for your ASP page by using the IIS snap-in located in the **Administrative Tools** folder of the **Control Panel**.</span></span>

## <a name="wmi-asp-page-example"></a><span data-ttu-id="40817-118">WMI ASP 頁面範例</span><span class="sxs-lookup"><span data-stu-id="40817-118">WMI ASP Page Example</span></span>

<span data-ttu-id="40817-119">下列範例會使用 Active Server 頁面中的 Windows Management Instrumentation (WMI)  (ASP) ，以顯示執行此腳本之伺服器的 IP 位址和預設 IP 閘道設定。</span><span class="sxs-lookup"><span data-stu-id="40817-119">The following example uses Windows Management Instrumentation (WMI) within an Active Server Page (ASP) to display the IP address and default IP gateway settings for the server from which this script is executed.</span></span>


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 



